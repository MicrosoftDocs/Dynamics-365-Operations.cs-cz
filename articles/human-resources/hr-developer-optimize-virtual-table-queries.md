---
title: Optimalizace dotazů virtuálních tabulek Dataverse
description: Optimalizace a řešení problémů s výkonem dotazů virtuální tabulky Dataverse
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 40fc4c06c563415cd5b1a13c145b778276274fd97279dc9f56ff5e3f8954dc76
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732002"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Optimalizace dotazů virtuálních tabulek Dataverse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Výdej

### <a name="overview"></a>Přehled

Při použití virtuálních tabulek Dataverse k vývoji integrací a dalších datových připojení s Dynamics 365 Human Resources můžete narazit na problémy s výkonem při dotazech na virtuální tabulky. Pomalé provádění dotazů může nastat u různých klientů nebo rozhraní. Například k problému může dojít za následujících okolností:

- Při dotazování na virtuální tabulku prostřednictvím webového rozhraní API Dataverse
- Při vytváření aplikace Power App proti virtuální tabulce
- Při tvorbě sestavy Power BI na virtuální tabulce

Všechna tato rozhraní mají potenciál překonat problém s výkonem.

Jednou z příčin pomalého výkonu s virtuálními tabulkami Dataverse pro lidské zdroje jsou sloupce cizího klíče virtuální tabulky související s [vlastnostmi navigace](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) tabulky. Když jsou pro virtuální tabulku vytvořeny navigační vlastnosti, do tabulky se automaticky přidá sloupec cizího klíče, který představuje hodnotu klíče pro sloupec klíče související virtuální tabulky. Například sloupec **_mshr_fk_person_id_value** je přidán do entity **mshr_hcmworkerbaseentity** s vlastností cizího klíče z entity **mshr_dirpersonentity**. Z důvodu toho, jak jsou hodnoty pro tyto sloupce cizích klíčů udržovány v tabulce, může mít načítání hodnot negativní dopad na výkon dotazu vůči virtuální tabulce.

### <a name="potential-symptoms"></a>Možné příznaky

Příklad, kde můžete vidět tento dopad, je v dotazech proti entitě pracovník (**mshr_hcmworkerentity**) nebo základní pracovník (**mshr_hcmworkerbaseentity**). Problém s výkonem se může projevit několika různými způsoby:

- **Pomalé provádění dotazu**: Dotaz na virtuální tabulku může vrátit očekávané výsledky, ale provedení dotazu trvá déle, než se očekávalo.
- **Časový limit dotazu**: Dotaz může vypršet a vrátit následující chybu: „Byl získán token pro volání Finance and Operations, ale Finance and Operations vrátil chybu typu InternalServerError.“
- **Neočekávaná chyba** : Dotaz může vrátit chybu typu 400 s následující zprávou: „Došlo k neočekávané chybě.“

  ![Typ chyby 400 na HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType400.png)

- **Omezování**: Dotaz může nadužívat prostředky serveru a podléhat omezením. V tomto případě dotaz vrátí následující chybu: „Byl získán token pro volání Finance and Operations, ale Finance and Operations vrátil chybu typu 429.“ Další informace o omezení v v Human Resources najdete v tématu [Časté otázky k omezování](./hr-admin-integration-throttling-faq.md).

  ![Typ chyby 429 na HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Řešení

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Omezte počet sloupců obsažených v dotazu na data

U virtuálních tabulek je jednou z metod s největším potenciálem pro zlepšení výkonu dotazu omezení počtu sloupců vybraných v dotazu. Obecným návodem pro optimalizaci výkonu dotazu je omezení sloupců vrácených v dotazu pouze na ty vlastnosti, které potřebujete. To platí zejména u sloupců cizích klíčů na virtuálních tabulkách. Pokud nepotřebujete hodnoty ve sloupcích cizího klíče pro vaši integraci nebo sestavu, strukturujte dotaz tak, aby vybral pouze ty sloupce, které potřebujete, bez sloupců cizího klíče.

#### <a name="selecting-columns-in-an-odata-query"></a>Výběr sloupců v dotazu OData

Při dotazování na virtuální tabulku prostřednictvím webového rozhraní API Dataverse můžete omezit počet sloupců zahrnutých v dotazu pomocí možnosti systémového dotazu **$select** a definice sloupců, pro které chcete vrátit výsledky. Chcete-li maximalizovat výkon, vylučte sloupce cizího klíče (ty s předponou **_mshr_FK_**) z dotazu.

Například následující dotaz proti entitě **mshr_hcmworkerbaseentity** bude zahrnovat pouze sloupce obsažené ve výrazu možnosti dotazu **$select** bez hodnot cizího klíče. To poskytuje významné zlepšení výkonu oproti dotazu, který zahrnuje všechny sloupce tabulky.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Doporučení omezit počet vybraných sloupců platí také při použití možnost dotazu **$expand** dotazu k rozšíření dotazu na související virtuální tabulky prostřednictvím navigačních vlastností. Například následující dotaz obsahuje sloupce z entity **mshr_hcmworkerbaseentity** s rozšířenými sloupci z entity **mshr_dirpersonentity**. Možnost dotazu **$select** je také zahrnuta ve výrazu možnosti dotazu **$expand**.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Při použití této metody načítání dat pomocí možnosti dotazu **$select** ve výrazu možnosti dotazu **$select** obvykle uvidíte větší vylepšení výkonu, když je vlastnost navigace mezi entitami vztahem více : jedna. Při rozšiřování vztahu jedna k více se nemusíte setkat se stejným zkrácením doby provedení dotazu. Další informace o definici vztahu pro virtuální tabulky Dataverse, viz [Vztahy mezi tabulkami](/powerapps/maker/data-platform/create-edit-entity-relationships).

Další informace o používání možností systémového dotazu **$select** a **$expand** ve webovém rozhraní API Dataverse viz [Načíst související záznamy entit pomocí dotazu](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Výběr sloupců v Power BI

Pokud narazíte na některý z výše uvedených náznaků pomalého výkonu při sestavování sestavy Power BI proti virtuální tabulce Dataverse, můžete zlepšit výkon vyloučením sloupců cizího klíče ze sloupců vybraných z tabulky pro sestavu. Například pokud používáte Power BI Desktop k vytvoření sestavy proti entitě **mshr_hcmworkerbaseentity**, můžete pomocí následujících kroků vybrat sloupce, které chcete zahrnout do dotazu na sestavu.

1. V Power BI Desktop vyberte **Více...** z rozevíracího seznamu **Získat data** na pásu karet akcí.
2. Do okna **Získat data** zadejte do vyhledávacího pole **Common Data Service**, vyberte konektor **Common Data Service** a vyberte **Připojit**.
3. Do pole **URL serveru** okna Common Data Service zadejte URI organizace pro vaše prostředí Dataverse a vyberte **OK**.
  
   ![Zadejte URI pro prostředí Dataverse.](./media/PowerBIDataverseURLSetup.png)
  
4. V okně Navigátor rozbalte uzel **Entity**.
5. Do vyhledávacího pole zadejte **mshr_hcmworkerbaseentity** a vyberte entitu.
6. Vyberte možnost **Transformovat data**.
7. V okně Editoru Power Query vyberte **Rozšířený editor**.
8. V okně **Rozšířený editor** aktualizujte dotaz tak, aby vypadal jako dotaz níže, podle potřeby přidejte nebo odeberte sloupce v poli.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Aktualizujte dotaz v Rozšířeném editoru pro editor Power Query.](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. Vyberte **Hotovo**.

   > [!NOTE]
   > Pokud jste předtím obdrželi chybu typu 429 z dotazu před aktualizací, možná budete muset počkat na období opakování před obnovením dotazu, aby se úspěšně dokončil.

10. Klikněte na **Zavřít a použít** na pásu karet akcí Power Query Editor.

Pak můžete začít budovat sestavu Power BI proti sloupcům vybraným z virtuální tabulky.

#### <a name="selecting-columns-in-power-apps"></a>Výběr sloupců v Power Apps

Podobně jako dotazy webového rozhraní Dataverse a Power BI můžete zlepšit výkon dotazu pro Power Apps na základě virtuálních tabulek Dataverse vyloučením sloupců souvisejících tabulek z vaší aplikace. Pokud byly na stránku zahrnuty nějaké sloupce ze související tabulky, pak adresa URL požadavku vytvořená pro načtení dat bude obsahovat vlastnosti cizího klíče související tabulky. To, jako v příkladech [Výběr sloupců v dotazu OData](#selecting-columns-in-power-apps) výše, snižuje výkon tím, že způsobuje další vyhledávání dat.

Abyste to obešli, můžete ověřit, že žádná datová pole ze souvisejících tabulek nebyla zahrnuta do jakéhokoli datového formuláře vaší aplikace Power.

1. V podokně Stromové zobrazení vyberte datový formulář pro obrazovku.
2. V podokně **Vlastností** vyberte možnost **Upravit** na vlastnosti **Pole**.
3. V podokně **Data** ověřte, že žádná z vybraných polí nejsou poli virtuální tabulky zdroje dat.

Například pokud jedno z datových polí zahrnutých na stránce v aplikaci odkazuje na jinou tabulku, například **ThisItem.Worker.Name**, kde **Worker** je související tabulka, existuje potenciál pro snížení výkonu při načítání dat.

Můžete použít [Power Apps Monitor](/powerapps/maker/monitor-overview), abyste zajistili, že do dotazu budou zahrnuty pouze sloupce, které potřebujete, abyste získali data pro Power App. Můžete zobrazit adresu URL vytvořenou pro operaci getRows, abyste zajistili, že sloupce, které jste vybrali pro vaši aplikaci, budou optimální pro načítání dat.

![Použijte Power Apps Monitor k analyzování operace getData.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Filtrování datového dotazu

Další metodou pro zlepšení výkonu provádění dotazu je omezení počtu záznamů vrácených ve výsledcích dotazu. Můžete to udělat filtrováním výsledků, abyste zajistili, že přijímáte pouze záznamy, které potřebujete.

Viz [Filtrování výsledků](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) pro další informace o filtrování dat dotazu.

### <a name="limiting-the-page-size-of-the-query"></a>Omezení velikosti stránky dotazu

Pokud pracujete s velkými datovými sadami, můžete výsledky dotazu rozdělit na více stránek přidáním předvoleb `odata.maxpagesize` na datové dotazy.

Další informace o stránkování viz [Určit počet entit, které se mají na stránce vrátit](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>Viz také

- [Konfigurace virtuálních tabulek Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)
- [Nejčastější dotazy k virtuálním tabulkám Human Resources](hr-admin-virtual-entity-faq.md)
- [Nejčastější dotazy k omezování](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
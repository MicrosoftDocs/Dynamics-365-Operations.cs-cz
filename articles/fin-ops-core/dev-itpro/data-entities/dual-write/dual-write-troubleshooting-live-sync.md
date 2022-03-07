---
title: Poradce při potížích se synchronizací v ostrém provozu
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy se synchronizací v ostrém provozu.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 69667f8b64c048f5957168d1af21a6c858bc0bad
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782572"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Poradce při potížích se synchronizací v ostrém provozu

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Microsoft Dataverse. Toto téma obsahuje informace, které vám pomohou vyřešit problémy se synchronizací v ostrém provozu.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Azure Active Directory (Azure AD). Každý oddíl vysvětluje, zda jsou vyžadovány určité role nebo konkrétní pověření.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Živá synchronizace ukazuje chybu při vytváření řádku

Může se zobrazit následující chybová zpráva při vytváření řádku v aplikaci Finance and Operations:

*\[{\\"chyba\\":{\\"kód\\":\\"0x80072560\\",\\"zpráva\\":\\"Uživatel není členem organizace.\\"}}\], Vzdálený server vrátil chybu: (403) zakázáno."}}".*

Chcete-li tento problém vyřešit, postupujte podle kroků v [Požadavcích na systém a jeho předpoklady](requirements-and-prerequisites.md). K provedení těchto kroků musí mít uživatelé aplikace se dvojím zápisem, kteří jsou vytvořeni v aplikaci Dataverse, roli správce systému. Výchozí vlastnící tým musí mít také roli správce systému.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Živá synchronizace zobrazuje chybu při pokusu o uložení dat tabulky

**Požadovaná role pro opravu problému:** správce systému

Může se zobrazit následující chybová zpráva při pokusu o uložení dat v aplikaci Finance and Operations:

*Nelze uložit změny do databáze. Jednotka práce nemůže potvrdit transakci. Nelze zapsat data do entity uoms. Zápisy do UnitOfMeasureEntity se nezdařily. Chybová zpráva Nelze synchronizovat s entitou uoms.*

Chcete-li tento problém vyřešit, musíte zajistit, aby v aplikaci Finance and Operations i Dataverse existovala potřebná referenční data. Pokud například záznam zákazníka, který je součástí aplikace , patří do určité skupiny odběratelů, ujistěte se, že v Dataverse existuje daný záznam skupiny zákazníků.

Pokud existují data na obou místech a potvrdili jste, že problém není související s daty, postupujte následujícím způsobem.

1. Otevřete entitu **DualWriteProjectConfigurationEntity** pomocí doplňku aplikace Excel. Chcete-li doplněk použít, povolte režim návrhu v doplňku Finance and Operations pro Excel a přidejte **DualWriteProjectConfigurationEntity** do listu. Další informace viz [Zobrazit a aktualizovat data entit pomocí Excelu](../../office-integration/use-excel-add-in.md).
2. Vyberte a odstraňte záznamy, které mají problémy v mapě a projektu duálního zápisu. Pro každé mapování dvou zápisů budou dva záznamy.
3. Změny publikujte pomocí doplňku aplikace Excel. Tento krok je důležitý, protože odstraní záznamy z entity a podkladových tabulek.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Zpracování chyb oprávnění ke čtení nebo zapisování při vytváření dat v aplikaci Finance and Operations

Může se zobrazit chybová zpráva "špatný požadavek" při vytváření dat v aplikaci Finance and Operations.

![Příklad chybové zprávy o chybném požadavku.](media/error_record_id_source.png)

Chcete-li tento problém opravit, musíte povolit chybějící oprávnění přiřazením správné role zabezpečení týmu mapované obchodní jednotky Dynamics 365 Sales nebo Dynamics 365 Customer Service, aby bylo možné chybějící oprávnění povolit.

1. V aplikaci Finance and Operations vyhledejte organizační jednotku, která je mapována v sadě Data Integration Connection.

    ![Mapování organizace.](media/mapped_business_unit.png)

2. Přihlaste se k prostředí v aplikaci customer engagement, přejděte na **Nastavení \> Zabezpečení** a najděte tým mapované organizační jednotky.

    ![Tým mapované organizační jednotky.](media/setting_security_page.png)

3. Otevřete stránku týmu pro úpravy a poté vyberte **Spravovat role**.

    ![Tlačítko Spravovat role.](media/manage_team_roles.png)

4. V dialogovém okně **Spravovat role týmu** přiřaďte roli, která má oprávnění pro čtení/zápis pro příslušné tabulky, a poté vyberte **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Oprava synchronizačních potíží v prostředí, které má nedávno změněné prostředí Dataverse

**Požadovaná role pro opravu problému:** správce systému

Může se zobrazit následující chybová zpráva při vytváření dat v aplikaci Finance and Operations:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Nelze generovat datovou část pro entitu CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Vytvoření zatížení se nezdařilo s chybou Neplatný identifikátor URI: Identifikátor URI je prázdný."}\],"isErrorCountUpdated":true}*

Takto vypadá chybová zpráva v aplikaci customer engagement:

> V kódu ISV došlo k neočekávané chybě. (ErrorType = ClientError) Neočekávaná výjimka z modulu plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: Nepodařilo se zpracovat účet entity. (Pokus o připojení se nezdařil, protože připojená strana nereagovala správně po určitém časovém období, nebo navázané připojení se nezdařilo, protože připojený hostitel neodpověděl.

K této chybě dojde, pokud je prostředí Dataverse nesprávně resetováno, když se pokusíte vytvořit data v aplikaci Finance and Operations.

> [!IMPORTANT]
> Pokud jste prostředí znovu propojili, musíte zastavit všechny mapy entit, než budete pokračovat kroky zmírnění.

Chcete-li problém vyřešit, musíte provést kroky v aplikaci Dataverse i Finance and Operations.

1. V aplikaci Finance and Operations postupujte podle těchto kroků:

    1. Otevřete entitu **DualWriteProjectConfigurationEntity** pomocí doplňku aplikace Excel. Chcete-li doplněk použít, povolte režim návrhu v doplňku Finance and Operations pro Excel a přidejte **DualWriteProjectConfigurationEntity** do listu. Další informace viz [Zobrazit a aktualizovat data entit pomocí Excelu](../../office-integration/use-excel-add-in.md).
    2. Vyberte a odstraňte záznamy, které mají problémy v mapě a projektu duálního zápisu. Pro každé mapování dvou zápisů budou dva záznamy.
    3. Změny publikujte pomocí doplňku aplikace Excel. Tento krok je důležitý, protože odstraní záznamy z entity a podkladových tabulek.
    4. Abyste předešli chybám při opětovném propojení prostředí Finance and Operations nebo Dataverse, ujistěte se, že nezůstanou žádné konfigurace duálního zápisu.

2. V Dataverse postupujte následovně:

    1. Přihlaste se k prostředí Dataverse (například `https://*****.crm.dynamics.com/`).
    2. Jděte na **Pokročilé nastavení** \> **Rozšířené hledání**.
    3. Vyberte **Konfigurace běhu DualWrite**.
    4. Vyberte sloupec k zobrazení.
    5. Vyberte **Výsledky** pro zobrazení konfigurací.
    6. Odstraňte všechny instance.

3. V aplikaci Finance and Operations postupujte podle těchto kroků:

    1. Otevřete entitu **DualWriteProjectConfigurationEntity** pomocí doplňku aplikace Excel. Chcete-li doplněk použít, povolte režim návrhu v doplňku Finance and Operations pro Excel a přidejte **DualWriteProjectConfigurationEntity** do listu. Další informace viz [Zobrazit a aktualizovat data entit pomocí Excelu](../../office-integration/use-excel-add-in.md).
    2. Vyberte a odstraňte záznamy, které mají problémy v mapě a projektu duálního zápisu. Pro každé mapování dvou zápisů budou dva záznamy.
    3. Změny publikujte pomocí doplňku aplikace Excel. Tento krok je důležitý, protože odstraní záznamy z entity a podkladových tabulek.
    4. Abyste předešli chybám při opětovném propojení prostředí Finance and Operations nebo Dataverse, ujistěte se, že nezůstanou žádné konfigurace duálního zápisu.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Chyba živé synchronizace po provedení úplné kopie databáze

Po spuštění úplné kopie databáze z jednoho systému do druhého a pokusu o spuštění operace databáze se může zobrazit následující chybová zpráva:

*Organizace SecureConfig (???) neodpovídá skutečné organizaci CRM (???).*

Chybová zpráva se zobrazuje z modulu plug-in runtime dual-write, aby bylo zajištěno, že konfiguraci dual-write, která je nastavena v jednom systému, nelze použít v jiném systému.

Problém vyřešíte odstraněním všech záznamů v souboru **msdyn_dualwriteruntimeconfig** po obnovení databáze. Další informace viz [Odpojení a opětovné připojení prostředí s duálním zápisem](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Problémy se živou synchronizací, které jsou způsobeny nesprávnou syntaxí filtru dotazů na mapách duálního zápisu

Přestože je výraz dotazu pro filtr mapy duálního zápisu syntakticky správný, nemusí fungovat podle očekávání. Výraz filtru je na entitě, nikoli na individuálním zdroji dat objektu dotazu. Vygenerovaný dotaz SQL proto nevrací očekávané výsledky.

Následuje příklad.

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Můžete očekávat, že budou odfiltrovány projekty, které nemají nadřazené objekty. Filtr však nefunguje, protože je přeložen na dotaz, který se podobá následujícímu příkladu.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Skutečným výsledkem je, že pole `parentProject` je vyhodnoceno jako `null`. Nicméně `null` není totéž jako prázdný řetězec. Kvůli tomuto nesouladu filtr dotazů nevrací platné výsledky.

Chcete-li opravit problém, postupujte následovně.

1. Přidejte vypočítaný sloupec, který lze přidat do modelu rozšíření a který je podpořen logikou, která převádí `null` do prázdného řetězce.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Použijte filtr na nový vypočítaný sloupec namísto výchozího sloupce.

K vyhodnocení filtru ve vývojovém prostředí můžete použít následující kód X ++ k ověření výsledků. Spusťte tento kód jako samostatný program. Můžete jej použít k vyhodnocení různých druhů filtrů, které jsou použitelné pro entitu, než tyto filtry použijete na mapách s dvojitým zápisem. Dotaz lze spustit proti databázi a vyhodnotit nesrovnalosti.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Data z aplikace Finance and Operations nejsou synchronizována s Dataverse

Během živé synchronizace můžete narazit na problém, kdy je synchronizována pouze část dat aplikace Finance and Operations do Dataverse nebo data nejsou synchronizována vůbec.

> [!NOTE]
> Tento problém musíte vyřešit během vývoje.

Než začnete problém řešit, přečtěte si následující předpoklady:

+ Ujistěte se, že vaše vlastní změny jsou zapsány v jediném rozsahu transakce.
+ Obchodní události a rámec pro dvojí zápis nezvládají operace `doinsert()`, `doUpdate()` a `recordset()` nebo záznamy, kde je označeno `skipBusinessEvents(true)`. Pokud je váš kód uvnitř těchto funkcí, nebude spuštěn duální zápis.
+ Obchodní události musí být registrovány pro mapovaný zdroj dat. Některé zdroje dat mohou používat vnější spojení a mohou být označeny jako pouze pro čtení v aplikacích Finance and Operations. Tyto zdroje dat nejsou sledovány.
+ Změny budou spuštěny pouze v případě, že jsou úpravy na mapovaných polích. Nemapované úpravy pole nespustí duální zápis.
+ Ujistěte se, že vyhodnocení filtrů poskytuje platný výsledek.

### <a name="troubleshooting-steps"></a>Kroky řešení potíží

1. Zkontrolujte mapování polí na stránce správy s duálním zápisem. Pokud pole není mapováno z aplikace Finance and Operations do Dataverse, nebude sledováno. Například na následujícím obrázku je pole **Popis** sledováno z Dataverse, ale ne z aplikace Finance and Operations. Žádné změny v tomto poli uvnitř aplikace Finance and Operations nebudou sledovány.

    ![Sledované pole.](media/live-sync-troubleshooting-1.png)

2. Určete, zda je zdroj dat sledován v definici obchodních událostí. Například na následujícím obrázku není žádné pole z tabulky **DefaultDimensionDAVs** a podkladové tabulky budou sledovány kvůli změnám. Zdroje dat, které používají vnější spojení a které jsou označeny pouze pro čtení, nejsou sledovány.

    ![Pole, které není sledováno.](media/live-sync-troubleshooting-2.png)

3. Zjistěte, zda se mapovaná pole tabulky zobrazí v tabulce **BUSINESSEVENTSDEFINICE**, jak ukazuje následující obrázek. Pokud ve výsledku dotazu nenajdete hledané pole, nebude spuštěno dvojitým zápisem.

    ![Sledované pole v tabulce.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Ukázkový scénář

V aplikacích Finance and Operations existuje aktualizace adresy pro záznam kontaktu, ale změna adresy není synchronizována s Dataverse. K tomuto scénáři dochází, protože žádný záznam v tabulce **BusinessEventsDefinice** neobsahuje kombinaci ovlivněné tabulky a entity. Konkrétně tabulka **LogistikaPostalAddress** není přímým zdrojem dat pro entitu **smmContactpersonCDSV2Entity**. Entita **smmContactpersonCDSV2Entity** má **smmContactPersonV2Entity** jako zdroj dat a entita **smmContactPersonV2Entity** zase má jako zdroj dat **LogisticsPostalAddressBaseEntity**. Tabulka **LogistikaPostalAddress** je zdrojem dat pro **LogisticsPostalAddressBaseEntity**.

Podobná situace může nastat u některých nestandardních vzorů, například v případech, kdy tabulka upravovaná ve Finance and Operations není zjevně propojena s entitou, která ji obsahuje. Například data primární adresy se vypočítají v entitě **smmContactPersonCDSV2Entity**. Rámec duálního zápisu se pokouší určit, jak je změna podkladové tabulky mapována zpět na entity. Obvykle je tento přístup dostačující. V některých případech je však odkaz tak složitý, že musíte být konkrétní. Musíte se ujistit, že **RecId** související tabulky je přímo k dispozici v účetní jednotce. Poté přidejte statickou metodu ke sledování změn v tabulce.

Například si prohlédněte metodu **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping ()**. **CustCustomerV3entity** a **VendVendorV2Entity** byly upraveny tak, aby tuto situaci zvládly.

Chcete-li opravit problém, postupujte následovně.

1. Přidejte pole **PrimaryPostalAddressRecId** do entity **smmContactPersonV2Entity**. Nastavte jako interní.

    ![Pole přidané do entity smmContactPersonV2Entity.](media/Troubleshoot_live_sync_issue_1.png)

2. Stejné pole přidejte do entity **smmContactPersonCDSV2Entity**.

    ![Pole přidané do entity smmContactPersonCDSV2Entity.](media/Troubleshoot_live_sync_issue_2.png)

3. Přidejte následující metodu do třídy **smmContactPersonCDSV2Entity**.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Synchronizujte databázi a vytvořte aplikaci.
5. Zastavte všechny mapy s dvojitým zápisem, které jsou vytvořeny v entitě **smmContactPersonCDSV2Entity**.
6. Spusťte mapu. Měli byste vidět novou tabulku (**LogisticsPostalAddress** v tomto případě), které jste začali sledovat pomocí sloupce **RefTableName** pro řádek, kde hodnota **refentityname** rovná se **smmContactPersonCDSV2Entity** v tabulce **BusinessEventsDefinice**.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Chyba při vytváření záznamu, kam je odesláno více záznamů z aplikace Finance and Operations do Dataverse ve stejné dávce

U jakékoli transakce aplikace Finance and Operations vytváří data v dávce a odešle je jako dávku do Dataverse. Pokud jsou v rámci stejné transakce vytvořeny dva záznamy a navzájem na sebe odkazují, může se zobrazit chybová zpráva podobná následujícímu příkladu v aplikaci Finance and Operations:

*Nelze zapisovat data do entity aaa_fundingsources. Nelze vyhledat ebecsfs_contracts s hodnotami {PC00...}. Nelze vyhledat aaa_fundingsources s hodnotami {PC00...}. Zápisy do aaa_fundingsources se nezdařily s chybovou zprávou Zpráva o výjimce: Vzdálený server vrátil chybu: (400) Chybný požadavek.*

Chcete -li problém vyřešit, vytvořte vztahy entit v aplikaci Finance and Operations k označení, že tyto dvě entity spolu souvisejí a že související záznamy jsou zpracovávány ve stejné transakci.

## <a name="enable-verbose-logging-of-error-messages"></a>Povolit podrobné protokolování chybových zpráv

V aplikaci Finance and Operations můžete narazit na chyby související s prostředím Dataverse. Chybová zpráva nemusí obsahovat plný text zprávy nebo jiná relevantní data. Chcete -li získat další informace, můžete povolit podrobné protokolování nastavením příznaku **IsDebugMode**, který je přítomen v entitě **DualWriteProjectConfigurationEntity** ve všech konfiguracích projektu v aplikaci Finance and Operations.

1. Otevřete entitu **DualWriteProjectConfigurationEntity** pomocí doplňku aplikace Excel. Chcete-li doplněk použít, povolte režim návrhu v doplňku Finance and Operations pro Excel a přidejte **DualWriteProjectConfigurationEntity** do listu. Další informace viz [Zobrazit a aktualizovat data entit pomocí Excelu](../../office-integration/use-excel-add-in.md).
2. Nastavte příznak **IsDebugMode** na **Ano** v projektu.
3. Spusťte scénář.
4. Podrobné protokoly jsou k dispozici v tabulce **DualWriteErrorLog**. Chcete -li vyhledat data pomocí prohlížeče tabulek, použijte následující adresu URL: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. Chcete -li zachytit více protokolů v režimu ladění, nainstalujte aktualizaci v [KB 4595434 (Oprava prázdných hodnot šířených v živé synchronizaci duálního zápisu)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Chyba při přidání adresy pro zákazníka nebo kontakt

Při pokusu o přidání adresy pro zákazníka nebo kontakt se může zobrazit následující chybová zpráva aplikací Finance and Operations nebo Dataverse:

*Nelze zapsat data do entity msdyn_partypostaladdresses. Zápisy do entity DirPartyPostalAddressLocationCDSEntity se nezdařily s následující chybovou zprávou Žádost selhala s kódem stavu Kód chyby BadRequest a CDS: Zpráva odpovědi: 0x80040265: Došlo k chybě v pluginu. Záznam, který má hodnoty atributů Umístění ID již existuje. Klíč entity Umístění ID klíče vyžaduje, aby tato sada atributů obsahovala jedinečné hodnoty. Vyberte jedinečné hodnoty a zkuste to znovu.*

Chcete-li problém vyřešit, nainstalujte balíček orchestrace dvojitého zápisu verze (2.2.2.60), aby klíče v tabulce **Adresa** byly definovány tak, jak je uvedeno v následující tabulce.

| Vlastnost | Hodnota |
|---|---|
| Zobrazovaný název | **Klíč místa** |
| Jméno | **msdyn_locationkey** |
| Pole | **msdyn_locationid**, **parentid** |
| Stav | **Aktivní** |
| Systémová úloha | Bianko |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Chyba při přidání zákazníka do Dataverse

Může se zobrazit následující chybová zpráva při pokusu o přidání zákazníka v Dataverse:

*"RecordError0":"Zápis se nezdařil pro entitu Customers V3 s neznámou výjimkou - pro typ strany 'Organizace' nebyl nalezen záznam strany}.*

Když je zákazník vytvořen v Dataverse, vygeneruje se nové číslo strany. Chybová zpráva se zobrazí, když je záznam zákazníka synchronizován s aplikacemi Finance and Operations, ale již existuje záznam zákazníka, který má jiné číslo strany.

Chcete -li problém vyřešit, najděte zákazníka vyhledáním strany. Pokud zákazník neexistuje, vytvořte nový záznam zákazníka. Pokud zákazník existuje, použijte stávající stranu k vytvoření nového záznamu o zákazníkovi.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Chyba při vytváření nového zákazníka, dodavatele nebo kontaktu v Dataverse

Při pokusu o vytvoření nového zákazníka, dodavatele nebo kontakt v Dataverse můžete obdržet následující chybovou zprávu:

*Nelze aktualizovat typ strany z 'DirOrganization' na 'DirPerson', místo toho by mělo být provedeno odstranění stávající strany následované vložením s novým typem.*

V Dataverse je číselná sekvence v tabulce **msdyn_party**. Když je účet vytvořen v Dataverse, vytvoří se nová strana (např. **Party-001** typu **Organizace**). Tato data jsou odesílána do aplikace Finance and Operations. Pokud se prostředí Dataverse resetuje nebo je prostředí Finance and Operations spojeno s jiným prostředím Dataverse a poté se vytvoří nový záznam kontaktu v Dataverse, vytvoří se nová hodnota strany, která začíná **Party-001**. Tentokrát bude vytvořen záznam strany **Party-001** typu **Osoba**. Když jsou tato data synchronizována, aplikace Finance and Operations zobrazují předchozí chybovou zprávu, protože záznam **Party-001** typu **Organizace** již existuje.

Chcete -li problém vyřešit, změňte automatickou sekvenci čísel pro pole **msdyn_partynumber** tabulky **msdyn_party** v Dataverse na jinou automatickou číselnou sekvenci.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Problém s výkonem při mapování zákazníků nebo kontaktů

Možná budete moci okrajově zlepšit výkon živé synchronizace pro zákazníky a kontakty přizpůsobením metody **getEntityDataSourceToFieldMapping** (v entitě **CustCustomerV3Entity**) a metody **getEntityDataSourceToFieldMapping** (v entitě **smmContactPersonCDSV2Entity**). Tato přizpůsobení snižují počet záznamů v tabulce **BusinessEventsDefinice**. Toto snížení počtu záznamů zase snižuje počet vyvolávaných událostí.

Metoda **getEntityDataSourceToFieldMapping** v entitě **CustCustomerV3Entity** způsobí, že aktualizace elektronické adresy nebo poštovní adresy zákazníka vyvolá obchodní události, takže aktualizovaná data budou odeslána do Dataverse. Pokud nepoužíváte všechna pole a nepotřebujete informace v duálním zápisu, okomentujte příslušné řádky v metodě. Každé sledované pole a tabulka přidaná v této metodě přidá záznam do tabulky **BusinessEventsDefinice** pro kombinaci sledované tabulky a sledované entity.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Podobně musí metoda **getEntityDataSourceToFieldMapping** v entitě **smmContactPersonCDSV2Entity** zajistit, že aktualizace elektronické adresy nebo poštovní adresy kontaktu vyvolá obchodní události, takže aktualizovaná data budou odeslána do Dataverse. V této metodě můžete komentovat řádky pro všechna pole, která nepoužíváte.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Po aktualizaci metod proveďte následující kroky.

1. Synchronizujte databázi a vytvořte aplikaci.
2. Zastavte všechny mapy s dvojitým zápisem, které jsou vytvořeny v entitě **smmContactPersonCDSV2Entity** a **CustCustomerV3Entity**.
3. Spusťte mapy. Měli byste vidět méně záznamů v entitách **smmContactPersonCDSV2Entity** a **CustCustomerV3Entity** a v tabulce **BusinessEventsDefinition** a výkon by se měl nepatrně zlepšit.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

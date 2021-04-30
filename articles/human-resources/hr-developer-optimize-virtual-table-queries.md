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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8026abd5c3e0f9b78e8c016731fd7785490bc945
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891095"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="467a1-103">Optimalizace dotazů virtuálních tabulek Dataverse</span><span class="sxs-lookup"><span data-stu-id="467a1-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="467a1-104">Výdej</span><span class="sxs-lookup"><span data-stu-id="467a1-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="467a1-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="467a1-105">Overview</span></span>

<span data-ttu-id="467a1-106">Při použití virtuálních tabulek Dataverse k vývoji integrací a dalších datových připojení s Dynamics 365 Human Resources můžete narazit na problémy s výkonem při dotazech na virtuální tabulky.</span><span class="sxs-lookup"><span data-stu-id="467a1-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="467a1-107">Pomalé provádění dotazů může nastat u různých klientů nebo rozhraní.</span><span class="sxs-lookup"><span data-stu-id="467a1-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="467a1-108">Například k problému může dojít za následujících okolností:</span><span class="sxs-lookup"><span data-stu-id="467a1-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="467a1-109">Při dotazování na virtuální tabulku prostřednictvím webového rozhraní API Dataverse</span><span class="sxs-lookup"><span data-stu-id="467a1-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="467a1-110">Při vytváření aplikace Power App proti virtuální tabulce</span><span class="sxs-lookup"><span data-stu-id="467a1-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="467a1-111">Při tvorbě sestavy Power BI na virtuální tabulce</span><span class="sxs-lookup"><span data-stu-id="467a1-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="467a1-112">Všechna tato rozhraní mají potenciál překonat problém s výkonem.</span><span class="sxs-lookup"><span data-stu-id="467a1-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="467a1-113">Jednou z příčin pomalého výkonu s virtuálními tabulkami Dataverse pro lidské zdroje jsou sloupce cizího klíče virtuální tabulky související s [vlastnostmi navigace](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) tabulky.</span><span class="sxs-lookup"><span data-stu-id="467a1-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="467a1-114">Když jsou pro virtuální tabulku vytvořeny navigační vlastnosti, do tabulky se automaticky přidá sloupec cizího klíče, který představuje hodnotu klíče pro sloupec klíče související virtuální tabulky.</span><span class="sxs-lookup"><span data-stu-id="467a1-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="467a1-115">Například sloupec **_mshr_fk_person_id_value** je přidán do entity **mshr_hcmworkerbaseentity** s vlastností cizího klíče z entity **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="467a1-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="467a1-116">Z důvodu toho, jak jsou hodnoty pro tyto sloupce cizích klíčů udržovány v tabulce, může mít načítání hodnot negativní dopad na výkon dotazu vůči virtuální tabulce.</span><span class="sxs-lookup"><span data-stu-id="467a1-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="467a1-117">Možné příznaky</span><span class="sxs-lookup"><span data-stu-id="467a1-117">Potential symptoms</span></span>

<span data-ttu-id="467a1-118">Příklad, kde můžete vidět tento dopad, je v dotazech proti entitě pracovník (**mshr_hcmworkerentity**) nebo základní pracovník (**mshr_hcmworkerbaseentity**).</span><span class="sxs-lookup"><span data-stu-id="467a1-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="467a1-119">Problém s výkonem se může projevit několika různými způsoby:</span><span class="sxs-lookup"><span data-stu-id="467a1-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="467a1-120">**Pomalé provádění dotazu**: Dotaz na virtuální tabulku může vrátit očekávané výsledky, ale provedení dotazu trvá déle, než se očekávalo.</span><span class="sxs-lookup"><span data-stu-id="467a1-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="467a1-121">**Časový limit dotazu**: Dotaz může vypršet a vrátit následující chybu: „Byl získán token pro volání Finance and Operations, ale Finance and Operations vrátil chybu typu InternalServerError.“</span><span class="sxs-lookup"><span data-stu-id="467a1-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="467a1-122">**Neočekávaná chyba** : Dotaz může vrátit chybu typu 400 s následující zprávou: „Došlo k neočekávané chybě.“</span><span class="sxs-lookup"><span data-stu-id="467a1-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Typ chyby 400 na HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="467a1-124">**Omezování**: Dotaz může nadužívat prostředky serveru a podléhat omezením.</span><span class="sxs-lookup"><span data-stu-id="467a1-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="467a1-125">V tomto případě dotaz vrátí následující chybu: „Byl získán token pro volání Finance and Operations, ale Finance and Operations vrátil chybu typu 429.“</span><span class="sxs-lookup"><span data-stu-id="467a1-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="467a1-126">Další informace o omezení v v Human Resources najdete v tématu [Časté otázky k omezování](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="467a1-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Typ chyby 429 na HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="467a1-128">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="467a1-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="467a1-129">Omezte počet sloupců obsažených v dotazu na data</span><span class="sxs-lookup"><span data-stu-id="467a1-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="467a1-130">U virtuálních tabulek je jednou z metod s největším potenciálem pro zlepšení výkonu dotazu omezení počtu sloupců vybraných v dotazu.</span><span class="sxs-lookup"><span data-stu-id="467a1-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="467a1-131">Obecným návodem pro optimalizaci výkonu dotazu je omezení sloupců vrácených v dotazu pouze na ty vlastnosti, které potřebujete.</span><span class="sxs-lookup"><span data-stu-id="467a1-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="467a1-132">To platí zejména u sloupců cizích klíčů na virtuálních tabulkách.</span><span class="sxs-lookup"><span data-stu-id="467a1-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="467a1-133">Pokud nepotřebujete hodnoty ve sloupcích cizího klíče pro vaši integraci nebo sestavu, strukturujte dotaz tak, aby vybral pouze ty sloupce, které potřebujete, bez sloupců cizího klíče.</span><span class="sxs-lookup"><span data-stu-id="467a1-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="467a1-134">Výběr sloupců v dotazu OData</span><span class="sxs-lookup"><span data-stu-id="467a1-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="467a1-135">Při dotazování na virtuální tabulku prostřednictvím webového rozhraní API Dataverse můžete omezit počet sloupců zahrnutých v dotazu pomocí možnosti systémového dotazu **$select** a definice sloupců, pro které chcete vrátit výsledky.</span><span class="sxs-lookup"><span data-stu-id="467a1-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="467a1-136">Chcete-li maximalizovat výkon, vylučte sloupce cizího klíče (ty s předponou **_mshr_FK_**) z dotazu.</span><span class="sxs-lookup"><span data-stu-id="467a1-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="467a1-137">Například následující dotaz proti entitě **mshr_hcmworkerbaseentity** bude zahrnovat pouze sloupce obsažené ve výrazu možnosti dotazu **$select** bez hodnot cizího klíče.</span><span class="sxs-lookup"><span data-stu-id="467a1-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="467a1-138">To poskytuje významné zlepšení výkonu oproti dotazu, který zahrnuje všechny sloupce tabulky.</span><span class="sxs-lookup"><span data-stu-id="467a1-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="467a1-139">Doporučení omezit počet vybraných sloupců platí také při použití možnost dotazu **$expand** dotazu k rozšíření dotazu na související virtuální tabulky prostřednictvím navigačních vlastností.</span><span class="sxs-lookup"><span data-stu-id="467a1-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="467a1-140">Například následující dotaz obsahuje sloupce z entity **mshr_hcmworkerbaseentity** s rozšířenými sloupci z entity **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="467a1-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="467a1-141">Možnost dotazu **$select** je také zahrnuta ve výrazu možnosti dotazu **$expand**.</span><span class="sxs-lookup"><span data-stu-id="467a1-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="467a1-142">Při použití této metody načítání dat pomocí možnosti dotazu **$select** ve výrazu možnosti dotazu **$select** obvykle uvidíte větší vylepšení výkonu, když je vlastnost navigace mezi entitami vztahem více : jedna.</span><span class="sxs-lookup"><span data-stu-id="467a1-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="467a1-143">Při rozšiřování vztahu jedna k více se nemusíte setkat se stejným zkrácením doby provedení dotazu.</span><span class="sxs-lookup"><span data-stu-id="467a1-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="467a1-144">Další informace o definici vztahu pro virtuální tabulky Dataverse, viz [Vztahy mezi tabulkami](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="467a1-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="467a1-145">Další informace o používání možností systémového dotazu **$select** a **$expand** ve webovém rozhraní API Dataverse viz [Načíst související záznamy entit pomocí dotazu](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="467a1-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="467a1-146">Výběr sloupců v Power BI</span><span class="sxs-lookup"><span data-stu-id="467a1-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="467a1-147">Pokud narazíte na některý z výše uvedených náznaků pomalého výkonu při sestavování sestavy Power BI proti virtuální tabulce Dataverse, můžete zlepšit výkon vyloučením sloupců cizího klíče ze sloupců vybraných z tabulky pro sestavu.</span><span class="sxs-lookup"><span data-stu-id="467a1-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="467a1-148">Například pokud používáte Power BI Desktop k vytvoření sestavy proti entitě **mshr_hcmworkerbaseentity**, můžete pomocí následujících kroků vybrat sloupce, které chcete zahrnout do dotazu na sestavu.</span><span class="sxs-lookup"><span data-stu-id="467a1-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="467a1-149">V Power BI Desktop vyberte **Více...** z rozevíracího seznamu **Získat data** na pásu karet akcí.</span><span class="sxs-lookup"><span data-stu-id="467a1-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="467a1-150">Do okna **Získat data** zadejte do vyhledávacího pole **Common Data Service**, vyberte konektor **Common Data Service** a vyberte **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="467a1-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="467a1-151">Do pole **URL serveru** okna Common Data Service zadejte URI organizace pro vaše prostředí Dataverse a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="467a1-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Zadejte URI pro prostředí Dataverse](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="467a1-153">V okně Navigátor rozbalte uzel **Entity**.</span><span class="sxs-lookup"><span data-stu-id="467a1-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="467a1-154">Do vyhledávacího pole zadejte **mshr_hcmworkerbaseentity** a vyberte entitu.</span><span class="sxs-lookup"><span data-stu-id="467a1-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="467a1-155">Vyberte možnost **Transformovat data**.</span><span class="sxs-lookup"><span data-stu-id="467a1-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="467a1-156">V okně Editoru Power Query vyberte **Rozšířený editor**.</span><span class="sxs-lookup"><span data-stu-id="467a1-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="467a1-157">V okně **Rozšířený editor** aktualizujte dotaz tak, aby vypadal jako dotaz níže, podle potřeby přidejte nebo odeberte sloupce v poli.</span><span class="sxs-lookup"><span data-stu-id="467a1-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Aktualizujte dotaz v Rozšířeném editoru pro editor Power Query](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="467a1-159">Vyberte **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="467a1-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="467a1-160">Pokud jste předtím obdrželi chybu typu 429 z dotazu před aktualizací, možná budete muset počkat na období opakování před obnovením dotazu, aby se úspěšně dokončil.</span><span class="sxs-lookup"><span data-stu-id="467a1-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="467a1-161">Klikněte na **Zavřít a použít** na pásu karet akcí Power Query Editor.</span><span class="sxs-lookup"><span data-stu-id="467a1-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="467a1-162">Pak můžete začít budovat sestavu Power BI proti sloupcům vybraným z virtuální tabulky.</span><span class="sxs-lookup"><span data-stu-id="467a1-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="467a1-163">Výběr sloupců v Power Apps</span><span class="sxs-lookup"><span data-stu-id="467a1-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="467a1-164">Podobně jako dotazy webového rozhraní Dataverse a Power BI můžete zlepšit výkon dotazu pro Power Apps na základě virtuálních tabulek Dataverse vyloučením sloupců souvisejících tabulek z vaší aplikace.</span><span class="sxs-lookup"><span data-stu-id="467a1-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="467a1-165">Pokud byly na stránku zahrnuty nějaké sloupce ze související tabulky, pak adresa URL požadavku vytvořená pro načtení dat bude obsahovat vlastnosti cizího klíče související tabulky.</span><span class="sxs-lookup"><span data-stu-id="467a1-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="467a1-166">To, jako v příkladech [Výběr sloupců v dotazu OData](#selecting-columns-in-power-apps) výše, snižuje výkon tím, že způsobuje další vyhledávání dat.</span><span class="sxs-lookup"><span data-stu-id="467a1-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="467a1-167">Abyste to obešli, můžete ověřit, že žádná datová pole ze souvisejících tabulek nebyla zahrnuta do jakéhokoli datového formuláře vaší aplikace Power.</span><span class="sxs-lookup"><span data-stu-id="467a1-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="467a1-168">V podokně Stromové zobrazení vyberte datový formulář pro obrazovku.</span><span class="sxs-lookup"><span data-stu-id="467a1-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="467a1-169">V podokně **Vlastností** vyberte možnost **Upravit** na vlastnosti **Pole**.</span><span class="sxs-lookup"><span data-stu-id="467a1-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="467a1-170">V podokně **Data** ověřte, že žádná z vybraných polí nejsou poli virtuální tabulky zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="467a1-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="467a1-171">Například pokud jedno z datových polí zahrnutých na stránce v aplikaci odkazuje na jinou tabulku, například **ThisItem.Worker.Name**, kde **Worker** je související tabulka, existuje potenciál pro snížení výkonu při načítání dat.</span><span class="sxs-lookup"><span data-stu-id="467a1-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="467a1-172">Můžete použít [Power Apps Monitor](/powerapps/maker/monitor-overview), abyste zajistili, že do dotazu budou zahrnuty pouze sloupce, které potřebujete, abyste získali data pro Power App.</span><span class="sxs-lookup"><span data-stu-id="467a1-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="467a1-173">Můžete zobrazit adresu URL vytvořenou pro operaci getRows, abyste zajistili, že sloupce, které jste vybrali pro vaši aplikaci, budou optimální pro načítání dat.</span><span class="sxs-lookup"><span data-stu-id="467a1-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Použijte Power Apps Monitor k analyzování operace getData](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="467a1-175">Filtrování datového dotazu</span><span class="sxs-lookup"><span data-stu-id="467a1-175">Filtering the data query</span></span>

<span data-ttu-id="467a1-176">Další metodou pro zlepšení výkonu provádění dotazu je omezení počtu záznamů vrácených ve výsledcích dotazu.</span><span class="sxs-lookup"><span data-stu-id="467a1-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="467a1-177">Můžete to udělat filtrováním výsledků, abyste zajistili, že přijímáte pouze záznamy, které potřebujete.</span><span class="sxs-lookup"><span data-stu-id="467a1-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="467a1-178">Viz [Filtrování výsledků](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) pro další informace o filtrování dat dotazu.</span><span class="sxs-lookup"><span data-stu-id="467a1-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="467a1-179">Omezení velikosti stránky dotazu</span><span class="sxs-lookup"><span data-stu-id="467a1-179">Limiting the page size of the query</span></span>

<span data-ttu-id="467a1-180">Pokud pracujete s velkými datovými sadami, můžete výsledky dotazu rozdělit na více stránek přidáním předvoleb `odata.maxpagesize` na datové dotazy.</span><span class="sxs-lookup"><span data-stu-id="467a1-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="467a1-181">Další informace o stránkování viz [Určit počet entit, které se mají na stránce vrátit](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="467a1-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="467a1-182">Viz také</span><span class="sxs-lookup"><span data-stu-id="467a1-182">See also</span></span>

- [<span data-ttu-id="467a1-183">Konfigurace virtuálních tabulek Dataverse</span><span class="sxs-lookup"><span data-stu-id="467a1-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="467a1-184">Nejčastější dotazy k virtuálním tabulkám Human Resources</span><span class="sxs-lookup"><span data-stu-id="467a1-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="467a1-185">Nejčastější dotazy k omezování</span><span class="sxs-lookup"><span data-stu-id="467a1-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
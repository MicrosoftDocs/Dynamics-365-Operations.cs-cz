---
title: Nejčastější dotazy týkající se integrace s aplikací Finance
description: Tento článek vysvětluje, jaká data jsou synchronizována v rámci integrace aplikací Human Resources a Finance.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5befac6c72153332319eefc1aaeab30c33f4c69
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892244"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="e5c1a-103">Nejčastější dotazy týkající se integrace s aplikací Finance</span><span class="sxs-lookup"><span data-stu-id="e5c1a-103">Integration with Finance FAQ</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e5c1a-104">Toto téma uvádí odpovědi na časté otázky spojené s tím, jaká data jsou synchronizována při integraci aplikace Dynamics 365 Human Resources s Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a><span data-ttu-id="e5c1a-105">Mohu upravit uživatele aplikace Dynamics 365 Talent v Power Apps?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-105">Can I edit the Dynamics 365 Talent application user in Power Apps?</span></span>

<span data-ttu-id="e5c1a-106">Č.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-106">No.</span></span> <span data-ttu-id="e5c1a-107">Pokud upravíte uživatele aplikace Human Resources, integrace mezi Human Resources a Dataverse může selhat.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-107">If you edit the Human Resources application user, the integration between Human Resources and Dataverse might fail.</span></span> <span data-ttu-id="e5c1a-108">V následující tabulce jsou uvedena výchozí nastavení pro uživatele aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-108">The following table shows the default settings for the Talent application user.</span></span>

| <span data-ttu-id="e5c1a-109">Celé jméno</span><span class="sxs-lookup"><span data-stu-id="e5c1a-109">Full Name</span></span> | <span data-ttu-id="e5c1a-110">ID přihlášky</span><span class="sxs-lookup"><span data-stu-id="e5c1a-110">Application ID</span></span> | <span data-ttu-id="e5c1a-111">ID objektu Azure AD</span><span class="sxs-lookup"><span data-stu-id="e5c1a-111">Azure AD Object ID</span></span> | <span data-ttu-id="e5c1a-112">Identifikátor URI ID přihlášky</span><span class="sxs-lookup"><span data-stu-id="e5c1a-112">Application ID URI</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="e5c1a-113">Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="e5c1a-113">Dynamics365 for Talent</span></span> | <span data-ttu-id="e5c1a-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="e5c1a-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> | <span data-ttu-id="e5c1a-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span><span class="sxs-lookup"><span data-stu-id="e5c1a-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span></span> | <span data-ttu-id="e5c1a-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="e5c1a-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> |

![Výchozí nastavení pro uživatele aplikace Talent](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="e5c1a-118">Jsou synchronizovaná všechna data nebo jenom některé datové entity?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-118">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="e5c1a-119">Je synchronizována dílčí skupina dat.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-119">A subset of the data is synchronized.</span></span> <span data-ttu-id="e5c1a-120">Seznam všech entit uvádí téma [Integrace s Dynamics 365 Finance](hr-admin-integration-finance.md).</span><span class="sxs-lookup"><span data-stu-id="e5c1a-120">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a><span data-ttu-id="e5c1a-121">Proč se nezobrazují žádná data synchronizovaná s touto funkcí Dataverse?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-121">Why don't I see any data synced to Dataverse?</span></span>

<span data-ttu-id="e5c1a-122">Ve výchozím nastavení je integrace Dataverse v nových prostředích, která nezahrnují zadaná ukázková data, zakázána.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-122">By default, the Dataverse integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="e5c1a-123">Ve výchozím nastavení je tato možnost zapnutá v nových prostředích zahrnujících ukázková data a synchronizace dat je zahájena při zřizování prostředí.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-123">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="e5c1a-124">Jakmile bude prostředí připraveno k synchronizaci dat, můžete zapnout integraci.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-124">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="e5c1a-125">Další informace naleznete v tématu [Konfigurace integrace Dataverse](hr-admin-integration-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="e5c1a-125">For more information, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="e5c1a-126">Je možné vytvořit nové mapování bez použití šablon</span><span class="sxs-lookup"><span data-stu-id="e5c1a-126">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="e5c1a-127">Šablony jsou počátečním bodem.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-127">Templates are the starting point.</span></span> <span data-ttu-id="e5c1a-128">Můžete vytvořit vlastní šablonu, ale při vytváření projektu integrace je šablona potřeba vždy.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-128">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="e5c1a-129">Další informace o šablonách integrátoru dat (DI) a projektech naleznete v tématu [Integrace dat v Microsoft Dataverse](/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="e5c1a-129">For more information about data integrator (DI), templates, and projects, see [Integrate data into Microsoft Dataverse](/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="e5c1a-130">Lze mapovat finanční dimenze k přenosu mezi aplikacemi Human Resources a Finance?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-130">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="e5c1a-131">Finanční dimenze aktuálně nejsou v Dataverse pro aplikace a proto nejsou součástí výchozí šablony.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-131">Financial dimensions aren’t currently in Dataverse and as a result aren’t part of the default template.</span></span> <span data-ttu-id="e5c1a-132">Tato entita je plánována, ale v současné době není k dispozici žádná časová osa pro uvolnění.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-132">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="e5c1a-133">V případě dat, která existují v modulu Finance, ale ne v aplikaci Human Resources, spojte tyto dva systémy pomocí příkazu **Konfigurovat odkazy** v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-133">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![Mapovat finanční dimenze](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="e5c1a-135">Někdy se stane, že když importuji zaměstnance, přejdou v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-135">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="e5c1a-136">Proč?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-136">Why?</span></span>

<span data-ttu-id="e5c1a-137">Jestliže zaměstnanci nemají záznam podrobností o aktivním zaměstnání v aplikaci Human Resources může dojít k této chybě.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-137">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="e5c1a-138">Chybu vyřešíte tak, že přejdete na položky **Správa zaměstnanců \> Zaměstnanci \> Historie zaměstnání \> Správce dat** a ověříte, že existuje aktivní záznam detailů zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-138">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="e5c1a-139">Pokud vyberu možnost mapovat pouze dílčí sadu polí, spustí provedené změny provedené v nemapovaných polích synchronizaci?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-139">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="e5c1a-140">Synchronizace dat řídí plán provedení.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-140">Data sync follows the execution schedule.</span></span> <span data-ttu-id="e5c1a-141">Integrace vyzvedne záznam, pokud se změní některé pole v záznamu, bez ohledu na to, zda je pole součástí mapování integrace.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-141">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="e5c1a-142">Jak se dají poslat pouze změny aktivního pracovníka a ne ukončené záznamy?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-142">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="e5c1a-143">S použitím "Rozšířeného dotazu" můžete filtrovat a měnit tvar zdrojových dat před předáním do cíle.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-143">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Rozšířený dotaz aktivních pracovníků](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="e5c1a-145">Můžu určit pole, která chcete odeslat do modulu Finance pro konkrétní entitu?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-145">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="e5c1a-146">Pole lze přidat nebo odebrat z úkolu integrace.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-146">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="e5c1a-147">Ne všechna datová pole, která existují na Dataverse budou doplněna z Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-147">Not all data fields that exist on the Dataverse table will be populated from Human Resources.</span></span>
<span data-ttu-id="e5c1a-148">Prostřednictvím Power Apps lze naplnit další data.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-148">Additional data can be populated via Power Apps.</span></span>

![Přidání do úkolu integrace a odstranění z něj](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="e5c1a-150">Mám nastavenou integraci jako dávkovou úlohu, ale aplikace Human Resources ztratila připojení do cílového systému.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-150">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="e5c1a-151">Jak se dá odeslat stejná sada změny do cílového systému?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-151">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="e5c1a-152">Není potřeba žádné speciální nastavení pro zpracování výjimek.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-152">No special setup is required for exception handling.</span></span> <span data-ttu-id="e5c1a-153">Integrátor dat automaticky zachytí a zaznamená chyby, které se objevují ve zdroji a cíli a umožní ruční opakování.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-153">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="e5c1a-154">Avšak nepovoluje ruční opravy dat.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-154">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="e5c1a-155">Pokud je nutné provést aktualizace dat, mělo by tak být provedeno ve zdroji nebo v cíli.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-155">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="e5c1a-156">Můžu nastavit integraci obousměrně?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-156">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="e5c1a-157">Ne, integrace je nyní jednosměrná (Human Resources do Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="e5c1a-157">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="e5c1a-158">Je však k dispozici výchozí šablona pro odeslání dat z aplikace Human Resources do Finance.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-158">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="e5c1a-159">Můžu povolit odstranění záznamu v rámci Moje integrace?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-159">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="e5c1a-160">Ne, integrátor dat nebude zaznamenávat odstraněné záznamy pro přenos dat.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-160">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="e5c1a-161">V současné době jsou zahrnuta pouze data vytvoření a aktualizace (UPSERT).</span><span class="sxs-lookup"><span data-stu-id="e5c1a-161">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="e5c1a-162">Můžu znovu spustit chybné spuštění?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-162">Can I rerun the errored execution?</span></span> <span data-ttu-id="e5c1a-163">Odešle se v takovém případě celý soubor nebo pouze změny?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-163">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="e5c1a-164">Při prvním spuštění aplikace Integrátor dat je vždy úplné spuštění.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-164">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="e5c1a-165">Dalším spuštění jsou založeny na sledování změn.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-165">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="e5c1a-166">Při chybě spuštění se záznamy v rozsahu spuštění extrahují a odešlou z Dataverse poslední změny.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-166">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Dataverse.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="e5c1a-167">Při ukládání projektu se zobrazila chybová zpráva: "Projekt obsahuje chyby mapování".</span><span class="sxs-lookup"><span data-stu-id="e5c1a-167">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="e5c1a-168">Co udělat?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-168">What do I do?</span></span>

<span data-ttu-id="e5c1a-169">Zkontrolujte nastavení klíčů integrace, proveďte požadované změny nastavení a aktualizujte entity v projektu.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-169">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="e5c1a-170">Při použití výchozí šablony budou integrační klíče automaticky importovány.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-170">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="e5c1a-171">K tomuto problému může dojít, když jsou do existující šablony přidány nové úkoly.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-171">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="e5c1a-172">Pokud mám nekonečný počet právnických osob, kde mají zaměstnanci zaměstnání, je nutné vytvořit mapování pro každý z nich?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-172">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="e5c1a-173">Ano, pro každou právnickou osobu v modulu Finance je nutný samostatný integrační projekt v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-173">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="e5c1a-174">Je třeba převést data, která nejsou součástí výchozí šablony od společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-174">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="e5c1a-175">Lze to provést?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-175">Can I do this?</span></span>

<span data-ttu-id="e5c1a-176">Ano, pole můžete přidat do existující šablony nebo z ní odebrat.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-176">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="e5c1a-177">Šablony lze upravit tak, aby obsahovaly další data z jiných tabulek Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-177">The template can be modified to include additional data from other Dataverse tables.</span></span> <span data-ttu-id="e5c1a-178">Entita musí být Dataverse, aby byla zahrnuta do šablony.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-178">The entity must be in Dataverse for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="e5c1a-179">Právě jsem vytvořil nová prostředí Finance a Human Resources a zobrazuje se chyba Hodnota data porušuje omezení integrity.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-179">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="e5c1a-180">Proč?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-180">Why?</span></span>

<span data-ttu-id="e5c1a-181">Důvody této chyby mohou zahrnovat:</span><span class="sxs-lookup"><span data-stu-id="e5c1a-181">Reasons for this error can include:</span></span>

- <span data-ttu-id="e5c1a-182">Převod dat měl za následek extrahování duplicitních záznamů ve zdroji (Dataverse).</span><span class="sxs-lookup"><span data-stu-id="e5c1a-182">The data transfer resulted in duplicate records extraction at the source (Dataverse).</span></span>

- <span data-ttu-id="e5c1a-183">Přenos dat má hodnoty null pro pole, která jsou v aplikaci Finance and Operations povinná.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-183">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="e5c1a-184">Ověřte data, která se jsou v Dataverse a splňují požadavky aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-184">Verify the data that is in Dataverse and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="e5c1a-185">Pokud došlo k chybám provedení a neproběhla synchronizace ID zaměstnance, jak lze najít úlohu historie s neúspěšným záznamem zaměstnance?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-185">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="e5c1a-186">Integrátor dat v modulu Finance vytvoří více projektů.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-186">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="e5c1a-187">Vztah mezi úlohou integrátoru dat a projektem Finance je jedna ku jedné.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-187">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="e5c1a-188">Sledujte čas od historie provedení integrátoru dat a hledejte projekt index - 1 v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-188">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="e5c1a-189">Pokud je číslo úlohy v integrátoru dat 9, index modulu operace Finance je 8.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-189">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="e5c1a-190">Zaznamenejte index úkolů z integrátoru dat (v tomto případě je to "9").</span><span class="sxs-lookup"><span data-stu-id="e5c1a-190">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![Zaznamenání indexu úkolů z integrátoru dat](media/CaptureTaskIndex.png)

2. <span data-ttu-id="e5c1a-192">Sledujte čas provádění projektu.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-192">Track the execution time of the project.</span></span>

    ![Sledování času provádění projektu.](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="e5c1a-194">V modulu finance určete index - 1.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-194">In Finance, identify index - 1.</span></span> <span data-ttu-id="e5c1a-195">V tomto příkladu projekt bude mít příponu 8 a čas provedení projektu indexu 0 odpovídá času provedení v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-195">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![Identifikace indexu](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="e5c1a-197">Po integraci aplikací Human Resources a Finance nevidím v aplikaci Finance žádná data z aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-197">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="e5c1a-198">Co udělat?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-198">What do I do?</span></span>

<span data-ttu-id="e5c1a-199">Integrace s aplikací Finance je proces ve dvou krocích.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-199">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="e5c1a-200">Nejprve ověřte, že jsou data aplikace Human Resources aktualizovaná a dostupná v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-200">First, verify that the Human Resources data is updated and available in Dataverse.</span></span> <span data-ttu-id="e5c1a-201">To je synchronizace v reálném čase a lze ji ověřit v Power Apps pohledem na data v rámci datových tabulek.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-201">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data tables.</span></span>

![Data v Dataverse](media/DataInCDS.png)

<span data-ttu-id="e5c1a-203">Pokud se data v Dataverse nezobrazují požadovaným způsobem, ověřte, že je entita v integraci podporovaná.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-203">If the data is not appearing as expected in Dataverse, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="e5c1a-204">Pokud chcete zahrnout do Dataverse další data, bude požadována změna na straně společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-204">To include additional data in Dataverse, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="e5c1a-205">Pokud je entita podporovaná a data jsou v Dataverse k dispozici, ověřte, zda je v integrátoru dat správné mapování.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-205">If the entity is supported and the data is available in Dataverse, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="e5c1a-206">Pokud se mapování integrátoru zdá v pořádně, ověřte, zda jsou úspěšně spuštěné úlohy správy dat.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-206">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="e5c1a-207">Během zpracování dávkových úloh může dojít k chybám.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-207">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="e5c1a-208">Další informace o způsobu použití nástroje pro správu dat naleznete v tématu [Správa dat](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="e5c1a-208">For more information about Data Management, see [Data management](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="e5c1a-209">Údaje o adrese mých zaměstnanců nejdou po importu do aplikace Finance správné.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-209">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="e5c1a-210">Co mám dělat?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-210">What should I do?</span></span>

<span data-ttu-id="e5c1a-211">Číselná řada pro **ID skladového místa** používá stejný vzorec v aplikacích Human Resources i Finance.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-211">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="e5c1a-212">Číselné řady musí být jedinečný na obou stranách tak, aby nebyla žádná kolize adres při integraci dat z Dataverse do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-212">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Dataverse to Finance and Operations.</span></span>

<span data-ttu-id="e5c1a-213">Při implementaci aplikace Human Resources ověřte, zda číselné řady v aplikaci Human Resources a Finance nejsou stejné.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-213">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="e5c1a-214">Ověřte, zda nejsou všechny číselné řady stejné, když lze udržovat data v obou systémech.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-214">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="e5c1a-215">Při vytvoření sady připojení nevidím připojení v rozevíracím seznamu připojení.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-215">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="e5c1a-216">Co udělat?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-216">What do I do?</span></span>

<span data-ttu-id="e5c1a-217">Při vytváření připojení zvolte Dynamics 365 Finance a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-217">Make sure when creating your connections, you choose Dynamics 365 Finance and Dataverse.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="e5c1a-218">Při synchronizaci zaměstnání se zobrazují chyby "CompanyInfo_FK neexistuje" nebo "Hodnota 31/12 a 2154 23:59:59: 00 ' v poli Koncové datum zaměstnání nebyla nalezena v související tabulce"Zaměstnání"." Co mám dělat?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-218">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="e5c1a-219">Mapujte na správné právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-219">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="e5c1a-220">Synchronizace právnické osoby není součástí výchozí šablony, takže se očekává, že každá právnická osoba přítomná v aplikacích Human Resources a Dataverse je dostupná také v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-220">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Dataverse is also present in Finance.</span></span>
<span data-ttu-id="e5c1a-221">Dále také vyberte správné právnické osoby pro přidruženou sadu připojení.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-221">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="e5c1a-222">Po nastavení projektu se zdá mapování polí pro Finance prázdné.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-222">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="e5c1a-223">Co mám dělat?</span><span class="sxs-lookup"><span data-stu-id="e5c1a-223">What should I do?</span></span>

<span data-ttu-id="e5c1a-224">Aktualizujte entity dat v aplikaci Finance v části **Správa dat \> Parametry systému \> Nastavení entity \> Aktualizovat seznam entit.**</span><span class="sxs-lookup"><span data-stu-id="e5c1a-224">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="e5c1a-225">Mělo by to trvat několik minut a poté by se mělo zobrazit toto mapování.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-225">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="e5c1a-226">K tomuto problému dochází při vytváření nových projektů.</span><span class="sxs-lookup"><span data-stu-id="e5c1a-226">This issue occurs when new projects are created.</span></span>

![Mapování chybějících polí](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="e5c1a-228">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e5c1a-228">Additional resources</span></span>

- <span data-ttu-id="e5c1a-229">Integrátor dat (Di):</span><span class="sxs-lookup"><span data-stu-id="e5c1a-229">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="e5c1a-230">Integrace dat do Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="e5c1a-230">Integrate data into Microsoft Dataverse</span></span>](/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="e5c1a-231">Správa chyb a řešení problémů integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="e5c1a-231">Data Integrator error management and troubleshooting</span></span>](/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="e5c1a-232">Odpovídání na požadavky DSR u systémem generovaných protokolů v Power Apps, Microsoft Power Automate a Dataverse</span><span class="sxs-lookup"><span data-stu-id="e5c1a-232">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Dataverse</span></span>](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="e5c1a-233">Správa dat:</span><span class="sxs-lookup"><span data-stu-id="e5c1a-233">Data Management:</span></span>

  - [<span data-ttu-id="e5c1a-234">Správa dat</span><span class="sxs-lookup"><span data-stu-id="e5c1a-234">Data management</span></span>](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
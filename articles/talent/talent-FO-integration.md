---
title: Nejčastější dotazy týkající se integrace aplikace Dynamics 365 for Talent s Dynamics 365 for Finance and Operations
description: Toto téma vysvětluje, jaká data jsou synchronizována v rámci integrace aplikací Talent a Finance and Operations.
author: negudava
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aea025bc4898d6399e82030cf1f52b21949e014f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303609"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a><span data-ttu-id="36d64-103">Nejčastější dotazy týkající se integrace aplikace Dynamics 365 for Talent s Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="36d64-103">Dynamics 365 for Talent to Dynamics 365 for Finance and Operations integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="36d64-104">Toto téma uvádí odpovědi na časté otázky spojené s tím, jaká data jsou synchronizována při integraci aplikace Dynamics 365 for Talent s Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36d64-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 for Talent is integrated with Dynamics 365 for Finance and Operations.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="36d64-105">Jsou synchronizovaná všechna data nebo jenom některé datové entity?</span><span class="sxs-lookup"><span data-stu-id="36d64-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="36d64-106">S aplikací Core Human Resources (HR) je synchronizována dílčí skupina dat.</span><span class="sxs-lookup"><span data-stu-id="36d64-106">With Core Human Resources (HR), a subset of the data is synchronized.</span></span> <span data-ttu-id="36d64-107">Seznam všech entit uvádí téma [Integrace z aplikace Dynamics 365 for Talent do Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="36d64-107">For a list of all the entities, see [Integration from Dynamics 365 for Talent to Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="36d64-108">V případě Attract a Onboard jsou všechna data nativní pro Common Data Service (CDS) pro aplikace.</span><span class="sxs-lookup"><span data-stu-id="36d64-108">For Attract and Onboard, all data is native to Common Data Services (CDS) for Apps.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="36d64-109">Je možné vytvořit nové mapování bez použití šablon</span><span class="sxs-lookup"><span data-stu-id="36d64-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="36d64-110">Šablony jsou počátečním bodem.</span><span class="sxs-lookup"><span data-stu-id="36d64-110">Templates are the starting point.</span></span> <span data-ttu-id="36d64-111">Můžete vytvořit vlastní šablonu, ale při vytváření projektu integrace je šablona potřeba vždy.</span><span class="sxs-lookup"><span data-stu-id="36d64-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="36d64-112">Další informace o šablonách integrátoru dat (DI) a projektech naleznete v tématu [Integrace dat v Common Data Service pro aplikace](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="36d64-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a><span data-ttu-id="36d64-113">Lze mapovat finanční dimenze k přenosu mezi aplikacemi Talent and Finance and Operations?</span><span class="sxs-lookup"><span data-stu-id="36d64-113">Can I map financial dimensions to transfer between Talent and Finance and Operations?</span></span>

<span data-ttu-id="36d64-114">Finanční dimenze aktuálně nejsou v CDS pro aplikace a proto nejsou součástí výchozí šablony.</span><span class="sxs-lookup"><span data-stu-id="36d64-114">Financial dimensions aren’t currently in CDS for Apps and as a result aren’t part of the default template.</span></span> <span data-ttu-id="36d64-115">Tato entita je plánována, ale v současné době není k dispozici žádná časová osa pro uvolnění.</span><span class="sxs-lookup"><span data-stu-id="36d64-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="36d64-116">V případě dat, která existují v modulu Finance and Operations, ale ne v aplikaci Talent, spojte tyto dva systémy pomocí příkazu **Konfigurovat odkazy** v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="36d64-116">For data that resides in Finance and Operations but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="36d64-117">Další informace o tom, jak konfigurovat propojení mezi aplikacemi Talent a Finance and Operations získáte v tématu [Co je nového nebo změněného v Dynamics 365 for Talent Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="36d64-117">For more information about how to configure links between Talent and Finance and Operations, see [What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a><span data-ttu-id="36d64-118">Někdy se stane, že když importuji zaměstnance, přejdou v modulu Finance and Operations mezi neaktivní zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="36d64-118">Sometimes when I import employees, they go into inactive workers in Finance and Operations.</span></span> <span data-ttu-id="36d64-119">Proč?</span><span class="sxs-lookup"><span data-stu-id="36d64-119">Why?</span></span>

<span data-ttu-id="36d64-120">Jestliže zaměstnanci nemají záznam podrobností o aktivním zaměstnání v aplikaci Talent může dojít k této chybě.</span><span class="sxs-lookup"><span data-stu-id="36d64-120">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="36d64-121">Chybu vyřešíte tak, že přejdete na položky **Správa zaměstnanců \> Zaměstnanci \> Historie zaměstnání \> Správce dat** a ověříte, že existuje aktivní záznam detailů zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="36d64-121">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="36d64-122">Pokud vyberu možnost mapovat pouze dílčí sadu polí, spustí provedené změny provedené v nemapovaných polích synchronizaci?</span><span class="sxs-lookup"><span data-stu-id="36d64-122">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="36d64-123">Synchronizace dat řídí plán provedení.</span><span class="sxs-lookup"><span data-stu-id="36d64-123">Data sync follows the execution schedule.</span></span> <span data-ttu-id="36d64-124">Integrace vyzvedne záznam, pokud se změní některé pole v záznamu, bez ohledu na to, zda je pole součástí mapování integrace.</span><span class="sxs-lookup"><span data-stu-id="36d64-124">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="36d64-125">Jak se dají poslat pouze změny aktivního pracovníka a ne ukončené záznamy?</span><span class="sxs-lookup"><span data-stu-id="36d64-125">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="36d64-126">S použitím "Rozšířeného dotazu" můžete filtrovat a měnit tvar zdrojových dat před předáním do cíle.</span><span class="sxs-lookup"><span data-stu-id="36d64-126">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a><span data-ttu-id="36d64-127">Můžu určit pole, která chcete odeslat do modulu Finance and Operations pro konkrétní entitu?</span><span class="sxs-lookup"><span data-stu-id="36d64-127">Can I specify which fields to send to Finance and Operations for a specific entity?</span></span>

<span data-ttu-id="36d64-128">Pole lze přidat nebo odebrat z úkolu integrace.</span><span class="sxs-lookup"><span data-stu-id="36d64-128">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="36d64-129">Ne všechna datová pole, která existují na CDS pro aplikace (CD 2.0) budou doplněna z Core HR.</span><span class="sxs-lookup"><span data-stu-id="36d64-129">Not all data fields that exist on the CDS for Apps (CDS 2.0) entity will be populated from Core HR.</span></span>
<span data-ttu-id="36d64-130">Prostřednictvím PowerApps lze naplnit další data.</span><span class="sxs-lookup"><span data-stu-id="36d64-130">Additional data can be populated via PowerApps.</span></span>

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="36d64-131">Mám nastavenou integraci jako dávkovou úlohu, ale Talent ztratil připojení do cílového systému.</span><span class="sxs-lookup"><span data-stu-id="36d64-131">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="36d64-132">Jak se dá odeslat stejná sada změny do cílového systému?</span><span class="sxs-lookup"><span data-stu-id="36d64-132">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="36d64-133">Není potřeba žádné speciální nastavení pro zpracování výjimek.</span><span class="sxs-lookup"><span data-stu-id="36d64-133">No special setup is required for exception handling.</span></span> <span data-ttu-id="36d64-134">Integrátor dat automaticky zachytí a zaznamená chyby, které se objevují ve zdroji a cíli a umožní ruční opakování.</span><span class="sxs-lookup"><span data-stu-id="36d64-134">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="36d64-135">Avšak nepovoluje ruční opravy dat.</span><span class="sxs-lookup"><span data-stu-id="36d64-135">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="36d64-136">Pokud je nutné provést aktualizace dat, mělo by se tak stát ve zdroji nebo v cíli.</span><span class="sxs-lookup"><span data-stu-id="36d64-136">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="36d64-137">Můžu nastavit integraci obousměrně?</span><span class="sxs-lookup"><span data-stu-id="36d64-137">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="36d64-138">Ne, integrace je v současné době jednosměrná (z aplikace Talent do aplikace Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="36d64-138">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="36d64-139">Je však k dispozici výchozí šablona pro odeslání dat z aplikace Talent do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36d64-139">However, there is a default template available to send data from Talent to Finance and Operations.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="36d64-140">Můžu povolit odstranění záznamu v rámci Moje integrace?</span><span class="sxs-lookup"><span data-stu-id="36d64-140">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="36d64-141">Ne, integrátor dat nebude zaznamenávat odstraněné záznamy pro přenos dat.</span><span class="sxs-lookup"><span data-stu-id="36d64-141">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="36d64-142">V současné době jsou zahrnuta pouze data vytvoření a aktualizace (UPSERT).</span><span class="sxs-lookup"><span data-stu-id="36d64-142">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="36d64-143">Můžu znovu spustit chybné spuštění?</span><span class="sxs-lookup"><span data-stu-id="36d64-143">Can I rerun the errored execution?</span></span> <span data-ttu-id="36d64-144">Odešle se v takovém případě celý soubor nebo pouze změny?</span><span class="sxs-lookup"><span data-stu-id="36d64-144">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="36d64-145">Při prvním spuštění aplikace Integrátor dat je vždy úplné spuštění.</span><span class="sxs-lookup"><span data-stu-id="36d64-145">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="36d64-146">Dalším spuštění jsou založeny na sledování změn.</span><span class="sxs-lookup"><span data-stu-id="36d64-146">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="36d64-147">Při chybě spuštění se záznamy v rozsahu spuštění extrahují a odešlou z CDS poslední změny.</span><span class="sxs-lookup"><span data-stu-id="36d64-147">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from CDS.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="36d64-148">Při ukládání projektu se zobrazila chybová zpráva: "Projekt obsahuje chyby mapování".</span><span class="sxs-lookup"><span data-stu-id="36d64-148">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="36d64-149">Co udělat?</span><span class="sxs-lookup"><span data-stu-id="36d64-149">What do I do?</span></span>

<span data-ttu-id="36d64-150">Zkontrolujte nastavení klíčů integrace, proveďte požadované změny nastavení a aktualizujte entity v projektu.</span><span class="sxs-lookup"><span data-stu-id="36d64-150">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="36d64-151">Při použití výchozí šablony budou integrační klíče automaticky importovány.</span><span class="sxs-lookup"><span data-stu-id="36d64-151">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="36d64-152">K tomuto problému může dojít, když jsou do existující šablony přidány nové úkoly.</span><span class="sxs-lookup"><span data-stu-id="36d64-152">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="36d64-153">Pokud mám nekonečný počet právnických osob, kde mají zaměstnanci zaměstnání, je nutné vytvořit mapování pro každý z nich?</span><span class="sxs-lookup"><span data-stu-id="36d64-153">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="36d64-154">Ano, pro každou právnickou osobu v modulu Finance and Operations je nutný samostatný integrační projekt v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="36d64-154">Yes, for each legal entity in Finance and Operations, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="36d64-155">Je třeba převést data, která nejsou součástí výchozí šablony od společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="36d64-155">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="36d64-156">Lze to provést?</span><span class="sxs-lookup"><span data-stu-id="36d64-156">Can I do this?</span></span>

<span data-ttu-id="36d64-157">Ano, pole můžete přidat do existující šablony nebo z ní odebrat.</span><span class="sxs-lookup"><span data-stu-id="36d64-157">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="36d64-158">Šablony lze upravit tak, aby obsahovaly další data z jiných entit aplikací CDS.</span><span class="sxs-lookup"><span data-stu-id="36d64-158">The template can be modified to include additional data from other CDS for Apps entities.</span></span> <span data-ttu-id="36d64-159">Entita musí být v CDS pro aplikace, aby byla zahrnuta do šablony.</span><span class="sxs-lookup"><span data-stu-id="36d64-159">The entity must be in CDS for Apps for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="36d64-160">Právě jsem vytvořil nová prostředí Finance and Operations a Talent a zobrazuje se chyba Hodnota data porušuje omezení integrity.</span><span class="sxs-lookup"><span data-stu-id="36d64-160">I just created new Finance and Operations and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="36d64-161">Proč?</span><span class="sxs-lookup"><span data-stu-id="36d64-161">Why?</span></span>

<span data-ttu-id="36d64-162">Důvody této chyby mohou zahrnovat:</span><span class="sxs-lookup"><span data-stu-id="36d64-162">Reasons for this error can include:</span></span>

- <span data-ttu-id="36d64-163">Převod dat měl za následek extrahování duplicitních záznamů ve zdroji (CD).</span><span class="sxs-lookup"><span data-stu-id="36d64-163">The data transfer resulted in duplicate records extraction at the source (CDS).</span></span>

- <span data-ttu-id="36d64-164">Přenos dat má hodnoty null pro pole, která jsou v aplikaci Finance and Operations povinná.</span><span class="sxs-lookup"><span data-stu-id="36d64-164">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="36d64-165">Ověřte data, která se jsou v CDS a splňují požadavky modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36d64-165">Verify the data that is in CDS and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="36d64-166">Pokud došlo k chybám provedení a neproběhla synchronizace ID zaměstnance, jak lze najít úlohu historie s neúspěšným záznamem zaměstnance?</span><span class="sxs-lookup"><span data-stu-id="36d64-166">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="36d64-167">Integrátor dat v modulu Finance and Operations vytvoří více projektů.</span><span class="sxs-lookup"><span data-stu-id="36d64-167">Data Integrator will create multiple projects in Finance and Operations.</span></span> <span data-ttu-id="36d64-168">Vztah mezi úlohou integrátoru dat a projektem Finance and Operations je jedna ku jedné.</span><span class="sxs-lookup"><span data-stu-id="36d64-168">The relationship between the Data Integrator task and the Finance and Operations project is one to one.</span></span>

<span data-ttu-id="36d64-169">Sledujte čas od historie provedení integrátoru dat a hledejte projekt index - 1 v modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36d64-169">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance and Operations.</span></span> <span data-ttu-id="36d64-170">Pokud je číslo úlohy v integrátoru dat 9, index modulu operace Finance and Operations je 8.</span><span class="sxs-lookup"><span data-stu-id="36d64-170">If the task number is 9 in Data Integrator, the index in Finance and Operations is 8.</span></span>

1. <span data-ttu-id="36d64-171">Zaznamenejte index úkolů z integrátoru dat (v tomto případě je to "9").</span><span class="sxs-lookup"><span data-stu-id="36d64-171">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![Zaznamenání indexu úkolů z integrátoru dat](media/CaptureTaskIndex.png)

2. <span data-ttu-id="36d64-173">Sledujte čas provádění projektu.</span><span class="sxs-lookup"><span data-stu-id="36d64-173">Track the execution time of the project.</span></span>

![Sledování času provádění projektu.](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="36d64-175">V aplikaci Finance and Operations vyhledejte index -1.</span><span class="sxs-lookup"><span data-stu-id="36d64-175">In Finance and Operations, identify index - 1.</span></span> <span data-ttu-id="36d64-176">V tomto příkladu projekt bude mít příponu 8 a čas provedení projektu indexu 0 odpovídá času provedení v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="36d64-176">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![Identifikace indexu](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a><span data-ttu-id="36d64-178">Po integraci aplikací Talent a Finance and Operations nevidím data Talent v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36d64-178">After integrating Talent and Finance and Operations, I don’t see my Talent data in Finance and Operations.</span></span> <span data-ttu-id="36d64-179">Co udělat?</span><span class="sxs-lookup"><span data-stu-id="36d64-179">What do I do?</span></span>

<span data-ttu-id="36d64-180">Integrace s aplikací Finance and Operations je proces ve dvou krocích.</span><span class="sxs-lookup"><span data-stu-id="36d64-180">The integration to Finance and Operations is a two-step process.</span></span> <span data-ttu-id="36d64-181">Nejprve ověřte, že jsou data aplikace Talent aktualizovaná a dostupná v CDS.</span><span class="sxs-lookup"><span data-stu-id="36d64-181">First, verify that the Talent data is updated and available in CDS.</span></span> <span data-ttu-id="36d64-182">To je synchronizace v reálném čase a lze ji ověřit v PowerApps pohledem na data v rámci datových entit.</span><span class="sxs-lookup"><span data-stu-id="36d64-182">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Data v CDS](media/DataInCDS.png)

<span data-ttu-id="36d64-184">Pokud se data v CDS nezobrazují požadovaným způsobem, ověřte, že je entita v integraci podporovaná.</span><span class="sxs-lookup"><span data-stu-id="36d64-184">If the data is not appearing as expected in CDS, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="36d64-185">Pokud chcete zahrnout do CDS další data, bude požadována změna na straně společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="36d64-185">To include additional data in CDS, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="36d64-186">Pokud je entita podporovaná a data jsou v CDS k dispozici, ověřte, zda je v integrátoru dat správné mapování.</span><span class="sxs-lookup"><span data-stu-id="36d64-186">If the entity is supported and the data is available in CDS, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="36d64-187">Pokud se mapování integrátoru zdá v pořádně, ověřte, zda jsou úspěšně spuštěné úlohy správy dat.</span><span class="sxs-lookup"><span data-stu-id="36d64-187">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="36d64-188">Během zpracování dávkových úloh může dojít k chybám.</span><span class="sxs-lookup"><span data-stu-id="36d64-188">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="36d64-189">Další informace o způsobu použití nástroje pro správu dat naleznete v tématu [Správa dat](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="36d64-189">For more information about Data Management, see [Data management](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a><span data-ttu-id="36d64-190">Údaje o adrese mých zaměstnanců nejdou po importu do aplikace Finance and Operations správné.</span><span class="sxs-lookup"><span data-stu-id="36d64-190">The addresses for my employees are incorrect after I import them into Finance and Operations.</span></span> <span data-ttu-id="36d64-191">Co mám dělat?</span><span class="sxs-lookup"><span data-stu-id="36d64-191">What should I do?</span></span>

<span data-ttu-id="36d64-192">Číselná řada pro **ID skladového místa** používá stejný vzorec v aplikacích Talent i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36d64-192">The number sequence for **Location ID** uses the same pattern in both Talent and Finance and Operations.</span></span> <span data-ttu-id="36d64-193">Číselné řady musí být jedinečný na obou stranách tak, aby nebyla žádná kolize adres při integraci dat z CDS do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36d64-193">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from CDS to Finance and Operations.</span></span>

<span data-ttu-id="36d64-194">Při implementaci aplikace Talent ověřte, zda číselné řady v aplikaci Talent a Finance and Operations nejsou stejné.</span><span class="sxs-lookup"><span data-stu-id="36d64-194">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance and Operations.</span></span> <span data-ttu-id="36d64-195">Ověřte, zda nejsou všechny číselné řady stejné, když lze udržovat data v obou systémech.</span><span class="sxs-lookup"><span data-stu-id="36d64-195">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="36d64-196">Při vytvoření sady připojení nevidím připojení v rozevíracím seznamu připojení.</span><span class="sxs-lookup"><span data-stu-id="36d64-196">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="36d64-197">Co udělat?</span><span class="sxs-lookup"><span data-stu-id="36d64-197">What do I do?</span></span>

<span data-ttu-id="36d64-198">Při vytváření připojení zvolte Dynamics 365 for Finance and Operations (aktuálně v náhledu) a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="36d64-198">Make sure when creating your connections, you choose Dynamics 365 for Finance and Operations (currently in preview) and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="36d64-199">Při synchronizaci zaměstnání se zobrazují chyby "CompanyInfo_FK neexistuje" nebo "Hodnota 31/12 a 2154 23:59:59: 00 ' v poli Koncové datum zaměstnání nebyla nalezena v související tabulce"Zaměstnání"." Co mám dělat?</span><span class="sxs-lookup"><span data-stu-id="36d64-199">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="36d64-200">Mapujte na správné právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="36d64-200">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="36d64-201">Synchronizace právnické osoby není součástí výchozí šablony, takže se očekává, že každá právnická osoba přítomná v aplikacích Talent a CDS je dostupná také v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="36d64-201">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and CDS is also present in Finance and Operations.</span></span>
<span data-ttu-id="36d64-202">Dále také vyberte správné právnické osoby pro přidruženou sadu připojení.</span><span class="sxs-lookup"><span data-stu-id="36d64-202">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="36d64-203">Po nastavení projektu se zdá mapování polí pro Finance and Operations prázdné.</span><span class="sxs-lookup"><span data-stu-id="36d64-203">After setting up my project, the field mapping for Finance and Operations appears to be empty.</span></span> <span data-ttu-id="36d64-204">Co mám dělat?</span><span class="sxs-lookup"><span data-stu-id="36d64-204">What should I do?</span></span>

<span data-ttu-id="36d64-205">Aktualizujte entity dat v aplikaci Finance and Operations v části **Správa dat \> Parametry systému \> Nastavení entity \> Aktualizovat seznam entit.**</span><span class="sxs-lookup"><span data-stu-id="36d64-205">Refresh the data entities in Finance and Operations by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="36d64-206">Mělo by to trvat několik minut a poté by se mělo zobrazit toto mapování.</span><span class="sxs-lookup"><span data-stu-id="36d64-206">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="36d64-207">K tomuto problému dochází při vytváření nových projektů.</span><span class="sxs-lookup"><span data-stu-id="36d64-207">This issue occurs when new projects are created.</span></span>

![Mapování chybějících polí](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="36d64-209">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="36d64-209">Additional resources</span></span>

- <span data-ttu-id="36d64-210">Integrátor dat (Di):</span><span class="sxs-lookup"><span data-stu-id="36d64-210">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="36d64-211">Integrace dat do Common Data Service for Apps</span><span class="sxs-lookup"><span data-stu-id="36d64-211">Integrate data into Common Data Service for Apps</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="36d64-212">Správa chyb a řešení problémů integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="36d64-212">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="36d64-213">Odpovídání na požadavky DSR u systémem generovaných protokolů v PowerApps, Microsoft Flow a Common Data Service for Apps</span><span class="sxs-lookup"><span data-stu-id="36d64-213">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service for Apps</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="36d64-214">Správa dat:</span><span class="sxs-lookup"><span data-stu-id="36d64-214">Data Management:</span></span>

  - [<span data-ttu-id="36d64-215">Správa dat</span><span class="sxs-lookup"><span data-stu-id="36d64-215">Data management</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
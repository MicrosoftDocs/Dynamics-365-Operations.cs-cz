---
title: Nejčastější dotazy týkající se integrace aplikace Dynamics 365 Talent s Dynamics 365 Finance
description: Toto téma vysvětluje, jaká data jsou synchronizována v rámci integrace aplikací Talent a Finance.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5bb855e6dd7ff236b7bda9e59e12ed8cc8ab9bc9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251007"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a><span data-ttu-id="4ed1b-103">Nejčastější dotazy týkající se integrace aplikace Dynamics 365 Talent s Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="4ed1b-103">Dynamics 365 Talent to Dynamics 365 Finance integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4ed1b-104">Toto téma uvádí odpovědi na časté otázky spojené s tím, jaká data jsou synchronizována při integraci aplikace Dynamics 365 Talent s Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Talent is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="4ed1b-105">Jsou synchronizovaná všechna data nebo jenom některé datové entity?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="4ed1b-106">S aplikací Core HR je synchronizována dílčí skupina dat.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-106">For Core HR, a subset of the data is synchronized.</span></span> <span data-ttu-id="4ed1b-107">Seznam všech entit uvádí téma [Integrace z aplikace Dynamics 365 Talent do Dynamics 365 Finance](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-107">For a list of all the entities, see [Integration from Dynamics 365 Talent to Dynamics 365 Finance](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="4ed1b-108">V případě Attract a Onboard jsou všechna data nativní pro Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="4ed1b-109">Je možné vytvořit nové mapování bez použití šablon</span><span class="sxs-lookup"><span data-stu-id="4ed1b-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="4ed1b-110">Šablony jsou počátečním bodem.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-110">Templates are the starting point.</span></span> <span data-ttu-id="4ed1b-111">Můžete vytvořit vlastní šablonu, ale při vytváření projektu integrace je šablona potřeba vždy.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="4ed1b-112">Další informace o šablonách integrátoru dat (DI) a projektech naleznete v tématu [Integrace dat v Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a><span data-ttu-id="4ed1b-113">Lze mapovat finanční dimenze k přenosu mezi aplikacemi Talent a Finance?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-113">Can I map financial dimensions to transfer between Talent and Finance?</span></span>

<span data-ttu-id="4ed1b-114">Finanční dimenze aktuálně nejsou v Common Data Service pro aplikace a proto nejsou součástí výchozí šablony.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-114">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="4ed1b-115">Tato entita je plánována, ale v současné době není k dispozici žádná časová osa pro uvolnění.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="4ed1b-116">V případě dat, která existují v modulu Finance, ale ne v aplikaci Talent, spojte tyto dva systémy pomocí příkazu **Konfigurovat odkazy** v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-116">For data that resides in Finance but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="4ed1b-117">Další informace o tom, jak konfigurovat propojení mezi aplikacemi Talent a Finance získáte v tématu [Co je nového nebo změněného v Dynamics 365 Talent: Core HR Core HR (31. října 2018)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-117">For more information about how to configure links between Talent and Finance, see [What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![Mapovat finanční dimenze](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="4ed1b-119">Někdy se stane, že když importuji zaměstnance, přejdou v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-119">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="4ed1b-120">Proč?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-120">Why?</span></span>

<span data-ttu-id="4ed1b-121">Jestliže zaměstnanci nemají záznam podrobností o aktivním zaměstnání v aplikaci Talent může dojít k této chybě.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-121">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="4ed1b-122">Chybu vyřešíte tak, že přejdete na položky **Správa zaměstnanců \> Zaměstnanci \> Historie zaměstnání \> Správce dat** a ověříte, že existuje aktivní záznam detailů zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-122">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="4ed1b-123">Pokud vyberu možnost mapovat pouze dílčí sadu polí, spustí provedené změny provedené v nemapovaných polích synchronizaci?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-123">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="4ed1b-124">Synchronizace dat řídí plán provedení.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-124">Data sync follows the execution schedule.</span></span> <span data-ttu-id="4ed1b-125">Integrace vyzvedne záznam, pokud se změní některé pole v záznamu, bez ohledu na to, zda je pole součástí mapování integrace.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-125">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="4ed1b-126">Jak se dají poslat pouze změny aktivního pracovníka a ne ukončené záznamy?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-126">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="4ed1b-127">S použitím "Rozšířeného dotazu" můžete filtrovat a měnit tvar zdrojových dat před předáním do cíle.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-127">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Rozšířený dotaz aktivních pracovníků](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="4ed1b-129">Můžu určit pole, která chcete odeslat do modulu Finance pro konkrétní entitu?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-129">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="4ed1b-130">Pole lze přidat nebo odebrat z úkolu integrace.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-130">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="4ed1b-131">Ne všechna datová pole, která existují na Common Data Service budou doplněna z Core HR.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-131">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="4ed1b-132">Prostřednictvím PowerApps lze naplnit další data.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-132">Additional data can be populated via PowerApps.</span></span>

![Přidání do úkolu integrace a odstranění z něj](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="4ed1b-134">Mám nastavenou integraci jako dávkovou úlohu, ale Talent ztratil připojení do cílového systému.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-134">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="4ed1b-135">Jak se dá odeslat stejná sada změny do cílového systému?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-135">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="4ed1b-136">Není potřeba žádné speciální nastavení pro zpracování výjimek.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-136">No special setup is required for exception handling.</span></span> <span data-ttu-id="4ed1b-137">Integrátor dat automaticky zachytí a zaznamená chyby, které se objevují ve zdroji a cíli a umožní ruční opakování.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-137">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="4ed1b-138">Avšak nepovoluje ruční opravy dat.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-138">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="4ed1b-139">Pokud je nutné provést aktualizace dat, mělo by se tak stát ve zdroji nebo v cíli.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-139">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="4ed1b-140">Můžu nastavit integraci obousměrně?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-140">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="4ed1b-141">Ne, integrace je v současné době jednosměrná (z aplikace Talent do aplikace Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-141">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="4ed1b-142">Je však k dispozici výchozí šablona pro odeslání dat z aplikace Talent do Finance.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-142">However, there is a default template available to send data from Talent to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="4ed1b-143">Můžu povolit odstranění záznamu v rámci Moje integrace?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-143">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="4ed1b-144">Ne, integrátor dat nebude zaznamenávat odstraněné záznamy pro přenos dat.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-144">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="4ed1b-145">V současné době jsou zahrnuta pouze data vytvoření a aktualizace (UPSERT).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-145">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="4ed1b-146">Můžu znovu spustit chybné spuštění?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-146">Can I rerun the errored execution?</span></span> <span data-ttu-id="4ed1b-147">Odešle se v takovém případě celý soubor nebo pouze změny?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-147">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="4ed1b-148">Při prvním spuštění aplikace Integrátor dat je vždy úplné spuštění.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-148">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="4ed1b-149">Dalším spuštění jsou založeny na sledování změn.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-149">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="4ed1b-150">Při chybě spuštění se záznamy v rozsahu spuštění extrahují a odešlou z Common Data Service poslední změny.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-150">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="4ed1b-151">Při ukládání projektu se zobrazila chybová zpráva: "Projekt obsahuje chyby mapování".</span><span class="sxs-lookup"><span data-stu-id="4ed1b-151">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="4ed1b-152">Co udělat?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-152">What do I do?</span></span>

<span data-ttu-id="4ed1b-153">Zkontrolujte nastavení klíčů integrace, proveďte požadované změny nastavení a aktualizujte entity v projektu.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-153">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="4ed1b-154">Při použití výchozí šablony budou integrační klíče automaticky importovány.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-154">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="4ed1b-155">K tomuto problému může dojít, když jsou do existující šablony přidány nové úkoly.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-155">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="4ed1b-156">Pokud mám nekonečný počet právnických osob, kde mají zaměstnanci zaměstnání, je nutné vytvořit mapování pro každý z nich?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-156">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="4ed1b-157">Ano, pro každou právnickou osobu v modulu Finance je nutný samostatný integrační projekt v integraci dat.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-157">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="4ed1b-158">Je třeba převést data, která nejsou součástí výchozí šablony od společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-158">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="4ed1b-159">Lze to provést?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-159">Can I do this?</span></span>

<span data-ttu-id="4ed1b-160">Ano, pole můžete přidat do existující šablony nebo z ní odebrat.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-160">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="4ed1b-161">Šablony lze upravit tak, aby obsahovaly další data z jiných entit Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-161">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="4ed1b-162">Entita musí být Common Data Service, aby byla zahrnuta do šablony.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-162">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="4ed1b-163">Právě jsem vytvořil nová prostředí Finance a Talent a zobrazuje se chyba Hodnota data porušuje omezení integrity.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-163">I just created new Finance and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="4ed1b-164">Proč?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-164">Why?</span></span>

<span data-ttu-id="4ed1b-165">Důvody této chyby mohou zahrnovat:</span><span class="sxs-lookup"><span data-stu-id="4ed1b-165">Reasons for this error can include:</span></span>

- <span data-ttu-id="4ed1b-166">Převod dat měl za následek extrahování duplicitních záznamů ve zdroji (Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-166">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="4ed1b-167">Přenos dat má hodnoty null pro pole, která jsou v aplikaci Finance and Operations povinná.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-167">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="4ed1b-168">Ověřte data, která se jsou v Common Data Service a splňují požadavky aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-168">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="4ed1b-169">Pokud došlo k chybám provedení a neproběhla synchronizace ID zaměstnance, jak lze najít úlohu historie s neúspěšným záznamem zaměstnance?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-169">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="4ed1b-170">Integrátor dat v modulu Finance vytvoří více projektů.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-170">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="4ed1b-171">Vztah mezi úlohou integrátoru dat a projektem Finance je jedna ku jedné.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-171">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="4ed1b-172">Sledujte čas od historie provedení integrátoru dat a hledejte projekt index - 1 v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-172">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="4ed1b-173">Pokud je číslo úlohy v integrátoru dat 9, index modulu operace Finance je 8.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-173">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="4ed1b-174">Zaznamenejte index úkolů z integrátoru dat (v tomto případě je to "9").</span><span class="sxs-lookup"><span data-stu-id="4ed1b-174">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![Zaznamenání indexu úkolů z integrátoru dat](media/CaptureTaskIndex.png)

2. <span data-ttu-id="4ed1b-176">Sledujte čas provádění projektu.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-176">Track the execution time of the project.</span></span>

![Sledování času provádění projektu.](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="4ed1b-178">V modulu finance určete index - 1.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-178">In Finance, identify index - 1.</span></span> <span data-ttu-id="4ed1b-179">V tomto příkladu projekt bude mít příponu 8 a čas provedení projektu indexu 0 odpovídá času provedení v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-179">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![Identifikace indexu](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a><span data-ttu-id="4ed1b-181">Po integraci aplikací Talent a Finance nevidím data Talent v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-181">After integrating Talent and Finance, I don’t see my Talent data in Finance.</span></span> <span data-ttu-id="4ed1b-182">Co udělat?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-182">What do I do?</span></span>

<span data-ttu-id="4ed1b-183">Integrace s aplikací Finance je proces ve dvou krocích.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-183">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="4ed1b-184">Nejprve ověřte, že jsou data aplikace Talent aktualizovaná a dostupná v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-184">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="4ed1b-185">To je synchronizace v reálném čase a lze ji ověřit v PowerApps pohledem na data v rámci datových entit.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-185">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Data v Common Data Service](media/DataInCDS.png)

<span data-ttu-id="4ed1b-187">Pokud se data v Common Data Service nezobrazují požadovaným způsobem, ověřte, že je entita v integraci podporovaná.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-187">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="4ed1b-188">Pokud chcete zahrnout do Common Data Service další data, bude požadována změna na straně společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-188">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="4ed1b-189">Pokud je entita podporovaná a data jsou v Common Data Service k dispozici, ověřte, zda je v integrátoru dat správné mapování.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-189">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="4ed1b-190">Pokud se mapování integrátoru zdá v pořádně, ověřte, zda jsou úspěšně spuštěné úlohy správy dat.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-190">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="4ed1b-191">Během zpracování dávkových úloh může dojít k chybám.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-191">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="4ed1b-192">Další informace o způsobu použití nástroje pro správu dat naleznete v tématu [Správa dat](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="4ed1b-192">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="4ed1b-193">Údaje o adrese mých zaměstnanců nejdou po importu do aplikace Finance správné.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-193">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="4ed1b-194">Co mám dělat?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-194">What should I do?</span></span>

<span data-ttu-id="4ed1b-195">Číselná řada pro **ID skladového místa** používá stejný vzorec v aplikacích Talent i Finance.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-195">The number sequence for **Location ID** uses the same pattern in both Talent and Finance.</span></span> <span data-ttu-id="4ed1b-196">Číselné řady musí být jedinečný na obou stranách tak, aby nebyla žádná kolize adres při integraci dat z Common Data Service do Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-196">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="4ed1b-197">Při implementaci aplikace Talent ověřte, zda číselné řady v aplikaci Talent a Finance nejsou stejné.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-197">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance.</span></span> <span data-ttu-id="4ed1b-198">Ověřte, zda nejsou všechny číselné řady stejné, když lze udržovat data v obou systémech.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-198">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="4ed1b-199">Při vytvoření sady připojení nevidím připojení v rozevíracím seznamu připojení.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-199">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="4ed1b-200">Co udělat?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-200">What do I do?</span></span>

<span data-ttu-id="4ed1b-201">Při vytváření připojení zvolte Dynamics 365 Finance a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-201">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="4ed1b-202">Při synchronizaci zaměstnání se zobrazují chyby "CompanyInfo_FK neexistuje" nebo "Hodnota 31/12 a 2154 23:59:59: 00 ' v poli Koncové datum zaměstnání nebyla nalezena v související tabulce"Zaměstnání"." Co mám dělat?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-202">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="4ed1b-203">Mapujte na správné právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-203">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="4ed1b-204">Synchronizace právnické osoby není součástí výchozí šablony, takže se očekává, že každá právnická osoba přítomná v aplikacích Talent a Common Data Service je dostupná také v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-204">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="4ed1b-205">Dále také vyberte správné právnické osoby pro přidruženou sadu připojení.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-205">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="4ed1b-206">Po nastavení projektu se zdá mapování polí pro Finance prázdné.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-206">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="4ed1b-207">Co mám dělat?</span><span class="sxs-lookup"><span data-stu-id="4ed1b-207">What should I do?</span></span>

<span data-ttu-id="4ed1b-208">Aktualizujte entity dat v aplikaci Finance v části **Správa dat \> Parametry systému \> Nastavení entity \> Aktualizovat seznam entit.**</span><span class="sxs-lookup"><span data-stu-id="4ed1b-208">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="4ed1b-209">Mělo by to trvat několik minut a poté by se mělo zobrazit toto mapování.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-209">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="4ed1b-210">K tomuto problému dochází při vytváření nových projektů.</span><span class="sxs-lookup"><span data-stu-id="4ed1b-210">This issue occurs when new projects are created.</span></span>

![Mapování chybějících polí](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="4ed1b-212">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="4ed1b-212">Additional resources</span></span>

- <span data-ttu-id="4ed1b-213">Integrátor dat (Di):</span><span class="sxs-lookup"><span data-stu-id="4ed1b-213">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="4ed1b-214">Integrace dat do Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4ed1b-214">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="4ed1b-215">Správa chyb a řešení problémů integrátoru dat</span><span class="sxs-lookup"><span data-stu-id="4ed1b-215">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="4ed1b-216">Odpovídání na požadavky DSR u systémem generovaných protokolů v PowerApps, Microsoft Flow a Common Data Service</span><span class="sxs-lookup"><span data-stu-id="4ed1b-216">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="4ed1b-217">Správa dat:</span><span class="sxs-lookup"><span data-stu-id="4ed1b-217">Data Management:</span></span>

  - [<span data-ttu-id="4ed1b-218">Správa dat</span><span class="sxs-lookup"><span data-stu-id="4ed1b-218">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)

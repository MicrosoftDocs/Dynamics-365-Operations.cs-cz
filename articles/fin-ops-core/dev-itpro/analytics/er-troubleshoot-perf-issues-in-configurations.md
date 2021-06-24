---
title: Odstraňování problémů s výkonem v konfiguracích ER
description: Toto téma vysvětluje, jak najít a opravit problémy s výkonem v konfiguracích Elektronického výkaznictví (ER).
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216858"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="ff235-103">Odstraňování problémů s výkonem v konfiguracích ER</span><span class="sxs-lookup"><span data-stu-id="ff235-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="ff235-104">Toto téma vysvětluje, jak najít a vyřešit problémy s výkonem v [konfiguracích](general-electronic-reporting.md#Configuration) [Elektronického výkaznictví](general-electronic-reporting.md) (ER).</span><span class="sxs-lookup"><span data-stu-id="ff235-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="ff235-105">Vyšetřování problémů s výkonem se obvykle skládá z několika kroků.</span><span class="sxs-lookup"><span data-stu-id="ff235-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="ff235-106">[Sběr](#collecting-data) dat.</span><span class="sxs-lookup"><span data-stu-id="ff235-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="ff235-107">Analýza shromážděných dat.</span><span class="sxs-lookup"><span data-stu-id="ff235-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="ff235-108">Na základě výsledků analýzy použijte konfigurace ER k [provedené změn](#making-changes) nebo se rozhodnete shromáždit více údajů.</span><span class="sxs-lookup"><span data-stu-id="ff235-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ff235-109">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="ff235-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="ff235-110">Analyzujte čas provedení</span><span class="sxs-lookup"><span data-stu-id="ff235-110">Analyze execution time</span></span>

<span data-ttu-id="ff235-111">Čas spuštění může záviset na nepředvídatelných faktorech, jako jsou jiné úkoly spuštěné ve stejném prostředí a ukládání do mezipaměti, které používá data při prvním volání.</span><span class="sxs-lookup"><span data-stu-id="ff235-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="ff235-112">Proto byste měli provádění a měření několikrát opakovat.</span><span class="sxs-lookup"><span data-stu-id="ff235-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="ff235-113">Někdy nejsou problémy s výkonem způsobeny konfigurací formátu ER, která se používá pro vytváření sestav.</span><span class="sxs-lookup"><span data-stu-id="ff235-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="ff235-114">Místo toho jsou způsobeny kódem X++, který se používá k otevření konfigurace formátu ER.</span><span class="sxs-lookup"><span data-stu-id="ff235-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="ff235-115">V [Centru akcí](#infolog-time) nebo [protokolu událostí](#event-log-time) se podívejte na čas provedení sestavy.</span><span class="sxs-lookup"><span data-stu-id="ff235-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="ff235-116">Porovnejte čas provedení sestavy s celkovou dobou provedení ve scénáři.</span><span class="sxs-lookup"><span data-stu-id="ff235-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="ff235-117">Pokud je doba spuštění sestavy mnohem kratší než celková doba provedení, zvažte množství dat, která sestava zpracovává:</span><span class="sxs-lookup"><span data-stu-id="ff235-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="ff235-118">Pokud sestava zpracovává malé množství dat, problém může zahrnovat dobu načítání konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ff235-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="ff235-119">Pokud sestava zpracovává velké množství dat, problém může zahrnovat předzpracování X++.</span><span class="sxs-lookup"><span data-stu-id="ff235-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="ff235-120">Použijte [Trace parser](#analyze-trace-parser-trace) k analýze tohoto případu.</span><span class="sxs-lookup"><span data-stu-id="ff235-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="ff235-121">V ostatních případech viz další části.</span><span class="sxs-lookup"><span data-stu-id="ff235-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="ff235-122">Spusťte více testů, které zahrnují různá množství dat, abyste zjistili, jak čas provedení závisí na množství dat.</span><span class="sxs-lookup"><span data-stu-id="ff235-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="ff235-123">Analýza trasování Trace parseru</span><span class="sxs-lookup"><span data-stu-id="ff235-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="ff235-124">Připravte si malý příklad nebo shromážděte několik tras během náhodných částí generování sestavy.</span><span class="sxs-lookup"><span data-stu-id="ff235-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="ff235-125">Pak v [Trace parseru](#trace-parser) proveďte standardní analýzu zdola nahoru a odpovězte na následující otázky:</span><span class="sxs-lookup"><span data-stu-id="ff235-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="ff235-126">Jaké jsou nejlepší metody z hlediska spotřeby času?</span><span class="sxs-lookup"><span data-stu-id="ff235-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="ff235-127">Jakou část celkového času tyto metody používají?</span><span class="sxs-lookup"><span data-stu-id="ff235-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="ff235-128">Na dotazy odpovídejte na stejné otázky.</span><span class="sxs-lookup"><span data-stu-id="ff235-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="ff235-129">Pokud uvidíte, že před metodami je uvedeno „ER“, přejděte k další části.</span><span class="sxs-lookup"><span data-stu-id="ff235-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="ff235-130">Pokud vidíte, že metody nebo dotazy pocházejí z aplikační sady, zvažte obecné optimalizace (například vytvořte indexy).</span><span class="sxs-lookup"><span data-stu-id="ff235-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="ff235-131">Analyzujte počet hovorů.</span><span class="sxs-lookup"><span data-stu-id="ff235-131">Analyze the number of calls.</span></span> <span data-ttu-id="ff235-132">Pokud je počet výrazně vyšší, než se očekávalo, zvažte uložení do mezipaměti odpovídajících uzlů konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ff235-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="ff235-133">Analyzujte volání databáze</span><span class="sxs-lookup"><span data-stu-id="ff235-133">Analyze database calls</span></span>

<span data-ttu-id="ff235-134">Připravte si příklad, který obsahuje malé množství dat, abyste mohli shromáždit [trasování ER](#electronic-reporting-traces).</span><span class="sxs-lookup"><span data-stu-id="ff235-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="ff235-135">Poté otevřete trasování v návrháři mapování modelů ER a podívejte se na spodní část stránky.</span><span class="sxs-lookup"><span data-stu-id="ff235-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="ff235-136">Odpovězte na následující otázky:</span><span class="sxs-lookup"><span data-stu-id="ff235-136">Answer the following questions:</span></span>

- <span data-ttu-id="ff235-137">Existuje nějaká duplikace dotazu?</span><span class="sxs-lookup"><span data-stu-id="ff235-137">Is there any query duplication?</span></span> <span data-ttu-id="ff235-138">Pokud existuje, zvažte jednu z následujících oprav:</span><span class="sxs-lookup"><span data-stu-id="ff235-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="ff235-139">[Použijte ukládání do mezipaměti](#use-caching), pokud si myslíte, že uvnitř jednoho nadřazeného záznamu je několik volání.</span><span class="sxs-lookup"><span data-stu-id="ff235-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="ff235-140">[Použijte parametrizované vypočítané pole v mezipaměti](#cached-parameterized), pokud si myslíte, že existují volání stejného záznamu v různých záznamech.</span><span class="sxs-lookup"><span data-stu-id="ff235-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="ff235-141">[Použijte zdroj dat **JOIN**](#use-join-datasource), pokud musíte číst značný počet různých záznamů z databáze.</span><span class="sxs-lookup"><span data-stu-id="ff235-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="ff235-142">Odpovídá počet dotazů a načtených záznamů celkovému množství dat?</span><span class="sxs-lookup"><span data-stu-id="ff235-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="ff235-143">Například pokud má dokument 10 řádků, ukazují statistiky, že zpráva extrahuje 10 řádků nebo 1 000 řádků?</span><span class="sxs-lookup"><span data-stu-id="ff235-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="ff235-144">Pokud máte značný počet načtených záznamů, zvažte jednu z následujících oprav:</span><span class="sxs-lookup"><span data-stu-id="ff235-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="ff235-145">[Použijte funkci **FILTER** namísto **WHERE**](#filter), chcete-li zpracovávat data na straně serveru SQL.</span><span class="sxs-lookup"><span data-stu-id="ff235-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="ff235-146">Abyste zabránili načítání stejných dat, použijte ukládání do mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="ff235-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="ff235-147">[Používejte shromážděné datové funkce](#collected-data), chcete-li se vyhnout načítání stejných dat pro sumarizaci.</span><span class="sxs-lookup"><span data-stu-id="ff235-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="ff235-148">Analyzujte trasování PerfView</span><span class="sxs-lookup"><span data-stu-id="ff235-148">Analyze PerfView traces</span></span>

<span data-ttu-id="ff235-149">[PerfView](#perfview) je nástroj pro zkušené vývojáře.</span><span class="sxs-lookup"><span data-stu-id="ff235-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="ff235-150">Podrobnější informace o následujících krocích najdete v části [Základy šetřování času nástěnných hodin](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="ff235-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="ff235-151">Shromážděte trasování pomocí času vlákna.</span><span class="sxs-lookup"><span data-stu-id="ff235-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="ff235-152">Zahrnujte pouze zásobníky, které používají **runUnattended**, pro filtrování pouze vlákna, které má provádění konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ff235-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="ff235-153">(Přidejte **runUnattended** do vstupního pole **IncPats**.)</span><span class="sxs-lookup"><span data-stu-id="ff235-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="ff235-154">Přeložte celou síť COU a blokovaný čas.</span><span class="sxs-lookup"><span data-stu-id="ff235-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="ff235-155">Nahrejte [Předvolby ER pro PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span><span class="sxs-lookup"><span data-stu-id="ff235-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="ff235-156">Vyberte **ER** \> **Další předvolba**.</span><span class="sxs-lookup"><span data-stu-id="ff235-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="ff235-157">Podívejte se na jména:</span><span class="sxs-lookup"><span data-stu-id="ff235-157">Look at the names:</span></span>

    - <span data-ttu-id="ff235-158">Pravděpodobně uvidíte kód platformy, který spotřebovává nejvíce času.</span><span class="sxs-lookup"><span data-stu-id="ff235-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="ff235-159">Můžete poklepat (nebo dvakrát kliknout) a projít **callees**.</span><span class="sxs-lookup"><span data-stu-id="ff235-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="ff235-160">Pokud najdete třídy, které mají předponu „ERExpression“, a pokud se jedná o funkce, které se vztahují k vzorcům, můžete uhodnout název funkce na základě názvu třídy a můžete se podívat na úložiště ER, kde můžete zobrazit atributy.</span><span class="sxs-lookup"><span data-stu-id="ff235-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="ff235-161">Opravy</span><span class="sxs-lookup"><span data-stu-id="ff235-161">Fixes</span></span>

- <span data-ttu-id="ff235-162">Pokud zjistíte, že většinu času CPU spotřebovávají dotazy, zkuste snížit počet dotazů:</span><span class="sxs-lookup"><span data-stu-id="ff235-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="ff235-163">[Zkontrolujte trasování ER](#analyze-database-calls) pro duplicitní dotazy.</span><span class="sxs-lookup"><span data-stu-id="ff235-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="ff235-164">Podívejte se, kolik záznamů je načteno, a vyhodnoťte, kolik dat by teoreticky mělo být načteno.</span><span class="sxs-lookup"><span data-stu-id="ff235-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="ff235-165">Pokud vidíte, že většinu času CPU spotřebovávají použité funkce, zkuste najít místo v konfiguraci, která spotřebovává nejvíce prostředků.</span><span class="sxs-lookup"><span data-stu-id="ff235-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="ff235-166">Pokud vidíte, že většinu času CPU spotřebovávají funkce sběru dat, zvažte jejich nahrazení *Skupina SQL podle* na straně mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="ff235-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="ff235-167">Shromažďování dat</span><span class="sxs-lookup"><span data-stu-id="ff235-167">Collecting data</span></span>

<span data-ttu-id="ff235-168">V závislosti na vašem prostředí existuje několik způsobů, jak shromažďovat dostupná data:</span><span class="sxs-lookup"><span data-stu-id="ff235-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="ff235-169">Získejte celkovou dobu chodu:</span><span class="sxs-lookup"><span data-stu-id="ff235-169">Get the total running time:</span></span>

    - <span data-ttu-id="ff235-170">Z centra akcí</span><span class="sxs-lookup"><span data-stu-id="ff235-170">From the Action center</span></span>
    - <span data-ttu-id="ff235-171">Z protokolu událostí</span><span class="sxs-lookup"><span data-stu-id="ff235-171">From the event log</span></span>

- <span data-ttu-id="ff235-172">Profilovat provedení:</span><span class="sxs-lookup"><span data-stu-id="ff235-172">Profile the execution:</span></span>

    - <span data-ttu-id="ff235-173">Pomocí nástrojů ER</span><span class="sxs-lookup"><span data-stu-id="ff235-173">By using ER tools</span></span>
    - <span data-ttu-id="ff235-174">Pomocí Trace parseru</span><span class="sxs-lookup"><span data-stu-id="ff235-174">By using Trace parser</span></span>
    - <span data-ttu-id="ff235-175">Pomocí PerfView</span><span class="sxs-lookup"><span data-stu-id="ff235-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="ff235-176">Sběr dat v produkčním prostředí</span><span class="sxs-lookup"><span data-stu-id="ff235-176">Collecting data in a production environment</span></span>

<span data-ttu-id="ff235-177">Někdy lze problémy reprodukovat pouze v produkčním prostředí.</span><span class="sxs-lookup"><span data-stu-id="ff235-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="ff235-178">Data lze vybírat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="ff235-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="ff235-179">Sledování pomocí [Trace parser](../perf-test/trace-trace-tutorial.md)</span><span class="sxs-lookup"><span data-stu-id="ff235-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="ff235-180">Sledováním [Spuštění ER](trace-execution-er-troubleshoot-perf.md)</span><span class="sxs-lookup"><span data-stu-id="ff235-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="ff235-181">Použitím celkové doby spuštění</span><span class="sxs-lookup"><span data-stu-id="ff235-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="ff235-182">Sběr dat ve vývojovém prostředí</span><span class="sxs-lookup"><span data-stu-id="ff235-182">Collecting data in a development environment</span></span>

<span data-ttu-id="ff235-183">Kromě nástrojů, které lze použít v produkčním prostředí, existuje několik nástrojů, které můžete použít ve vývojovém prostředí:</span><span class="sxs-lookup"><span data-stu-id="ff235-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="ff235-184">Protokol událostí (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="ff235-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="ff235-185">Tento protokol vám může poskytnout celkovou dobu spuštění.</span><span class="sxs-lookup"><span data-stu-id="ff235-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="ff235-186">Běžné nástroje .NET, například PerfView.</span><span class="sxs-lookup"><span data-stu-id="ff235-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="ff235-187">Vývojové prostředí vám navíc poskytuje větší flexibilitu při experimentování.</span><span class="sxs-lookup"><span data-stu-id="ff235-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="ff235-188">Můžete například vypnout části sestav, abyste viděli, jak je ovlivněna doba spuštění.</span><span class="sxs-lookup"><span data-stu-id="ff235-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="ff235-189">Nástroje</span><span class="sxs-lookup"><span data-stu-id="ff235-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="ff235-190">Čas spuštění v centru akcí</span><span class="sxs-lookup"><span data-stu-id="ff235-190">Execution time in the Action center</span></span>

<span data-ttu-id="ff235-191">ER může zobrazit čas spuštění konfigurace v centru akcí.</span><span class="sxs-lookup"><span data-stu-id="ff235-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="ff235-192">Tato možnost funguje pouze pro konkrétního uživatele a konkrétní společnost a pouze pro interaktivní relace.</span><span class="sxs-lookup"><span data-stu-id="ff235-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="ff235-193">Chcete-li tuto funkci zpřístupnit, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ff235-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="ff235-194">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="ff235-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ff235-195">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="ff235-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="ff235-196">V dialogovém okně **Uživatelské parametry** nastavte u možnosti **Zobrazit čas generování souboru** možnost **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ff235-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="ff235-197">Čas spuštění v protokolu událostí</span><span class="sxs-lookup"><span data-stu-id="ff235-197">Execution time in the event log</span></span>

1. <span data-ttu-id="ff235-198">Otevřít prohlížeč událostí Windows.</span><span class="sxs-lookup"><span data-stu-id="ff235-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="ff235-199">V **Protokolech aplikací a služeb** otevřete **Microsoft-Dynamics-ElectronicReporting/Operational**.</span><span class="sxs-lookup"><span data-stu-id="ff235-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="ff235-200">Vyhledejte události **FormatMapingRun**, kde **EventID=2**, protože tyto události obsahují informace o uplynulém čase.</span><span class="sxs-lookup"><span data-stu-id="ff235-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="ff235-201">Sledování Trace parseru</span><span class="sxs-lookup"><span data-stu-id="ff235-201">Trace parser traces</span></span> 

<span data-ttu-id="ff235-202">Protože ER je implementováno v X++, můžete k analýze výkonu použít běžné nástroje X++.</span><span class="sxs-lookup"><span data-stu-id="ff235-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="ff235-203">Další informace viz [Sledování pomocí Trace parseru](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="ff235-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="ff235-204">Tento přístup má několik omezení.</span><span class="sxs-lookup"><span data-stu-id="ff235-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="ff235-205">Protože část ER je implementována v C #, nebudou k dispozici všechny podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="ff235-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="ff235-206">Můžete však zobrazit podrobnosti o využití dat.</span><span class="sxs-lookup"><span data-stu-id="ff235-206">However, you can view the data usage details.</span></span> <span data-ttu-id="ff235-207">Dlouhé spouštění sestav může navíc překročit omezení úložiště trasování.</span><span class="sxs-lookup"><span data-stu-id="ff235-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="ff235-208">Sledování ER</span><span class="sxs-lookup"><span data-stu-id="ff235-208">ER traces</span></span>

<span data-ttu-id="ff235-209">ER může shromažďovat své vlastní stopy a má pro tyto stopy nástroje pro vizualizaci a analýzu.</span><span class="sxs-lookup"><span data-stu-id="ff235-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="ff235-210">Více informací viz [Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="ff235-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="ff235-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="ff235-211">PerfView</span></span>

<span data-ttu-id="ff235-212">Protože X++ i ER jsou implementovány na platformě .NET, můžete použít běžné nástroje .NET.</span><span class="sxs-lookup"><span data-stu-id="ff235-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="ff235-213">Můžete například použít bezplatný nástroj [PerfView](https://github.com/Microsoft/perfview).</span><span class="sxs-lookup"><span data-stu-id="ff235-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="ff235-214">Můžete také shromažďovat data z příkazového řádku.</span><span class="sxs-lookup"><span data-stu-id="ff235-214">You can also collect data from the command line.</span></span> <span data-ttu-id="ff235-215">Například následující skript prostředí Windows PowerShell shromažďuje čas spuštění, dokud se na počítači nezastaví jakékoli provádění formátu.</span><span class="sxs-lookup"><span data-stu-id="ff235-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="ff235-216">Tento přístup má několik omezení.</span><span class="sxs-lookup"><span data-stu-id="ff235-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="ff235-217">Musíte mít administrativní přístup k tomuto počítači.</span><span class="sxs-lookup"><span data-stu-id="ff235-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="ff235-218">Kromě toho musíte být zkušeným vývojářem, protože je strmá křivka učení.</span><span class="sxs-lookup"><span data-stu-id="ff235-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="ff235-219">Provádění změn</span><span class="sxs-lookup"><span data-stu-id="ff235-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="ff235-220">Použijte ukládání do mezipaměti</span><span class="sxs-lookup"><span data-stu-id="ff235-220">Use caching</span></span>

<span data-ttu-id="ff235-221">Přestože ukládání do mezipaměti snižuje dobu potřebnou k opětovnému načtení dat, spotřebovává paměť.</span><span class="sxs-lookup"><span data-stu-id="ff235-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="ff235-222">Ukládání do mezipaměti použijte v případech, kdy množství načtených dat není příliš velké.</span><span class="sxs-lookup"><span data-stu-id="ff235-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="ff235-223">Další informace a příklad, který ukazuje, jak používat ukládání do mezipaměti, najdete v tématu [Vylepšete mapování modelu na základě informací z trasování spuštění](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="ff235-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="ff235-224">Použijte parametrizované vypočítané pole v mezipaměti</span><span class="sxs-lookup"><span data-stu-id="ff235-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="ff235-225">Někdy musí být hodnoty vyhledávány opakovaně.</span><span class="sxs-lookup"><span data-stu-id="ff235-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="ff235-226">Mezi příklady patří názvy účtů a čísla účtů.</span><span class="sxs-lookup"><span data-stu-id="ff235-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="ff235-227">Chcete-li ušetřit čas, můžete vytvořit vypočítané pole, které má parametry na nejvyšší úrovni, a poté pole přidat do mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="ff235-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="ff235-228">Doporučujeme použít tento přístup pouze v případě, že je velikost dat v mezipaměti malá.</span><span class="sxs-lookup"><span data-stu-id="ff235-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="ff235-229">Další informace viz [Zlepšete výkon řešení ER přidáním parametrizovaných zdrojů dat CALCULATED FIELD](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="ff235-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="ff235-230">Použít datový zdroj JOIN</span><span class="sxs-lookup"><span data-stu-id="ff235-230">Use a JOIN data source</span></span>

<span data-ttu-id="ff235-231">Zdroje dat **JOIN** umožňuje načíst několik připojených záznamů jedním dotazem.</span><span class="sxs-lookup"><span data-stu-id="ff235-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="ff235-232">K načtení každého připojeného záznamu není nutné použít samostatný dotaz.</span><span class="sxs-lookup"><span data-stu-id="ff235-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="ff235-233">Například, pokud máte 1 000 řádků a načtete data položky pro každý řádek podle relace, budete mít 1 001 dotazů (= 1 000 + 1).</span><span class="sxs-lookup"><span data-stu-id="ff235-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="ff235-234">Pokud používáte datový zdroj **JOIN**, k načtení stejných dat použijete pouze jeden dotaz.</span><span class="sxs-lookup"><span data-stu-id="ff235-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="ff235-235">Další informace viz [Použití zdrojů dat JOIN v mapování modelu ER k získání dat z více aplikačních tabulek](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="ff235-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="ff235-236">Místo funkce WHERE použijte funkci FILTER</span><span class="sxs-lookup"><span data-stu-id="ff235-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="ff235-237">Funkce **[FILTER](er-functions-list-filter.md)** spouští podmínky na serveru SQL Server, zatímco funkce **WHERE** načte všechna data ze seznamu, jeden záznam po druhém, a použije podmínku pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="ff235-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="ff235-238">Například chcete vybrat jeden záznam z 1000 záznamů.</span><span class="sxs-lookup"><span data-stu-id="ff235-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="ff235-239">Pokud používáte **WHERE**, bude načteno všech 1 000 záznamů.</span><span class="sxs-lookup"><span data-stu-id="ff235-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="ff235-240">Pokud však používáte **FILTER**, načte se přesně jeden záznam.</span><span class="sxs-lookup"><span data-stu-id="ff235-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="ff235-241">**FILTER** můžete také použít indexy na straně databáze.</span><span class="sxs-lookup"><span data-stu-id="ff235-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="ff235-242">Pomocí shromážděných datových funkcí nebo nahromaděného zdroje dat</span><span class="sxs-lookup"><span data-stu-id="ff235-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="ff235-243">Pokud má vaše konfigurace komponentu *seskupit podle*, která shrnuje dříve načtená data podle zprávy, načte všechna data znovu.</span><span class="sxs-lookup"><span data-stu-id="ff235-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="ff235-244">Použitím funkcí shromážděných dat umožníte ER shromáždit data během prvního načtení.</span><span class="sxs-lookup"><span data-stu-id="ff235-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="ff235-245">Další informace naleznete v tématu [Konfigurace formátu ER pro počítání a sčítání](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="ff235-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="ff235-246">Přepište části konfigurace v X++</span><span class="sxs-lookup"><span data-stu-id="ff235-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="ff235-247">ER podporuje volání metod tabulek a tříd, včetně rozšíření.</span><span class="sxs-lookup"><span data-stu-id="ff235-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="ff235-248">Zvažte přepsání částí mapování modelu v X++, které vám pomohou zlepšit výkon.</span><span class="sxs-lookup"><span data-stu-id="ff235-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="ff235-249">ER může využívat data z následujících zdrojů:</span><span class="sxs-lookup"><span data-stu-id="ff235-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="ff235-250">Třídy (datové zdroje **objekt** a **třída**)</span><span class="sxs-lookup"><span data-stu-id="ff235-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="ff235-251">Tabulky (datové zdroje **tabulka** a **záznamy v tabulce**)</span><span class="sxs-lookup"><span data-stu-id="ff235-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="ff235-252">[Rozhraní ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) také poskytuje způsob, jak odeslat předpočítaná data z kódu volání.</span><span class="sxs-lookup"><span data-stu-id="ff235-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="ff235-253">Sada aplikací obsahuje řadu příkladů tohoto přístupu.</span><span class="sxs-lookup"><span data-stu-id="ff235-253">The application suite contains numerous examples of this approach.</span></span>

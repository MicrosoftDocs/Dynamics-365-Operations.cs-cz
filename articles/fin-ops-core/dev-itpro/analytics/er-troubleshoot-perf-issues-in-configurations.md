---
title: Odstraňování problémů s výkonem v konfiguracích ER
description: Tento článek vysvětluje, jak najít a opravit problémy s výkonem v konfiguracích Elektronického výkaznictví (ER).
author: kfend
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
ms.openlocfilehash: 283577e70d4e5c4314776f7420857cf8e25e735f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278729"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>Odstraňování problémů s výkonem v konfiguracích ER

Tento článek vysvětluje, jak najít a vyřešit problémy s výkonem v [konfiguracích](general-electronic-reporting.md#Configuration) [Elektronického výkaznictví](general-electronic-reporting.md) (ER).

Vyšetřování problémů s výkonem se obvykle skládá z několika kroků.

1. [Sběr](#collecting-data) dat.
2. Analýza shromážděných dat.
3. Na základě výsledků analýzy použijte konfigurace ER k [provedené změn](#making-changes) nebo se rozhodnete shromáždit více údajů.

## <a name="troubleshooting"></a>Řešení potíží

### <a name="analyze-execution-time"></a>Analyzujte čas provedení

Čas spuštění může záviset na nepředvídatelných faktorech, jako jsou jiné úkoly spuštěné ve stejném prostředí a ukládání do mezipaměti, které používá data při prvním volání. Proto byste měli provádění a měření několikrát opakovat.

Někdy nejsou problémy s výkonem způsobeny konfigurací formátu ER, která se používá pro vytváření sestav. Místo toho jsou způsobeny kódem X++, který se používá k otevření konfigurace formátu ER.

1. V [Centru akcí](#infolog-time) nebo [protokolu událostí](#event-log-time) se podívejte na čas provedení sestavy.
2. Porovnejte čas provedení sestavy s celkovou dobou provedení ve scénáři.
3. Pokud je doba spuštění sestavy mnohem kratší než celková doba provedení, zvažte množství dat, která sestava zpracovává:

    - Pokud sestava zpracovává malé množství dat, problém může zahrnovat dobu načítání konfigurace.
    - Pokud sestava zpracovává velké množství dat, problém může zahrnovat předzpracování X++. Použijte [Trace parser](#analyze-trace-parser-trace) k analýze tohoto případu.

    V ostatních případech viz další části.

4. Spusťte více testů, které zahrnují různá množství dat, abyste zjistili, jak čas provedení závisí na množství dat.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Analýza trasování Trace parseru

Připravte si malý příklad nebo shromážděte několik tras během náhodných částí generování sestavy.

Pak v [Trace parseru](#trace-parser) proveďte standardní analýzu zdola nahoru a odpovězte na následující otázky:

- Jaké jsou nejlepší metody z hlediska spotřeby času?
- Jakou část celkového času tyto metody používají?

Na dotazy odpovídejte na stejné otázky.

Pokud uvidíte, že před metodami je uvedeno „ER“, přejděte k další části.

Pokud vidíte, že metody nebo dotazy pocházejí z aplikační sady, zvažte obecné optimalizace (například vytvořte indexy).

Analyzujte počet hovorů. Pokud je počet výrazně vyšší, než se očekávalo, zvažte uložení do mezipaměti odpovídajících uzlů konfigurace.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Analyzujte volání databáze

Připravte si příklad, který obsahuje malé množství dat, abyste mohli shromáždit [trasování ER](#electronic-reporting-traces).

Poté otevřete trasování v návrháři mapování modelů ER a podívejte se na spodní část stránky. Odpovězte na následující otázky:

- Existuje nějaká duplikace dotazu? Pokud existuje, zvažte jednu z následujících oprav:

    - [Použijte ukládání do mezipaměti](#use-caching), pokud si myslíte, že uvnitř jednoho nadřazeného záznamu je několik volání.
    - [Použijte parametrizované vypočítané pole v mezipaměti](#cached-parameterized), pokud si myslíte, že existují volání stejného záznamu v různých záznamech.
    - [Použijte zdroj dat **JOIN**](#use-join-datasource), pokud musíte číst značný počet různých záznamů z databáze.

- Odpovídá počet dotazů a načtených záznamů celkovému množství dat? Například pokud má dokument 10 řádků, ukazují statistiky, že zpráva extrahuje 10 řádků nebo 1 000 řádků? Pokud máte značný počet načtených záznamů, zvažte jednu z následujících oprav:

    - [Použijte funkci **FILTER** namísto **WHERE**](#filter), chcete-li zpracovávat data na straně Microsoft SQL Server.
    - Abyste zabránili načítání stejných dat, použijte ukládání do mezipaměti.
    - [Používejte shromážděné datové funkce](#collected-data), chcete-li se vyhnout načítání stejných dat pro sumarizaci.

### <a name="analyze-perfview-traces"></a>Analyzujte trasování PerfView

[PerfView](#perfview) je nástroj pro zkušené vývojáře. Podrobnější informace o následujících krocích najdete v části [Základy šetřování času nástěnných hodin](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).

1. Shromážděte trasování pomocí času vlákna.
2. Zahrnujte pouze zásobníky, které používají **runUnattended**, pro filtrování pouze vlákna, které má provádění konfigurace. (Přidejte **runUnattended** do vstupního pole **IncPats**.)
3. Přeložte celou síť COU a blokovaný čas.
4. Nahrejte [Předvolby ER pro PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).
5. Vyberte **ER** \> **Další předvolba**.
6. Podívejte se na jména:

    - Pravděpodobně uvidíte kód platformy, který spotřebovává nejvíce času.
    - Můžete poklepat (nebo dvakrát kliknout) a projít **callees**.

        Pokud najdete třídy, které mají předponu „ERExpression“, a pokud se jedná o funkce, které se vztahují k vzorcům, můžete uhodnout název funkce na základě názvu třídy a můžete se podívat na úložiště ER, kde můžete zobrazit atributy.

### <a name="fixes"></a>Opravy

- Pokud zjistíte, že většinu času CPU spotřebovávají dotazy, zkuste snížit počet dotazů:

    - [Zkontrolujte trasování ER](#analyze-database-calls) pro duplicitní dotazy.
    - Podívejte se, kolik záznamů je načteno, a vyhodnoťte, kolik dat by teoreticky mělo být načteno.

- Pokud vidíte, že většinu času CPU spotřebovávají použité funkce, zkuste najít místo v konfiguraci, která spotřebovává nejvíce prostředků.
- Pokud vidíte, že většinu času CPU spotřebovávají funkce sběru dat, zvažte jejich nahrazení *Skupina SQL podle* na straně mapování modelu.

### <a name="collecting-data"></a><a name="collecting-data"></a>Shromažďování dat

V závislosti na vašem prostředí existuje několik způsobů, jak shromažďovat dostupná data:

- Získejte celkovou dobu chodu:

    - Z centra akcí
    - Z protokolu událostí

- Profilovat provedení:

    - Pomocí nástrojů ER
    - Pomocí Trace parseru
    - Pomocí PerfView

#### <a name="collecting-data-in-a-production-environment"></a>Sběr dat v produkčním prostředí

Někdy lze problémy reprodukovat pouze v produkčním prostředí. Data lze vybírat následujícím způsobem:

- Sledování pomocí [Trace parser](../perf-test/trace-trace-tutorial.md)
- Sledováním [Spuštění ER](trace-execution-er-troubleshoot-perf.md)
- Použitím celkové doby spuštění

#### <a name="collecting-data-in-a-development-environment"></a>Sběr dat ve vývojovém prostředí

Kromě nástrojů, které lze použít v produkčním prostředí, existuje několik nástrojů, které můžete použít ve vývojovém prostředí:

- Protokol událostí (Microsoft-Dynamics-ElectronicReporting). Tento protokol vám může poskytnout celkovou dobu spuštění.
- Běžné nástroje .NET, například PerfView.

Vývojové prostředí vám navíc poskytuje větší flexibilitu při experimentování. Můžete například vypnout části sestav, abyste viděli, jak je ovlivněna doba spuštění.

### <a name="tools"></a><a name="tools"></a>Nástroje

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Čas spuštění v centru akcí

ER může zobrazit čas spuštění konfigurace v centru akcí. Tato možnost funguje pouze pro konkrétního uživatele a konkrétní společnost a pouze pro interaktivní relace. Chcete-li tuto funkci zpřístupnit, postupujte takto.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. V dialogovém okně **Uživatelské parametry** nastavte u možnosti **Zobrazit čas generování souboru** možnost **Ano**.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Čas spuštění v protokolu událostí

1. Otevřít prohlížeč událostí Windows.
2. V **Protokolech aplikací a služeb** otevřete **Microsoft-Dynamics-ElectronicReporting/Operational**.
3. Vyhledejte události **FormatMapingRun**, kde **EventID=2**, protože tyto události obsahují informace o uplynulém čase.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Sledování Trace parseru 

Protože ER je implementováno v X++, můžete k analýze výkonu použít běžné nástroje X++. Další informace viz [Sledování pomocí Trace parseru](../perf-test/trace-trace-tutorial.md).

Tento přístup má několik omezení. Protože část ER je implementována v C #, nebudou k dispozici všechny podrobnosti. Můžete však zobrazit podrobnosti o využití dat. Dlouhé spouštění sestav může navíc překročit omezení úložiště trasování.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>Sledování ER

ER může shromažďovat své vlastní stopy a má pro tyto stopy nástroje pro vizualizaci a analýzu. Více informací viz [Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem](trace-execution-er-troubleshoot-perf.md).

#### <a name="perfview"></a><a name="perfview"></a>PerfView

Protože X++ i ER jsou implementovány na platformě .NET, můžete použít běžné nástroje .NET. Můžete například použít bezplatný nástroj [PerfView](https://github.com/Microsoft/perfview).

Můžete také shromažďovat data z příkazového řádku. Například následující skript prostředí Windows PowerShell shromažďuje čas spuštění, dokud se na počítači nezastaví jakékoli provádění formátu.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Tento přístup má několik omezení. Musíte mít administrativní přístup k tomuto počítači. Kromě toho musíte být zkušeným vývojářem, protože je strmá křivka učení.

### <a name="making-changes"></a><a name="making-changes"></a>Provádění změn

#### <a name="use-caching"></a><a name="use-caching"></a>Použijte ukládání do mezipaměti

Přestože ukládání do mezipaměti snižuje dobu potřebnou k opětovnému načtení dat, spotřebovává paměť. Ukládání do mezipaměti použijte v případech, kdy množství načtených dat není příliš velké. Další informace a příklad, který ukazuje, jak používat ukládání do mezipaměti, najdete v tématu [Vylepšete mapování modelu na základě informací z trasování spuštění](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).

#### <a name="reduce-volume-of-data-fetched"></a><a name="reduce-fetched-data"></a>Snižte objem načítaných dat

Spotřebu paměti pro ukládání do mezipaměti můžete snížit omezením počtu polí v záznamech tabulky aplikace, které načítáte za běhu. V tomto případě získáte pouze ty hodnoty polí tabulky aplikace, které potřebujete ve svém mapování modelu ER. Ostatní pole v této tabulce nebudou načtena. Proto je objem paměti, který je vyžadován pro ukládání načtených záznamů do mezipaměti, snížen. Další informace viz [Zlepšete výkon řešení ER snížením počtu polí tabulky, která jsou načítána za běhu](er-reduce-fetched-fields-number.md).

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Použijte parametrizované vypočítané pole v mezipaměti

Někdy musí být hodnoty vyhledávány opakovaně. Mezi příklady patří názvy účtů a čísla účtů. Chcete-li ušetřit čas, můžete vytvořit vypočítané pole, které má parametry na nejvyšší úrovni, a poté pole přidat do mezipaměti.

Doporučujeme použít tento přístup pouze v případě, že je velikost dat v mezipaměti malá. Další informace viz [Zlepšete výkon řešení ER přidáním parametrizovaných zdrojů dat CALCULATED FIELD](er-calculated-field-ds-performance.md).

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>Použít datový zdroj JOIN

Zdroje dat **JOIN** umožňuje načíst několik připojených záznamů jedním dotazem. K načtení každého připojeného záznamu není nutné použít samostatný dotaz. Například, pokud máte 1 000 řádků a načtete data položky pro každý řádek podle relace, budete mít 1 001 dotazů (= 1 000 + 1). Pokud používáte datový zdroj **JOIN**, k načtení stejných dat použijete pouze jeden dotaz. Další informace viz [Použití zdrojů dat JOIN v mapování modelu ER k získání dat z více aplikačních tabulek](er-join-data-sources.md).

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>Místo funkce WHERE použijte funkci FILTER

Funkce **[FILTER](er-functions-list-filter.md)** spouští podmínky na serveru SQL Server, zatímco funkce **WHERE** načte všechna data ze seznamu, jeden záznam po druhém, a použije podmínku pro každý záznam. Například chcete vybrat jeden záznam z 1000 záznamů. Pokud používáte **WHERE**, bude načteno všech 1 000 záznamů. Pokud však používáte **FILTER**, načte se přesně jeden záznam. **FILTER** můžete také použít indexy na straně databáze.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Pomocí shromážděných datových funkcí nebo nahromaděného zdroje dat

Pokud má vaše konfigurace komponentu *seskupit podle*, která shrnuje dříve načtená data podle zprávy, načte všechna data znovu. Použitím funkcí shromážděných dat umožníte ER shromáždit data během prvního načtení. Další informace naleznete v tématu [Konfigurace formátu ER pro počítání a sčítání](tasks/er-format-counting-summing-2.md).

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Přepište části konfigurace v X++

ER podporuje volání metod tabulek a tříd, včetně rozšíření. Zvažte přepsání částí mapování modelu v X++, které vám pomohou zlepšit výkon.

ER může využívat data z následujících zdrojů:

- Třídy (datové zdroje **objekt** a **třída**)
- Tabulky (datové zdroje **tabulka** a **záznamy v tabulce**)

[Aplikační pozhraní ER (API)](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) také poskytuje způsob, jak odeslat předpočítaná data z kódu volání. Sada aplikací obsahuje řadu příkladů tohoto přístupu.

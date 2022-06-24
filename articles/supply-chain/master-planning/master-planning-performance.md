---
title: Vylepšení výkonu hlavního plánování
description: V tomto článku jsou vysvětleny různé možnosti, které vám mohou pomoci při zlepšení výkonnosti hlavního plánování či řešení problémů.
author: t-benebo
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: b2c4b7e2197d312d22f9851121a9e6d4d4d03ba3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897596"
---
# <a name="improve-master-planning-performance"></a>Vylepšení výkonu hlavního plánování

[!include [banner](../includes/banner.md)]

V tomto článku jsou vysvětleny různé možnosti, které vám mohou pomoci při zlepšení výkonnosti hlavního plánování či řešení problémů. Obsahuje informace o parametrech a nastaveních a o doporučených konfiguracích a akcích. Obsahuje také souhrn všech důležitých parametrů, které byste měli zvážit v případě dlouhotrvajících úloh hlavního plánování.

Tento článek je určeno pro správce systému nebo IT uživatele, kteří mají možnost odstraňovat potíže. Je také určen pro plánovače výroby nebo dodávek, protože obsahuje informace o parametrech souvisejících s požadavky na obchodní plánování. 

## <a name="parameters-related-to-master-planning-performance"></a>Parametry související s výkonem hlavního plánování

Různé parametry ovlivňují operační dobu hlavního plánování a měly by být vzaty v úvahu.

### <a name="number-of-threads"></a>Počet vláken

Parametr **Počet vláken** umožňuje upravit proces hlavního plánování, aby se zlepšila výkonnost na určité sadě dat. Tento parametr určuje celkový počet vláken, která budou použita ke spuštění hlavního plánování. To způsobuje paralelizaci spuštění hlavního plánování, což pomáhá snížit operační dobu. 

Parametr **Počet vláken** lze nastavit v dialogovém okně **Spuštění hlavního plánování**. Chcete-li otevřít toto dialogové okno, přejděte na **Hlavní plánování \> Hlavní plánování \> Spuštění \> Hlavní plánování** nebo vyberte **Spustit** v pracovním prostoru **Hlavní plánování**. Chcete-li určit nejlepší hodnotu pro tento parametr, musíte se spolehnout na proces pokus omyl. K výpočtu počáteční hodnoty však můžete použít následující vzorce:

- **Pokud váš obor vyrábí:** (počet vláken) = (počet plánovaných objednávek ÷ 1 000)
- **V opačném případě:** (počet vláken) = (počet položek ÷ 1 000)

Počet pomocníků použitých během hlavního plánování musí být menší nebo rovný maximálnímu počtu vláken, které jsou povoleny na dávkovém serveru. Pokud počet pomocníků překročí počet vláken na dávkovém serveru, nebudou další vlákna provádět žádné práce.

> [!NOTE]
> Nastavení parametru **Počet vláken** na **0** (nula) zvyšuje operační čas hlavního plánování. Proto doporučujeme, abyste vždy nastavili hodnotu, která je větší než 0.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Počet úkolů v sadě úkolů pomocníka

Změnou nastavení **Počet úkolů v sadě úkolů pomocníka** (tj. velikosti sady) můžete operační dobu zkrátit. Toto nastavení kontroluje počet položek, které jsou plánovány společně jediným pomocníkem.

Můžete nastavit parametr **Počet úkolů v sadě úkolů pomocníka** v části **Výkon** na kartě **Obecné** stránky **Parametry hlavního plánování** (**Hlavní plánování \> Nastavení \> Parametry hlavního plánování**). Nejlepší hodnota pro tento parametr závisí na vašich datech. Proto doporučujeme, abyste začínaly s hodnotou **1** a potom pomocí procesu pokus omyl určíte nejlepší hodnotu pro nastavení.

Obecně doporučujeme, abyste zvýšili počet úkolů v případě, že je počet položek velmi velký (ve stovkách tisíc). V opačném případě byste měli snížit počet úkolů. U následujících konkrétních odvětví je třeba vzít v úvahu tato doporučení:

- V odvětví maloobchodu a distribuce, kde existuje mnoho nezávislých položek, použijte mnoho pomocníků, protože mezi položkami neexistuje žádná závislost. 
- Ve výrobním odvětví, kde existuje mnoho kusovníků a sdílených dílčích součástí, se používá méně pomocníků, protože závislosti mezi položkami mohou způsobovat čekací dobu.

> [!TIP]
> Pokud máte problémy s výkonem, doporučujeme snížit nastavení možnosti **Počet pomocníků v sadě úkolů** na **1**. Poté můžete zahájením procesu pokus omyl najít nejlepší hodnotu pro nastavení. K problémům s výkonem obecně dochází, když trvá zpracování jedné položky déle než zbývajících položek. V tomto případě uvidíte, že dva následující úkoly, které mají status **Disponibilita** při spuštění hlavního plánování, zabírají značně rozdílné operační doby. V extrémních případech může tento rozdíl být až 30 minut. Dobu, po kterou jsou úkoly spuštěny, můžete odvodit tak, že se podíváte na trvání jednotlivých úkolů.

### <a name="use-of-cache"></a>Použít mezipaměť

Parametr **Použít mezipaměť** umožňuje upravit proces hlavního plánování, aby měl lepší výkon na určité sadě dat. Lze jej například upravit, aby byly dosaženy následující výsledky:

- Je-li provedeno více uložení do mezipaměti, v datové paměti se shromáždí více dat. Očekává se, že data budou použita později. Pokud jsou data v paměti, můžete uložit některé databázové požadavky. Je-li však prováděno více ukládání do mezipaměti, zvýší se nároky na paměť.
- Pokud se provádí méně ukládání do mezipaměti, může se stát, že stejná data budou muset být načtena z databáze častěji. Navíc aplikační objektový server během procesu ukládá do paměti pouze malá data.

Je obtížné předvídat, která možnost bude lepší, protože jednotlivé případy závisejí nejen na datech, ale také na hardwaru. Vzhledem k tomu, že menší ukládání do mezipaměti způsobuje další zatížení na databázovém serveru, pravděpodobně není vhodné použít tuto možnost, pokud je databázový server již přetížený.

Můžete nastavit parametr **Použít mezipaměť** v části **Výkon** na kartě **Obecné** stránky **Parametry hlavního plánování** (**Hlavní plánování \> Nastavení \> Parametry hlavního plánování**). Efektivita ukládání do mezipaměti ve vysoké míře závisí na datech odběratelů. Nejsou-li například data uložená v mezipaměti nikdy vyžadována, jedná se o plýtvání pamětí, pokud ukládáte data až do ukončení procesu plánování. V takovém případě, pokud konfigurujete méně ukládání do mezipaměti, může dojít ke zvýšení výkonu, protože server AOS vyžaduje méně paměti a prostředky serveru jsou uvolněny pro jiné úlohy.

> [!TIP]
> Obecně doporučujeme nastavit parametr **Použít mezipaměť** na **Maximum**, protože parametr je zamýšlen jako funkce zvýšení výkonu. Doporučujeme nastavit parametr na **Minimum**, pokud dochází k místnímu spuštění a máte k dispozici omezenou paměť (přibližně 2 gigabajty \[GB\]).

### <a name="number-of-orders-in-firming-bundle"></a>Počet objednávek v potvrzování sady

Parametr **Počet objednávek v potvrzování sady** určuje celkový počet objednávek, které budou každým vláknem nebo dávkou zpracovány najednou. To způsobuje paralelizaci procesu automatického potvrzování.

Můžete nastavit parametr **Počet objednávek v potvrzování sady** v části **Výkon** na kartě **Obecné** stránky **Parametry hlavního plánování** (**Hlavní plánování \> Nastavení \> Parametry hlavního plánování**). Paralelizace procesu automatického potvrzování je založena na objednávkách, které je nutné zpracovat společně. Je-li tento parametr nastaven například na **50**, každé vlákno nebo dávková úloha vybere 50 objednávek najednou a zpracuje je současně. Nejlepší hodnotu získáte pomocí procesu pokus omyl. K výpočtu počáteční hodnoty však můžete použít následující vzorec:

(Počet objednávek na sadu) = (počet položek poptávky ÷ počet vláken)

> [!NOTE]
> Nastavíte-li parametr **Počet objednávek v potvrzování sady** na **0** (nula), nebude docházet k žádné paralelizaci procesu automatického potvrzování. Celý proces bude spuštěn na jednom dávkovém úkolu a bude mít kumulativní operační dobu. Proto se zvýší operační doba hlavního plánování. Z tohoto důvodu doporučujeme nastavit tento parametr na hodnotu, která je větší než **0** (nula).

### <a name="time-fences"></a>Ochranné doby

Ochranné doby určují, jak daleko v budoucnosti musí být výpočty a další požadavky vypočteny hlavním plánováním. Čím větší je ochranná doba, tím déle bude trvat i hlavní plánování. Proto nastavte ochranné doby podle požadavků podniku. Další informace o ochranný dobách naleznete v tématu [Nastavení hlavního plánování](master-planning-setup.md).

### <a name="actions"></a>Akce

Mezi ochrannými dobami můžete také vyhledat parametr **Zpráva akce**. Výpočet zpráv akce má za následek delší operační dobu hlavního plánování. Nejsou-li zprávy akce pravidelně analyzovány a použity (denně, týdně atd.), zvažte při spuštění hlavního plánování vypnutí výpočtu. Chcete-li vypnout výpočet, na stránce **Hlavní plány** (**Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**) nastavte ochrannou dobu **Zprávy akce** na **0** (nula). Rovněž zkontrolujte, zda je nastavení **Zprávy akce** vypnuto pro všechny skupiny disponibility.

### <a name="futures"></a>Termíny

Výpočet termínů má za následek delší operační dobu hlavního plánování. Pokud neplánujete kusovníky nebo pokud zpoždění nemusí být propagována z nabídky do poptávky během plánování, zvažte vypnutí výpočtů termínů během hlavního plánování. Chcete-li vypnout výpočty, nastavte ochrannou dobu **Termínů** na **0** (nula) pro hlavní plán, který spouštíte. Rovněž zkontrolujte, zda je nastavení **Termíny** vypnuto pro všechny skupiny disponibility.

## <a name="one-heavy-routine-at-a-time"></a>Jedna těžká rutina najednou

Při plánování hlavního plánování neplánujte žádnou jinou dávkovou úlohu. Buďte obzvláště opatrní, abyste nenaplánovali žádné další těžké rutiny, jako je například uzávěrka skladu ve stejnou dobu.

## <a name="review-the-session-log"></a>Kontrola protokolu relace

Systém může shromažďovat další informace o úkolech spuštěných během hlavního plánování. Chcete-li, aby systém tyto informace shromáždil, zapněte nastavení **Sledovat čas zpracování** v dialogovém okně **Spuštění hlavního plánování**. Shromažďované informace vám mohou pomoci nalézt kritické body při spuštění. Je-li například parametr **Počet úkolů v sadě úkolů pomocníka** nastaven na **1**, můžete identifikovat položku s nejdelším operačním časem. Můžete také porovnat operační doby pro různá vlákna se stavem **Disponibilita** a porovnat dobu trvání každého úkolu.

Chcete-li zkontrolovat spuštění hlavního plánování systému, postupujte podle jednoho z následujících kroků.

- V pracovním prostoru **Hlavní plánování** vyberte hlavní plán v rozevíracím poli a poté na dlaždici **Hlavní plánování** vyberte možnost **Historie**. Vyberte úlohu, na kartě s náhledem vyberte **Dotazy** a poté vyberte **Doba trvání zpracování úkolu**.
- Na stránce **Hlavní plány** vyberte v levém podokně plán a poté na záložce s náhledem vyberte **Historie**. Vyberte úlohu, na kartě s náhledem vyberte **Dotazy** a poté vyberte **Doba trvání zpracování úkolu**.

Při kontrole protokolu relace je třeba vzít v úvahu následující:

- **Aktualizace** by neměla dlouho trvat (obecně by měla trvat až 30 minut), přestože obsahuje jedno vlákno.
- **Kopírování plánu** by nemělo trvat dlouho (měla by trvat asi jedna minutu).
- **Automatické potvrzování** obvykle trvá přibližně 30 minut. Může však zabrat až několik hodin v závislosti na počtu objednávek a složitosti položek.
- **Automatické potvrzování** by mělo zabrat méně času než **Disponibilita**.
- **Disponibilita** by měla ve srovnání se zbytkem trvat nejdéle.
- **Akce** a **Budoucí zpráva** mohou v závislosti na datech a počtu kusovníků trvat dlouho.

## <a name="filtering-of-items"></a>Filtrování položek

Filtry použité v dialogovém okně **Spuštění hlavního plánování** mají vliv na spuštění hlavního plánování. Přejděte na **Hlavní plánování \> Hlavní plánování \> Spuštění \> Hlavní plánování** nebo vyberte **Spustit** v pracovním prostoru **Hlavní plánování**. Chcete-li vyloučit položky ze spuštění, doporučujeme, abyste filtrovalo podle stavu životního cyklu položky (nikoli podle čísel položek). Když filtrujete podle stavu životního cyklu, proces aktualizace zabere méně času, než když filtrujete podle čísel položek.

## <a name="automatically-filter-by-items-with-direct-demand"></a>Automaticky filtrovat podle položek s přímou poptávkou

Chcete-li zlepšit dobu běhu hlavního plánování, můžete zvolit, aby byly zahrnuty pouze položky s přímou poptávkou. Tento filtr lze použít pouze pro provedení úplného hlavního plánování bez dalších filtrů, které se aplikují na pole **Záznamy k zahrnutí**. Hlavní plánování spouštěné pomocí filtrů bude ignorovat nastavení **Automaticky filtrovat podle položek s přímou poptávkou**.

Pole **Automaticky filtrovat podle položek s přímou poptávkou** se nachází na stránce **Parametry hlavního plánování** a lze jej použít s nastavením předběžného zpracování i po zpracování.

### <a name="pre-processing"></a>Předběžné zpracování
Parametr **Předběžné zpracování: Automaticky filtrovat podle položek s přímou poptávkou** zajišťuje, že fáze před zpracováním hlavního plánování bude obsahovat pouze položky, které splňují alespoň jednu z následujících podmínek:
  - Položka má očekávaný příjem nebo výdej, jako je například nákupní objednávka, prodejní objednávka, nabídka, objednávka transferu nebo výrobní zakázka. 
  - Položka má disponibilitu položky s pojistnou zásobu (minimální množství na skladě).
  - Pro položku existuje Prognóza poptávky po dnešku.
  - Pro položku existuje Prognóza nabídky po dnešku.
  - Položka zahrnuje všechny spojnice kontinuity z modulu call centra, které dosud nebyly vytvořeny.

> [!NOTE]
> Položka, která má fyzicky dostupné množství na skladě, nebude vykazovat transakci požadavku, protože pro položku neexistuje poptávka.

### <a name="post-processing"></a>Následné zpracování
Volba **Následné zpracování: Automaticky filtrovat podle položek s přímou poptávkou** je relevantní pouze v případě, že ve skupinách disponibility nastavíte **Požad. verze kusovníku**. V opačném případě není nutné parametr povolovat. 

Před zahájením kroku disponibility se zobrazí krok předběžné disponibility, během kterého budou položky s povoleným nastavením **Požad. verze kusovníku** znovu zpracovány. To se provádí tak, aby bylo zajištěno plánování položek z požadované verze kusovníku. Položky považované za žádosti v průběhu předběžného zpracování již nemají žádný požadavek, a proto by měly být vyloučeny z běhu plánování.

## <a name="performance-checklist-summary"></a>Souhrn kontrolního seznamu výkonu

- **Počet vláken** – Nastavte na hodnotu, která je větší než **0** (nula).
- **Počet úkolů v sadě úkolů pomocníka** – Nastavte na hodnotu, která je větší než **0** (nula). (Použijte vzorce uvedené dříve v tomto článku.)
- **Použití mezipaměti** – Nastavte na **Maximum**, pokud systém nemá nedostatek paměti.
- **Počet objednávek v potvrzování sady** – Nastavte na hodnotu, která je větší než **0** (nula). (Použijte vzorec uvedený dříve v tomto článku.)
- **Ochranné doby** – Přizpůsobte se potřebám svého podniku.
- **Akce a termíny** – Deaktivujte akce a termín, pokud je nepoužíváte.
- **Jedna těžká rutina najednou** – Nespouštějte hlavní plánování spolu s žádnou jinou těžkou rutinou.
- **Zkontroluje protokol relace.**
- **Filtrování položek** – Použijte stav životního cyklu pro vyloučení položek ze spuštění hlavního plánovaní. (Nepoužívejte čísla položek.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
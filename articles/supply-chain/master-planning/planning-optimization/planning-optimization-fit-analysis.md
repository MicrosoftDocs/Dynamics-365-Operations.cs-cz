---
title: Analýza přizpůsobení pro optimalizaci plánování
description: V tomto tématu je vysvětleno, jak ověřit aktuální nastavení a data proti funkcím funkce optimalizace plánování.
author: ChristianRytt
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 60f63a49222b3d0f13850b0f39764c6c848aba15
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049429"
---
# <a name="planning-optimization-fit-analysis"></a>Analýza přizpůsobení pro optimalizaci plánování

[!include [banner](../../includes/banner.md)]

Výsledek analýzy přizpůsobení pro optimalizaci plánování byste měli analyzovat jako součást procesu migrace. Všimněte si, že se rozsah optimalizace plánování nerovná aktuální integrované hlavní plánovací funkce. Doporučujeme, abyste spolupracovali se svým partnerem a v rámci přípravy na migraci si přečetli dokumentaci. 

Analýza přizpůsobení optimalizace plánování vám může ukázat, kde se může výsledek lišit mezi integrovaným hlavním plánovacím modulem a optimalizací plánování. Tato analýza probíhá na základě vašeho aktuálního nastavení a dat. 

Chcete-li si zobrazit výsledek analýzy přizpůsobení pro optimalizaci plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Analýza přizpůsobení pro optimalizaci plánování** a potom vyberte **Spustit analýzu**. Pokud analýza nalezne nějaké nekonzistence, budou uvedeny na stejné stránce. (Provádění analýzy může trvat několik minut.)

> [!NOTE]
> Pokud jsou nalezeny nekonzistence, můžete stále používat optimalizaci plánování. Výsledky analýzy přizpůsobení zobrazují pouze místa, kde plánovací služba nerespektuje vaše aktuální nastavení. Jinými slovy, zobrazují místa, kde některé procesy mohou být ignorovány nebo nejsou podporovány.

## <a name="analysis-results-example-1"></a>Výsledky analýzy: Příklad 1

- **Funkce:** Výroba
- **Problém:** Položky s úrovní kusovníku (BOM) vyšší než nula: 56
- **Vysvětlení:** Analýza přizpůsobení nalezla 56 položek, které mají pro výrobu nastaven kusovník. Vzhledem k tomu, že aktuální verze optimalizace plánování nepodporuje výrobu, optimalizace plánování vygeneruje plánované nákupní objednávky namísto plánovaných výrobních zakázek. Zobrazí se také upozornění, které obsahuje seznam ovlivněných položek.

## <a name="analysis-results-example-2"></a>Výsledky analýzy: Příklad 2

- **Funkce:** Akce
- **Problém:** Skupiny disponibility s povolenou kalkulací akcí: 6
- **Vysvětlení:** Analýza přizpůsobení našla šest skupin disponibility, kde je zapnut výpočet akce. Vzhledem k tomu, že aktuální verze optimalizace plánování nepodporuje akce, nebudou při hlavním plánování generovány žádné akce.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Přehled možných výsledků analýzy přizpůsobení

V následující tabulce jsou uvedeny různé výsledky, které lze zobrazit po analýze přizpůsobení. Symbol čísla (_\#_) bude nahrazen číslem označujícím počet záznamů s uvedeným problémem. Podporované funkce nebo funkce v náhledu jsou k dispozici od verze 10.0.9 nebo novější (pokud ve sloupci „Očekávaná dostupnost“ není uvedeno vyšší číslo verze).

| Funkce | Uvedený problém | Vysvětlení | Očekávaná dostupnost |
| --- | --- | --- | --- |
| Akce | Výpočet skupin disponibility s akcemi povolen: _\#_ | Tato funkce čeká na implementaci. V současné době nejsou akce generovány během hlavního plánování, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. Hlavním účelem akcí je navrhovat změny ve stávajících objednávkách. Vyhodnoťte, zda jsou akce aktivně uplatňovány jako součást vašich obchodních procesů nebo zda jsou dostatečné informace o zpoždění související s objednávkami. | Říjen 2021 - duben 2022 |
| Základní kalendáře | Kalendáře používající základní kalendář: _\#_ | Tato funkce čeká na implementaci. V současné době je základní kalendář ignorován při povolení optimalizace plánování. Vyhodnoťte, zda je pro vaše obchodní procesy potřeba základní kalendář nebo zda postačuje přímé nastavení v kalendářích. | Duben - říjen 2021 | 
| Kódy dispozice dávky | Vzory dispozice dávky bez čisté hodnoty: _\#_ | Tato funkce čeká na implementaci. V současné době jsou dispoziční kódy dávky ignorovány, pokud je povolena optimalizace plánování. | Říjen 2021 - duben 2022 |
| Příslib na základě ověření dostupné kapacity (CTP) | Výchozí nastavení objednávky s datem dodání nastaveným na CTP: _\#_ | Tato funkce čeká na implementaci. V současnosti je CTP ignorováno, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | Říjen 2021 - duben 2022 |
| Kopírovat statický do dynamického plánu | Kopírování statického do dynamického plánu je povoleno na parametrech hlavního plánování. | Optimalizace plánování nekopíruje statický plán do dynamického plánu bez ohledu na toto nastavení. Obecně platí, že tento koncept je méně významný z důvodu rychlosti a úplného obnovení, které poskytuje optimalizace plánování. Pokud jsou použity dva nebo více plánů, je třeba pro každý plán spustit hlavní plánování. | Říjen 2021 - duben 2022 |
| Potvrzení | Skupiny disponibility s nastavenou ochrannou dobou automatického potvrzení: _\#_ | Ve verzi 10.0.7 a novějších je potvrzení podporováno jako samostatná dávková úloha potvrzení po dokončení hlavního plánování (za předpokladu , že ve [správě funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) byla povolena funkce _Automatické potvrzení pro optimalizaci plánování_). Všimněte si, že automatické potvrzení pro optimalizaci plánování je založeno na datu objednávky (počáteční datum), nikoli na datu požadavku (koncové datum). Toto chování zajišťuje, že k potvrzení plánovaných objednávek dojde včas, aniž by bylo nutné zahrnout dobu realizace do ochranné doby potvrzování. | Podporováno |
| Potvrzení | Záznamy disponibility položky s nastaveným automatickým potvrzením: _\#_ | Ve verzi 10.0.7 a novějších je automatické potvrzení podporováno jako samostatná dávková úloha potvrzení po dokončení hlavního plánování (za předpokladu, že ve [správě funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) byla povolena funkce _Automatické potvrzení pro optimalizaci plánování_). Všimněte si, že automatické potvrzení pro optimalizaci plánování je založeno na datu objednávky (počáteční datum), nikoli na datu požadavku (koncové datum). Toto chování zajišťuje, že k potvrzení plánovaných objednávek dojde včas, aniž by bylo nutné zahrnout dobu realizace do ochranné doby potvrzování. | Podporováno |
| Potvrzení | Hlavní plány s nastaveným automatickým potvrzením: _\#_ | Ve verzi 10.0.7 a novějších je automatické potvrzení podporováno jako samostatná dávková úloha potvrzení po dokončení hlavního plánování (za předpokladu, že ve [správě funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) byla povolena funkce _Automatické potvrzení pro optimalizaci plánování_). Všimněte si, že automatické potvrzení pro optimalizaci plánování je založeno na datu objednávky (počáteční datum), nikoli na datu požadavku (koncové datum). Toto chování zajišťuje, že k potvrzení plánovaných objednávek dojde včas, aniž by bylo nutné zahrnout dobu realizace do ochranné doby potvrzování. | Podporováno |
| FitAnalysisPlanningItems | Položky plánování: _\#_ | Tato funkce čeká na implementaci. V současné době jsou položky plánování zpracovány jako běžné položky, když je povolena optimalizace plánování. | Říjen 2021 - duben 2022 |
| Prognóza | Skupiny disponibility s povolenou možností „zahrnout mezipodnikové objednávky“: _\#_ | Tato funkce je nyní podporována. Další informace viz [Mezipodnikové plánování](Intercompany-planning.md) | Podporováno |
| Prognóza | Skupiny disponibility s nastavením „snížit prognózu podle“ nastavené na jinou hodnotu než „objednávky“: _\#_ | Tato funkce je nyní podporována. Další informace naleznete v části [Hlavní plánování s prognózami poptávky](demand-forecast.md). | Podporováno |
| Prognóza | Modely prognóz s dílčími modely: _\#_ |  Tato funkce je nyní podporována. Další informace naleznete v části [Hlavní plánování s prognózami poptávky](demand-forecast.md). | Podporováno |
| Prognóza | Hlavní plány s povolenou možností „zahrnout prognózu dodávek“: _\#_ | Tato funkce čeká na implementaci. Prognózy dodávek nejsou aktuálně podporovány, pokud je povolena optimalizace plánování. Budou ignorovány bez ohledu na toto nastavení. | Říjen 2021 - duben 2022 |
| Ochranná doba zablokování | Skupiny disponibility s nastavenou ochrannou dobou zablokování: _\#_ | Ochranná doba zablokování se často nepoužívá a momentálně neexistují žádné plány, že by byla zahrnuta do optimalizace plánování. V současnosti je ignorováno nastavení ochranné doby zablokování, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | Nevztahuje se |
| Ochranná doba zablokování | Záznamy disponibility položky s nastavenou ochrannou dobou zablokování: _\#_ | Ochranná doba zablokování se často nepoužívá a momentálně neexistují žádné plány, že by byla zahrnuta do optimalizace plánování. V současnosti je ignorováno nastavení ochranné doby zablokování, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | Nevztahuje se |
| Ochranná doba zablokování | Hlavní plány s nastavenou ochrannou dobou zablokování: _\#_ | Ochranná doba zablokování se často nepoužívá a momentálně neexistují žádné plány, že by byla zahrnuta do optimalizace plánování. V současnosti je ignorováno nastavení ochranné doby zablokování, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | Nevztahuje se |
| Mezipodnikové | Hlavní plány zahrnující plánovanou navazující poptávku: _\#_ | Tato funkce je nyní podporována. Další informace viz [Mezipodnikové plánování](Intercompany-planning.md) | Podporováno |
| Kanban | Záznamy disponibility položky s plánovaným typem objednávky kanban: _\#_ | Tato funkce čeká na implementaci. V současné době je disponibilita položky nastavená na Kanban ignorována, pokud je povolena optimalizace plánování. Typ kanbanové plánované objednávky vytvoří upozornění během hlavního plánování a vytvoří se plánované nákupní objednávky, které pokrývají související poptávku. | Říjen 2021 - duben 2022 |
| Kanban | Položky s výchozím typem objednávky kanban: _\#_ | V současné době je výchozí typ objednávky nastavený na Kanban ignorován, pokud je povolena optimalizace plánování. Výchozí typ kanbanové objednávky vytvoří upozornění během hlavního plánování a vytvoří se plánované nákupní objednávky, které pokrývají související poptávku. | Říjen 2021 - duben 2022 |
| Stav životního cyklu produktu | Stavy životního cyklu produktu neaktivní pro plánování: _\#_ | Tato funkce je nyní podporována. Další informace viz [Vyloučení produktů s konkrétními stavy životního cyklu produktu](product-lifecycle-state.md) | Podporováno |
| Výrobní | Řádky kusovníku se zaokrouhlením nebo vícenásobným nastavením: _\#_ | Tato funkce čeká na implementaci. V současné době je zaokrouhlení a více nastavení ignorováno na řádcích kusovníku při povolení optimalizace plánování bez ohledu na toto nastavení. | Duben - říjen 2021 |
| Výrobní | Řádky kusovníků/receptur s měřením receptury: _\#_ | Tato funkce čeká na implementaci. V současné době je měření receptury ignorováno na řádcích kusovníku a receptur při povolení optimalizace plánování bez ohledu na toto nastavení. | 2021. říjen |
| Výrobní | Řádky kusovníků/receptur s nahrazením položky (skupiny plánu): _\#_ | Tato funkce čeká na implementaci. V současné době je nahrazení položky (skupiny plánu) ignorováno na řádcích kusovníku a receptur při povolení optimalizace plánování bez ohledu na toto nastavení. | 2021. říjen |
| Výrobní | Řádky kusovníku/receptur s negativním množstvím: _\#_ | Tato funkce čeká na implementaci. Řádky kusovníku a receptury, které mají záporné množství, budou zahrnuty s množstvím 0 (nula) a při povolení optimalizace plánování bude vydána výstraha. Aktualizujte hlavní data, abyste se vyhnuli varování. | 2021. říjen |
| Výrobní | Řádky kusovníků/receptur se spotřebou zdrojů: _\#_ | Tato funkce čeká na implementaci. V současné době se řádky kusovníku a receptur se spotřebou zdroje při povolení optimalizace plánování ignorují. Když je tato funkce podporována, bude požadavek na materiál nastaven na datum zahájení výroby. Dokud nebude tato funkce podporována, nebudou se generovat požadavky na materiály, které jsou označeny příznakem spotřeby prostředků. | Duben - říjen 2021 |
| Výrobní | Řádky kusovníků/receptur s krokovou spotřebou: _\#_ | Tato funkce čeká na implementaci. V současné době je ignorována kroková spotřeba na řádcích kusovníku a receptur při povolení optimalizace plánování. | 2021. říjen |
| Výrobní | Kusovníky s definovaným konstantním nebo variabilním odpadem: _\#_ | Tato funkce čeká na implementaci. V současné době je při povolení optimalizace plánování ignorován konstantní a variabilní odpad, které jsou definovány v kusovnících. | Říjen 2021 - duben 2022 |
| Výrobní | Kusovníky se subdodávkami: _\#_ | Tato funkce čeká na implementaci. V současnosti je ignorováno nastavení subdodávek v kusovníku, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | Říjen 2021 - duben 2022 |
| Výrobní | Kusovníky bez pracoviště: _\#_ | Tato funkce je nyní podporována. Další informace viz [Plánování výroby](production-planning.md) | Podporováno |
| Výrobní | Poptávka se specifickým kusovníkem nebo definovanými požadavky postupu: _\#_ | Tato funkce čeká na implementaci. V současné době jsou ignorovány konkrétní požadavky kusovníku nebo postupu definovanými pro poptávku (například dílčí kusovník nebo dílčí postup v prodejní objednávce), pokud je povolena optimalizace plánování. Bude použit standardní kusovník nebo postup bez ohledu na toto nastavení. | Říjen 2021 - duben 2022 |
| Výrobní | Verze receptur se souběžnými nebo vedlejšími produkty: _\#_ | Tato funkce čeká na implementaci. V současné době se při povolení optimalizace plánování ignorují souběžné a vedlejší produkty, které jsou přidruženy k verzi receptury. | 2021. říjen |
| Výrobní | Verze receptury s výtěžností: _\#_ | Tato funkce čeká na implementaci. V současné době se při povolení optimalizace plánování ignoruje výtěžnost, která je přidružena k verzi receptury. | Říjen 2021 - duben 2022 |
| Výrobní | Plány včetně pořadí: _\#_ | Tato funkce čeká na implementaci. V současnosti je pořadí ignorováno, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | Říjen 2021 - duben 2022 |
| Výrobní | Nezahájené uvolněné výrobní zakázky, kde je naplánované zahájení dříve než dnes: _\#_ | Tato funkce čeká na implementaci. V současné době, pokud dojde ke zpoždění výrobní zakázky, bude hlavní plánování předpokládat, že bude dokončena dnes. To je relevantní pro uvolněné výrobní zakázky, kde je datum dodání v minulosti, ale ještě nebylo dokončeno. | Říjen 2021 - duben 2022 |
| Výrobní | Zdroje naplánované s omezenou kapacitou: _\#_ | Tato funkce čeká na implementaci. Zdroje, které jsou naplánovány s omezenou kapacitou, jsou aktuálně ignorovány, pokud je povolena optimalizace plánování. Plánování je provedeno na základě výchozí doby realizace produktu. | Nekonečný: červen 2021, konečný: říjen 2021 |
| Výrobní | Postupy používané při plánování: _\#_ | Tato funkce čeká na implementaci. V současné době jsou postupy ignorovány, pokud je povolena optimalizace plánování. Použije se výchozí doba realizace z produktu. | Červenec 2021 |
| Výrobní | Rezervace řádku prodeje pomocí rozpadu: _\#_ | Rezervace řádku prodeje, která používá rozpad, není podporována, pokud je povolena optimalizace plánování. | 2021. říjen |
| Výrobní | Plánování s rozpadem výrobních zakázek: _\#_ | Plánování, které používá rozpad výrobních zakázek, není podporováno, pokud je povolena optimalizace plánování. Výrobní zakázky lze plánovat individuálně. | 2021. říjen |
| Požadavek na nabídky | Hlavní plány s povolenými požadavky na nabídku: _\#_ | Tato funkce čeká na implementaci. V současné době nejsou požadavky na nabídku (RFQ) považovány za poptávku v případě, že je povolena optimalizace plánování. Budou ignorovány bez ohledu na toto nastavení. | Říjen 2021 - duben 2022 |
| Žádanky | Hlavní plány s povolenými žádankami: _\#_ | Tato funkce je nyní podporována. Další informace naleznete v tématu [Nákupní žádanky](purchase-requisitions.md) | Podporováno |
| Pojistné doby | Skupiny disponibility s pojistnou dobou: _\#_ | Tato funkce je nyní částečně podporována. Další informace viz [Pojistné doby](safety-margins.md) | Marže účtenky: Podporováno. Změna pořadí a rezerva výdeje: duben 2021 - říjen 2021 |
| Pojistné doby | Hlavní plány s pojistnou dobou: _\#_ | Tato funkce je nyní částečně podporována. Další informace viz [Pojistné doby](safety-margins.md) | Marže účtenky: Podporováno. Změna pořadí a rezerva výdeje: duben 2021 - říjen 2021 |
| Plnění rezervních zásob | Záznamy disponibility položky s hodnotou „splnit minimum“ se liší od „dnešní datum a čas pořízení“: _\#_ | Optimalizace plánování vždy používá *dnešní datum a čas pořízení*. Tato změna je provedena kvůli přípravě na zjednodušené nastavení plánování v budoucnu a k zajištění výsledku s akcemi. Není-li k dispozici doba pořízení pro pojistnou zásobu, plánované objednávky, které jsou vytvořeny pro aktuální nízké zásoby na skladě, budou vždy zpožděny kvůli době realizace. Toto chování může způsobit výrazný nedostatek informací a nežádoucí plánované objednávky. Doporučeným postupem je změna nastavení tak, aby bylo použito *dnešní datum a čas pořízení*. Aktualizujte hlavní data, abyste se vyhnuli varování. | Nevztahuje se |
| Prodejní nabídky | Hlavní plány s povolenými prodejními nabídkami: _\#_ | Tato funkce čeká na implementaci. V současné době nejsou nabídky brány v potaz, pokud je povolena optimalizace plánování. Budou ignorovány bez ohledu na toto nastavení. | Říjen 2021 - duben 2022 |
| Skladovatelnost | Hlavní plány s povolenou skladovatelností: _\#_ | Tato funkce čeká na implementaci. V současnosti není skladovatelnost brána v potaz, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | 2021. říjen |

## <a name="additional-resources"></a>Další prostředky

[Přehled optimalizace plánování](planning-optimization-overview.md)

[Začínáme s optimalizací plánování](get-started.md)

[Zobrazení historie plánu a protokolů plánování](plan-history-logs.md)

[Použití filtrů v plánu](plan-filters.md)

[Zrušení úlohy plánování](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

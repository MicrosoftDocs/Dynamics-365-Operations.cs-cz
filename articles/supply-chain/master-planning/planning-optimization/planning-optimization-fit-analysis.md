---
title: Analýza přizpůsobení pro optimalizaci plánování
description: V tomto článku je vysvětleno, jak ověřit aktuální nastavení a data proti funkcím funkce optimalizace plánování.
author: t-benebo
ms.date: 08/11/2022
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 15ec53c1f13b3017fb6e829bd1c8e99fbb938ce3
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689987"
---
# <a name="planning-optimization-fit-analysis"></a>Analýza přizpůsobení pro optimalizaci plánování

[!include [banner](../../includes/banner.md)]

Výsledek analýzy přizpůsobení pro optimalizaci plánování byste měli analyzovat jako součást procesu migrace. Všimněte si, že se rozsah optimalizace plánování nerovná aktuální integrované hlavní plánovací funkce. Doporučujeme, abyste spolupracovali se svým partnerem a v rámci přípravy na migraci si přečetli dokumentaci. 

Analýza přizpůsobení optimalizace plánování vám může ukázat, kde se může výsledek lišit mezi integrovaným hlavním plánovacím modulem a optimalizací plánování. Tato analýza probíhá na základě vašeho aktuálního nastavení a dat. 

Chcete-li si zobrazit výsledek analýzy přizpůsobení pro optimalizaci plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Analýza přizpůsobení pro optimalizaci plánování** a potom vyberte **Spustit analýzu**. Pokud analýza nalezne nějaké nekonzistence, budou uvedeny na stejné stránce. (Provádění analýzy může trvat několik minut.)

> [!NOTE]
>
> - Některé nesrovnalosti nelze identifikovat analýzou přizpůsobení optimalizace plánování. Další informace viz [Rozdíly mezi klasickým hlavním plánováním a optimalizací plánování](planning-optimization-differences-with-built-in.md).
>
> - Pokud jsou nalezeny nekonzistence, můžete stále používat optimalizaci plánování. Výsledky analýzy přizpůsobení zobrazují pouze místa, kde plánovací služba nerespektuje vaše aktuální nastavení. Jinými slovy, zobrazují místa, kde některé procesy mohou být ignorovány nebo nejsou podporovány.

## <a name="analysis-results-example-1"></a>Výsledky analýzy: Příklad 1

- **Funkce:** Výroba
- **Problém:** Položky s úrovní kusovníku (BOM) vyšší než nula: 56
- **Vysvětlení:** Analýza přizpůsobení nalezla 56 položek, které mají pro výrobu nastaven kusovník. Vzhledem k tomu, že aktuální verze optimalizace plánování nepodporuje výrobu, optimalizace plánování vygeneruje plánované nákupní objednávky namísto plánovaných výrobních zakázek. Zobrazí se také upozornění, které obsahuje seznam ovlivněných položek.

## <a name="analysis-results-example-2"></a>Výsledky analýzy: Příklad 2

- **Funkce:** Akce
- **Problém:** Skupiny disponibility s povolenou kalkulací akcí: 6
- **Vysvětlení:** Analýza přizpůsobení našla šest skupin disponibility, kde je zapnut výpočet akce. Vzhledem k tomu, že aktuální verze optimalizace plánování nepodporuje akce, nebudou při hlavním plánování generovány žádné akce.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Přehled možných výsledků analýzy přizpůsobení

V následující tabulce jsou uvedeny různé výsledky, které lze zobrazit po analýze přizpůsobení. Symbol čísla (*\#*) bude nahrazen číslem označujícím počet záznamů s uvedeným problémem.

> [!IMPORTANT]
> U funkcí, které ještě nejsou podporovány, jsou v následující tabulce uvedeny očekávané informace o dostupnosti, které jsou odhadovány na základě našeho aktuálního plánu. Tyto odhady se mohou bez upozornění změnit.

| Funkce | Uvedený problém | Vysvětlení | Očekávaná dostupnost |
| --- | --- | --- | --- |
| Akce | Výpočet skupin disponibility s akcemi povolen: *\#* | Tato funkce je nyní podporována. | Podporováno |
| Základní kalendáře | Kalendáře používající základní kalendář: *\#* | Tato funkce je nyní podporována. | Podporováno | 
| Kódy dispozice dávky | Vzory dispozice dávky bez čisté hodnoty: *\#* | Tato funkce je nyní podporována. Další informace viz [Označení dávky jako K dispozici nebo Není k dispozici pomocí kódů dispozice dávky](../../inventory/batch-disposition-codes.md) | Podporováno |
| Příslib na základě ověření dostupné kapacity (CTP) | Výchozí nastavení objednávky s datem dodání nastaveným na CTP: *\#* | V Supply Chain Management 10.0.28 a novějších proces nazvaný *CTP pro optimalizaci plánování* zpřístupní potvrzená data odeslání a přijetí po spuštění dynamického plánu. U starších verzí Supply Chain Management je starší nastavení CTP ignorováno, když je povolena optimalizace plánování. | Podporováno |
| Kopírovat statický do dynamického plánu | Kopírování statického do dynamického plánu je povoleno na parametrech hlavního plánování. | Optimalizace plánování nekopíruje statický plán do dynamického plánu bez ohledu na toto nastavení. Obecně platí, že tento koncept je méně významný z důvodu rychlosti a úplného obnovení, které poskytuje optimalizace plánování. Pokud jsou použity dva nebo více plánů, je třeba pro každý plán spustit hlavní plánování. | Není k dispozici |
| Potvrzení | Skupiny disponibility s nastavenou ochrannou dobou automatického potvrzení: *\#* | Ve verzi 10.0.7 a novějších je potvrzení podporováno jako samostatná dávková úloha potvrzení po dokončení hlavního plánování (za předpokladu , že ve [správě funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) byla povolena funkce *Automatické potvrzení pro optimalizaci plánování*). Všimněte si, že automatické potvrzení pro optimalizaci plánování je založeno na datu objednávky (počáteční datum), nikoli na datu požadavku (koncové datum). Toto chování zajišťuje, že k potvrzení plánovaných objednávek dojde včas, aniž by bylo nutné zahrnout dobu realizace do ochranné doby potvrzování. | Podporováno |
| Potvrzení | Záznamy disponibility položky s nastaveným automatickým potvrzením: *\#* | Ve verzi 10.0.7 a novějších je automatické potvrzení podporováno jako samostatná dávková úloha potvrzení po dokončení hlavního plánování (za předpokladu, že ve [správě funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) byla povolena funkce *Automatické potvrzení pro optimalizaci plánování*). Všimněte si, že automatické potvrzení pro optimalizaci plánování je založeno na datu objednávky (počáteční datum), nikoli na datu požadavku (koncové datum). Toto chování zajišťuje, že k potvrzení plánovaných objednávek dojde včas, aniž by bylo nutné zahrnout dobu realizace do ochranné doby potvrzování. | Podporováno |
| Potvrzení | Hlavní plány s nastaveným automatickým potvrzením: *\#* | Ve verzi 10.0.7 a novějších je automatické potvrzení podporováno jako samostatná dávková úloha potvrzení po dokončení hlavního plánování (za předpokladu, že ve [správě funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) byla povolena funkce *Automatické potvrzení pro optimalizaci plánování*). Všimněte si, že automatické potvrzení pro optimalizaci plánování je založeno na datu objednávky (počáteční datum), nikoli na datu požadavku (koncové datum). Toto chování zajišťuje, že k potvrzení plánovaných objednávek dojde včas, aniž by bylo nutné zahrnout dobu realizace do ochranné doby potvrzování. | Podporováno |
| FitAnalysisPlanningItems | Položky plánování: *\#* | Tato funkce čeká na implementaci. V současné době jsou položky plánování zpracovány jako běžné položky, když je povolena optimalizace plánování. | Vlna verze 2022 2 nebo novější |
| Prognóza | Skupiny disponibility s povolenou možností „zahrnout mezipodnikové objednávky“: *\#* | Tato funkce je nyní podporována. Další informace viz [Mezipodnikové plánování](Intercompany-planning.md) | Podporováno |
| Prognóza | Skupiny disponibility s nastavením „snížit prognózu podle“ nastavené na jinou hodnotu než „objednávky“: *\#* | Tato funkce je nyní podporována. Další informace naleznete v části [Hlavní plánování s prognózami poptávky](demand-forecast.md). | Podporováno |
| Prognóza | Modely prognóz s dílčími modely: *\#* |  Tato funkce je nyní podporována. Další informace naleznete v části [Hlavní plánování s prognózami poptávky](demand-forecast.md). | Podporováno |
| Prognóza | Hlavní plány s povolenou možností „zahrnout prognózu dodávek“: *\#* | Tato funkce čeká na implementaci. Prognózy dodávek nejsou aktuálně podporovány, pokud je povolena optimalizace plánování. Budou ignorovány bez ohledu na toto nastavení. | Vlna verze 2022 2 nebo novější |
| Ochranná doba zablokování | Skupiny disponibility s nastavenou ochrannou dobou zablokování: *\#* | Tato funkce čeká na implementaci. V současnosti je ignorováno nastavení ochranné doby zablokování, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | Vlna verze 2022 2 |
| Ochranná doba zablokování | Záznamy disponibility položky s nastavenou ochrannou dobou zablokování: *\#* | Tato funkce čeká na implementaci. V současnosti je ignorováno nastavení ochranné doby zablokování, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | Vlna verze 2022 2 |
| Ochranná doba zablokování | Hlavní plány s nastavenou ochrannou dobou zablokování: *\#* | Tato funkce čeká na implementaci. V současnosti je ignorováno nastavení ochranné doby zablokování, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | Vlna verze 2022 2 |
| Mezipodnikové | Hlavní plány zahrnující plánovanou navazující poptávku: *\#* | Tato funkce je nyní podporována. Další informace viz [Mezipodnikové plánování](Intercompany-planning.md) | Podporováno |
| Kanban | Záznamy disponibility položky s plánovaným typem objednávky kanban: *\#* | Tato funkce čeká na implementaci. V současné době je disponibilita položky nastavená na Kanban ignorována, pokud je povolena optimalizace plánování. Typ kanbanové plánované objednávky vytvoří upozornění během hlavního plánování a vytvoří se plánované nákupní objednávky, které pokrývají související poptávku. | Budoucí vlna |
| Kanban | Položky s výchozím typem objednávky kanban: *\#* | V současné době je výchozí typ objednávky nastavený na Kanban ignorován, pokud je povolena optimalizace plánování. Výchozí typ kanbanové objednávky vytvoří upozornění během hlavního plánování a vytvoří se plánované nákupní objednávky, které pokrývají související poptávku. | Budoucí vlna |
| Stav životního cyklu produktu | Stavy životního cyklu produktu neaktivní pro plánování: *\#* | Tato funkce je nyní podporována. Další informace viz [Vyloučení produktů s konkrétními stavy životního cyklu produktu](product-lifecycle-state.md) | Podporováno |
| Výroba | Řádky kusovníku se zaokrouhlením nebo vícenásobným nastavením: *\#* | Tato funkce čeká na implementaci. V současné době je zaokrouhlení a více nastavení ignorováno na řádcích kusovníku při povolení optimalizace plánování bez ohledu na toto nastavení. | Budoucí vlna|
| Výrobní | Řádky kusovníků/receptur s měřením receptury: *\#* | Tato funkce čeká na implementaci. V současné době je měření receptury ignorováno na řádcích kusovníku a receptur při povolení optimalizace plánování bez ohledu na toto nastavení. | Vlna verze 2022 2 |
| Výrobní | Řádky kusovníků/receptur s nahrazením položky (skupiny plánu): *\#* | Tato funkce čeká na implementaci. V současné době je nahrazení položky (skupiny plánu) ignorováno na řádcích kusovníku a receptur při povolení optimalizace plánování bez ohledu na toto nastavení. | Vlna verze 2022 2 |
| Výrobní | Řádky kusovníku/receptur s negativním množstvím: *\#* | Tato funkce čeká na implementaci. Řádky kusovníku a receptury, které mají záporné množství, budou zahrnuty s množstvím 0 (nula) a při povolení optimalizace plánování bude vydána výstraha. Aktualizujte hlavní data, abyste se vyhnuli varování. | Vlna verze 2022 2 |
| Výrobní | Řádky kusovníků/receptur se spotřebou zdrojů: *\#* | Tato funkce čeká na implementaci. V současné době se řádky kusovníku a receptur se spotřebou zdroje při povolení optimalizace plánování ignorují. Když je tato funkce podporována, bude požadavek na materiál nastaven na datum zahájení výroby. Dokud nebude tato funkce podporována, nebudou se generovat požadavky na materiály, které jsou označeny příznakem spotřeby prostředků. | Vlna verze 2022 2 |
| Výrobní | Řádky kusovníků/receptur s krokovou spotřebou: *\#* | Tato funkce čeká na implementaci. V současné době je ignorována kroková spotřeba na řádcích kusovníku a receptur při povolení optimalizace plánování. | Vlna verze 2022 2 |
| Výrobní | Kusovníky s definovaným konstantním nebo variabilním odpadem: *\#* | Tato funkce čeká na implementaci. V současné době je při povolení optimalizace plánování ignorován konstantní a variabilní odpad, které jsou definovány v kusovnících. | Vlna verze 2022 2 |
| Výrobní | Kusovníky se subdodávkami: *\#* | Tato funkce je nyní podporována. | Podporováno |
| Výrobní | Kusovníky bez pracoviště: *\#* | Tato funkce je nyní podporována. Další informace viz [Plánování výroby](production-planning.md) | Podporováno |
| Výroba | Poptávka se specifickým kusovníkem nebo definovanými požadavky postupu: *\#* | Tato funkce čeká na implementaci. V současné době jsou ignorovány konkrétní požadavky kusovníku nebo postupu definovanými pro poptávku (například dílčí kusovník nebo dílčí postup v prodejní objednávce), pokud je povolena optimalizace plánování. Bude použit standardní kusovník nebo postup bez ohledu na toto nastavení. | Vlna verze 2022 2 |
| Výrobní | Verze receptur se souběžnými nebo vedlejšími produkty: *\#* | Tato funkce čeká na implementaci. V současné době se při povolení optimalizace plánování ignorují souběžné a vedlejší produkty, které jsou přidruženy k verzi receptury. | Vlna verze 2022 2 |
| Výrobní | Verze receptury s výtěžností: *\#* | Tato funkce čeká na implementaci. V současné době se při povolení optimalizace plánování ignoruje výtěžnost, která je přidružena k verzi receptury. | Vlna verze 2022 2 |
| Výrobní | Plány včetně pořadí: *\#* | Tato funkce čeká na implementaci. V současnosti je pořadí ignorováno, pokud je povolena optimalizace plánování, bez ohledu na toto nastavení. | Vlna verze 2022 2 |
| Výrobní | Nezahájené uvolněné výrobní zakázky, kde je naplánované zahájení dříve než dnes: *\#* | Tato funkce čeká na implementaci. V současné době, pokud dojde ke zpoždění výrobní zakázky, bude hlavní plánování předpokládat, že bude dokončena dnes. To je relevantní pro uvolněné výrobní zakázky, kde je datum dodání v minulosti, ale ještě nebylo dokončeno. | Budoucí vlna |
| Výrobní | Zdroje naplánované s omezenou kapacitou: *\#* | Tato funkce je nyní podporována.| Podporováno |
| Výrobní | Postupy používané při plánování: *\#* | Tato funkce je podporována. | Podporováno |
| Výrobní | Rezervace řádku prodeje pomocí rozpadu: *\#* | Rezervace řádku prodeje, která používá rozpad, není podporována, pokud je povolena optimalizace plánování. | Budoucí vlna |
| Výrobní | Plánování s rozpadem výrobních zakázek: *\#* | Plánování, které používá rozpad výrobních zakázek, není podporováno, pokud je povolena optimalizace plánování. Výrobní zakázky lze plánovat individuálně. | Budoucí vlna |
| Požadavek na nabídky | Hlavní plány s povolenými požadavky na nabídku: *\#* | Tato funkce čeká na implementaci. V současné době nejsou požadavky na nabídku (RFQ) považovány za poptávku v případě, že je povolena optimalizace plánování. Budou ignorovány bez ohledu na toto nastavení. | Vlna verze 2022 2 |
| Žádanky | Hlavní plány s povolenými žádankami: *\#* | Tato funkce je nyní podporována. Další informace naleznete v tématu [Nákupní žádanky](purchase-requisitions.md) | Podporováno |
| Pojistné doby | Skupiny disponibility s pojistnou dobou: *\#* | Tato funkce je nyní podporována. Další informace viz [Pojistné doby](safety-margins.md) | Podporováno |
| Pojistné doby | Hlavní plány s pojistnou dobou: *\#* | Tato funkce je nyní podporována. Další informace viz [Pojistné doby](safety-margins.md) |  Podporováno |
| Plnění rezervních zásob | Záznamy disponibility položky s hodnotou „splnit minimum“ se liší od „dnešní datum a čas pořízení“: *\#* | Optimalizace plánování vždy používá *dnešní datum a čas pořízení*. Tato změna je provedena kvůli přípravě na zjednodušené nastavení plánování v budoucnu a k zajištění výsledku s akcemi. Není-li k dispozici doba pořízení pro pojistnou zásobu, plánované objednávky, které jsou vytvořeny pro aktuální nízké zásoby na skladě, budou vždy zpožděny kvůli době realizace. Toto chování může způsobit výrazný nedostatek informací a nežádoucí plánované objednávky. Doporučeným postupem je změna nastavení tak, aby bylo použito *dnešní datum a čas pořízení*. Aktualizujte hlavní data, abyste se vyhnuli varování. | Nevztahuje se |
| Prodejní nabídky | Hlavní plány s povolenými prodejními nabídkami: *\#* | Tato funkce čeká na implementaci. V současné době nejsou nabídky brány v potaz, pokud je povolena optimalizace plánování. Budou ignorovány bez ohledu na toto nastavení. | Vlna verze 2022 2 nebo novější |
| Skladovatelnost | Hlavní plány s povolenou skladovatelností: *\#* | Tato funkce čeká na implementaci. | Vlna verze 2022 2 |

## <a name="additional-resources"></a>Další prostředky

[Přehled optimalizace plánování](planning-optimization-overview.md)

[Začínáme s optimalizací plánování](get-started.md)

[Rozdíly mezi klasickým hlavním plánováním a optimalizací plánování](planning-optimization-differences-with-built-in.md)

[Parametry, které optimalizace plánování nepoužívá](not-used-parameters.md)

[Zobrazení historie pánů a plánovacích protokolů](plan-history-logs.md)

[Použití filtrů v plánu](plan-filters.md)

[Zrušení úlohy plánování](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

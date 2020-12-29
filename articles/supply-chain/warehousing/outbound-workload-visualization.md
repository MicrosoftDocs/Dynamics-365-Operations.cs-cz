---
title: Vizualizace odchozího pracovní vytížení
description: Toto téma popisuje informace o vizualizaci odchozího pracovní vytížení. Tato funkce umožňuje správcům skladu a supervizorům vytvářet vlastní grafy pracovního vytížení, které lze použít k monitorování postupu aktuální práce a jejího množství, které zbývá. Manažeři skladu mohou podle potřeby vytvářet více zobrazení a nastavit automatické obnovování.
author: Mirzaab
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: cbfb395c9103ff31979bfd57333f689e38915652
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645422"
---
# <a name="outbound-workload-visualization"></a>Vizualizace odchozího pracovní vytížení

[!include [banner](../includes/banner.md)]

Pokročilé možnosti nastavení, které jsou přístupné ze stránky **Vizualizace odchozího pracovní vytížení** umožňuje manažerům skladu a supervizorům vytvářet vlastní grafy pracovního vytížení, které lze použít k monitorování postupu aktuální práce a jejího zbývajícího množství. Manažeři skladu mohou podle potřeby vytvářet více zobrazení a nastavit automatické obnovování. Vizualizace odchozího pracovní vytížení jsou vhodné pro zobrazení na stránkách výkonu skladu.

Tuto funkci lze použít ke sledování postupu práce výdeje. Tato funkce je integrována do správy práce a pokud je nastavena správa práce, mohou vizualizace odchozího pracovní vytížení zobrazit výpočet počtu hodin, které zbývají pro zobrazenou práci výdeje (filtrovanou).

## <a name="turn-on-the-outbound-workload-visualization-feature"></a>Zapnutí funkce vizualizace odchozího pracovní vytížení

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Vizualizace odchozího pracovní vytížení*

## <a name="set-up-outbound-workload-visualizations"></a>Nastavení vizualizací odchozího pracovní vytížení

Chcete-li nastavit své vizualizace, vytvoříte kolekci filtrů (zobrazení) a každý filtr navrhnete tak, aby zobrazoval jiný typ analýzy. Použijte stránku **Konfigurovat filtry** pro navržení filtrů.

Chcete-li nastavit vizualizaci odchozího pracovní vytížení, postupujte takto.

1. Přejděte na **Řízení skladu \> Sestavy sledování skladu \> Vizualizace odchozího pracovní vytížení**.

    Zobrazí se stránka **Vizualizace odchozího pracovní vytížení**. Po vytvoření některých filtrů se na této stránce zobrazí vaše vizualizace. Můžete vytvořit tolik filtrů, kolik chcete. Všechny filtry, které vytvoříte, jsou uloženy pod vaším uživatelským účtem, abyste je mohli později použít. Jinými slovy, každý uživatel bude mít vlastní sadu filtrů, které vytvořil. Tyto filtry nebudou sdíleny s ostatními uživateli.

1. Na stránce **Vizualizace odchozího pracovní vytížení** v podokně akcí na kartě **Filtry** vyberte možnost **Konfigurovat filtry**.
1. Na stránce **Konfigurovat filtry** v podokně akcí vyberte **Nový**, přidejte filtr a poté pro něj nastavit následující pole:

    - **Tabulka seskupení osy X** - Vyberte tabulku obsahující pole, které by se mělo použít k seskupení hodnot v ose X.
    - **Pole seskupení osy X** - Z polí tabulky, která jste vybrali v poli **Tabulka seskupení osy X**, vyberte pole, které se má použít k seskupení hodnot v ose X.
    - **Tabulka hodnot osy X** - Vyberte tabulku obsahující pole, které by se mělo použít k další analýze skupin.
    - **Pole hodnot osy X** - Z polí tabulky, která jste vybrali v poli **Tabulka hodnot osy X**, vyberte pole s hodnotami, které by měly být analyzovány pro každou skupinu.
    - **Automatická aktualizace** - Vyberte, zda se má vizualizace automaticky aktualizovat.
    - **Interval aktualizace (minuty)** - Zadejte počet minut mezi automatickým obnovením.
    - **Úroveň zobrazení** - Vyberte, zda by měl graf zobrazovat otevřené čáry nebo počet otevřených záhlaví.
    - **Typ výdeje** - Pokud nastavíte pole **Úroveň zobrazení** na _Otevřené řádky_, vyberte, zda má počet otevřených řádků práce v grafu zahrnovat počáteční výdeje, postupné výdeje, nebo oba počáteční výdeje a přechodné výdeje.
    - **Pracoviště** - Vyberte pracoviště, pro které chcete načíst graf.
    - **Sklad** - Vyberte sklad, pro který chcete načíst graf.
    - **Dny k zahrnutí** - Zadejte počet dní v minulosti, pro které by měl být graf vygenerován.
    - **Typ pracovního příkazu** - Vyberte typy odchozích pracovních příkazů, na kterých chcete filtrovat.

    ![Stránka Konfigurace filtrů](media/work-viz-filters-1.png "Stránka Konfigurace filtrů")

1. Zavřete stránku **Konfigurovat filtry** pro návrat na stránku **Vizualizace odchozího pracovní vytížení**.

    Stránka **Vizualizace odchozího pracovní vytížení** nyní zobrazuje data na základě vašeho nového nastavení filtru. Váš nový filtr je nyní k dispozici a je vybrán v poli **Filtr**. V horní části grafu jsou k dispozici následující pole:

    - **Filtr** - Toto pole zahrnuje všechny filtry, které jste dosud vytvořili. Vyberte filtr a zobrazte jeho data v grafu.
    - **Poslední aktualizace** - Toto pole zobrazuje datum a čas, kdy byly informace v grafu naposledy aktualizovány.
    - **Odhadovaný/skutečný čas** - Pokud jsou ve vašem systému nastaveny pracovní standardy, nastavte tuto možnost na *Ano* pro zobrazení kumulovaných odhadovaných časů výdeje v horní části každého sloupce v grafu. Pokud nepoužíváte pracovní standardy, tato možnost není k dispozici.

    ![Příklad vizualizace](media/work-viz-chart.png "Příklad vizualizace")

1. Vyberte libovolný pruh v grafu a zobrazte podrobnosti přidruženého řádku práce.

    ![Podrobnosti řádku práce](media/work-viz-work-details.png "Podrobnosti řádku práce")

## <a name="example-outbound-workload-visualization-for-zones"></a>Příklad: Vizualizace odchozího pracovní vytížení pro zóny

V tomto příkladu chcete nastavit vizualizaci, která zobrazuje řádky práce pro každou zónu a stav každého řádku práce (_Otevřeno_, _Zavřeno_ nebo _Zrušeno_). V tomto případě můžete nastavit filtr, který má následující nastavení:

- **Název filtru** - Zadejte název tohoto filtru (například _Stav zóny a práce_).
- **Popis** - Zadejte krátký popis tohoto filtru (například _Stav zóny a práce_).
- **Tabulka seskupení osy X** - Vyberte _Místa._
- **Skupina osy X** - Vyberte _ID zóny_.
- **Tabulka hodnot osy X** - Vyberte _Práce_, protože chcete zobrazit práci podle zón.
- **Pole hodnot osy X** - Vyberte _Stav práce_, protože chcete zobrazit stav práce.
- **Automatická aktualizace** - Vyberte, zda se má vizualizace automaticky aktualizovat.
- **Typ výdeje** - Vyberte _Počáteční výdeje a přechodné výdeje_, protože chcete zahrnout počáteční výdeje i výdeje z přechodná míst. Jinými slovy, v zásadě chcete zahrnout všechny řádky práce výdeje, které máte.
- **Úroveň zobrazení** - Vyberte _Otevřené řádky_, protože chcete zobrazit informace podle řádku, nikoliv podle záhlaví práce.

Následující ilustrace znázorňuje příklad výsledného grafu.

![Vizualizace stavu zóny a práce](media/work-viz-chart.png "Vizualizace stavu zóny a práce")

Tento graf ukazuje dvě zóny pojmenované **FLOOR** a **BULK** a zónu s názvem **Prázdná**. Zóna **Prázdná** představuje všechny řádky práce, které nejsou členy žádné zóny. Graf vždy zobrazuje všechna nesouvisející filtrovaná data jako **Prázdná**, aby byla zajištěna co největší viditelnost. V zóně **FLOOR** graf ukazuje tři uzavřené čáry a čtyři otevřené čáry. V zóně **BULK** graf ukazuje čtyři uzavřené čáry jednu otevřenou čáru a 24 zrušených čar. Nakonec graf ukazuje osm uzavřených čar, které nejsou součástí žádné zóny, a proto jsou uvedeny jako **Prázdné**.

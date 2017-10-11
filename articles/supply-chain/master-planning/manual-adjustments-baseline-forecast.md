---
title: "Ruční úpravy základní prognózy"
description: "Tento článek vysvětluje, jak lze provádět ruční úpravy v základní prognóze, a jak zobrazit podrobnosti o prognóze."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 0b3b56aa838888461a6d27c6612e405a3cf59414
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Ruční úpravy základní prognózy

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje, jak lze provádět ruční úpravy v základní prognóze, a jak zobrazit podrobnosti o prognóze. 

Dříve, než začnete provádět ruční úpravy, je třeba mít na paměti několik konceptů z různých stran.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Tabulka na stránce Upravená prognóza poptávky
Stránka **Upravená prognóza poptávky** obsahuje tabulku, která obsahuje následující strukturu:

-   V prvním sloupci se zobrazují položky, alokační klíče položky, společnosti apod., pro které je prognóza generována. Podtitulek stránky obsahuje popis aktuálních dimenzí prognózy, které jsou zobrazeny v mřížce. Například, když je podnadpis stránky **Společnost / pracoviště / alokační klíč položky** a jedno ze záhlaví sloupců v mřížce je **USMF / 1 / D\_Alloc**, daný řádek popisuje prognózu pro společnost, s pracovištěm 1 a alokačním klíčem položky **D\_Alloc**.
-   Další sloupce představují intervaly prognóz, pro které jsou prognózy generované. Záhlaví každého sloupce je první datem intervalu prognózy, který je zobrazen ve sloupci.
-   Hodnoty buněk představují prognózu pro jednu položku, alokační klíč položky a tak dále, pro tento konkrétní interval prognózy.

## <a name="forecast-aggregation-and-deaggregation"></a>Seskupení a zrušení seskupení prognózy
Podtitulek stránky popisuje úroveň seskupení prognózy. 

Například pokud je podnadpis stránky **Společnost / pracoviště / alokační klíč / číslo položky / barva / velikost / konfigurace / styl**, neexistuje žádná agregace prognózy a prognóza se zobrazí na úrovni položky a jejích dimenzích. Pokud chcete změnit agregaci, použijte stránku **Změna dimenzí prognózy**, kterou lze otevřít z nabídky aplikace. 

Pokud chcete upravit prognózu, klikněte na libovolnou buňku, která je k dispozici, a zadejte upravenou hodnotu prognózy. Upravená buňka bude okamžitě zobrazena tučně a označí tak, že uvedená prognóza není prognózou vytvořenou ve službě generování prognózy poptávky, ale že je ručně upravená. 

Pokud změníte agregaci v situaci, kdy chcete zobrazit více agregovaná data, můžete použít stránku **Řádky prognózy poptávky** a zobrazit tak jednotlivé řádky prognóz, které tvoří agregovanou prognózu. 

Například jste vygenerovali prognózu na úrovni položky, ale víte, že poptávka pro tuto položku se zvýší pro všechna pracoviště z důvodu povýšení nebo jiné podobné události. V tomto případě můžete nastavit agregaci na **Společnost / alokační klíč položky / položka** na stránce **Změna dimenzí prognózy**. V mřížce **Upravená prognóza poptávky** můžete nastavit globální prognózu pro položku pro všechna pracoviště. Chcete-li vidět změny pro všechna pracoviště, otevřete stránku **Řádky prognózy poptávky**. Na této stránce uvidíte jeden řádek pro položku pro každé pracoviště, upravené množství prognózy a původní množství prognózy. 

Po provedení úprav prognózy na agregační úrovni použije systém vážené přidělení a rozdělí změny mezi řádky tvořící agregaci. 

Můžete provést také ruční úpravy na stránce **Řádky prognózy poptávky**, a to změnou buď buňky **Celkové množství** nebo **Množství** v mřížce pro zrušení agregace.

## <a name="viewing-details-of-the-forecast"></a>Zobrazení podrobností o prognóze
Můžete otevřít stránku **Podrobnosti prognózy poptávky** a zobrazit další informace o prognóze. 

Stránka **Podrobnosti prognózy poptávky** popisuje následující informace v grafickém a tabulkovém formátu:

-   Historická poptávka, na které je předpověď prognózy založena.
-   Aktuální prognóza používaná pro hlavní plánování.
-   Hodnoty nové prognózy poptávky a částky, o které byly ručně upraveny.
-   Interval spolehlivosti pro předpokládané hodnoty.
-   Model prognózy, který byl použit ke generování předpovědi. Pokud zobrazíte souhrnné údaje, zobrazí se seznam všech metod, které byly použity pro všechny agregované časové úseky.
-   Přesnost interního modelu (MAPE). Další informace o přesnosti prognózy naleznete v tématu [Sledování přesnosti prognózy](monitor-forecast-accuracy.md).

**Poznámky:**

-   Interval jistoty, který se zobrazí v části **Prognóza** na stránce, představuje rozdíl mezi horním limitem intervalu jistoty a dolním limitem intervalu jistoty. Pokud chcete zobrazit hodnoty pro dolní a horní limit, umístěte ukazatel myši do grafu v části **Historická poptávka a prognóza – graficky**.
-   Pokud používáte službu pro prognózu poptávky Microsoft Azure Machine Learning v aplikaci Finance and Operations, můžete určit podíl úrovně jistoty, který by měla mít generovaná prognóza. Interval jistoty obsahuje určitý úsek hodnot, které fungují jako vhodné odhady pro prognózu poptávky. 95% úroveň jistoty například označuje existenci 5% riziko, že prognóza poptávky se bude nacházet mimo rozsah intervalu jistoty.

Musíte také provést ruční úpravy prognózy na stránce **Podrobnosti prognózy poptávky** tím, že změníte hodnoty na řádku **Prognóza** v části **Prognóza**.

<a name="see-also"></a>Viz také
--------

[Měření přesnosti prognózy](monitor-forecast-accuracy.md)

[Generování statistické základní prognózy](generate-statistical-baseline-forecast.md)




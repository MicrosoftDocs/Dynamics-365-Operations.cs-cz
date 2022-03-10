---
title: Domovská stránka Hlavního plánování
description: Hlavní plánování umožňuje společnostem určit a vyvážit budoucí potřebu surovin a kapacit ke splnění cílů společnosti.
author: ChristianRytt
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7dd25fdd1549fb2fddff57dc2d9cf8762cfd6823
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416520"
---
# <a name="master-planning-home-page"></a>Domovská stránka Hlavního plánování

[!include [banner](../includes/banner.md)]

Ve svém jádru hlavní plánování umožňuje společnostem určit a vyvážit budoucí potřebu surovin a kapacit ke splnění cílů společnosti. Hlavní plánování posuzuje následující:

- Jaké materiály a kapacita jsou v současné době k dispozici?
- Jaké materiály a kapacita jsou nutné k dokončení výroby? Například co musí být vyrobeno, zakoupeno, převedeno nebo odloženo jako pojistná zásoba předtím, než můžete dokončit výrobu.

Hlavní plánování používá informace k výpočtu požadavků a vygenerování plánovaných objednávek.

Tři hlavní procesy plánování jsou:

- **Hlavní plánování** - Hlavní plán vypočítá čisté požadavky. To je založeno na skutečných aktuálních objednávkách a umožňuje společnostem řídit každodenního a každodenní doplňování skladu. Můžeme použít i termín *Plán čistých požadavků*. Další informace o hlavních plánech naleznete v tématu [Přehled hlavních plánů](master-plans.md).

- **Plánování prognóz** - Plánu prognózy vypočítá hrubé požadavky. To je založeno na budoucích odhadech (prognózách) a umožňuje společnostem provádět dlouhodobé plánování materiálů a kapacity. Další informace viz [Přehled prognózy poptávky](introduction-demand-forecasting.md).

- **Mezipodnikové hlavní plánování** - Mezipodnikový hlavní plán vypočítá čisté požadavky napříč právnickými osobami. Propojí poptávku a nabídku mezi společnostmi nejen z krátkodobého hlediska potvrzené poptávky a nabídky, ale i z dlouhodobého (ještě nepotvrzeného) hlediska poptávky a dodávek. Více informací získáte v části [Mezipodnikové plánování](planning-optimization/Intercompany-planning.md).

Společnosti mohou změnit výstup plánu. Mohou spouštět regenerativní, čistou změnu, nebo obojí. Regenerativní plány aktualizují všechny požadavky, zatímco plány čisté změny aktualizují pouze plán týkající se položek s novými požadavky, které se objevily od spuštění posledního plánování.

Hlavní plány zpravidla zahrnují krátkodobý horizont, což může být období od jednoho týdne po šest měsíců. Modul hlavního plánování určuje potřebu dodávek (surovin) a kapacit (zdrojů), které budou splňovat aktuální poptávku (čisté požadavky). Ve většině společností je to rozšířeno tak, aby to zahrnovalo nejdelší kumulativní dobu realizace mezi produkty, které mají být přijaty.

## <a name="learning-map"></a>Mapa výuky

Následující mapa výuky zobrazuje hlavní koncepty a úkoly, které tvoří rámec modulu Hlavní plánování. Informace o způsobu použití tohoto modulu získáte kliknutím na odkazy v sekci [Rychlé odkazy](#quick-links).

[![Mapa výuky pro hlavní plánování.](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>Rychlé odkazy

- [Přehled hlavních plánů](master-plans.md)  
- [Vygenerování plánu s omezeními](./tasks/constrained-plan.md)
- [Vytvoření materiálového plánu pro vedlejší produkty](./tasks/create-material-plan-co-products.md)
- [Přehled hlavního plánování a funkce více pracovišť](master-plan-multisite-functionality.md)
- [Vytvoření mezipodnikového plánu](./tasks/create-intercompany-plan.md)
- [Přehled prognózy poptávky](introduction-demand-forecasting.md)
- [Redukční klíče prognózy](reduction-keys.md)

## <a name="additional-resources"></a>Další zdroje

### <a name="roadmaps"></a>Plánování

Přejděte na [Přehled Microsoft Dynamics 365](https://roadmap.dynamics.com/) a zjistěte, jaké nové funkce se vydávají a jaké se chystají.

### <a name="blogs"></a>Blogy

Názory, novinky a další informace o hlavním plánování a jiných řešeních naleznete na [blogu Tým výzkumu a vývoje pro výrobu v Dynamics AX](/archive/blogs/axmfg/) a v [blogu Tým výzkumu a vývoje pro správu dodavatelského řetězce v Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm).

### <a name="task-guides"></a>Průvodci záznamem úloh

K dispozici je další nápověda v podobě průvodců záznamem úloh. Průvodce záznamem úloh zobrazíte kliknutím na tlačítko **Nápověda** na kterékoliv stránce.

### <a name="webinars"></a>Webináře

[Použití strojového učení Azure pro prognózu poptávky](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>Nahrávky z technické konference

- [Rozšíření funkce prognózy poptávky](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
- [Hlavní plánování – tipy a triky pro řešení problémů s výkonem](https://youtu.be/7v8BPmEs9Dg)
- [Ladění výkonu MRP](https://youtu.be/RLXybx20B5o)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
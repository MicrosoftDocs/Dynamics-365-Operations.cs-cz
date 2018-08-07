---
title: "Přehled prognózy poptávky"
description: "Pomocí prognózy poptávky lze odhadnout nezávislé poptávky z prodejních objednávek a závislých požadavků v libovolném oddělovacím bodě objednávky odběratele. Rozšířená pravidla redukce prognózy poptávky nabízí ideální řešení pro hromadné přizpůsobení."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 20eb67a341f462328bc73907fb3052b3405190d4
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="demand-forecasting-overview"></a>Přehled prognózy poptávky

[!include [banner](../includes/banner.md)]

Pomocí prognózy poptávky lze odhadnout nezávislé poptávky z prodejních objednávek a závislých požadavků v libovolném oddělovacím bodě objednávky odběratele. Rozšířená pravidla redukce prognózy poptávky nabízí ideální řešení pro hromadné přizpůsobení.

Pro generování základní prognózy je souhrn historických transakcí předán do služby Microsoft Azure Machine Learning hostované na platformě Azure. Vzhledem k tomu, že tato služba není sdílena mezi uživateli, lze ji snadno upravit pro splnění průmyslově specifických požadavků. Pomocí aplikace Finance and Operations můžete zobrazit a upravovat prognózy a zobrazit klíčové indikátory výkonnosti popisující přesnost prognózy.

## <a name="key-features-of-demand-forecasting"></a>Klíčové funkce prognózy poptávky
Zde jsou uvedeny některé z hlavních charakteristik vytváření prognózy poptávky:

-   Generování statistické základní prognózy, která je založena na historických datech.
-   Používání dynamické sady dimenzí prognózy.
-   Vizualizace trendů poptávky, intervalů spolehlivosti a úpravy prognózy.
-   Autorizování úprav prognóza pro použití v procesech plánování.
-   Odebrání odlehlých hodnot.
-   Vytvoření měrného systému přesnosti prognózy.

## <a name="major-themes-in-demand-forecasting"></a>Hlavní motivy v prognóze poptávky
Do prognózy poptávky jsou implementovány tři hlavní motivy:

-   **Modulární struktura** – prognóza poptávky je modulární a lze ji snadno konfigurovat. Funkci lze zapnout nebo vypnout změnou konfiguračního klíče v nabídce **Obchod** &gt; **Prognóza zásob** &gt; **Prognóza poptávky**.
-   **Opětovné použití zásobníku Microsoft** – Společnost Microsoft spustila platformu strojového učení v únoru 2015. Strojové učení, které je nyní součástí Microsoft Cortana Analytics Suite, umožňuje rychle a snadno vytvářet experimenty prediktivní analýzy, jako jsou pokusy o odhad poptávky, pomocí programovacích jazyků algoritmů R nebo Python a jednoduché rozhraní přetažení.
    -   Můžete si stáhnout experimenty s prognózou poptávky aplikace Finance and Operations, změnit je tak, aby odpovídaly vašim obchodním požadavkům, publikovat je jako webové služby pro platformu Azure, a použít je pro generování prognóz poptávky. Pokud jste si zakoupili předplatné aplikace Finance and Operations pro plánovač výroby na úrovni podnikového uživatele, jsou experimenty dostupné ke stažení.
    -   Můžete stáhnout všechny aktuálně dostupné pokusy předpovědi poptávky z adresy [Galerie analýzy Cortana](https://gallery.cortanaanalytics.com/). Zatímco experimenty s prognózou poptávky aplikace Finance and Operations jsou do aplikace Finance and Operations integrovány automaticky, experimenty stažené z [Galerie analýzy Cortana](https://gallery.cortanaanalytics.com/) musí zákazníci a partneři integrovat ručně. Používání experimentů z [Galerie analýzy Cortana](https://gallery.cortanaanalytics.com/) proto není tak přímočaré jako u experimentů s prognózou poptávky aplikace Finance and Operations. Kód experimentů je třeba upravit tak, aby používaly rozhraní API aplikace Finance and Operations.
    -   Můžete vytvořit vlastní pokusy v aplikaci Microsoft Azure Machine Learning Studio, publikovat je jako služby Azure a použít je pro generování prognóz poptávky.
    -   Pokud nevyžadujete vysoký výkon, nebo nechcete-li zpracovat velké množství dat, můžete používat bezplatnou verzi služby Machine Learning. Doporučujeme vždy začínat od této verze, zejména během implementace a testování. Chcete-li dosáhnout vyššího výkonu a dalšího úložiště, můžete začít používat standardní verzi Machine Learning. Tato verze vyžaduje odběr služby Azure a zahrnuje dodatečné náklady. Podrobnosti strojovém učení naleznete v tématu <http://aka.ms/machine-learning-price-info>.
-   **Snížení prognózy v libovolném z oddělovacích bodů** – prognóza poptávky v aplikaci Finance and Operations je založena na této funkci, která umožňuje prognózy závislé i nezávislé poptávky v libovolném oddělovacím bodě.

## <a name="basic-flow-in-demand-forecasting"></a>Základní tok v prognóze poptávky
Následující diagram znázorňuje základní průběh v prognóze poptávky. 

[![diagram zavedení prognózy poptávky](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

V aplikaci Finance and Operations se začne generovat prognóza poptávky. Historická transakční data z transakční databáze aplikace Finance and Operations se shromáždí a vyplní tabulku fázování. Tato pracovní tabulka je později předána do služby Machine Learning. Provedením minimálního přizpůsobení můžete připojit různé zdroje dat do pracovní tabulky. Zdroje dat mohou zahrnovat soubory aplikace Microsoft Excel, textové soubory s oddělovači (CSV) soubory a data z aplikace Microsoft Dynamics AX 2009 a Microsoft Dynamics AX 2012. Proto lze generovat prognózy poptávky, které zvažují historická data, která se šíří mezi více systémy. Avšak hlavní data, jako jsou například názvy položek a měrné jednotky, musí být stejná napříč různými zdroji dat.

Při použití experimentů s prognózou poptávky se strojovým učením v aplikaci Finance and Operations dojde k hledání nejlepší volby mezi pěti metodami prognózy v časových řadách s cílem vypočítat základní prognózu. Parametry pro tyto metody prognózy se spravují v aplikaci Finance and Operations. 

Prognózy, historická data a veškeré změny provedené v prognózách poptávky v předchozích iteracích se v aplikaci Finance and Operations následně zpřístupní. 

Aplikaci Finance and Operations můžete použít k zobrazení a úpravě základních prognóz. Před použitím prognóz pro plánování musí být autorizovány ruční úpravy.

## <a name="limitations"></a>Omezení
Prognóza poptávky v aplikaci Finance and Operations je nástroj, který usnadňuje zákazníkům ve výrobním průmyslu vytváření prognostických procesů. Nabízí základní funkce řešení prognózy poptávky a je navržen tak, že lze snadno rozšířit. Prognóza poptávky nemusí být nejlepší pro zákazníky v oborech jako je maloobchod, velkoobchod, skladování, přeprava nebo jiné odborné služby.

<a name="additional-resources"></a>Další zdroje
--------

[Nastavení prognózy poptávky](demand-forecasting-setup.md)

[Generování statistické základní prognózy](generate-statistical-baseline-forecast.md)

[Ruční úpravy základní prognózy](manual-adjustments-baseline-forecast.md)

[Autorizování upravené prognózy](authorize-adjusted-forecast.md)

[Měření přesnosti prognózy](monitor-forecast-accuracy.md)

[Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky](remove-historical-outliers-calculating-demand-forecast.md)

[Rozšíření funkce prognózy poptávky](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)





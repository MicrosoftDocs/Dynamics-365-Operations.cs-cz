---
title: "Přehled prognózy poptávky"
description: "Pomocí prognózy poptávky lze odhadnout nezávislé poptávky z prodejních objednávek a závislých požadavků v libovolném oddělovacím bodě objednávky odběratele. Rozšířená pravidla redukce prognózy poptávky nabízí ideální řešení pro hromadné přizpůsobení."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 86f2f556d1b2d8711e7419b4e85904e297097380
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="demand-forecasting-overview"></a>Přehled prognózy poptávky

[!include[banner](../includes/banner.md)]


Pomocí prognózy poptávky lze odhadnout nezávislé poptávky z prodejních objednávek a závislých požadavků v libovolném oddělovacím bodě objednávky odběratele. Rozšířená pravidla redukce prognózy poptávky nabízí ideální řešení pro hromadné přizpůsobení.

Pro generování základní prognózy je souhrn historických transakcí předán do služby Microsoft Azure Machine Learning hostované na platformě Azure. Vzhledem k tomu, že tato služba není sdílena mezi uživateli, lze ji snadno upravit pro splnění průmyslově specifických požadavků. Pomocí aplikace Dynamics 365 for Operations můžete zobrazit prognózu, upravit prognózu a zobrazit klíčové indikátory výkonnosti popisující přesnost prognózy.

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
    -   Můžete si stáhnout pokusy prognózy poptávky Dynamics 365 for Operations, změnit je tak, aby odpovídaly vašim obchodním požadavkům, publikovat je jako webové služby pro platformu Azure, a použít je pro generování prognóz poptávky. Pokusy jsou k dispozici ke stažení v případě zakoupení předplatného aplikace Dynamics 365 for Operations pro plánovač výroby na úrovni podnikového uživatele.
    -   Můžete stáhnout všechny aktuálně dostupné pokusy předpovědi poptávky z adresy [Galerie analýzy Cortana](https://gallery.cortanaanalytics.com/). Vzhledem k tomu, že pokusy poptávky prognózy v aplikaci Dynamics 365 for Operations jsou automaticky integrované do aplikace Dynamics 365 for Operations, zákazníci a partneři musí zpracovat integraci pokusů, které stáhnou z [Galerie analýzy Cortana](https://gallery.cortanaanalytics.com/). Proto pokusy z [Galerie analýzy Cortana](https://gallery.cortanaanalytics.com/) nejsou tak přímočaré, jako pokusy prognózy poptávky aplikace Dynamics 365 for Operations . Je třeba upravit kód pokusů tak, aby používaly rozhraní API aplikace Dynamics 365 for Operations.
    -   Můžete vytvořit vlastní pokusy v aplikaci Microsoft Azure Machine Learning Studio, publikovat je jako služby Azure a použít je pro generování prognóz poptávky.
    -   Pokud nevyžadujete vysoký výkon, nebo nechcete-li zpracovat velké množství dat, můžete používat bezplatnou verzi služby Machine Learning. Doporučujeme vždy začínat od této verze, zejména během implementace a testování. Chcete-li dosáhnout vyššího výkonu a dalšího úložiště, můžete začít používat standardní verzi Machine Learning. Tato verze vyžaduje odběr služby Azure a zahrnuje dodatečné náklady. Podrobnosti o cenách produktu Machine Learning naleznete v tématu <http://aka.ms/machine-learning-price-info>.
-   **Snížení prognózy v libovolném z oddělovacích bodů** – prognóza poptávky v aplikaci Dynamics 365 for Operations staví na této funkci, která umožňuje vytvářet závislé i nezávislé prognózy poptávky v libovolném oddělovacím bodě.

## <a name="basic-flow-in-demand-forecasting"></a>Základní tok v prognóze poptávky
Následující diagram znázorňuje základní průběh v prognóze poptávky. 

[![diagram zavedení prognózy poptávky](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Generování prognózy poptávky začíná v aplikaci Dynamics 365 for Operations. Historická transakční data z transakční databáze aplikace Dynamics 365 for Operations jsou shromažďována a vyplněna v tabulce fázování. Tato pracovní tabulka je později předána do služby Machine Learning. Provedením minimálního přizpůsobení můžete připojit různé zdroje dat do pracovní tabulky. Zdroje dat mohou zahrnovat soubory aplikace Microsoft Excel, textové soubory s oddělovači (CSV) soubory a data z aplikace Microsoft Dynamics AX 2009 a Microsoft Dynamics AX 2012. Proto lze generovat prognózy poptávky, které zvažují historická data, která se šíří mezi více systémy. Avšak hlavní data, jako jsou například názvy položek a měrné jednotky, musí být stejná napříč různými zdroji dat.

Při použití pokusů prognózy poptávky Machine Learning v aplikaci Dynamics 365 for Operations dojde k vyhledávání nejlepší volby v pěti metodách prognózy v časových řadách s cílem použít výpočet základní prognózy. Parametry pro tyto metody prognózy se spravují v aplikaci Dynamics 365 for Operations. 

Prognózy, historická data a veškeré změny provedené v prognózách poptávky v předchozích iteracích budou k dispozici v aplikaci Dynamics 365 for Operations. 

Aplikaci Dynamics 365 for Operations můžete použít pro zobrazení a úpravu základních prognóz. Před použitím prognóz pro plánování musí být autorizovány ruční úpravy.

## <a name="limitations"></a>Omezení
Vytváření prognózy poptávky v aplikaci Dynamics 365 for Operations je nástroj, který usnadňuje odběratelům ve výrobním průmyslu vytvořit procesy prognózy. Nabízí základní funkce řešení prognózy poptávky a je navržen tak, že lze snadno rozšířit. Prognóza poptávky nemusí být nejlepší pro zákazníky v oborech jako je maloobchod, velkoobchod, skladování, přeprava nebo jiné odborné služby.

<a name="see-also"></a>Viz také
--------

[Nastavení prognózy poptávky](demand-forecasting-setup.md)

[Generování statistické základní prognózy](generate-statistical-baseline-forecast.md)

[Ruční úpravy základní prognózy](manual-adjustments-baseline-forecast.md)

[Autorizování upravené prognózy](authorize-adjusted-forecast.md)

[Měření přesnosti prognózy](monitor-forecast-accuracy.md)

[Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky](remove-historical-outliers-calculating-demand-forecast.md)





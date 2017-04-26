---
title: "Přehled prognózy poptávky"
description: "Pomocí prognózy poptávky lze odhadnout nezávislé poptávky z prodejních objednávek a závislých požadavků v libovolném oddělovacím bodě objednávky odběratele. Vylepšené poptávky prognózy snížení pravidla poskytují ideální řešení pro hromadné úpravy."
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Přehled prognózy poptávky

[!include[banner](../includes/banner.md)]


Pomocí prognózy poptávky lze odhadnout nezávislé poptávky z prodejních objednávek a závislých požadavků v libovolném oddělovacím bodě objednávky odběratele. Vylepšené poptávky prognózy snížení pravidla poskytují ideální řešení pro hromadné úpravy.

Pro generování základní prognózy je souhrn historických transakcí předán do služby Microsoft Azure Machine Learning hostované na platformě Azure. Vzhledem k tomu, že tato služba není sdílena mezi uživateli, lze ji snadno upravit pro splnění průmyslově specifických požadavků. 365 Dynamics pro operace lze vizualizovat prognózy, nastavení prognózy a zobrazit klíčové ukazatele výkonu (KPI) o správnosti prognózy.

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

-   **Modulární struktura** – prognóza poptávky je modulární a lze ji snadno konfigurovat. Zapnutí a vypnutí funkce můžete upravit změnou konfigurační klíč na **obchodní**&gt;**prognóz zásob**&gt;**prognózy poptávky**.
-   **Opětovné použití zásobníku Microsoft** – Microsoft spustila platform strojovém učení v únoru 2015. Strojovém učení, které je nyní součástí Microsoft Cortana Analytics Suite umožňuje rychle a snadno vytvářet prediktivní analýzy experimenty, jako jsou pokusy o odhad poptávky, pomocí algoritmů R nebo Python programovacích jazyků a jednoduché rozhraní a přetažení.
    -   Můžete stáhnout Dynamics 365 operace poptávky prognózy experimenty, změnit jim splnit obchodní požadavky, je publikovat jako webové služby na Azure a jejich použití k vytvoření prognózy poptávky. Pokusy jsou k dispozici ke stažení, pokud jste zakoupili Dynamics 365 předplatné operací pro výrobní plánovač jako uživatel na úrovni organizace.
    -   Můžete stáhnout všechny aktuálně dostupné pokusy předpovědi poptávky z adresy [Galerie analýzy Cortana](https://gallery.cortanaanalytics.com/). Že jsou 365 Dynamics experimenty prognózy poptávky operace automaticky integruje s 365 Dynamics pro operace, Zákazníci a partneři musí zpracovat integrace pokusy, které mohou stáhnout z [Cortana Analytics Galerie](https://gallery.cortanaanalytics.com/). Z důvodu pokusů [Cortana Analytics Galerie](https://gallery.cortanaanalytics.com/) nejsou stejně jednoduché jako Dynamics 365 pro experimenty prognózy poptávky operace použít. Je třeba upravit kód pokusy tak, že používají Dynamics 365 pro operace aplikační programovací rozhraní (API).
    -   Můžete vytvořit vlastní pokusy v aplikaci Microsoft Azure Machine Learning Studio, publikovat je jako služby Azure a použít je pro generování prognóz poptávky.
    -   Pokud nevyžadujete vysoký výkon, nebo nechcete-li zpracovat velké množství dat, můžete používat bezplatnou verzi služby Machine Learning. Doporučujeme vždy začínat od této verze, zejména během implementace a testování. Chcete-li dosáhnout vyššího výkonu a dalšího úložiště, můžete začít používat standardní verzi Machine Learning. Tato verze vyžaduje odběr služby Azure a zahrnuje dodatečné náklady. Podrobnosti o cenách produktu Machine Learning naleznete v tématu <http://aka.ms/machine-learning-price-info>.
-   **Prognózy snížení oddělovací kdykoli** – poptávky prognózy Dynamics 365 pro sestavení operací na tuto funkci, která umožňuje prognózy poptávky závislé a nezávislé oddělovací kdykoli.

## <a name="basic-flow-in-demand-forecasting"></a>Základní tok v prognóze poptávky
Následující diagram znázorňuje základní průběh v prognóze poptávky. 

[![diagram zavedení prognózy poptávky](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Spuštění generování v 365 Dynamics pro operace prognózy poptávky. Historické transakční data z 365 Dynamics pro transakční databázové operace jsou shromažďovány a naplní pracovní tabulky. Tato pracovní tabulka je podáván později do služby Machine Learning. Provedením úprav minimální možné připojit různé zdroje dat do pracovní tabulky. Zdroje dat můžete zahrnout soubory aplikace Microsoft Excel, textový soubor s oddělovači (CSV) soubory a data z aplikace Microsoft Dynamics AX 2009 a Microsoft Dynamics AX 2012. Proto lze generovat prognózy poptávky, které považuje za historických dat, které se šíří mezi více systémy. Avšak hlavní data, jako jsou například názvy položek a měrné jednotky, musí být stejná napříč různými zdroji dat.

Používáte-li Dynamics 365 experimenty Machine Learning prognózy poptávky operací, oblast pro nejlepší shoda mezi pěti časové řady předpovědních metod výpočtu směrného plánu prognózy. Parametry pro tyto předpovědních metod jsou spravovány v 365 Dynamics pro operace. 

Odhady, historická data a všechny změny provedené v předchozí iterací prognózy poptávky budou k dispozici v 365 Dynamics pro operace. 

365 Dynamics pro operace slouží k vizualizaci a upravit podle směrného plánu prognózy. Před použitím prognóz pro plánování musí být autorizovány ruční úpravy.

## <a name="limitations"></a>Omezení
Prognóza poptávky v 365 Dynamics pro operace je nástroj, který pomáhá zákazníkům v odvětví výroby vytvořit prognózy procesy. Nabízí základní funkce řešení prognózy poptávky a je navržen tak, že lze snadno rozšířit. Požadovat předpovědi nemusí být nejlepší vhodný pro zákazníky v oborech jako je maloobchod, velkoobchodu, skladování, přepravy nebo jiné odborné služby.

<a name="see-also"></a>Viz také
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)





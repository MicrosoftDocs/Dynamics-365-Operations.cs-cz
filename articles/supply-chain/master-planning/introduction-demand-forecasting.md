---
title: Přehled prognózy poptávky
description: Pomocí prognózy poptávky lze odhadnout nezávislé poptávky z prodejních objednávek a závislých požadavků v libovolném oddělovacím bodě objednávky odběratele. Rozšířená pravidla redukce prognózy poptávky nabízí ideální řešení pro hromadné přizpůsobení.
author: roxanadiaconu
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27aa2b7a3d595fadfc1af969e45975e95322812f
ms.sourcegitcommit: 3895279cc5c1cf4826143d2ccb95ccceccb0a3c2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2021
ms.locfileid: "5081360"
---
# <a name="demand-forecasting-overview"></a>Přehled prognózy poptávky

[!include [banner](../includes/banner.md)]

Pomocí prognózy poptávky lze odhadnout nezávislé poptávky z prodejních objednávek a závislých požadavků v libovolném oddělovacím bodě objednávky odběratele. Rozšířená pravidla redukce prognózy poptávky nabízí ideální řešení pro hromadné přizpůsobení.

Pro generování základní prognózy je souhrn historických transakcí předán strojovému učení Microsoft Azure hostovanému na platformě Azure. Vzhledem k tomu, že tato služba není sdílena mezi uživateli, lze ji snadno upravit pro splnění průmyslově specifických požadavků. Pomocí aplikace Supply Chain Management můžete zobrazit a upravovat prognózy a zobrazit klíčové indikátory výkonnosti popisující přesnost prognózy.

> [!NOTE]
> Pro generování předpovědi pomocí strojového učení je vyžadováno Microsoft Azure Machine Learning Studio (klasické). Od ledna 2021 je k dispozici pro západní Japonsko, jižní a střední USA, jihovýchodní Asii, středozápad USA a západní Evropu. Aktualizované informace o aktuální dostupnosti najdete v části [Produkty Azure podle oblasti.](https://azure.microsoft.com/global-infrastructure/services/?regions=all&products=machine-learning-studio)

## <a name="key-features-of-demand-forecasting"></a>Klíčové funkce prognózy poptávky

Zde jsou uvedeny některé z hlavních charakteristik vytváření prognózy poptávky:

- Generování statistické základní prognózy, která je založena na historických datech.
- Používání dynamické sady dimenzí prognózy.
- Vizualizace trendů poptávky, intervalů spolehlivosti a úpravy prognózy.
- Autorizování úprav prognóza pro použití v procesech plánování.
- Odebrání odlehlých hodnot.
- Vytvoření měrného systému přesnosti prognózy.

## <a name="major-themes-in-demand-forecasting"></a>Hlavní motivy v prognóze poptávky

Do prognózy poptávky jsou implementovány tři hlavní motivy:

- **Modulární struktura** – prognóza poptávky je modulární a lze ji snadno konfigurovat. Funkci lze zapnout nebo vypnout změnou konfiguračního klíče v nabídce **Obchod** &gt; **Prognóza zásob** &gt; **Prognóza poptávky**.
- **Opakované použití Microsoft stack** - Strojové učení, které je nyní součástí Microsoft Cortana Analytics Suite, umožňuje rychle a snadno vytvářet experimenty prediktivní analýzy, jako jsou pokusy o odhad poptávky, pomocí programovacích jazyků algoritmů R nebo Python a jednoduché rozhraní přetažení.
  - Pokusy prognózy poptávky můžete stáhnout, změnit je tak, aby odpovídaly obchodním požadavkům, publikovat je jako webové služby pro platformu Azure, a použít je pro generování prognóz poptávky. Pokud jste si zakoupili předplatné aplikace Supply Chain Management pro plánovač výroby na úrovni podnikového uživatele, jsou experimenty dostupné ke stažení.
  - Můžete stáhnout všechny aktuálně dostupné pokusy předpovědi poptávky z adresy [Galerie analýzy Cortana](https://gallery.cortanaanalytics.com/). Zatímco experimenty s prognózou poptávky jsou do aplikace Supply Chain Management integrovány automaticky, experimenty stažené z [Galerie analýzy Cortana](https://gallery.cortanaanalytics.com/) musí zákazníci a partneři integrovat ručně. Proto nejsou pokusy z [Galerie analýzy Cortana](https://gallery.cortanaanalytics.com/) nejsou tak přímočaré jako pokusy prognózy poptávky aplikace Finance and Operations. Je třeba upravit kód pokusů tak, aby používaly programovací rozhraní (API) aplikace Finance and Operations.
  - Můžete vytvořit vlastní pokusy v aplikaci studia strojového učení Microsoft Azure (klasické), publikovat je jako služby Azure a použít je pro generování prognóz poptávky.
  - Pokud nevyžadujete vysoký výkon, nebo nechcete-li zpracovat velké množství dat, můžete používat bezplatnou verzi služby Machine Learning. Doporučujeme vždy začínat od této verze, zejména během implementace a testování. Chcete-li dosáhnout vyššího výkonu a dalšího úložiště, můžete začít používat standardní verzi Machine Learning. Tato verze vyžaduje odběr služby Azure a zahrnuje dodatečné náklady. Podrobnosti o cenách produktu Machine Learning naleznete v tématu [ceny Machine Learning Studio](https://aka.ms/machine-learning-price-info).
- **Snížení prognózy v libovolném z oddělovacích bodů** – prognóza poptávky staví na této funkci, která umožňuje vytvářet závislé i nezávislé prognózy poptávky v libovolném oddělovacím bodě.

## <a name="basic-flow-in-demand-forecasting"></a>Základní tok v prognóze poptávky

Následující diagram znázorňuje základní průběh v prognóze poptávky.

[![diagram zavedení prognózy poptávky](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Generování prognózy poptávky začíná v Supply Chain Management. Historická transakční data z transakční databáze aplikace Supply Chain Management se shromáždí a vyplní tabulku fázování. Tato pracovní tabulka je později předána do služby Machine Learning. Provedením minimálního přizpůsobení můžete připojit různé zdroje dat do pracovní tabulky. Zdroje dat mohou zahrnovat soubory Microsoft Excel, soubory hodnot oddělených čárkou (CSV) a data z Microsoft Dynamics AX 2009 a Microsoft Dynamics AX 2012. Proto lze generovat prognózy poptávky, které zvažují historická data, která se šíří mezi více systémy. Avšak hlavní data, jako jsou například názvy položek a měrné jednotky, musí být stejná napříč různými zdroji dat.

Při použití pokusů prognózy poptávky Machine Learning dojde k vyhledávání nejlepší volby v pěti metodách prognózy v časových řadách s cílem použít výpočet základní prognózy. Parametry pro tyto metody prognózy se spravují v aplikaci Supply Chain Management.

Prognózy, historická data a veškeré změny provedené v prognózách poptávky v předchozích iteracích se v aplikaci Supply Chain Management následně zpřístupní.

Aplikaci Supply Chain Management můžete použít k zobrazení a úpravě základních prognóz. Před použitím prognóz pro plánování musí být autorizovány ruční úpravy.

## <a name="limitations"></a>Omezení

Vytváření prognózy poptávky je nástroj, který usnadňuje odběratelům ve výrobním průmyslu vytvořit procesy prognózy. Nabízí základní funkce řešení prognózy poptávky a je navržen tak, že lze snadno rozšířit. Prognóza poptávky nemusí být nejlepší pro zákazníky v oborech jako je obchod, velkoobchod, skladování, přeprava nebo jiné odborné služby.

### <a name="demand-forecast-variant-conversion-limitation"></a>Omezení konverze varianty prognózy poptávky

Měrná jednotka (UOM) na konverzi varianty není plně podporována při generování prognózy poptávky, pokud je UOM inventáře odlišná od UOM prognózy poptávky.

Generování prognózy (**Zásoby UOM > Předpověď poptávky UOM**) používá konverzi UOM produktu. Při načítání historických dat pro generování prognózy poptávky bude vždy použita konverze UOM na úrovni produktu při převodu z inventáře UOM na UOM prognózy poptávky, i když jsou na úrovni varianty definovány konverze.

První část schvalování prognózy (**Prognóza poptávky UOM > UOM inventáře**) používá konverzi UOM produktu. Druhá část schvalování prognózy (**UOM inventáře > UOM prodeje**) používá variantu konverze UOM. Když je vygenerovaná prognóza poptávky autorizovaná, převede se na UOM inventury z UOM prognózy poptávky pomocí konverze UOM na úrovni produktu. Současně bude převod mezi jednotkou inventáře a prodejním UOM respektovat převody definované na úrovni varianty.

Upozorňujeme, že UOM prognózy poptávky nemusí mít žádný konkrétní význam. Lze ji definovat jako „Jednotka prognózy poptávky“. U každého z produktů můžete pomocí převodu zásob UOM definovat převod 1:1.

## <a name="additional-resources"></a>Další prostředky

[Nastavení prognózy poptávky](demand-forecasting-setup.md)

[Generování statistické základní prognózy](generate-statistical-baseline-forecast.md)

[Ruční úpravy základní prognózy](manual-adjustments-baseline-forecast.md)

[Autorizace upravené prognózy](authorize-adjusted-forecast.md)

[Monitorování přesnosti prognózy](monitor-forecast-accuracy.md)

[Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky](remove-historical-outliers-calculating-demand-forecast.md)

[Rozšíření funkce prognózy poptávky](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)

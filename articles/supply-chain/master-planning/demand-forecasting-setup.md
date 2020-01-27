---
title: Nastavení prognózy poptávky
description: Toto téma popisuje úlohy nastavení, které je třeba provést, aby bylo možné používat prognózy poptávky.
author: roxanadiaconu
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f56157be8cc61486801fc4c01bb191432dd9a541
ms.sourcegitcommit: 34395464ec80cea800b953eae49af579d436fc1b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935484"
---
# <a name="demand-forecasting-setup"></a>Nastavení prognózy poptávky

[!include [banner](../includes/banner.md)]

Toto téma popisuje úlohy nastavení, které je třeba provést, aby bylo možné používat prognózy poptávky.  

Nastavení zahrnuje nastavení následujících dat a parametrů.

## <a name="item-allocation-key"></a>Alokační klíč položky
Prognóza poptávky se vypočítá pro položku a její dimenze pouze v případě, že položka je součástí alokačního klíče položky. Toto pravidlo je vynuceno pro seskupení velkého počtu položek tak, abyste prognózy poptávky mohli vytvářet rychleji. Při generování prognóz poptávky je procento alokačního klíče položky ignorováno. Prognózy se vytváří pouze podle historických dat. 

Položka a její dimenze musí být součástí pouze jednoho alokačního klíče položky, pokud se alokační klíč položky používá při vytváření prognózy. 

Chcete-li přidat alokační klíč položky do skladové jednotky zásob, přejděte na **Hlavní plánování** &gt; **Nastavení** &gt; **Prognóza poptávky** &gt; **Alokační klíče položky**. Pomocí stránky **Přiřadit položky** přiřaďte položku k alokačnímu klíči položky.

## <a name="intercompany-planning-groups"></a>Skupiny mezipodnikového plánování
Prognóza poptávky generuje prognózy mezi více společnostmi. V aplikaci Dynamics 365 Supply Chain Management jsou společnosti, které jsou plánovány společně, seskupeny do jedné skupiny pro mezipodnikové plánování. Pokud chcete určit podle společnosti, které alokační klíče položek by měly být zahrnuty pro tvorbu prognóz poptávky, přiřaďte alokační klíč položky členovi skupiny mezipodnikového plánování v nabídce **Hlavní plánování** &gt; **Nastavení** &gt; **Skupiny mezipodnikového plánování**. 

Ve výchozím nastavení pokud nejsou přiřazeny žádné alokační klíče položek k členům skupiny mezipodnikového plánování, prognóza poptávky bude vypočtena pro všechny položky, které jsou přiřazeny ke všem alokačním klíčům položek ze všech společností. Další možnosti pro filtrování společností a alokačních klíčů položek jsou k dispozici na stránce **Vygenerování statistické základní prognózy**. 

Prohlédněte si počet položek, které jsou předvídány. Zbytečné položek mohou způsobit zvýšení nákladů při použití služby strojového učení Microsoft Azure.

## <a name="demand-forecasting-parameters"></a>Parametry tvorby prognóz poptávky
K nastavení parametrů prognózy poptávky přejděte na **Hlavní plánování** &gt; **Nastavení** &gt; **Parametry tvorby prognóz poptávky**. Vzhledem k tomu, že prognózy poptávky jsou spuštěny mezi více společnostmi, toto nastavení je globální. Jinak řečeno nastavení platí pro všechny společnosti. 

Prognóza poptávky generuje prognózy ve větším množství. Je tedy nutné v poli **Jednotka prognózy poptávky** vyjádřit měrnou jednotku množství. Měrná jednotka musí být jedinečná pro zajištění toho, že agregace a procentuální rozdělení bude dávat smysl. Další informace o agregaci a procentuálním rozdělení naleznete v tématu [Provedení ručních úprav u základní prognózy](manual-adjustments-baseline-forecast.md). Pro každou měrnou jednotku používanou pro skladové jednotky, které jsou zahrnuty do prognózy poptávky, se ujistěte, že existuje pravidlo převodu pro měrnou jednotku a měrnou jednotku obecné prognózy. Po spuštění generování předpovědi se zaznamená seznam položek, které nemají převod měrné jednotky, takže lze snadno nastavení opravit. 

Prognóza poptávky slouží k provedení prognózy u závislé i nezávislé poptávky. Například pouze pokud označíte pole **Prodejní objednávka** a pokud všechny položky, které jsou považovány při tvorbě prognózy poptávky jsou položky, které jsou prodány, systém vypočítá nezávislou poptávku. Kritické dílčí komponenty však lze přidat k alokačním klíčům položek a zahrnout do prognózy poptávky. V takovém případě pokud označíte pole **Řádek výroby**, vypočítá se závislá prognóza. 

Existují dva způsoby vytvoření základní prognózy. Můžete použít modely prognózy při použití historických dat, nebo můžete pouze zkopírovat historická data do prognózy. Pole **Strategie generování prognózy** umožňuje vybrat mezi těmito dvěma metodami. Chcete-li použít modely prognózy, vyberte **Azure Machine Learning**. 

Klepnutím na tlačítko **Dimenze prognózy** v levém podokně stránky **Parametry vytváření prognózy poptávky** můžete také vybrat sadu dimenzí prognózy, která má být použita při generování prognózy poptávky. Dimenze prognózy označují úroveň podrobností, pro které je prognóza definována. Společnost, pracoviště a alokační klíč položky jsou povinné dimenze prognózy, ale lze rovněž vygenerovat prognózy pro sklad, stav zásob, skupinu odběratelů, účet odběratele, zemi nebo oblast, stát a položky společně se všemi úrovněmi dimenze položky. 

Kdykoli je možné přidat dimenze prognózy na seznam dimenzí, které se používají pro tvorbu prognózy poptávky. Můžete také dimenze prognózy ze seznamu odebrat. Ruční úpravy jsou však ztraceny, pokud přidáte nebo odeberete dimenze prognózy. 

Ne všechny položky se chovají stejným způsobem z perspektivy prognózy poptávky. Podobné položky mohou být seskupeny do jednoho alokačního klíče položky a pro každý alokační klíč položky lze nastavit parametry, jako například typy transakcí a nastavení metody prognózy. Klepněte na tlačítko **Alokační klíče položek** v levém podokně stránky **Parametry vytváření prognózy poptávky**. 

Pokud chcete generovat prognózu, aplikace Supply Chain Management používá webovou službu Machine Learning. Pro připojení ke službě je třeba zadat následující informace pro přihlášení do studia strojového učení Microsoft Azure (klasický):

-   Klíč rozhraní API webové služby
-   Koncový bod URL webové služby
-   Název účtu úložiště Azure
-   Klíč účtu úložiště Azure

> [!NOTE]
> Název účtu úložiště Azure a klíč jsou nutné pouze při použití vlastního účtu pro úložiště. Při nasazování místní verze musíte mít vlastní účet úložiště ve službě Azure, aby služba Machine Learning měla přístup k historickým datům. 

Pokud chcete vytvořit předpovědi poptávky, můžete nasadit vlastní službu pomocí experimentů s prognózou poptávky v rámci Machine Learning Studio nebo aplikace Supply Chain Management. Pokyny pro nasazení experimentů s prognózou poptávky v podobě webové služby jsou k dispozici v aplikaci Supply Chain Management. Na stránce **Parametry vytváření prognózy poptávky** klepněte na kartu **Azure Machine Learning**.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Nastavení pro službu Machine Learning pro vytváření prognózy poptávky.
Chcete-li zobrazit parametry, které lze konfigurovat pro službu vytváření prognózy poptávky, přejděte na **Hlavní plánování** &gt; **Nastavení** &gt; **Prognóza poptávky** &gt; **Parametry algoritmu prognózy**. Stránka **Parametry algoritmu prognózy** popisuje výchozí hodnoty parametrů. Tyto parametry lze přepsat na stránce **Parametry vytváření prognózy poptávky**. Na kartě **Hlavní** můžete parametry přepsat globálně, nebo použít kartu **Alokační klíče položek** a přepsat tak parametry pro každý alokační klíč položky. Parametry, které budou přepsány pro alokační klíč položky, ovlivní pouze prognózu položek, které jsou přidruženy k danému alokačnímu klíči položky.

### <a name="forecast-algorithm-parameters"></a>Parametry algoritmu prognózy

Na kartě **Alokační klíče** lze nastavit **Parametry algoritmu prognózy** pro každý alokační klíč položky. K dispozici jsou tyto možnosti.
- **Procento úrovně jistoty**: Interval jistoty obsahuje určitý úsek hodnot, které fungují jako vhodné odhady pro prognózu poptávky. 95% úroveň jistoty například označuje existenci 5% riziko, že budoucí poptávka se bude nacházet mimo rozsah intervalu jistoty.
- **Vynutit sezónnost**: Určuje, zda vynutit, aby model použil určitý typ sezónnosti. Platí pouze pro ARIMA a ETS. Možnosti: AUTO (výchozí), žáDNá, DOPLŇKOVá, MULTIPLIKATIVNí.
- **Model prognózy**: Možnosti: ARIMA, ETS, STL, ETS + ARIMA, ETS + STL, VšE. Chcete-li vybrat nejlépe odpovídající model, použijte možnost **VŠE**.
- **Maximální předpokládaná hodnota**: Určuje maximální hodnotu, která má být použita pro prognózy. Formát: + 1E [n] nebo číselná konstanta.
- **Minimální předpokládaná hodnota**: Určuje minimální hodnotu, která má být použita pro prognózy. Formát: -1E [n] nebo číselná konstanta.
- **Chybějící nahrazení hodnoty**: Určuje, jak jsou vyplněny mezery v historických datech. Možnosti: číselná hodnota, STŘEDNÍ, PŘEDCHOZÍ, INTERPOLOVANÁ LINEÁRNÍ, INTERPOLOVANÁ POLYNOMIÁLNÍ.
- **Chybí rozsah nahrazení hodnoty**: Určuje, zda se nahrazení hodnoty vztahuje pouze na rozsah dat každého jednotlivého atributu rozlišení nebo na celou sadu dat. Možnosti: GRANULARITY_ATTRIBUTE (výchozí), GLOBAL.
- **Nápověda k sezónnosti**: pro sezónní data uveďte nápovědu pro model prognózy, která zlepší přesnost prognózy. Formát: celé číslo, které představuje počet intervalů pro opakování vzoru poptávky. Zadejte například "6" pro data, která se opakují jednou za 6 měsíců.
- **Procento velikosti testovací sady**: Procentní míra historických dat, která se má použít jako testovací sada pro výpočet přesnosti prognózy. 

<a name="additional-resources"></a>Další zdroje
--------

[Přehled prognózy poptávky](introduction-demand-forecasting.md)

[Generování statistické základní prognózy](generate-statistical-baseline-forecast.md)

[Ruční úpravy základní prognózy](manual-adjustments-baseline-forecast.md)




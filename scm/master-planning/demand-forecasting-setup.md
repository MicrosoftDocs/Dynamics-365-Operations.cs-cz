---
title: "Nastavení prognózy poptávky"
description: "Toto téma popisuje úlohy nastavení, které je třeba provést, aby bylo možné používat prognózy poptávky."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Nastavení prognózy poptávky

[!include[banner](../includes/banner.md)]


Toto téma popisuje úlohy nastavení, které je třeba provést, aby bylo možné používat prognózy poptávky.  

Nastavení zahrnuje nastavení následujících dat a parametrů.

## <a name="item-allocation-key"></a>Alokační klíč položky
Prognóza poptávky se vypočítá pro položku a její dimenze pouze v případě, že položka je součástí alokačního klíče položky. Toto pravidlo je vynuceno do skupiny velkého počtu položek, takže lze rychle vytvořit prognózy poptávky. Procento klíče přidělení položky je ignorován při generování prognózy poptávky. Prognózy se vytváří pouze podle historických dat. 

Položka a její dimenze musí být součástí pouze jednoho alokačního klíče položky, pokud se alokační klíč položky používá při vytváření prognózy. 

Přídělový klíč položky přidat skladová jednotka (SKU), přejděte na **Master planning**&gt;**nastavení**&gt;**prognózy poptávky**&gt;**alokační klíče položek**. Pomocí stránky **Přiřadit položky** přiřaďte položku k alokačnímu klíči položky.

## <a name="intercompany-planning-groups"></a>Skupiny mezipodnikového plánování
Prognóza poptávky generuje prognózy mezi více společnostmi. Ve 365 Microsoft Dynamics pro operace jsou společnosti, které jsou plánovány společně seskupeny do jednoho mezipodnikového plánování skupiny. Určit jednotlivé společnosti, které alokační klíče položek musí vzít v úvahu pro předpověď poptávky přidružit alokační klíč položky vnitropodnikového plánování člen skupiny přechodem **Master planning**&gt;**nastavení**&gt;**vnitropodnikového plánování skupin**. 

Ve výchozím nastavení Pokud žádné přídělové klíče položky jsou přiřazeny vnitropodnikové plánování členů skupiny, prognóza poptávky vypočtena pro všechny položky, které jsou přiřazeny všechny klíče přidělení položky ze všech 365 Dynamics pro operace společnosti. Další možnosti pro filtrování společností a alokačních klíčů položek jsou k dispozici na stránce **Vygenerování statistické základní prognózy**. 

Prohlédněte si počet položek, které jsou předvídány. Zbytečné položek mohou způsobit zvýšení nákladů při použití služby Microsoft Azure Machine Learning.

## <a name="demand-forecasting-parameters"></a>Parametry tvorby prognóz poptávky
Chcete-li nastavit parametry prognózy poptávky, přejděte na **Master planning**&gt;**nastavení**&gt;**parametry prognózy poptávky**. Vzhledem k tomu, že prognózy poptávky jsou spuštěny mezi více společnostmi, toto nastavení je globální. Jinak řečeno nastavení platí pro všechny společnosti. 

Prognóza poptávky generuje prognózy ve větším množství. Je tedy nutné v poli **Jednotka prognózy poptávky** vyjádřit měrnou jednotku množství. Měrná jednotka musí být jedinečná pro zajištění toho, že agregace a procentuální rozdělení bude dávat smysl. Další informace o agregaci a procentuálním rozdělení naleznete v tématu [Provedení ručních úprav u základní prognózy](manual-adjustments-baseline-forecast.md). Pro každou měrnou jednotku používanou pro skladové jednotky, které jsou zahrnuty do prognózy poptávky, se ujistěte, že existuje pravidlo převodu pro měrnou jednotku a měrnou jednotku obecné prognózy. Po spuštění generování předpovědi se zaznamená seznam položek, které nemají převod měrné jednotky, takže lze snadno nastavení opravit. 

Prognóza poptávky slouží k provedení prognózy u závislé i nezávislé poptávky. Například pouze pokud označíte pole **Prodejní objednávka** a pokud všechny položky, které jsou považovány při tvorbě prognózy poptávky jsou položky, které jsou prodány, systém vypočítá nezávislou poptávku. Kritické dílčí komponenty však lze přidat k alokačním klíčům položek a zahrnout do prognózy poptávky. V takovém případě pokud označíte pole **Řádek výroby**, vypočítá se závislá prognóza. 

Existují dvě metody pro vytvoření směrného plánu prognózy v 365 Dynamics pro operace. Můžete použít modely prognózy při použití historických dat, nebo můžete pouze zkopírovat historická data do prognózy. Pole **Strategie generování prognózy** umožňuje vybrat mezi těmito dvěma metodami. Chcete-li použít modely prognózy, vyberte **Azure Machine Learning**. 

Klepnutím na tlačítko **Dimenze prognózy** v levém podokně stránky **Parametry vytváření prognózy poptávky** můžete také vybrat sadu dimenzí prognózy, která má být použita při generování prognózy poptávky. Dimenze prognózy označují úroveň podrobností, pro které je prognóza definována. Společnost, pracoviště a alokační klíč položky jsou povinné dimenze prognózy, ale lze rovněž vygenerovat prognózy pro sklad, stav zásob, skupinu odběratelů, účet odběratele, zemi nebo oblast, stát a položky společně se všemi úrovněmi dimenze položky. 

Kdykoli je možné přidat dimenze prognózy na seznam dimenzí, které se používají pro tvorbu prognózy poptávky. Můžete také dimenze prognózy ze seznamu odebrat. Ruční úpravy jsou však ztraceny, pokud přidáte nebo odeberete dimenze prognózy. 

Ne všechny položky se chovají stejným způsobem z perspektivy prognózy poptávky. Podobné položky mohou být seskupeny do jednoho alokačního klíče položky a pro každý alokační klíč položky lze nastavit parametry, jako například typy transakcí a nastavení metody prognózy. Klepněte na tlačítko **Alokační klíče položek** v levém podokně stránky **Parametry vytváření prognózy poptávky**. 

Generovat prognózy, 365 Dynamics pro operace používá webová služba Machine Learning. Chcete-li se připojit ke službě, je nutné zadat Dynamics 365 pro operace následující informace po přihlášení k aplikaci Microsoft Azure Machine Learning Studio:

-   Klíč rozhraní API webové služby
-   Koncový bod URL webové služby
-   Název účtu úložiště Azure
-   Klíč účtu úložiště Azure

**Poznámka:** Název účtu úložiště Azure a klíč jsou nutné pouze při použití vlastního účtu pro úložiště. Při nasazování pro místní verzi, potřebujete účet vlastního úložiště v Azure, tak, aby Služba Machine Learning přístup historická data. 

K vytvoření předpovědi poptávky, můžete nasadit vlastní služby pomocí operace poptávky prognózy experimenty Machine Learning Studio nebo Dynamics 365. Pokyny pro nasazení Dynamics 365 operace poptávky prognózy experimenty jako webové služby jsou k dispozici 365 Dynamics pro operace. Na stránce **Parametry vytváření prognózy poptávky** klepněte na kartu **Azure Machine Learning**.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Nastavení pro 365 Dynamics pro operace poptávky prognózy učení servis
Chcete-li zobrazit parametry, které lze nakonfigurovat pro Dynamics 365 pro operace poptávky prognózy služby, přejděte na **hlavního plánování**&gt;**nastavení**&gt;**prognózy poptávky**&gt;**parametry algoritmu prognózy**. **Parametry algoritmu prognózy** stránky jsou uvedeny výchozí hodnoty pro parametry. Tyto parametry lze přepsat na **parametry prognózy poptávky** stránky. Na kartě **Hlavní** můžete parametry přepsat globálně, nebo použít kartu **Alokační klíče položek** a přepsat tak parametry pro každý alokační klíč položky. Parametry, které budou přepsány pro alokační klíč položky, ovlivní pouze prognózu položek, které jsou přidruženy k danému alokačnímu klíči položky.

<a name="see-also"></a>Viz také
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)





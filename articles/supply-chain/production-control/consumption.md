---
title: Výpočet spotřeby materiálu
description: Tento článek poskytuje informace o různých volbách, které se vztahují k výpočtu spotřeby materiálu.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e4010b5abb6b5a871d098422f1489cb2db3a071
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "316181"
---
# <a name="calculate-material-consumption"></a>Výpočet spotřeby materiálu

[!include [banner](../includes/banner.md)]

Tento článek poskytuje informace o různých volbách, které se vztahují k výpočtu spotřeby materiálu. 

Následující možnosti, které se vztahují k výpočtu spotřeby materiálu, jsou k dispozici na kartě **Nastavení** a **Spotřeba kroku** na pevné záložce **Podrobnosti řádku** na stránce **Kusovník**.

## <a name="variable-and-constant-consumption"></a>Proměnná a konstantní spotřeba
V poli **Spotřeba je** můžete určit, zda se spotřeba vypočte jako konstantní množství nebo variabilní množství. Vyberte **Konstantní**, pokud jsou pevné množství nebo objem nutné pro výrobu, bez ohledu na vyráběné množství. Vyberte **Variabilní**, což je výchozí nastavení, je-li požadované množství materiálu v dokončeném zboží úměrné počtu dokončených výrobků, které jsou vyrobeny.

## <a name="calculating-consumption-from-a-formula"></a>Výpočet spotřeby podle vzorce
V poli **Vzorec** můžete nastavit různé vzorce pro výpočet spotřeby materiálu. Pokud použijete výchozí hodnotu, **Standardní**, spotřeba není vypočtena ze vzorce. Následující vzorce mohou pracovat spolu v polích **Výška**, **Šířka**, **Hloubka**, **Hustota** a **Konstantní**:

-   Výška \* Konstantní
-   Výška \* Šířka \* Konstantní
-   Výška \* Šířka \* Hloubka \* Konstantní
-   (Výška \* Šířka \* Hloubka / Hustota) \* Konstantní

## <a name="rounding-up-and-multiples"></a>Zaokrouhlení a násobky
Společně pole **Zaokrouhlení** a **Násobky** umožňují zaokrouhlování hodnoty spotřeby materiálu. Například můžete použít zaokrouhlování hodnoty podle manipulační jednotky, ve které jsou suroviny vydané pro výrobu. Existují tyto možnosti v poli **Zaokrouhlení**: **Množství**, **Měření** a **Spotřeby**.

### <a name="quantity"></a>Množství

Vyberete-li **Množství** jako mechanismus zaokrouhlování, množství musí být násobkem zadaného množství. Jsou-li například vyžadována celá čísla, vyberte **1** v poli **Násobky**. Čísla jsou pak zaokrouhlena na množství dělitelné hodnotou 1.

### <a name="measurement"></a>Měrný systém

Obvykle vyberete **Měření** jako mechanismus zaokrouhlování, pokud surovina přichází ve specifických dimenzích. Například část 2metrové kovové trubice je vyžadována pro dokončené zboží, a kovová trubice je uložena v délce 4,5 metru. V takovém případě mechanismus zaokrouhlování **Měření** lze použít k výpočtu toho, kolik kovových trubek je zapotřebí pro výrobu určitého počtu kusů dokončeného zboží. V tomto příkladu je pole **Vzorec** nastaveno na **Výška \* Konstantní**. Pole **Výška** je nastaveno na **2** pro označení délky trubky potřebné k dokončení výrobku. Pole **Více** je nastaveno na **4,5** a označuje tak, že je trubice vydaná v délkách po 4,5 metrech. Kalkulace je tato:

1.  Počet násobků, které jsou požadovány pro 10 kusů dokončeného zboží: 10 ÷ 2 = 5 kusů
2.  Celková spotřeba: 4,5 x 5 = 22,5 metru kovové trubice

Předpokládá se, že, 0,5 metru trubice je vyřazeno pro každých pět částí trubice, která je spotřebována.

### <a name="consumption"></a>Spotřeba

Obvykle vyberete**Spotřeba** jako mechanismus zaokrouhlování, když musí být suroviny vyskladněny v celém množství konkrétní manipulační jednotky produktu. Například k výrobě jednoho kusu dokončeného zboží jsou použity 2 plechovky barvy a barva je vydána v 25litrových plechovkách. V takovém případě mechanismus zaokrouhlování **Spotřeba** lze použít k zaokrouhlení spotřeby nahoru na celá čísla 25litrových plechovek. Následuje výpočet množství barvy, která je vyžadována, pokud je třeba vyrobit 180 kusů dokončeného zboží:

1.  Barva, která je nutná (bez odpadu): 180 x 2 = 360 plechovek
2.  Počet plechovek: 360 ÷ 25 = 14,4, což je zaokrouhleno 15.
3.  Barva, která je nutná (včetně odpadu): 15 x 25 = 375 plechovek

## <a name="step-consumption"></a>Spotřeba kroku
Spotřeba kroku se používá k výpočtu konstantní spotřeby v intervalech množství. Vyberete-li **Spotřeba kroku** v poli **Vzorec** na kartě **Nastavení**, můžete přidat informace o krocích na kartě **Spotřeba kroku**. Pevné spotřebované množství lze nastavit v intervalech vyrobeného množství. Například spotřeba kroku je nastavena způsobem znázorněným v následující tabulce.

| Od řady | Množství |
|-------------|----------|
| 0,00        | 10,0000  |
| 100,00      | 20,0000  |
| 200,00      | 40,0000  |

Množství kusovníku je 1 a výrobní množství je 110. Vzorec pro spotřebu je Z řady (Množství) = Spotřeba. Protože výrobní množství je 110, spadá do kategorie "Ze série 100". Množství je proto 20.




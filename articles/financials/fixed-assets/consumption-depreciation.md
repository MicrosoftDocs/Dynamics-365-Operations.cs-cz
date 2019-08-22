---
title: Odpis spotřeby
description: Tento článek poskytuje přehled o metodě odpisu spotřeby.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840690"
---
# <a name="consumption-depreciation"></a>Odpis spotřeby

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled o metodě odpisu spotřeby.

Když vytvoříte odpisový plán pro dlouhodobý majetek a vyberete položku **Spotřeba** v poli **Metoda** ve formuláři **Odpisové plány**, budou dlouhodobé majetky přiřazeny k odpisovému plánu podle jejich používání. Na stránce **Odpisové plány** není nutné nastavovat procenta a intervaly. Po vytvoření odpisového plánu využívajícího metodu Spotřeba můžete metodu nastavit několika způsoby.

## <a name="set-up-and-use-consumption-depreciation"></a>Nastavení a použití odpisu spotřeby
1.  Na stránce **Odpisové plány** vytvořte odpisový plán. Pro výpočet spotřeby musí odpisový plán obsahovat ID a název a v poli **Metoda** musí být zvolena možnost **Spotřeba**.
2.  Na stránce  **Koeficienty spotřeby** nastavte koeficienty spotřeby. Každý koeficient spotřeby musí mít ID a název a koeficient spotřeby, který je zadán jako množství nebo jako procento.
3.  Na stránce **Jednotky spotřeby** nastavte jednotky spotřeby. Každá jednotka spotřeby musí mít ID a název. Na stránce **Odpis spotřeby** se pro výpočet odpisu spotřeby používají odpisové jednotky. Příklady jednotek jsou kilometr (km), kilogram (kg) nebo hodina.
4.  Na stránce **Dlouhodobý majetek** nastavte jednotlivé položky dlouhodobého majetku. Pro každý dlouhodobý majetek zvolte oceňovací model a knihu odpisů, které mají odpisový plán. Pokud některý z vašich dlouhodobých majetků používá odpisové plány založené na metodě Spotřeba, je nutné nastavit oceňovací model nebo knihy odpisů pro odpis spotřeby. Toto nastavení se provádí buď na kartě **Odpisy** na stránce **Oceňovací modely**, nebo na pevné záložce **Obecné** na stránce **Odpisový plán**. Stejný oceňovací model můžete použít pro více položek dlouhodobého majetku. Odpisové plány tvoří součást oceňovacího modelu nebo knihy odpisů, které jsou vybrány pro každý dlouhodobý majetek. Profily nelze přidávat ani upravovat přímo na stránce **Dlouhodobý majetek**. Odpisové profily je možné upravovat pouze na stránce **Knihy odpisů**.
5.  Na stránce **Oceňovací modely** nebo na stránce **Odpisové knihy** zadejte do skupiny polí **Odpis spotřeby** tyto informace:
    -   Koeficient spotřeby
    -   Jednotka
    -   Jednotkový odpis
    -   Odhadovaná spotřeba

    V poli **Zaúčtovaná spotřeba** se zobrazuje odpis spotřeby v jednotkách, které již byly zaúčtovány buď pro kombinaci dlouhodobého majetku a oceňovacího modelu, nebo pro knihu odpisů. Hodnotu v tomto poli nelze ručně upravit.

## <a name="examples"></a>Příklad
### <a name="example-1"></a>Příklad 1

Následující koeficient spotřeby je nastaven na 31. leden:

-   Množství je 1 000.
-   Odpisová cena jednotky, která je určena pro dlouhodobý majetek, je 1,5.

Návrh odpisu dne 31. ledna vypadá takto: množství × jednotkový odpis 1 000 × 1,5 = 1 500. Jestliže je pro dlouhodobý majetek nastaven procentuální koeficient, bude odhadované množství v poli **Odhadovaná spotřeba** pro oceňovací model dlouhodobého majetku vynásobeno procentem, které je nastaveno pro vybrané koncové datum. Výsledné množství je pak navrženo jako odpisové množství pro dané období.

### <a name="example-2"></a>Příklad 2

Následující koeficient pro odpis spotřeby je nastaven na 31. leden:

-   Procentuální hodnota činí 10 procent.
-   Odpisová cena jednotky, která je určena pro dlouhodobý majetek, je 1,5.
-   Odhadované množství dlouhodobého majetku je 2 000.

Odpisový plán 31. ledna vypadá takto: odhadované množství × procento × jednotkový odpis 2 000 × 0,10 × 1,5 = 300




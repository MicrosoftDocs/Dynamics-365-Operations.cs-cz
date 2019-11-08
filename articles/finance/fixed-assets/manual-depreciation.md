---
title: Ruční odpis
description: Tento článek poskytuje přehled o metodě ručního odpisu.
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
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84cde511ab0b5cbe4b99e72832bf548336b6b28c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187215"
---
# <a name="manual-depreciation"></a>Ruční odpis

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled o metodě ručního odpisu.

Když nastavujete odpisový plán dlouhodobého majetku a v poli **Metoda** na stránce **Odpisové plány** vyberete položku **Ručně**, jsou odpisy dlouhodobého majetku přiřazené k odpisovému plánu stanoveny podle procentuální hodnoty zadané pro každý interval v kalendářním roce. Nastavené procentuální hodnoty pro intervaly jsou zaúčtovány podle hodnoty, kterou jste vybrali v poli **Frekvence období** na pevné záložce **Obecné** na stránce **Odpisové plány**. Vybrat můžete tyto hodnoty:

-   Ročně
-   Měsíčně
-   Kvartálně
-   Pololetně
-   Denně

Po výběru frekvence období klikněte na možnost **Ruční plány** a nastavte procentuální hodnoty pro jednotlivé intervaly účtování. Ručně zadávané plány a intervaly účtování společně definují částku odpisu (viz příklady níže v tomto článku). Ruční odpisy se vždy počítají jako procentuální hodnota pořizovací ceny. U ručních odpisů nemusí procentuální hodnoty, které zadáváte do intervalů odpisu, dávat dohromady 100 procent. Ruční odpisy jsou flexibilní odpisovou metodu, která se často používá k určení mimořádného odpisového plánu na stránce **Knihy**, jako je například nepravidelný odpis pro zvláštní účely (například daň).

## <a name="examples"></a>Příklad
Pořizovací cena: 11 000,00 Předpokládaná konečná zůstatková hodnota: 1 000,00 V následující tabulce jsou uvedeny intervaly a procentuální hodnoty, které se nastavují na stránce **Plán odpisových plánů dlouhodobého majetku**.

| Číslo intervalu | Procento |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

V následující tabulce je znázorněn způsob výpočtu odpisu pro jednotlivé intervaly.

|  Číslo intervalu | Výpočet částky ročního odpisu | Zůstatková účetní hodnota na konci intervalu |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11 000 – 1 000) × 10 % = 1 000                | 10,000 (11 000 – 1 000)                   |
| 2                | (11 000 – 1 000) × 50 % = 5 000                | 5 000 (10 000 – 5 000)                    |
| 3                | (11 000 – 1 000) × 8 % = 800                   | 4 200 (5 000 – 800)                       |

Pokud v poli **Frekvence období** vyberete hodnotu **Měsíčně**, je nutné zadat 12 ručně naplánovaných intervalů. V následující tabulce jsou uvedeny částky odpisů za první dva intervaly.

| Interval | Odpisovaná částka            |
|----------|--------------------------------|
| Leden  | (11 000 – 1 000) × 10 % = 1 000 |
| Únor | (11 000 – 1 000) × 50 % = 5 000 |

Pokud vyberete hodnotu <strong>Pololetně</strong> v poli *<strong><em>Frekvence období</em>*,</strong> nastavujete dva ruční intervaly plánu. V následující tabulce jsou uvedeny částky odpisů za tyto dva intervaly.

| Interval    | Odpisovaná částka            |
|-------------|--------------------------------|
| 30. června     | (11 000 – 1 000) × 10 % = 1 000 |
| 31. prosince | (11 000 – 1 000) × 50 % = 5 000 |

Celkové procento pro všechny intervaly nemusí být 100. Pokud však hodnota v poli **Kumulativní procento** na stránce **Plán odpisových plánů dlouhodobého majetku** není **100**, obdržíte zprávu.



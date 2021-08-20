---
title: Z řádků prognózy nemůžete odstranit dimenzi prognózy poptávky skladu
description: Z řádků prognózy nemůžete odstranit dimenzi prognózy poptávky skladu.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 96af593d2e8a738258fe614f0f252620cb48c5f19eeb4425c9659ee6f9cd8c0c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741206"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Z řádků prognózy nemůžete odstranit dimenzi prognózy poptávky skladu

Číslo článku znalostní báze: 4614408

## <a name="symptoms"></a>Příznaky

K tomuto problému dochází, když dimenze **Sklad** není přiřazena na kartě **Dimenze prognózy** stránky **Parametr prognózy poptávky**. Sloupec **Sklad** se však na stránce **Prognóza poptávky** zobrazuje (**Hlavní plánování \> Prognóza \> Entita ruční prognózy \> Řádky prognózy poptávky**).

## <a name="resolution"></a>Rozlišení

Nastavení na kartě **Dimenze prognózy** na stránce **Parametr prognózy poptávky** neovlivňuje stránku **Prognóza poptávky**. Řídí základní prognózu, která se generuje a zobrazuje v upravené prognóze poptávky. Neřídí však rozměry, které jsou vyžadovány pro „skutečnou“ prognózu poptávky. Autorizací záznamů, které jsou zobrazeny na stránce **Upravená prognóza poptávky**, je můžete převést na „skutečné“ položky prognózy pro model prognózy. Tento model lze poté použít pro hlavní plánování.

Na stránce **Prognóza poptávky** jsou dimenze pro „skutečnou“ prognózu, které se zobrazují na řádcích prognózy poptávky, součástí dimenzí zásob. (Toto chování se podobá chování pro řádky prodejní objednávky.) Pokud váš systém není nastaven na použití **Skladu** jako povinné dimenze zásob, můžete stránku upravit tak, aby se sloupec skryl.

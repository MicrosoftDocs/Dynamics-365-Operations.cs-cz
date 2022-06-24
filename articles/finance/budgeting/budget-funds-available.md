---
title: Dostupné rozpočtové prostředky
description: Tento článek představuje funkci dostupných prostředků rozpočtu a poskytuje informace, které vám mohou pomoci nakonfigurovat kontrolu rozpočtu tak, aby optimalizovala správu finančních zdrojů vaší organizace.
author: RyanCCarlson2
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: b6f94931ba3514c1c66d80b64846d882861d555c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898233"
---
# <a name="budget-funds-available"></a>Dostupné rozpočtové prostředky

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tento článek představuje funkci dostupných prostředků rozpočtu a poskytuje informace, které vám mohou pomoci nakonfigurovat kontrolu rozpočtu tak, aby optimalizovala správu finančních zdrojů vaší organizace.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>K dispozici je vylepšená funkce výpočtu rozpočtových prostředků

Funkce **Sledovat pouze částky ve výpočtu dostupných rozpočtových prostředků** umožňuje sledovat základní tabulky řízení rozpočtu pro typy a stavy dokumentů na základě nastavení na stránce **Definovat parametry kontroly rozpočtu**.

Aby funkce správně fungovala, musí mít některé možnosti konfigurace řízení rozpočtu specifická nastavení. Tyto možnosti jsou vybrány nebo zrušeny na kartě **Dostupné rozpočtové prostředky** stránky **Definujte parametry kontroly rozpočtu**. Následující tabulka ukazuje nastavení, která jsou vyžadována pro funkci dostupných rozpočtových prostředků.

| Pokud je vybrána tato možnost | Tato možnost musí být také vybrána |
| ------------------------- | -------------------------------- |
| Rezervace rozpočtu pro předběžné břemeno | Rezervace rozpočtu pro břemena *a* Skutečné výdaje |
| Rezervace rozpočtu pro břemena | Skutečné výdaje |
| Rezervace rozpočtu pro břemena s dokumenty typu nákupní žádanka | Rezervace rozpočtu pro předběžné břemeno |

Tato funkce se týká pouze nových dokumentů. Částky pro stávající dokumenty budou nadále sledovány a zobrazovány v dotazu na statistiku kontroly rozpočtu, dokud se nezmění nastavení dostupných rozpočtových prostředků a neaktivuje se nová konfigurace kontroly rozpočtu. V tomto okamžiku budou odstraněna data sledování rozpočtu pro dokumenty, které byly odstraněny z výpočtu dostupných rozpočtových prostředků.

Doporučujeme, abyste nechali možnost **Nezaúčtované skutečné výdaje** nevybranou. Pokud je vybrána, provede se časově náročný výpočet kontroly rozpočtu na nezaúčtovaných dokumentech, jako jsou nevyřízené faktury dodavatele.

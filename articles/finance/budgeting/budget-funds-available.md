---
title: Dostupné rozpočtové prostředky
description: Toto téma představuje funkci dostupných prostředků rozpočtu a poskytuje informace, které vám mohou pomoci nakonfigurovat kontrolu rozpočtu tak, aby optimalizovala správu finančních zdrojů vaší organizace.
author: rcarlson
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: a8279ae9b08c7537548c1c8b71e6e978fee2b8a1
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891304"
---
# <a name="budget-funds-available"></a>Dostupné rozpočtové prostředky

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma představuje funkci dostupných prostředků rozpočtu a poskytuje informace, které vám mohou pomoci nakonfigurovat kontrolu rozpočtu tak, aby optimalizovala správu finančních zdrojů vaší organizace.

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

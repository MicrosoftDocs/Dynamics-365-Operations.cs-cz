---
title: Sestava dopředného posunutí dlouhodobého majetku
description: Toto téma vysvětluje postup při použití sestavy dopředného posunutí dlouhodobého majetku.
author: saraschi2
manager: ''
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 9374f4ae75d321d82a7c6e8be0770f766afef90e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257650"
---
# <a name="fixed-assets-roll-forward-report"></a>Sestava dopředného posunutí dlouhodobého majetku

[!include [banner](../includes/banner.md)]

**Sestava dopředného posunutí dlouhodobého majetku** poskytuje ve snadno čitelném formátu aplikace Microsoft Excel podrobná data dlouhodobého majetku, která vyžadujete pro uzávěrku období, finanční výkazy a vykazování daní. Tato sestava zahrnuje počáteční a koncové zůstatky dlouhodobého majetku, spolu s pohyby ocenění pro dané období, a jakákoliv pořízení nového majetku a vyřazení, ke kterým došlo během tohoto období. Data se vykazujuí pro jednotlivý dlouhodobý majetek a hodnoty jsou dále shrnuty pro skupiny dlouhodobého majetku a právnickou osobu.

Setava **dopředného posunutí dlouhodobého majetku** používá architekturu elektronického výkaznictví. Před spuštěním sestavy je nutné importovat model dlouhodobého majetku a konfigurace dopředného posunutí dlouhodobého majetku ze služby Microsoft Dynamics Lifecycle Services. Pokyny viz [Stažení konfigurace elektronického vykazování ze služby Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Tato sestava je k dispozici v Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3, nebo jako oprava hotfix pro Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (červenec 2017). Pro prostředí verze z července 2017 musí být aplikovány tři opravy hotfix:

- **KB 4041754:** Konfiguraci elektronického výkaznictví stáhnout z LCS jako použitelnou pro aktuální verzi po použití balíčku aktualizace platformy
- **KB 4056107:** Kumulativní aktualizace 5 elektronického výkaznictví
- **KB 4056353:** Sestavy výpisů a poznámek dlouhodobého majetku nesplňují požadavky v GAAP a IFRS

V následující tabulce jsou popsána pole, která jsou k dispozici v sestavě.


|                    Pole                    |                                                                                                                                popis                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              Zůstatky: Počáteční              |                                                                                           Zůstatková účetní hodnota dlouhodobého majetku k datu „od“ uvedenému v sestavě.                                                                                           |
|              Zůstatky: Konečné              |                                                                                            Zůstatková účetní hodnota dlouhodobého majetku k datu „do“ uvedenému v sestavě.                                                                                            |
|         Pořízení: Počáteční hodnota         |                                                 Součet všech transakcí typu <strong>Pořízení</strong> a <strong>Oprava pořizovací ceny</strong> k datu „od“ uvedenému v sestavě.                                                  |
|      Pořízení: Pořízení za období      |                                                 Součet všech transakcí typu <strong>Pořízení</strong> a <strong>Oprava pořizovací ceny</strong>, které byly zaúčtovány během rozsahu dat sestavy.                                                  |
|       Pořízení: Vyřazení za období        |                                                                        Součet všech zaúčtovaných stornování pořízení, která měla transakci vyřazení během rozsahu dat sestavy.                                                                        |
|         Pořízení: Konečná hodnota         |                                                  Součet všech transakcí typu <strong>Pořízení</strong> a <strong>Oprava pořizovací ceny</strong> k datu „do“ uvedenému v sestavě.                                                   |
|        Odpisy: Počáteční hodnota         | Součet všech transakcí typu <strong>Odpis</strong>, <strong>Oprava odpisu</strong>, <strong>Náhrada za zvláštní odpisy</strong> a <strong>Mimořádný odpis</strong> až do data „od“ uvedeného v sestavě. |
|     Odpisy: Odpisy za období     |                         Součet všech transakcí typu <strong>Odpis</strong>, <strong>Oprava odpisu</strong> a <strong>Mimořádný odpis</strong>, které byly zaúčtovány během rozsahu dat sestavy.                          |
| Odpisy: Speciální odpisy za období |                                                              Součet všech transakcí typu <strong>Náhrada za zvláštní odpisy</strong>, které byly zaúčtovány během rozsahu dat sestavy.                                                               |
|       Odpisy: Vyřazení za období       |                                                                       Součet všech zaúčtovaných stornování vyřazení, která měla transakci vyřazení během rozsahu dat sestavy.                                                                        |
|        Odpisy: Konečná hodnota         |  Součet všech transakcí typu <strong>Odpis</strong>, <strong>Oprava odpisu</strong>, <strong>Náhrada za zvláštní odpisy</strong> a <strong>Mimořádný odpis</strong> až do data „do“ uvedeného v sestavě.  |
|    Zvýšení odpisu/Snížení odpisu: Počáteční hodnota     |                              Součet všech transakcí typu <strong>Zvýšení odpisu</strong>, <strong>Snížení odpisu</strong> a <strong>Přecenění</strong> k datu „od“ uvedenému v sestavě.                               |
|   Zvýšení odpisu/Snížení odpisu: Zvýšení odpisu za období   |                                                                    Součet všech transakcí typu <strong>Zvýšení odpisu</strong>, které byly zaúčtovány během rozsahu dat sestavy.                                                                    |
|  Zvýšení odpisu/Snížení odpisu: Snížení odpisu za období  |                                                                   Součet všech transakcí typu <strong>Snížení odpisu</strong>, které byly zaúčtovány během rozsahu dat sestavy.                                                                   |
| Zvýšení odpisu/Snížení odpisu: Přecenění za období  |                                                                        Součet všech transakcí typu <strong>Přecenění</strong>, které byly zaúčtovány během rozsahu dat sestavy.                                                                        |
|   Zvýšení odpisu/Snížení odpisu: Vyřazení za období   |                                                           Součet všech zaúčtovaných stornování zvýšení odpisu, snížení odpisu a přecenění, která měla transakci vyřazení během rozsahu dat sestavy.                                                           |
|    Zvýšení odpisu/Snížení odpisu: Konečná hodnota     |                               Součet všech transakcí typu <strong>Zvýšení odpisu</strong>, <strong>Snížení odpisu</strong> a <strong>Přecenění</strong> k datu „do“ uvedenému v sestavě.                                |
|          Vyřazení: Datum vyřazení           |                                                                                                                Datum vyřazení pro knihu dlouhodobého majetku.                                                                                                                |
|    Vyřazení: Zůstatková účetní hodnota při vyřazení    |                                                                                                    Zůstatková účetní hodnota knihy dlouhodobého majetku při vyřazení.                                                                                                    |
|            Vyřazení: Hodnota prodeje            |                                                                                               Hodnota prodeje pro knihu dlouhodobého majetku s vyřazením – prodejní transakce.                                                                                                |
|           Vyřazení: Likvidační hodnota            |                                                                                               Likvidační hodnota prodeje pro knihu dlouhodobého majetku s vyřazením – likvidační transakce.                                                                                               |
|           Vyřazení: Zisk/ztráta            |                                                                                 Hodnota zisku nebo ztráty, která je vypočtena jako součást transakce vyřazení pro knihu dlouhodobého majetku.                                                                                 |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
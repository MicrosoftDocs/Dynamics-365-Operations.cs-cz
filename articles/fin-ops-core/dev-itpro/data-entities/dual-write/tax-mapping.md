---
title: Integrovaná daň
description: Toto téma popisuje integraci údajů o dani mezi finančními a provozními aplikacemi a Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 532e6603b74ad0293d65684d2d6858ef31fbc496
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063180"
---
# <a name="integrated-tax"></a>Integrovaná daň

[!include [banner](../../includes/banner.md)]



Data nastavení daně určují nastavení pro obě nepřímé daně (DPH, GST, DPH) a srážkové daně. Popisuje pravidlo výpočtu daně, daňovou sazbu, daňové účetnictví, vyrovnání a další koncepty.

## <a name="templates"></a>Šablony

Daňová data zahrnují mapy kolekce tabulek, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

| Finanční a provozní aplikace | Aplikace Customer Engagement | Popis |
|-----------------------------|-----------------------------------|-------------|
[Skupina DPH zboží](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Finanční úřady](mapping-reference.md#193) | msdyn_taxauthorities | |
[CDS entita kódu osvobození od DPH](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Skupiny DPH](mapping-reference.md#195) | msdyn_taxgroups | |
[Účetní skupiny hlavní knihy pro DPH V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Kódy srážkové daně](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Skupiny srážkové daně](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

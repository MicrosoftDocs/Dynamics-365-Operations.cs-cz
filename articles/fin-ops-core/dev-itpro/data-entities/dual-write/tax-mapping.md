---
title: Integrovaná daň
description: Tento článek popisuje integraci údajů o dani mezi finančními a provozními aplikacemi a Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8864a9567d57739aa72fa1859f5cfce6df33e8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864536"
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

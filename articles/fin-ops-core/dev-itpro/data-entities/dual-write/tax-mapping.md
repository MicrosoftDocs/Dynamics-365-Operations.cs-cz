---
title: Integrovaná daň
description: Toto téma popisuje integraci dat daní mezi aplikacemi Finance and Operations a Dataverse.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e1b5d62e56dd1f87dbfedc6a8ca7379587481ff4
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542312"
---
# <a name="integrated-tax"></a>Integrovaná daň

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Data nastavení daně určují nastavení pro obě nepřímé daně (DPH, GST, DPH) a srážkové daně. Popisuje pravidlo výpočtu daně, daňovou sazbu, daňové účetnictví, vyrovnání a další koncepty.

## <a name="templates"></a>Šablony

Daňová data zahrnují mapy kolekce tabulek, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

| Aplikace Finance and Operations | Aplikace Customer Engagement | popis |
|-----------------------------|-----------------------------------|-------------|
[Skupina DPH zboží](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Finanční úřady](mapping-reference.md#193) | msdyn_taxauthorities | |
[CDS entita kódu osvobození od DPH](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Skupiny DPH](mapping-reference.md#195) | msdyn_taxgroups | |
[Účetní skupiny hlavní knihy pro DPH V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Kódy srážkové daně](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Skupiny srážkové daně](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

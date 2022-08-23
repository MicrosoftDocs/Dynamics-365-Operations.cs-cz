---
title: Integrovaná daň
description: Tento článek popisuje integraci údajů o dani mezi finančními a provozními aplikacemi a Dataverse.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288787"
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


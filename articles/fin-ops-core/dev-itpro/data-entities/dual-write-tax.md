---
title: Integrovaná daň
description: Toto téma popisuje integraci údajů o dani mezi aplikacemi Finance and Operations a Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b6be53e9a2065373ca37c2791568a8161823803f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772403"
---
## <a name="integrated-tax"></a>Integrovaná daň

[!include [banner](../includes/banner.md)]

Data nastavení daně určují nastavení pro obě nepřímé daně (DPH, GST, DPH) a srážkové daně. Popisuje pravidlo výpočtu daně, daňovou sazbu, daňové účetnictví, vyrovnání a další koncepty.

## <a name="templates"></a>Šablony

Daňová data zahrnují mapy kolekce entit, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

Finance and Operations   | Aplikace Customer Engagement
-------------------------|---------------------------------
Kódy daní                  | msdyn\_taxcodes.md
Daňové skupiny               | msdyn\_taxgroups.md
Skupiny položek daně          | msdyn\_taxitemgroups.md
Osvobození od daně           | msdyn\_taxexemptcodes.md
Finanční úřady          | msdyn\_taxauthorities.md
Kódy srážkové daně      | msdyn\_withholdingtaxcodes.md
Skupiny srážkové daně   | msdyn\_withholdingtaxgroups.md
Skupina účtu hlavní daňové knihy | msdyn\_taxpostinggroups  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]


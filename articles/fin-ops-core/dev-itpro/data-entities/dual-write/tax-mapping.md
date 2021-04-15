---
title: Integrovaná daň
description: Toto téma popisuje integraci dat daní mezi aplikacemi Finance and Operations a Dataverse.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a7992520b57b4c19b6dc8e13bd8e9ffc87b40f5a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750635"
---
# <a name="integrated-tax"></a>Integrovaná daň

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Data nastavení daně určují nastavení pro obě nepřímé daně (DPH, GST, DPH) a srážkové daně. Popisuje pravidlo výpočtu daně, daňovou sazbu, daňové účetnictví, vyrovnání a další koncepty.

## <a name="templates"></a>Šablony

Daňová data zahrnují mapy kolekce tabulek, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

Aplikace Finance and Operations | Modelem řízené aplikace v Dynamics 365 | popis |
-------------------------|---------------------------------|----|
Skupina DPH zboží | msdyn_taxitemgroups |
Finanční úřady | msdyn_taxauthorities |
CDS entita kódu osvobození od DPH | msdyn_taxexemptcodes |
Skupiny DPH | msdyn_taxgroups |
Účetní skupiny hlavní knihy pro DPH V2 | msdyn_taxpostinggroups |
Kódy srážkové daně | msdyn_withholdingtaxcodes |
Skupiny srážkové daně | msdyn_withholdingtaxgroups | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
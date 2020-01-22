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
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853852"
---
# <a name="integrated-tax"></a><span data-ttu-id="24ac7-103">Integrovaná daň</span><span class="sxs-lookup"><span data-stu-id="24ac7-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24ac7-104">Data nastavení daně určují nastavení pro obě nepřímé daně (DPH, GST, DPH) a srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="24ac7-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="24ac7-105">Popisuje pravidlo výpočtu daně, daňovou sazbu, daňové účetnictví, vyrovnání a další koncepty.</span><span class="sxs-lookup"><span data-stu-id="24ac7-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="24ac7-106">Šablony</span><span class="sxs-lookup"><span data-stu-id="24ac7-106">Templates</span></span>

<span data-ttu-id="24ac7-107">Daňová data zahrnují mapy kolekce entit, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="24ac7-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="24ac7-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="24ac7-108">Finance and Operations</span></span>   | <span data-ttu-id="24ac7-109">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="24ac7-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="24ac7-110">Kódy daní</span><span class="sxs-lookup"><span data-stu-id="24ac7-110">Tax codes</span></span>                  | <span data-ttu-id="24ac7-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="24ac7-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="24ac7-112">Daňové skupiny</span><span class="sxs-lookup"><span data-stu-id="24ac7-112">Tax groups</span></span>               | <span data-ttu-id="24ac7-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="24ac7-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="24ac7-114">Skupiny položek daně</span><span class="sxs-lookup"><span data-stu-id="24ac7-114">Tax item groups</span></span>          | <span data-ttu-id="24ac7-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="24ac7-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="24ac7-116">Osvobození od daně</span><span class="sxs-lookup"><span data-stu-id="24ac7-116">Tax Exemptions</span></span>           | <span data-ttu-id="24ac7-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="24ac7-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="24ac7-118">Finanční úřady</span><span class="sxs-lookup"><span data-stu-id="24ac7-118">Tax Authorities</span></span>          | <span data-ttu-id="24ac7-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="24ac7-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="24ac7-120">Kódy srážkové daně</span><span class="sxs-lookup"><span data-stu-id="24ac7-120">Withholding tax codes</span></span>      | <span data-ttu-id="24ac7-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="24ac7-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="24ac7-122">Skupiny srážkové daně</span><span class="sxs-lookup"><span data-stu-id="24ac7-122">Withholding tax groups</span></span>   | <span data-ttu-id="24ac7-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="24ac7-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="24ac7-124">Skupina účtu hlavní daňové knihy</span><span class="sxs-lookup"><span data-stu-id="24ac7-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="24ac7-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="24ac7-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]


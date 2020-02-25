---
title: Integrovaná daň
description: Toto téma popisuje integraci dat daní mezi aplikacemi Finance and Operations a Common Data Service.
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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019676"
---
# <a name="integrated-tax"></a><span data-ttu-id="71fe4-103">Integrovaná daň</span><span class="sxs-lookup"><span data-stu-id="71fe4-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="71fe4-104">Data nastavení daně určují nastavení pro obě nepřímé daně (DPH, GST, DPH) a srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="71fe4-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="71fe4-105">Popisuje pravidlo výpočtu daně, daňovou sazbu, daňové účetnictví, vyrovnání a další koncepty.</span><span class="sxs-lookup"><span data-stu-id="71fe4-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="71fe4-106">Šablony</span><span class="sxs-lookup"><span data-stu-id="71fe4-106">Templates</span></span>

<span data-ttu-id="71fe4-107">Daňová data zahrnují mapy kolekce entit, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="71fe4-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="71fe4-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="71fe4-108">Finance and Operations</span></span>   | <span data-ttu-id="71fe4-109">Jiné aplikace Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="71fe4-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="71fe4-110">Kódy daní</span><span class="sxs-lookup"><span data-stu-id="71fe4-110">Tax codes</span></span>                  | <span data-ttu-id="71fe4-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="71fe4-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="71fe4-112">Daňové skupiny</span><span class="sxs-lookup"><span data-stu-id="71fe4-112">Tax groups</span></span>               | <span data-ttu-id="71fe4-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="71fe4-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="71fe4-114">Skupiny položek daně</span><span class="sxs-lookup"><span data-stu-id="71fe4-114">Tax item groups</span></span>          | <span data-ttu-id="71fe4-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="71fe4-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="71fe4-116">Osvobození od daně</span><span class="sxs-lookup"><span data-stu-id="71fe4-116">Tax Exemptions</span></span>           | <span data-ttu-id="71fe4-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="71fe4-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="71fe4-118">Finanční úřady</span><span class="sxs-lookup"><span data-stu-id="71fe4-118">Tax Authorities</span></span>          | <span data-ttu-id="71fe4-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="71fe4-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="71fe4-120">Kódy srážkové daně</span><span class="sxs-lookup"><span data-stu-id="71fe4-120">Withholding tax codes</span></span>      | <span data-ttu-id="71fe4-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="71fe4-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="71fe4-122">Skupiny srážkové daně</span><span class="sxs-lookup"><span data-stu-id="71fe4-122">Withholding tax groups</span></span>   | <span data-ttu-id="71fe4-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="71fe4-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="71fe4-124">Skupina účtu hlavní daňové knihy</span><span class="sxs-lookup"><span data-stu-id="71fe4-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="71fe4-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="71fe4-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]


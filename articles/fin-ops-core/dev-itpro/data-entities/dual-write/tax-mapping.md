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
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173078"
---
# <a name="integrated-tax"></a><span data-ttu-id="2ee64-103">Integrovaná daň</span><span class="sxs-lookup"><span data-stu-id="2ee64-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="2ee64-104">Data nastavení daně určují nastavení pro obě nepřímé daně (DPH, GST, DPH) a srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="2ee64-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="2ee64-105">Popisuje pravidlo výpočtu daně, daňovou sazbu, daňové účetnictví, vyrovnání a další koncepty.</span><span class="sxs-lookup"><span data-stu-id="2ee64-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="2ee64-106">Šablony</span><span class="sxs-lookup"><span data-stu-id="2ee64-106">Templates</span></span>

<span data-ttu-id="2ee64-107">Daňová data zahrnují mapy kolekce entit, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="2ee64-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="2ee64-108">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2ee64-108">Finance and Operations apps</span></span> | <span data-ttu-id="2ee64-109">Modelem řízené aplikace v Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="2ee64-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="2ee64-110">popis</span><span class="sxs-lookup"><span data-stu-id="2ee64-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="2ee64-111">Kódy daní</span><span class="sxs-lookup"><span data-stu-id="2ee64-111">Tax codes</span></span>                   | <span data-ttu-id="2ee64-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="2ee64-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="2ee64-113">Daňové skupiny</span><span class="sxs-lookup"><span data-stu-id="2ee64-113">Tax groups</span></span>                 | <span data-ttu-id="2ee64-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="2ee64-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="2ee64-115">Skupiny položek daně</span><span class="sxs-lookup"><span data-stu-id="2ee64-115">Tax item groups</span></span>             | <span data-ttu-id="2ee64-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="2ee64-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="2ee64-117">Osvobození od daně</span><span class="sxs-lookup"><span data-stu-id="2ee64-117">Tax Exemptions</span></span>             | <span data-ttu-id="2ee64-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="2ee64-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="2ee64-119">Finanční úřady</span><span class="sxs-lookup"><span data-stu-id="2ee64-119">Tax Authorities</span></span>             | <span data-ttu-id="2ee64-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="2ee64-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="2ee64-121">Kódy srážkové daně</span><span class="sxs-lookup"><span data-stu-id="2ee64-121">Withholding tax codes</span></span>       | <span data-ttu-id="2ee64-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="2ee64-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="2ee64-123">Skupiny srážkové daně</span><span class="sxs-lookup"><span data-stu-id="2ee64-123">Withholding tax groups</span></span>     | <span data-ttu-id="2ee64-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="2ee64-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="2ee64-125">Skupina účtu hlavní daňové knihy</span><span class="sxs-lookup"><span data-stu-id="2ee64-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="2ee64-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="2ee64-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]


---
title: Integrovaná daň
description: Toto téma popisuje integraci dat daní mezi aplikacemi Finance and Operations a Dataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 14c22dd6602b5fbf866c8dc6b057f6c8acb1f48f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679289"
---
# <a name="integrated-tax"></a><span data-ttu-id="de5e5-103">Integrovaná daň</span><span class="sxs-lookup"><span data-stu-id="de5e5-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="de5e5-104">Data nastavení daně určují nastavení pro obě nepřímé daně (DPH, GST, DPH) a srážkové daně.</span><span class="sxs-lookup"><span data-stu-id="de5e5-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="de5e5-105">Popisuje pravidlo výpočtu daně, daňovou sazbu, daňové účetnictví, vyrovnání a další koncepty.</span><span class="sxs-lookup"><span data-stu-id="de5e5-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="de5e5-106">Šablony</span><span class="sxs-lookup"><span data-stu-id="de5e5-106">Templates</span></span>

<span data-ttu-id="de5e5-107">Daňová data zahrnují mapy kolekce tabulek, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="de5e5-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="de5e5-108">Aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="de5e5-108">Finance and Operations apps</span></span> | <span data-ttu-id="de5e5-109">Modelem řízené aplikace v Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="de5e5-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="de5e5-110">popis</span><span class="sxs-lookup"><span data-stu-id="de5e5-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="de5e5-111">Skupina DPH zboží</span><span class="sxs-lookup"><span data-stu-id="de5e5-111">Item sales tax group</span></span> | <span data-ttu-id="de5e5-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="de5e5-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="de5e5-113">Finanční úřady</span><span class="sxs-lookup"><span data-stu-id="de5e5-113">Sales tax authorities</span></span> | <span data-ttu-id="de5e5-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="de5e5-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="de5e5-115">CDS entita kódu osvobození od DPH</span><span class="sxs-lookup"><span data-stu-id="de5e5-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="de5e5-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="de5e5-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="de5e5-117">Skupiny DPH</span><span class="sxs-lookup"><span data-stu-id="de5e5-117">Sales tax groups</span></span> | <span data-ttu-id="de5e5-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="de5e5-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="de5e5-119">Účetní skupiny hlavní knihy pro DPH V2</span><span class="sxs-lookup"><span data-stu-id="de5e5-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="de5e5-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="de5e5-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="de5e5-121">Kódy srážkové daně</span><span class="sxs-lookup"><span data-stu-id="de5e5-121">Withholding tax codes</span></span> | <span data-ttu-id="de5e5-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="de5e5-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="de5e5-123">Skupiny srážkové daně</span><span class="sxs-lookup"><span data-stu-id="de5e5-123">Withholding tax groups</span></span> | <span data-ttu-id="de5e5-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="de5e5-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]


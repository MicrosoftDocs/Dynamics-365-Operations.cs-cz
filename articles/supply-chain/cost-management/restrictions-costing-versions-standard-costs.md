---
title: Omezení nákladových verzí pro standardní náklady
description: Toto téma popisuje omezení, která se vztahují na nákladové verze pro standardní náklady.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0383f78ea5cfa42183e0bfe8a96d7d3866766e7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547714"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="c1682-103">Omezení nákladových verzí pro standardní náklady</span><span class="sxs-lookup"><span data-stu-id="c1682-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1682-104">Toto téma popisuje omezení, která se vztahují na nákladové verze pro standardní náklady.</span><span class="sxs-lookup"><span data-stu-id="c1682-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="c1682-105">Následující omezení pomáhají zajistit zachování principů pro standardní náklady:</span><span class="sxs-lookup"><span data-stu-id="c1682-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="c1682-106">Do nákladů na položku musí být zahrnuty náklady.</span><span class="sxs-lookup"><span data-stu-id="c1682-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="c1682-107">Náklady pro vyráběnou položku reprezentují amortizované konstantní náklady v informaci o kusovníku a údaji o postupu.</span><span class="sxs-lookup"><span data-stu-id="c1682-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="c1682-108">Náklady musí být tedy zahrnuty do jednotkových nákladů.</span><span class="sxs-lookup"><span data-stu-id="c1682-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="c1682-109">Náklady pro zakoupenou položku budou také zahrnuty do jednotkových nákladů položky.</span><span class="sxs-lookup"><span data-stu-id="c1682-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="c1682-110">Výpočet standardních nákladů pro vyráběné položky musí být založen na záznamech nákladů v nákladové verzi pro standardní náklady.</span><span class="sxs-lookup"><span data-stu-id="c1682-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="c1682-111">Alternativní zdroje dat nákladů lze použít pouze s nákladovou verzí pro plánované náklady, jako jsou například obchodní smlouvy s nákupní cenou pro zakoupené položky.</span><span class="sxs-lookup"><span data-stu-id="c1682-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="c1682-112">Alternativní zdroje dat nákladů jsou definované podle skupiny výpočtu kusovníku.</span><span class="sxs-lookup"><span data-stu-id="c1682-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="c1682-113">Výpočty kusovníku musí být prováděny v režimu rozpadu s jedinou úrovní.</span><span class="sxs-lookup"><span data-stu-id="c1682-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="c1682-114">Data nákladů na položku pro standardní náklady mohou být zkopírována do jiné nákladové verze, která obsahuje standardní náklady nebo plánované náklady.</span><span class="sxs-lookup"><span data-stu-id="c1682-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="c1682-115">Data nákladů na položku pro plánované náklady však nelze zkopírovat do nákladové verze, která obsahuje standardní náklady, protože by pro plánované náklady nebyla použita omezení uvedená výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="c1682-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="c1682-116">Související témata</span><span class="sxs-lookup"><span data-stu-id="c1682-116">Related topics</span></span>
--------

[<span data-ttu-id="c1682-117">Nákladové verze</span><span class="sxs-lookup"><span data-stu-id="c1682-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="c1682-118">Aktualizace standardních nákladů v nevýrobním prostředí</span><span class="sxs-lookup"><span data-stu-id="c1682-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="c1682-119">Postup přípravy na správu standardních nákladů pro vyráběné položky</span><span class="sxs-lookup"><span data-stu-id="c1682-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)


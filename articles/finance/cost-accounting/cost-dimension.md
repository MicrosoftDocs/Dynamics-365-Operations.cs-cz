---
title: Vytvoření dimenzí a import členů dimenze
description: Nákladové účetnictví je nezávislý modul vyžadující hlavní data z ostatních modulů.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3eedce9cd092f9c299a2381a28a801351f15c4cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226382"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="dbb59-103">Vytvoření dimenzí a import členů dimenze</span><span class="sxs-lookup"><span data-stu-id="dbb59-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbb59-104">Nákladové účetnictví je nezávislý modul vyžadující data z ostatních modulů.</span><span class="sxs-lookup"><span data-stu-id="dbb59-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="dbb59-105">Tato data lze rozdělit do následujících kategorií:</span><span class="sxs-lookup"><span data-stu-id="dbb59-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="dbb59-106">Prvky nákladů</span><span class="sxs-lookup"><span data-stu-id="dbb59-106">Cost elements</span></span>
-  <span data-ttu-id="dbb59-107">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="dbb59-107">Cost objects</span></span>
-  <span data-ttu-id="dbb59-108">Statistické dimenze</span><span class="sxs-lookup"><span data-stu-id="dbb59-108">Statistical dimensions</span></span>

<span data-ttu-id="dbb59-109">**Prvek nákladů** odpovídá příslušné položce nákladů v účtové osnově.</span><span class="sxs-lookup"><span data-stu-id="dbb59-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="dbb59-110">**Objekt nákladů** odpovídá jakémukoliv typu finanční dimenze, jako například produktům, nákladovým střediskům a projektům, které chcete odhadnout, přímo měřit nebo jim přidělit náklady.</span><span class="sxs-lookup"><span data-stu-id="dbb59-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="dbb59-111">**Statistická dimenze** a její členy se používají pro registraci nepeněžních položek.</span><span class="sxs-lookup"><span data-stu-id="dbb59-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="dbb59-112">Členy statistické dimenze lze použít jako základ přidělení v distribuci a přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="dbb59-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="dbb59-113">Následující diagram znázorňuje dimenze, které se používají v nákladovém účetnictví.</span><span class="sxs-lookup"><span data-stu-id="dbb59-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="dbb59-114">[![Dimenze nákladového účetnictví](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="dbb59-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="dbb59-115">Po importu dat do nákladového účetnictví můžete vytvořit různé perspektivy, které poskytují informace manažerům na všech úrovních organizace.</span><span class="sxs-lookup"><span data-stu-id="dbb59-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="dbb59-116">Následující témata obsahují informace o vytváření dimenzí a členech dimenze importu.</span><span class="sxs-lookup"><span data-stu-id="dbb59-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="dbb59-117">Dimenze prvku nákladů</span><span class="sxs-lookup"><span data-stu-id="dbb59-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="dbb59-118">Vytváření prvků nákladů</span><span class="sxs-lookup"><span data-stu-id="dbb59-118">Create cost elements</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="dbb59-119">Dimenze objektu nákladů</span><span class="sxs-lookup"><span data-stu-id="dbb59-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="dbb59-120">Mapování členů dimenze prvků nákladů na společnou sadu členů dimenze</span><span class="sxs-lookup"><span data-stu-id="dbb59-120">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="dbb59-121">Namapování dimenze prvku nákladů</span><span class="sxs-lookup"><span data-stu-id="dbb59-121">Map a cost element dimension</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="dbb59-122">Členy statistické dimenze a šablony poskytovatelů statistických měření</span><span class="sxs-lookup"><span data-stu-id="dbb59-122">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]
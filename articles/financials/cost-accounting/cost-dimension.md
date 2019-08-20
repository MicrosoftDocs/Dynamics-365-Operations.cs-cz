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
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a7db93e1877034051b6add4c11ddfe7cd7d17e0b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841578"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="8fcc9-103">Vytvoření dimenzí a import členů dimenze</span><span class="sxs-lookup"><span data-stu-id="8fcc9-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fcc9-104">Nákladové účetnictví je nezávislý modul vyžadující data z ostatních modulů.</span><span class="sxs-lookup"><span data-stu-id="8fcc9-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="8fcc9-105">Tato data lze rozdělit do následujících kategorií:</span><span class="sxs-lookup"><span data-stu-id="8fcc9-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="8fcc9-106">Prvky nákladů</span><span class="sxs-lookup"><span data-stu-id="8fcc9-106">Cost elements</span></span>
-  <span data-ttu-id="8fcc9-107">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="8fcc9-107">Cost objects</span></span>
-  <span data-ttu-id="8fcc9-108">Statistické dimenze</span><span class="sxs-lookup"><span data-stu-id="8fcc9-108">Statistical dimensions</span></span>

<span data-ttu-id="8fcc9-109">**Prvek nákladů** odpovídá příslušné položce nákladů v účtové osnově.</span><span class="sxs-lookup"><span data-stu-id="8fcc9-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="8fcc9-110">**Objekt nákladů** odpovídá jakémukoliv typu finanční dimenze, jako například produktům, nákladovým střediskům a projektům, které chcete odhadnout, přímo měřit nebo jim přidělit náklady.</span><span class="sxs-lookup"><span data-stu-id="8fcc9-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="8fcc9-111">**Statistická dimenze** a její členy se používají pro registraci nepeněžních položek.</span><span class="sxs-lookup"><span data-stu-id="8fcc9-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="8fcc9-112">Členy statistické dimenze lze použít jako základ přidělení v distribuci a přidělení nákladů.</span><span class="sxs-lookup"><span data-stu-id="8fcc9-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="8fcc9-113">Následující diagram znázorňuje dimenze, které se používají v nákladovém účetnictví.</span><span class="sxs-lookup"><span data-stu-id="8fcc9-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="8fcc9-114">[![Dimenze nákladového účetnictví](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="8fcc9-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="8fcc9-115">Po importu dat do nákladového účetnictví můžete vytvořit různé perspektivy, které poskytují informace manažerům na všech úrovních organizace.</span><span class="sxs-lookup"><span data-stu-id="8fcc9-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="8fcc9-116">Následující témata obsahují informace o vytváření dimenzí a členech dimenze importu.</span><span class="sxs-lookup"><span data-stu-id="8fcc9-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="8fcc9-117">Dimenze prvku nákladů</span><span class="sxs-lookup"><span data-stu-id="8fcc9-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="8fcc9-118">Vytváření prvků nákladů (průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="8fcc9-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="8fcc9-119">Dimenze objektu nákladů</span><span class="sxs-lookup"><span data-stu-id="8fcc9-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="8fcc9-120">Vytváření prvků nákladů (průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="8fcc9-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="8fcc9-121">Mapování členů dimenze prvků nákladů na společnou sadu členů dimenze</span><span class="sxs-lookup"><span data-stu-id="8fcc9-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="8fcc9-122">Namapování dimenze prvku nákladů (průvodce záznamem úloh)</span><span class="sxs-lookup"><span data-stu-id="8fcc9-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="8fcc9-123">Členy statistické dimenze a šablony poskytovatelů statistických měření</span><span class="sxs-lookup"><span data-stu-id="8fcc9-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)







---
title: "Nákupní objednávky pro projekt"
description: "Tento článek popisuje různé metody, které slouží k vytváření nákupních objednávek pro určitý projekt. Použitá metodu závisí na účelu nákupní objednávky a kdy jsou zakoupené položky spotřebovány a účtovány v projektu."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 985a57ae9fb116b1c4514b836b35c5da0f8838fd
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="e6b74-104">Nákupní objednávky pro projekt</span><span class="sxs-lookup"><span data-stu-id="e6b74-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e6b74-105">Tento článek popisuje různé metody, které slouží k vytváření nákupních objednávek pro určitý projekt.</span><span class="sxs-lookup"><span data-stu-id="e6b74-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="e6b74-106">Použitá metodu závisí na účelu nákupní objednávky a kdy jsou zakoupené položky spotřebovány a účtovány v projektu.</span><span class="sxs-lookup"><span data-stu-id="e6b74-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="e6b74-107">V aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition můžete použít několik způsobů pro vytvoření nákupních objednávek pro určitý projekt.</span><span class="sxs-lookup"><span data-stu-id="e6b74-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="e6b74-108">Použitá metodu závisí na účelu nákupní objednávky, kdy jsou zakoupené položky spotřebovány, a kdy jsou zakoupené položky účtovány v projektu.</span><span class="sxs-lookup"><span data-stu-id="e6b74-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="e6b74-109">Způsoby vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="e6b74-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="e6b74-110">Jednu z následujících metod můžete použít k vytvoření nákupní objednávky v modulu Řízení a účetnictví projektu.</span><span class="sxs-lookup"><span data-stu-id="e6b74-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="e6b74-111">Účel nákupní objednávky určuje, kdy je nákupní objednávka spotřebována a tedy kdy lze na projektu účtovat poplatky za položky.</span><span class="sxs-lookup"><span data-stu-id="e6b74-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6b74-112">Metoda</span><span class="sxs-lookup"><span data-stu-id="e6b74-112">Method</span></span></th>
<th><span data-ttu-id="e6b74-113">Účel</span><span class="sxs-lookup"><span data-stu-id="e6b74-113">Purpose</span></span></th>
<th><span data-ttu-id="e6b74-114">Spotřeba položek</span><span class="sxs-lookup"><span data-stu-id="e6b74-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6b74-115">Vytvoření nákupní objednávky přímo z projektu.</span><span class="sxs-lookup"><span data-stu-id="e6b74-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="e6b74-116">Tuto metodu použijte pro nákup zboží od externího dodavatele pro účely spotřeby na projektu.</span><span class="sxs-lookup"><span data-stu-id="e6b74-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="e6b74-117">Nákupní objednávku lze vytvořit dvěma způsoby.</span><span class="sxs-lookup"><span data-stu-id="e6b74-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="e6b74-118">Ze samotného projektu.</span><span class="sxs-lookup"><span data-stu-id="e6b74-118">From the project itself.</span></span> <span data-ttu-id="e6b74-119">V tomto případě je projekt pro nákupní objednávku již definován.</span><span class="sxs-lookup"><span data-stu-id="e6b74-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="e6b74-120">Přechodem k nákupní objednávce projektu.</span><span class="sxs-lookup"><span data-stu-id="e6b74-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="e6b74-121">Je nezbytné vybrat jak dodavatele, tak projekt, pro který se má nákupní objednávka vytvořit.</span><span class="sxs-lookup"><span data-stu-id="e6b74-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="e6b74-122">Položky jsou spotřebovány při aktualizaci faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e6b74-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6b74-123">Vytvořte nákupní objednávku z prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e6b74-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="e6b74-124">Tato metoda se použije, pokud se mají nakoupit položky při vytváření prodejní objednávky z projektu.</span><span class="sxs-lookup"><span data-stu-id="e6b74-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="e6b74-125">Položky jsou spotřebovány, když se prodejní objednávka fakturuje odběrateli.</span><span class="sxs-lookup"><span data-stu-id="e6b74-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6b74-126">Vytvořte nákupní objednávku z požadavku na položku.</span><span class="sxs-lookup"><span data-stu-id="e6b74-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="e6b74-127">Tato metoda se použije, pokud se mají nakoupit položky při vytváření požadavku na položku z projektu.</span><span class="sxs-lookup"><span data-stu-id="e6b74-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="e6b74-128">Položky jsou spotřebovány, když se aktualizuje dodací list požadavku na položku.</span><span class="sxs-lookup"><span data-stu-id="e6b74-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="e6b74-129">Při aktualizaci faktury nebo dodacího listu dodavatele budete požádáni, abyste aktualizovali dodací list v požadavku na položku.</span><span class="sxs-lookup"><span data-stu-id="e6b74-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="e6b74-130">Další informace naleznete v tématu [Přijetí položek na nákupní objednávce z požadavku na položku](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="e6b74-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



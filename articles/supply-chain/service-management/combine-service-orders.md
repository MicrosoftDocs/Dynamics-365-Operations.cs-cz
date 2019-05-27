---
title: Kombinace servisních zakázek
description: Servisní zakázky můžete kombinovat.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b94d81c431a068e891a0e05e996594f7e0be19f9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571943"
---
# <a name="combine-service-orders"></a><span data-ttu-id="73a47-103">Kombinace servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="73a47-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="73a47-104">Při vytváření řádků servisní zakázky automaticky ve formuláři **servisní smlouvy** můžete vybrat některou z následujících možností k určení způsobu jejich seskupení:</span><span class="sxs-lookup"><span data-stu-id="73a47-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="73a47-105">**Podle servisní smlouvy**</span><span class="sxs-lookup"><span data-stu-id="73a47-105">**By service agreement**</span></span>

  - <span data-ttu-id="73a47-106">**Podle servisní úlohy**</span><span class="sxs-lookup"><span data-stu-id="73a47-106">**By service task**</span></span>

  - <span data-ttu-id="73a47-107">**Podle zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="73a47-107">**By employee**</span></span>

  - <span data-ttu-id="73a47-108">**Podle předmětu servisu**</span><span class="sxs-lookup"><span data-stu-id="73a47-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="73a47-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="73a47-109">Example</span></span>

<span data-ttu-id="73a47-110">Vytvoříte servisní smlouvu s počátečním datem 31. 3. 2007.</span><span class="sxs-lookup"><span data-stu-id="73a47-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="73a47-111">V poli **Kombinace servisních zakázek** vyberte **Podle předmětu servisu**.</span><span class="sxs-lookup"><span data-stu-id="73a47-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="73a47-112">Poté vytvoříte následující řádky servisní zakázky:</span><span class="sxs-lookup"><span data-stu-id="73a47-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73a47-113">Číslo řádku smlouvy</span><span class="sxs-lookup"><span data-stu-id="73a47-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="73a47-114">typ transakce</span><span class="sxs-lookup"><span data-stu-id="73a47-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="73a47-115">popis</span><span class="sxs-lookup"><span data-stu-id="73a47-115">Description</span></span></p></th>
<th><p><span data-ttu-id="73a47-116">Interval</span><span class="sxs-lookup"><span data-stu-id="73a47-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="73a47-117">Předmět servisu</span><span class="sxs-lookup"><span data-stu-id="73a47-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="73a47-118">Datum zahájení</span><span class="sxs-lookup"><span data-stu-id="73a47-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73a47-119">1</span><span class="sxs-lookup"><span data-stu-id="73a47-119">1</span></span></p></td>
<td><p><span data-ttu-id="73a47-120"><strong>Hodina</strong></span><span class="sxs-lookup"><span data-stu-id="73a47-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="73a47-121">ŘSZ1</span><span class="sxs-lookup"><span data-stu-id="73a47-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="73a47-122">Týdně</span><span class="sxs-lookup"><span data-stu-id="73a47-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="73a47-123">X-1</span><span class="sxs-lookup"><span data-stu-id="73a47-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="73a47-124">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="73a47-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73a47-125">2</span><span class="sxs-lookup"><span data-stu-id="73a47-125">2</span></span></p></td>
<td><p><span data-ttu-id="73a47-126"><strong>Hodina</strong></span><span class="sxs-lookup"><span data-stu-id="73a47-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="73a47-127">ŘSZ2</span><span class="sxs-lookup"><span data-stu-id="73a47-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="73a47-128">Každé 2 týdny</span><span class="sxs-lookup"><span data-stu-id="73a47-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="73a47-129">X-2</span><span class="sxs-lookup"><span data-stu-id="73a47-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="73a47-130">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="73a47-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73a47-131">3</span><span class="sxs-lookup"><span data-stu-id="73a47-131">3</span></span></p></td>
<td><p><span data-ttu-id="73a47-132"><strong>Hodina</strong></span><span class="sxs-lookup"><span data-stu-id="73a47-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="73a47-133">ŘSZ3</span><span class="sxs-lookup"><span data-stu-id="73a47-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="73a47-134">Týdně</span><span class="sxs-lookup"><span data-stu-id="73a47-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="73a47-135">X-2</span><span class="sxs-lookup"><span data-stu-id="73a47-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="73a47-136">01.04.2007</span><span class="sxs-lookup"><span data-stu-id="73a47-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73a47-137">Pro žádný z řádků servisní zakázky nevytvoříte časová okna.</span><span class="sxs-lookup"><span data-stu-id="73a47-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="73a47-138">Řádky servisní zakázky proto nebude možné přesunout z vypočteného data, na které připadají.</span><span class="sxs-lookup"><span data-stu-id="73a47-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="73a47-139">Poté vygenerujete řádky servisní zakázky z formuláře **Vytvořit servisní zakázky** od 01.04.2007 do 30.04.2007.</span><span class="sxs-lookup"><span data-stu-id="73a47-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="73a47-140">Celkem vytvoříte 10 servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="73a47-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="73a47-141">Vzhledem k tomu, že jste vybrali nastavení kombinace **Podle předmětu servisu**, budou všechny vytvořené servisní zakázky obsahovat pouze řádky servisní zakázky, které se vztahují k jednomu konkrétnímu předmětu servisu.</span><span class="sxs-lookup"><span data-stu-id="73a47-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="73a47-142">Do jedné servisní zakázky budou zkombinovány řádky servisní zakázky vygenerované ze servisní smlouvy, které mají stejné datum servisu a stejný předmět.</span><span class="sxs-lookup"><span data-stu-id="73a47-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="73a47-143">V tomto příkladu neobsahuje kalendář uvedený ve formuláři <STRONG>Parametry řízení servisu</STRONG> žádné uzavřené dny.</span><span class="sxs-lookup"><span data-stu-id="73a47-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="73a47-144">Další seskupení řádků servisní zakázky do servisních objednávek vychází z časového intervalu, který jste zadali na řádcích servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="73a47-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="73a47-145">Viz také</span><span class="sxs-lookup"><span data-stu-id="73a47-145">See also</span></span>

[<span data-ttu-id="73a47-146">Automatické vytvoření servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="73a47-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  



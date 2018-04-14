--- 
title: "Přijetí položek na nákupní objednávce z požadavku na položku"
description: "Tento postup ukazuje, jak přijmout položky na nákupní objednávce z požadavku na položku."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fef6a597ed126ff4e1148fd9710b214c0425c3ab
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="7930b-103">Přijetí položek na nákupní objednávce z požadavku na položku</span><span class="sxs-lookup"><span data-stu-id="7930b-103">Receive items on purchase order from item requirement</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7930b-104">Tento postup ukazuje, jak přijmout položky na nákupní objednávce z požadavku na položku.</span><span class="sxs-lookup"><span data-stu-id="7930b-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="7930b-105">Použitím požadavků zboží namísto transakcí zboží můžete naplánovat dodávku těsně před vlastním použitím zboží, vytvořit prodejní objednávku, zahrnout zboží do rámce obchodní smlouvy nebo zahrnout požadavek na zboží do provozního plánování.</span><span class="sxs-lookup"><span data-stu-id="7930b-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="7930b-106">Tato úloha používá sadu dat USSI.</span><span class="sxs-lookup"><span data-stu-id="7930b-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="7930b-107">Přejděte na Řízení projektu a účetnictví > Projekty > Všechny projekty.</span><span class="sxs-lookup"><span data-stu-id="7930b-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="7930b-108">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7930b-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="7930b-109">V podokně akcí klikněte na položku Plán.</span><span class="sxs-lookup"><span data-stu-id="7930b-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="7930b-110">Klikněte na Požadavky na položky.</span><span class="sxs-lookup"><span data-stu-id="7930b-110">Click Item requirements.</span></span>
5. <span data-ttu-id="7930b-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7930b-111">Click New.</span></span>
6. <span data-ttu-id="7930b-112">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="7930b-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="7930b-113">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7930b-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="7930b-114">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="7930b-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="7930b-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7930b-115">Click Save.</span></span>
10. <span data-ttu-id="7930b-116">V podokně akcí klepněte na možnost Spravovat.</span><span class="sxs-lookup"><span data-stu-id="7930b-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="7930b-117">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="7930b-117">Click Functions.</span></span>
12. <span data-ttu-id="7930b-118">Klikněte na Vytvořit nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="7930b-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="7930b-119">Zaškrtněte políčko Zahrnout.</span><span class="sxs-lookup"><span data-stu-id="7930b-119">Select the Include check box.</span></span>
14. <span data-ttu-id="7930b-120">V poli Účet dodavatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7930b-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="7930b-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7930b-121">Click OK.</span></span>
16. <span data-ttu-id="7930b-122">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="7930b-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="7930b-123">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7930b-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="7930b-124">V podokně akcí klikněte na položku Nákup.</span><span class="sxs-lookup"><span data-stu-id="7930b-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="7930b-125">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="7930b-125">Click Confirm.</span></span>
20. <span data-ttu-id="7930b-126">V podokně akcí klikněte na položku Přijmout.</span><span class="sxs-lookup"><span data-stu-id="7930b-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="7930b-127">Klikněte na položku Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="7930b-127">Click Product receipt.</span></span>
22. <span data-ttu-id="7930b-128">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="7930b-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="7930b-129">Zadejte hodnotu do pole Příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="7930b-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="7930b-130">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7930b-130">Click OK.</span></span>



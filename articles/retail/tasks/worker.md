--- 
title: " Konfigurace pracovníka"
description: "Tato procedura ukazuje, jak nakonfigurovat pracovníka maloobchodu jako obchodního zástupce, který má nárok na provizi z prodeje v POS."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 721c075aa7bbe9d1ed439a84cae907e3db3aafa8
ms.contentlocale: cs-cz
ms.lasthandoff: 01/19/2018

---
# <a name="configure-a-worker"></a><span data-ttu-id="ac1d3-103"> Konfigurace pracovníka</span><span class="sxs-lookup"><span data-stu-id="ac1d3-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ac1d3-104">Tato procedura ukazuje, jak nakonfigurovat pracovníka maloobchodu jako obchodního zástupce, který má nárok na provizi z prodeje v POS.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="ac1d3-105">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="ac1d3-106">Vytvoření skupiny prodejní provize pro pracovníka</span><span class="sxs-lookup"><span data-stu-id="ac1d3-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="ac1d3-107">Přejděte na Prodej a marketing > Provize > Prodejní skupiny.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="ac1d3-108">Pracovníky lze přiřadit k jedné nebo více prodejních skupin.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="ac1d3-109">V POS můžete vybrat libovolnou prodejní skupinu, která obsahuje pracovníky z adresáře prodejny.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="ac1d3-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-110">Click New.</span></span>
3. <span data-ttu-id="ac1d3-111">Zadejte hodnotu do pole Skupina.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="ac1d3-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ac1d3-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-113">Click Save.</span></span>
6. <span data-ttu-id="ac1d3-114">V podokně akcí klikněte na položku Obecné.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="ac1d3-115">Klepněte na Obchodní zástupce.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-115">Click Sales rep.</span></span>
    * <span data-ttu-id="ac1d3-116">Prodejní skupina může obsahovat více než jednoho pracovníka.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="ac1d3-117">Provize můžete rozdělit mezi pracovníky podle toho, jak definujete podíl na provizi.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="ac1d3-118">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="ac1d3-119">V poli Podíl na provizi zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="ac1d3-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-120">Click Save.</span></span>
11. <span data-ttu-id="ac1d3-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-121">Close the page.</span></span>
12. <span data-ttu-id="ac1d3-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="ac1d3-123">Přiřazení výchozí prodejní skupiny pracovníkům</span><span class="sxs-lookup"><span data-stu-id="ac1d3-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="ac1d3-124">Přejděte na Maloobchodní a velkoobchodní prodej > Zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="ac1d3-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ac1d3-126">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ac1d3-127">Klikněte na kartu Maloobchod.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="ac1d3-128">Pracovníka lze přiřadit výchozí prodejní skupině.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="ac1d3-129">Výchozí prodejní skupina bude automaticky přidána do prodejních linek v POS, pokud je tato možnost povolena v profilu funkčnosti pro prodejnu.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="ac1d3-130">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-130">Click Edit.</span></span>
6. <span data-ttu-id="ac1d3-131">V poli Výchozí skupina zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="ac1d3-132">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ac1d3-132">Click Save.</span></span>



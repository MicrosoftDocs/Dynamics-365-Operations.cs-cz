---
title: Vytvoření dílčí nákupní objednávky z nákupní smlouvy
description: Tento postup popisuje použití nákupní smlouvy při vytváření nákupní objednávky.
author: mkirknel
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee0c40dfc3c820343c7054238cc2da47e8203d59
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204800"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="664c5-103">Vytvoření dílčí nákupní objednávky z nákupní smlouvy</span><span class="sxs-lookup"><span data-stu-id="664c5-103">Create a purchase release order from a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="664c5-104">Tento postup popisuje použití nákupní smlouvy při vytváření nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="664c5-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="664c5-105">Nákupní smlouva musí být použita při vytvoření nákupní objednávky, protože jsou v ní obecné podmínky, které musí být zkopírovány do záhlaví nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="664c5-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="664c5-106">Tento úkol obvykle provádí nákupčí.</span><span class="sxs-lookup"><span data-stu-id="664c5-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="664c5-107">Nezbytným předpokladem pro tohoto průvodce je platná nákupní smlouva se závazkem na množství produktu pro dodavatele a položky.</span><span class="sxs-lookup"><span data-stu-id="664c5-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="664c5-108">Stejný postup lze použít, máte-li nákupní smlouvou s jinými typy závazků.</span><span class="sxs-lookup"><span data-stu-id="664c5-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="664c5-109">Tohoto průvodce můžete použít s ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="664c5-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="664c5-110">Pokud používáte data USMF, můžete nejprve použít průvodce „Vytvoření nákupní smlouvy“ k nastavení nutných předpokladů pro tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="664c5-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="664c5-111">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="664c5-111">Create a purchase order</span></span>
1. <span data-ttu-id="664c5-112">V **navigačním podokně** přejděte na **Pracovní prostory > Příprava nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="664c5-112">In the **Navigation pane**, go to **Workspaces > Purchase order preparation**.</span></span> 
2. <span data-ttu-id="664c5-113">Klikněte na možnost **Nová nákupní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="664c5-113">Click **New purchase order**.</span></span>
3. <span data-ttu-id="664c5-114">V poli **Účet dodavatele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="664c5-114">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="664c5-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="664c5-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="664c5-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="664c5-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="664c5-117">Rozbalte záložku s náhledem **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="664c5-117">Expand the **General** fastTab.</span></span>
7. <span data-ttu-id="664c5-118">V poli **Nákupní smlouva** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="664c5-118">In the **Purchase agreement** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="664c5-119">Zde jsou uvedeny všechny dostupné smlouvy pro daného dodavatele.</span><span class="sxs-lookup"><span data-stu-id="664c5-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="664c5-120">Najděte platnou smlouvu, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="664c5-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="664c5-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="664c5-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="664c5-122">Klepněte na tlačítko **Ano**.</span><span class="sxs-lookup"><span data-stu-id="664c5-122">Click **Yes**.</span></span>
10. <span data-ttu-id="664c5-123">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="664c5-123">Click **OK**.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="664c5-124">Přidání řádku</span><span class="sxs-lookup"><span data-stu-id="664c5-124">Add a line</span></span>
1. <span data-ttu-id="664c5-125">Zadejte hodnotu do pole **Číslo zboží**.</span><span class="sxs-lookup"><span data-stu-id="664c5-125">In the **Item number** field, type a value.</span></span> <span data-ttu-id="664c5-126">Pokud jsou u závazku konkrétní dimenze zásob nebo místa, je nutné zadat stejné hodnoty na řádku nákupní objednávky, aby bylo možné smlouvu použít.</span><span class="sxs-lookup"><span data-stu-id="664c5-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="664c5-127">V poli **Lokalita** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="664c5-127">In the **Site** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="664c5-128">Site již může být vyplněn výchozí hodnotou z objednávky a od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="664c5-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="664c5-129">Pokud je vyplněn, tento krok vynechejte.</span><span class="sxs-lookup"><span data-stu-id="664c5-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="664c5-130">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="664c5-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="664c5-131">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="664c5-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="664c5-132">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="664c5-132">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="664c5-133">Ověřte, že se cena zkopírovala ze závazku.</span><span class="sxs-lookup"><span data-stu-id="664c5-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="664c5-134">Vyhledání závazku</span><span class="sxs-lookup"><span data-stu-id="664c5-134">Look up the commitment</span></span>
1. <span data-ttu-id="664c5-135">Klikněte na **Aktualizovat řádek**.</span><span class="sxs-lookup"><span data-stu-id="664c5-135">Click **Update line**.</span></span>
2. <span data-ttu-id="664c5-136">Klikněte na **Připojeno**.</span><span class="sxs-lookup"><span data-stu-id="664c5-136">Click **Attached**.</span></span> <span data-ttu-id="664c5-137">Zde můžete zjistit podrobnosti nákupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="664c5-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="664c5-138">Například zde je cena a údaj, zda jsou cena a sleva pevné, což znamená, že při změně ceny nebo slevy na nákupní objednávce na jinou hodnotu, než která je v závazku, systém propojení odebere, aby řádek nákupní objednávky nesplňoval závazek.</span><span class="sxs-lookup"><span data-stu-id="664c5-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="664c5-139">Můžete také vidět, zda je vybrána možnost Max je vynuceno, což znamená, že množství v závazku nelze překročit v součtu všech nákupů, které splňují daný závazek.</span><span class="sxs-lookup"><span data-stu-id="664c5-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="664c5-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="664c5-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="664c5-141">Vyhledání nákupní smlouvy</span><span class="sxs-lookup"><span data-stu-id="664c5-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="664c5-142">V **podokně akcí** klikněte na **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="664c5-142">On the **Action Pane**, click **General**.</span></span>
2. <span data-ttu-id="664c5-143">Klikněte na možnost **Nákupní smlouva**.</span><span class="sxs-lookup"><span data-stu-id="664c5-143">Click **Purchase agreement**.</span></span>
3. <span data-ttu-id="664c5-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="664c5-144">Close the page.</span></span>
4. <span data-ttu-id="664c5-145">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="664c5-145">Close the page.</span></span>


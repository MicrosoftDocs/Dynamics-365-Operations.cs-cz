---
title: "Přidání ovládacího prvku doporučení na stránku transakce na zařízení POS"
description: "Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 0d366997fbb6f23474047fa8c465a594491c46ad
ms.contentlocale: cs-cz
ms.lasthandoff: 01/19/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="c08c1-103">Přidání ovládacího prvku doporučení na stránku transakce na zařízení POS</span><span class="sxs-lookup"><span data-stu-id="c08c1-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="c08c1-104">Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="c08c1-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="c08c1-105">Když používáte Microsoft Dynamics 365 for Retail, můžete zobrazit na svém zařízení POS doporučení produktu.</span><span class="sxs-lookup"><span data-stu-id="c08c1-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="c08c1-106">*Doporučení* jsou položky, které mohou vaše zákazníky zajímat na základě jejich historie nákupů, položky v jejich seznamu požadovaných položek a položky, které jiní zákazníci nakoupili online nebo v kamenných obchodech.</span><span class="sxs-lookup"><span data-stu-id="c08c1-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="c08c1-107">Abyste mohli zobrazit doporučení produktu, musíte přidat ovládací prvek na obrazovce transakce pomocí návrháře rozložení obrazovky.</span><span class="sxs-lookup"><span data-stu-id="c08c1-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="c08c1-108">Otevřete návrháře rozložení</span><span class="sxs-lookup"><span data-stu-id="c08c1-108">Open Layout designer</span></span>
1.  <span data-ttu-id="c08c1-109">Přejděte do nabídky **Maloobchod** &gt; **Instalace kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Rozložení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="c08c1-110">Pomocí rychlého filtru vyhledejte obrazovku, ke které chcete přidat ovládací prvek.</span><span class="sxs-lookup"><span data-stu-id="c08c1-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="c08c1-111">Například použijte filtr na pole **ID rozvržení obrazovky** pomocí hodnoty F2CP16:9M.</span><span class="sxs-lookup"><span data-stu-id="c08c1-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="c08c1-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c08c1-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="c08c1-113">Vyberte například Název: F2CP16:9M ID rozvržení obrazovky: F2CP16:9M.</span><span class="sxs-lookup"><span data-stu-id="c08c1-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="c08c1-114">Klikněte na možnost **Návrhář rozložení**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="c08c1-115">Podle pokynů spusťte návrháře rozložení.</span><span class="sxs-lookup"><span data-stu-id="c08c1-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="c08c1-116">Po zobrazení výzvy k zadání přihlašovacích údajů zadejte stejné přihlašovací údaje, které jste použili při spuštění návrháře rozložení ze stránky **Rozložení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="c08c1-117">Při přihlášení se zobrazí stránka podobná té na obrázku.</span><span class="sxs-lookup"><span data-stu-id="c08c1-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="c08c1-118">Rozložení se bude lišit podle přizpůsobení, která jste pro svůj obchod provedli.</span><span class="sxs-lookup"><span data-stu-id="c08c1-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="c08c1-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Zvolte možnost zobrazení</span><span class="sxs-lookup"><span data-stu-id="c08c1-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="c08c1-120">K dispozici jsou dvě možnosti konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c08c1-120">There are two configurations options available.</span></span> <span data-ttu-id="c08c1-121">Vyberte možnost, která nejlépe vyhovuje vašemu obchodu, a postupujte podle dalších pokynů k dokončení nastavení ovládacího prvku.</span><span class="sxs-lookup"><span data-stu-id="c08c1-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="c08c1-122">Tyto dvě možnosti jsou:</span><span class="sxs-lookup"><span data-stu-id="c08c1-122">The two options are:</span></span>
-   <span data-ttu-id="c08c1-123">Doporučení jsou vždy viditelná.</span><span class="sxs-lookup"><span data-stu-id="c08c1-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="c08c1-124">Karta **Doporučení** se zobrazí v mřížce na pravé straně obrazovky.</span><span class="sxs-lookup"><span data-stu-id="c08c1-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="c08c1-125">Jak udělat, aby byla doporučení vždy viditelná</span><span class="sxs-lookup"><span data-stu-id="c08c1-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="c08c1-126">Zmenšete výšku oblasti podrobností řádků transakce tak, aby byla stejná jako výška panelu odběratele po levé straně.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="c08c1-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="c08c1-127">Z nabídky vlevo přetáhněte ovládací prvek doporučení mezi oblast podrobností řádků transakce a mřížku tlačítek uprostřed dolní části obrazovky transakce.</span><span class="sxs-lookup"><span data-stu-id="c08c1-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="c08c1-128">Změňte velikost ovládacího prvku tak, aby se vešel do prostoru.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="c08c1-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="c08c1-129">Návrháře rozložení uložíte a zavřete kliknutím na **X**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="c08c1-130">V aplikaci Dynamics 365 for Retail přejděte na **Maloobchod** &gt; **IT pro maloobchod** &gt; **Plány distribuce**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="c08c1-131">V seznamu vyberte možnost **1090, Pokladny**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="c08c1-132">Klikněte na možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="c08c1-133">Jak přidat kartu Doporučení na mřížku tlačítek na pravé straně obrazovky</span><span class="sxs-lookup"><span data-stu-id="c08c1-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="c08c1-134">Klikněte pravým tlačítkem myši do prázdného místa pod poslední kartou na mřížce tlačítek umístěné na pravé straně stránky.</span><span class="sxs-lookup"><span data-stu-id="c08c1-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="c08c1-135">Klikněte na **Přizpůsobit**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="c08c1-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="c08c1-136">Klikněte na možnost **Nová karta**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="c08c1-137">Najděte novou kartu, kterou jste právě přidali.</span><span class="sxs-lookup"><span data-stu-id="c08c1-137">Find the new tab that you just added.</span></span> <span data-ttu-id="c08c1-138">Možná se budete muset posunout dolů.</span><span class="sxs-lookup"><span data-stu-id="c08c1-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="c08c1-139">V rozevíracím seznamu **Obsah** zvolte **Doporučené produkty**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="c08c1-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="c08c1-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="c08c1-141">Do pole **Popisek** zadejte název pro kartu doporučení. Zadejte například Doporučené produkty.</span><span class="sxs-lookup"><span data-stu-id="c08c1-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="c08c1-142">V poli **Obrázek** zvolte obrázek, který se zobrazí na kartě.</span><span class="sxs-lookup"><span data-stu-id="c08c1-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="c08c1-143">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-143">Click **OK**.</span></span> <span data-ttu-id="c08c1-144">Nová karta se zobrazí v mřížce tlačítek.</span><span class="sxs-lookup"><span data-stu-id="c08c1-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="c08c1-145">Návrháře rozložení uložíte a zavřete kliknutím na **X**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="c08c1-146">V aplikaci Dynamics 365 for Retail přejděte na **Maloobchod** &gt; **IT pro maloobchod** &gt; **Plány distribuce**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="c08c1-147">V seznamu vyberte možnost **1090, Pokladny**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="c08c1-148">Klikněte na možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="c08c1-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="c08c1-149">Viz také</span><span class="sxs-lookup"><span data-stu-id="c08c1-149">See also</span></span>
--------

[<span data-ttu-id="c08c1-150">Přehled přizpůsobených doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="c08c1-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)





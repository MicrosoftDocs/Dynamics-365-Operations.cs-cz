---
title: "Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS"
description: "Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 26b03b6712c97b12e1221598de308813c7986179
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="dddbc-103">Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS</span><span class="sxs-lookup"><span data-stu-id="dddbc-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="dddbc-104">Aktuální verzi služby doporučení produktu odstraňujeme, protože předěláváme tuto funkci s lepším algoritmem a novějšími funkčnostmi orientovanými na maloobchod.</span><span class="sxs-lookup"><span data-stu-id="dddbc-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="dddbc-105">Další informace naleznete v části [Odstraněné nebo zastaralé funkce](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="dddbc-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="dddbc-106">Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="dddbc-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="dddbc-107">Když používáte Microsoft Dynamics 365 for Retail, můžete zobrazit na svém zařízení POS doporučení produktu.</span><span class="sxs-lookup"><span data-stu-id="dddbc-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="dddbc-108">*Doporučení* jsou položky, které mohou vaše zákazníky zajímat na základě jejich historie nákupů, položky v jejich seznamu požadovaných položek a položky, které jiní zákazníci nakoupili online nebo v kamenných obchodech.</span><span class="sxs-lookup"><span data-stu-id="dddbc-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="dddbc-109">Abyste mohli zobrazit doporučení produktu, musíte přidat ovládací prvek na obrazovce transakce pomocí návrháře rozložení obrazovky.</span><span class="sxs-lookup"><span data-stu-id="dddbc-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="dddbc-110">Otevřete návrháře rozložení</span><span class="sxs-lookup"><span data-stu-id="dddbc-110">Open Layout designer</span></span>
1.  <span data-ttu-id="dddbc-111">Přejděte do nabídky **Maloobchod** &gt; **Instalace kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Rozložení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="dddbc-112">Pomocí rychlého filtru vyhledejte obrazovku, ke které chcete přidat ovládací prvek.</span><span class="sxs-lookup"><span data-stu-id="dddbc-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="dddbc-113">Například použijte filtr na pole **ID rozvržení obrazovky** pomocí hodnoty F2CP16:9M.</span><span class="sxs-lookup"><span data-stu-id="dddbc-113">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="dddbc-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="dddbc-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="dddbc-115">Vyberte například Název: F2CP16:9M ID rozvržení obrazovky: F2CP16:9M.</span><span class="sxs-lookup"><span data-stu-id="dddbc-115">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="dddbc-116">Klikněte na možnost **Návrhář rozložení**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-116">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="dddbc-117">Podle pokynů spusťte návrháře rozložení.</span><span class="sxs-lookup"><span data-stu-id="dddbc-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="dddbc-118">Po zobrazení výzvy k zadání přihlašovacích údajů zadejte stejné přihlašovací údaje, které jste použili při spuštění návrháře rozložení ze stránky **Rozložení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="dddbc-119">Při přihlášení se zobrazí stránka podobná té na obrázku.</span><span class="sxs-lookup"><span data-stu-id="dddbc-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="dddbc-120">Rozložení se bude lišit podle přizpůsobení, která jste pro svůj obchod provedli.</span><span class="sxs-lookup"><span data-stu-id="dddbc-120">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="dddbc-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Zvolte možnost zobrazení</span><span class="sxs-lookup"><span data-stu-id="dddbc-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="dddbc-122">K dispozici jsou dvě možnosti konfigurace.</span><span class="sxs-lookup"><span data-stu-id="dddbc-122">There are two configurations options available.</span></span> <span data-ttu-id="dddbc-123">Vyberte možnost, která nejlépe vyhovuje vašemu obchodu, a postupujte podle dalších pokynů k dokončení nastavení ovládacího prvku.</span><span class="sxs-lookup"><span data-stu-id="dddbc-123">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="dddbc-124">Tyto dvě možnosti jsou:</span><span class="sxs-lookup"><span data-stu-id="dddbc-124">The two options are:</span></span>
-   <span data-ttu-id="dddbc-125">Doporučení jsou vždy viditelná.</span><span class="sxs-lookup"><span data-stu-id="dddbc-125">Recommendations are always visible.</span></span>
-   <span data-ttu-id="dddbc-126">Karta **Doporučení** se zobrazí v mřížce na pravé straně obrazovky.</span><span class="sxs-lookup"><span data-stu-id="dddbc-126">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="dddbc-127">Jak udělat, aby byla doporučení vždy viditelná</span><span class="sxs-lookup"><span data-stu-id="dddbc-127">To make recommendations always visible</span></span>

1.  <span data-ttu-id="dddbc-128">Zmenšete výšku oblasti podrobností řádků transakce tak, aby byla stejná jako výška panelu odběratele po levé straně.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="dddbc-128">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="dddbc-129">Z nabídky vlevo přetáhněte ovládací prvek doporučení mezi oblast podrobností řádků transakce a mřížku tlačítek uprostřed dolní části obrazovky transakce.</span><span class="sxs-lookup"><span data-stu-id="dddbc-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="dddbc-130">Změňte velikost ovládacího prvku tak, aby se vešel do prostoru.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="dddbc-130">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="dddbc-131">Návrháře rozložení uložíte a zavřete kliknutím na **X**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-131">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="dddbc-132">V aplikaci Dynamics 365 for Retail přejděte na **Maloobchod** &gt; **IT pro maloobchod** &gt; **Plány distribuce**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-132">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="dddbc-133">V seznamu vyberte možnost **1090, Pokladny**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-133">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="dddbc-134">Klikněte na možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-134">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="dddbc-135">Jak přidat kartu Doporučení na mřížku tlačítek na pravé straně obrazovky</span><span class="sxs-lookup"><span data-stu-id="dddbc-135">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="dddbc-136">Klikněte pravým tlačítkem myši do prázdného místa pod poslední kartou na mřížce tlačítek umístěné na pravé straně stránky.</span><span class="sxs-lookup"><span data-stu-id="dddbc-136">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="dddbc-137">Klikněte na **Přizpůsobit**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="dddbc-137">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="dddbc-138">Klikněte na možnost **Nová karta**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-138">Click **New tab**.</span></span>
4.  <span data-ttu-id="dddbc-139">Najděte novou kartu, kterou jste právě přidali.</span><span class="sxs-lookup"><span data-stu-id="dddbc-139">Find the new tab that you just added.</span></span> <span data-ttu-id="dddbc-140">Možná se budete muset posunout dolů.</span><span class="sxs-lookup"><span data-stu-id="dddbc-140">You may need to scroll down.</span></span>
5.  <span data-ttu-id="dddbc-141">V rozevíracím seznamu **Obsah** zvolte **Doporučené produkty**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-141">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="dddbc-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="dddbc-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="dddbc-143">Do pole **Popisek** zadejte název pro kartu doporučení. Zadejte například Doporučené produkty.</span><span class="sxs-lookup"><span data-stu-id="dddbc-143">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="dddbc-144">V poli **Obrázek** zvolte obrázek, který se zobrazí na kartě.</span><span class="sxs-lookup"><span data-stu-id="dddbc-144">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="dddbc-145">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-145">Click **OK**.</span></span> <span data-ttu-id="dddbc-146">Nová karta se zobrazí v mřížce tlačítek.</span><span class="sxs-lookup"><span data-stu-id="dddbc-146">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="dddbc-147">Návrháře rozložení uložíte a zavřete kliknutím na **X**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-147">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="dddbc-148">V aplikaci Dynamics 365 for Retail přejděte na **Maloobchod** &gt; **IT pro maloobchod** &gt; **Plány distribuce**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-148">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="dddbc-149">V seznamu vyberte možnost **1090, Pokladny**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-149">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="dddbc-150">Klikněte na možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="dddbc-150">Click **Run now**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="dddbc-151">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="dddbc-151">Additional resources</span></span>
--------

[<span data-ttu-id="dddbc-152">Přehled doporučení přizpůsobeného produktu</span><span class="sxs-lookup"><span data-stu-id="dddbc-152">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)





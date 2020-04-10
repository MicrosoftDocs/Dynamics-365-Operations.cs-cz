---
title: Přidání doporučení na obrazovku transakce
description: Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/19/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: a39389da0908953cbbc161f07d067ce3fc569a1b
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154125"
---
# <a name="add-recommendations-to-the-transaction-screen"></a><span data-ttu-id="e94d6-103">Přidání doporučení na obrazovku transakce</span><span class="sxs-lookup"><span data-stu-id="e94d6-103">Add recommendations to the transaction screen</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="e94d6-104">Toto téma popisuje, jak přidat ovládací prvek doporučení na obrazovku transakcí na zařízení POS pomocí návrháře rozložení obrazovky v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e94d6-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="e94d6-105">Další informace o doporučeních produktů naleznete v dokumentaci [doporučení produktu v dokumentaci POS](product.md).</span><span class="sxs-lookup"><span data-stu-id="e94d6-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="e94d6-106">Když používáte Commerce, můžete zobrazit na svém zařízení POS doporučení produktu.</span><span class="sxs-lookup"><span data-stu-id="e94d6-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="e94d6-107">Abyste mohli zobrazit doporučení produktu, musíte přidat ovládací prvek na obrazovce transakce pomocí návrháře rozložení obrazovky.</span><span class="sxs-lookup"><span data-stu-id="e94d6-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="e94d6-108">Otevřete návrháře rozložení</span><span class="sxs-lookup"><span data-stu-id="e94d6-108">Open Layout designer</span></span>

1. <span data-ttu-id="e94d6-109">Přejděte do nabídky **Retail and Commerce** &gt; **Instalace kanálu** &gt; **Nastavení POS** &gt; **POS** &gt; **Rozložení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="e94d6-110">Pomocí rychlého filtru vyhledejte obrazovku, ke které chcete přidat ovládací prvek.</span><span class="sxs-lookup"><span data-stu-id="e94d6-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="e94d6-111">Například použijte filtr na pole **ID rozvržení obrazovky** pomocí hodnoty **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="e94d6-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e94d6-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="e94d6-113">Vyberte například **Název: F2CP16:9M ID rozvržení obrazovky: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="e94d6-114">Klikněte na možnost **Návrhář rozložení**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="e94d6-115">Podle pokynů spusťte návrháře rozložení.</span><span class="sxs-lookup"><span data-stu-id="e94d6-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="e94d6-116">Po zobrazení výzvy k zadání přihlašovacích údajů zadejte stejné přihlašovací údaje, které jste použili při spuštění návrháře rozložení ze stránky **Rozložení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="e94d6-117">Při přihlášení se zobrazí stránka podobná té na obrázku.</span><span class="sxs-lookup"><span data-stu-id="e94d6-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="e94d6-118">Rozložení se bude lišit podle přizpůsobení, která jste pro svůj obchod provedli.</span><span class="sxs-lookup"><span data-stu-id="e94d6-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="e94d6-119">[![Návrhář rozložení](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="e94d6-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="e94d6-120">Zvolit zobrazenou možnost</span><span class="sxs-lookup"><span data-stu-id="e94d6-120">Choose a display option</span></span>

<span data-ttu-id="e94d6-121">K dispozici jsou dvě možnosti konfigurace.</span><span class="sxs-lookup"><span data-stu-id="e94d6-121">There are two configurations options available.</span></span> <span data-ttu-id="e94d6-122">Vyberte možnost, která nejlépe vyhovuje vašemu obchodu, a postupujte podle dalších pokynů k dokončení nastavení ovládacího prvku.</span><span class="sxs-lookup"><span data-stu-id="e94d6-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="e94d6-123">Tyto dvě možnosti jsou:</span><span class="sxs-lookup"><span data-stu-id="e94d6-123">The two options are:</span></span>

- <span data-ttu-id="e94d6-124">Doporučení jsou vždy viditelná.</span><span class="sxs-lookup"><span data-stu-id="e94d6-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="e94d6-125">Karta **Doporučení** se zobrazí v mřížce na pravé straně obrazovky.</span><span class="sxs-lookup"><span data-stu-id="e94d6-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="e94d6-126">Nastavení, aby byla doporučení vždy viditelná</span><span class="sxs-lookup"><span data-stu-id="e94d6-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="e94d6-127">Zmenšete výšku oblasti podrobností řádků transakce tak, aby byla stejná jako výška panelu odběratele po levé straně.</span><span class="sxs-lookup"><span data-stu-id="e94d6-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="e94d6-128">[![Snížená výška oblasti podrobností řádků transakce](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="e94d6-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="e94d6-129">Z nabídky vlevo přetáhněte ovládací prvek doporučení mezi oblast podrobností řádků transakce a mřížku tlačítek uprostřed dolní části obrazovky transakce.</span><span class="sxs-lookup"><span data-stu-id="e94d6-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="e94d6-130">Změňte velikost ovládacího prvku tak, aby se vešel do prostoru.</span><span class="sxs-lookup"><span data-stu-id="e94d6-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="e94d6-131">[![Ovládací prvek doporučení přidaný do rozvržení](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="e94d6-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="e94d6-132">Návrháře rozložení uložíte a zavřete kliknutím na **X**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="e94d6-133">V aplikaci Commerce přejděte na **Retail and Commerce** &gt; **IT pro Retail and Commerce** &gt; **Plány distribuce**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="e94d6-134">V seznamu vyberte možnost **1090, Pokladny**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="e94d6-135">Klikněte na možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="e94d6-136">Jak přidat kartu Doporučení na mřížku tlačítek na pravé straně obrazovky</span><span class="sxs-lookup"><span data-stu-id="e94d6-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="e94d6-137">Klikněte pravým tlačítkem myši do prázdného místa pod poslední kartou na mřížce tlačítek umístěné na pravé straně stránky.</span><span class="sxs-lookup"><span data-stu-id="e94d6-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="e94d6-138">Klikněte na tlačítko**přizpůsobit**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-138">Click **Customize**.</span></span>

    <span data-ttu-id="e94d6-139">[![Přizpůsobení – dialogové okno ovládacího prvku karty](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="e94d6-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="e94d6-140">Klikněte na možnost **Nová karta**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-140">Click **New tab**.</span></span>
4. <span data-ttu-id="e94d6-141">Najděte novou kartu, kterou jste právě přidali.</span><span class="sxs-lookup"><span data-stu-id="e94d6-141">Find the new tab that you just added.</span></span> <span data-ttu-id="e94d6-142">Možná se budete muset posunout dolů.</span><span class="sxs-lookup"><span data-stu-id="e94d6-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="e94d6-143">V rozevíracím seznamu **Obsah** zvolte **Doporučené produkty**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="e94d6-144">[![Zvolení doporučených produktů v poli obsahu](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="e94d6-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="e94d6-145">Do pole **Popisek** zadejte název pro kartu doporučení. Zadejte například "Doporučené produkty".</span><span class="sxs-lookup"><span data-stu-id="e94d6-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="e94d6-146">V poli **Obrázek** zvolte obrázek, který se zobrazí na kartě.</span><span class="sxs-lookup"><span data-stu-id="e94d6-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="e94d6-147">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-147">Click **OK**.</span></span> <span data-ttu-id="e94d6-148">Nová karta se zobrazí v mřížce tlačítek.</span><span class="sxs-lookup"><span data-stu-id="e94d6-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="e94d6-149">Návrháře rozložení uložíte a zavřete kliknutím na **X**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="e94d6-150">V aplikaci Commerce přejděte na **Retail and Commerce** &gt; **IT pro Retail and Commerce** &gt; **Plány distribuce**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="e94d6-151">V seznamu vyberte možnost **1090, Pokladny**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="e94d6-152">Klikněte na možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="e94d6-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e94d6-153">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="e94d6-153">Additional resources</span></span>

[<span data-ttu-id="e94d6-154">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="e94d6-154">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="e94d6-155">Povolení ADLS v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e94d6-155">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="e94d6-156">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="e94d6-156">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="e94d6-157">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="e94d6-157">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="e94d6-158">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="e94d6-158">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="e94d6-159">Přidání doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="e94d6-159">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e94d6-160">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="e94d6-160">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="e94d6-161">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="e94d6-161">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="e94d6-162">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="e94d6-162">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="e94d6-163">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="e94d6-163">Product recommendations FAQ</span></span>](faq-recommendations.md)

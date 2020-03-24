---
title: Přidání doporučení produktů v POS
description: Toto téma popisuje používání doporučení produktů na zařízení v místě prodeje (POS).
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 48533596c5bdc73dd8c815166e7dde0ca2f3cb4d
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127806"
---
# <a name="add-product-recommendations-on-pos"></a><span data-ttu-id="75421-103">Přidání doporučení produktů v POS</span><span class="sxs-lookup"><span data-stu-id="75421-103">Add product recommendations on POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="75421-104">Doporučení produktu jsou ve své podstatě transformativní obchodní aplikace, která pokrývá všechny obchodní prostory a vytváří bohaté, poutavé a na míru šité zkušenosti objevování produktů.</span><span class="sxs-lookup"><span data-stu-id="75421-104">At its core, product recommendations are a transformative business application that span across all commerce spaces to create rich, engaging, and tailored product discovery experiences.</span></span> <span data-ttu-id="75421-105">Chcete-li tuto funkci implementovat do programu POS, postupujte [podle pokynů, jak přidat doporučení na zařízení POS.](add-recommendations-control-pos-screen.md)</span><span class="sxs-lookup"><span data-stu-id="75421-105">To implement this feature on POS, follow the steps on [how to add recommendations to your POS devices.](add-recommendations-control-pos-screen.md)</span></span> 

<span data-ttu-id="75421-106">Další informace o funkcích doporučeních produktů naleznete v [přehledu doporučení produktu.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="75421-106">For more information about product recommendations features, read the [product recommendations overview.](../commerce/product-recommendations.md)</span></span> 

## <a name="scenarios"></a><span data-ttu-id="75421-107">Scénáře</span><span class="sxs-lookup"><span data-stu-id="75421-107">Scenarios</span></span>

<span data-ttu-id="75421-108">Doporučení produktu jsou povolena pro následující scénáře POS.</span><span class="sxs-lookup"><span data-stu-id="75421-108">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="75421-109">Jsou k dispozici v Cloud POS nebo Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="75421-109">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1. <span data-ttu-id="75421-110">Na stránce **Podrobnosti o produktu**:</span><span class="sxs-lookup"><span data-stu-id="75421-110">On the **Product details** page:</span></span>

    - <span data-ttu-id="75421-111">Pokud obchod asociuje návštěvy se stránkou **Podrobnosti o produktu** při vyhledávání předchozích transakcí napříč různými kanály, služba doporučení navrhuje další položky, které budou pravděpodobně nakoupeny společně.</span><span class="sxs-lookup"><span data-stu-id="75421-111">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendations service suggests additional items that are likely to be purchased together.</span></span>

    <span data-ttu-id="75421-112">[![Doporučení na stránce Podrobnosti produktu](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="75421-112">[![Recommendations on the Product details page](./media/proddetails.png)](./media/proddetails.png)</span></span>

2. <span data-ttu-id="75421-113">Na stránce **Transakce**:</span><span class="sxs-lookup"><span data-stu-id="75421-113">On the **Transaction** page:</span></span>

    - <span data-ttu-id="75421-114">Modul doporučení navrhuje položky založené na celém seznamu položek v nákupním košíku, které se často nakupují.</span><span class="sxs-lookup"><span data-stu-id="75421-114">The recommendation engine suggests items based on the entire list of items in the basket that are frequently bought together.</span></span>

    > [!NOTE]
    > <span data-ttu-id="75421-115">Pokud chce maloobchodník zobrazit doporučení na stránce **Transakce**, musí aktualizovat rozložení obrazovky v Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="75421-115">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 Commerce.</span></span> <span data-ttu-id="75421-116">Ovládací prvek **Doporučení** musí být na stránce **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="75421-116">The **Recommendations** control must be dropped onto the **Transaction** page.</span></span>

    <span data-ttu-id="75421-117">[![Doporučení na stránce Transakce](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="75421-117">[![Recommendations on the Transaction page](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

## <a name="configure-commerce-to-enable-pos-recommendations"></a><span data-ttu-id="75421-118">Konfigurace aplikace Commerce pro povolení doporučení POS</span><span class="sxs-lookup"><span data-stu-id="75421-118">Configure Commerce to enable POS recommendations</span></span>

<span data-ttu-id="75421-119">Chcete-li nastavit doporučení produktu, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="75421-119">To set up product recommendations, follow these steps:</span></span>

1. <span data-ttu-id="75421-120">Zkontrolujte, zda byla služba aktualizována v sestavení **10.0.6.**</span><span class="sxs-lookup"><span data-stu-id="75421-120">Ensure your service has been updated to the **10.0.6 build.**</span></span>
2. <span data-ttu-id="75421-121">Postupujte podle pokynů pro [povolení doporučení produktu](../commerce/enable-product-recommendations.md) pro váš podnik.</span><span class="sxs-lookup"><span data-stu-id="75421-121">Follow the instructions on how to [enable product recommendations](../commerce/enable-product-recommendations.md) for your business.</span></span>
3. <span data-ttu-id="75421-122">Volitelné: Chcete-li zobrazit doporučení na obrazovce transakce, přejděte na **Rozvržení obrazovky**, zvolte rozložení obrazovky, spusťte **Návrhář rozvržení obrazovky**, a potom umístěte ovládací prvek **doporučení**, kam je třeba.</span><span class="sxs-lookup"><span data-stu-id="75421-122">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>
4. <span data-ttu-id="75421-123">Přejděte na **Parametry velkoobchodu**, vyberte **Strojové učení** a vyberte **Ano** v části **Povolit doporučení POS**.</span><span class="sxs-lookup"><span data-stu-id="75421-123">Go to **Commerce parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5. <span data-ttu-id="75421-124">Doporučení na POS zobrazíte spuštěním globální konfigurační úlohy **1110**.</span><span class="sxs-lookup"><span data-stu-id="75421-124">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="75421-125">Aby se změny návrháře rozvržení obrazovky POS projevily, spusťte úlohu konfigurace kanálu **1070**.</span><span class="sxs-lookup"><span data-stu-id="75421-125">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a><span data-ttu-id="75421-126">Řešení problémů, když máte doporučení produktu již povolena</span><span class="sxs-lookup"><span data-stu-id="75421-126">Troubleshoot issues where you have Product recommendations already enabled</span></span>

- <span data-ttu-id="75421-127">Přejděte na **Parametry velkoobchodu** \> **Seznam doporučení** \> **Zakázat doporučení produktu** a spusťte **globální konfigurační úlohu \[9999\]**.</span><span class="sxs-lookup"><span data-stu-id="75421-127">Navigate to **Commerce Parameters** \> **Recommendation lists** \> **Disable product recommendations** and run **Global configuration job \[9999\]**.</span></span> 
- <span data-ttu-id="75421-128">Pokud jste přidali **Řízení doporučení** na svou obrazovku transakcí pomocí nástroje **Návrhář rozložení obrazovky**, odstraňte ho také.</span><span class="sxs-lookup"><span data-stu-id="75421-128">If you added the **Recommendations control** to your transaction screen using the **Screen layout designer**, please remove that as well.</span></span>
- <span data-ttu-id="75421-129">Máte-li další dotazy, vyhledejte další informace [v nejčastějších dotazech k doporučením produktu](../commerce/faq-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="75421-129">If you have additional questions, check out the [Product recommendations FAQ](../commerce/faq-recommendations.md) for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75421-130">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="75421-130">Additional resources</span></span>

[<span data-ttu-id="75421-131">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="75421-131">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="75421-132">Povolení ADLS v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="75421-132">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="75421-133">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="75421-133">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="75421-134">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="75421-134">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="75421-135">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="75421-135">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="75421-136">Přidání seznamů doporučení na web e-Commerce</span><span class="sxs-lookup"><span data-stu-id="75421-136">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="75421-137">Přidání doporučení na obrazovku transakce</span><span class="sxs-lookup"><span data-stu-id="75421-137">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="75421-138">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="75421-138">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="75421-139">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="75421-139">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="75421-140">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="75421-140">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="75421-141">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="75421-141">Product recommendations FAQ</span></span>](faq-recommendations.md)

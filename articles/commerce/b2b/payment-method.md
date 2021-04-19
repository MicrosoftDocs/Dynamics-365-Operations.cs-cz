---
title: Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B
description: Toto téma popisuje, jak nakonfigurovat platební metodu zákaznického účtu pro weby elektronického obchodování typu business-to-business (B2B).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 62e8f4949dcea1cb201bece171991047ce28da04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799798"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="59422-103">Nakonfigurujte způsob platby zákaznického účtu pro stránky elektronického obchodování B2B</span><span class="sxs-lookup"><span data-stu-id="59422-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59422-104">Toto téma popisuje, jak nakonfigurovat platební metodu zákaznického účtu pro weby elektronického obchodování typu business-to-business (B2B).</span><span class="sxs-lookup"><span data-stu-id="59422-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="59422-105">Maloobchodní prodejci mohou přijímat různé typy plateb za výrobky a služby, které prodávají v kanálu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="59422-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="59422-106">Každý typ platby, kterou prodejce přijímá, musí být nakonfigurován při nastavení systému v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="59422-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="59422-107">Platební metoda zákaznického účtu (nebo „na účet“) musí být podporována na webech B2B elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="59422-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="59422-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="59422-108">Prerequisites</span></span>

1. <span data-ttu-id="59422-109">Přidejte platební metodu zákaznického účtu v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="59422-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="59422-110">Přiřaďte platební metodu zákaznického účtu ke kanálu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="59422-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="59422-111">Ujistěte se, že je povolena funkce **Povolit na účet** pro zákazníka povoleno v **Retail a Commerce \> Zákazníci \> Všichni zákazníci \> Výchozí nastavení plateb** v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="59422-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="59422-112">Ujistěte se také, že jsou parametry **Úvěrový limit** pro zákazníka nastaveny vhodně v **Retail a Commerce \> Zákazníci \> Všichni zákazníci \> Úvěr a inkasa** v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="59422-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="59422-113">Povolte způsob platby zákaznického účtu v konfigurátoru webů Commerce</span><span class="sxs-lookup"><span data-stu-id="59422-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="59422-114">Chcete-li povolit způsob platby zákaznického účtu v konfigurátoru webů Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="59422-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="59422-115">Přejděte na **Nastavení webu \> Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="59422-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="59422-116">Nastavte vlastnost **Povolit platby na zákaznický účet** na **Povoleno pro zákazníky B2B**.</span><span class="sxs-lookup"><span data-stu-id="59422-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="59422-117">Vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="59422-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="59422-118">Nové nastavení webu se projeví až po aktualizaci souboru app.settings.json.</span><span class="sxs-lookup"><span data-stu-id="59422-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="59422-119">Další informace viz [Aktualizace knihoven SDK a modulů](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="59422-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="59422-120">Povolte platební metodu zákaznického účtu na stránce pokladny pro web elektronického obchodování B2B</span><span class="sxs-lookup"><span data-stu-id="59422-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="59422-121">Chcete-li povolit platební metodu zákaznického účtu na stránce pokladny pro web elektronického obchodování B2B, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="59422-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="59422-122">V konfigurátoru webů Commerce vyhledejte a upravte stránku pokladny nebo fragment, který obsahuje modul pokladny pro web elektronického obchodování B2B.</span><span class="sxs-lookup"><span data-stu-id="59422-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="59422-123">Ve slotu **Kontejner sekce pokladny** vyberte **Přidat modul** a pak přidejte modul **Platba na účet zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="59422-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="59422-124">Umístěte modul **Platba na účet zákazníka** výběrem třech teček (**...**) a poté vyberte **Posunout nahoru** nebo **Posunout dolů** podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="59422-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="59422-125">Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="59422-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="59422-126">Potvrďte, že byla povolena a zveřejněna platební metoda zákaznického účtu</span><span class="sxs-lookup"><span data-stu-id="59422-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="59422-127">Chcete-li potvrdit, že byla povolena a zveřejněna platební metoda zákaznického účtu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="59422-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="59422-128">Přihlaste se do webu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="59422-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="59422-129">Přidejte produkt do košíku.</span><span class="sxs-lookup"><span data-stu-id="59422-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="59422-130">Přejděte na stránku pokladny.</span><span class="sxs-lookup"><span data-stu-id="59422-130">Go to the checkout page.</span></span> <span data-ttu-id="59422-131">Měli byste vidět novou platební metodu **Zákaznický účet**.</span><span class="sxs-lookup"><span data-stu-id="59422-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59422-132">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="59422-132">Additional resources</span></span>

[<span data-ttu-id="59422-133">Nastavení webu elektronického obchodování B2B</span><span class="sxs-lookup"><span data-stu-id="59422-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="59422-134">Vytvářejte hierarchie modelování org pro organizace B2B</span><span class="sxs-lookup"><span data-stu-id="59422-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="59422-135">Spravujte uživatele - obchodní partnery - na webech B2B elektronického obchodování</span><span class="sxs-lookup"><span data-stu-id="59422-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="59422-136">Nastavte limity množství produktů pro weby B2B elektronického obchodování</span><span class="sxs-lookup"><span data-stu-id="59422-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="59422-137">SDK a aktualizace knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="59422-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
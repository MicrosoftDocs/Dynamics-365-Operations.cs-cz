---
title: Možnost vyzvednout se nezobrazí na stránkách podrobností košíku nebo produktu
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se možnost vyzvednutí v obchodě nezobrazí na stránce košíku nebo na stránkách s podrobnostmi o produktu.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585228"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="b7dc4-103">Možnost „vyzvednout“ se nezobrazí na stránkách podrobností košíku nebo produktu</span><span class="sxs-lookup"><span data-stu-id="b7dc4-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b7dc4-104">Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se možnost vyzvednutí v obchodě nezobrazí na stránce košíku nebo na stránkách s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="b7dc4-105">popis</span><span class="sxs-lookup"><span data-stu-id="b7dc4-105">Description</span></span>

<span data-ttu-id="b7dc4-106">Tlačítko **Vyzvednout** se nezobrazí na stránkách podrobností košíku nebo produktu.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="b7dc4-107">Následující obrázek ukazuje příklad stránky, která obsahuje tlačítko **Vyzvednout**.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Tlačítko Vyzvednout](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="b7dc4-109">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="b7dc4-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="b7dc4-110">Povolte rozšíření BOPIS v Tvůrci webů Commerce</span><span class="sxs-lookup"><span data-stu-id="b7dc4-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="b7dc4-111">Chcete-li povolit rozšíření „koupit online, vyzvednout v obchodě“ (BOPIS) v nástroji pro tvorbu webů Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b7dc4-112">Vyberte web.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-112">Select your site.</span></span>
1. <span data-ttu-id="b7dc4-113">Vyberte **Nastavení webu** a pak vyberte **Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="b7dc4-114">Ujistěte se, že není vybrána možnost **Zakázat BOPIS**.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="b7dc4-115">Konfigurace způsobů doručení v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="b7dc4-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="b7dc4-116">Konfiguraci režimu doručení v centrále Commerce provedete následovně.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b7dc4-117">Přejděte na **Zásobování a zdroje \> Nastavení \> Způsoby dodání**.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="b7dc4-118">Ujistěte se, že byl vytvoření režim doručení **Vyzvednutí zákazníkem** a k němu jsou přiřazeny produkty a adresy.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="b7dc4-119">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry**.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="b7dc4-120">V levém navigačním podokně vyberte položku **Objednávky zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="b7dc4-121">Ujistěte se, že je **Způsob doručení vyzvednutím** správně nakonfigurován.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="b7dc4-122">Konfigurace plateb objednávek zákazníků</span><span class="sxs-lookup"><span data-stu-id="b7dc4-122">Configure customer orders payments</span></span>

<span data-ttu-id="b7dc4-123">Chcete-li nakonfigurovat platby objednávek zákazníků v centrále Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b7dc4-124">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry**.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="b7dc4-125">V levém navigačním podokně vyberte položku **Objednávky zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="b7dc4-126">Na kartě s náhledem **Platby** zkontrolujte se, že pole **Platební podmínky** a **Způsob platby** jsou správně nastavena.</span><span class="sxs-lookup"><span data-stu-id="b7dc4-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7dc4-127">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b7dc4-127">Additional resources</span></span>

[<span data-ttu-id="b7dc4-128">Konfigurace BOPIS</span><span class="sxs-lookup"><span data-stu-id="b7dc4-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="b7dc4-129">Povolení více způsobů vyzvednutí/doručení objednávek zákazníků</span><span class="sxs-lookup"><span data-stu-id="b7dc4-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="b7dc4-130">Omnikanálové platby objednávek Commerce</span><span class="sxs-lookup"><span data-stu-id="b7dc4-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="b7dc4-131">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="b7dc4-131">Store selector module</span></span>](../store-selector.md)

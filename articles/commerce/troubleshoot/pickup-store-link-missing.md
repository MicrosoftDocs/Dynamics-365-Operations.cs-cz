---
title: Možnost vyzvednout se nezobrazí na stránkách podrobností košíku nebo produktu
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se možnost vyzvednutí v obchodě nezobrazí na stránce košíku nebo na stránkách s podrobnostmi o produktu.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: f692d73bf1755422e9bfc8314c1156e043ccf761
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020797"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="d919e-103">Možnost „vyzvednout“ se nezobrazí na stránkách podrobností košíku nebo produktu</span><span class="sxs-lookup"><span data-stu-id="d919e-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d919e-104">Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když se možnost vyzvednutí v obchodě nezobrazí na stránce košíku nebo na stránkách s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="d919e-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="d919e-105">popis</span><span class="sxs-lookup"><span data-stu-id="d919e-105">Description</span></span>

<span data-ttu-id="d919e-106">Tlačítko **Vyzvednout** se nezobrazí na stránkách podrobností košíku nebo produktu.</span><span class="sxs-lookup"><span data-stu-id="d919e-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="d919e-107">Následující obrázek ukazuje příklad stránky, která obsahuje tlačítko **Vyzvednout**.</span><span class="sxs-lookup"><span data-stu-id="d919e-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Tlačítko Vyzvednout](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="d919e-109">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="d919e-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="d919e-110">Povolte rozšíření BOPIS v Tvůrci webů Commerce</span><span class="sxs-lookup"><span data-stu-id="d919e-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="d919e-111">Chcete-li povolit rozšíření „koupit online, vyzvednout v obchodě“ (BOPIS) v nástroji pro tvorbu webů Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="d919e-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d919e-112">Vyberte web.</span><span class="sxs-lookup"><span data-stu-id="d919e-112">Select your site.</span></span>
1. <span data-ttu-id="d919e-113">Vyberte **Nastavení webu** a pak vyberte **Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="d919e-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="d919e-114">Ujistěte se, že není vybrána možnost **Zakázat BOPIS**.</span><span class="sxs-lookup"><span data-stu-id="d919e-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="d919e-115">Konfigurace způsobů doručení v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="d919e-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="d919e-116">Konfiguraci režimu doručení v centrále Commerce provedete následovně.</span><span class="sxs-lookup"><span data-stu-id="d919e-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d919e-117">Přejděte na **Zásobování a zdroje \> Nastavení \> Způsoby dodání**.</span><span class="sxs-lookup"><span data-stu-id="d919e-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="d919e-118">Ujistěte se, že byl vytvoření režim doručení **Vyzvednutí zákazníkem** a k němu jsou přiřazeny produkty a adresy.</span><span class="sxs-lookup"><span data-stu-id="d919e-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="d919e-119">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry**.</span><span class="sxs-lookup"><span data-stu-id="d919e-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="d919e-120">V levém navigačním podokně vyberte položku **Objednávky zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="d919e-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="d919e-121">Ujistěte se, že je **Způsob doručení vyzvednutím** správně nakonfigurován.</span><span class="sxs-lookup"><span data-stu-id="d919e-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="d919e-122">Konfigurace plateb objednávek zákazníků</span><span class="sxs-lookup"><span data-stu-id="d919e-122">Configure customer orders payments</span></span>

<span data-ttu-id="d919e-123">Chcete-li nakonfigurovat platby objednávek zákazníků v centrále Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="d919e-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d919e-124">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry**.</span><span class="sxs-lookup"><span data-stu-id="d919e-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="d919e-125">V levém navigačním podokně vyberte položku **Objednávky zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="d919e-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="d919e-126">Na kartě s náhledem **Platby** zkontrolujte se, že pole **Platební podmínky** a **Způsob platby** jsou správně nastavena.</span><span class="sxs-lookup"><span data-stu-id="d919e-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d919e-127">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="d919e-127">Additional resources</span></span>

[<span data-ttu-id="d919e-128">Konfigurace BOPIS</span><span class="sxs-lookup"><span data-stu-id="d919e-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="d919e-129">Povolení více způsobů vyzvednutí/doručení objednávek zákazníků</span><span class="sxs-lookup"><span data-stu-id="d919e-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="d919e-130">Omnikanálové platby objednávek Commerce</span><span class="sxs-lookup"><span data-stu-id="d919e-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="d919e-131">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="d919e-131">Store selector module</span></span>](../store-selector.md)

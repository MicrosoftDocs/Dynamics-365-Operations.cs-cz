---
title: Možnost Uložit pro mou další platbu se nezobrazí
description: Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se políčko Uložit pro moji další platbu nezobrazí v části Platební metoda na stránce pokladny webu elektronického obchodování.
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
ms.openlocfilehash: 3a4fbcd522651ed1b82b72b751ff6ead44c94a71
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585233"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="09ec0-103">Možnost „Uložit pro mou další platbu“ se nezobrazí</span><span class="sxs-lookup"><span data-stu-id="09ec0-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09ec0-104">Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se políčko **Uložit pro moji další platbu** nezobrazí v části **Platební metoda** na stránce pokladny webu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="09ec0-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="09ec0-105">popis</span><span class="sxs-lookup"><span data-stu-id="09ec0-105">Description</span></span>

<span data-ttu-id="09ec0-106">Zaškrtávací políčko **Uložit na mou další platbu** políčko se nezobrazí v části **Způsob platby** na stránce pokladny webu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="09ec0-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="09ec0-107">Následující obrázek ukazuje příklad stránky pokladny, která obsahuje zaškrtávacího políčka **Uložit pro mou další platbu**.</span><span class="sxs-lookup"><span data-stu-id="09ec0-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Zaškrtávací políčko Uložit pro mou další platbu v modulu Platba](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="09ec0-109">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="09ec0-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="09ec0-110">Ověřte, zda je Konektor platby Dynamics 365 pro Adyen správně nakonfigurován v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="09ec0-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="09ec0-111">K ověření, zda je Konektor platby Dynamics 365 pro Adyen správně nakonfigurován v centrále Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="09ec0-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="09ec0-112">Přejděte na **Retail a Commerce \> Kanály \> Online obchody**.</span><span class="sxs-lookup"><span data-stu-id="09ec0-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="09ec0-113">Vyberte online obchod.</span><span class="sxs-lookup"><span data-stu-id="09ec0-113">Select the online store.</span></span>
1. <span data-ttu-id="09ec0-114">Na kartě s náhledem **Platební účty** zkontrolujte, že pole **Povolit ukládání platebních údajů v elektronickém obchodování** je nastaveno na **True**.</span><span class="sxs-lookup"><span data-stu-id="09ec0-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Povolení ukládání platebních údajů v poli elektronického obchodu v centrále Commerce](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="09ec0-116">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="09ec0-116">Additional resources</span></span>

[<span data-ttu-id="09ec0-117">Platební modul</span><span class="sxs-lookup"><span data-stu-id="09ec0-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="09ec0-118">Úspora nástrojů online plateb s konektorem Adyen</span><span class="sxs-lookup"><span data-stu-id="09ec0-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)

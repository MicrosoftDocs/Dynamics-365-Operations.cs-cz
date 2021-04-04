---
title: Platby jsou automaticky vypořádány před fakturací nebo odesláním objednávek
description: Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když je platba vypořádána na portálu Adyen ihned po zadání objednávky, přestože prodejní objednávka nebyla fakturována nebo odeslána.
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
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585231"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="0f0a2-103">Platby jsou automaticky vypořádány před fakturací nebo odesláním objednávek</span><span class="sxs-lookup"><span data-stu-id="0f0a2-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f0a2-104">Toto téma poskytuje pokyny pro řešení potíží, které mohou pomoci, když je platba vypořádána na portálu Adyen ihned po zadání objednávky, přestože prodejní objednávka nebyla fakturována nebo odeslána.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="0f0a2-105">popis</span><span class="sxs-lookup"><span data-stu-id="0f0a2-105">Description</span></span>

<span data-ttu-id="0f0a2-106">Platba je vypořádána na portálu Adyen ihned po zadání objednávky, přestože prodejní objednávka nebyla fakturována nebo odeslána.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="0f0a2-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="0f0a2-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="0f0a2-108">Konfigurace ručního snímání pro platby elektronickým obchodem na portálu Adyen</span><span class="sxs-lookup"><span data-stu-id="0f0a2-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="0f0a2-109">Ke konfiguraci ručního snímání pro platby elektronickým obchodem na portálu Adyen postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="0f0a2-110">Přihlaste se do portálu Adyen.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="0f0a2-111">V pravém horním rohu vyberte svůj účet obchodníka pro kanál elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="0f0a2-112">Na horním navigačním panelu vyberte **Účet** a potom vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="0f0a2-113">V poli **Zachycení zpoždění** vyberte **ruční**.</span><span class="sxs-lookup"><span data-stu-id="0f0a2-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Nastavení Zachycení zpoždění na portálu Adyen](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="0f0a2-115">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="0f0a2-115">Additional resources</span></span>

[<span data-ttu-id="0f0a2-116">Zachycení platby Adyen</span><span class="sxs-lookup"><span data-stu-id="0f0a2-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="0f0a2-117">Platební konektor Dynamics 365 pro Adyen</span><span class="sxs-lookup"><span data-stu-id="0f0a2-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="0f0a2-118">Nastavení konektoru plateb Adyen pro Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0f0a2-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
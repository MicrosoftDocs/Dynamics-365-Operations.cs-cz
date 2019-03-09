---
title: Vrácení položek napříč vícero objednávkami odběratele a fakturami
description: Toto téma popisuje funkci, která umožňuje vrácení napříč vícero objednávkami odběratele a fakturami v Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2019
ms.locfileid: "373061"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="64bef-103">Vrácení položek napříč vícero objednávkami odběratele a fakturami</span><span class="sxs-lookup"><span data-stu-id="64bef-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="64bef-104">V aplikaci Dynamics 365 for Finance and Operations verze 10.0 lze provést vrácení napříč vícero objednávkami a fakturami, zatímco ve verzích předcházejících verzi 10.0 mohla být vrácení zpracovávána pouze pomocí jedné faktury současně.</span><span class="sxs-lookup"><span data-stu-id="64bef-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="64bef-105">Konfigurace aplikace Retail pro podporu vrácení napříč vícero objednávkami a fakturami</span><span class="sxs-lookup"><span data-stu-id="64bef-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="64bef-106">Přejděte na **Parametry maloobchodu \> Objednávky odběratele**.</span><span class="sxs-lookup"><span data-stu-id="64bef-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="64bef-107">Zapněte parametr **Povolit vrácení pro více objednávek**.</span><span class="sxs-lookup"><span data-stu-id="64bef-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="64bef-108">Zpracování vracení</span><span class="sxs-lookup"><span data-stu-id="64bef-108">Process returns</span></span>

<span data-ttu-id="64bef-109">Poté, co je zapnut tento parametr a změny se synchronizují do obchodů, pokladník v obchodě může zvolit více prodejních objednávek pro odběratele k vrácení.</span><span class="sxs-lookup"><span data-stu-id="64bef-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="64bef-110">Když jsou zvoleny objednávky, zobrazí se seznam všech vratných produktů napříč všemi fakturami pro objednávky.</span><span class="sxs-lookup"><span data-stu-id="64bef-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="64bef-111">Pokladník může poté zvolit produkty, které mají být vráceny.</span><span class="sxs-lookup"><span data-stu-id="64bef-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="64bef-112">Pro všechny zvolené produkty bude vytvořena jediná vratka.</span><span class="sxs-lookup"><span data-stu-id="64bef-112">A single return order will be created for all the selected products.</span></span>
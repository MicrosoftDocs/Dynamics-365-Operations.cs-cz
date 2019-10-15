---
title: Vrácení položek napříč vícero objednávkami odběratele a fakturami
description: Toto téma popisuje funkci, která umožňuje vrácení napříč vícero objednávkami odběratele a fakturami v Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
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
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017982"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="8ea21-103">Vrácení položek napříč vícero objednávkami odběratele a fakturami</span><span class="sxs-lookup"><span data-stu-id="8ea21-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="8ea21-104">Vrácení lze provést napříč vícero objednávkami a fakturami.</span><span class="sxs-lookup"><span data-stu-id="8ea21-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="8ea21-105">Konfigurace aplikace Retail pro podporu vrácení napříč vícero objednávkami a fakturami</span><span class="sxs-lookup"><span data-stu-id="8ea21-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="8ea21-106">Přejděte na **Parametry maloobchodu \> Objednávky odběratele**.</span><span class="sxs-lookup"><span data-stu-id="8ea21-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="8ea21-107">Zapněte parametr **Povolit vrácení pro více objednávek**.</span><span class="sxs-lookup"><span data-stu-id="8ea21-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="8ea21-108">Zpracování vracení</span><span class="sxs-lookup"><span data-stu-id="8ea21-108">Process returns</span></span>

<span data-ttu-id="8ea21-109">Poté, co je zapnut tento parametr a změny se synchronizují do obchodů, pokladník v obchodě může zvolit více prodejních objednávek pro odběratele k vrácení.</span><span class="sxs-lookup"><span data-stu-id="8ea21-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="8ea21-110">Když jsou zvoleny objednávky, zobrazí se seznam všech vratných produktů napříč všemi fakturami pro objednávky.</span><span class="sxs-lookup"><span data-stu-id="8ea21-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="8ea21-111">Pokladník může poté zvolit produkty, které mají být vráceny.</span><span class="sxs-lookup"><span data-stu-id="8ea21-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="8ea21-112">Pro všechny zvolené produkty bude vytvořena jediná vratka.</span><span class="sxs-lookup"><span data-stu-id="8ea21-112">A single return order will be created for all the selected products.</span></span>

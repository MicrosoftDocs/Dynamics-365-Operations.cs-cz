---
title: Vrácení položek napříč vícero objednávkami odběratele a fakturami
description: Toto téma popisuje funkci, která umožňuje vrácení napříč vícero objednávkami odběratele a fakturami v Dynamics 365 Commerce.
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
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004451"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="ef1b7-103">Vrácení položek napříč vícero objednávkami odběratele a fakturami</span><span class="sxs-lookup"><span data-stu-id="ef1b7-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="ef1b7-104">Vrácení lze provést napříč vícero objednávkami a fakturami.</span><span class="sxs-lookup"><span data-stu-id="ef1b7-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="ef1b7-105">Konfigurace aplikace Commerce pro podporu vrácení napříč vícero objednávkami a fakturami</span><span class="sxs-lookup"><span data-stu-id="ef1b7-105">Configure Commerce to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="ef1b7-106">Přejděte na **Parametry obchodu \> Objednávky odběratele**.</span><span class="sxs-lookup"><span data-stu-id="ef1b7-106">Go to **Commerce parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="ef1b7-107">Zapněte parametr **Povolit vrácení pro více objednávek**.</span><span class="sxs-lookup"><span data-stu-id="ef1b7-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="ef1b7-108">Zpracování vracení</span><span class="sxs-lookup"><span data-stu-id="ef1b7-108">Process returns</span></span>

<span data-ttu-id="ef1b7-109">Poté, co je zapnut tento parametr a změny se synchronizují do obchodů, pokladník v obchodě může zvolit více prodejních objednávek pro odběratele k vrácení.</span><span class="sxs-lookup"><span data-stu-id="ef1b7-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="ef1b7-110">Když jsou zvoleny objednávky, zobrazí se seznam všech vratných produktů napříč všemi fakturami pro objednávky.</span><span class="sxs-lookup"><span data-stu-id="ef1b7-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="ef1b7-111">Pokladník může poté zvolit produkty, které mají být vráceny.</span><span class="sxs-lookup"><span data-stu-id="ef1b7-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="ef1b7-112">Pro všechny zvolené produkty bude vytvořena jediná vratka.</span><span class="sxs-lookup"><span data-stu-id="ef1b7-112">A single return order will be created for all the selected products.</span></span>

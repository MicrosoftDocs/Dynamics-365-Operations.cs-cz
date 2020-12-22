---
title: Vrácení položek napříč vícero objednávkami odběratele a fakturami
description: Toto téma popisuje funkci, která umožňuje vrácení napříč vícero objednávkami odběratele a fakturami v Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
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
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458590"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="1f1ad-103">Vrácení položek napříč vícero objednávkami odběratele a fakturami</span><span class="sxs-lookup"><span data-stu-id="1f1ad-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="1f1ad-104">Tento článek popisuje dvě funkce, které optimalizují vratky zákazníků na více fakturách.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="1f1ad-105">Povolit refundace přes více záznamů</span><span class="sxs-lookup"><span data-stu-id="1f1ad-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="1f1ad-106">Tato funkce umožňuje více propojených refundací proti stejné objednávce zákazníka.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="1f1ad-107">Přejděte do pracovního prostoru **Správa funkcí** a vyhledejte možnost **Povolit refundace na vícero záznamech**.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="1f1ad-108">Vyberte **Povolit refundace na vícero objednávkách** a poté klikněte na **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="1f1ad-109">Povolení správného výpočtu daně pro vrácení s částečným množstvím</span><span class="sxs-lookup"><span data-stu-id="1f1ad-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="1f1ad-110">Tato funkce zajišťuje, že při vrácení objednávky s použitím více faktur se daně nakonec budou rovnat původně účtované částce daně.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="1f1ad-111">Přejděte do pracovního prostoru **Správa funkcí** a vyhledejte možnost **Povolení správného výpočtu daně pro vrácení s částečným množstvím**.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="1f1ad-112">Vyberte **Povolení správného výpočtu daně pro vrácení s částečným množstvím** a poté klikněte na **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="1f1ad-113">Zpracování vracení</span><span class="sxs-lookup"><span data-stu-id="1f1ad-113">Process returns</span></span>

<span data-ttu-id="1f1ad-114">Poté, co jsou zapnuty tyto funkce a změny se synchronizují do obchodů, pokladník v obchodě může zvolit více prodejních objednávek pro odběratele k vrácení.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="1f1ad-115">Když jsou zvoleny objednávky, zobrazí se seznam všech vratných produktů napříč všemi fakturami pro objednávky.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="1f1ad-116">Pokladník může poté zvolit produkty, které mají být vráceny.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="1f1ad-117">Pro všechny zvolené produkty bude vytvořena jediná vratka.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="1f1ad-118">Pokud je objednávka plně vrácena, částka daní vrácená zákazníkovi se bude rovnat částce původně účtované daně.</span><span class="sxs-lookup"><span data-stu-id="1f1ad-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>


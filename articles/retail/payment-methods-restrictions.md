---
title: Omezení platebních metod pro vrácení bez příjemky
description: Toto téma popisuje, jak lze určité typy plateb omezit pro refundaci, pokud jsou vrácení provedená bez příjemky.
author: rapraj
manager: AnnBe
ms.date: 013/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 6e2c32aae06ce7bbdde30809d7a197f43b856af1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564335"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="d799a-103">Omezení platebních metod pro vrácení bez příjemky</span><span class="sxs-lookup"><span data-stu-id="d799a-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d799a-104">Každý typ platby, kterou prodejce přijímá, musí být nakonfigurován při nastavení systému.</span><span class="sxs-lookup"><span data-stu-id="d799a-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="d799a-105">Toto téma popisuje, jak lze určité typy plateb omezit pro refundaci, pokud jsou vrácení provedená bez příjemky.</span><span class="sxs-lookup"><span data-stu-id="d799a-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="d799a-106">Nastavení metod platby</span><span class="sxs-lookup"><span data-stu-id="d799a-106">Set up payment methods</span></span>

<span data-ttu-id="d799a-107">K nastavení způsobů platby je třeba dokončit následující úlohy.</span><span class="sxs-lookup"><span data-stu-id="d799a-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="d799a-108">Vytvořte metody platby, které jsou přijímány v rámci celé organizace.</span><span class="sxs-lookup"><span data-stu-id="d799a-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="d799a-109">Vytvoření celoorganizačních typů karet a čísel karet.</span><span class="sxs-lookup"><span data-stu-id="d799a-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="d799a-110">Budou-li přijímány kreditní nebo debetní karty, je třeba vytvořit jeden typ úhrady pro karty a poté vytvořit celoorganizační typy karet a čísla karet.</span><span class="sxs-lookup"><span data-stu-id="d799a-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="d799a-111">Nastavte platební metody obchodu.</span><span class="sxs-lookup"><span data-stu-id="d799a-111">Set up store payment methods.</span></span> <span data-ttu-id="d799a-112">Přiřaďte způsoby plateb ke každému obchodu a poté zadejte konkrétní nastavení pro každý způsob platby.</span><span class="sxs-lookup"><span data-stu-id="d799a-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="d799a-113">Nastavte karetní platební metody pro obchody.</span><span class="sxs-lookup"><span data-stu-id="d799a-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="d799a-114">Pro jakékoli metody platby kartou, které obchod přijímá, dokončete nastavení karty.</span><span class="sxs-lookup"><span data-stu-id="d799a-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="d799a-115">![Nastavení maloobchodu](media/NoReceiptReturns1.png "Nastavení maloobchodu")</span><span class="sxs-lookup"><span data-stu-id="d799a-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="d799a-116">Omezení platebních metod pro vrácení bez příjemky</span><span class="sxs-lookup"><span data-stu-id="d799a-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="d799a-117">Pro každý způsob platby obchodu nastavte na stránce **Řízení maloobchodu** pod položkou **Bez vratky** možnost **Omezit pro refundace bez příjemky** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d799a-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="d799a-118">Výchozí hodnota přepínače je **Ne**, což zaručuje, že metoda platby pro refundaci je povolena.</span><span class="sxs-lookup"><span data-stu-id="d799a-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="d799a-119">Když je možnost **Omezit pro refundace bez příjemky** nastavena na **Ano**, zvolená metoda platby nebude pro refundace povolena.</span><span class="sxs-lookup"><span data-stu-id="d799a-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="d799a-120">![Způsob platby maloobchodu](media/NoReceiptReturns3.png "Způsob platby maloobchodu")</span><span class="sxs-lookup"><span data-stu-id="d799a-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="d799a-121">Pokud pokladník vybere způsob platby, který je omezen pro refundaci bez příjemky, zobrazí se zpráva pro ověření přijatelných způsobů platby.</span><span class="sxs-lookup"><span data-stu-id="d799a-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="d799a-122">![Přijatelné způsoby platby](media/NoReceiptReturns4.png "Přijatelné způsoby platby")</span><span class="sxs-lookup"><span data-stu-id="d799a-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="d799a-123">Pokud má transakce vrácení s příjemkou i bez příjemky, podmínky omezení nebudou vynuceny, protože transakce bude workflow vrácení s příjemkou.</span><span class="sxs-lookup"><span data-stu-id="d799a-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 


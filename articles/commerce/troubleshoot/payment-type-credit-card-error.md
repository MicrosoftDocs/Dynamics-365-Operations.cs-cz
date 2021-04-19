---
title: Chyba Typ platby musí být kreditní karta na stránce prodejní objednávky
description: Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se po synchronizaci objednávky zobrazí chybová zpráva na stránce prodejní objednávky.
author: Reza-Assadi
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
ms.openlocfilehash: eabc64acc74645c7e6c7c4ab5794ed9fdb9dc997
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801668"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="6f6a1-103">Chyba „Typ platby musí být kreditní karta“ na stránce prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="6f6a1-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f6a1-104">Toto téma poskytuje pokyny pro řešení potíží, které vám mohou pomoci, když se po synchronizaci objednávky zobrazí chybová zpráva na stránce prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="6f6a1-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="6f6a1-105">popis</span><span class="sxs-lookup"><span data-stu-id="6f6a1-105">Description</span></span>

<span data-ttu-id="6f6a1-106">Když otevřete stránku prodejní objednávky po synchronizaci objednávky, zobrazí se následující chybová zpráva: „Typ platby musí být kreditní karta, protože bylo zadáno číslo kreditní karty“.</span><span class="sxs-lookup"><span data-stu-id="6f6a1-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Chyba typ platby musí být kreditní karta](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="6f6a1-108">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="6f6a1-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="6f6a1-109">Nastavení typu platby v centrále Commerce</span><span class="sxs-lookup"><span data-stu-id="6f6a1-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="6f6a1-110">Přejděte do nabídky **Pohledávky \> Nastavení platby \> Platební podmínky**.</span><span class="sxs-lookup"><span data-stu-id="6f6a1-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="6f6a1-111">Na levém navigačním panelu vyberte platební podmínky.</span><span class="sxs-lookup"><span data-stu-id="6f6a1-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="6f6a1-112">V poli **Způsob platby** zkontrolujte, že je vybráno **Kreditní karta**.</span><span class="sxs-lookup"><span data-stu-id="6f6a1-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f6a1-113">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="6f6a1-113">Additional resources</span></span>

[<span data-ttu-id="6f6a1-114">Zaúčtování online prodeje a plateb</span><span class="sxs-lookup"><span data-stu-id="6f6a1-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)

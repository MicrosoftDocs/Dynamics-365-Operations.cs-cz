---
title: Na stránce zadání kreditní karty se při placení zobrazuje chyba
description: Toto téma poskytuje pokyny k řešení potíží, které mohou pomoci, když se nenačte část Platební metoda, a zobrazuje chybovou zprávu.
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
ms.openlocfilehash: d2c5f01d17df79c9b23fd513aaeb5c0605d657e9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801764"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="69e24-103">Na stránce zadání kreditní karty se při placení zobrazuje chyba</span><span class="sxs-lookup"><span data-stu-id="69e24-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69e24-104">Toto téma poskytuje pokyny k řešení potíží, které mohou pomoci, když se nenačte část **Platební metoda**, a zobrazuje chybovou zprávu.</span><span class="sxs-lookup"><span data-stu-id="69e24-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="69e24-105">popis</span><span class="sxs-lookup"><span data-stu-id="69e24-105">Description</span></span>

<span data-ttu-id="69e24-106">Když otevřete stránku pokladny online obchodu, část **Způsob platby** se nenačte a zobrazí se následující chybová zpráva: „Něco se pokazilo.</span><span class="sxs-lookup"><span data-stu-id="69e24-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="69e24-107">Prosím zkuste to znovu později.“</span><span class="sxs-lookup"><span data-stu-id="69e24-107">Please try again later."</span></span>

![Chyba platebního modulu](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="69e24-109">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="69e24-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="69e24-110">Počkejte, než vyprší platnost mezipaměti Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="69e24-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="69e24-111">Nastavení platebních služeb na stránce pokladny internetového obchodu jsou uložena v mezipaměti v jednotce Commerce Scale Unit a jejich zobrazení na webu elektronického obchodování může trvat až 15 minut.</span><span class="sxs-lookup"><span data-stu-id="69e24-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="69e24-112">Tato nastavení platebních služeb zahrnují změny ID obchodního účtu, klíče cloudového API a různá nastavení konfigurace, která souvisí s platební metodou.</span><span class="sxs-lookup"><span data-stu-id="69e24-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69e24-113">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="69e24-113">Additional resources</span></span>

[<span data-ttu-id="69e24-114">Nastavení online kanálu</span><span class="sxs-lookup"><span data-stu-id="69e24-114">Set up an online channel</span></span>](../channel-setup-online.md)

---
title: Nastavení čárových kódů
description: Tento článek popisuje, jak lze používat čárové kódy v aplikaci Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 74a08fc168dd3c41fa501ca8110af899a181e333
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021889"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="f2661-103">Nastavení čárových kódů</span><span class="sxs-lookup"><span data-stu-id="f2661-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2661-104">Tento článek popisuje, jak lze používat čárové kódy v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2661-104">This article describes how to use bar codes in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f2661-105">Čárové kódy slouží pro nákup a prodej produktů, sledování variant produktů a nastavení zákazníků a zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="f2661-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="f2661-106">Čárové kódy slouží také pro vydávání a schvalování kupónů, dárkových poukazů a dobropisů.</span><span class="sxs-lookup"><span data-stu-id="f2661-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="f2661-107">k maloobchodním produktům lze nastavit standardní čárové kódy nebo vlastní, podnikové čárové kódy.</span><span class="sxs-lookup"><span data-stu-id="f2661-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="f2661-108">Produkty mohou mít více čárových kódů.</span><span class="sxs-lookup"><span data-stu-id="f2661-108">Products can have more than one bar code.</span></span> <span data-ttu-id="f2661-109">Například produkt může mít více čárových kódů, pokud pochází od různých výrobců, nebo pokud má varianty, které jsou založeny na velikosti, stylu či barvě.</span><span class="sxs-lookup"><span data-stu-id="f2661-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="f2661-110">Čárové kódy mohou obsahovat hmotnost nebo cenu produktu.</span><span class="sxs-lookup"><span data-stu-id="f2661-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="f2661-111">Masky čárových kódů jsou šablony, které slouží k vytvoření čárových kódů.</span><span class="sxs-lookup"><span data-stu-id="f2661-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="f2661-112">Přiřadíte-li každé kombinaci variant jedinečný čárový kód, program po skenování čárového kódu na registrační pokladně vyhledá variantu produktu, která je prodávána.</span><span class="sxs-lookup"><span data-stu-id="f2661-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="f2661-113">Díky tomu lze také shromažďovat a zobrazovat statistické údaje o prodeji podle variant.</span><span class="sxs-lookup"><span data-stu-id="f2661-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="f2661-114">Každé skupině velikostí, barev a stylů lze přiřadit jedinečné číslo, které v čárovém kódu identifikuje skupinu.</span><span class="sxs-lookup"><span data-stu-id="f2661-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="f2661-115">Retail pomocí masky čárového kódu automaticky generuje čárové kódy pro každou kombinaci variant.</span><span class="sxs-lookup"><span data-stu-id="f2661-115">Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="f2661-116">To může být užitečné v případě, že je k dispozici mnoho velikostí, barev a stylů, protože počet kombinací s každým přidaným kódem varianty značně vzrůstá.</span><span class="sxs-lookup"><span data-stu-id="f2661-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="f2661-117">Pokud tato funkce není použita, musí být čárové kódy ručně přiděleny ke každé kombinaci představující variantu produktu.</span><span class="sxs-lookup"><span data-stu-id="f2661-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="f2661-118">Čárové kódy lze vytvářet ručně nebo automaticky.</span><span class="sxs-lookup"><span data-stu-id="f2661-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="f2661-119">Pokud chcete vytvořit čárové kódy, proveďte následující úlohy v pořadí, ve kterém jsou uvedeny.</span><span class="sxs-lookup"><span data-stu-id="f2661-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="f2661-120">[Nastavení znaků masky čárového kódu](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="f2661-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="f2661-121">[Nastavení masek čárových kódů](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="f2661-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="f2661-122">Konfigurace nastavení čárových kódů.</span><span class="sxs-lookup"><span data-stu-id="f2661-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="f2661-123">Vytváření čárových kódů pro produkty.</span><span class="sxs-lookup"><span data-stu-id="f2661-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2661-124">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f2661-124">Additional resources</span></span>

[<span data-ttu-id="f2661-125">Nastavení masek čárových kódů</span><span class="sxs-lookup"><span data-stu-id="f2661-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)

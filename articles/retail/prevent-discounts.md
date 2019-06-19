---
title: Možnosti zabránění slevám pro maloobchodní produkty
description: Existují různé důvody, proč maloobchodní prodejci mohou chtít, aby na některé produkty neplatila sleva, buď v rámci promoakce nebo během prodeje v POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 64f54c1a63706ccd9225d47df96ffc3f88cf3332
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606911"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="c8979-103">Možnosti zabránění slevám pro maloobchodní produkty</span><span class="sxs-lookup"><span data-stu-id="c8979-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8979-104">Existují různé důvody, proč maloobchodní prodejci mohou chtít, aby na některé produkty neplatila sleva, buď v rámci promoakce nebo během prodeje v POS.</span><span class="sxs-lookup"><span data-stu-id="c8979-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="c8979-105">Následující možnosti, které se nachází na kartě **Maloobchod** vydaných produktů, umožní nakonfigurování výrobku tak, aby se na něj nevztahovaly všechny nebo pouze manuální slevy.</span><span class="sxs-lookup"><span data-stu-id="c8979-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="c8979-106">Nastavení lze také určit na úrovni kategorie z hierarchie kategorií maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="c8979-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

- <span data-ttu-id="c8979-107">**Zabránit všem selvám** - Výběrem této volby můžete zabránit, aby se na tento produkt aplikoval jakýkoliv typ slevy.</span><span class="sxs-lookup"><span data-stu-id="c8979-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="c8979-108">To zahrnuje promoakce, jako například kombinační slevy, množstevní a mezní slevy, jakož i manuální slevy řádku a transakce použité při prodeji uživatelem POS.</span><span class="sxs-lookup"><span data-stu-id="c8979-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="c8979-109">**Zabránit ručním slevám** - Tuto možnost vyberte pouze pro zabránění slev řádku nebo transakce použitým při prodeji uživatelem POS.</span><span class="sxs-lookup"><span data-stu-id="c8979-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="c8979-110">Produkty s touto zvolenou možností mají stále nárok na promoakce, jako jsou například kombinační, množstevní a mezní slevy.</span><span class="sxs-lookup"><span data-stu-id="c8979-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="c8979-111">Tato nastavení neomezují operaci přepisu ceny, protože se nastaví základní cena, se kterou se nenakládá jako se slevou.</span><span class="sxs-lookup"><span data-stu-id="c8979-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="c8979-112">[![Pole zabránění slev](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="c8979-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>

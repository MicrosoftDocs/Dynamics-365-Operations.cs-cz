---
title: Možnosti zabránění slevám pro maloobchodní produkty
description: Existují různé důvody, proč maloobchodní prodejci mohou chtít, aby na některé produkty neplatila sleva, buď v rámci promoakce nebo během prodeje v POS.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ddf3834057c89f5a091f09412183ca79540225fc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802880"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="0fed5-103">Možnosti zabránění slevám pro maloobchodní produkty</span><span class="sxs-lookup"><span data-stu-id="0fed5-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0fed5-104">Existují různé důvody, proč maloobchodní prodejci mohou chtít, aby na některé produkty neplatila sleva, buď v rámci promoakce nebo během prodeje v POS.</span><span class="sxs-lookup"><span data-stu-id="0fed5-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="0fed5-105">Následující možnosti, které se nachází na kartě **Velkoobchod** vydaných produktů, umožní nakonfigurování výrobku tak, aby se na něj nevztahovaly všechny nebo pouze manuální slevy.</span><span class="sxs-lookup"><span data-stu-id="0fed5-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="0fed5-106">Nastavení lze také určit na úrovni kategorie z hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="0fed5-106">The settings can also be specified at the category level from the category hierarchy.</span></span>

- <span data-ttu-id="0fed5-107">**Zabránit všem selvám** - Výběrem této volby můžete zabránit, aby se na tento produkt aplikoval jakýkoliv typ slevy.</span><span class="sxs-lookup"><span data-stu-id="0fed5-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="0fed5-108">To zahrnuje promoakce, jako například kombinační slevy, množstevní a mezní slevy, jakož i manuální slevy řádku a transakce použité při prodeji uživatelem POS.</span><span class="sxs-lookup"><span data-stu-id="0fed5-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="0fed5-109">**Zabránit ručním slevám** - Tuto možnost vyberte pouze pro zabránění slev řádku nebo transakce použitým při prodeji uživatelem POS.</span><span class="sxs-lookup"><span data-stu-id="0fed5-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="0fed5-110">Produkty s touto zvolenou možností mají stále nárok na promoakce, jako jsou například kombinační, množstevní a mezní slevy.</span><span class="sxs-lookup"><span data-stu-id="0fed5-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="0fed5-111">Tato nastavení neomezují operaci přepisu ceny, protože se nastaví základní cena, se kterou se nenakládá jako se slevou.</span><span class="sxs-lookup"><span data-stu-id="0fed5-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="0fed5-112">[![Pole zabránění slev](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="0fed5-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
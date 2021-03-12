---
title: Sestavy maloobchodních cen
description: Toto téma obsahuje přehled funkce sestavy cen, kterou lze použít k zobrazení nadcházejících cenových změn u roztříděných produktů.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: e14b029a1420eda6af6e83392f295a071a29842a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972423"
---
# <a name="retail-price-reports"></a><span data-ttu-id="27eb5-103">Sestavy maloobchodních cen</span><span class="sxs-lookup"><span data-stu-id="27eb5-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="27eb5-104">S cílem poskytnout konkurenční ceny pro své zákazníky maloobchodní prodejci často mění ceny produktů.</span><span class="sxs-lookup"><span data-stu-id="27eb5-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="27eb5-105">Manažeři obchodu vyžadují možnost snadný přístup k nedávným nebo nadcházejícím cenovým změnám, aby mohly plánovat požadovaným zdrojům aktualizace cenových štítků zobrazených na policích obchodu.</span><span class="sxs-lookup"><span data-stu-id="27eb5-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="27eb5-106">S verzí 10.0 aplikace Retail může manažer obchodu otevřít sestavu **Cena** přechodem na **Všechny obchody \> Obchod \> Sestava cen** a zobrazením aktualizovaných cen pro produkty přidružené k obchodu.</span><span class="sxs-lookup"><span data-stu-id="27eb5-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="27eb5-107">Pro povolení sestavy cen musí být zapnut parametr **Povolit sestavu cen pro obchod**.</span><span class="sxs-lookup"><span data-stu-id="27eb5-107">To enable the price report, the **Enable price report for store** parameter must be turned on.</span></span> <span data-ttu-id="27eb5-108">Tento parametr se nachází na kartě **Parametry velkoobchodu \> Slevy \> Různé**. Otevření stránky **Sestava cen** zobrazí dialogové okno s různými konfiguracemi.</span><span class="sxs-lookup"><span data-stu-id="27eb5-108">This parameter is located on the **Commerce parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="27eb5-109">Dostupné konfigurace jsou uvedené níže.</span><span class="sxs-lookup"><span data-stu-id="27eb5-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="27eb5-110">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="27eb5-110">Configuration</span></span> | <span data-ttu-id="27eb5-111">popis</span><span class="sxs-lookup"><span data-stu-id="27eb5-111">Description</span></span> |
|---|---|
| <span data-ttu-id="27eb5-112">Od data / Do data</span><span class="sxs-lookup"><span data-stu-id="27eb5-112">From date / To date</span></span>| <span data-ttu-id="27eb5-113">Rozsah dat, pro který se má vygenerovat sestava cen.</span><span class="sxs-lookup"><span data-stu-id="27eb5-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="27eb5-114">Doba trvání je nyní omezena na 7 dnů.</span><span class="sxs-lookup"><span data-stu-id="27eb5-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="27eb5-115">Kanál</span><span class="sxs-lookup"><span data-stu-id="27eb5-115">Channel</span></span>| <span data-ttu-id="27eb5-116">Obchod, pro který se má vygenerovat sestava cen.</span><span class="sxs-lookup"><span data-stu-id="27eb5-116">The store for which the price report should be generated.</span></span> |
| <span data-ttu-id="27eb5-117">Zobrazit produkty s dostupnými zásobami</span><span class="sxs-lookup"><span data-stu-id="27eb5-117">Display products with available inventory</span></span>| <span data-ttu-id="27eb5-118">Nastavení na **Ano** zobrazí ceny pouze pro ty produkty, které mají momentálně dostupné fyzické zásoby v obchodě.</span><span class="sxs-lookup"><span data-stu-id="27eb5-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="27eb5-119">Zobrazení cen pro varianty</span><span class="sxs-lookup"><span data-stu-id="27eb5-119">Display prices for variants</span></span> | <span data-ttu-id="27eb5-120">Nastavení na **Ano** zobrazí ceny variant spolu s hlavními produkty.</span><span class="sxs-lookup"><span data-stu-id="27eb5-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="27eb5-121">Tuto možnost je třeba **zapnout**, pokud máte ceny specifické pro varianty, protože počet řádků strmě roste.</span><span class="sxs-lookup"><span data-stu-id="27eb5-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="27eb5-122">V budoucích verzích povolíme ceny založené na dimenzích, aby manažer obchodu mohl vybrat dimenze, pro které by se měly ceny zobrazovat.</span><span class="sxs-lookup"><span data-stu-id="27eb5-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="27eb5-123">Zobrazení produktů se změnami cen</span><span class="sxs-lookup"><span data-stu-id="27eb5-123">Display products with price changes</span></span> | <span data-ttu-id="27eb5-124">Nastavení na **Ano** zobrazí ceny pouze pro ta data, kdy byla cena změněna.</span><span class="sxs-lookup"><span data-stu-id="27eb5-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="27eb5-125">Cena pro *jeden den před* datem vybraným v možnosti **Od data** se zobrazí vždy, aby manažer ochodu mohl snadno určit produkty, u kterých se nezměnily ceny po celou zvolenou dobu. Rovněž mohou zobrazit aktuální cenu.</span><span class="sxs-lookup"><span data-stu-id="27eb5-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="27eb5-126">Po vygenerování sestavy lze stáhnout soubor aplikace Excel pro všechny další potřeby filtrování.</span><span class="sxs-lookup"><span data-stu-id="27eb5-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="27eb5-127">Sestavu cen lze také použít ke kontrole historických cen produktů pro minulá data.</span><span class="sxs-lookup"><span data-stu-id="27eb5-127">The price report can also be used to check the historical prices of products for past dates.</span></span>

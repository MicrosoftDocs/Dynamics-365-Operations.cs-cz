---
title: Synchronizace s cenovým modulem Dynamics 365 Supply Chain Management na požádání
description: V tomto tématu je popsán způsob použití cenového modulu v aplikaci Microsoft Dynamics 365 Supply Chain Management z Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 740ae20704abd9c59f64c2c7622fa96d65dccb1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4450603"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="2d73a-103">Synchronizace s cenovým modulem Dynamics 365 Supply Chain Management na požádání</span><span class="sxs-lookup"><span data-stu-id="2d73a-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="2d73a-104">Microsoft Dynamics 365 Supply Chain Management obsahuje cenový modul, který zpracovává obchodní smlouvy, ceníky, zákaznické věrnostní programy, promoakce a slevy.</span><span class="sxs-lookup"><span data-stu-id="2d73a-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="2d73a-105">Cenový modul používá složitá pravidla k určení nejvhodnější ceny pro danou nabídku nebo objednávku.</span><span class="sxs-lookup"><span data-stu-id="2d73a-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="2d73a-106">Při použití dvojitého zápisu, v aplikaci Dynamics 365 Sales použijete buď cenovou kalkulaci nebo cenový modul z Dynamics 365 Supply Chain Management na stránkách Nabídka nebo Objednávka.</span><span class="sxs-lookup"><span data-stu-id="2d73a-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="2d73a-107">Použití cenového modulu ze Supply Chain Management v Sales</span><span class="sxs-lookup"><span data-stu-id="2d73a-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="2d73a-108">V Sales přejděte na **Prodej \> Objednávky**.</span><span class="sxs-lookup"><span data-stu-id="2d73a-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="2d73a-109">Volbo **Nová** vytvořte novou objednávku nebo vyberte existující objednávku v seznamu **Moje objednávky**.</span><span class="sxs-lookup"><span data-stu-id="2d73a-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="2d73a-110">Přidejte novou řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="2d73a-110">Add a new order line.</span></span>
4. <span data-ttu-id="2d73a-111">Pokud vytváříte novou objednávku, vyberte v podokně Akce možnost **Ocenit objednávku**.</span><span class="sxs-lookup"><span data-stu-id="2d73a-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="2d73a-112">Pokud aktualizujete existující objednávku, vyberte v podokně Akce možnost **Přepočítat**.</span><span class="sxs-lookup"><span data-stu-id="2d73a-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="2d73a-113">Automaticky budou vyplněna následující pole:</span><span class="sxs-lookup"><span data-stu-id="2d73a-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="2d73a-114">Rozepsaná částka</span><span class="sxs-lookup"><span data-stu-id="2d73a-114">Detail Amount</span></span>
    + <span data-ttu-id="2d73a-115">Sleva %</span><span class="sxs-lookup"><span data-stu-id="2d73a-115">Discount %</span></span>
    + <span data-ttu-id="2d73a-116">Sleva</span><span class="sxs-lookup"><span data-stu-id="2d73a-116">Discount</span></span>
    + <span data-ttu-id="2d73a-117">Částka bez přepravného</span><span class="sxs-lookup"><span data-stu-id="2d73a-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="2d73a-118">Částka s přepravným</span><span class="sxs-lookup"><span data-stu-id="2d73a-118">Freight Amount</span></span>
    + <span data-ttu-id="2d73a-119">Celková daň</span><span class="sxs-lookup"><span data-stu-id="2d73a-119">Total Tax</span></span>
    + <span data-ttu-id="2d73a-120">Celková částka</span><span class="sxs-lookup"><span data-stu-id="2d73a-120">Total Amount</span></span>
    
5. <span data-ttu-id="2d73a-121">Chcete-li zajistit, aby systém při výpočtu ceny přihlížel k obchodním a prodejním smlouvám, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2d73a-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="2d73a-122">Přejděte k prostředí Supply Chain Management .</span><span class="sxs-lookup"><span data-stu-id="2d73a-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="2d73a-123">Přejděte na **Pohledávky \> Nastavení \> Parametry pohledávek**.</span><span class="sxs-lookup"><span data-stu-id="2d73a-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="2d73a-124">Na vedlejším navigačním panelu vyberte kartu **Ceny**.</span><span class="sxs-lookup"><span data-stu-id="2d73a-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="2d73a-125">Na pebné záložce **Hodnocení obchodní smlouvy** zrušte zaškrtnutí políčka **Ruční zadání**.</span><span class="sxs-lookup"><span data-stu-id="2d73a-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="2d73a-126">Jak to funguje</span><span class="sxs-lookup"><span data-stu-id="2d73a-126">How it works</span></span>

<span data-ttu-id="2d73a-127">Když v Sales vyberete **Ocenit objednávku**, pro přidruženou prodejní objednávku je volána funkce **Součty** na kartě **Prodejní objednávka \> Zobrazení** v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2d73a-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="2d73a-128">Hodnoty celkové výše objednávky v Sales se používají k vyplnění odpovídajících polí v modulu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2d73a-128">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="2d73a-129">Při výpočtu celkové částky prodejní objednávky v modulu Supply Chain Management vyhodnotí výpočet existující obchodní smlouvy a prodejní smlouvy pro zákazníka a produkty, které jsou uvedeny v prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="2d73a-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="2d73a-130">Tyto informace se použijí k výpočtu součtů.</span><span class="sxs-lookup"><span data-stu-id="2d73a-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="2d73a-131">Když je vybrána možnost **Ocenit objednávku**, Sales automaticky převezme veškeré nastavení, které bylo provedeno v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2d73a-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="2d73a-132">Omezení</span><span class="sxs-lookup"><span data-stu-id="2d73a-132">Limitations</span></span>

<span data-ttu-id="2d73a-133">Při vyplnění polí v Sales platí následující omezení:</span><span class="sxs-lookup"><span data-stu-id="2d73a-133">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="2d73a-134">Nastavení nákladů a přidělení nákladů v Supply Chain Management není replikováno v Sales.</span><span class="sxs-lookup"><span data-stu-id="2d73a-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="2d73a-135">Cenová kalkulace nebere v potaz zvláštní maloobchodní ceny, které jsou zadány v poli **Maloobchodní síť** na stránce řádku prodejní objednávky v modulu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2d73a-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="2d73a-136">Slevy, které jsou definovány v oddílu **Správa obchodních náhrad** v modulu Supply Chain Management, se neberou v úvahu.</span><span class="sxs-lookup"><span data-stu-id="2d73a-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>

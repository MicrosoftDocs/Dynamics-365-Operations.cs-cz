---
title: Konfigurace a zpracování výměny u vratek
description: Toto téma vysvětluje, jak nakonfigurovat výměnu u vratky v aplikaci Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6d7688e78a375bc262b1156c5439c0fff7cd1f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458612"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="a1ffc-103">Konfigurace a zpracování výměny u vratek</span><span class="sxs-lookup"><span data-stu-id="a1ffc-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a1ffc-104">V předchozích verzích aplikace Dynamics 365 Commerce se vrácení proti objednávkám odběratele zpracovávala pomocí dokumentu vratky v modulu Headquarters.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-104">In previous versions of Dynamics 365 Commerce, returns against customer orders were processed by using the return order document in Headquarters.</span></span> <span data-ttu-id="a1ffc-105">Dokument vratky lze však použít pouze pro zpracování produktů, které jsou vráceny.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="a1ffc-106">Vrácené produkty jsou označeny negativním množstvím na řádcích vratky.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="a1ffc-107">Naopak prodej je označen kladným množstvím.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="a1ffc-108">Dokument vratky však nepodporuje kladná množství.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="a1ffc-109">Kvůli této limitaci předchozí verze aplikace nepodporovaly scénáře, kde dochází k výměně produktu pomocí dokumentu vratky.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-109">Because of this limitation, previous versions of the app didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="a1ffc-110">Byla však přidána funkcionality pro podporu scénářů, kde jsou výměny prováděny u vratek.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="a1ffc-111">Commerce nyní používá dokument prodejní objednávky namísto dokumentu vratky pro zpracování těchto typů transakcí.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-111">Commerce now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a><span data-ttu-id="a1ffc-112">Konfigurace aplikace Commerce pro podporu výměn u vratek</span><span class="sxs-lookup"><span data-stu-id="a1ffc-112">Configure Commerce to support exchanges on return orders</span></span>

<span data-ttu-id="a1ffc-113">Postupujte podle těchto kroků pro konfiguraci podpory výměn u vratek.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="a1ffc-114">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="a1ffc-115">Na pevné záložce **Objednávky odběratele** nastavte možnost **Zpracovat vratky jako prodejní objednávky** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="a1ffc-116">Spusťte úlohu **Globální plán distribuce konfigurace** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="a1ffc-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="a1ffc-117">Provedení výměny</span><span class="sxs-lookup"><span data-stu-id="a1ffc-117">Make an exchange</span></span>

<span data-ttu-id="a1ffc-118">Poté, co je systém nakonfigurován podle popisu v předchozí části, uživatel pokladního místa nadále bude vybírat prodejní objednávku nebo prodejní fakturu pro zpracování vratky, jako v předchozích verzích aplikace.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of the app.</span></span> <span data-ttu-id="a1ffc-119">Nicméně když jsou vrácené položky přidány do košíku, uživatel bude moct přidat do košíku nové prodejní řádky.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="a1ffc-120">Pro tyto nové prodejní řádky musí uživatel definovat všechny atributy, které jsou nutné ke zpracování řádku objednávky odběratele.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="a1ffc-121">Tyto atributy zahrnují způsob doručení a místo plnění.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="a1ffc-122">Platba, která je splatná za transakci, bude čistá částka řádků vratky a prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="a1ffc-123">Když je platba za transakci vyrovnána, vratka bude zaúčtována jako dokument prodejní objednávky v Headquarters a systém okamžitě vyfakturuje řádky vratky.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="a1ffc-124">Za účelem lepší viditelnosti různých částek košíku byla ke košíku přidána tři nová pole částek.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="a1ffc-125">Můžete použít návrháře obrazovky a zpřístupnit tato nová pole v uživatelském rozhraní pokladního místa.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="a1ffc-126">**Použitá záloha** – Částka zálohy použitá na transakci, když uživatel provede výdej objednávky odběratele.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="a1ffc-127">Pokud neexistuje přepsání zálohy a je nakonfigurována 10% záloha, částka v tomto poli je 90 % celkové částky objednávky odběratele.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="a1ffc-128">**Vyvézt částku** – Celková částka pro řádky, kde byl způsob doručení nastaven na **Vyvézt** při vytvoření nebo úpravě objednávky odběratele, nebo při výměně objednávky odběratele.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="a1ffc-129">Částka v tomto poli zahrnuje daně a poplatky.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="a1ffc-130">**Částka k vrácení** – Celková částka řádků s negativním množstvím během výměny objednávky odběratele.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="a1ffc-131">Částka v tomto poli zahrnuje daně a poplatky.</span><span class="sxs-lookup"><span data-stu-id="a1ffc-131">The amount in this field includes taxes and charges.</span></span>

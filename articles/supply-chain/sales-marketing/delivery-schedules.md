---
title: "Plány dodávek"
description: "Plány dodávek vám umožňují sledovat množství na řádku objednávky, když pracujete s více dodávkami na jedné prodejní objednávce, prodejní nabídce nebo nákupní objednávce."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ceb568cc223a631f704caf2417f1a3bd56b56288
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="delivery-schedules"></a><span data-ttu-id="dd77b-103">Plány dodávek</span><span class="sxs-lookup"><span data-stu-id="dd77b-103">Delivery schedules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="dd77b-104">Plány dodávek vám umožňují sledovat množství na řádku objednávky, když pracujete s více dodávkami na jedné prodejní objednávce, prodejní nabídce nebo nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="dd77b-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="dd77b-105">Použijte plán dodávek, pokud celkové množství na objednávce nebo řádku nabídky musí být dodáno v podobě vícenásobné expedice.</span><span class="sxs-lookup"><span data-stu-id="dd77b-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="dd77b-106">Řádky dodávky představují jednotlivé dodávky.</span><span class="sxs-lookup"><span data-stu-id="dd77b-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="dd77b-107">Dva nebo více řádků dodávek tvoří jeden plán dodávek.</span><span class="sxs-lookup"><span data-stu-id="dd77b-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="dd77b-108">Řádky dodávky mohou mít jiná data dodání, množství, způsoby dodání a dimenze úložiště, jako například pracoviště a sklad.</span><span class="sxs-lookup"><span data-stu-id="dd77b-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="dd77b-109">**Příklad plánu dodávek**</span><span class="sxs-lookup"><span data-stu-id="dd77b-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="dd77b-110">Celková objednávka (původní řádek objednávky)</span><span class="sxs-lookup"><span data-stu-id="dd77b-110">Total order (original order line)</span></span> | <span data-ttu-id="dd77b-111">600 židlí</span><span class="sxs-lookup"><span data-stu-id="dd77b-111">600 chairs</span></span>                               |
| <span data-ttu-id="dd77b-112">Plán požadovaných dodávek</span><span class="sxs-lookup"><span data-stu-id="dd77b-112">Requested delivery schedule</span></span>       | <span data-ttu-id="dd77b-113">100 židlí měsíčně</span><span class="sxs-lookup"><span data-stu-id="dd77b-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="dd77b-114">Požadovaný časový rámec dodání</span><span class="sxs-lookup"><span data-stu-id="dd77b-114">Requested time frame for delivery</span></span> | <span data-ttu-id="dd77b-115">6 měsíců, v první den každého měsíce</span><span class="sxs-lookup"><span data-stu-id="dd77b-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="dd77b-116">V této situaci zákazník požaduje dodání 600 židlí v dávkách 100 židlí po dobu šesti měsíců.</span><span class="sxs-lookup"><span data-stu-id="dd77b-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="dd77b-117">Ke sledování požadavků na dodání vytvoříte plán dodávek.</span><span class="sxs-lookup"><span data-stu-id="dd77b-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="dd77b-118">Na stránce plánu dodávek vytvoříte šest samostatných řádků dodávky.</span><span class="sxs-lookup"><span data-stu-id="dd77b-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="dd77b-119">Každý řádek dodávky obsahuje 100 židlí a označuje datum dodání těchto 100 židlí.</span><span class="sxs-lookup"><span data-stu-id="dd77b-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="dd77b-120">V tomto případě se každý řádek posune u prvního dne měsíce po šest po sobě následujících měsíců.</span><span class="sxs-lookup"><span data-stu-id="dd77b-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="dd77b-121">Při vytváření plánu dodávek se typ původního řádku objednávky automaticky změní na **Řádek objednávky s více dodávkami**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="dd77b-122">Řádek tohoto typu je označován jako obchodní řádek a je označen ikonou.</span><span class="sxs-lookup"><span data-stu-id="dd77b-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="dd77b-123">Řádek dodávky je označen jinou ikonou.</span><span class="sxs-lookup"><span data-stu-id="dd77b-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="dd77b-124">Pokud změníte množství na řádku dodávky, aktualizuje se obchodní řádek na celkové množství plánu dodávek.</span><span class="sxs-lookup"><span data-stu-id="dd77b-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="dd77b-125">Pokud obchodní smlouva definuje celkovou slevu pro objednávku, plán dodávek zajistí, že objednávka bude splňovat požadavky na slevu celkové objednávky, a to i v případě, že objednávka bude rozdělena na samostatné dodávky.</span><span class="sxs-lookup"><span data-stu-id="dd77b-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="dd77b-126">Objednávky, které mají plán dodávek, se zpracují proti řádkům dodávky.</span><span class="sxs-lookup"><span data-stu-id="dd77b-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="dd77b-127">Zpracování zahrnuje zaúčtování dodacích listů, příjemek produktů a fakturaci.</span><span class="sxs-lookup"><span data-stu-id="dd77b-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="dd77b-128">Výtisky dokumentů objednávek a nabídek, které mají plán dodávek, zobrazují jen řádky dodávky.</span><span class="sxs-lookup"><span data-stu-id="dd77b-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="dd77b-129">Neobsahují původní řádky (obchodní řádky).</span><span class="sxs-lookup"><span data-stu-id="dd77b-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="dd77b-130">**Poznámka:** Navíc se zobrazí jen řádky dodávky při provedení těchto akcí:</span><span class="sxs-lookup"><span data-stu-id="dd77b-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="dd77b-131">Zaúčtovat</span><span class="sxs-lookup"><span data-stu-id="dd77b-131">Post</span></span>
-   <span data-ttu-id="dd77b-132">Kopírování stránek</span><span class="sxs-lookup"><span data-stu-id="dd77b-132">Copy pages</span></span>
-   <span data-ttu-id="dd77b-133">Procházení stránek se seznamy a sestav</span><span class="sxs-lookup"><span data-stu-id="dd77b-133">Browse list pages and reports</span></span>

<span data-ttu-id="dd77b-134">Při potvrzení prodejní nabídky se na výsledných prodejních objednávkách zobrazí celý plán dodávek, i když mají řádky objednávky více dodávek.</span><span class="sxs-lookup"><span data-stu-id="dd77b-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="dd77b-135">Dále se celý plán dodávky zobrazí na všech hlavních stránkách, například na prodejních objednávkách, prodejních nabídkách a nákupních objednávkách.</span><span class="sxs-lookup"><span data-stu-id="dd77b-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>





---
title: Plány dodávek
description: Plány dodávek vám umožňují sledovat množství na řádku objednávky, když pracujete s více dodávkami na jedné prodejní objednávce, prodejní nabídce nebo nákupní objednávce.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193775"
---
# <a name="delivery-schedules"></a><span data-ttu-id="f9761-103">Plány dodávek</span><span class="sxs-lookup"><span data-stu-id="f9761-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9761-104">Plány dodávek vám umožňují sledovat množství na řádku objednávky, když pracujete s více dodávkami na jedné prodejní objednávce, prodejní nabídce nebo nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="f9761-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="f9761-105">Použijte plán dodávek, pokud celkové množství na objednávce nebo řádku nabídky musí být dodáno v podobě vícenásobné expedice.</span><span class="sxs-lookup"><span data-stu-id="f9761-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="f9761-106">Řádky dodávky představují jednotlivé dodávky.</span><span class="sxs-lookup"><span data-stu-id="f9761-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="f9761-107">Dva nebo více řádků dodávek tvoří jeden plán dodávek.</span><span class="sxs-lookup"><span data-stu-id="f9761-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="f9761-108">Řádky dodávky mohou mít jiná data dodání, množství, způsoby dodání a dimenze uskladnění, jako například pracoviště a sklad.</span><span class="sxs-lookup"><span data-stu-id="f9761-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="f9761-109">**Příklad plánu dodávek**</span><span class="sxs-lookup"><span data-stu-id="f9761-109">**Example of a delivery schedule**</span></span>

| <span data-ttu-id="f9761-110">Zboží</span><span class="sxs-lookup"><span data-stu-id="f9761-110">Item</span></span>                              | <span data-ttu-id="f9761-111">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f9761-111">Value</span></span>                                    |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="f9761-112">Celková objednávka (původní řádek objednávky)</span><span class="sxs-lookup"><span data-stu-id="f9761-112">Total order (original order line)</span></span> | <span data-ttu-id="f9761-113">600 židlí</span><span class="sxs-lookup"><span data-stu-id="f9761-113">600 chairs</span></span>                               |
| <span data-ttu-id="f9761-114">Plán požadovaných dodávek</span><span class="sxs-lookup"><span data-stu-id="f9761-114">Requested delivery schedule</span></span>       | <span data-ttu-id="f9761-115">100 židlí měsíčně</span><span class="sxs-lookup"><span data-stu-id="f9761-115">100 chairs per month</span></span>                     |
| <span data-ttu-id="f9761-116">Požadovaný časový rámec dodání</span><span class="sxs-lookup"><span data-stu-id="f9761-116">Requested time frame for delivery</span></span> | <span data-ttu-id="f9761-117">6 měsíců, v první den každého měsíce</span><span class="sxs-lookup"><span data-stu-id="f9761-117">6 months, on the first day of each month</span></span> |

<span data-ttu-id="f9761-118">V této situaci zákazník požaduje dodání 600 židlí v dávkách 100 židlí po dobu šesti měsíců.</span><span class="sxs-lookup"><span data-stu-id="f9761-118">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="f9761-119">Ke sledování požadavků na dodání vytvoříte plán dodávek.</span><span class="sxs-lookup"><span data-stu-id="f9761-119">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="f9761-120">Na stránce plánu dodávek vytvoříte šest samostatných řádků dodávky.</span><span class="sxs-lookup"><span data-stu-id="f9761-120">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="f9761-121">Každý řádek dodávky obsahuje 100 židlí a označuje datum dodání těchto 100 židlí.</span><span class="sxs-lookup"><span data-stu-id="f9761-121">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="f9761-122">V tomto případě se každý řádek posune u prvního dne měsíce po šest po sobě následujících měsíců.</span><span class="sxs-lookup"><span data-stu-id="f9761-122">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="f9761-123">Při vytváření plánu dodávek se typ původního řádku objednávky automaticky změní na **Řádek objednávky s více dodávkami**.</span><span class="sxs-lookup"><span data-stu-id="f9761-123">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="f9761-124">Řádek tohoto typu je označován jako obchodní řádek a je označen ikonou.</span><span class="sxs-lookup"><span data-stu-id="f9761-124">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="f9761-125">Řádek dodávky je označen jinou ikonou.</span><span class="sxs-lookup"><span data-stu-id="f9761-125">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="f9761-126">Pokud změníte množství na řádku dodávky, aktualizuje se obchodní řádek na celkové množství plánu dodávek.</span><span class="sxs-lookup"><span data-stu-id="f9761-126">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="f9761-127">Pokud obchodní smlouva definuje celkovou slevu pro objednávku, plán dodávek zajistí, že objednávka bude splňovat požadavky na slevu celkové objednávky, a to i v případě, že objednávka bude rozdělena na samostatné dodávky.</span><span class="sxs-lookup"><span data-stu-id="f9761-127">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="f9761-128">Objednávky, které mají plán dodávek, se zpracují proti řádkům dodávky.</span><span class="sxs-lookup"><span data-stu-id="f9761-128">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="f9761-129">Zpracování zahrnuje zaúčtování dodacích listů, příjemek produktů a fakturaci.</span><span class="sxs-lookup"><span data-stu-id="f9761-129">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="f9761-130">Výtisky dokumentů objednávek a nabídek, které mají plán dodávek, zobrazují jen řádky dodávky.</span><span class="sxs-lookup"><span data-stu-id="f9761-130">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="f9761-131">Neobsahují původní řádky (obchodní řádky).</span><span class="sxs-lookup"><span data-stu-id="f9761-131">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="f9761-132">**Poznámka:** Navíc se zobrazí jen řádky dodávky při provedení těchto akcí:</span><span class="sxs-lookup"><span data-stu-id="f9761-132">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="f9761-133">Zaúčtovat</span><span class="sxs-lookup"><span data-stu-id="f9761-133">Post</span></span>
-   <span data-ttu-id="f9761-134">Kopírování stránek</span><span class="sxs-lookup"><span data-stu-id="f9761-134">Copy pages</span></span>
-   <span data-ttu-id="f9761-135">Procházení stránek se seznamy a sestav</span><span class="sxs-lookup"><span data-stu-id="f9761-135">Browse list pages and reports</span></span>

<span data-ttu-id="f9761-136">Při potvrzení prodejní nabídky se na výsledných prodejních objednávkách zobrazí celý plán dodávek, i když mají řádky objednávky více dodávek.</span><span class="sxs-lookup"><span data-stu-id="f9761-136">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="f9761-137">Dále se celý plán dodávky zobrazí na všech hlavních stránkách, například na prodejních objednávkách, prodejních nabídkách a nákupních objednávkách.</span><span class="sxs-lookup"><span data-stu-id="f9761-137">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
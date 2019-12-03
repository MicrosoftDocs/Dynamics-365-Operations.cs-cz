---
title: Postupné vytváření objednávek pro maloobchodní transakce
description: V tomto tématu je popsáno postupné vytváření objednávek pro maloobchodní transakce v Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: deb8399aa401af16b6fe123a433eb21864e178c6
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693082"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="a8e82-103">Postupné vytváření objednávek pro maloobchodní transakce (veřejná verze Preview)</span><span class="sxs-lookup"><span data-stu-id="a8e82-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a8e82-104">V aplikaci Dynamics 365 Retail verze 10.0.4 a starších je zaúčtování maloobchodních výkazů operací na konci dne a všechny transakce jsou zaúčtovány do knih až na konci dne.</span><span class="sxs-lookup"><span data-stu-id="a8e82-104">In Dynamics 365 Retail versions 10.0.4 and earlier, retail statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="a8e82-105">Rozsáhlé transakce tak musí být zpracovány v omezeném časovém úseku, což má někdy za následek vytížení a uzamčení a selhání zaúčtování výkazů.</span><span class="sxs-lookup"><span data-stu-id="a8e82-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="a8e82-106">Maloobchodní prodejci také nemohou uznat výnosy a platby ve svých knihách v průběhu dne.</span><span class="sxs-lookup"><span data-stu-id="a8e82-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="a8e82-107">Ve veřejné verzi Preview se díky postupnému vytváření objednávek, funkci představené ve verzi 10.0.5 aplikace Retails, transakce zpracovávají po celý den a na konci dne se zpracovávají pouze finanční odsouhlasení úhrad a jiné transakce řízení hotovosti.</span><span class="sxs-lookup"><span data-stu-id="a8e82-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="a8e82-108">Tato funkce rozdělí vytížení vytváření prodejních objednávek, faktur a plateb na celý den a poskytuje lepší vnímaný výkon a schopnost uznat výnosy a platby v knihách v téměř reálném čase.</span><span class="sxs-lookup"><span data-stu-id="a8e82-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="a8e82-109">Jak používat postupné účtování</span><span class="sxs-lookup"><span data-stu-id="a8e82-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="a8e82-110">Chcete-li povolit postupné účtování maloobchodních transakcí, přejděte na **Správa systému > Nastavení > Konfigurace licence** a zakažte klíč **Výkazy maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="a8e82-110">To enable trickle feed-based posting of retail transactions, go to **System administration > Set up > License configuration** and disable the the **Retail statements** key.</span></span>

2. <span data-ttu-id="a8e82-111">Na stejné stránce povolte licenční klíč **Výkazy maloobchodu (postupné) – Preview**.</span><span class="sxs-lookup"><span data-stu-id="a8e82-111">On the same page, enable the **Retail statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="a8e82-112">Když povolíte tento klíč, ujistěte se, že neexistují žádné nevyřízené výkazy čekající na zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="a8e82-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

> [!Important]
> <span data-ttu-id="a8e82-113">Před povolením licenčního klíče **Výkazy maloobchodu (postupné) – Preview** se ujistěte, že neexistují žádné nevyřízené výkazy čekající na zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="a8e82-113">Before you enable the **Retail statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="a8e82-114">Aktuální dokument výkazu bude rozdělen na dva různé typy. transakční výkaz a finanční výkaz.</span><span class="sxs-lookup"><span data-stu-id="a8e82-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="a8e82-115">Transakční výkaz vybere všechny nezaúčtované a ověřené maloobchodní transakce a bude vytvářet prodejní objednávky, prodejní faktury, deníky slev a plateb a transakce příjmů a výdajů ve frekvenci, kterou nakonfigurujete.</span><span class="sxs-lookup"><span data-stu-id="a8e82-115">The transactional statement will pick up all unposted and validated retail transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="a8e82-116">Tento proces byste měli nakonfigurovat ke spouštění v časté frekvenci, aby dokumenty byly vytvářeny při odesílání maloobchodních transakcí do Retail Headquarters prostřednictvím úlohy P.</span><span class="sxs-lookup"><span data-stu-id="a8e82-116">You should configure this process to run at a high frequency so that documents are created when the retail transactions are uploaded into Retail Headquarters through the P-job.</span></span> <span data-ttu-id="a8e82-117">U transakčního výkazu, který již vytváří prodejní objednávky a prodejní faktury, není třeba konfigurovat dávkovou úlohu **Zaúčtovat zásoby**.</span><span class="sxs-lookup"><span data-stu-id="a8e82-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="a8e82-118">Lze ji však stále použít k uspokojení specifických obchodních požadavků, které můžete mít.</span><span class="sxs-lookup"><span data-stu-id="a8e82-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="a8e82-119">Finanční výkaz je určen k tomu, aby byl vytvořen na konci dne, a podporuje pouze metodu uzávěrky **Směna**.</span><span class="sxs-lookup"><span data-stu-id="a8e82-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="a8e82-120">Tento výkaz bude omezen na finanční odsouhlasení a bude vytvářet pouze deníky pro rozdílné částky mezi spočtenou částkou a částkou transakce pro různé úhrady, společně s deníky pro ostatní transakce řízení hotovosti.</span><span class="sxs-lookup"><span data-stu-id="a8e82-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="a8e82-121">Chcete-li vypočítat transakční výkaz, klikněte na **Maloobchod > IT pro maloobchod > Zaúčtování POS > Vypočítat transakční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="a8e82-121">To calculate the transactional statement, click **Retail > Retail IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="a8e82-122">Chcete-li zaúčtovat transakční výkazy v dávce, klikněte na **Maloobchod > IT pro maloobchod > Zaúčtování POS > Zaúčtovat transakční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="a8e82-122">To post the transactional statement statements in batch, click **Retail > Retail IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="a8e82-123">Chcete-li vypočítat finanční výkaz, klikněte na **Maloobchod > IT pro maloobchod > Zaúčtování POS > Vypočítat finanční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="a8e82-123">To calculate the financial statement, click **Retail > Retail IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="a8e82-124">Chcete-li zaúčtovat finanční výkazy v dávce, klikněte na **Maloobchod > IT pro maloobchod > Zaúčtování POS > Zaúčtovat finanční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="a8e82-124">To post the financial statements in batch, click **Retail > Retail IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="a8e82-125">Položky nabídky **Maloobchod > IT pro maloobchod > Zaúčtování POS > Vypočítat výkazy v dávce** a **Maloobchod > IT pro maloobchod > Zaúčtování POS > Zaúčtovat výkazy v dávce** jsou s touto novou funkcí odebrány.</span><span class="sxs-lookup"><span data-stu-id="a8e82-125">The menu items **Retail > Retail IT > POS Posting > Calculate statements in batch** and **Retail > Retail IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="a8e82-126">Typy transakčních a finančních výkazů lze alternativně vytvořit ručně.</span><span class="sxs-lookup"><span data-stu-id="a8e82-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="a8e82-127">Přejděte na **Maloobchod > Kanály > Maloobchody** a klikněte na **Maloobchodní výkazy**.</span><span class="sxs-lookup"><span data-stu-id="a8e82-127">Go to **Retail > Channels > Retail stores** and click **Retail statements**.</span></span> <span data-ttu-id="a8e82-128">Klikněte na **Nový** a pak zvolte typ výkazu, který chcete vytvořit.</span><span class="sxs-lookup"><span data-stu-id="a8e82-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="a8e82-129">Pole na stránce **Maloobchodní výkazy** a akce pod položkou **Skupina výkazů** této stránky zobrazí relevantní data a akce založené na vybraném typu výkazu.</span><span class="sxs-lookup"><span data-stu-id="a8e82-129">Fields on the **Retail statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>

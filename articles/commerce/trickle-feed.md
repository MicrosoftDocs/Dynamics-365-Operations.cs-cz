---
title: Postupné vytváření objednávek pro maloobchodní transakce
description: V tomto tématu je popsáno postupné vytváření objednávek pro transakce obchodu v Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 06/08/2020
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
ms.openlocfilehash: 6e097ead7cacb3f71452323656546a4be661457f
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710276"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="cb3ad-103">Postupné vytváření objednávek pro maloobchodní transakce</span><span class="sxs-lookup"><span data-stu-id="cb3ad-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cb3ad-104">V aplikaci Dynamics 365 Retail verze 10.0.4 a starších je zaúčtování výkazů operací na konci dne a všechny transakce jsou zaúčtovány do knih až na konci dne.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="cb3ad-105">Rozsáhlé transakce tak musí být zpracovány v omezeném časovém úseku, což má někdy za následek vytížení a uzamčení a selhání zaúčtování výkazů.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="cb3ad-106">Maloobchodní prodejci také nemohou uznat výnosy a platby ve svých knihách v průběhu dne.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="cb3ad-107">Díky postupnému vytváření objednávek, funkci představené ve verzi 10.0.5 aplikace Retail, transakce zpracovávají po celý den a na konci dne se zpracovávají pouze finanční odsouhlasení úhrad a jiné transakce řízení hotovosti.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="cb3ad-108">Tato funkce rozdělí vytížení vytváření prodejních objednávek, faktur a plateb na celý den a poskytuje lepší vnímaný výkon a schopnost uznat výnosy a platby v knihách v téměř reálném čase.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="cb3ad-109">Jak používat postupné účtování</span><span class="sxs-lookup"><span data-stu-id="cb3ad-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="cb3ad-110">Chcete-li povolit postupné účtování transakcí, přejděte na **Správa systému > Nastavení > Konfigurace licence** a zakažte klíč **Výkazy**.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-110">To enable trickle feed-based posting of transactions, go to **System administration > Set up > License configuration** and disable the the **Statements** key.</span></span>

2. <span data-ttu-id="cb3ad-111">Na stejné stránce povolte licenční klíč **Výkazy (postupné) – Preview**.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-111">On the same page, enable the **Statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="cb3ad-112">Když povolíte tento klíč, ujistěte se, že neexistují žádné nevyřízené výkazy čekající na zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

    > [!Important]
    > <span data-ttu-id="cb3ad-113">Před povolením licenčního klíče **Výkazy (postupné) – Preview** se ujistěte, že neexistují žádné nevyřízené výkazy čekající na zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-113">Before you enable the **Statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="cb3ad-114">Aktuální dokument výkazu bude rozdělen na dva různé typy. transakční výkaz a finanční výkaz.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="cb3ad-115">Transakční výkaz vybere všechny nezaúčtované a ověřené transakce a bude vytvářet prodejní objednávky, prodejní faktury, deníky slev a plateb a transakce příjmů a výdajů ve frekvenci, kterou nakonfigurujete.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-115">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="cb3ad-116">Tento proces byste měli nakonfigurovat ke spouštění v časté frekvenci, aby dokumenty byly vytvářeny při odesílání transakcí do centrály prostřednictvím úlohy P.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-116">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="cb3ad-117">U transakčního výkazu, který již vytváří prodejní objednávky a prodejní faktury, není třeba konfigurovat dávkovou úlohu **Zaúčtovat zásoby**.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="cb3ad-118">Lze ji však stále použít k uspokojení specifických obchodních požadavků, které můžete mít.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="cb3ad-119">Finanční výkaz je určen k tomu, aby byl vytvořen na konci dne, a podporuje pouze metodu uzávěrky **Směna**.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="cb3ad-120">Tento výkaz bude omezen na finanční odsouhlasení a bude vytvářet pouze deníky pro rozdílné částky mezi spočtenou částkou a částkou transakce pro různé úhrady, společně s deníky pro ostatní transakce řízení hotovosti.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="cb3ad-121">Chcete-li vypočítat transakční výkaz, klikněte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Vypočítat transakční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-121">To calculate the transactional statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="cb3ad-122">Chcete-li zaúčtovat transakční výkazy v dávce, klikněte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Zaúčtovat transakční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-122">To post the transactional statement statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="cb3ad-123">Chcete-li vypočítat finanční výkaz, klikněte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Vypočítat finanční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-123">To calculate the financial statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="cb3ad-124">Chcete-li zaúčtovat finanční výkazy v dávce, klikněte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Zaúčtovat finanční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-124">To post the financial statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="cb3ad-125">Položky nabídky **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Vypočítat výkazy v dávce** a **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Zaúčtovat výkazy v dávce** jsou s touto novou funkcí odebrány.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-125">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="cb3ad-126">Typy transakčních a finančních výkazů lze alternativně vytvořit ručně.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="cb3ad-127">Přejděte na **Retail a Commerce > Kanály > Obchody** a klikněte na **Výkazy**.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-127">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="cb3ad-128">Klikněte na **Nový** a pak zvolte typ výkazu, který chcete vytvořit.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="cb3ad-129">Pole na stránce **Výkazy** a akce pod položkou **Skupina výkazů** této stránky zobrazí relevantní data a akce založené na vybraném typu výkazu.</span><span class="sxs-lookup"><span data-stu-id="cb3ad-129">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>

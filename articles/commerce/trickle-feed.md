---
title: Postupné vytváření objednávek pro maloobchodní transakce
description: V tomto tématu je popsáno postupné vytváření objednávek pro transakce obchodu v Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
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
ms.openlocfilehash: 79f99b9b401de3e3bcca6ec5a13a3b4f7bad6f8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458629"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="78dc7-103">Postupné vytváření objednávek pro maloobchodní transakce</span><span class="sxs-lookup"><span data-stu-id="78dc7-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="78dc7-104">V aplikaci Dynamics 365 Retail verze 10.0.4 a starších je zaúčtování výkazů operací na konci dne a všechny transakce jsou zaúčtovány do knih až na konci dne.</span><span class="sxs-lookup"><span data-stu-id="78dc7-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="78dc7-105">Rozsáhlé transakce tak musí být zpracovány v omezeném časovém úseku, což má někdy za následek vytížení a uzamčení a selhání zaúčtování výkazů.</span><span class="sxs-lookup"><span data-stu-id="78dc7-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="78dc7-106">Maloobchodní prodejci také nemohou uznat výnosy a platby ve svých knihách v průběhu dne.</span><span class="sxs-lookup"><span data-stu-id="78dc7-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="78dc7-107">Díky postupnému vytváření objednávek, funkci představené ve verzi 10.0.5 aplikace Retail, transakce zpracovávají po celý den a na konci dne se zpracovávají pouze finanční odsouhlasení úhrad a jiné transakce řízení hotovosti.</span><span class="sxs-lookup"><span data-stu-id="78dc7-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="78dc7-108">Tato funkce rozdělí vytížení vytváření prodejních objednávek, faktur a plateb na celý den a poskytuje lepší vnímaný výkon a schopnost uznat výnosy a platby v knihách v téměř reálném čase.</span><span class="sxs-lookup"><span data-stu-id="78dc7-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="78dc7-109">Jak používat postupné účtování</span><span class="sxs-lookup"><span data-stu-id="78dc7-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="78dc7-110">Chcete-li povolit postupné účtování maloobchodních transakcí, povolte funkci s názvem **Výkazy maloobchodu – Postupné** pomocí správy funkcí.</span><span class="sxs-lookup"><span data-stu-id="78dc7-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="78dc7-111">Než povolíte tuto funkci, ujistěte se, že na zaúčtování nečekají žádné nevyřízené výkazy.</span><span class="sxs-lookup"><span data-stu-id="78dc7-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="78dc7-112">Aktuální dokument výkazu bude rozdělen na dva typy: transakční výkaz a finanční výkaz.</span><span class="sxs-lookup"><span data-stu-id="78dc7-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="78dc7-113">Transakční výkaz vybere všechny nezaúčtované a ověřené transakce a bude vytvářet prodejní objednávky, prodejní faktury, deníky slev a plateb a transakce příjmů a výdajů ve frekvenci, kterou nakonfigurujete.</span><span class="sxs-lookup"><span data-stu-id="78dc7-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="78dc7-114">Tento proces byste měli nakonfigurovat ke spouštění v časté frekvenci, aby dokumenty byly vytvářeny při odesílání transakcí do centrály prostřednictvím úlohy P.</span><span class="sxs-lookup"><span data-stu-id="78dc7-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="78dc7-115">U transakčního výkazu, který již vytváří prodejní objednávky a prodejní faktury, není třeba konfigurovat dávkovou úlohu **Zaúčtovat zásoby**.</span><span class="sxs-lookup"><span data-stu-id="78dc7-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="78dc7-116">Lze ji však stále použít k uspokojení specifických obchodních požadavků, které můžete mít.</span><span class="sxs-lookup"><span data-stu-id="78dc7-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="78dc7-117">Finanční výkaz je určen k tomu, aby byl vytvořen na konci dne, a podporuje pouze metodu uzávěrky **Směna**.</span><span class="sxs-lookup"><span data-stu-id="78dc7-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="78dc7-118">Tento výkaz bude omezen na finanční odsouhlasení a bude vytvářet pouze deníky pro rozdílné částky mezi spočtenou částkou a částkou transakce pro různé úhrady, společně s deníky pro ostatní transakce řízení hotovosti.</span><span class="sxs-lookup"><span data-stu-id="78dc7-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="78dc7-119">Chcete-li vypočítat transakční výkaz, přejděte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Vypočítat transakční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="78dc7-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="78dc7-120">Chcete-li zaúčtovat transakční výkazy v dávce, přejděte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Zaúčtovat transakční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="78dc7-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="78dc7-121">Chcete-li vypočítat finanční výkaz, přejděte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Vypočítat finanční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="78dc7-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="78dc7-122">Chcete-li zaúčtovat finanční výkazy v dávce, přejděte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Zaúčtovat finanční výkazy v dávce**.</span><span class="sxs-lookup"><span data-stu-id="78dc7-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="78dc7-123">Položky nabídky **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Vypočítat výkazy v dávce** a **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Zaúčtovat výkazy v dávce** jsou s touto novou funkcí odebrány.</span><span class="sxs-lookup"><span data-stu-id="78dc7-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="78dc7-124">Typy transakčních a finančních výkazů lze alternativně vytvořit ručně.</span><span class="sxs-lookup"><span data-stu-id="78dc7-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="78dc7-125">Přejděte na **Retail a Commerce > Kanály > Obchody** a klikněte na **Výkazy**.</span><span class="sxs-lookup"><span data-stu-id="78dc7-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="78dc7-126">Klikněte na **Nový** a pak zvolte typ výkazu, který chcete vytvořit.</span><span class="sxs-lookup"><span data-stu-id="78dc7-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="78dc7-127">Pole na stránce **Výkazy** a akce pod položkou **Skupina výkazů** této stránky zobrazí relevantní data a akce založené na vybraném typu výkazu.</span><span class="sxs-lookup"><span data-stu-id="78dc7-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>

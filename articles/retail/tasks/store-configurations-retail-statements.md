---
title: " Konfigurace obchodů pro maloobchodní výkazy"
description: Tato procedura vás provede konfiguracemi pro maloobchod, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbedcda59f503b103d5448e59038e4ed8ca0b51d
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916523"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="5c498-103"> Konfigurace obchodů pro maloobchodní výkazy</span><span class="sxs-lookup"><span data-stu-id="5c498-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5c498-104">Tato procedura vás provede konfiguracemi pro maloobchod, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="5c498-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="5c498-105">Finanční dimenze maloobchodu jsou zahrnuty v jiné proceduře.</span><span class="sxs-lookup"><span data-stu-id="5c498-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="5c498-106">Tato procedura používá ukázkovou společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="5c498-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="5c498-107">V **Navigačním podokně** přejděte na **Moduly > Maloobchodní a velkoobchodní prodej > Kanály > Maloobchody > Všechny maloobchody**.</span><span class="sxs-lookup"><span data-stu-id="5c498-107">In the **Navgiation pane**, go to **Modules > Retail and commerce > Channels > Retail stores > All retail stores**.</span></span>
2. <span data-ttu-id="5c498-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5c498-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5c498-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5c498-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5c498-110">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="5c498-110">Click **Edit**.</span></span>
5. <span data-ttu-id="5c498-111">Nastavení v pevné záložce **Výkaz/uzávěrka** ovlivní vytvoření ověření a zaúčtování výkazu pro obchod.</span><span class="sxs-lookup"><span data-stu-id="5c498-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="5c498-112">Rozbalte pevnou záložku **Výkaz/uzávěrka**.</span><span class="sxs-lookup"><span data-stu-id="5c498-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="5c498-113">V poli **Metoda výkazu** vyberte metodu, podle které chcete seskupit řádky výpisu.</span><span class="sxs-lookup"><span data-stu-id="5c498-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="5c498-114">Vyberte „Ano“ v možnosti **Jeden výkaz denně**, pokud má existovat pouze jeden výkaz vytvořený denně při vytváření výpisů z výkazu vytvoření dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="5c498-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="5c498-115">Pole **Výpočet výkazu úhrad** definuje, zda je třeba společně přidat výkazy úhrad, nebo zda má být použit poslední.</span><span class="sxs-lookup"><span data-stu-id="5c498-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="5c498-116">V poli **Zaokrouhlení** vyberte účet hlavní knihy pro zaúčtování haléřových rozdílů.</span><span class="sxs-lookup"><span data-stu-id="5c498-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="5c498-117">V poli **Maximální rozdíl zaokrouhlení** můžete zadat maximální povolený rozdíl zaokrouhlení.</span><span class="sxs-lookup"><span data-stu-id="5c498-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="5c498-118">V poli **Zaúčtování** můžete zadat maximální celkový povolený rozdíl pro zaúčtování pro výkaz.</span><span class="sxs-lookup"><span data-stu-id="5c498-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="5c498-119">V poli **Směna** můžete zadat maximální celkový rozdíl v rámci směny ve výkazu.</span><span class="sxs-lookup"><span data-stu-id="5c498-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="5c498-120">V poli **Transakce** můžete zadat maximální celkový rozdíl v řádku výkazu.</span><span class="sxs-lookup"><span data-stu-id="5c498-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="5c498-121">V poli **Metoda uzávěrky** můžete definovat, zda transakce, které budou zahrnuty do výkazu, by měly být součástí uzavřené směny, nebo zda se může jednat o libovolné transakce v rámci definovaného data a času.</span><span class="sxs-lookup"><span data-stu-id="5c498-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="5c498-122">V poli **Konec pracovního dne** můžete zadat čas, pokud mají být transakce, ke kterým dojde po půlnoci, zaúčtovány v rámci předchozího dne.</span><span class="sxs-lookup"><span data-stu-id="5c498-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="5c498-123">Vyberte „Ano“ v možnosti **Zaúčtovat jako pracovní den**, pokud mají být transakce, ke kterým dojde po půlnoci, zaúčtovány jako součást předchozího dne.</span><span class="sxs-lookup"><span data-stu-id="5c498-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="5c498-124">Vyberte možnost „Ano“ v možnosti **Metoda rozdělení podle výpisu**, chcete-li získat výkazy vytvořené pro každou definovanou metodu výkazu.</span><span class="sxs-lookup"><span data-stu-id="5c498-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="5c498-125">To je užitečné v případě, že výkon při účtování je třeba zlepšit pro obchody s vysokými objemy transakcí, protože vytvoří mnoho menších výkazů, které lze zpracovat současně.</span><span class="sxs-lookup"><span data-stu-id="5c498-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="5c498-126">Na pevné záložce **Obecné**, v poli **Výchozí odběratel** můžete vybrat účet odběratele, který se má použít pro prodeje příchozím odběratelům.</span><span class="sxs-lookup"><span data-stu-id="5c498-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  


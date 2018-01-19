--- 
title: " Konfigurace obchodů pro maloobchodní výkazy"
description: "Tato procedura vás provede konfiguracemi pro maloobchod, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: c2140afc869686ae3f6d6c73ddaa31a4954d4d72
ms.contentlocale: cs-cz
ms.lasthandoff: 01/19/2018

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="43ea3-103"> Konfigurace obchodů pro maloobchodní výkazy</span><span class="sxs-lookup"><span data-stu-id="43ea3-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="43ea3-104">Tato procedura vás provede konfiguracemi pro maloobchod, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="43ea3-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="43ea3-105">Finanční dimenze maloobchodu jsou zahrnuty v jiné proceduře.</span><span class="sxs-lookup"><span data-stu-id="43ea3-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="43ea3-106">Tato procedura používá ukázkovou společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="43ea3-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="43ea3-107">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Kanály > Maloobchody > Všechny maloobchody.</span><span class="sxs-lookup"><span data-stu-id="43ea3-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="43ea3-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43ea3-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="43ea3-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="43ea3-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="43ea3-110">Nastavení v části Výkaz/uzávěrka ovlivní vytvoření ověření a zaúčtování výkazu pro obchod.</span><span class="sxs-lookup"><span data-stu-id="43ea3-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="43ea3-111">Otevřete oddíl Výkaz/uzávěrka.</span><span class="sxs-lookup"><span data-stu-id="43ea3-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="43ea3-112">Vyberte metodu, podle které chcete seskupit řádky výpisu.</span><span class="sxs-lookup"><span data-stu-id="43ea3-112">Select the method you want to use to group the statement lines by.</span></span>  
    * <span data-ttu-id="43ea3-113">Vyberte „Ano“, pokud má existovat pouze jeden výkaz vytvořený denně při vytváření výpisů z výkazu vytvoření dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="43ea3-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="43ea3-114">Pole Výpočet výkazu úhrad definuje, zda je třeba společně přidat výkazy úhrad, nebo zda má být použit poslední.</span><span class="sxs-lookup"><span data-stu-id="43ea3-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="43ea3-115">Vyberte účet hlavní knihy pro zaúčtování haléřových rozdílů.</span><span class="sxs-lookup"><span data-stu-id="43ea3-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="43ea3-116">V poli Maximální rozdíl zaokrouhlení můžete zadat maximální povolený rozdíl zaokrouhlení.</span><span class="sxs-lookup"><span data-stu-id="43ea3-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="43ea3-117">V poli Zaúčtování můžete zadat maximální celkový povolený rozdíl pro zaúčtování pro výkaz.</span><span class="sxs-lookup"><span data-stu-id="43ea3-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="43ea3-118">V poli Směna můžete zadat maximální celkový rozdíl v rámci směny ve výkazu.</span><span class="sxs-lookup"><span data-stu-id="43ea3-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="43ea3-119">V poli Transakce můžete zadat maximální celkový rozdíl v řádku výkazu.</span><span class="sxs-lookup"><span data-stu-id="43ea3-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="43ea3-120">V poli Metoda uzávěrky můžete definovat, zda transakce, které budou zahrnuty do výkazu, by měly být součástí uzavřené směny, nebo zda se může jednat o libovolné transakce v rámci definovaného data a času.</span><span class="sxs-lookup"><span data-stu-id="43ea3-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="43ea3-121">V poli Konec pracovního dne můžete zadat čas, pokud mají být transakce, ke kterým dojde po půlnoci, zaúčtovány v rámci předchozího dne.</span><span class="sxs-lookup"><span data-stu-id="43ea3-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="43ea3-122">Vyberte „Ano“, pokud mají být transakce, ke kterým dojde po půlnoci, zaúčtovány jako součást předchozího dne.</span><span class="sxs-lookup"><span data-stu-id="43ea3-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="43ea3-123">Vyberte možnost „Ano“ chcete-li získat výkazy vytvořené pro každou definovanou metodu výkazu.</span><span class="sxs-lookup"><span data-stu-id="43ea3-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="43ea3-124">To je užitečné v případě, že výkon při účtování je třeba zlepšit pro obchody s vysokými objemy transakcí, protože vytvoří mnoho menších výkazů, které lze zpracovat současně.</span><span class="sxs-lookup"><span data-stu-id="43ea3-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="43ea3-125">V poli Výchozí odběratel můžete vybrat účet odběratele, který se má použít pro prodeje příchozím odběratelům.</span><span class="sxs-lookup"><span data-stu-id="43ea3-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  



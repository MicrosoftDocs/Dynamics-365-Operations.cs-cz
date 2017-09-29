--- 
title: " Vytváření finančních dimenzí pro maloobchodní sítě a konfigurace hodnot dimenzí v obchodech"
description: "Tato procedura vás provede vytvořením finanční dimenze maloobchodního kanálu s hodnotami dimenzí a postupem pro konfiguraci hodnot finančních dimenzí v maloobchodních prodejnách."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 56b586e971cfd4684f3c0b259270cc8b31521ac9
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="1435c-103"> Vytváření finančních dimenzí pro maloobchodní sítě a konfigurace hodnot dimenzí v obchodech</span><span class="sxs-lookup"><span data-stu-id="1435c-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1435c-104">Tato procedura vás provede vytvořením finanční dimenze maloobchodního kanálu s hodnotami dimenzí a postupem pro konfiguraci hodnot finančních dimenzí v maloobchodních prodejnách.</span><span class="sxs-lookup"><span data-stu-id="1435c-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="1435c-105">Téma neobsahuje další související postup, jako je například vytváření sad dimenzí a účetních struktur.</span><span class="sxs-lookup"><span data-stu-id="1435c-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="1435c-106">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="1435c-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="1435c-107">Přejděte do části Hlavní kniha > Účtová osnova > Dimenze > Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="1435c-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="1435c-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1435c-108">Click New.</span></span>
3. <span data-ttu-id="1435c-109">V poli Použít hodnoty od vyberte „Maloobchodní kanály“.</span><span class="sxs-lookup"><span data-stu-id="1435c-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="1435c-110">Do pole Název dimenze zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1435c-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="1435c-111">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="1435c-111">Click Activate.</span></span>
6. <span data-ttu-id="1435c-112">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="1435c-112">Click Close.</span></span>
7. <span data-ttu-id="1435c-113">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="1435c-113">Click Activate.</span></span>
8. <span data-ttu-id="1435c-114">Klepněte na Hodnoty dimenzí.</span><span class="sxs-lookup"><span data-stu-id="1435c-114">Click Dimension values.</span></span>
9. <span data-ttu-id="1435c-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1435c-115">Close the page.</span></span>
10. <span data-ttu-id="1435c-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1435c-116">Click Save.</span></span>
11. <span data-ttu-id="1435c-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1435c-117">Close the page.</span></span>
12. <span data-ttu-id="1435c-118">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Kanály > Maloobchody > Všechny maloobchody.</span><span class="sxs-lookup"><span data-stu-id="1435c-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="1435c-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1435c-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1435c-120">Rozbalte oddíl Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="1435c-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="1435c-121">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="1435c-121">Click Edit.</span></span>
16. <span data-ttu-id="1435c-122">V poli Retailchannel kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1435c-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="1435c-123">V seznamu vyhledejte a vyberte hodnotu dimenze pro aktualizovaný obchod.</span><span class="sxs-lookup"><span data-stu-id="1435c-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="1435c-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1435c-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="1435c-125">V poli Nákladové středisko kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1435c-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="1435c-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1435c-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="1435c-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1435c-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="1435c-128">V poli Oddělení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1435c-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="1435c-129">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1435c-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="1435c-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1435c-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="1435c-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1435c-131">Click Save.</span></span>



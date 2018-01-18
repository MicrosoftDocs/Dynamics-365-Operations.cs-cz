--- 
title: " Vytvoření finančních dimenzí pro pokladny POS a konfigurace hodnot dimenzí na pokladnách"
description: "Tato procedura vás provede procesem vytvoření finančních dimenzí pro registry pokladních míst (POS) a ukazuje, jak nakonfigurovat hodnoty finančních dimenzí na registračních pokladnách."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
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
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: d2dd2b2dfac44dc343a4b13738c68ccbb27b9e16
ms.contentlocale: cs-cz
ms.lasthandoff: 01/17/2018

---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="38bac-103"> Vytvoření finančních dimenzí pro pokladny POS a konfigurace hodnot dimenzí na pokladnách</span><span class="sxs-lookup"><span data-stu-id="38bac-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="38bac-104">Tato procedura vás provede procesem vytvoření finančních dimenzí pro registry pokladních míst (POS) a ukazuje, jak nakonfigurovat hodnoty finančních dimenzí na registračních pokladnách.</span><span class="sxs-lookup"><span data-stu-id="38bac-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="38bac-105">Tato procedura neobsahuje další související postup, jako je například vytváření sad dimenzí a účetních struktur.</span><span class="sxs-lookup"><span data-stu-id="38bac-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="38bac-106">Tyto úkoly můžete najít v jiných tématech.</span><span class="sxs-lookup"><span data-stu-id="38bac-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="38bac-107">Tento záznam používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="38bac-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="38bac-108">Přejděte do části Hlavní kniha > Účtová osnova > Dimenze > Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="38bac-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="38bac-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="38bac-109">Click New.</span></span>
3. <span data-ttu-id="38bac-110">Vyberte možnost v poli Použít hodnoty od.</span><span class="sxs-lookup"><span data-stu-id="38bac-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="38bac-111">Do pole Název dimenze zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="38bac-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="38bac-112">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="38bac-112">Click Activate.</span></span>
6. <span data-ttu-id="38bac-113">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="38bac-113">Click Close.</span></span>
7. <span data-ttu-id="38bac-114">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="38bac-114">Click Activate.</span></span>
8. <span data-ttu-id="38bac-115">Klepněte na Hodnoty dimenzí.</span><span class="sxs-lookup"><span data-stu-id="38bac-115">Click Dimension values.</span></span>
9. <span data-ttu-id="38bac-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="38bac-116">Close the page.</span></span>
10. <span data-ttu-id="38bac-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="38bac-117">Click Save.</span></span>
11. <span data-ttu-id="38bac-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="38bac-118">Close the page.</span></span>
12. <span data-ttu-id="38bac-119">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Nastavení POS > Pokladny.</span><span class="sxs-lookup"><span data-stu-id="38bac-119">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="38bac-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="38bac-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="38bac-121">Rozbalte oddíl Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="38bac-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="38bac-122">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="38bac-122">Click Edit.</span></span>
16. <span data-ttu-id="38bac-123">V poli Terminál kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="38bac-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="38bac-124">Na seznamu vyhledejte a vyberte hodnotu dimenze pro aktualizovaný registr.</span><span class="sxs-lookup"><span data-stu-id="38bac-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="38bac-125">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="38bac-125">Click Save.</span></span>



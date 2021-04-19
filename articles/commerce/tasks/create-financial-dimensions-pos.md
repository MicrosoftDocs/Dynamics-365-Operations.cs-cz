---
title: " Vytvoření finančních dimenzí pro pokladny POS a konfigurace hodnot dimenzí na pokladnách"
description: Tato procedura vás provede procesem vytvoření finančních dimenzí pro registry pokladních míst (POS) a ukazuje, jak nakonfigurovat hodnoty finančních dimenzí na registračních pokladnách.
author: jashanno
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eecb126ae550d67310ada22bd7d91438f7a20cf2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790951"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="a3a61-103"> Vytvoření finančních dimenzí pro pokladny POS a konfigurace hodnot dimenzí na pokladnách</span><span class="sxs-lookup"><span data-stu-id="a3a61-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3a61-104">Tato procedura vás provede procesem vytvoření finančních dimenzí pro registry pokladních míst (POS) a ukazuje, jak nakonfigurovat hodnoty finančních dimenzí na registračních pokladnách.</span><span class="sxs-lookup"><span data-stu-id="a3a61-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="a3a61-105">Tato procedura neobsahuje další související postup, jako je například vytváření sad dimenzí a účetních struktur.</span><span class="sxs-lookup"><span data-stu-id="a3a61-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="a3a61-106">Tyto úkoly můžete najít v jiných tématech.</span><span class="sxs-lookup"><span data-stu-id="a3a61-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="a3a61-107">Tento záznam používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="a3a61-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="a3a61-108">Přejděte do části Hlavní kniha > Účtová osnova > Dimenze > Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="a3a61-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="a3a61-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a3a61-109">Click New.</span></span>
3. <span data-ttu-id="a3a61-110">Vyberte možnost v poli Použít hodnoty od.</span><span class="sxs-lookup"><span data-stu-id="a3a61-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="a3a61-111">Do pole Název dimenze zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a3a61-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="a3a61-112">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="a3a61-112">Click Activate.</span></span>
6. <span data-ttu-id="a3a61-113">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="a3a61-113">Click Close.</span></span>
7. <span data-ttu-id="a3a61-114">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="a3a61-114">Click Activate.</span></span>
8. <span data-ttu-id="a3a61-115">Klepněte na Hodnoty dimenzí.</span><span class="sxs-lookup"><span data-stu-id="a3a61-115">Click Dimension values.</span></span>
9. <span data-ttu-id="a3a61-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a3a61-116">Close the page.</span></span>
10. <span data-ttu-id="a3a61-117">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="a3a61-117">Click Save.</span></span>
11. <span data-ttu-id="a3a61-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a3a61-118">Close the page.</span></span>
12. <span data-ttu-id="a3a61-119">Přejděte do nabídky Retail and Commerce > Nastavení kanálu > Nastavení POS > Pokladny.</span><span class="sxs-lookup"><span data-stu-id="a3a61-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="a3a61-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a3a61-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a3a61-121">Rozbalte oddíl Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="a3a61-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="a3a61-122">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="a3a61-122">Click Edit.</span></span>
16. <span data-ttu-id="a3a61-123">V poli Terminál kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a3a61-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="a3a61-124">Na seznamu vyhledejte a vyberte hodnotu dimenze pro aktualizovaný registr.</span><span class="sxs-lookup"><span data-stu-id="a3a61-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="a3a61-125">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="a3a61-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
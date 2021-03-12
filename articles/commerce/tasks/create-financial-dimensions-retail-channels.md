---
title: Vytváření finančních dimenzí pro maloobchodní sítě a konfigurace hodnot dimenzí v obchodech
description: Tato procedura vás provede vytvořením finanční dimenze kanálu commerce s hodnotami dimenzí a postupem pro konfiguraci hodnot finančních dimenzí v obchodech.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86fc9c9a400bee1280b32f10b1e8f55e581e1984
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964738"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="9e9bc-103">Vytváření finančních dimenzí pro maloobchodní sítě a konfigurace hodnot dimenzí v obchodech</span><span class="sxs-lookup"><span data-stu-id="9e9bc-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e9bc-104">Tato procedura vás provede vytvořením finanční dimenze kanálu commerce s hodnotami dimenzí a postupem pro konfiguraci hodnot finančních dimenzí v obchodech.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="9e9bc-105">Téma neobsahuje další související postup, jako je například vytváření sad dimenzí a účetních struktur.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="9e9bc-106">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9e9bc-107">Přejděte do části Hlavní kniha > Účtová osnova > Dimenze > Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="9e9bc-108">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-108">Click New.</span></span>
3. <span data-ttu-id="9e9bc-109">V poli Použít hodnoty od vyberte „Kanály Commerce“.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="9e9bc-110">Do pole Název dimenze zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="9e9bc-111">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-111">Click Activate.</span></span>
6. <span data-ttu-id="9e9bc-112">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-112">Click Close.</span></span>
7. <span data-ttu-id="9e9bc-113">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-113">Click Activate.</span></span>
8. <span data-ttu-id="9e9bc-114">Klepněte na Hodnoty dimenzí.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-114">Click Dimension values.</span></span>
9. <span data-ttu-id="9e9bc-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-115">Close the page.</span></span>
10. <span data-ttu-id="9e9bc-116">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-116">Click Save.</span></span>
11. <span data-ttu-id="9e9bc-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-117">Close the page.</span></span>
12. <span data-ttu-id="9e9bc-118">Přejděte na Maloobchodní a velkoobchodní prodej > Kanály > Obchody > Všechny obchody.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="9e9bc-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9e9bc-120">Rozbalte oddíl Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="9e9bc-121">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-121">Click Edit.</span></span>
16. <span data-ttu-id="9e9bc-122">V poli Kanál Commerce kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="9e9bc-123">V seznamu vyhledejte a vyberte hodnotu dimenze pro aktualizovaný obchod.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="9e9bc-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="9e9bc-125">V poli Nákladové středisko kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="9e9bc-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="9e9bc-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="9e9bc-128">V poli Oddělení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="9e9bc-129">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="9e9bc-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="9e9bc-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="9e9bc-131">Click Save.</span></span>


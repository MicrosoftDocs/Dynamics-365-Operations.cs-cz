---
title: Vytváření konfiguračních pravidel
description: Tento postup se zaměřuje na vytvoření konfiguračních pravidel, která lze použít pro konfiguraci založenou na dimenzích k vynucení nebo zamezení vzniku určitých kombinací řádků kusovníku.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bc0af4d95e9430d0b5c8b7fc9a4ade076802044
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423817"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="8ae64-103">Vytváření konfiguračních pravidel</span><span class="sxs-lookup"><span data-stu-id="8ae64-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ae64-104">Tento postup se zaměřuje na vytvoření konfiguračních pravidel, která lze použít pro konfiguraci založenou na dimenzích k vynucení nebo zamezení vzniku určitých kombinací řádků kusovníku.</span><span class="sxs-lookup"><span data-stu-id="8ae64-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="8ae64-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="8ae64-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8ae64-106">Jedná se o sedmý postup z osmi, který vysvětluje vytvoření kombinací konfigurace založené na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="8ae64-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="8ae64-107">Přejděte do nabídky Řízení informací o produktech > Kusovníky a receptury > Kusovníky.</span><span class="sxs-lookup"><span data-stu-id="8ae64-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="8ae64-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="8ae64-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8ae64-109">Najděte a vyberte kusovník pro konfiguraci založenou na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="8ae64-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="8ae64-110">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="8ae64-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="8ae64-111">Klikněte na tlačítko Změnit zobrazení.</span><span class="sxs-lookup"><span data-stu-id="8ae64-111">Click Change view.</span></span>
5. <span data-ttu-id="8ae64-112">Klikněte na možnost Zobrazení záhlaví.</span><span class="sxs-lookup"><span data-stu-id="8ae64-112">Click Header view.</span></span>
    * <span data-ttu-id="8ae64-113">Otevřením zobrazení záhlaví získejte přístup na pevnou záložku Konfigurační postup.</span><span class="sxs-lookup"><span data-stu-id="8ae64-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="8ae64-114">Rozbalte nebo sbalte oddíl Konfigurační postup.</span><span class="sxs-lookup"><span data-stu-id="8ae64-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="8ae64-115">Pevná záložka Konfigurační postup musí být v rozbaleném stavu.</span><span class="sxs-lookup"><span data-stu-id="8ae64-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="8ae64-116">Klikněte na možnost Konfigurační pravidla.</span><span class="sxs-lookup"><span data-stu-id="8ae64-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="8ae64-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8ae64-117">Click New.</span></span>
9. <span data-ttu-id="8ae64-118">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="8ae64-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="8ae64-119">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8ae64-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8ae64-120">Zobrazí se položky v aktuální konfigurační skupině.</span><span class="sxs-lookup"><span data-stu-id="8ae64-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="8ae64-121">Vyberte jednu, která představuje podmínku pravidla.</span><span class="sxs-lookup"><span data-stu-id="8ae64-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="8ae64-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="8ae64-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="8ae64-123">Vyberte volbu v poli Metoda.</span><span class="sxs-lookup"><span data-stu-id="8ae64-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="8ae64-124">Je možné vynutit volbu nebo zrušení volby položky z jiné konfigurační skupiny.</span><span class="sxs-lookup"><span data-stu-id="8ae64-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="8ae64-125">V poli Odvozená skupina kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8ae64-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="8ae64-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="8ae64-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="8ae64-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="8ae64-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8ae64-128">Vyberte požadovanou konfigurační skupinu.</span><span class="sxs-lookup"><span data-stu-id="8ae64-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="8ae64-129">V poli Odvozené číslo položky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8ae64-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="8ae64-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="8ae64-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8ae64-131">Vyberte číslo položky, které má být v závislosti na zvolené metodě vybráno nebo jehož volba má být zrušena.</span><span class="sxs-lookup"><span data-stu-id="8ae64-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="8ae64-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8ae64-132">Close the page.</span></span>


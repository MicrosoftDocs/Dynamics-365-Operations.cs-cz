---
title: "Pravidla přidělení hlavní knihy"
description: "Tento článek obsahuje informace o pravidlech přidělení hlavní knihy. Popisuje různé aspekty těchto pravidel přidělení a metod přidělení, které lze pro ně použít."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: abbeb1bb4481139dff902916362a479f94fb96e5
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="ledger-allocation-rules"></a><span data-ttu-id="b66f0-104">Pravidla přidělení hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="b66f0-104">Ledger allocation rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b66f0-105">Tento článek obsahuje informace o pravidlech přidělení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b66f0-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="b66f0-106">Popisuje různé aspekty těchto pravidel přidělení a metod přidělení, které lze pro ně použít.</span><span class="sxs-lookup"><span data-stu-id="b66f0-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="b66f0-107">Pravidla přidělení hlavní knihy se používají k automatickému výpočtu a generování deníků přidělení a účetních položek pro přidělování zůstatků hlavní knihy nebo pevných částek.</span><span class="sxs-lookup"><span data-stu-id="b66f0-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="b66f0-108">Metody přidělení mohou být proměnné nebo pevné.</span><span class="sxs-lookup"><span data-stu-id="b66f0-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="b66f0-109">Pro pravidla přidělení hlavní knihy můžete použít následující metody přidělení:</span><span class="sxs-lookup"><span data-stu-id="b66f0-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="b66f0-110">**Základ** – tato proměnná metody se používá, když přidělení závisí na skutečném zůstatku hlavní knihy na základě kritérií filtru.</span><span class="sxs-lookup"><span data-stu-id="b66f0-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="b66f0-111">Příklad: Výdaje společnosti na reklamu lze přidělit úměrně podle prodeje jednotlivých oddělení vzhledem k celkovému prodeji oddělení.</span><span class="sxs-lookup"><span data-stu-id="b66f0-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="b66f0-112">**Pevné procento** a **Pevná váha** – pro tyto metody je procentuální hodnota nebo váha přidělení definována přímo pro pravidlo.</span><span class="sxs-lookup"><span data-stu-id="b66f0-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="b66f0-113">Například výdaje na reklamu lze alokovat tak, aby oddělení A přijalo 70 procent výdajů na reklamu a oddělení B 30 procent.</span><span class="sxs-lookup"><span data-stu-id="b66f0-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="b66f0-114">**Rovnoměrně** – tato metoda distribuuje částku rovnoměrně mezi jednotlivé definované cíle.</span><span class="sxs-lookup"><span data-stu-id="b66f0-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="b66f0-115">Například pokud jsou místa určení definována pro oddělení A a B, náklady na reklamu lze rozdělit tak, aby na obě oddělení A a B připadlo 50 procent výdajů na reklamu.</span><span class="sxs-lookup"><span data-stu-id="b66f0-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="b66f0-116">Je-li použita metoda přidělení Základ pro pravidlo přidělení, je nutné definovat také samostatná pravidla základu přidělení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b66f0-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="b66f0-117">Proces "Požadavek na přidělení procesu" umožňuje uživatelům zpracovat pravidlo přidělení hlavní knihy a zobrazit náhled výsledných položek deníku přidělení před zaúčtováním nebo odstraněním vypočítaných přidělení.</span><span class="sxs-lookup"><span data-stu-id="b66f0-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="b66f0-118">Součásti pravidel přidělení hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="b66f0-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="b66f0-119">Každé pravidlo přidělení má čtyři komponenty: obecné údaje, zdroj, cíl a protiúčet.</span><span class="sxs-lookup"><span data-stu-id="b66f0-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="b66f0-120">Další komponenta, pravidla základu přidělení hlavní knihy, jsou požadována, je-li Základ použit jako metoda přidělení.</span><span class="sxs-lookup"><span data-stu-id="b66f0-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="b66f0-121">Každá komponenta poskytuje důležité informace potřebné ke zpracování přidělení.</span><span class="sxs-lookup"><span data-stu-id="b66f0-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="b66f0-122">**Obecné** – v této součásti uživatel určuje volby, jako například metodu přidělení, nastavení mezipodnikových pravidel a také to, zda má být pravidlo aktivní.</span><span class="sxs-lookup"><span data-stu-id="b66f0-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="b66f0-123">**Zdroj** – tato součást slouží uživateli k určení zdrojových dat pro přidělení.</span><span class="sxs-lookup"><span data-stu-id="b66f0-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="b66f0-124">Přidělení může být založeno na zůstatcích hlavní knihy (**Zdroj dat** = **Hlavní kniha**) nebo pevných částkách (**Zdroj dat** = **Pevná hodnota**).</span><span class="sxs-lookup"><span data-stu-id="b66f0-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="b66f0-125">Při nastavení možnosti **Zdroj dat** na hodnotu **Hlavní kniha** musí být definována kritéria filtru zdroje pro pravidlo přidělení hlavní knihy (například pro výdaje na reklamu).</span><span class="sxs-lookup"><span data-stu-id="b66f0-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="b66f0-126">**Cíl** – tato komponenta určuje způsob, jak má být výsledek výpočtu přidělení distribuován a zaúčtován.</span><span class="sxs-lookup"><span data-stu-id="b66f0-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="b66f0-127">Například může existovat jeden řádek cíle pro každé oddělení.</span><span class="sxs-lookup"><span data-stu-id="b66f0-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="b66f0-128">**Protiúčet** – tato komponenta určuje, jak mají být hlavní účty a dimenze určeny pro položky protiúčtu, které vyrovnávají položky cíle.</span><span class="sxs-lookup"><span data-stu-id="b66f0-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="b66f0-129">Namísto účtů a dimenzí založených na zdroji se obvykle používají uživatelem definované možnosti.</span><span class="sxs-lookup"><span data-stu-id="b66f0-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="b66f0-130">Při nastavení možnosti **Zdroj dat** na hodnotu **Pevná hodnota** nelze použít možnost **Zdroj**.</span><span class="sxs-lookup"><span data-stu-id="b66f0-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="b66f0-131">**Pravidla základu přidělení hlavní knihy** – tato pravidla používají vlastní kritéria filtru zdroje k určení, které zůstatky hlavní knihy mají být použity pro přidělení (například výnosy pro jednotlivá oddělení).</span><span class="sxs-lookup"><span data-stu-id="b66f0-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="b66f0-132">Každé pravidlo základu přidělení lze použít s více pravidly přidělení.</span><span class="sxs-lookup"><span data-stu-id="b66f0-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>






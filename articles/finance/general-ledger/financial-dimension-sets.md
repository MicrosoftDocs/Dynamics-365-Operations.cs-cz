---
title: Sady finančních dimenzí
description: Toto téma popisuje sady finančních dimenzí a poskytuje několik tipů pro optimalizaci jejich použití.
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ba11be028ebeea140df93e2a07dbb463402e3ef0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021821"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="49c84-103">Sady finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="49c84-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49c84-104">Toto téma popisuje sady finančních dimenzí a poskytuje několik tipů pro optimalizaci jejich použití.</span><span class="sxs-lookup"><span data-stu-id="49c84-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="49c84-105">Sada dimenzí je seřazený seznam finančních dimenzí, které lze použít k shrnutí dat hlavní knihy uživatelem definovaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="49c84-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="49c84-106">Primárním použitím sady dimenzí je definování předvahy.</span><span class="sxs-lookup"><span data-stu-id="49c84-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="49c84-107">Jedinou standardní sadou dimenzí je sada dimenzí, která obsahuje pouze hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="49c84-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="49c84-108">Stránku **Sady finanční dimenze** používáte pro vytváření a správu sad finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="49c84-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="49c84-109">Zůstatky sad dimenzí</span><span class="sxs-lookup"><span data-stu-id="49c84-109">Dimension set balances</span></span>

<span data-ttu-id="49c84-110">Sada dimenzí může mít zůstatky, které jsou založeny na jejích finančních dimenzích.</span><span class="sxs-lookup"><span data-stu-id="49c84-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="49c84-111">Zůstatky existují v hlavní knize a jsou založeny na definici sady dimenzí.</span><span class="sxs-lookup"><span data-stu-id="49c84-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="49c84-112">Zůstatky jsou shrnuty z údajů hlavní knihy, aby pomohly zlepšit výkon při jejich načtení (například při generování předvahy).</span><span class="sxs-lookup"><span data-stu-id="49c84-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="49c84-113">Vytvořit zůstatky</span><span class="sxs-lookup"><span data-stu-id="49c84-113">Create balances</span></span>

<span data-ttu-id="49c84-114">Použijte tlačítko **Vytvořit zůstatky** k inicializaci zůstatků pro sadu dimenzí, která aktuálně nemá zůstatky.</span><span class="sxs-lookup"><span data-stu-id="49c84-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="49c84-115">Doporučujeme omezit počet sad dimenzí, které mají zůstatky, protože aktualizace zůstatků ovlivňují všechny aktivity účtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="49c84-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="49c84-116">Aktualizovat zůstatky</span><span class="sxs-lookup"><span data-stu-id="49c84-116">Update balances</span></span>

<span data-ttu-id="49c84-117">Použijte tlačítko **Aktualizovat zůstatky** k zahrnutí nejnovější aktivity účtování hlavní knihy do zůstatků.</span><span class="sxs-lookup"><span data-stu-id="49c84-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="49c84-118">Aktualizace zůstatku jsou lehké operace.</span><span class="sxs-lookup"><span data-stu-id="49c84-118">Balance updates are light operations.</span></span> <span data-ttu-id="49c84-119">Musí zpracovat pouze aktivitu účtování hlavní knihy, ke které došlo od poslední aktualizace.</span><span class="sxs-lookup"><span data-stu-id="49c84-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="49c84-120">Zobrazení zkušebního zůstatku vynutí aktualizaci, aby se zajistilo, že zobrazené zůstatky jsou aktuální.</span><span class="sxs-lookup"><span data-stu-id="49c84-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="49c84-121">Zvažte použití opakované dávkové úlohy, aby aktualizace vašich nejčastěji používaných sad dimenzí byly rychlé.</span><span class="sxs-lookup"><span data-stu-id="49c84-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="49c84-122">Tímto způsobem pomáháte minimalizovat dobu, po kterou musí uživatelé zůstatku na předvahu čekat.</span><span class="sxs-lookup"><span data-stu-id="49c84-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="49c84-123">Znovu sestavit zůstatky</span><span class="sxs-lookup"><span data-stu-id="49c84-123">Rebuild balances</span></span>

<span data-ttu-id="49c84-124">Tlačítko **Znovu sestavit zůstatky** použijte pro opětovné vytvoření zůstatků od nuly.</span><span class="sxs-lookup"><span data-stu-id="49c84-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="49c84-125">Tímto způsobem pomůžete zajistit, aby odpovídaly údajům v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="49c84-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="49c84-126">Opětovné sestavení zůstatků vyžaduje spoustu zpracování a nemělo by se obvykle vyžadovat.</span><span class="sxs-lookup"><span data-stu-id="49c84-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="49c84-127">Pokud máte scénář, který pravidelně vyžaduje opětovné sestavení zůstatků, doporučujeme vám kontaktovat zákaznickou podporu.</span><span class="sxs-lookup"><span data-stu-id="49c84-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="49c84-128">Zákaznická podpora vám pomůže určit, proč zůstatky neodpovídají údajům v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="49c84-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="49c84-129">Vymazat zůstatky</span><span class="sxs-lookup"><span data-stu-id="49c84-129">Clear balances</span></span>

<span data-ttu-id="49c84-130">Tlačítko **Vymazat zůstatky** použijte k odstranění zůstatků a zastavení dalších aktualizací.</span><span class="sxs-lookup"><span data-stu-id="49c84-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="49c84-131">Sada dimenzí již nebude mít dopad na aktivity účtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="49c84-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="49c84-132">Další informace naleznete v tématu [Finanční dimenze](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="49c84-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

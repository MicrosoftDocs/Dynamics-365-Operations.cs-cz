---
title: Sady finančních dimenzí
description: Toto téma popisuje sady finančních dimenzí a poskytuje několik tipů pro optimalizaci jejich použití.
author: yukonpeegs
manager: AnnBe
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
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864405"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="4f476-103">Sady finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="4f476-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f476-104">Toto téma popisuje sady finančních dimenzí a poskytuje několik tipů pro optimalizaci jejich použití.</span><span class="sxs-lookup"><span data-stu-id="4f476-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="4f476-105">Sada dimenzí je seřazený seznam finančních dimenzí, které lze použít k shrnutí dat hlavní knihy uživatelem definovaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="4f476-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="4f476-106">Primárním použitím sady dimenzí je definování předvahy.</span><span class="sxs-lookup"><span data-stu-id="4f476-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="4f476-107">Jedinou standardní sadou dimenzí je sada dimenzí, která obsahuje pouze hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="4f476-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="4f476-108">Stránku **Sady finanční dimenze** používáte pro vytváření a správu sad finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="4f476-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="4f476-109">Zůstatky sad dimenzí</span><span class="sxs-lookup"><span data-stu-id="4f476-109">Dimension set balances</span></span>

<span data-ttu-id="4f476-110">Sada dimenzí může mít zůstatky, které jsou založeny na jejích finančních dimenzích.</span><span class="sxs-lookup"><span data-stu-id="4f476-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="4f476-111">Zůstatky existují v hlavní knize a jsou založeny na definici sady dimenzí.</span><span class="sxs-lookup"><span data-stu-id="4f476-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="4f476-112">Zůstatky jsou shrnuty z údajů hlavní knihy, aby pomohly zlepšit výkon při jejich načtení (například při generování předvahy).</span><span class="sxs-lookup"><span data-stu-id="4f476-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="4f476-113">Vytvořit zůstatky</span><span class="sxs-lookup"><span data-stu-id="4f476-113">Create balances</span></span>

<span data-ttu-id="4f476-114">Použijte tlačítko **Vytvořit zůstatky** k inicializaci zůstatků pro sadu dimenzí, která aktuálně nemá zůstatky.</span><span class="sxs-lookup"><span data-stu-id="4f476-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="4f476-115">Doporučujeme omezit počet sad dimenzí, které mají zůstatky, protože aktualizace zůstatků ovlivňují všechny aktivity účtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="4f476-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="4f476-116">Aktualizovat zůstatky</span><span class="sxs-lookup"><span data-stu-id="4f476-116">Update balances</span></span>

<span data-ttu-id="4f476-117">Použijte tlačítko **Aktualizovat zůstatky** k zahrnutí nejnovější aktivity účtování hlavní knihy do zůstatků.</span><span class="sxs-lookup"><span data-stu-id="4f476-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="4f476-118">Aktualizace zůstatku jsou lehké operace.</span><span class="sxs-lookup"><span data-stu-id="4f476-118">Balance updates are light operations.</span></span> <span data-ttu-id="4f476-119">Musí zpracovat pouze aktivitu účtování hlavní knihy, ke které došlo od poslední aktualizace.</span><span class="sxs-lookup"><span data-stu-id="4f476-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="4f476-120">Zobrazení zkušebního zůstatku vynutí aktualizaci, aby se zajistilo, že zobrazené zůstatky jsou aktuální.</span><span class="sxs-lookup"><span data-stu-id="4f476-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="4f476-121">Zvažte použití opakované dávkové úlohy, aby aktualizace vašich nejčastěji používaných sad dimenzí byly rychlé.</span><span class="sxs-lookup"><span data-stu-id="4f476-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="4f476-122">Tímto způsobem pomáháte minimalizovat dobu, po kterou musí uživatelé zůstatku na předvahu čekat.</span><span class="sxs-lookup"><span data-stu-id="4f476-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="4f476-123">Znovu sestavit zůstatky</span><span class="sxs-lookup"><span data-stu-id="4f476-123">Rebuild balances</span></span>

<span data-ttu-id="4f476-124">Tlačítko **Znovu sestavit zůstatky** použijte pro opětovné vytvoření zůstatků od nuly.</span><span class="sxs-lookup"><span data-stu-id="4f476-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="4f476-125">Tímto způsobem pomůžete zajistit, aby odpovídaly údajům v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="4f476-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="4f476-126">Opětovné sestavení zůstatků vyžaduje spoustu zpracování a nemělo by se obvykle vyžadovat.</span><span class="sxs-lookup"><span data-stu-id="4f476-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="4f476-127">Pokud máte scénář, který pravidelně vyžaduje opětovné sestavení zůstatků, doporučujeme vám kontaktovat zákaznickou podporu.</span><span class="sxs-lookup"><span data-stu-id="4f476-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="4f476-128">Zákaznická podpora vám pomůže určit, proč zůstatky neodpovídají údajům v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="4f476-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="4f476-129">Vymazat zůstatky</span><span class="sxs-lookup"><span data-stu-id="4f476-129">Clear balances</span></span>

<span data-ttu-id="4f476-130">Tlačítko **Vymazat zůstatky** použijte k odstranění zůstatků a zastavení dalších aktualizací.</span><span class="sxs-lookup"><span data-stu-id="4f476-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="4f476-131">Sada dimenzí již nebude mít dopad na aktivity účtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="4f476-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="4f476-132">Další informace naleznete v tématu [Finanční dimenze](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="4f476-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

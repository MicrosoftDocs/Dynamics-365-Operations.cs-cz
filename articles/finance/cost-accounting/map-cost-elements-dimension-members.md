---
title: Mapování členů dimenze prvků nákladů na společnou sadu členů dimenze
description: Mapováním různých členů dimenze prvku nákladů do sady běžné sady členů dimenze prvku nákladů slučujete data do běžného formátu pro účely analýzy.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6a9618a762d3af840beb05d86518b3588118e80
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976348"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="f5ca9-103">Mapování členů dimenze prvků nákladů na společnou sadu členů dimenze</span><span class="sxs-lookup"><span data-stu-id="f5ca9-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5ca9-104">Mapováním různých členů dimenze prvku nákladů do sady běžné sady členů dimenze prvku nákladů slučujete data do běžného formátu pro účely analýzy.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="f5ca9-105">Fungujete-li coby globální společnost a řídíte se požadavky účetnictví, můžete používat několik účtových osnov.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="f5ca9-106">Při importu členů dimenze prvku nákladů z různých účtových osnov sám může vzniknout směs účtů.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="f5ca9-107">Tyto účty však mohou mít stejný ráz a vy pro ně můžete chtít analyzovat a přidělovat náklady pomocí běžného formátu.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="f5ca9-108">Mapovat členy dimenze prvku nákladů do běžného formátu</span><span class="sxs-lookup"><span data-stu-id="f5ca9-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="f5ca9-109">Následující příklad ukazuje, jak vy, coby správce nákladů, můžete vytvořit nový prvek dimenze nákladů v nákladovém účetnictví, který mapuje členy dimenze prvku nákladů v americké struktuře účtové osnovy a francouzské struktuře účtové osnovy do běžné sady členů dimenze prvku nákladů.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="f5ca9-110">Poté můžete použít běžnou sadu členů dimenze prvku nákladů k analýze dat nákladů ze dvou právnických osob v hlavní knize nákladového účetnictví.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="f5ca9-111">Zdroj: americká účtová osnova</span><span class="sxs-lookup"><span data-stu-id="f5ca9-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="f5ca9-112">Zdroj: francouzská účtová osnova</span><span class="sxs-lookup"><span data-stu-id="f5ca9-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="f5ca9-113">Nová běžná sada členů dimenze prvku nákladů</span><span class="sxs-lookup"><span data-stu-id="f5ca9-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f5ca9-114">Importované členy dimenze prvku nákladů z americké účtové osnovy</span><span class="sxs-lookup"><span data-stu-id="f5ca9-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="f5ca9-115">Importované členy dimenze prvku nákladů z francouzské účtové osnovy</span><span class="sxs-lookup"><span data-stu-id="f5ca9-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="f5ca9-116">Mapovat americké a francouzské členy dimenze prvku nákladů do běžné sady</span><span class="sxs-lookup"><span data-stu-id="f5ca9-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="f5ca9-117">5001: Prodej</span><span class="sxs-lookup"><span data-stu-id="f5ca9-117">5001: Sales</span></span>                                                           | <span data-ttu-id="f5ca9-118">5001: Prodej a marketing</span><span class="sxs-lookup"><span data-stu-id="f5ca9-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="f5ca9-119">5000: Prodej a marketing</span><span class="sxs-lookup"><span data-stu-id="f5ca9-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="f5ca9-120">5030: Reklama</span><span class="sxs-lookup"><span data-stu-id="f5ca9-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="f5ca9-121">6390: Skladový nákup\*</span><span class="sxs-lookup"><span data-stu-id="f5ca9-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="f5ca9-122">7000: náklady na úklid</span><span class="sxs-lookup"><span data-stu-id="f5ca9-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="f5ca9-123">7001: náklady na úklid</span><span class="sxs-lookup"><span data-stu-id="f5ca9-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="f5ca9-124">7001: Cestovní výdaje</span><span class="sxs-lookup"><span data-stu-id="f5ca9-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="f5ca9-125">7001: Cestovné a výdaje</span><span class="sxs-lookup"><span data-stu-id="f5ca9-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="f5ca9-126">\*Skladový nákup francouzského prvku dimenze prvku nákladů není zmapován.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="f5ca9-127">Převod měny</span><span class="sxs-lookup"><span data-stu-id="f5ca9-127">Currency conversion</span></span>
<span data-ttu-id="f5ca9-128">Různé účtové osnovy, které používáte, jsou pravděpodobně nastaveny pro použití v různých měnách.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="f5ca9-129">V takovém případě je nutné zadat převod měny tak, aby data nákladů byla zpracovávána ve správné měně do hlavní knihy nákladového účetnictví, kde se používají členy dimenze prvku nákladů.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="f5ca9-130">V předcházejícím příkladu, pokud by se používaly americké dolary (USD) v hlavní knize nákladového účetnictví, museli byste vytvořit převod měny z USD do euro (EUR), aby mohlo dojít ke zpracování transakcí pro mapování členů dimenze prvku nákladů.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="f5ca9-131">Kdykoli aktualizujte mapování</span><span class="sxs-lookup"><span data-stu-id="f5ca9-131">Update mappings at any time</span></span>
<span data-ttu-id="f5ca9-132">Kdykoli můžete aktualizovat upřesnění mapování dimenze prvku nákladů.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="f5ca9-133">Vzhledem k tomu, že mapování nejsou časově efektivní, změny se projeví, až budete příště zpracovávat transakce nákladů nebo provádět výpočty nákladových.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>




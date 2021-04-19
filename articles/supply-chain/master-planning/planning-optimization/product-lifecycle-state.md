---
title: Vyloučení produktů s konkrétními stavy životního cyklu produktu
description: Toto téma vysvětluje, jak vyloučit produkty na základě jejich stavu životního cyklu při použití funkce Optimalizace plánování.
author: ChristianRytt
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7028a509aa884589958542f7ec627d69dffcfcec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839240"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="01a01-103">Vyloučení produktů s konkrétními stavy životního cyklu produktu</span><span class="sxs-lookup"><span data-stu-id="01a01-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01a01-104">Uvolněné produkty a uvolněné verze produktů obsahují pole **Stav životního cyklu produktu**.</span><span class="sxs-lookup"><span data-stu-id="01a01-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="01a01-105">Toto pole umožňuje mimo jiné řídit, které produkty jsou zahrnuty během hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="01a01-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="01a01-106">Stavy životního cyklu můžete podle potřeby přidávat, odebírat a upravovat přechodem na **Správa informací o produktu \> Nastavit \> Stav životního cyklu produktu**.</span><span class="sxs-lookup"><span data-stu-id="01a01-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="01a01-107">Pro každý stav životního cyklu produktu nastavte možnost **Je aktivní pro plánování** na *Ano*, pokud by během hlavního plánování měly být zahrnuty produkty, které mají tento stav.</span><span class="sxs-lookup"><span data-stu-id="01a01-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="01a01-108">Když je možnost nastavena na *Ne*, přidružené produkty a varianty budou vyloučeny ze všech hlavních plánování a všech výpočtů na úrovni kusovníku (BOM).</span><span class="sxs-lookup"><span data-stu-id="01a01-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="01a01-109">S vydanými produkty a variantami, kde pole **Stav životního cyklu produktu** je ponecháno prázdné, se zachází způsobem, jako by měly stav životního cyklu produktu, kde možnost **Je aktivní pro plánování** je nastavena na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="01a01-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="01a01-110">Jinými slovy budou zahrnuty během hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="01a01-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="01a01-111">Abychom se vyhnuli zbytečným návrhům dodávek, důrazně doporučujeme, abyste všechny zastaralé uvolněné produkty a varianty přidružili ke stavu životního cyklu produktu, kde je možnost **Je aktivní pro plánování** nastavena na *Ne*.</span><span class="sxs-lookup"><span data-stu-id="01a01-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="01a01-112">Tento přístup je obzvláště důležitý, když pracujete s variantami konfigurace produktu, které nelze opakovaně použít, protože to pomůže zabránit plýtvání.</span><span class="sxs-lookup"><span data-stu-id="01a01-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="01a01-113">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="01a01-113">Related resources</span></span>

<span data-ttu-id="01a01-114">Další informace o stavech životního cyklu produktu najdete v části [Přehled stavu životního cyklu produktu](../../pim/product-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="01a01-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="01a01-115">Podrobné informace, které zahrnují kroky pro použití stavů životního cyklu produktu k vyloučení produktů z hlavního plánování a výpočtů na úrovni kusovníku, najdete v části [Vytvoření stavu životního cyklu produktu k vyloučení produktů z hlavního plánování](../../pim/tasks/exclude-products-master-planning.md).</span><span class="sxs-lookup"><span data-stu-id="01a01-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
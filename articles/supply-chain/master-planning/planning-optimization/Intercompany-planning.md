---
title: Mezipodnikové plánování
description: Toto téma popisuje mezipodnikové plánování a vysvětluje, jak nakonfigurovat mezipodnikové plánování pomocí optimalizace plánování v Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 12/02/2020
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
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e6fff06cb6194f17444025f7ea1f9dbb46e4f3ea
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907636"
---
# <a name="intercompany-planning"></a><span data-ttu-id="ea5c3-103">Mezipodnikové plánování</span><span class="sxs-lookup"><span data-stu-id="ea5c3-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea5c3-104">U některých organizací závisí logistické operace na jiných právnických osobách (společnostech) v organizaci.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="ea5c3-105">Tyto operace jsou zpracovávány pomocí mezipodnikových prodejů a nákupů, protože každá právnická osoba má samostatnou účtovou osnovu.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="ea5c3-106">Toto téma popisuje mezipodnikové plánování a vysvětluje, jak nakonfigurovat mezipodnikové plánování pomocí optimalizace plánování v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="ea5c3-107">Toto téma používá následující důležité mezipodnikové výrazy:</span><span class="sxs-lookup"><span data-stu-id="ea5c3-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="ea5c3-108">**Směrem k dodavateli** - Relativní reference ve firmě nebo dodavatelském řetězci.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="ea5c3-109">Indikuje pohyb ve směru k dodavateli suroviny.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="ea5c3-110">**Směrem ke spotřebiteli** - Relativní reference ve firmě nebo dodavatelském řetězci.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="ea5c3-111">Indikuje pohyb ve směru k zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="ea5c3-112">**Plánovaná mezipodniková poptávka** - Plánovaná poptávka po produktu ve společnosti na základě plánované poptávky po produktu od navazující společnosti.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="ea5c3-113">V hlavním plánování může plán v jedné společnosti zahrnovat plánovanou mezipodnikovou poptávku, která souvisí s plánovanými objednávkami z plánu v jiné společnosti.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="ea5c3-114">Tato funkce je užitečná, protože poskytuje úplný přehled o plánovaných objednávkách napříč společnostmi.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="ea5c3-115">Zajišťuje také, že jsou vytvořeny všechny požadované plánované objednávky dodávek, ale bez požadavku, aby byly plánované objednávky zpracovány pro mezipodnikovou poptávku.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="ea5c3-116">Pokud spustíte hlavní plánování z hlavního plánu, který zahrnuje plánovanou následnou poptávku, plánované nákupní objednávky od příslušných mezipodnikových dodavatelů budou zahrnuty do plánu jako poptávka.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="ea5c3-117">Požadované nastavení</span><span class="sxs-lookup"><span data-stu-id="ea5c3-117">Required setup</span></span>

<span data-ttu-id="ea5c3-118">Chcete-li použít mezipodnikové plánování, musíte svůj systém připravit následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="ea5c3-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="ea5c3-119">Příslušné produkty musí být uvolněny ve všech příslušných společnostech.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="ea5c3-120">Další informace naleznete v tématu [Konfigurace a použití mezipodnikového obchodu v Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) na Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="ea5c3-121">Následná poptávka musí být pokryta nákupy od dodavatele, který má mezipodnikový vztah k předcházející společnosti a relevantní výchozí dimenze zásob (pracoviště a sklad) na zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="ea5c3-122">Další informace naleznete v tématu [Konfigurace a použití mezipodnikového obchodu v Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) na Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management](/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="ea5c3-123">Hlavní plán v předcházející společnosti musí zahrnovat plánovanou následnou poptávku a příslušná společnost a hlavní plán musí být specifikovány v následných plánech.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="ea5c3-124">Zahrnout podřízenou plánovanou poptávku</span><span class="sxs-lookup"><span data-stu-id="ea5c3-124">Include planned downstream demand</span></span>

<span data-ttu-id="ea5c3-125">Podle těchto pokynů nakonfigurujte svůj hlavní plán tak, aby zahrnoval plánovanou následnou poptávku.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="ea5c3-126">Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="ea5c3-127">Vyberte nebo vytvořte hlavní plán.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="ea5c3-128">Na záložce s náhledem **Mezipodnikové plánování** zadejte následující pole:</span><span class="sxs-lookup"><span data-stu-id="ea5c3-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="ea5c3-129">**Zahrnout plánovanou následnou poptávku** - Nastavte tuto možnost na *Ano*, čímž umožníte mezipodnikové plánování pro hlavní plán.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="ea5c3-130">**Následné plány** - Pokud nastavíte možnost **Zahrnout plánovanou následnou poptávku** na *Ano*, použijte panel nástrojů a mřížku a přidejte požadované hlavní plány od jiných společností.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="ea5c3-131">Dokládání napříč společnostmi pomocí víceúrovňového doložení</span><span class="sxs-lookup"><span data-stu-id="ea5c3-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="ea5c3-132">Ve víceúrovňovém doložení můžete zobrazit doložení napříč společnostmi, abyste viděli počáteční zdroj poptávky, který je krytý nabídkou.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="ea5c3-133">Chcete-li zobrazit informace o víceúrovňovém doložení, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="ea5c3-134">Přejděte na **Hlavní plánování \> Hlavní plánování \> Plánované objednávky**.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="ea5c3-135">Vyberte nebo otevřete plánovanou objednávku.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="ea5c3-136">V podokně akcí na kartě **Zobrazit** ve skupině **Požadavky** vyberte **Víceúrovňové doložení**.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="ea5c3-137">Mezipodnikový příklad, který zahrnuje dvě společnosti</span><span class="sxs-lookup"><span data-stu-id="ea5c3-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="ea5c3-138">V tomto příkladu je ve společnosti USMF vytvořena plánovaná výrobní zakázka, která pokryje prodejní objednávku ve společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="ea5c3-139">V USMF je přímá poptávka plánovanou mezipodnikovou poptávkou.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="ea5c3-140">Aby se tato poptávka objevila v USMF, je hlavní plánování spuštěno nejprve v DEMF a poté v USMF.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="ea5c3-141">Následující ilustrace ukazuje, jak by se tento příklad mohl objevit na stránce **Víceúrovňové zakotvení** pro plánovanou výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Mezipodnikový příklad, který zahrnuje dvě společnosti](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="ea5c3-143">Mezipodnikový příklad, který zahrnuje tři společnosti</span><span class="sxs-lookup"><span data-stu-id="ea5c3-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="ea5c3-144">V tomto příkladu je ve společnosti USMF vytvořena plánovaná nákupní objednávka, která pokryje prodejní objednávku ve společnosti FRRT.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="ea5c3-145">Ve společnostech DEMF a USMF je přímá poptávka plánovanou mezipodnikovou poptávkou.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="ea5c3-146">Aby se tato poptávka objevila v USMF, je hlavní plánování spuštěno nejprve v FRRT, poté v DEMF a nakonec v USMF.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="ea5c3-147">Následující ilustrace ukazuje, jak by se tento příklad mohl objevit na stránce **Víceúrovňové zakotvení** pro plánovanou výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="ea5c3-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Mezipodnikový příklad, který zahrnuje tři společnosti](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
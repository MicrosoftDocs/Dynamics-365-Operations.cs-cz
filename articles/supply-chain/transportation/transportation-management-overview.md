---
title: Přehled správy přepravy
description: Toto téma poskytuje přehled správy přepravy v aplikaci Supply Chain Management.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4affc5846ee329a4571d6fb3e0c42873387241ad
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016371"
---
# <a name="transportation-management-overview"></a><span data-ttu-id="c2575-103">Přehled správy přepravy</span><span class="sxs-lookup"><span data-stu-id="c2575-103">Transportation management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2575-104">Toto téma poskytuje přehled správy přepravy v aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c2575-104">This topic gives an overview of the transportation management functionality in Supply Chain Management.</span></span>

<span data-ttu-id="c2575-105">Modul Správa přepravy slouží ke správě přepravy ve vaší společnosti a zároveň určování dodavatelů a řešení trasy pro vstupní a výstupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="c2575-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="c2575-106">Můžete například určit nejrychlejší trasu nebo nejlevnější sazbu pro dodávku.</span><span class="sxs-lookup"><span data-stu-id="c2575-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="c2575-107">V následující tabulce jsou popsány základní scénáře používání modulu Správa přepravy.</span><span class="sxs-lookup"><span data-stu-id="c2575-107">The following table describes the main scenarios for using Transportation management.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c2575-108">Scénář</span><span class="sxs-lookup"><span data-stu-id="c2575-108">Scenario</span></span></th>
<th><span data-ttu-id="c2575-109">Možnosti modulu Správa přepravy</span><span class="sxs-lookup"><span data-stu-id="c2575-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c2575-110">Použití externích poskytovatelů logistiky pro činností přepravy.</span><span class="sxs-lookup"><span data-stu-id="c2575-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="c2575-111">Použití modulu Správa přepravy pro příchozí a/nebo odchozí přepravu.</span><span class="sxs-lookup"><span data-stu-id="c2575-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2575-112">Vlastní vozový park společnosti je k dispozici pro doručení/výdej – náklady na dodání se přenáší na odběratele.</span><span class="sxs-lookup"><span data-stu-id="c2575-112">The company&#39;s own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="c2575-113">Pro výstupní procesy můžete pomocí modulu Správa přepravy určit náklady na dopravu a předat je na odběratele.</span><span class="sxs-lookup"><span data-stu-id="c2575-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="c2575-114">Nicméně proces vyrovnání faktury s dopravcem není vyžadován.</span><span class="sxs-lookup"><span data-stu-id="c2575-114">However, the carrier invoice reconciliation process isn&#39;t required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c2575-115">Vozový park společnosti je k dispozici pro doručení/výdej, ale náklady na doručení se nepředávají odběratelům, protože ceny produktu zahrnují přepravu.</span><span class="sxs-lookup"><span data-stu-id="c2575-115">The company&#39;s own fleet is available for delivery/pickup, but delivery charges aren&#39;t passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="c2575-116">Není požadováno velké množství funkcí pro správu přepravy.</span><span class="sxs-lookup"><span data-stu-id="c2575-116">A lot of the Transportation management functionality isn&#39;t required.</span></span> <span data-ttu-id="c2575-117">Nicméně modul Správa přepravy můžete použít a určit s ním sazbu přepravy a odpovídajícím způsobem upravit prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="c2575-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c2575-118">Služby z oblasti logistiky jsou poskytovány jinou právnickou osobou ve stejné společnosti.</span><span class="sxs-lookup"><span data-stu-id="c2575-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="c2575-119">Modul Správa přepravy můžete použít pro zacházení s jinými právními subjekty stejně jako s jiným dopravcem.</span><span class="sxs-lookup"><span data-stu-id="c2575-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="c2575-120">Nelze automaticky provádět ekonomické transakce mezi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="c2575-120">You can&#39;t automate the economic transactions between legal entities.</span></span> <span data-ttu-id="c2575-121">Z tohoto důvodu je nutné zpracovat tyto transakce ručně (například: vytvořením nákupní objednávky).</span><span class="sxs-lookup"><span data-stu-id="c2575-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="c2575-122">V právnické osobě, která poskytuje služby z oblasti logistiky, je možné modul Správa přepravy použít k určení sazeb přepravy.</span><span class="sxs-lookup"><span data-stu-id="c2575-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a><span data-ttu-id="c2575-123">Plánování přepravy v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c2575-123">Planning transportation in Supply Chain Management</span></span>
<span data-ttu-id="c2575-124">V modulu Správa přepravy lze dopravní plánování založit na objednávkách nebo na dodávkách, které jsou vytvořeny na základě těchto objednávek.</span><span class="sxs-lookup"><span data-stu-id="c2575-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="c2575-125">Dodávky vždy v každém okamžiku existují, ale nejsou požadovány pro plánování přepravy.</span><span class="sxs-lookup"><span data-stu-id="c2575-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="c2575-126">Převodní příkazy jsou součástí odchozího scénáře a je možné je plánovat společně s prodejními objednávkami.</span><span class="sxs-lookup"><span data-stu-id="c2575-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Načíst výkres](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="c2575-128">Příchozí přeprava</span><span class="sxs-lookup"><span data-stu-id="c2575-128">Inbound transportation</span></span>
<span data-ttu-id="c2575-129">Pokud objednáváte od dodavatele zboží, které je potřeba dodat na sklad, pravděpodobně budete chtít zajistitt přepravu tohoto zboží sami.</span><span class="sxs-lookup"><span data-stu-id="c2575-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="c2575-130">Pomocí aplikace Supply Chain Management můžete naplánovat přepravu i převzetí příchozího nákladu.</span><span class="sxs-lookup"><span data-stu-id="c2575-130">You can use Supply Chain Management to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="c2575-131">Následující obrázek znázorňuje tok obchodního procesu pro plánování přepravy příchozího nákladu.</span><span class="sxs-lookup"><span data-stu-id="c2575-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Obchodní proces: průběh přepravy pro vstupní náklady](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="c2575-133">Odchozí přeprava</span><span class="sxs-lookup"><span data-stu-id="c2575-133">Outbound transportation</span></span>
<span data-ttu-id="c2575-134">Můžete naplánovat a zpracovat odchozí náklad a dodat tak konkrétní položky ze skladu společnosti odběrateli.</span><span class="sxs-lookup"><span data-stu-id="c2575-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="c2575-135">Pomocí aplikace Supply Chain Management můžete naplánovat přepravu i expedici odchozího nákladu.</span><span class="sxs-lookup"><span data-stu-id="c2575-135">You can use Supply Chain Management to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="c2575-136">Následující obrázek znázorňuje tok obchodního procesu pro plánování a zpracování odchozích nákladů pro expedici.</span><span class="sxs-lookup"><span data-stu-id="c2575-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Plánování a zpracování odchozích nákladů](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="c2575-138">Sestavení vytížení</span><span class="sxs-lookup"><span data-stu-id="c2575-138">Load building</span></span>
<span data-ttu-id="c2575-139">Aplikace Supply Chain Management obsahuje strategii sestavení vytížení, která se nazývá Strategie sestavení vytížení založená na objemu.</span><span class="sxs-lookup"><span data-stu-id="c2575-139">Supply Chain Management provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="c2575-140">Tato strategie umožňuje použít maximální hodnoty zadané pro výšku a hmotnost v šabloně vytížení nebo přepsat nastavení zadáním nových hodnot.</span><span class="sxs-lookup"><span data-stu-id="c2575-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="c2575-141">Pokud chcete použít tuto strategii, vyberte ji v poli **Strategie sestavení vytížení** na pevné záložce **Nastavení** na stránce **Pracovní plocha sestavení vytížení**.</span><span class="sxs-lookup"><span data-stu-id="c2575-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="c2575-142">Kromě toho můžete přidat vlastní strategie sestavení vytížení vytvořením nové třídy ve stromu aplikačních objektů (AOT).</span><span class="sxs-lookup"><span data-stu-id="c2575-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>




---
title: "Přehled správy přepravy"
description: "Toto téma poskytuje přehled o funkci správy přepravy v aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1c71c8f6c4f94342ac18cbfb7dfbc02ddb3f9f35
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="transportation-management-overview"></a><span data-ttu-id="26c64-103">Přehled správy přepravy</span><span class="sxs-lookup"><span data-stu-id="26c64-103">Transportation management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="26c64-104">Toto téma poskytuje přehled o funkci správy přepravy v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="26c64-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="26c64-105">Modul Správa přepravy slouží ke správě přepravy ve vaší společnosti a zároveň určování dodavatelů a řešení trasy pro vstupní a výstupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="26c64-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="26c64-106">Můžete například určit nejrychlejší trasu nebo nejlevnější sazbu pro dodávku.</span><span class="sxs-lookup"><span data-stu-id="26c64-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="26c64-107">V následující tabulce jsou popsány základní scénáře používání modulu Správa přepravy v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="26c64-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26c64-108">Scénář</span><span class="sxs-lookup"><span data-stu-id="26c64-108">Scenario</span></span></th>
<th><span data-ttu-id="26c64-109">Možnosti modulu Správa přepravy</span><span class="sxs-lookup"><span data-stu-id="26c64-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26c64-110">Použití externích poskytovatelů logistiky pro činností přepravy.</span><span class="sxs-lookup"><span data-stu-id="26c64-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="26c64-111">Použití modulu Správa přepravy pro příchozí a/nebo odchozí přepravu.</span><span class="sxs-lookup"><span data-stu-id="26c64-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26c64-112">Vlastní vozový park společnosti je k dispozici pro doručení/výdej – náklady na dodání se přenáší na odběratele.</span><span class="sxs-lookup"><span data-stu-id="26c64-112">The company's own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="26c64-113">Pro výstupní procesy můžete pomocí modulu Správa přepravy určit náklady na dopravu a předat je na odběratele.</span><span class="sxs-lookup"><span data-stu-id="26c64-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="26c64-114">Nicméně proces vyrovnání faktury s dopravcem není vyžadován.</span><span class="sxs-lookup"><span data-stu-id="26c64-114">However, the carrier invoice reconciliation process isn't required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26c64-115">Vozový park společnosti je k dispozici pro doručení/výdej, ale náklady na doručení se nepředávají odběratelům, protože ceny produktu zahrnují přepravu.</span><span class="sxs-lookup"><span data-stu-id="26c64-115">The company's own fleet is available for delivery/pickup, but delivery charges aren't passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="26c64-116">Není požadováno velké množství funkcí pro správu přepravy.</span><span class="sxs-lookup"><span data-stu-id="26c64-116">A lot of the Transportation management functionality isn't required.</span></span> <span data-ttu-id="26c64-117">Nicméně modul Správa přepravy můžete použít a určit s ním sazbu přepravy a odpovídajícím způsobem upravit prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="26c64-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26c64-118">Služby z oblasti logistiky jsou poskytovány jinou právnickou osobou ve stejné společnosti.</span><span class="sxs-lookup"><span data-stu-id="26c64-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="26c64-119">Modul Správa přepravy můžete použít pro zacházení s jinými právními subjekty stejně jako s jiným dopravcem.</span><span class="sxs-lookup"><span data-stu-id="26c64-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="26c64-120">Nelze automaticky provádět ekonomické transakce mezi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="26c64-120">You can't automate the economic transactions between legal entities.</span></span> <span data-ttu-id="26c64-121">Z tohoto důvodu je nutné zpracovat tyto transakce ručně (například: vytvořením nákupní objednávky).</span><span class="sxs-lookup"><span data-stu-id="26c64-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="26c64-122">V právnické osobě, která poskytuje služby z oblasti logistiky, je možné modul Správa přepravy použít k určení sazeb přepravy.</span><span class="sxs-lookup"><span data-stu-id="26c64-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="26c64-123">Plánování přepravy v modulu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="26c64-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="26c64-124">V modulu Správa přepravy lze dopravní plánování založit na objednávkách nebo na dodávkách, které jsou vytvořeny na základě těchto objednávek.</span><span class="sxs-lookup"><span data-stu-id="26c64-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="26c64-125">Dodávky vždy v každém okamžiku existují, ale nejsou požadovány pro plánování přepravy.</span><span class="sxs-lookup"><span data-stu-id="26c64-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="26c64-126">Převodní příkazy jsou součástí odchozího scénáře a je možné je plánovat společně s prodejními objednávkami.</span><span class="sxs-lookup"><span data-stu-id="26c64-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Načíst výkres](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="26c64-128">Příchozí přeprava</span><span class="sxs-lookup"><span data-stu-id="26c64-128">Inbound transportation</span></span>
<span data-ttu-id="26c64-129">Pokud objednáváte od dodavatele zboží, které je potřeba dodat na sklad, pravděpodobně budete chtít zajistitt přepravu tohoto zboží sami.</span><span class="sxs-lookup"><span data-stu-id="26c64-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="26c64-130">Pomocí aplikace Finance and Operations můžete naplánovat přepravu i převzetí příchozího nákladu.</span><span class="sxs-lookup"><span data-stu-id="26c64-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="26c64-131">Následující obrázek znázorňuje tok obchodního procesu pro plánování přepravy příchozího nákladu.</span><span class="sxs-lookup"><span data-stu-id="26c64-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Obchodní proces: průběh přepravy pro vstupní náklady](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="26c64-133">Odchozí přeprava</span><span class="sxs-lookup"><span data-stu-id="26c64-133">Outbound transportation</span></span>
<span data-ttu-id="26c64-134">Můžete naplánovat a zpracovat odchozí náklad a dodat tak konkrétní položky ze skladu společnosti odběrateli.</span><span class="sxs-lookup"><span data-stu-id="26c64-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="26c64-135">Pomocí aplikace Finance and Operations můžete naplánovat přepravu a doručení odchozího nákladu.</span><span class="sxs-lookup"><span data-stu-id="26c64-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="26c64-136">Následující obrázek znázorňuje tok obchodního procesu pro plánování a zpracování odchozích nákladů pro expedici.</span><span class="sxs-lookup"><span data-stu-id="26c64-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Plánování a zpracování odchozích nákladů](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="26c64-138">Sestavení vytížení</span><span class="sxs-lookup"><span data-stu-id="26c64-138">Load building</span></span>
<span data-ttu-id="26c64-139">Aplikace Finance and Operations obsahuje strategii sestavení vytížení, která se nazývá Strategie sestavení vytížení založená na objemu.</span><span class="sxs-lookup"><span data-stu-id="26c64-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="26c64-140">Tato strategie umožňuje použít maximální hodnoty zadané pro výšku a hmotnost v šabloně vytížení nebo přepsat nastavení zadáním nových hodnot.</span><span class="sxs-lookup"><span data-stu-id="26c64-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="26c64-141">Pokud chcete použít tuto strategii, vyberte ji v poli **Strategie sestavení vytížení** na pevné záložce **Nastavení** na stránce **Pracovní plocha sestavení vytížení**.</span><span class="sxs-lookup"><span data-stu-id="26c64-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="26c64-142">Kromě toho můžete přidat vlastní strategie sestavení vytížení vytvořením nové třídy ve stromu aplikačních objektů (AOT).</span><span class="sxs-lookup"><span data-stu-id="26c64-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>





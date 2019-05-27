---
title: Kontrola dostupnosti zásob
description: Tento postup popisuje způsob kontroly množství na skladě a zásob fyzicky k dispozici pro určité číslo položky.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26a8f51eda1f4249862a23fa0103b7a144d974a1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549857"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="8303a-103">Kontrola dostupnosti zásob</span><span class="sxs-lookup"><span data-stu-id="8303a-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8303a-104">Tento postup popisuje způsob kontroly množství na skladě a zásob fyzicky k dispozici pro určité číslo položky.</span><span class="sxs-lookup"><span data-stu-id="8303a-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="8303a-105">Také ukazuje, jak získat informace o zásobách související s položkou.</span><span class="sxs-lookup"><span data-stu-id="8303a-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="8303a-106">Fyzické zásoby na skladě je množství na skladě, které je k dispozici – tedy, je zakoupené, přijaté a registrované.</span><span class="sxs-lookup"><span data-stu-id="8303a-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="8303a-107">Množství na skladě zahrnuje dostupné zásoby na skladě, ale i zásoby, které byly objednány a jsou očekávané, ale dosud nebyly přijaty nebo registrovány.</span><span class="sxs-lookup"><span data-stu-id="8303a-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="8303a-108">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="8303a-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="8303a-109">Pokud používáte USMF, můžete použít ukázkové hodnoty, které jsou zobrazeny.</span><span class="sxs-lookup"><span data-stu-id="8303a-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="8303a-110">Tyto úkoly obvykle provádějí pracovníci skladu.</span><span class="sxs-lookup"><span data-stu-id="8303a-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="8303a-111">Kontrola zásob na skladě pro konkrétní položku</span><span class="sxs-lookup"><span data-stu-id="8303a-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="8303a-112">Přejděte na Řízení zásob > Dotazy a sestavy > Zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="8303a-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="8303a-113">Vyberte řádek Číslo položky.</span><span class="sxs-lookup"><span data-stu-id="8303a-113">Select the Item number row.</span></span>
    * <span data-ttu-id="8303a-114">Pokud chcete vytvořit dotaz na množství na skladě podle čísla položky, vyberte řádek, kde je Tabulka nastavena na Množství na skladě, a Pole je nastaveno na Číslo položky.</span><span class="sxs-lookup"><span data-stu-id="8303a-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="8303a-115">V poli Kritéria vyberte položku, pro kterou chcete vytvořit dotaz.</span><span class="sxs-lookup"><span data-stu-id="8303a-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="8303a-116">V případě, že používáte ukázková data společnosti USMF, můžete vybrat 'M9201'.</span><span class="sxs-lookup"><span data-stu-id="8303a-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="8303a-117">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8303a-117">Click OK.</span></span>
5. <span data-ttu-id="8303a-118">Klikněte na Dimenze.</span><span class="sxs-lookup"><span data-stu-id="8303a-118">Click Dimensions.</span></span>
    * <span data-ttu-id="8303a-119">Karta Dimenze umožňuje vybrat způsob, jak podrobné údaje chcete zobrazit o množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="8303a-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="8303a-120">Pokud potřebujete data související s rezervací, musíte zobrazit všechny dimenze zásob pro položky používající procesy rozšířené skladu (řízení skladu).</span><span class="sxs-lookup"><span data-stu-id="8303a-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="8303a-121">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8303a-121">Click OK.</span></span>
7. <span data-ttu-id="8303a-122">V podokně akcí klikněte na možnost Související informace.</span><span class="sxs-lookup"><span data-stu-id="8303a-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="8303a-123">Pokud tyto informace vidět nepotřebujete, klikněte na tlačítko se třemi tečkami (...) a otevřete tak další možnosti v podokně.</span><span class="sxs-lookup"><span data-stu-id="8303a-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="8303a-124">Klikněte na Přehled dodávek.</span><span class="sxs-lookup"><span data-stu-id="8303a-124">Click Supply overview.</span></span>
    * <span data-ttu-id="8303a-125">Karta Přehled dodávek obsahuje informace o zásobách pro určitou položku, jako je například množství na skladě, doba realizace a informace o dodavateli.</span><span class="sxs-lookup"><span data-stu-id="8303a-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="8303a-126">Rozbalte sekci Na skladě.</span><span class="sxs-lookup"><span data-stu-id="8303a-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="8303a-127">Rozbalte sekci Dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="8303a-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="8303a-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8303a-128">Close the page.</span></span>
12. <span data-ttu-id="8303a-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8303a-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="8303a-130">Kontrola fyzického množství na skladě</span><span class="sxs-lookup"><span data-stu-id="8303a-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="8303a-131">Přejděte na Řízení skladu > Dotazy a sestavy > Fyzické množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="8303a-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="8303a-132">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="8303a-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8303a-133">Chcete-li filtrovat seznam položek, můžete použít pole Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="8303a-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="8303a-134">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="8303a-134">Refresh the page.</span></span>
4. <span data-ttu-id="8303a-135">Klikněte na Zobrazit dimenze.</span><span class="sxs-lookup"><span data-stu-id="8303a-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="8303a-136">Karta Zobrazit dimenze umožňuje vybrat způsob, jak podrobné údaje chcete zobrazit o množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="8303a-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="8303a-137">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8303a-137">Click OK.</span></span>
6. <span data-ttu-id="8303a-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8303a-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="8303a-139">Kontrola množství na skladě podle skladového místa</span><span class="sxs-lookup"><span data-stu-id="8303a-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="8303a-140">Přejděte na Řízení skladu > Dotazy a sestavy > Množství na skladě podle skladového místa.</span><span class="sxs-lookup"><span data-stu-id="8303a-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="8303a-141">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="8303a-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="8303a-142">V případě, že používáte ukázková data společnosti USMF, můžete použít „51“.</span><span class="sxs-lookup"><span data-stu-id="8303a-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="8303a-143">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="8303a-143">Refresh the page.</span></span>
4. <span data-ttu-id="8303a-144">Klikněte na Zobrazit dimenze.</span><span class="sxs-lookup"><span data-stu-id="8303a-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="8303a-145">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8303a-145">Click OK.</span></span>
6. <span data-ttu-id="8303a-146">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8303a-146">Close the page.</span></span>


---
title: Kontrola dostupnosti zásob
description: Tento postup popisuje způsob kontroly množství na skladě a zásob fyzicky k dispozici pro určité číslo položky.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3f6f601d2d48ede2c4db198ac5438aa32e056d
ms.sourcegitcommit: 8cbaeb6443ce47a4c4bc02b5e1a1212eb0056b38
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829770"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="10d35-103">Kontrola dostupnosti zásob</span><span class="sxs-lookup"><span data-stu-id="10d35-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10d35-104">Tento postup popisuje způsob kontroly množství na skladě a zásob fyzicky k dispozici pro určité číslo položky.</span><span class="sxs-lookup"><span data-stu-id="10d35-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="10d35-105">Také ukazuje, jak získat informace o zásobách související s položkou.</span><span class="sxs-lookup"><span data-stu-id="10d35-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="10d35-106">Fyzické zásoby na skladě je množství na skladě, které je k dispozici – tedy, je zakoupené, přijaté a registrované.</span><span class="sxs-lookup"><span data-stu-id="10d35-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="10d35-107">Množství na skladě zahrnuje dostupné zásoby na skladě, ale i zásoby, které byly objednány a jsou očekávané, ale dosud nebyly přijaty nebo registrovány.</span><span class="sxs-lookup"><span data-stu-id="10d35-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="10d35-108">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="10d35-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="10d35-109">Pokud používáte USMF, můžete použít ukázkové hodnoty, které jsou zobrazeny.</span><span class="sxs-lookup"><span data-stu-id="10d35-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="10d35-110">Tyto úkoly obvykle provádějí pracovníci skladu.</span><span class="sxs-lookup"><span data-stu-id="10d35-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="10d35-111">Kontrola zásob na skladě pro konkrétní položku</span><span class="sxs-lookup"><span data-stu-id="10d35-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="10d35-112">Přejděte na **Navigační podokno > Moduly > Řízení zásob > Dotazy a sestavy > Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="10d35-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="10d35-113">Vyberte řádek **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="10d35-113">Select the **Item number** row.</span></span> <span data-ttu-id="10d35-114">Pokud chcete vytvořit dotaz na množství na skladě podle čísla položky, vyberte řádek, kde je Tabulka nastavena na **Množství na skladě**, a Pole je nastaveno na číslo **Položky**.</span><span class="sxs-lookup"><span data-stu-id="10d35-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="10d35-115">V poli **Kritéria** vyberte položku, pro kterou chcete vytvořit dotaz.</span><span class="sxs-lookup"><span data-stu-id="10d35-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="10d35-116">V případě, že používáte ukázková data společnosti USMF, můžete vybrat 'M9201'.</span><span class="sxs-lookup"><span data-stu-id="10d35-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="10d35-117">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="10d35-117">Click **OK**.</span></span>
5. <span data-ttu-id="10d35-118">V **podokně akcí** klikněte na možnost **Dimenze**.</span><span class="sxs-lookup"><span data-stu-id="10d35-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="10d35-119">Karta **Dimenze** umožňuje vybrat způsob, jak podrobné údaje chcete zobrazit o množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="10d35-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="10d35-120">Pokud potřebujete data související s rezervací, musíte zobrazit všechny dimenze zásob pro položky používající procesy rozšířené skladu (řízení skladu).</span><span class="sxs-lookup"><span data-stu-id="10d35-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="10d35-121">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="10d35-121">Click **OK**.</span></span>
7. <span data-ttu-id="10d35-122">V **podokně akcí** klikněte na možnost **Související informace**.</span><span class="sxs-lookup"><span data-stu-id="10d35-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="10d35-123">Pokud tuto možnost nevidíte, klikněte na tlačítko se třemi tečkami (...) a otevřete tak další možnosti v podokně.</span><span class="sxs-lookup"><span data-stu-id="10d35-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="10d35-124">Klikněte na **Přehled dodávek**.</span><span class="sxs-lookup"><span data-stu-id="10d35-124">Click **Supply overview**.</span></span> <span data-ttu-id="10d35-125">Karta **Přehled dodávek** obsahuje informace o zásobách pro určitou položku, jako je například množství na skladě, doba realizace a informace o dodavateli.</span><span class="sxs-lookup"><span data-stu-id="10d35-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="10d35-126">Rozbalte sekci **Na skladě**.</span><span class="sxs-lookup"><span data-stu-id="10d35-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="10d35-127">Rozbalte sekci **Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="10d35-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="10d35-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="10d35-128">Close the page.</span></span>
12. <span data-ttu-id="10d35-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="10d35-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="10d35-130">Kontrola fyzického množství na skladě</span><span class="sxs-lookup"><span data-stu-id="10d35-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="10d35-131">Přejděte na **Navigační podokno > Moduly > Řízení skladu > Dotazy a sestavy > Fyzické zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="10d35-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="10d35-132">Zadejte hodnotu do pole **Číslo zboží**.</span><span class="sxs-lookup"><span data-stu-id="10d35-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="10d35-133">Chcete-li filtrovat seznam položek, můžete použít pole Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="10d35-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="10d35-134">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="10d35-134">Refresh the page.</span></span>
4. <span data-ttu-id="10d35-135">V **podokně akcí** klikněte na možnost **Zobrazit dimenze**.</span><span class="sxs-lookup"><span data-stu-id="10d35-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="10d35-136">Karta Zobrazit dimenze umožňuje vybrat způsob, jak podrobné údaje chcete zobrazit o množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="10d35-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="10d35-137">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="10d35-137">Click **OK**.</span></span>
6. <span data-ttu-id="10d35-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="10d35-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="10d35-139">Kontrola množství na skladě podle skladového místa</span><span class="sxs-lookup"><span data-stu-id="10d35-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="10d35-140">Přejděte na **Navigační podokno > Moduly > Řízení skladu > Dotazy a sestavy > Množství na skladě podle místa**.</span><span class="sxs-lookup"><span data-stu-id="10d35-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="10d35-141">Zadejte hodnotu do pole **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="10d35-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="10d35-142">V případě, že používáte ukázková data společnosti USMF, můžete použít „51“.</span><span class="sxs-lookup"><span data-stu-id="10d35-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="10d35-143">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="10d35-143">Refresh the page.</span></span>
4. <span data-ttu-id="10d35-144">Klikněte na **Zobrazit dimenze**.</span><span class="sxs-lookup"><span data-stu-id="10d35-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="10d35-145">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="10d35-145">Click **OK**.</span></span>
6. <span data-ttu-id="10d35-146">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="10d35-146">Close the page.</span></span>


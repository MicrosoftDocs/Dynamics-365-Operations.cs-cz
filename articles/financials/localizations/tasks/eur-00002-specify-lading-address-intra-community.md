---
title: EUR-00002 Zadání adresy nakládky pro intrakomunitární transakci
description: Tato procedura ukazuje, jak zadat adresu nakládky pro interní obchodní transakci.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid,  VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71f93d0ebc660199710d4bbfaff27eb7754a81da
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537630"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a><span data-ttu-id="0e58d-103">EUR-00002 Zadání adresy nakládky pro intrakomunitární transakci</span><span class="sxs-lookup"><span data-stu-id="0e58d-103">EUR-00002 Specifying a lading address for an intra-community transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e58d-104">Tato procedura ukazuje, jak zadat adresu nakládky pro interní obchodní transakci.</span><span class="sxs-lookup"><span data-stu-id="0e58d-104">This procedure shows how to specify a lading address for an intra-community trade transaction.</span></span> <span data-ttu-id="0e58d-105">Německá firma si například objedná zboží od dodavatele s firemní adresou v Německu.</span><span class="sxs-lookup"><span data-stu-id="0e58d-105">For example, a Germany company orders items from a vendor with a German business address.</span></span> <span data-ttu-id="0e58d-106">Tento dodavatel má sklad v Itálii a odtud dodává zboží.</span><span class="sxs-lookup"><span data-stu-id="0e58d-106">This vendor has a warehouse in Italy and ships the items from there.</span></span> <span data-ttu-id="0e58d-107">Tato dodávka musí být vykázána v Intrastatu.</span><span class="sxs-lookup"><span data-stu-id="0e58d-107">This delivery must be reported in the Intrastat.</span></span> <span data-ttu-id="0e58d-108">Stejné chování platí pro vrácené položky odběratele.</span><span class="sxs-lookup"><span data-stu-id="0e58d-108">The same behavior is valid for customer returns.</span></span>
<span data-ttu-id="0e58d-109">Postup se vztahuje na všechny evropské země/oblasti.</span><span class="sxs-lookup"><span data-stu-id="0e58d-109">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="0e58d-110">Úkol byl vytvořen za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu.</span><span class="sxs-lookup"><span data-stu-id="0e58d-110">The task was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="0e58d-111">Před dokončením této procedury je nutné nakonfigurovat výkaznictví Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e58d-111">Before you can complete this procedure, you must configure Intrastat reporting.</span></span> <span data-ttu-id="0e58d-112">Tento postup je určen pouze pro účetní.</span><span class="sxs-lookup"><span data-stu-id="0e58d-112">This procedure is intended for accountants.</span></span> <span data-ttu-id="0e58d-113">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="0e58d-113">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="0e58d-114">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0e58d-114">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="0e58d-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0e58d-115">Click New.</span></span>
3. <span data-ttu-id="0e58d-116">Zadání nebo výběr hodnoty</span><span class="sxs-lookup"><span data-stu-id="0e58d-116">Enter or select a value</span></span>
    * <span data-ttu-id="0e58d-117">Vyberte například DE-001.</span><span class="sxs-lookup"><span data-stu-id="0e58d-117">For example, select DE-001.</span></span> <span data-ttu-id="0e58d-118">Tento dodavatel má adresu firmy v Německu.</span><span class="sxs-lookup"><span data-stu-id="0e58d-118">This vendor has a German business address.</span></span>  
4. <span data-ttu-id="0e58d-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0e58d-119">Click OK.</span></span>
5. <span data-ttu-id="0e58d-120">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="0e58d-120">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="0e58d-121">V poli Číslo zboží zadejte nebo vyberte hodnotu D0001.</span><span class="sxs-lookup"><span data-stu-id="0e58d-121">In the Item number field, enter or select a value D0001.</span></span>
7. <span data-ttu-id="0e58d-122">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="0e58d-122">Click Save.</span></span>
8. <span data-ttu-id="0e58d-123">V podokně akcí klikněte na možnost Přijmout.</span><span class="sxs-lookup"><span data-stu-id="0e58d-123">On the Action Pane, click Receive.</span></span>
9. <span data-ttu-id="0e58d-124">Klikněte na Podrobnosti přepravy.</span><span class="sxs-lookup"><span data-stu-id="0e58d-124">Click Transportation details.</span></span>
10. <span data-ttu-id="0e58d-125">Do pole Datum a čas nakládky zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="0e58d-125">In the Loading date and time field, enter a date and time.</span></span>
11. <span data-ttu-id="0e58d-126">Klikněte na Přidat adresu.</span><span class="sxs-lookup"><span data-stu-id="0e58d-126">Click Add address.</span></span>
12. <span data-ttu-id="0e58d-127">Klepněte na tlačítko Nový a vytvořte novou adresu s účelem Nakládka.</span><span class="sxs-lookup"><span data-stu-id="0e58d-127">Click New and create new address with purpose Lading.</span></span>
13. <span data-ttu-id="0e58d-128">Do pole Název nebo popis zadejte Italština.</span><span class="sxs-lookup"><span data-stu-id="0e58d-128">In the Name or description field, type 'Italian'.</span></span>
14. <span data-ttu-id="0e58d-129">Vyberte Nakládka jako hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0e58d-129">Select Lading as the value.</span></span>
    * <span data-ttu-id="0e58d-130">Všimněte si, že účel adresy musí být Nakládka.</span><span class="sxs-lookup"><span data-stu-id="0e58d-130">Note that that address purpose must be Lading.</span></span>  
15. <span data-ttu-id="0e58d-131">V poli Země/oblast zadejte nebo vyberte hodnotu ITA.</span><span class="sxs-lookup"><span data-stu-id="0e58d-131">In the Country/region field, enter or select a value ITA.</span></span>
16. <span data-ttu-id="0e58d-132">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0e58d-132">Click Save.</span></span>
17. <span data-ttu-id="0e58d-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0e58d-133">Close the page.</span></span>
18. <span data-ttu-id="0e58d-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0e58d-134">Click Save.</span></span>
    * <span data-ttu-id="0e58d-135">Ověřte správnost adresy nakládky.</span><span class="sxs-lookup"><span data-stu-id="0e58d-135">Verify that the lading address is correct.</span></span>  
19. <span data-ttu-id="0e58d-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0e58d-136">Close the page.</span></span>
20. <span data-ttu-id="0e58d-137">V podokně akcí klikněte na položku Nákup.</span><span class="sxs-lookup"><span data-stu-id="0e58d-137">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="0e58d-138">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="0e58d-138">Click Confirm.</span></span>
22. <span data-ttu-id="0e58d-139">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="0e58d-139">On the Action Pane, click Invoice.</span></span>
23. <span data-ttu-id="0e58d-140">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="0e58d-140">Click Invoice.</span></span>
24. <span data-ttu-id="0e58d-141">Zadejte hodnotu do pole Číslo.</span><span class="sxs-lookup"><span data-stu-id="0e58d-141">In the Number field, type a value.</span></span>
25. <span data-ttu-id="0e58d-142">Do pole Datum faktury zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="0e58d-142">In the Invoice date field, enter a date.</span></span>
26. <span data-ttu-id="0e58d-143">Kliknutím na Výchozí od: Množství v příjemce produktu otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="0e58d-143">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
27. <span data-ttu-id="0e58d-144">V poli Výchozí množství pro řádky vyberte Objednané množství.</span><span class="sxs-lookup"><span data-stu-id="0e58d-144">In the Default quantity for lines field, select 'Ordered quantity'.</span></span>
28. <span data-ttu-id="0e58d-145">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0e58d-145">Click OK.</span></span>
29. <span data-ttu-id="0e58d-146">Klikněte na Podrobnosti přepravy.</span><span class="sxs-lookup"><span data-stu-id="0e58d-146">Click Transportation details.</span></span>
    * <span data-ttu-id="0e58d-147">Ověřte, že zboží bylo dodáno z Itálie.</span><span class="sxs-lookup"><span data-stu-id="0e58d-147">Verify that goods were shipped from Italy.</span></span> <span data-ttu-id="0e58d-148">V případě potřeby můžete upravit podrobnosti o nakládce.</span><span class="sxs-lookup"><span data-stu-id="0e58d-148">If necessary, you can edit the lading details.</span></span>  
30. <span data-ttu-id="0e58d-149">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0e58d-149">Close the page.</span></span>
31. <span data-ttu-id="0e58d-150">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="0e58d-150">Click Post.</span></span>
32. <span data-ttu-id="0e58d-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0e58d-151">Close the page.</span></span>
33. <span data-ttu-id="0e58d-152">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0e58d-152">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
34. <span data-ttu-id="0e58d-153">Klepněte na položku Převod.</span><span class="sxs-lookup"><span data-stu-id="0e58d-153">Click Transfer.</span></span>
35. <span data-ttu-id="0e58d-154">Vyberte možnost Ano v poli Tisk faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="0e58d-154">Select Yes in the Vendor invoice field.</span></span>
36. <span data-ttu-id="0e58d-155">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0e58d-155">Click OK.</span></span>
37. <span data-ttu-id="0e58d-156">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="0e58d-156">Click the General tab.</span></span>
    * <span data-ttu-id="0e58d-157">Vyhledejte nově vytvořený řádek a ověřte, že odesílatel dodal zboží z Itálie.</span><span class="sxs-lookup"><span data-stu-id="0e58d-157">Find a newly created line and verify that the sender shipped the goods from Italy.</span></span>  


--- 
title: "EUR-00015 Registrace DIČ dodavatele"
description: "Tato procedura ukazuje, jak přidat ID registrace DPH a číslo osvobození od daně k účtu dodavatele."
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d9788a35e768a4a289742e9cd864b3ca185a0407
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="eur-00015-registration-of-vendor-vat-id"></a><span data-ttu-id="be83c-103">EUR-00015 Registrace DIČ dodavatele</span><span class="sxs-lookup"><span data-stu-id="be83c-103">EUR-00015 Registration of vendor VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be83c-104">Tato procedura ukazuje, jak přidat ID registrace DPH a číslo osvobození od daně k účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="be83c-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="be83c-105">Tento proces je podobný pro právnické osoby a odběratele.</span><span class="sxs-lookup"><span data-stu-id="be83c-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="be83c-106">Dokončení této procedury vyžaduje nastavení hodnot DIČ.</span><span class="sxs-lookup"><span data-stu-id="be83c-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="be83c-107">Postup se vztahuje na všechny evropské země/oblasti.</span><span class="sxs-lookup"><span data-stu-id="be83c-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="be83c-108">Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu.</span><span class="sxs-lookup"><span data-stu-id="be83c-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="be83c-109">Tato procedura je určena pro správce správy dat, manažera závazků nebo manažera pohledávek.</span><span class="sxs-lookup"><span data-stu-id="be83c-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="be83c-110">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="be83c-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="be83c-111">Přejděte do části Závazky > Dodavatelé > Všichni dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="be83c-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="be83c-112">V seznamu vyhledejte a vyberte dodavatele DE-01001.</span><span class="sxs-lookup"><span data-stu-id="be83c-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="be83c-113">Klikněte na ID registrace.</span><span class="sxs-lookup"><span data-stu-id="be83c-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="be83c-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="be83c-114">Click Add.</span></span>
5. <span data-ttu-id="be83c-115">Vyberte DIČ.</span><span class="sxs-lookup"><span data-stu-id="be83c-115">Select VAT ID.</span></span>
6. <span data-ttu-id="be83c-116">Zadejte hodnotu do pole Číslo registrace.</span><span class="sxs-lookup"><span data-stu-id="be83c-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="be83c-117">Zadejte DIČ v Německu pro vybraného dodavatele.</span><span class="sxs-lookup"><span data-stu-id="be83c-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="be83c-118">Identifikátor se musí shodovat se zadaným formátem typu registrace.</span><span class="sxs-lookup"><span data-stu-id="be83c-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="be83c-119">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="be83c-119">Click the General tab.</span></span>
8. <span data-ttu-id="be83c-120">V poli Platnost zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="be83c-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="be83c-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be83c-121">Click Save.</span></span>
10. <span data-ttu-id="be83c-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be83c-122">Click New.</span></span>
11. <span data-ttu-id="be83c-123">Zadejte hodnotu do pole Název nebo popis.</span><span class="sxs-lookup"><span data-stu-id="be83c-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="be83c-124">Zadejte například ITA.</span><span class="sxs-lookup"><span data-stu-id="be83c-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="be83c-125">V poli Země/oblast zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be83c-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="be83c-126">Vyberte například ITA.</span><span class="sxs-lookup"><span data-stu-id="be83c-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="be83c-127">Vyberte možnost Primární v poli Země.</span><span class="sxs-lookup"><span data-stu-id="be83c-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="be83c-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be83c-128">Click Save.</span></span>
15. <span data-ttu-id="be83c-129">Klikněte na záložku Přehled.</span><span class="sxs-lookup"><span data-stu-id="be83c-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="be83c-130">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="be83c-130">Click Add.</span></span>
17. <span data-ttu-id="be83c-131">V poli Typ registrace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be83c-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="be83c-132">Vyberte například DIČ.</span><span class="sxs-lookup"><span data-stu-id="be83c-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="be83c-133">Zadejte hodnotu do pole Číslo registrace.</span><span class="sxs-lookup"><span data-stu-id="be83c-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="be83c-134">Například zadejte DIČ v Itálii.</span><span class="sxs-lookup"><span data-stu-id="be83c-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="be83c-135">Identifikátor musí mít stejný formát jako typ registrace.</span><span class="sxs-lookup"><span data-stu-id="be83c-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="be83c-136">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be83c-136">Click Save.</span></span>
20. <span data-ttu-id="be83c-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be83c-137">Close the page.</span></span>
21. <span data-ttu-id="be83c-138">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="be83c-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="be83c-139">Vyberte například DE-01001.</span><span class="sxs-lookup"><span data-stu-id="be83c-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="be83c-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="be83c-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="be83c-141">Rozbalte oddíl Faktury a dodávky.</span><span class="sxs-lookup"><span data-stu-id="be83c-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="be83c-142">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="be83c-142">Click Edit.</span></span>
25. <span data-ttu-id="be83c-143">V poli DIČ zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be83c-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="be83c-144">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be83c-144">Click Save.</span></span>



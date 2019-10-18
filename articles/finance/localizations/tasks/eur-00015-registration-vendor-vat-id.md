---
title: EUR-00015 Registrace DIČ dodavatele
description: Tato procedura ukazuje, jak přidat ID registrace DPH a číslo osvobození od daně k účtu dodavatele.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68475c96e7c85cc5a4c540441a4b1f3752ecf0bd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175083"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a><span data-ttu-id="33897-103">EUR-00015 Registrace DIČ dodavatele</span><span class="sxs-lookup"><span data-stu-id="33897-103">EUR-00015 Registration of vendor VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33897-104">Tato procedura ukazuje, jak přidat ID registrace DPH a číslo osvobození od daně k účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="33897-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="33897-105">Tento proces je podobný pro právnické osoby a odběratele.</span><span class="sxs-lookup"><span data-stu-id="33897-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="33897-106">Dokončení této procedury vyžaduje nastavení hodnot DIČ.</span><span class="sxs-lookup"><span data-stu-id="33897-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="33897-107">Postup se vztahuje na všechny evropské země/oblasti.</span><span class="sxs-lookup"><span data-stu-id="33897-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="33897-108">Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu.</span><span class="sxs-lookup"><span data-stu-id="33897-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="33897-109">Tato procedura je určena pro správce správy dat, manažera závazků nebo manažera pohledávek.</span><span class="sxs-lookup"><span data-stu-id="33897-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="33897-110">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="33897-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="33897-111">Přejděte do části Závazky > Dodavatelé > Všichni dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="33897-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="33897-112">V seznamu vyhledejte a vyberte dodavatele DE-01001.</span><span class="sxs-lookup"><span data-stu-id="33897-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="33897-113">Klikněte na ID registrace.</span><span class="sxs-lookup"><span data-stu-id="33897-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="33897-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33897-114">Click Add.</span></span>
5. <span data-ttu-id="33897-115">Vyberte DIČ.</span><span class="sxs-lookup"><span data-stu-id="33897-115">Select VAT ID.</span></span>
6. <span data-ttu-id="33897-116">Zadejte hodnotu do pole Číslo registrace.</span><span class="sxs-lookup"><span data-stu-id="33897-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="33897-117">Zadejte DIČ v Německu pro vybraného dodavatele.</span><span class="sxs-lookup"><span data-stu-id="33897-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="33897-118">Identifikátor se musí shodovat se zadaným formátem typu registrace.</span><span class="sxs-lookup"><span data-stu-id="33897-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="33897-119">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="33897-119">Click the General tab.</span></span>
8. <span data-ttu-id="33897-120">V poli Platnost zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="33897-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="33897-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="33897-121">Click Save.</span></span>
10. <span data-ttu-id="33897-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="33897-122">Click New.</span></span>
11. <span data-ttu-id="33897-123">Zadejte hodnotu do pole Název nebo popis.</span><span class="sxs-lookup"><span data-stu-id="33897-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="33897-124">Zadejte například ITA.</span><span class="sxs-lookup"><span data-stu-id="33897-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="33897-125">V poli Země/oblast zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="33897-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="33897-126">Vyberte například ITA.</span><span class="sxs-lookup"><span data-stu-id="33897-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="33897-127">Vyberte možnost Primární v poli Země.</span><span class="sxs-lookup"><span data-stu-id="33897-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="33897-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="33897-128">Click Save.</span></span>
15. <span data-ttu-id="33897-129">Klikněte na záložku Přehled.</span><span class="sxs-lookup"><span data-stu-id="33897-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="33897-130">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33897-130">Click Add.</span></span>
17. <span data-ttu-id="33897-131">V poli Typ registrace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="33897-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="33897-132">Vyberte například DIČ.</span><span class="sxs-lookup"><span data-stu-id="33897-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="33897-133">Zadejte hodnotu do pole Číslo registrace.</span><span class="sxs-lookup"><span data-stu-id="33897-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="33897-134">Například zadejte DIČ v Itálii.</span><span class="sxs-lookup"><span data-stu-id="33897-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="33897-135">Identifikátor musí mít stejný formát jako typ registrace.</span><span class="sxs-lookup"><span data-stu-id="33897-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="33897-136">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="33897-136">Click Save.</span></span>
20. <span data-ttu-id="33897-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="33897-137">Close the page.</span></span>
21. <span data-ttu-id="33897-138">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="33897-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="33897-139">Vyberte například DE-01001.</span><span class="sxs-lookup"><span data-stu-id="33897-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="33897-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="33897-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="33897-141">Rozbalte oddíl Faktury a dodávky.</span><span class="sxs-lookup"><span data-stu-id="33897-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="33897-142">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="33897-142">Click Edit.</span></span>
25. <span data-ttu-id="33897-143">V poli DIČ zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="33897-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="33897-144">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="33897-144">Click Save.</span></span>


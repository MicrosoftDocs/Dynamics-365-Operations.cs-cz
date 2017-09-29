--- 
title: " Definování kanálu kontaktního střediska a atributů kanálu"
description: "Tento postup vás provede vytvářením nového maloobchodního kanálu a definováním atributů kanálu."
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c3d2f6785b9054ede7ea96ebd48c5d1f23e510e7
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="define-call-center-channel-and-channel-attributes"></a><span data-ttu-id="39a2e-103"> Definování kanálu kontaktního střediska a atributů kanálu</span><span class="sxs-lookup"><span data-stu-id="39a2e-103">Define call center channel and channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="39a2e-104">Tento postup vás provede vytvářením nového maloobchodního kanálu a definováním atributů kanálu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="39a2e-105">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="39a2e-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="39a2e-106">Tento postup je určen pro roli IT pro maloobchod.</span><span class="sxs-lookup"><span data-stu-id="39a2e-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="39a2e-107">Vytvořit nový obchod</span><span class="sxs-lookup"><span data-stu-id="39a2e-107">Create new store</span></span>
1. <span data-ttu-id="39a2e-108">Přejděte do části Všechny pracovní prostory > Nasazení kanálu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="39a2e-109">Klikněte na Nový kanál.</span><span class="sxs-lookup"><span data-stu-id="39a2e-109">Click New channel.</span></span>
3. <span data-ttu-id="39a2e-110">Klepněte na Obchod.</span><span class="sxs-lookup"><span data-stu-id="39a2e-110">Click Store.</span></span>
4. <span data-ttu-id="39a2e-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="39a2e-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="39a2e-112">Zadejte hodnotu do pole Číslo obchodu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="39a2e-113">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="39a2e-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="39a2e-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="39a2e-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="39a2e-116">V poli Časové pásmo obchodu vyberte požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="39a2e-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="39a2e-117">V poli Profil kanálu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="39a2e-118">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="39a2e-119">V poli Jazyk kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="39a2e-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="39a2e-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="39a2e-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="39a2e-122">V poli Skupina prodejní daně kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="39a2e-123">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="39a2e-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="39a2e-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="39a2e-125">V poli Adresář odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="39a2e-126">Vyberte adresář používaný ke spojení odběratelů s tímto obchodem.</span><span class="sxs-lookup"><span data-stu-id="39a2e-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="39a2e-127">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="39a2e-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="39a2e-128">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="39a2e-129">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="39a2e-129">Click Select.</span></span>
22. <span data-ttu-id="39a2e-130">V poli Adresář zaměstnance kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="39a2e-131">Vyberte adresář používaný ke spojení pokladníků s tímto kanálem.</span><span class="sxs-lookup"><span data-stu-id="39a2e-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="39a2e-132">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="39a2e-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="39a2e-133">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="39a2e-134">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="39a2e-134">Click Select.</span></span>
26. <span data-ttu-id="39a2e-135">V poli Výchozí zákazník kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="39a2e-136">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="39a2e-137">Rozbalte nebo sbalte oddíl Rozložení obrazovky.</span><span class="sxs-lookup"><span data-stu-id="39a2e-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="39a2e-138">V poli ID rozvržení obrazovky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="39a2e-139">Vyberte výchozí rozvržení obrazovky POS pro tento obchod.</span><span class="sxs-lookup"><span data-stu-id="39a2e-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="39a2e-140">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="39a2e-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="39a2e-141">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="39a2e-142">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="39a2e-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="39a2e-143">Klikněte na Atributy kanálu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="39a2e-144">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="39a2e-144">Click New.</span></span>
35. <span data-ttu-id="39a2e-145">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="39a2e-146">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="39a2e-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="39a2e-147">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="39a2e-148">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="39a2e-148">Click Save.</span></span>
39. <span data-ttu-id="39a2e-149">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39a2e-149">Close the page.</span></span>
40. <span data-ttu-id="39a2e-150">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="39a2e-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="39a2e-151">Klikněte na Způsoby platby.</span><span class="sxs-lookup"><span data-stu-id="39a2e-151">Click Payment methods.</span></span>
42. <span data-ttu-id="39a2e-152">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="39a2e-152">Click New.</span></span>
43. <span data-ttu-id="39a2e-153">V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="39a2e-154">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="39a2e-155">Rozbalte nebo sbalte oddíl zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="39a2e-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="39a2e-156">Zadejte požadované hodnoty do pole Číslo účtu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="39a2e-157">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="39a2e-157">Click Save.</span></span>
48. <span data-ttu-id="39a2e-158">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39a2e-158">Close the page.</span></span>
49. <span data-ttu-id="39a2e-159">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="39a2e-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="39a2e-160">Klikněte na Výkaz hotovosti.</span><span class="sxs-lookup"><span data-stu-id="39a2e-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="39a2e-161">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="39a2e-161">Click New.</span></span>
52. <span data-ttu-id="39a2e-162">Zadejte číslo do pole Částka v měně transakce.</span><span class="sxs-lookup"><span data-stu-id="39a2e-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="39a2e-163">V poli Měna kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="39a2e-164">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="39a2e-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="39a2e-165">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="39a2e-166">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="39a2e-166">Click Save.</span></span>
57. <span data-ttu-id="39a2e-167">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39a2e-167">Close the page.</span></span>
58. <span data-ttu-id="39a2e-168">V podokně akcí klikněte na možnost Nastavit.</span><span class="sxs-lookup"><span data-stu-id="39a2e-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="39a2e-169">Klikněte na Přiřazení skupiny lokátoru obchodů.</span><span class="sxs-lookup"><span data-stu-id="39a2e-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="39a2e-170">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="39a2e-170">Click New.</span></span>
61. <span data-ttu-id="39a2e-171">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="39a2e-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="39a2e-172">V poli Skupina lokátorů kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="39a2e-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="39a2e-173">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="39a2e-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="39a2e-174">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39a2e-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="39a2e-175">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="39a2e-175">Click Save.</span></span>
66. <span data-ttu-id="39a2e-176">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="39a2e-176">Close the page.</span></span>



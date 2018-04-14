--- 
title: "Vytvoření rozšířených pravidel pro deníky"
description: "Tento postup vás provede vytvářením rozšířených pravidel pro deníky."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 36f4edd6fa9711022e291ea5ceffbcc9ef55b2a9
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="35a7f-103">Vytvoření rozšířených pravidel pro deníky</span><span class="sxs-lookup"><span data-stu-id="35a7f-103">Create advanced rules for journals</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35a7f-104">Tento postup vás provede vytvářením rozšířených pravidel pro deníky.</span><span class="sxs-lookup"><span data-stu-id="35a7f-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="35a7f-105">To zahrnuje nastavení deníků, řízení a omezení zaúčtování uživatele.</span><span class="sxs-lookup"><span data-stu-id="35a7f-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="35a7f-106">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="35a7f-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="35a7f-107">Nastavení kontroly deníku</span><span class="sxs-lookup"><span data-stu-id="35a7f-107">Set up journal control</span></span>
1. <span data-ttu-id="35a7f-108">Přejděte do hlavní knihy > Nastavení deníku > Názvy deníků.</span><span class="sxs-lookup"><span data-stu-id="35a7f-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="35a7f-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="35a7f-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="35a7f-110">Klepněte na Kontrola deníku.</span><span class="sxs-lookup"><span data-stu-id="35a7f-110">Click Journal control.</span></span>
4. <span data-ttu-id="35a7f-111">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="35a7f-111">Click Add.</span></span>
5. <span data-ttu-id="35a7f-112">V poli Účty společnosti klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="35a7f-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="35a7f-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="35a7f-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="35a7f-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="35a7f-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="35a7f-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="35a7f-115">Click Add.</span></span>
9. <span data-ttu-id="35a7f-116">V poli Účetní struktura klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="35a7f-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="35a7f-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="35a7f-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="35a7f-118">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="35a7f-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="35a7f-119">V poli Segment klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="35a7f-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="35a7f-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="35a7f-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="35a7f-121">V poli Od hodnoty klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="35a7f-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="35a7f-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="35a7f-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="35a7f-123">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="35a7f-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="35a7f-124">V poli Do hodnoty klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="35a7f-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="35a7f-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="35a7f-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="35a7f-126">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="35a7f-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="35a7f-127">Nastavení omezení zaúčtování</span><span class="sxs-lookup"><span data-stu-id="35a7f-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="35a7f-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="35a7f-128">Close the page.</span></span>
2. <span data-ttu-id="35a7f-129">Klepněte na Omezení účtování.</span><span class="sxs-lookup"><span data-stu-id="35a7f-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="35a7f-130">V poli Jak chcete nastavit omezení zaúčtování? vyberte možnost Podle skupin uživatelů.</span><span class="sxs-lookup"><span data-stu-id="35a7f-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="35a7f-131">Ve stromu zkontrolujte „skupinu, pro kterou chcete povolit zaúčtování pro tento název deníku“.</span><span class="sxs-lookup"><span data-stu-id="35a7f-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="35a7f-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="35a7f-132">Click OK.</span></span>



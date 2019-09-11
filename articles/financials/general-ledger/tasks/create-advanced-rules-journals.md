---
title: Vytvoření rozšířených pravidel pro deníky
description: Tento postup vás provede vytvářením rozšířených pravidel pro deníky.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3eb34ac419aeab3663a8931d022abf7bcbfddd37
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916132"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="eaf4f-103">Vytvoření rozšířených pravidel pro deníky</span><span class="sxs-lookup"><span data-stu-id="eaf4f-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eaf4f-104">Tento postup vás provede vytvářením rozšířených pravidel pro deníky.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="eaf4f-105">To zahrnuje nastavení deníků, řízení a omezení zaúčtování uživatele.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="eaf4f-106">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="eaf4f-107">Nastavení kontroly deníku</span><span class="sxs-lookup"><span data-stu-id="eaf4f-107">Set up journal control</span></span>
1. <span data-ttu-id="eaf4f-108">V **navigačním podokně** přejděte na **Moduly > Hlavní kniha > Nastavení deníku > Názvy deníku**.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="eaf4f-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="eaf4f-110">V **Podokně akcí** klikněte na možnost **Kontrola deníku**.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="eaf4f-111">Na záložce s náhledem **Které typy účtů lze zaúčtovat** klikněte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="eaf4f-112">V poli **Účty společnosti** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="eaf4f-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="eaf4f-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="eaf4f-115">Na záložce s náhledem **Které hodnoty segmentu jsou platné pro tento deník** klikněte na **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="eaf4f-116">V poli **Účetní struktura** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="eaf4f-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="eaf4f-118">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="eaf4f-119">V poli **Segment** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="eaf4f-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="eaf4f-121">V poli **Od hodnoty** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="eaf4f-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="eaf4f-123">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="eaf4f-124">V poli **Do hodnoty** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="eaf4f-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="eaf4f-126">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="eaf4f-127">Nastavení omezení zaúčtování</span><span class="sxs-lookup"><span data-stu-id="eaf4f-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="eaf4f-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-128">Close the page.</span></span>
2. <span data-ttu-id="eaf4f-129">Klikněte na **Omezení účtování**.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="eaf4f-130">V poli **Jak chcete nastavit omezení zaúčtování** vyberte možnost Podle skupin uživatelů.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="eaf4f-131">Ve stromu zkontrolujte „skupinu, pro kterou chcete povolit zaúčtování pro tento název deníku“.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="eaf4f-132">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="eaf4f-132">Click **OK**.</span></span>


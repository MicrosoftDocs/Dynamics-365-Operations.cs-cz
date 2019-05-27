---
title: Vytvoření rozšířených pravidel pro deníky
description: Tento postup vás provede vytvářením rozšířených pravidel pro deníky.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553100"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="bfba0-103">Vytvoření rozšířených pravidel pro deníky</span><span class="sxs-lookup"><span data-stu-id="bfba0-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bfba0-104">Tento postup vás provede vytvářením rozšířených pravidel pro deníky.</span><span class="sxs-lookup"><span data-stu-id="bfba0-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="bfba0-105">To zahrnuje nastavení deníků, řízení a omezení zaúčtování uživatele.</span><span class="sxs-lookup"><span data-stu-id="bfba0-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="bfba0-106">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="bfba0-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="bfba0-107">Nastavení kontroly deníku</span><span class="sxs-lookup"><span data-stu-id="bfba0-107">Set up journal control</span></span>
1. <span data-ttu-id="bfba0-108">Přejděte do hlavní knihy > Nastavení deníku > Názvy deníků.</span><span class="sxs-lookup"><span data-stu-id="bfba0-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="bfba0-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bfba0-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bfba0-110">Klepněte na Kontrola deníku.</span><span class="sxs-lookup"><span data-stu-id="bfba0-110">Click Journal control.</span></span>
4. <span data-ttu-id="bfba0-111">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="bfba0-111">Click Add.</span></span>
5. <span data-ttu-id="bfba0-112">V poli Účty společnosti klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bfba0-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="bfba0-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bfba0-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="bfba0-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bfba0-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="bfba0-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="bfba0-115">Click Add.</span></span>
9. <span data-ttu-id="bfba0-116">V poli Účetní struktura klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bfba0-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="bfba0-117">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bfba0-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="bfba0-118">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bfba0-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="bfba0-119">V poli Segment klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bfba0-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="bfba0-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bfba0-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="bfba0-121">V poli Od hodnoty klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bfba0-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="bfba0-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bfba0-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="bfba0-123">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bfba0-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="bfba0-124">V poli Do hodnoty klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bfba0-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="bfba0-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bfba0-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="bfba0-126">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bfba0-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="bfba0-127">Nastavení omezení zaúčtování</span><span class="sxs-lookup"><span data-stu-id="bfba0-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="bfba0-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="bfba0-128">Close the page.</span></span>
2. <span data-ttu-id="bfba0-129">Klepněte na Omezení účtování.</span><span class="sxs-lookup"><span data-stu-id="bfba0-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="bfba0-130">V poli Jak chcete nastavit omezení zaúčtování? vyberte možnost Podle skupin uživatelů.</span><span class="sxs-lookup"><span data-stu-id="bfba0-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="bfba0-131">Ve stromu zkontrolujte „skupinu, pro kterou chcete povolit zaúčtování pro tento název deníku“.</span><span class="sxs-lookup"><span data-stu-id="bfba0-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="bfba0-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bfba0-132">Click OK.</span></span>


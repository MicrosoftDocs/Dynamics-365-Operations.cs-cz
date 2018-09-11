--- 
title: "Zpracování deníku přidělení hlavní knihy"
description: "Použijte stránku Požadavek na přidělení procesu k vytvoření deníku přidělování, který lze před zaúčtováním do hlavní knihy zkontrolovat a schválit nebo přímo zaúčtovat do hlavní knihy."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: d9caebc6004d0a513ab2c3947300d7dd6e283750
ms.contentlocale: cs-cz
ms.lasthandoff: 09/11/2018

---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="33859-103">Zpracování deníku přidělení hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="33859-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33859-104">Použijte stránku Požadavek na přidělení procesu k vytvoření deníku přidělování, který lze před zaúčtováním do hlavní knihy zkontrolovat a schválit nebo přímo zaúčtovat do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="33859-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="33859-105">Předtím, než budete moci vytvořit deník přidělení, je nejprve nutné mít aktivní alespoň jedno pravidlo přidělení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="33859-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="33859-106">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="33859-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="33859-107">Přejděte do hlavní knihy > Přidělení > Požadavek na přidělení procesu.</span><span class="sxs-lookup"><span data-stu-id="33859-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="33859-108">V poli Pravidlo klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="33859-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="33859-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="33859-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="33859-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="33859-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="33859-111">Do pole K datu zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="33859-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="33859-112">Datum je velmi důležité, když je hlavní kniha zdrojem dat pro pravidlo.</span><span class="sxs-lookup"><span data-stu-id="33859-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="33859-113">Toto datum určuje, jaké zůstatky hlavní knihy budou zahrnuty do přidělení.</span><span class="sxs-lookup"><span data-stu-id="33859-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="33859-114">V poli Nulový zdroj vyberte Zastavit.</span><span class="sxs-lookup"><span data-stu-id="33859-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="33859-115">To zastaví proces přidělování a zobrazí zprávu informující o tom, že je vybrána nulová zdrojová částka.</span><span class="sxs-lookup"><span data-stu-id="33859-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="33859-116">V poli Možnosti návrhu vyberte „Pouze návrh“.</span><span class="sxs-lookup"><span data-stu-id="33859-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="33859-117">Vyberte Návrh pouze zkontrolovat a před zaúčtováním přidělení do hlavní knihy volitelně schvalte výsledek v Denících přidělení.</span><span class="sxs-lookup"><span data-stu-id="33859-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="33859-118">Zadejte datum do pole Datum zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="33859-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="33859-119">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33859-119">Click OK.</span></span>
9. <span data-ttu-id="33859-120">Přejděte do hlavní knihy > Přidělení > Deníky přidělení.</span><span class="sxs-lookup"><span data-stu-id="33859-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="33859-121">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="33859-121">Click Lines.</span></span>
11. <span data-ttu-id="33859-122">Klikněte na možnost Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="33859-122">Click Post.</span></span>
12. <span data-ttu-id="33859-123">Klikněte na možnost Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="33859-123">Click Post.</span></span>



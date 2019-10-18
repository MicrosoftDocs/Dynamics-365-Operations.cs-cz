---
title: Zpracování deníku přidělení hlavní knihy
description: Toto téma vysvětluje, jak zpracovat požadavek přidělení v aplikaci Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 882362a03e4fc4e249b092caea374640813eef88
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186065"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="95d02-103">Zpracování deníku přidělení hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="95d02-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95d02-104">Toto téma vysvětluje, jak zpracovat požadavek na přidělení.</span><span class="sxs-lookup"><span data-stu-id="95d02-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="95d02-105">Použijte stránku Požadavek na přidělení procesu k vytvoření deníku přidělování, který lze před zaúčtováním do hlavní knihy zkontrolovat a schválit nebo přímo zaúčtovat do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="95d02-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="95d02-106">Předtím, než budete moci vytvořit deník přidělení, je nejprve nutné mít aktivní alespoň jedno pravidlo přidělení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="95d02-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="95d02-107">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="95d02-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="95d02-108">V navigačním podokně přejděte na **Moduly > Hlavní kniha > Přidělení > Zpracovat požadavek na přidělení**.</span><span class="sxs-lookup"><span data-stu-id="95d02-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="95d02-109">V poli **Pravidlo** vyberte požadovaný záznam v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="95d02-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="95d02-110">Do pole **K datu** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="95d02-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="95d02-111">Pole **K datu** je velmi důležité, když je hlavní kniha zdrojem dat pro pravidlo.</span><span class="sxs-lookup"><span data-stu-id="95d02-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="95d02-112">Toto datum určuje, jaké zůstatky hlavní knihy budou zahrnuty do přidělení.</span><span class="sxs-lookup"><span data-stu-id="95d02-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="95d02-113">V poli **Nulový zdroj** vyberte **Zastavit**.</span><span class="sxs-lookup"><span data-stu-id="95d02-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="95d02-114">To zastaví proces přidělování a zobrazí zprávu informující o tom, že je vybrána nulová zdrojová částka.</span><span class="sxs-lookup"><span data-stu-id="95d02-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="95d02-115">V poli **Možnosti návrhu** vyberte **Pouze návrh**.</span><span class="sxs-lookup"><span data-stu-id="95d02-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="95d02-116">Vyberte **Pouze návrh** pro kontrolu a volitelné schválení výsledku v Denících přidělení před zaúčtováním přidělení do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="95d02-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="95d02-117">Zadejte datum do pole Datum zaúčtování do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="95d02-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="95d02-118">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="95d02-118">Select **OK**.</span></span>
7. <span data-ttu-id="95d02-119">V navigačním podokně přejděte na **Moduly > Hlavní kniha > Přidělení > Deníky přidělení**.</span><span class="sxs-lookup"><span data-stu-id="95d02-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="95d02-120">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="95d02-120">Select **Lines**.</span></span>
9. <span data-ttu-id="95d02-121">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="95d02-121">Select **Post**.</span></span>
10. <span data-ttu-id="95d02-122">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="95d02-122">Select **Post**.</span></span>


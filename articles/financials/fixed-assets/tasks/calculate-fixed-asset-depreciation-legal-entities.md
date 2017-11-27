--- 
title: "Výpočet odpisů dlouhodobého majetku mezi právnickými osobami"
description: "Tento postup ukazuje, jak nastavit a spustit proces odpisování pro více právnických osob."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: cs-cz
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="29822-103">Výpočet odpisů dlouhodobého majetku mezi právnickými osobami</span><span class="sxs-lookup"><span data-stu-id="29822-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29822-104">Odpis dlouhodobého majetku lze spustit napříč právnickými osobami v jediném kroku.</span><span class="sxs-lookup"><span data-stu-id="29822-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="29822-105">Tento postup ukazuje, jak nastavit a spustit proces pro více právnických osob.</span><span class="sxs-lookup"><span data-stu-id="29822-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="29822-106">Používá roli účetního.</span><span class="sxs-lookup"><span data-stu-id="29822-106">It uses the accountant role.</span></span>  

<span data-ttu-id="29822-107">Tento záznam používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="29822-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="29822-108">Kroky (16) Dílčí úlohy: Nastavte deníky spuštění odpisování napříč společností.</span><span class="sxs-lookup"><span data-stu-id="29822-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="29822-109">Nejprve musíte nastavit deníky pro použití při spuštění odepisování napříč společností v každé právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="29822-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="29822-110">Přejděte na Dlouhodobý majetek > Nastavení > Parametry dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="29822-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="29822-111">Rozbalte část Návrhy dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="29822-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="29822-112">Vytvořte záznam s názvem deníku, který má být použit pro každou účtovací vrstvu v právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="29822-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="29822-113">Pokud knihy neúčtují do hlavní knihy, pak s přidruženým deníkem zvolte možnost Žádná pro účtovací vrstvu.</span><span class="sxs-lookup"><span data-stu-id="29822-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="29822-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="29822-114">Click Add.</span></span> 
4. <span data-ttu-id="29822-115">V poli Účtovací vrstva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="29822-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="29822-116">V poli Název deníku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="29822-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="29822-117">Opakujte nastavení deníku na stránce Parametry dlouhodobého majetku u každé právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="29822-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="29822-118">Dílčí úkol: Výpočet odpisu</span><span class="sxs-lookup"><span data-stu-id="29822-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="29822-119">Použijte stránku Vytvořit návrh odpisu ke spuštění odepisování mezi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="29822-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="29822-120">Přejděte na Dlouhodobý majetek > Položky deníku > Vytvořit návrh odpisu.</span><span class="sxs-lookup"><span data-stu-id="29822-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="29822-121">V poli Účtovací vrstva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="29822-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="29822-122">Název deníku bude odvozen z parametrů dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="29822-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="29822-123">Lze změnit na tomto místě pro aktuální právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="29822-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="29822-124">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="29822-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="29822-125">Vyberte právnické osoby, které mají být zahrnuty do spuštění odpisů.</span><span class="sxs-lookup"><span data-stu-id="29822-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="29822-126">V seznamu se zobrazí pouze právnické osoby s deníky nastavenými pro návrhy dlouhodobého majetku na stránce Parametry dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="29822-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="29822-127">Když je povolena, možnost Zaúčtovat deníky automaticky zaúčtuje deníky odpisů, když jsou vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="29822-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="29822-128">Pokud není tato možnost zvolena, deníky se vytvoří, ale nebudou zaúčtovány, a proto je možné zkontrolovat podrobnosti před zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="29822-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="29822-129">Vyberte možnost Ano v poli Zaúčtovat deníky.</span><span class="sxs-lookup"><span data-stu-id="29822-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="29822-130">Filtrovací pole zahrnují dlouhodobý majetek, skupiny a knihy pro právnické osoby, které jsou vybrány pro toto spuštění odpisu.</span><span class="sxs-lookup"><span data-stu-id="29822-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="29822-131">Ve výchozím nastavení je povolena možnost Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="29822-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="29822-132">Pokud je tato možnost povolena, vytvoření a zaúčtování deníku odpisů se spustí na pozadí.</span><span class="sxs-lookup"><span data-stu-id="29822-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="29822-133">Klikněte na Vytvoří deník.</span><span class="sxs-lookup"><span data-stu-id="29822-133">Click Create journal.</span></span> 
10. <span data-ttu-id="29822-134">Musíte zobrazit deníky odpisů vytvořené v odpovídajících právnických osobách.</span><span class="sxs-lookup"><span data-stu-id="29822-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="29822-135">Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="29822-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>


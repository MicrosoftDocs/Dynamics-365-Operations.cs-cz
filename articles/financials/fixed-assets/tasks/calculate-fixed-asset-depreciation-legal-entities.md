---
title: Výpočet odpisů dlouhodobého majetku mezi právnickými osobami
description: Odpis dlouhodobého majetku lze spustit napříč právnickými osobami v jediném kroku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 500aa71e57f9c1ac8d1a2a080468381bc248741c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840090"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="fdf8b-103">Výpočet odpisů dlouhodobého majetku mezi právnickými osobami</span><span class="sxs-lookup"><span data-stu-id="fdf8b-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fdf8b-104">Odpis dlouhodobého majetku lze spustit napříč právnickými osobami v jediném kroku.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="fdf8b-105">Tento postup ukazuje, jak nastavit a spustit proces pro více právnických osob.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="fdf8b-106">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="fdf8b-107">Nastavení deníků spuštění odpisování napříč společností</span><span class="sxs-lookup"><span data-stu-id="fdf8b-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="fdf8b-108">Přejděte na Dlouhodobý majetek > Nastavení > Parametry dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="fdf8b-109">Rozbalte část Návrhy dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="fdf8b-110">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-110">Click Add.</span></span>
4. <span data-ttu-id="fdf8b-111">V poli Účtovací vrstva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="fdf8b-112">V poli Název deníku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="fdf8b-113">Opakujte nastavení deníku na stránce Parametry dlouhodobého majetku u každé právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="fdf8b-114">Spuštění odpisu</span><span class="sxs-lookup"><span data-stu-id="fdf8b-114">Depreciation run</span></span>
1. <span data-ttu-id="fdf8b-115">Přejděte na Dlouhodobý majetek > Položky deníku > Vytvořit návrh odpisu.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="fdf8b-116">V poli Účtovací vrstva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="fdf8b-117">Název deníku bude odvozen z parametrů dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="fdf8b-118">Lze změnit na tomto místě pro aktuální právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="fdf8b-119">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="fdf8b-120">Vyberte právnické osoby, které mají být zahrnuty do spuštění odpisů.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="fdf8b-121">V seznamu se zobrazí pouze právnické osoby s deníky nastavenými pro návrhy dlouhodobého majetku na stránce Parametry dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="fdf8b-122">Vyberte možnost Ano v poli Zaúčtovat deníky.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="fdf8b-123">Filtrovací pole zahrnují dlouhodobý majetek, skupiny a knihy pro právnické osoby, které jsou vybrány pro toto spuštění odpisu.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="fdf8b-124">Ve výchozím nastavení je povolena možnost Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="fdf8b-125">Pokud je tato možnost povolena, vytvoření a zaúčtování deníku odpisů se spustí na pozadí.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="fdf8b-126">Klikněte na Vytvoří deník.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-126">Click Create journal.</span></span>
6. <span data-ttu-id="fdf8b-127">Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="fdf8b-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>


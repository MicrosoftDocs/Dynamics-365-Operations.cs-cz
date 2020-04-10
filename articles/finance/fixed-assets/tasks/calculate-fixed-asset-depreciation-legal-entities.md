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
ms.openlocfilehash: 074a1b80584050302920a95c20fb547523a4866c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142908"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="a66cc-103">Výpočet odpisů dlouhodobého majetku mezi právnickými osobami</span><span class="sxs-lookup"><span data-stu-id="a66cc-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a66cc-104">Odpis dlouhodobého majetku lze spustit napříč právnickými osobami v jediném kroku.</span><span class="sxs-lookup"><span data-stu-id="a66cc-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="a66cc-105">Tento postup ukazuje, jak nastavit a spustit proces pro více právnických osob.</span><span class="sxs-lookup"><span data-stu-id="a66cc-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="a66cc-106">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="a66cc-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="a66cc-107">Nastavení deníků spuštění odpisování napříč společností</span><span class="sxs-lookup"><span data-stu-id="a66cc-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="a66cc-108">Přejděte na Dlouhodobý majetek > Nastavení > Parametry dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="a66cc-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="a66cc-109">Rozbalte část Návrhy dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="a66cc-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="a66cc-110">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="a66cc-110">Click Add.</span></span>
4. <span data-ttu-id="a66cc-111">V poli Účtovací vrstva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a66cc-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="a66cc-112">V poli Název deníku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a66cc-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="a66cc-113">Opakujte nastavení deníku na stránce Parametry dlouhodobého majetku u každé právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="a66cc-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="a66cc-114">Spuštění odpisu</span><span class="sxs-lookup"><span data-stu-id="a66cc-114">Depreciation run</span></span>
1. <span data-ttu-id="a66cc-115">Přejděte na Dlouhodobý majetek > Položky deníku > Vytvořit návrh odpisu.</span><span class="sxs-lookup"><span data-stu-id="a66cc-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="a66cc-116">V poli Účtovací vrstva zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a66cc-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="a66cc-117">Název deníku bude odvozen z parametrů dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="a66cc-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="a66cc-118">Lze změnit na tomto místě pro aktuální právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="a66cc-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="a66cc-119">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="a66cc-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="a66cc-120">Vyberte právnické osoby, které mají být zahrnuty do spuštění odpisů.</span><span class="sxs-lookup"><span data-stu-id="a66cc-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="a66cc-121">V seznamu se zobrazí pouze právnické osoby s deníky nastavenými pro návrhy dlouhodobého majetku na stránce Parametry dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="a66cc-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="a66cc-122">Vyberte možnost Ano v poli Zaúčtovat deníky.</span><span class="sxs-lookup"><span data-stu-id="a66cc-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="a66cc-123">Filtrovací pole zahrnují dlouhodobý majetek, skupiny a knihy pro právnické osoby, které jsou vybrány pro toto spuštění odpisu.</span><span class="sxs-lookup"><span data-stu-id="a66cc-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="a66cc-124">Ve výchozím nastavení je povolena možnost Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="a66cc-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="a66cc-125">Pokud je tato možnost povolena, vytvoření a zaúčtování deníku odpisů se spustí na pozadí.</span><span class="sxs-lookup"><span data-stu-id="a66cc-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="a66cc-126">Klikněte na Vytvoří deník.</span><span class="sxs-lookup"><span data-stu-id="a66cc-126">Click Create journal.</span></span>
6. <span data-ttu-id="a66cc-127">Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="a66cc-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>


---
title: Rozdělení dlouhodobého majetku
description: Toto téma vysvětluje, jak rozdělit procento jedné knihy majetku na novou knihu majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176757"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="236bb-103">Rozdělení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="236bb-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="236bb-104">Toto téma vysvětluje, jak rozdělit procento jedné knihy majetku na novou knihu majetku.</span><span class="sxs-lookup"><span data-stu-id="236bb-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="236bb-105">Používá účetní roli a vzorová data USMF.</span><span class="sxs-lookup"><span data-stu-id="236bb-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="236bb-106">Vytvořit nový dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="236bb-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="236bb-107">V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="236bb-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="236bb-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="236bb-108">Select **New**.</span></span>
3. <span data-ttu-id="236bb-109">Zadejte nebo vyberte hodnotu v poli **Skupina dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="236bb-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="236bb-110">Poznamenejte si číslo dlouhodobého majetku pro pozdější použití v procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="236bb-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="236bb-111">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="236bb-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="236bb-112">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="236bb-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="236bb-113">Rozdělení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="236bb-113">Split a fixed asset</span></span>
1. <span data-ttu-id="236bb-114">V seznamu najděte a vyberte odkaz na dlouhodobý majetek, který chcete rozdělit.</span><span class="sxs-lookup"><span data-stu-id="236bb-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="236bb-115">Vyberte **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="236bb-115">Select **Books**.</span></span> <span data-ttu-id="236bb-116">Vyberte knihu určenou pro rozdělení na nový majetek.</span><span class="sxs-lookup"><span data-stu-id="236bb-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="236bb-117">Vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="236bb-117">Select **Functions**.</span></span>
4. <span data-ttu-id="236bb-118">Vyberte **Rozdělit dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="236bb-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="236bb-119">Zadejte nebo vyberte hodnotu v poli **Do dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="236bb-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="236bb-120">V poli **Do knihy** vyberte tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="236bb-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="236bb-121">Zadejte datum do pole **Datum transakce**.</span><span class="sxs-lookup"><span data-stu-id="236bb-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="236bb-122">Zadejte číslo do pole **Procento**.</span><span class="sxs-lookup"><span data-stu-id="236bb-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="236bb-123">V poli **Název deníku** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="236bb-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="236bb-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="236bb-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="236bb-125">Zaúčtování transakce deníku</span><span class="sxs-lookup"><span data-stu-id="236bb-125">Post the journal transaction</span></span>
1. <span data-ttu-id="236bb-126">V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="236bb-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="236bb-127">V seznamu vyberte deník vytvořený pomocí procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="236bb-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="236bb-128">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="236bb-128">Select **Lines**.</span></span>

    - <span data-ttu-id="236bb-129">Ověřte, že byly vytvořeny řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="236bb-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="236bb-130">Transakce Oprava pořizovací ceny byla vytvořena pro původní majetek s cílem snížit hodnotu o procento uvedené během procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="236bb-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="236bb-131">Je vytvořena transakce pořízení pro nový majetek na stejnou částku.</span><span class="sxs-lookup"><span data-stu-id="236bb-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="236bb-132">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="236bb-132">Select **Post**.</span></span>


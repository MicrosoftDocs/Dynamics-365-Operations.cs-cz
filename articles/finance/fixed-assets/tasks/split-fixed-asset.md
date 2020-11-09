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
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000286"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="73b13-103">Rozdělení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="73b13-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73b13-104">Toto téma vysvětluje, jak rozdělit procento jedné knihy majetku na novou knihu majetku.</span><span class="sxs-lookup"><span data-stu-id="73b13-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="73b13-105">Používá účetní roli a vzorová data USMF.</span><span class="sxs-lookup"><span data-stu-id="73b13-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="73b13-106">Vytvořit nový dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="73b13-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="73b13-107">V navigačním podokně přejděte na **Moduly \> Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="73b13-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="73b13-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="73b13-108">Select **New**.</span></span>
3. <span data-ttu-id="73b13-109">Zadejte nebo vyberte hodnotu v poli **Skupina dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="73b13-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="73b13-110">Poznamenejte si číslo dlouhodobého majetku pro pozdější použití v procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="73b13-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="73b13-111">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="73b13-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="73b13-112">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="73b13-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="73b13-113">Rozdělení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="73b13-113">Split a fixed asset</span></span>

<span data-ttu-id="73b13-114">Před rozdělením plně odepsaného majetku je třeba ručně změnit stav rezervace majetku ze **Zavřeno** na **Otevřeno**.</span><span class="sxs-lookup"><span data-stu-id="73b13-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="73b13-115">Tento krok je nutný, protože stav rezervace musí být **Otevřeno** , pokud musíte pro majetek zaúčtovat transakce (například při odprodeji po vyřazení).</span><span class="sxs-lookup"><span data-stu-id="73b13-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="73b13-116">Po změně stavu rezervace majetku rozdělte majetek podle těchto pokynů.</span><span class="sxs-lookup"><span data-stu-id="73b13-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="73b13-117">V seznamu najděte a vyberte odkaz na dlouhodobý majetek, který chcete rozdělit.</span><span class="sxs-lookup"><span data-stu-id="73b13-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="73b13-118">Vyberte **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="73b13-118">Select **Books**.</span></span> <span data-ttu-id="73b13-119">Vyberte knihu určenou pro rozdělení na nový majetek.</span><span class="sxs-lookup"><span data-stu-id="73b13-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="73b13-120">Vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="73b13-120">Select **Functions**.</span></span>
4. <span data-ttu-id="73b13-121">Vyberte **Rozdělit dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="73b13-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="73b13-122">Zadejte nebo vyberte hodnotu v poli **Do dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="73b13-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="73b13-123">V poli **Do knihy** vyberte tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="73b13-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="73b13-124">Zadejte datum do pole **Datum transakce**.</span><span class="sxs-lookup"><span data-stu-id="73b13-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="73b13-125">Zadejte číslo do pole **Procento**.</span><span class="sxs-lookup"><span data-stu-id="73b13-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="73b13-126">V poli **Název deníku** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="73b13-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="73b13-127">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="73b13-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="73b13-128">Zaúčtování transakce deníku</span><span class="sxs-lookup"><span data-stu-id="73b13-128">Post the journal transaction</span></span>

1. <span data-ttu-id="73b13-129">V navigačním podokně přejděte na **Moduly \> Dlouhodobý majetek \> Položky deníku \> Deník dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="73b13-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="73b13-130">V seznamu vyberte deník vytvořený pomocí procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="73b13-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="73b13-131">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="73b13-131">Select **Lines**.</span></span>

    - <span data-ttu-id="73b13-132">Ověřte, že byly vytvořeny řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="73b13-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="73b13-133">Transakce Oprava pořizovací ceny byla vytvořena pro původní majetek s cílem snížit hodnotu o procento uvedené během procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="73b13-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="73b13-134">Je vytvořena transakce pořízení pro nový majetek na stejnou částku.</span><span class="sxs-lookup"><span data-stu-id="73b13-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="73b13-135">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="73b13-135">Select **Post**.</span></span>

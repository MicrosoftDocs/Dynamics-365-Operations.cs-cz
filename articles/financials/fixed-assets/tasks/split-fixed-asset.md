---
title: Rozdělení dlouhodobého majetku
description: Tento průvodce záznamem úloh rozdělí procento jedné knihy majetku na novou knihu majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566885"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="77df5-103">Rozdělení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="77df5-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="77df5-104">Tento průvodce záznamem úloh rozdělí procento jedné knihy majetku na novou knihu majetku.</span><span class="sxs-lookup"><span data-stu-id="77df5-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="77df5-105">Používá účetní roli a vzorová data USMF.</span><span class="sxs-lookup"><span data-stu-id="77df5-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="77df5-106">Vytvořit nový dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="77df5-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="77df5-107">Přejděte do části Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="77df5-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="77df5-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="77df5-108">Click New.</span></span>
3. <span data-ttu-id="77df5-109">Zadejte nebo vyberte hodnotu v poli Skupina dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="77df5-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="77df5-110">Poznamenejte si číslo dlouhodobého majetku pro pozdější použití v procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="77df5-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="77df5-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="77df5-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="77df5-112">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="77df5-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="77df5-113">Rozdělení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="77df5-113">Split a fixed asset</span></span>
1. <span data-ttu-id="77df5-114">V seznamu najděte a vyberte dlouhodobý majetek, který chcete rozdělit.</span><span class="sxs-lookup"><span data-stu-id="77df5-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="77df5-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="77df5-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="77df5-116">Klepněte na Knihy.</span><span class="sxs-lookup"><span data-stu-id="77df5-116">Click Books.</span></span>
    * <span data-ttu-id="77df5-117">Vyberte knihu určenou pro rozdělení na nový majetek.</span><span class="sxs-lookup"><span data-stu-id="77df5-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="77df5-118">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="77df5-118">Click Functions.</span></span>
5. <span data-ttu-id="77df5-119">Klikněte na Rozdělit dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="77df5-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="77df5-120">Zadejte nebo vyberte hodnotu v poli Do dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="77df5-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="77df5-121">V poli Do knihy kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="77df5-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="77df5-122">Zadejte datum do pole Datum transakce.</span><span class="sxs-lookup"><span data-stu-id="77df5-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="77df5-123">Zadejte číslo do pole Procento.</span><span class="sxs-lookup"><span data-stu-id="77df5-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="77df5-124">V poli Název deníku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="77df5-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="77df5-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="77df5-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="77df5-126">Zaúčtování transakce deníku</span><span class="sxs-lookup"><span data-stu-id="77df5-126">Post the journal transaction</span></span>
1. <span data-ttu-id="77df5-127">Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="77df5-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="77df5-128">V seznamu vyberte deník vytvořený pomocí procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="77df5-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="77df5-129">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="77df5-129">Click Lines.</span></span>
    * <span data-ttu-id="77df5-130">Ověřte, že byly vytvořeny řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="77df5-130">Verify the journal lines created.</span></span>  <span data-ttu-id="77df5-131">Transakce Oprava pořizovací ceny byla vytvořena pro původní majetek s cílem snížit hodnotu o procento uvedené během procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="77df5-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="77df5-132">Je vytvořena transakce pořízení pro nový majetek na stejnou částku.</span><span class="sxs-lookup"><span data-stu-id="77df5-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="77df5-133">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="77df5-133">Click Post.</span></span>


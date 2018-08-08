--- 
title: "Rozdělení dlouhodobého majetku"
description: "Tento průvodce záznamem úloh rozdělí procento jedné knihy majetku na novou knihu majetku."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ca96b07a944112bebc77aabd3d18fa95e0092373
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="73be2-103">Rozdělení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="73be2-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73be2-104">Tento průvodce záznamem úloh rozdělí procento jedné knihy majetku na novou knihu majetku.</span><span class="sxs-lookup"><span data-stu-id="73be2-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="73be2-105">Používá účetní roli a vzorová data USMF.</span><span class="sxs-lookup"><span data-stu-id="73be2-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="73be2-106">Vytvořit nový dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="73be2-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="73be2-107">Přejděte do části Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="73be2-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="73be2-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="73be2-108">Click New.</span></span>
3. <span data-ttu-id="73be2-109">Zadejte nebo vyberte hodnotu v poli Skupina dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="73be2-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="73be2-110">Poznamenejte si číslo dlouhodobého majetku pro pozdější použití v procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="73be2-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="73be2-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="73be2-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="73be2-112">Zavřete formulář.</span><span class="sxs-lookup"><span data-stu-id="73be2-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="73be2-113">Rozdělení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="73be2-113">Split a fixed asset</span></span>
1. <span data-ttu-id="73be2-114">V seznamu najděte a vyberte dlouhodobý majetek, který chcete rozdělit.</span><span class="sxs-lookup"><span data-stu-id="73be2-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="73be2-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="73be2-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="73be2-116">Klepněte na Knihy.</span><span class="sxs-lookup"><span data-stu-id="73be2-116">Click Books.</span></span>
    * <span data-ttu-id="73be2-117">Vyberte knihu určenou pro rozdělení na nový majetek.</span><span class="sxs-lookup"><span data-stu-id="73be2-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="73be2-118">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="73be2-118">Click Functions.</span></span>
5. <span data-ttu-id="73be2-119">Klikněte na Rozdělit dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="73be2-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="73be2-120">Zadejte nebo vyberte hodnotu v poli Do dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="73be2-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="73be2-121">V poli Do knihy kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="73be2-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="73be2-122">Zadejte datum do pole Datum transakce.</span><span class="sxs-lookup"><span data-stu-id="73be2-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="73be2-123">Zadejte číslo do pole Procento.</span><span class="sxs-lookup"><span data-stu-id="73be2-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="73be2-124">V poli Název deníku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="73be2-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="73be2-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="73be2-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="73be2-126">Zaúčtování transakce deníku</span><span class="sxs-lookup"><span data-stu-id="73be2-126">Post the journal transaction</span></span>
1. <span data-ttu-id="73be2-127">Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="73be2-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="73be2-128">V seznamu vyberte deník vytvořený pomocí procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="73be2-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="73be2-129">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="73be2-129">Click Lines.</span></span>
    * <span data-ttu-id="73be2-130">Ověřte, že byly vytvořeny řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="73be2-130">Verify the journal lines created.</span></span>  <span data-ttu-id="73be2-131">Transakce Oprava pořizovací ceny byla vytvořena pro původní majetek s cílem snížit hodnotu o procento uvedené během procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="73be2-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="73be2-132">Je vytvořena transakce pořízení pro nový majetek na stejnou částku.</span><span class="sxs-lookup"><span data-stu-id="73be2-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="73be2-133">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="73be2-133">Click Post.</span></span>



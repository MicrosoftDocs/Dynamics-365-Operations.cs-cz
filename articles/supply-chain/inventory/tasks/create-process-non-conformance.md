---
title: Vytvoření a zpracování neshody
description: Toto téma vysvětluje provádění správy neshody na základě existující objednávky kvality.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0c0c4415f490219485b3d96fa678a317c1f12f2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204118"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="f7410-103">Vytvoření a zpracování neshody</span><span class="sxs-lookup"><span data-stu-id="f7410-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7410-104">Toto téma vysvětluje provádění správy neshody na základě existující objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="f7410-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="f7410-105">Tento záznam lze spustit v ukázkové společnosti USMF a můžete navrhované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="f7410-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="f7410-106">Tento postup obvykle provádí úředník řízení kvality.</span><span class="sxs-lookup"><span data-stu-id="f7410-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="f7410-107">Nezbytným předpokladem je dokončení pokynů v části [Kontrola kvality zboží](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="f7410-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="f7410-108">Aby bylo možné zpracovat schválení neshody, uživatel, který spustí záznam úkolu, musí mít hodnotu "Název" přiřazenou na stránce Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="f7410-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="f7410-109">Aby bylo možné použít poznámky k dokumentům, uživatel musí také mít aktivováno řízení dokumentů v možnostech uživatele.</span><span class="sxs-lookup"><span data-stu-id="f7410-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="f7410-110">Vyberte objednávku kvality</span><span class="sxs-lookup"><span data-stu-id="f7410-110">Select a quality order</span></span>
1. <span data-ttu-id="f7410-111">V podokně navigace přejděte na **Moduly > Řízení zásob > Periodické úlohy > Správa kvality > Objednávky kvality**.</span><span class="sxs-lookup"><span data-stu-id="f7410-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="f7410-112">V seznamu vyberte objednávku kvality vytvořenou v části [Kontrola kvality zboží](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="f7410-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="f7410-113">Vytvoření neshody</span><span class="sxs-lookup"><span data-stu-id="f7410-113">Create a nonconformance</span></span>
1. <span data-ttu-id="f7410-114">V podokně akcí zvolte **Dotazy**.</span><span class="sxs-lookup"><span data-stu-id="f7410-114">In the action pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="f7410-115">Vyberte **Neshody**.</span><span class="sxs-lookup"><span data-stu-id="f7410-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="f7410-116">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f7410-116">Select **New**.</span></span>
4. <span data-ttu-id="f7410-117">V rozevírací nabídce pole **Typ problému** vyberte problém, který byl nalezen během procesu kontroly.</span><span class="sxs-lookup"><span data-stu-id="f7410-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="f7410-118">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7410-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="f7410-119">Schválení/zamítnutí neshody</span><span class="sxs-lookup"><span data-stu-id="f7410-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="f7410-120">Vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="f7410-120">Select **Functions**.</span></span>
2. <span data-ttu-id="f7410-121">Vyberte **Schválit neshodu**.</span><span class="sxs-lookup"><span data-stu-id="f7410-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="f7410-122">V tomto příkladu to je schválení neshody.</span><span class="sxs-lookup"><span data-stu-id="f7410-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="f7410-123">Schválené neshody lze přidružit k souvisejícím operacím k zaznamenání práce, která je provedena v průběhu zpracování neshody nebo během zpracování oprav jako v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="f7410-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="f7410-124">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f7410-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="f7410-125">Vytvoření akce opravy</span><span class="sxs-lookup"><span data-stu-id="f7410-125">Create a correction action</span></span>
1. <span data-ttu-id="f7410-126">Zvolte **Opravy**.</span><span class="sxs-lookup"><span data-stu-id="f7410-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="f7410-127">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f7410-127">Select **New**.</span></span>
3. <span data-ttu-id="f7410-128">V poli **Číslo zaměstnance** nového řádku vyberte požadovaný záznam z rozevírací nabídky.</span><span class="sxs-lookup"><span data-stu-id="f7410-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="f7410-129">Klepněte na tlačítko **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="f7410-129">Click **Select**.</span></span>
5. <span data-ttu-id="f7410-130">Vyberte **Připojit**.</span><span class="sxs-lookup"><span data-stu-id="f7410-130">Select **Attach**.</span></span> <span data-ttu-id="f7410-131">Vytvořte poznámku o opravě.</span><span class="sxs-lookup"><span data-stu-id="f7410-131">Create a note about the correction.</span></span> <span data-ttu-id="f7410-132">V tomto příkladu akce představuje kontaktování dodavatele za účelem diskuze o případu neshody.</span><span class="sxs-lookup"><span data-stu-id="f7410-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="f7410-133">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f7410-133">Select **New**.</span></span>
7. <span data-ttu-id="f7410-134">Zvolte **Poznámka**.</span><span class="sxs-lookup"><span data-stu-id="f7410-134">Select **Note**.</span></span> <span data-ttu-id="f7410-135">V závislosti na nastavení sestavy lze vytisknout různé typy dokumentů v sestavách, které se vztahují ke správě neshody.</span><span class="sxs-lookup"><span data-stu-id="f7410-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="f7410-136">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="f7410-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="f7410-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f7410-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="f7410-138">Údržba opravy</span><span class="sxs-lookup"><span data-stu-id="f7410-138">Maintain a correction</span></span>
1. <span data-ttu-id="f7410-139">Zvolte **Označit jako dokončené**.</span><span class="sxs-lookup"><span data-stu-id="f7410-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="f7410-140">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7410-140">Select **OK**.</span></span>
3. <span data-ttu-id="f7410-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f7410-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="f7410-142">Zavření neshody</span><span class="sxs-lookup"><span data-stu-id="f7410-142">Close a nonconformance</span></span>
1. <span data-ttu-id="f7410-143">Vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="f7410-143">Select **Functions**.</span></span>
2. <span data-ttu-id="f7410-144">Vyberte **Zavřít neshodu**.</span><span class="sxs-lookup"><span data-stu-id="f7410-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="f7410-145">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f7410-145">Select **Yes**.</span></span>
4. <span data-ttu-id="f7410-146">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="f7410-146">Close the pages.</span></span>

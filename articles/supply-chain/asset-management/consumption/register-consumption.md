---
title: Registrace spotřeby
description: Toto téma vysvětluje, jak registrovat spotřebu v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 61aea0261a62df9c029b429f33ba7b357621988b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259979"
---
# <a name="register-consumption"></a><span data-ttu-id="c369d-103">Registrace spotřeby</span><span class="sxs-lookup"><span data-stu-id="c369d-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c369d-104">Když byla úloha údržby dokončena na pracovním příkazu, následující krok provede registraci spotřeby a zaúčtuje deníky.</span><span class="sxs-lookup"><span data-stu-id="c369d-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="c369d-105">Registrace můžete provést u následujících typů spotřeby: hodiny, položky a výdaje.</span><span class="sxs-lookup"><span data-stu-id="c369d-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="c369d-106">Různé typy spotřeby jsou registrovány a zaúčtovány na stránce **Deníky pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="c369d-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="c369d-107">Nastavení deníku ve **Správě majetku** se používá k vytváření a zaúčtování samostatných deníků pro hodiny, položky a výdaje v modulu **Řízení a účetnictví projektu**.</span><span class="sxs-lookup"><span data-stu-id="c369d-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="c369d-108">Řádky prognózy můžete v některých případech přidávat nebo odstraňovat v rámci pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c369d-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="c369d-109">Nastavení stavu životního cyklu pracovního příkazu, související typ projektu a pravidla fáze související s typem projektu určují, zda lze přidávat nebo upravovat řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="c369d-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="c369d-110">Další informace o stavech životního cyklu pracovního příkazu a souvisejících fázích projektu si můžete přečíst v tématu [Prognózy, pracovní příkazy a projekty](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="c369d-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="c369d-111">Je možné nastavit automatické zaúčtování deníků ve stavu životního cyklu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c369d-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="c369d-112">Další informace najdete v části [Stavy životního cyklu pracovního příkazu](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="c369d-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="c369d-113">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="c369d-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c369d-114">Vyberte pracovní příkaz a klikněte na položku **Deníky**.</span><span class="sxs-lookup"><span data-stu-id="c369d-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="c369d-115">Kliknutím na možnost **Kopírovat z prognózy** můžete převést řádky prognózy, které mohou být spojeny s daným pracovním příkazem.</span><span class="sxs-lookup"><span data-stu-id="c369d-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="c369d-116">Můžete vybrat typy spotřeby, které chcete převést.</span><span class="sxs-lookup"><span data-stu-id="c369d-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="c369d-117">V případě potřeby můžete na příslušné pevné záložce přidat další řádky spotřeby kliknutím na položku **Přidat řádek** a vyplněním dat na řádku.</span><span class="sxs-lookup"><span data-stu-id="c369d-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="c369d-118">Kliknutím na možnost **Ověřit deníky** ověřte řádky deníku před zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="c369d-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="c369d-119">K zaúčtování řádků deníku klikněte na možnost **Zaúčtovat deníky**.</span><span class="sxs-lookup"><span data-stu-id="c369d-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="c369d-120">Po zaúčtování deníků spotřeby je možné aktualizovat stav životního cyklu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c369d-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="c369d-121">Chcete-li například označit, že byl pracovní příkaz dokončen, můžete stav životního cyklu aktualizovat na hodnotu ukončeno.</span><span class="sxs-lookup"><span data-stu-id="c369d-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="c369d-122">V poli **Zobrazit** v horní části stránky **Deníky pracovních příkazů** vyberte řádky deníku, které chcete zobrazit: **všechny**, **nezaúčtované** nebo **zaúčtované**.</span><span class="sxs-lookup"><span data-stu-id="c369d-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="c369d-123">Zaúčtované deníky mají zaškrtnutí v poli **Zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="c369d-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="c369d-124">Při vytvoření řádků položek v deníku pracovních příkazů se dimenze produktu a sledovací dimenze související s danou položkou automaticky přesunou do řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="c369d-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="c369d-125">Snímek obrazovky níže ukazuje příklad registrace hodin a položek na pracovním příkazu v **Denících pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="c369d-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Obrázek č. 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="c369d-127">Rozdělit hodiny na pracovní objednávky s několika úlohami pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="c369d-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="c369d-128">Obsahuje-li pracovní příkaz několik úloh pracovního příkazu, můžete zaregistrovat pracovní dobu pomocí funkce **Rozdělení hodin**, což znamená, že jeden řádek registrace hodin lze rovnoměrně rozložit na každé úloze pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c369d-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="c369d-129">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="c369d-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c369d-130">Vyberte pracovní příkaz a klikněte na položku **Deníky**.</span><span class="sxs-lookup"><span data-stu-id="c369d-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="c369d-131">Vyberte řádek registrace hodin, který chcete rozdělit, a klepněte na možnost **Rozdělení hodin**.</span><span class="sxs-lookup"><span data-stu-id="c369d-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="c369d-132">V dialogovém okně **Rozdělení hodin v práci údržby prac. příkazu** je v poli **Pracovník** automaticky zobrazen název přihlášeného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="c369d-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="c369d-133">V případě potřeby můžete vybrat jiného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="c369d-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="c369d-134">V poli **Kategorie** vyberte kategorii pro registraci hodin.</span><span class="sxs-lookup"><span data-stu-id="c369d-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="c369d-135">Zadejte počet odpracovaných hodin, které mají být rozděleny v poli **Hodiny**.</span><span class="sxs-lookup"><span data-stu-id="c369d-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![Obrázek č. 2](media/02-consumption.png)

7. <span data-ttu-id="c369d-137">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="c369d-137">Click **OK**.</span></span>

<span data-ttu-id="c369d-138">*Příklad:* v dolní části obrazovky se zobrazí řádky deníku pro pracovní příkaz, které obsahují tři úlohy pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c369d-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="c369d-139">První řádek, který obsahuje tři pracovní hodiny, byl rozdělen a pro každou úlohu pracovního příkazu je registrována jedna pracovní hodina.</span><span class="sxs-lookup"><span data-stu-id="c369d-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="c369d-140">Po vytvoření tří řádků pro registraci hodin se rozhodnete, co dělat s původním řádkem registrace hodin (první řádek v příkladu).</span><span class="sxs-lookup"><span data-stu-id="c369d-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="c369d-141">Můžete ji ponechat tak, jak je, nebo ji odstranit.</span><span class="sxs-lookup"><span data-stu-id="c369d-141">You can keep it as is or delete it.</span></span> 

![Obrázek č. 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="c369d-143">Finanční dimenze pro registrace spotřeby</span><span class="sxs-lookup"><span data-stu-id="c369d-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="c369d-144">Při provádění registrace spotřeby se do registrací v určitém pořadí přidají finanční dimenze související s různými typy registrací.</span><span class="sxs-lookup"><span data-stu-id="c369d-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="c369d-145">*Registrace hodin a výdajů:* nejprve se přidají finanční dimenze ze záhlaví deníku, pokud existují.</span><span class="sxs-lookup"><span data-stu-id="c369d-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="c369d-146">Dále se přidají finanční dimenze z souvisejícího projektu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c369d-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="c369d-147">Nakonec se přidají finanční dimenze od zdroje (pracovník).</span><span class="sxs-lookup"><span data-stu-id="c369d-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="c369d-148">*Registrace položek:* nejprve se přidají finanční dimenze ze záhlaví deníku, pokud existují.</span><span class="sxs-lookup"><span data-stu-id="c369d-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="c369d-149">Potom se přidají finanční dimenze z souvisejícího projektu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="c369d-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="c369d-150">Dále budou přidány finanční dimenze z pracoviště.</span><span class="sxs-lookup"><span data-stu-id="c369d-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="c369d-151">Nakonec se přidají finanční dimenze z položky.</span><span class="sxs-lookup"><span data-stu-id="c369d-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="c369d-152">Pro všechny tři typy registrace je ověřována kombinace finančních dimenzí a neplatné kombinace jsou prázdné.</span><span class="sxs-lookup"><span data-stu-id="c369d-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="c369d-153">Jedná se o standardní nastavení u dalších aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c369d-153">This is standard setup with other Finance and Operations apps.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
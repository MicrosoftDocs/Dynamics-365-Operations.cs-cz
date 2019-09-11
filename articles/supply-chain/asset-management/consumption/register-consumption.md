---
title: Registrace spotřeby
description: Toto téma vysvětluje, jak registrovat spotřebu v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f785b0935b952d6de68fd120a3639077ad124bd
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913075"
---
# <a name="register-consumption"></a><span data-ttu-id="5f903-103">Registrace spotřeby</span><span class="sxs-lookup"><span data-stu-id="5f903-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5f903-104">Když byla úloha údržby dokončena na pracovním příkazu, následující krok provede registraci spotřeby a zaúčtuje deníky.</span><span class="sxs-lookup"><span data-stu-id="5f903-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="5f903-105">Registrace můžete provést u následujících typů spotřeby: hodiny, položky a výdaje.</span><span class="sxs-lookup"><span data-stu-id="5f903-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="5f903-106">Různé typy spotřeby jsou registrovány a zaúčtovány na stránce **Deníky pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="5f903-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="5f903-107">Nastavení deníku ve **Správě majetku** se používá k vytváření a zaúčtování samostatných deníků pro hodiny, položky a výdaje v modulu **Řízení a účetnictví projektu**.</span><span class="sxs-lookup"><span data-stu-id="5f903-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="5f903-108">Řádky prognózy můžete přidávat nebo odstraňovat v rámci pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="5f903-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="5f903-109">Nastavení stavu životního cyklu pracovního příkazu, související typ projektu a pravidla fáze související s typem projektu určují, zda lze přidávat nebo upravovat řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="5f903-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="5f903-110">Další informace o stavech životního cyklu pracovního příkazu a souvisejících fází najdete v tématu [Integrace do řízení a účetnictví projektu](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="5f903-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="5f903-111">Je možné nastavit automatické zaúčtování deníků ve stavu životního cyklu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="5f903-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="5f903-112">Další informace najdete v části [Stavy životního cyklu pracovního příkazu](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="5f903-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="5f903-113">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="5f903-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="5f903-114">Vyberte pracovní příkaz a klikněte na položku **Deníky**.</span><span class="sxs-lookup"><span data-stu-id="5f903-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="5f903-115">Kliknutím na možnost **Kopírovat z prognózy** můžete převést řádky prognózy, které mohou být spojeny s daným pracovním příkazem.</span><span class="sxs-lookup"><span data-stu-id="5f903-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="5f903-116">Můžete vybrat typy spotřeby, které chcete převést.</span><span class="sxs-lookup"><span data-stu-id="5f903-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="5f903-117">V případě potřeby můžete na příslušné pevné záložce přidat další řádky spotřeby kliknutím na položku **Přidat řádek** a vyplněním dat na řádku.</span><span class="sxs-lookup"><span data-stu-id="5f903-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="5f903-118">Kliknutím na možnost **Ověřit deníky** ověřte řádky deníku před zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="5f903-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="5f903-119">K zaúčtování řádků deníku klikněte na možnost **Zaúčtovat deníky**.</span><span class="sxs-lookup"><span data-stu-id="5f903-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="5f903-120">Po zaúčtování deníků spotřeby je možné aktualizovat stav životního cyklu pracovního příkazu, například "Ukončeno", což znamená, že daný pracovní příkaz byl dokončen.</span><span class="sxs-lookup"><span data-stu-id="5f903-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="5f903-121">V poli **Zobrazit** v horní části stránky **Deníky pracovních příkazů** vyberte řádky deníku, které chcete zobrazit: všechny, nezaúčtované nebo zaúčtované.</span><span class="sxs-lookup"><span data-stu-id="5f903-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="5f903-122">Zaúčtované deníky mají zaškrtnutí v poli **Zaúčtováno**.</span><span class="sxs-lookup"><span data-stu-id="5f903-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="5f903-123">Při vytvoření řádků položek v deníku pracovních příkazů se dimenze produktu a sledovací dimenze související s danou položkou automaticky přesunou do řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="5f903-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="5f903-124">Snímek obrazovky níže ukazuje příklad registrace hodin a položek na pracovním příkazu v **Denících pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="5f903-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Obrázek č. 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="5f903-126">Rozdělit hodiny na pracovní objednávky s několika úlohami pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="5f903-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="5f903-127">Obsahuje-li pracovní příkaz několik úloh pracovního příkazu, můžete zaregistrovat pracovní dobu pomocí funkce **Rozdělení hodin**, což znamená, že jeden řádek registrace hodin lze rovnoměrně rozložit na každé úloze pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="5f903-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="5f903-128">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="5f903-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="5f903-129">Vyberte pracovní příkaz a klikněte na položku **Deníky**.</span><span class="sxs-lookup"><span data-stu-id="5f903-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="5f903-130">Vyberte řádek registrace hodin, který chcete rozdělit, a klepněte na možnost **Rozdělení hodin**.</span><span class="sxs-lookup"><span data-stu-id="5f903-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="5f903-131">V dialogovém okně **Rozdělení hodin v práci údržby prac. příkazu** je v poli **Pracovník** automaticky zobrazen název přihlášeného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="5f903-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="5f903-132">V případě potřeby můžete vybrat jiného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="5f903-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="5f903-133">V poli **Kategorie** vyberte kategorii pro registraci hodin.</span><span class="sxs-lookup"><span data-stu-id="5f903-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="5f903-134">Zadejte počet odpracovaných hodin, které mají být rozděleny v poli **Hodiny**.</span><span class="sxs-lookup"><span data-stu-id="5f903-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![Obrázek č. 2](media/02-consumption.png)

7. <span data-ttu-id="5f903-136">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5f903-136">Click **OK**.</span></span>

<span data-ttu-id="5f903-137">*Příklad:* v dolní části obrazovky se zobrazí řádky deníku pro pracovní příkaz, které obsahují tři úlohy pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="5f903-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="5f903-138">První řádek, který obsahuje tři pracovní hodiny, byl rozdělen a pro každou úlohu pracovního příkazu je registrována jedna pracovní hodina.</span><span class="sxs-lookup"><span data-stu-id="5f903-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="5f903-139">Po vytvoření tří řádků pro registraci hodin se rozhodnete, co dělat s původním řádkem registrace hodin (první řádek v příkladu).</span><span class="sxs-lookup"><span data-stu-id="5f903-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="5f903-140">Můžete ji ponechat tak, jak je, nebo ji odstranit.</span><span class="sxs-lookup"><span data-stu-id="5f903-140">You can keep it as is or delete it.</span></span> 

![Obrázek č. 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="5f903-142">Finanční dimenze pro registrace spotřeby</span><span class="sxs-lookup"><span data-stu-id="5f903-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="5f903-143">Při provádění registrace spotřeby se do registrací v určitém pořadí přidají finanční dimenze související s různými typy registrací.</span><span class="sxs-lookup"><span data-stu-id="5f903-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="5f903-144">*Registrace hodin a výdajů:* nejprve se přidají finanční dimenze ze záhlaví deníku, pokud existují.</span><span class="sxs-lookup"><span data-stu-id="5f903-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="5f903-145">Dále se přidají finanční dimenze z souvisejícího projektu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="5f903-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="5f903-146">Nakonec se přidají finanční dimenze od zdroje (pracovník).</span><span class="sxs-lookup"><span data-stu-id="5f903-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="5f903-147">*Registrace položek:* nejprve se přidají finanční dimenze ze záhlaví deníku, pokud existují.</span><span class="sxs-lookup"><span data-stu-id="5f903-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="5f903-148">Potom se přidají finanční dimenze z souvisejícího projektu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="5f903-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="5f903-149">Dále budou přidány finanční dimenze z pracoviště.</span><span class="sxs-lookup"><span data-stu-id="5f903-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="5f903-150">Nakonec se přidají finanční dimenze z položky.</span><span class="sxs-lookup"><span data-stu-id="5f903-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="5f903-151">Pro všechny tři typy registrace je ověřována kombinace finančních dimenzí a neplatné kombinace jsou prázdné.</span><span class="sxs-lookup"><span data-stu-id="5f903-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="5f903-152">Jedná se o standardní nastavení v aplikaci Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f903-152">This is standard setup in Dynamics 365 for Finance and Operations.</span></span>


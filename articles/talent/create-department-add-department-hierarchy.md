---
title: "Tvorba oddělení a jeho přidružení do hierarchie oddělení"
description: "Oddělení je provozní jednotka, která představuje kategorie nebo funkční oblasti organizace. Oddělení je zodpovědný za určitou oblast organizace, jako například prodej, účtování nebo lidské zdroje. Oddělení můžete použít k sestavování funkčních oblastí. Oddělení mohou mít odpovědnost ze zisků a ztrát."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cea3ecd66a57780c9ef1b3a3c21f1e5273faa0ef
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a><span data-ttu-id="78f05-106">Tvorba oddělení a jeho přidružení do hierarchie oddělení</span><span class="sxs-lookup"><span data-stu-id="78f05-106">Create a department and associate it with the department hierarchy</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="78f05-107">Oddělení je provozní jednotka, která představuje kategorie nebo funkční oblasti organizace.</span><span class="sxs-lookup"><span data-stu-id="78f05-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="78f05-108">Oddělení je zodpovědný za určitou oblast organizace, jako například prodej, účtování nebo lidské zdroje.</span><span class="sxs-lookup"><span data-stu-id="78f05-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="78f05-109">Oddělení můžete použít k sestavování funkčních oblastí.</span><span class="sxs-lookup"><span data-stu-id="78f05-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="78f05-110">Oddělení mohou mít odpovědnost ze zisků a ztrát.</span><span class="sxs-lookup"><span data-stu-id="78f05-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="78f05-111">Oddělení mohou obsahovat i skupinu nákladových středisek.</span><span class="sxs-lookup"><span data-stu-id="78f05-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="78f05-112">Pozice lze přiřadit k oddělení.</span><span class="sxs-lookup"><span data-stu-id="78f05-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="78f05-113">Chcete-li vytvořit oddělení, klikněte na možnost **Lidské zdroje** &gt; **Oddělení** &gt; **Oddělení**.</span><span class="sxs-lookup"><span data-stu-id="78f05-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="78f05-114">V následující tabulce jsou popsána pole, která jsou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="78f05-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="78f05-115">Pole</span><span class="sxs-lookup"><span data-stu-id="78f05-115">Field</span></span>               | <span data-ttu-id="78f05-116">Popis</span><span class="sxs-lookup"><span data-stu-id="78f05-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78f05-117">Název</span><span class="sxs-lookup"><span data-stu-id="78f05-117">Name</span></span>                | <span data-ttu-id="78f05-118">Zadejte název oddělení.</span><span class="sxs-lookup"><span data-stu-id="78f05-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="78f05-119">Číslo oddělení</span><span class="sxs-lookup"><span data-stu-id="78f05-119">Department number</span></span>   | <span data-ttu-id="78f05-120">výchozí hodnota může být generována automaticky, pokud je přiřazen kód číselné řady k odkazu **Číslo organizace** na stránce **Číselné řady**.</span><span class="sxs-lookup"><span data-stu-id="78f05-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="78f05-121">Vyhledávací název</span><span class="sxs-lookup"><span data-stu-id="78f05-121">Search name</span></span>         | <span data-ttu-id="78f05-122">Zadejte název nebo zkratku, které lze použít pro rychlé hledání oddělení.</span><span class="sxs-lookup"><span data-stu-id="78f05-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="78f05-123">Poznámka</span><span class="sxs-lookup"><span data-stu-id="78f05-123">Memo</span></span>                | <span data-ttu-id="78f05-124">Sem zadejte případné doplňkové informace.</span><span class="sxs-lookup"><span data-stu-id="78f05-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="78f05-125">V hierarchii</span><span class="sxs-lookup"><span data-stu-id="78f05-125">In hierarchy</span></span>        | <span data-ttu-id="78f05-126">Zaškrtnuté políčko označuje, že oddělení je součástí hierarchie oddělení.</span><span class="sxs-lookup"><span data-stu-id="78f05-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="78f05-127">Informace o přidávání oddělení do hierarchie oddělení naleznete níže v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="78f05-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="78f05-128">Číslo DUNS</span><span class="sxs-lookup"><span data-stu-id="78f05-128">DUNS number</span></span>         | <span data-ttu-id="78f05-129">Zkratka DUNS znamená systém čísel univerzálních dat.</span><span class="sxs-lookup"><span data-stu-id="78f05-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="78f05-130">Toto je devíticiferné číslo vydané organizací Dun & Bradstreet.</span><span class="sxs-lookup"><span data-stu-id="78f05-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="78f05-131">Manažer</span><span class="sxs-lookup"><span data-stu-id="78f05-131">Manager</span></span>             | <span data-ttu-id="78f05-132">Zadejte osobu, které řídí oddělení.</span><span class="sxs-lookup"><span data-stu-id="78f05-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="78f05-133">Adresy</span><span class="sxs-lookup"><span data-stu-id="78f05-133">Addresses</span></span>           | <span data-ttu-id="78f05-134">Přidejte informace o adrese pro oddělení</span><span class="sxs-lookup"><span data-stu-id="78f05-134">Add the address information for the department.</span></span> <span data-ttu-id="78f05-135">Například můžete přidat poštovní adresu budovy, ve které se oddělení nachází.</span><span class="sxs-lookup"><span data-stu-id="78f05-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="78f05-136">Kontaktní informace</span><span class="sxs-lookup"><span data-stu-id="78f05-136">Contact information</span></span> | <span data-ttu-id="78f05-137">Přidejte kontaktní informace pro oddělení.</span><span class="sxs-lookup"><span data-stu-id="78f05-137">Add contact information for the department.</span></span> <span data-ttu-id="78f05-138">Například můžete přidat telefonní číslo na oddělení služeb v oddělení.</span><span class="sxs-lookup"><span data-stu-id="78f05-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="78f05-139">Pro přidání oddělení do hierarchie oddělení postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="78f05-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="78f05-140">Klikněte na nabídku **Lidské zdroje** &gt; **Oddělení** &gt; **Hierarchie oddělení**.</span><span class="sxs-lookup"><span data-stu-id="78f05-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="78f05-141">Klepněte na tlačítko **Upravit**a poté vyberte organizaci, pod kterou má oddělení spadat.</span><span class="sxs-lookup"><span data-stu-id="78f05-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="78f05-142">Klepněte na tlačítko **Vložit**a v seznamu vyberte **Oddělení**.</span><span class="sxs-lookup"><span data-stu-id="78f05-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="78f05-143">V zobrazeném seznamu oddělení vyberte oddělení, které chcete přidat do hierarchie.</span><span class="sxs-lookup"><span data-stu-id="78f05-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="78f05-144">Uložte změny.</span><span class="sxs-lookup"><span data-stu-id="78f05-144">Save your changes.</span></span> <span data-ttu-id="78f05-145">Obdržíte zprávu, že byla vytvořena pracovní verzi hierarchie.</span><span class="sxs-lookup"><span data-stu-id="78f05-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="78f05-146">Po dokončení práce klikněte v návrháři hierarchie na tlačítko **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="78f05-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="78f05-147">Můžete zadat datum začátku platnosti, které určuje, kdy má být hierarchie publikována.</span><span class="sxs-lookup"><span data-stu-id="78f05-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="78f05-148">Například chcete-li přidat nové oddělení na začátku dalšího kalendářního roku, nastavte platné datum od 1. ledna nového kalendářního roku.</span><span class="sxs-lookup"><span data-stu-id="78f05-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="78f05-149">Změny hierarchie se projeví k tomuto datu.</span><span class="sxs-lookup"><span data-stu-id="78f05-149">The changes to the hierarchy will take effect on that date.</span></span>






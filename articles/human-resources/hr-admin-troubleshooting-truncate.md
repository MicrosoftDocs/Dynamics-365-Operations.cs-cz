---
title: Zabránění zkrácení textu na hierarchii pozic a export do aplikace Visio
description: Tento článek vysvětluje, jak vyřešit problém, kdy jsou názvy osob a pozic zkráceny při odběratelově zobrazení hierarchie pozic v aplikaci Microsoft Dynamics 365 Human Resources. Zkrácení textu může ztížit pořízení snímku obrazovky nebo tisk hierarchie.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f8310def6f33b807f7f749e659432e482245d007
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803866"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="bbb6d-104">Zabránění zkrácení textu na hierarchii pozic a export do aplikace Visio</span><span class="sxs-lookup"><span data-stu-id="bbb6d-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bbb6d-105">**Výdej**</span><span class="sxs-lookup"><span data-stu-id="bbb6d-105">**Issue**</span></span>

<span data-ttu-id="bbb6d-106">Když si zákazník zobrazí hierarchii pozic v aplikaci Microsoft Dynamics 365 Human Resources, názvy osob a pozic jsou zkráceny.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Human Resources, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="bbb6d-107">Z tohoto důvodu může být obtížné provést snímek obrazovky, nebo vytisknout a rozdělit hierarchii.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Hierarchie pozic](media/position-h.png)

<span data-ttu-id="bbb6d-109">**Příčina**</span><span class="sxs-lookup"><span data-stu-id="bbb6d-109">**Cause**</span></span>

<span data-ttu-id="bbb6d-110">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-110">This behavior is by design.</span></span>

<span data-ttu-id="bbb6d-111">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="bbb6d-111">**Resolution**</span></span>

<span data-ttu-id="bbb6d-112">Bohužel uživatelé nemohou snadno změnit velikost textu.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="bbb6d-113">Můžete však exportovat hierarchii pozic mimo aplikaci Human Resources a potom ji importovat do aplikace Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-113">However, you can export the position hierarchy out of Human Resources and then import it into Microsoft Visio.</span></span> <span data-ttu-id="bbb6d-114">Ačkoli je následující článek určen pro aplikaci Microsoft Dynamics AX 2012, proces platí i pro Human Resources: [Exportovat hierarchii pozic do aplikace Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="bbb6d-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Human Resources: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="bbb6d-115">Tento postup slouží k exportu do aplikace Visio.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="bbb6d-116">V modulu Lidské zdroje otevřete stránku se seznamem **pozic**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-116">In Human Resources, open the **Positions** list page.</span></span>

    <span data-ttu-id="bbb6d-117">Chcete-li do diagramu struktury organizace zahrnout další informace, přidejte pole do seznamu **Pozice**, aby byly k dispozici při použití tohoto průvodce později v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="bbb6d-118">V podokně akcí, vyberte tlačítko **Otevřít v aplikaci Microsoft Office** a poté v nabídce **Exportovat do aplikace Excel** vyberte **Pozice**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="bbb6d-119">Případně stiskněte Ctrl+T.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-119">Alternatively, press Ctrl+T.</span></span>

    ![Export stránky se seznamem Pozice do aplikace Excel](media/org-admin.png)

3. <span data-ttu-id="bbb6d-121">Uložte soubor aplikace Excel, který je vyexportovaný.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-121">Save the Excel file that is exported.</span></span>

    ![Export do dialogového okna Excelu](media/export-excel.png)

4. <span data-ttu-id="bbb6d-123">V aplikaci Visio vyberte **Visio – Vytvořit novou** a vyberte kategorii šablony **Obchodní**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Nový diagram](media/new.png)

5. <span data-ttu-id="bbb6d-125">Vyberte **Průvodce grafem organizace** a poté vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Dialogové okno průvodce grafem organizace](media/orgchart-wizard.png)

6. <span data-ttu-id="bbb6d-127">Vyberte **Informace, které jsou již uložené v souboru nebo databázi** a poté vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Průvodce grafem organizace 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="bbb6d-129">Zvolte **Text, Org Plus (\*.txt), nebo soubor aplikace Excel** a poté zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Průvodce grafem organizace 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="bbb6d-131">Vyhledejte exportovaný soubor aplikace Excel, který obsahuje hierarchii pozic, a poté vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Průvodce grafem organizace 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="bbb6d-133">Nastavte pole **Název** na **pozice**, nastavte pole **Nadřízená pozice** na **Podřízený pozice** a poté vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Průvodce grafem organizace 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="bbb6d-135">Vyberte pole, která mají být zobrazena na každém uzlu, a poté vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Průvodce grafem organizace 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="bbb6d-137">Přidejte sloupec **Pozice** do seznamu **Pole vlastností obrazce** a pak vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Průvodce grafem organizace 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="bbb6d-139">Obrázky nejsou v současné době k dispozici.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-139">Pictures aren't currently available.</span></span> <span data-ttu-id="bbb6d-140">Proto na další stránce vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="bbb6d-141">Vyberte **Chci, aby průvodce automaticky rozdělil organizační schéma mezi stránky**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Průvodce grafem organizace 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="bbb6d-143">Vyberte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-143">Select **Finish**.</span></span>

    <span data-ttu-id="bbb6d-144">Pokud existují nějaké pozice, které nejsou ve struktuře, budete vyzváni k jejich zařazení do schématu.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="bbb6d-145">Diagram, který se vygeneruje v aplikaci Visio, zobrazuje každého manažera v samostatném listu.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="bbb6d-146">Na základě polí, která jste vybrali do schématu, každý uzel zobrazí příslušné informace při generování souboru Visio.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Diagram hierarchie](media/hierarchy.png)

<span data-ttu-id="bbb6d-148">**Další možnost**</span><span class="sxs-lookup"><span data-stu-id="bbb6d-148">**Additional option**</span></span>

<span data-ttu-id="bbb6d-149">V aplikaci Human Resources můžete rovněž použít pracovní prostor **Osoby** pro zobrazení některých informací souvisejících s hierarchií.</span><span class="sxs-lookup"><span data-stu-id="bbb6d-149">In Human Resources, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
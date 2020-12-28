---
title: Nastavení správy nabídek v aplikaci Attract
description: Toto téma popisuje, jak nastavit nabídky v aplikaci Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc91a83afd5ce1627376685bcf612d6998ddbc02
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460557"
---
# <a name="set-up-offer-management-in-attract"></a><span data-ttu-id="11d62-103">Nastavení správy nabídek v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="11d62-103">Set up offer management in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="11d62-104">Když je kandidát posunut do fáze nabídky v aplikaci Dynamics 365 Talent: Attract, musíte zajistit, aby bylo možné nabídky kandidátům rychle vytvořit, schválit podle potřeby a zaslat kandidátovi.</span><span class="sxs-lookup"><span data-stu-id="11d62-104">When a candidate is moved to the offer stage in Dynamics 365 Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="11d62-105">Vzhledem k tomu, že většina nabídek je standardní, lze je vytvořit z opětovně použitelných šablon.</span><span class="sxs-lookup"><span data-stu-id="11d62-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="11d62-106">V aplikaci Attract budou všechny nabídky sbaleny do balíčku nabídky, což je kolekce jednoho nebo více dokumentů nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="11d62-107">Toto téma uvádí seznam všech kroků, které by měl správce aplikace Attract provést pro nastavení různých šablon balíčku nabídky jako součást funkce správy nabídky v aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="11d62-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="11d62-108">Uživatelé bez role správce nemají přístup k těmto funkcím.</span><span class="sxs-lookup"><span data-stu-id="11d62-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="11d62-109">Funkce správy nabídky jsou k dispozici jako součást doplňku komplexního náboru.</span><span class="sxs-lookup"><span data-stu-id="11d62-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="11d62-110">Data nabídky</span><span class="sxs-lookup"><span data-stu-id="11d62-110">Offer data</span></span> 

<span data-ttu-id="11d62-111">Data nabídky jsou nejmenší jednotkou uvnitř šablony balíčku nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="11d62-112">Typická nabídka se skládá ze standardního textu a sady hodnot.</span><span class="sxs-lookup"><span data-stu-id="11d62-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="11d62-113">Sady hodnot jsou pouze kusy, které se mohou změnit mezi nabídkami.</span><span class="sxs-lookup"><span data-stu-id="11d62-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="11d62-114">Během vytváření nabídky je nejdůležitějším aspektem, na který se tvůrce nabídky může zaměřit, seznam zástupných textů dat nabídky v šabloně balíčku nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="11d62-115">Pro nastavení dat nabídky postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="11d62-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="11d62-116">Přejděte na možnost **Správa nabídky**.</span><span class="sxs-lookup"><span data-stu-id="11d62-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="11d62-117">Rozbalte část **Knihovna** v levém navigačním podokně a pak přejděte na **Data nabídky**.</span><span class="sxs-lookup"><span data-stu-id="11d62-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="11d62-118">Na stránce **Data nabídky** jsou části **Podrobnosti o kandidátovi** a **Podrobnosti o práci**.</span><span class="sxs-lookup"><span data-stu-id="11d62-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="11d62-119">Attract poskytuje několik vestavěných zástupných textů pro data nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    > 
    > <span data-ttu-id="11d62-120">Existují části na stránce pro uspořádání různých zástupných textů dat nabídky do logických skupin.</span><span class="sxs-lookup"><span data-stu-id="11d62-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="11d62-121">Tyto části mohou pomoci s údržbou dat nabídky a naplňováním dat během procesu vytváření nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>
    > 
    > <span data-ttu-id="11d62-122">Chcete-li vytvořit seznam hodnot pro zástupný text, odešlete tabulku aplikace Excel obsahující jeden sloupec se zástupným textem coby název sloupce a seznam voleb v řádcích pod ním.</span><span class="sxs-lookup"><span data-stu-id="11d62-122">To create a list of values for a placeholder, upload an Excel spreadsheet that has one column with the placeholder as the column title and the list of choices in the rows underneath.</span></span> <span data-ttu-id="11d62-123">Pokud je na stejný zástupný text odkazováno v jiné sadě pravidel dat, ujistěte se, že mají společnou sadu hodnot.</span><span class="sxs-lookup"><span data-stu-id="11d62-123">If the same placeholder is referenced in another data rule set, ensure they have a common set of values.</span></span>
    
1.  <span data-ttu-id="11d62-124">Chcete-li vytvořit novou část dat nabídky, klikněte na **Přidat sekci** a zadejte jedinečný název pro sekci.</span><span class="sxs-lookup"><span data-stu-id="11d62-124">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="11d62-125">Chcete-li přidat zástupné texty dat nabídky pro jakoukoliv část, klikněte na **Přidat data nabídky** a zadejte jedinečný název pro zástupný text.</span><span class="sxs-lookup"><span data-stu-id="11d62-125">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="11d62-126">Chcete-li upravit název jakékoliv části, podržte ukazatel myši nad názvem části a aktualizujte název.</span><span class="sxs-lookup"><span data-stu-id="11d62-126">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="11d62-127">Chcete-li upravit název jakéhokoliv existujícího zástupného textu dat nabídky, nejprve se ujistěte, zda zástupný text již není součástí nějaké šablony.</span><span class="sxs-lookup"><span data-stu-id="11d62-127">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="11d62-128">Potom ukazatelem myši najeďte nad název zástupného textu dat nabídky a aktualizujte název podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="11d62-128">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="11d62-129">Chcete-li odstranit existující zástupný text dat nabídky, nejprve se ujistěte, zda zástupný text není součástí jiné šablony.</span><span class="sxs-lookup"><span data-stu-id="11d62-129">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="11d62-130">Potom ukazatelem myši najeďte nad zástupný text a když se objeví ikona koše, klikněte na koš pro odstranění zástupného textu dat nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-130">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="11d62-131">Můžete vidět, kolika šablon je zástupný text dat nabídky součástí podle číselného ukazatele vedle každých dat nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-131">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="11d62-132">Chcete-li odstranit jakoukoliv část, najeďte myší nad název.</span><span class="sxs-lookup"><span data-stu-id="11d62-132">To delete any section, hover over the name.</span></span> <span data-ttu-id="11d62-133">Pokud se v žádné šabloně neobjeví žádný zástupný text dat nabídky v části, můžete ho smazat kliknutím na ikonu koše.</span><span class="sxs-lookup"><span data-stu-id="11d62-133">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="11d62-134">Odstraněním části budou také odstraněny všechny zástupné texty dat nabídky v rámci této části.</span><span class="sxs-lookup"><span data-stu-id="11d62-134">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="11d62-135">Jakmile byly nastaveny zástupné texty dat nabídky, můžete je použít v jakékoli šabloně dokumentu</span><span class="sxs-lookup"><span data-stu-id="11d62-135">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="11d62-136">Zástupné texty dat nabídky nejsou omezeny na určitou šablonu - stejnou sadu lze použít ve všech šablonách.</span><span class="sxs-lookup"><span data-stu-id="11d62-136">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="11d62-137">Pravidla dat nabídky</span><span class="sxs-lookup"><span data-stu-id="11d62-137">Offer data rules</span></span>

<span data-ttu-id="11d62-138">Většina organizací má pravidla pro vytváření nabídek.</span><span class="sxs-lookup"><span data-stu-id="11d62-138">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="11d62-139">Například organizace může požadovat, aby maximální roční mzdová nabídka pro konkrétní kombinaci místa a úrovně služebního věku byla v určitém rozsahu, nebo aby existovalo jen několik konkrétních hodnot možných pro úroveň nabídky pro nově přijatého zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="11d62-139">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="11d62-140">Attract aktuálně podporuje všechna taková pravidla dat pomocí souboru CSV.</span><span class="sxs-lookup"><span data-stu-id="11d62-140">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="11d62-141">Chcete-li připravit CSV soubor pravidel dat, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="11d62-141">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="11d62-142">Určete zástupný text dat nabídky pro sadu pravidel.</span><span class="sxs-lookup"><span data-stu-id="11d62-142">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="11d62-143">Například **Roční mzda**.</span><span class="sxs-lookup"><span data-stu-id="11d62-143">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="11d62-144">Určete závislé hodnoty zástupného textu dat nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-144">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="11d62-145">Například **Místo výkonu práce** a **Úroveň**.</span><span class="sxs-lookup"><span data-stu-id="11d62-145">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="11d62-146">Určete sloupce 1 a 2 jako **Místo výkonu práce** a **Úroveň**.</span><span class="sxs-lookup"><span data-stu-id="11d62-146">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="11d62-147">Chcete-li načíst hodnotu rozsahu, udělejte ze sloupců 3 a 4 **roční mzdu**.</span><span class="sxs-lookup"><span data-stu-id="11d62-147">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="11d62-148">Chcete-li načíst konkrétní hodnotu místo rozsahu , udělejte **roční mzdu** pouze ze sloupce 3.</span><span class="sxs-lookup"><span data-stu-id="11d62-148">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="11d62-149">Naplňte soubor aplikace Microsoft Excel na základě vašich požadovaných rolí.</span><span class="sxs-lookup"><span data-stu-id="11d62-149">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="11d62-150">Ujistěte se, že každý řádek je jedinečnou kombinací všech hodnot spojených dohromady.</span><span class="sxs-lookup"><span data-stu-id="11d62-150">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="11d62-151">Uložte soubor jako CSV formát.</span><span class="sxs-lookup"><span data-stu-id="11d62-151">Save the file as a CSV format.</span></span>

<span data-ttu-id="11d62-152">Chcete-li odeslat soubor pravidel dat nabídky, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="11d62-152">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="11d62-153">Přejděte na možnost **Správa nabídky**.</span><span class="sxs-lookup"><span data-stu-id="11d62-153">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="11d62-154">Rozbalte část **Knihovna** v levém navigačním podokně a pak přejděte na **Pravidla dat nabídky**.</span><span class="sxs-lookup"><span data-stu-id="11d62-154">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="11d62-155">Klikněte na možnost **Nová sada dat** a zobrazte dialogové okno **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="11d62-155">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="11d62-156">Zadejte jedinečný název pro sadu pravidel a poté odešlete uložený soubor CSV.</span><span class="sxs-lookup"><span data-stu-id="11d62-156">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="11d62-157">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="11d62-157">Click **Add**.</span></span>
    <span data-ttu-id="11d62-158">Sada pravidel bude zpracována na pozadí a po dokončení budete upozorněni v aplikaci a e-mailem.</span><span class="sxs-lookup"><span data-stu-id="11d62-158">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="11d62-159">Budete upozorněni, pokud dojde k chybám při zpracování odeslání.</span><span class="sxs-lookup"><span data-stu-id="11d62-159">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="11d62-160">Můžete poté stáhnout protokol chyb, opravit soubor a odeslat ho znovu.</span><span class="sxs-lookup"><span data-stu-id="11d62-160">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="11d62-161">Klikněte na tlačítko s třemi tečkami (**...**), pokud chcete stáhnout sadu pravidel a odeslat sadu hodnot.</span><span class="sxs-lookup"><span data-stu-id="11d62-161">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="11d62-162">Po aktualizaci můžete odeslat soubor znovu.</span><span class="sxs-lookup"><span data-stu-id="11d62-162">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="11d62-163">Pokud se definovaný zástupný text nepoužívá v jiné šabloně dokumentu, můžete odstranit stávající odeslání sady pravidel.</span><span class="sxs-lookup"><span data-stu-id="11d62-163">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="11d62-164">Každý zástupný text může mít pouze jednu jedinečnou sadu sloupců, na které je závislý.</span><span class="sxs-lookup"><span data-stu-id="11d62-164">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="11d62-165">Například pokud je **Roční mzda** závislá na **místu výkonu práce** a **úrovni**, nelze odeslat jinou sadu pravidel, kde **roční mzda** závisí na odlišné sadě sloupců.</span><span class="sxs-lookup"><span data-stu-id="11d62-165">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="11d62-166">Můžete stáhnout vzorové sady pravidel dat nabídky na kartě **Ukázky** na stránce **Pravidla dat nabídky**.</span><span class="sxs-lookup"><span data-stu-id="11d62-166">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="11d62-167">Když tvůrce nabídky přepíše hodnoty, které jsou doporučeny pravidly dat nabídky, nabídka je označena jako nestandardní a workflow schvalování nabídek bude nařízeno.</span><span class="sxs-lookup"><span data-stu-id="11d62-167">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="11d62-168">Šablony dokumentů</span><span class="sxs-lookup"><span data-stu-id="11d62-168">Document templates</span></span>

<span data-ttu-id="11d62-169">Šablona dokumentu s nabídkou může pomoct správcům s vytvářením dopisů s nabídkou.</span><span class="sxs-lookup"><span data-stu-id="11d62-169">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="11d62-170">Šablona dokumentu s nabídkou je kombinací textu, který bude součástí nabídky, a definovaných zástupných textů dat nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-170">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="11d62-171">Chcete-li vytvořit šablonu dokumentu nabídky, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="11d62-171">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="11d62-172">Přejděte na možnost **Správa nabídky**.</span><span class="sxs-lookup"><span data-stu-id="11d62-172">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="11d62-173">Rozbalte část **Knihovna** v levém navigačním podokně a přejděte na **Šablony**.</span><span class="sxs-lookup"><span data-stu-id="11d62-173">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="11d62-174">Stránka **Šablony** zobrazí seznam šablon dokumentů, které již byly definovány.</span><span class="sxs-lookup"><span data-stu-id="11d62-174">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="11d62-175">Chcete-li vytvořit novou šablonu dokumentu, klikněte na **Nová šablona**.</span><span class="sxs-lookup"><span data-stu-id="11d62-175">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="11d62-176">Zadejte jedinečný název pro šablonu a klikněte na **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="11d62-176">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="11d62-177">Použijte editoru formátovaného textu nebo upravte obsah dokumentu nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-177">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="11d62-178">Můžete vložit tabulky, obrázky a hypertextové odkazy pomocí možností dostupných v horní části textového editoru.</span><span class="sxs-lookup"><span data-stu-id="11d62-178">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="11d62-179">Do dokumentu šablony nabídky můžete vložit zástupné texty dat nabídky pomocí:</span><span class="sxs-lookup"><span data-stu-id="11d62-179">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="11d62-180">Přetažením z pravého podokna.</span><span class="sxs-lookup"><span data-stu-id="11d62-180">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="11d62-181">Použitím hashtagu k zástupnému textu dat nabídky přímo na pozici.</span><span class="sxs-lookup"><span data-stu-id="11d62-181">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="11d62-182">Napište **\#** a poté začněte psát název zástupného textu dat nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-182">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="11d62-183">Možnosti se zobrazí v rozevíracím seznamu.</span><span class="sxs-lookup"><span data-stu-id="11d62-183">Options will appear in the drop-down list.</span></span> <span data-ttu-id="11d62-184">Klikněte nebo stiskněte **Enter** pro vložení zástupného textu dat nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-184">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="11d62-185">Chcete-li přidružit zástupný text do šablony dokumentu nabídky, aniž byste odkryli jeho hodnotu kandidátovi, najeďte myší nad zástupný text dat nabídky a klikněte na ikonu **špendlíku**.</span><span class="sxs-lookup"><span data-stu-id="11d62-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="11d62-186">To posune zástupný text do části **Připnutá data nabídky** šablony dokumentu nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="11d62-187">Pro odepnutí postupujte podle stejných kroků, ale v seznamu zástupných textů dat nabídky klikněte na **Odepnout**.</span><span class="sxs-lookup"><span data-stu-id="11d62-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="11d62-188">Chcete-li zobrazit seznam aktivních zástupných textů dat nabídky, přepněte na kartu **Aktivní** v pravém podokně.</span><span class="sxs-lookup"><span data-stu-id="11d62-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="11d62-189">Pokud vložíte zástupný text, který je řízen sadou pravidel dat nabídky, zobrazí se závislost tohoto zástupného textu dat nabídky na jiných hodnotách.</span><span class="sxs-lookup"><span data-stu-id="11d62-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="11d62-190">Popřípadě můžete **importovat** obsah ze souboru DOCX na svůj místní počítač a podle potřeby ho upravit.</span><span class="sxs-lookup"><span data-stu-id="11d62-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="11d62-191">Tímto způsobem nemusíte zadávat veškerý obsah v editoru.</span><span class="sxs-lookup"><span data-stu-id="11d62-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="11d62-192">Chcete-li zobrazit náhled dokumentu nabídky, použijte možnost **Náhled** v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="11d62-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="11d62-193">Chcete-li kontrolovat, zda tvůrce nabídky může upravovat obsah dokumentu s nabídkou, použijte možnost **Spravovat oprávnění** v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="11d62-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="11d62-194">Pokud chcete, aby mohl tvůrce nabídky pouze vkládat zástupné texty, nikoliv upravovat text, nastavte hodnotu oprávnění na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="11d62-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="11d62-195">Kliknutím na tlačítko **Uložit** uložte svůj průběh.</span><span class="sxs-lookup"><span data-stu-id="11d62-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="11d62-196">Šablona bude uložena ve stavu konceptu.</span><span class="sxs-lookup"><span data-stu-id="11d62-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="11d62-197">Chcete-li dokončit a označit dokument jako zveřejněný, klikněte na **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="11d62-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="11d62-198">Můžete zobrazit, které šablony dokumentu jsou momentálně aktivní, v režimu konceptu a archivované a již nepoužívané v cílovém rozhraní knihovny šablon dokumentů.</span><span class="sxs-lookup"><span data-stu-id="11d62-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="11d62-199">Můžete odstranit všechny šablony dokumentu s nabídkou, které nejsou součástí stávající šablony balíčku nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="11d62-200">Šablony balíčku nabídky</span><span class="sxs-lookup"><span data-stu-id="11d62-200">Offer package templates</span></span>

<span data-ttu-id="11d62-201">Balíčky nabídky jsou artefakty nabídky, které jsou sdíleny s kandidáty a které se skládají z kombinace jedné nebo více šablon dokumentů s nabídkou.</span><span class="sxs-lookup"><span data-stu-id="11d62-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="11d62-202">Chcete-li vytvořit balíček, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="11d62-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="11d62-203">Přejděte na možnost **Správa nabídky**.</span><span class="sxs-lookup"><span data-stu-id="11d62-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="11d62-204">Přejděte na **Balíčky** z levého navigačního podokna.</span><span class="sxs-lookup"><span data-stu-id="11d62-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="11d62-205">Zobrazí se seznam aktivních šablon balíčků, které jsou k dispozici k použití pro tvůrce nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="11d62-206">Chcete-li vytvořit nová balíček s nabídkou, klikněte na **Nový balíček**.</span><span class="sxs-lookup"><span data-stu-id="11d62-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="11d62-207">Zadejte jedinečný název a klikněte na **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="11d62-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="11d62-208">Klikněte na možnost **Přidat šablonu**.</span><span class="sxs-lookup"><span data-stu-id="11d62-208">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="11d62-209">Můžete zvolit vytvoření nové šablony nebo si vybrat jednu z již existujících šablon.</span><span class="sxs-lookup"><span data-stu-id="11d62-209">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="11d62-210">Pokud si zvolíte přidání existující šablony, musíte se ujistit, že šablona dokumentu nabídky byla uložena, dokončena a označena jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="11d62-210">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="11d62-211">Můžete si vybrat tolik šablon dokumentu, kolik chcete.</span><span class="sxs-lookup"><span data-stu-id="11d62-211">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="11d62-212">Klikněte na **Hotovo** pro návrat na položku **Správa balíčku**.</span><span class="sxs-lookup"><span data-stu-id="11d62-212">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="11d62-213">Můžete konfigurovat posloupnost dokumentů a také označit, zda je při vytváření nabídky požadován konkrétní dokument nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-213">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="11d62-214">Tvůrce nabídky bude mít možnost odstranit dokumenty označené jako **Nevyžadované**.</span><span class="sxs-lookup"><span data-stu-id="11d62-214">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="11d62-215">Chcete-li uložit šablonu balíčku nabídky, aby byla použitelná pro všechny tvůrce nabídky, klikněte na tlačítko **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="11d62-215">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="11d62-216">Chcete-li zobrazit koncepty šablon balíčku nabídky, přejděte na kartu **Koncepty**. Pokud je provedena změna šablony balíčku nabídky, musí být uložena a znovu publikována.</span><span class="sxs-lookup"><span data-stu-id="11d62-216">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="11d62-217">Konfigurace procesu nabídky</span><span class="sxs-lookup"><span data-stu-id="11d62-217">Configure an offer process</span></span>

<span data-ttu-id="11d62-218">Existuje několik částí procesu vytváření nabídky, které může konfigurovat správce aplikace Attract.</span><span class="sxs-lookup"><span data-stu-id="11d62-218">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="11d62-219">**Schválení nabídky** – Zvolte, zda jsou schválení nabídky požadována předtím, než může být nabídka odeslána kandidátovi.</span><span class="sxs-lookup"><span data-stu-id="11d62-219">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="11d62-220">Jako správce můžete také rozhodnout, zda ke všem schválením nabídky dojde ve workflow postupného nebo souběžného schvalování.</span><span class="sxs-lookup"><span data-stu-id="11d62-220">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="11d62-221">Můžete také přikázat, zda musí schvalovatelé nabídky přidat komentář ke svému schválení nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-221">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="11d62-222">Schválení nabídky jsou povinná pro všechny nestandardní nabídky.</span><span class="sxs-lookup"><span data-stu-id="11d62-222">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="11d62-223">**Vypršení nabídky kandidátovi** -Jako správce můžete určit, zda mají všechny nabídky datum vypršení platnosti, a pokud ano, jaký by mě být výchozí posun pro datum vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="11d62-223">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="11d62-224">Můžete také nastavit, zda kandidáti mohou odmítnout nabídku.</span><span class="sxs-lookup"><span data-stu-id="11d62-224">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="11d62-225">**Elektronické podpisy** -jako správce můžete také zvolit metodu, kterou mohou uchazeči používat k podepisování nabídek.</span><span class="sxs-lookup"><span data-stu-id="11d62-225">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="11d62-226">Adobe Sign - všechny nabídky budou odeslány a podepisovány pomocí Adobe Sign.</span><span class="sxs-lookup"><span data-stu-id="11d62-226">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="11d62-227">Každý autor nabídky, který ji publikuje, musí mít připojený účet Adobe Sign k aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="11d62-227">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="11d62-228">Ohledně licencí Adobe Sign a bezplatných zkušebních verzí navštivte tento [odkaz](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="11d62-228">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="11d62-229">DocuSign - všechny nabídky budou odeslány a podepisovány pomocí DocuSign.</span><span class="sxs-lookup"><span data-stu-id="11d62-229">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="11d62-230">Každý autor nabídky, který ji publikuje, musí mít připojený účet DocuSign k aplikaci Attract.</span><span class="sxs-lookup"><span data-stu-id="11d62-230">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="11d62-231">ESign – Toto je výchozí možnost poskytovaná přímo po vybalení, kde může uživatel podepsat nabídku zadáním svého jména a iniciál.</span><span class="sxs-lookup"><span data-stu-id="11d62-231">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="11d62-232">Další informace o procesu vytváření nabídky naleznete v tématu [Vytvoření, schválení a podepsání nabídek](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="11d62-232">To learn more about the offer creation process, see [Create, approve, and sign offers](./creating-offers.md).</span></span>

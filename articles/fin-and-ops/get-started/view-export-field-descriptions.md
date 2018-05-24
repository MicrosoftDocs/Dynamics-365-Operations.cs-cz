---
title: "Zobrazení a export popisů polí"
description: "Tento článek popisuje, jak zobrazit popisy pole, a jak používat stránku Popisy pole pro export popisů."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d1ee87dbe9dab089a893d9c69d2573a4c4b11b58
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="8805c-103">Zobrazení a export popisů polí</span><span class="sxs-lookup"><span data-stu-id="8805c-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8805c-104">Tento článek popisuje, jak zobrazit popisy pole, a jak používat stránku Popisy pole pro export popisů.</span><span class="sxs-lookup"><span data-stu-id="8805c-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="8805c-105">Microsoft Dynamics 365 for Finance and Operations má k dispozici pro některá složitější pole popisy.</span><span class="sxs-lookup"><span data-stu-id="8805c-105">Microsoft Dynamics 365 for Finance and Operations has descriptions for some of the more complex fields.</span></span> <span data-ttu-id="8805c-106">Tyto popisy se zobrazí při přesunutí ukazatele myši na pole.</span><span class="sxs-lookup"><span data-stu-id="8805c-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="8805c-107">Stránka **Popis polí** slouží také k zobrazení a exportu popisů polí.</span><span class="sxs-lookup"><span data-stu-id="8805c-107">You can also view and export descriptions on the **Field descriptions** page.</span></span> 

<span data-ttu-id="8805c-108">Ne všechny stránky obsahují popis polí.</span><span class="sxs-lookup"><span data-stu-id="8805c-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="8805c-109">Chceme poskytnout popisy pro složitější pole a nikoliv pro ty, kde je jejich použití zřejmé.</span><span class="sxs-lookup"><span data-stu-id="8805c-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="8805c-110">Proto některé stránky nemají žádné popisy pole, některé stránky mají několik popisů a některé složitější stránky, například mnoho stránek s parametry, mají mnoho popisů.</span><span class="sxs-lookup"><span data-stu-id="8805c-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span> 

<span data-ttu-id="8805c-111">Pokud máte přístup k vývojovému prostředí v aplikaci Finance and Operations, můžete přidat nový popis polí nebo stávající popisy přizpůsobit.</span><span class="sxs-lookup"><span data-stu-id="8805c-111">If you have access to the Finance and Operations development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="8805c-112">Můžete například přidat informace specifické pro společnost do popisu pole.</span><span class="sxs-lookup"><span data-stu-id="8805c-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="8805c-113">Další informace naleznete viz [Přizpůsobení nápovědy pole](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="8805c-113">For more information, see [Customize field help](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="8805c-114">Zobrazení popisu pole v uživatelském rozhraní</span><span class="sxs-lookup"><span data-stu-id="8805c-114">See field descriptions in the user interface</span></span>
<span data-ttu-id="8805c-115">Popis polí lze zobrazit umístěním ukazatele myši na pole.</span><span class="sxs-lookup"><span data-stu-id="8805c-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="8805c-116">Pokud není k dispozici žádný popis, zobrazí se po přesunutí ukazatele myši na pole název pole.</span><span class="sxs-lookup"><span data-stu-id="8805c-116">If no description is available, you see the field name when you hover over the field.</span></span> <span data-ttu-id="8805c-117">(Poznámka: V aplikaci Dynamics AX 7.0 (únor 2016) lze zobrazit popisy polí jen na stránce **Popisy polí**.) Následující obrázek znázorňuje popisy polí, které se zobrazí při přesunutí ukazatele myši na pole **Uzamknout položky během inventury**.</span><span class="sxs-lookup"><span data-stu-id="8805c-117">(Note: In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.) The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span> 

<span data-ttu-id="8805c-118">[![Příklad popisu pole](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="8805c-118">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="8805c-119">Pomocí stránky Popis pole můžete zobrazit a exportovat nápovědu pro pole</span><span class="sxs-lookup"><span data-stu-id="8805c-119">Use the Field descriptions page to view and export field help</span></span>
<span data-ttu-id="8805c-120">Stránka **Popis polí** slouží e zobrazení a exportu popisů polí.</span><span class="sxs-lookup"><span data-stu-id="8805c-120">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="8805c-121">Současně můžete zobrazit popisy, které jsou k dispozici na jedné stránce.</span><span class="sxs-lookup"><span data-stu-id="8805c-121">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="8805c-122">Zobrazení popisů pro stránku</span><span class="sxs-lookup"><span data-stu-id="8805c-122">View the descriptions for a page</span></span>

<span data-ttu-id="8805c-123">Pro zobrazení popisů pro stránku postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="8805c-123">To view the descriptions for a page, follow this step.</span></span>

-   <span data-ttu-id="8805c-124">Do pole **Vybrat stránku** zadejte název stránky.</span><span class="sxs-lookup"><span data-stu-id="8805c-124">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="8805c-125">Můžete také klepnutím na šipku otevřít seznam všech stránek a stránku vyhledat nebo seznam filtrovat.</span><span class="sxs-lookup"><span data-stu-id="8805c-125">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="8805c-126">Můžete použít také název stránky, která se zobrazí v uživatelském rozhraní (například: **Odběratelé**), nebo název kódu (název stromu AOT), který zpřístupníte kliknutím pravým tlačítkem myši na stránku (například **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="8805c-126">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span> 

<span data-ttu-id="8805c-127">Informace o různých způsobech, jak filtrovat seznam stránek, naleznete v části "Hledání stránky" níže v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="8805c-127">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span> 

<span data-ttu-id="8805c-128">Pokud jste nastavili možnost **Zahrnout pole bez popisu** na **Ano**, všechna pole na stránce se zobrazí bez ohledu na to, zda mají popis pole.</span><span class="sxs-lookup"><span data-stu-id="8805c-128">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="8805c-129">Export popisů pro stránku</span><span class="sxs-lookup"><span data-stu-id="8805c-129">Export the descriptions for a page</span></span>

<span data-ttu-id="8805c-130">Pro exportování popisů pro stránku postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="8805c-130">To export the descriptions for a page, follow these steps.</span></span>

1.  <span data-ttu-id="8805c-131">Vyberte stránku v poli **Vybrat stránku**.</span><span class="sxs-lookup"><span data-stu-id="8805c-131">In the **Select a page** field, select a page.</span></span>
2.  <span data-ttu-id="8805c-132">Klikněte na tlačítko **Otevřít v aplikaci Microsoft Office** v pravém horním rohu a potom klikněte na možnost **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="8805c-132">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="8805c-133">Hledání stránky</span><span class="sxs-lookup"><span data-stu-id="8805c-133">Searching for a page</span></span>

<span data-ttu-id="8805c-134">Vyhledat stránku v poli **Vybrat stránku** lze několika způsoby.</span><span class="sxs-lookup"><span data-stu-id="8805c-134">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="8805c-135">V mnoha případech je nutné kliknout na tlačítko se šipkou v poli **Vybrat stránku** pro otevření rozevíracího seznamu a výběr z filtrovaného seznamu stránek.</span><span class="sxs-lookup"><span data-stu-id="8805c-135">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

-   <span data-ttu-id="8805c-136">Zadejte část názvu a pak otevřete rozevírací seznam pro výběr z filtrovaného seznamu stránek.</span><span class="sxs-lookup"><span data-stu-id="8805c-136">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
-   <span data-ttu-id="8805c-137">Otevřete rozevírací seznam a klikněte na záhlaví **Název stránky** v horní části seznamu, nebo na záhlaví **Název AOT stránky**.</span><span class="sxs-lookup"><span data-stu-id="8805c-137">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="8805c-138">Otevře se dialogové okno, ve kterém můžete vybrat možnosti rozšířeného filtrování, jako například **Název stránky začíná na**.</span><span class="sxs-lookup"><span data-stu-id="8805c-138">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
-   <span data-ttu-id="8805c-139">Zadejte úplný název stránky.</span><span class="sxs-lookup"><span data-stu-id="8805c-139">Type the full name of the page.</span></span> <span data-ttu-id="8805c-140">Při použití této možnosti je nejvhodnější otevřít rozevírací seznam a zjistit, co další se nachází v seznamu, i když se zobrazí popis polí.</span><span class="sxs-lookup"><span data-stu-id="8805c-140">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>
    -   <span data-ttu-id="8805c-141">Pokud existuje jediná přesná shoda s názvem, tyto popisy polí se zobrazí na této stránce.</span><span class="sxs-lookup"><span data-stu-id="8805c-141">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    -   <span data-ttu-id="8805c-142">Pokud existuje více než jediná přesná shoda, nezobrazí se žádné popisy.</span><span class="sxs-lookup"><span data-stu-id="8805c-142">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="8805c-143">Bude nutné otevřít rozevírací seznam a vybrat požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="8805c-143">You must open the drop-down list and select the page that you want.</span></span>
    -   <span data-ttu-id="8805c-144">Pokud název, který jste zadali, je také částí názvu další stránky, zobrazí se popisy pro vaši stránku.</span><span class="sxs-lookup"><span data-stu-id="8805c-144">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="8805c-145">Pokud ale otevřete rozevírací seznam, zobrazí se další stránky, které obsahují tento název.</span><span class="sxs-lookup"><span data-stu-id="8805c-145">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="8805c-146">Například nejsou zobrazeny žádné popisy, když zadáte <strong>Inventura</strong> do pole *<strong><em>Vybrat stránku</em></strong>*.</span><span class="sxs-lookup"><span data-stu-id="8805c-146">For example, no descriptions are shown when you type <strong>Counting</strong> in the *<strong><em>Select a page</em></strong>* field.</span></span> <span data-ttu-id="8805c-147">Pokud kliknete na rozevírací seznam, zjistíte, že existují dvě stránky s názvem <strong>Inventura</strong> a také několik stránek, které obsahují v názvu slovo „Inventura“.</span><span class="sxs-lookup"><span data-stu-id="8805c-147">You open the drop-down list, and see that there are two pages that have the name <strong>Counting</strong> and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="8805c-148">Pokud vyberete stránku, který má název stromu AOT <strong>InventJournalCount</strong>, zobrazí se pro tuto stránku popisy polí.</span><span class="sxs-lookup"><span data-stu-id="8805c-148">If you select the page that has the AOT name <strong>InventJournalCount</strong>, the field descriptions are shown for that page.</span></span> <span data-ttu-id="8805c-149">Pokud však znovu otevřete na rozevírací seznam, zobrazený seznam nyní obsahuje všechny stránky, které mají „InventJournalCount“ jako součást jejich názvu stromu AOT.</span><span class="sxs-lookup"><span data-stu-id="8805c-149">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="8805c-150">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="8805c-150">Troubleshooting</span></span>
<span data-ttu-id="8805c-151">Tato sekce obsahuje informace o řešení problémů, ke kterým může dojít při používání popisů pole.</span><span class="sxs-lookup"><span data-stu-id="8805c-151">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="8805c-152">Nelze najít popis pole</span><span class="sxs-lookup"><span data-stu-id="8805c-152">I can't find a field description</span></span>

<span data-ttu-id="8805c-153">Právě probíhá přidávání popisů pro složitější pole.</span><span class="sxs-lookup"><span data-stu-id="8805c-153">We’re in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="8805c-154">Potřebujete-li nápovědu pro konkrétní pole, informujte nás přidáním komentáře k tomuto tématu.</span><span class="sxs-lookup"><span data-stu-id="8805c-154">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="8805c-155">Pole popisu není užitečné</span><span class="sxs-lookup"><span data-stu-id="8805c-155">The field description isn't helpful</span></span>

<span data-ttu-id="8805c-156">Informujte nás přidáním komentáře k tomuto tématu.</span><span class="sxs-lookup"><span data-stu-id="8805c-156">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="8805c-157">Pokud je to možné, uveďte další informace, které požadujete.</span><span class="sxs-lookup"><span data-stu-id="8805c-157">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="8805c-158">Nelze najít pole na stránce Popisy pole</span><span class="sxs-lookup"><span data-stu-id="8805c-158">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="8805c-159">Pokud chcete zobrazit všechna pole na stránce, nastavte pro možnost **Zahrnout pole bez popisu** hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8805c-159">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="8805c-160">Klepněte na pole **Vybrat stránku** a ověřte, že jste vybrali správnou stránku.</span><span class="sxs-lookup"><span data-stu-id="8805c-160">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="8805c-161">Pokud název, který jste zadali, je součástí názvu jiného pole, pravděpodobně jste vybrali stránku, který má delší název.</span><span class="sxs-lookup"><span data-stu-id="8805c-161">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="8805c-162">Nelze najít stránku na stránce Popisy pole</span><span class="sxs-lookup"><span data-stu-id="8805c-162">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="8805c-163">Informace o různých způsobech, jak vyhledat stránky, naleznete v části "Hledání stránek" dříve v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="8805c-163">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="8805c-164">Pokud jste zadali přesný název stránky, pravděpodobně nebudou zobrazeny v popisech polí, pokud existuje více než jedna stránka se stejným názvem.</span><span class="sxs-lookup"><span data-stu-id="8805c-164">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="8805c-165">Klikněte na šipku v poli **Vybrat stránku**, abyste otevřeli filtrovaný seznam dostupných stránek.</span><span class="sxs-lookup"><span data-stu-id="8805c-165">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

<a name="additional-resources"></a><span data-ttu-id="8805c-166">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="8805c-166">Additional resources</span></span>
--------

[<span data-ttu-id="8805c-167">Přizpůsobení nápovědy pole</span><span class="sxs-lookup"><span data-stu-id="8805c-167">Customize field help</span></span>](../../dev-itpro/user-interface/customize-field-help.md)






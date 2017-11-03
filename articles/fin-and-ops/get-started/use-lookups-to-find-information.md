---
title: "Zjišťování informací pomocí vyhledávání"
description: "Mnoho polí v aplikaci Microsoft Dynamics 365 for Finance and Operations umožňuje snadné vyhledávání správných a požadovaných hodnot. Vyhledávání bylo několika způsoby vylepšeno – ovládací prvky jsou nyní užitečnější a uživatelé díky nim mohou být produktivnější. V tomto tématu se dozvíte o těchto nových funkcích a užitečných tipech k optimálnímu využití vyhledávání v systému."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 013901724864092571099835b2c71b297710ff03
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="use-lookups-to-find-information"></a><span data-ttu-id="5488b-105">Zjišťování informací pomocí vyhledávání</span><span class="sxs-lookup"><span data-stu-id="5488b-105">Use lookups to find information</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5488b-106">Mnoho polí v aplikaci Microsoft Dynamics 365 for Finance and Operations umožňuje snadné vyhledávání správných a požadovaných hodnot.</span><span class="sxs-lookup"><span data-stu-id="5488b-106">In Microsoft Dynamics 365 for Finance and Operations, many fields have lookups that can help you easily find the correct or desired value.</span></span> <span data-ttu-id="5488b-107">Vyhledávání bylo několika způsoby vylepšeno – ovládací prvky jsou nyní užitečnější a uživatelé díky nim mohou být produktivnější.</span><span class="sxs-lookup"><span data-stu-id="5488b-107">Several enhancements have been added to lookups that make these controls more usable and make users more productive.</span></span> <span data-ttu-id="5488b-108">V tomto tématu se dozvíte o těchto nových funkcích a užitečných tipech k optimálnímu využití vyhledávání v systému.</span><span class="sxs-lookup"><span data-stu-id="5488b-108">In this topic, you will learn about these new lookup features and will receive some helpful tips to get the optimal use out of lookups in the system.</span></span>  

<a name="responsive-lookups"></a><span data-ttu-id="5488b-109">Lépe reagující vyhledávání</span><span class="sxs-lookup"><span data-stu-id="5488b-109">Responsive lookups</span></span>
------------------

<span data-ttu-id="5488b-110">V předchozích verzích aplikace Finance and Operations museli uživatelé při práci s ovládacími prvky vyhledávání provádět explicitní úkony, aby se otevřela rozevírací nabídka.</span><span class="sxs-lookup"><span data-stu-id="5488b-110">In previous versions of Finance and Operations, when interacting with a lookup control, a user would have to take an explicit action to open the drop-down menu.</span></span> <span data-ttu-id="5488b-111">K těmto úkonům patří zadání hvězdičky (\*) k filtrování podle aktuální hodnoty ovládacího prvku, kliknutí na tlačítko rozevíracího seznamu nebo použití klávesové zkratky **Alt**+**Šipka dolů**.</span><span class="sxs-lookup"><span data-stu-id="5488b-111">This may have been by typing an asterisk (\*) in the control to filter the lookup based on the current value of the control, clicking the drop-down button, or by using the **Alt**+**Down arrow** keyboard shortcut.</span></span> <span data-ttu-id="5488b-112">Ovládací prvky vyhledávání byly upraveny následujícími způsoby, aby lépe vyhovovaly současné praxi při používání webu:</span><span class="sxs-lookup"><span data-stu-id="5488b-112">Lookup controls have been modified in the following ways to better align with current web practices:</span></span>

-   <span data-ttu-id="5488b-113">Rozevírací nabídky vyhledávání se nyní automaticky otevírají po krátké pauze při zadávání a jejich obsah se filtruje podle aktuální hodnoty vyhledávacího ovládacího prvku.</span><span class="sxs-lookup"><span data-stu-id="5488b-113">Lookup drop-down menus will now open automatically after a slight pause in typing, with the drop-down menu contents filtered based on the lookup control's value.</span></span>
    -   <span data-ttu-id="5488b-114">Původní chování – automatické otevření rozevíracího seznamu po zadání hvězdičky (\*) – se již nepoužívá.</span><span class="sxs-lookup"><span data-stu-id="5488b-114">Note that the old behavior of automatic opening of the dropdown after typing an asterisk (\*) has been deprecated.</span></span>
-   <span data-ttu-id="5488b-115">Po otevření rozevírací nabídky vyhledávání se stane toto:</span><span class="sxs-lookup"><span data-stu-id="5488b-115">After the lookup drop-down menu has opened, the following will occur:</span></span>
    -   <span data-ttu-id="5488b-116">Kurzor zůstane ve vyhledávacím ovládacím prvku (místo přesunutí do rozevírací nabídky), abyste mohli hodnotu ovládacího prvku dále upravovat.</span><span class="sxs-lookup"><span data-stu-id="5488b-116">The cursor will stay in the lookup control (instead of focus moving into the drop-down menu) so you can continue to make modifications to the control's value.</span></span> <span data-ttu-id="5488b-117">Uživatel však stále může pomocí kláves **Šipka nahoru** a **Šipka dolů** měnit řádky v rozevírací nabídce a vybírat aktuální řádky klávesou Enter.</span><span class="sxs-lookup"><span data-stu-id="5488b-117">However, the user can still use the **Up arrow** and **Down arrow** to change rows in the drop-down menu, and enter to select the current row in the drop-down menu.</span></span>
    -   <span data-ttu-id="5488b-118">Obsah rozevírací nabídky bude reagovat na jakoukoli změnu hodnoty vyhledávacího ovládacího prvku.</span><span class="sxs-lookup"><span data-stu-id="5488b-118">The contents of the drop-down menu will adjust after any modifications are made to the lookup control's value.</span></span>

<span data-ttu-id="5488b-119">Jak příklad si uveďme vyhledávací pole s názvem **Město**.</span><span class="sxs-lookup"><span data-stu-id="5488b-119">For example, consider a lookup field called **City**.</span></span> 

<span data-ttu-id="5488b-120">Pokud je výběr nastaven na pole **Město**, můžete začít hledat požadované město zadáním několika písmen, například „col“.</span><span class="sxs-lookup"><span data-stu-id="5488b-120">When focus is in the **City** field, you can start looking for the city that you want by typing a few letters, like "col."</span></span>  <span data-ttu-id="5488b-121">Jakmile přestanete psát, vyhledávání se automaticky otevře a zobrazí města začínající na „col“.</span><span class="sxs-lookup"><span data-stu-id="5488b-121">After you stop typing, the lookup will open automatically, filtered to those cities that begin with "col".</span></span> 

<span data-ttu-id="5488b-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span><span class="sxs-lookup"><span data-stu-id="5488b-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span></span> 

<span data-ttu-id="5488b-123">V tomto okamžiku je kurzor stále ve vyhledávacím poli.</span><span class="sxs-lookup"><span data-stu-id="5488b-123">At this point, the cursor is still in the lookup field.</span></span> <span data-ttu-id="5488b-124">Pokud budete pokračovat v psaní a zadáte hodnotu „colum“, obsahu vyhledávání se tomuto zadání automaticky přizpůsobí.</span><span class="sxs-lookup"><span data-stu-id="5488b-124">If you continue typing so the value is "colum," the lookup contents adjust automatically to reflect the latest value in the control.</span></span> 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

<span data-ttu-id="5488b-126">I když je stále vybrán vyhledávací ovládací prvek, můžete pomocí kláves **Šipka nahoru** a **Šipka dolů** vybírat požadované řádky.</span><span class="sxs-lookup"><span data-stu-id="5488b-126">Even though focus is still in the lookup control, you can also use the **Up arrow** or **Down arrow** keys to highlight the row that you want to select.</span></span> <span data-ttu-id="5488b-127">Pokud stisknete klávesu **Enter**, zvýrazněný řádek se ve vyhledávání vybere a hodnota ovládacího prvku se aktualizuje.</span><span class="sxs-lookup"><span data-stu-id="5488b-127">If you press **Enter** the highlighted row will be selected from the lookup and the control's value will be updated.</span></span> 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a><span data-ttu-id="5488b-129">Zadání dalších údajů kromě ID</span><span class="sxs-lookup"><span data-stu-id="5488b-129">Typing in more than IDs</span></span>
<span data-ttu-id="5488b-130">Při zadávání dat se uživatelé přirozeně snaží určit entity (například odběratele nebo dodavatele) pomocí názvu, nikoli identifikátorů, které tyto entity zastupují.</span><span class="sxs-lookup"><span data-stu-id="5488b-130">When entering data, it's natural for users to attempt to identify an entity, such as a customer or vendor, in terms of the name rather than an identifier representing the entity.</span></span> <span data-ttu-id="5488b-131">V aktuální verzi aplikace Finance and Operations je nyní u mnoha (ale ne všech) funkcí vyhledávání možné kontextové zadávání dat.</span><span class="sxs-lookup"><span data-stu-id="5488b-131">In the current version of Finance and Operations, many (but not all) lookups now allow contextual data entry.</span></span> <span data-ttu-id="5488b-132">Díky této užitečné funkci může uživatel vyhledávat pomocí ID nebo odpovídajícího názvu.</span><span class="sxs-lookup"><span data-stu-id="5488b-132">This powerful feature allows the user to type the ID or the corresponding name into the lookup control.</span></span> 

<span data-ttu-id="5488b-133">Příkladem je pole **Účet odběratele** při vytváření prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="5488b-133">For example, consider the **Customer account** field when creating a sales order.</span></span> <span data-ttu-id="5488b-134">V tomto poli se zobrazuje **ID účtu** odběratele, ale uživatelé při tvorbě prodejních objednávek zadávají spíše **název účtu** než **ID účtu**, například „Forest Wholesales“ místo „US-003“.</span><span class="sxs-lookup"><span data-stu-id="5488b-134">This field shows the **Account ID** for the customer, but a user would typically prefer to enter an **Account name** instead of an **Account ID** for this field when creating a sales order, such as "Forest Wholesales" instead of "US-003."</span></span>

<span data-ttu-id="5488b-135">Pokud uživatel začne do vyhledávacího ovládacího prvku zadávat **ID účtu**, rozevírací nabídka se automaticky otevře (podle popisu v předchozí části) a vyhledávání se zobrazí jako níže.</span><span class="sxs-lookup"><span data-stu-id="5488b-135">If the user started to enter an **Account ID** into the lookup control, the drop-down menu would automatically open as described in the previous section and the user would see the lookup as shown below.</span></span>

<span data-ttu-id="5488b-136">[![Kontextové vyhledávání při zadání ID účtu odběratele](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="5488b-136">[![Contextual lookup when a customer account ID is entered](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span>

<span data-ttu-id="5488b-137">Uživatel však může zadat také začátek **názvu účtu**.</span><span class="sxs-lookup"><span data-stu-id="5488b-137">However, the user can also now enter the beginning of an **Account name** as well.</span></span> <span data-ttu-id="5488b-138">Pokud to udělá, zobrazí se následující vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5488b-138">If this is detected, then the user will see the following lookup.</span></span> <span data-ttu-id="5488b-139">Všimněte si, že sloupec **Název** se ve vyhledávání přesunul na první místo a že celé vyhledávání je seřazeno a filtrováno podle sloupce **Název**.</span><span class="sxs-lookup"><span data-stu-id="5488b-139">Notice how the **Name** column is moved to be the first column in the lookup, and how the lookup is sorted and filtered based on the **Name** column.</span></span>

<span data-ttu-id="5488b-140">[![Kontextové vyhledávání při zadání jména odběratele](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span><span class="sxs-lookup"><span data-stu-id="5488b-140">[![Contextual lookup when a customer name is entered](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span></span>

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a><span data-ttu-id="5488b-141">Rozšířené filtrování a řazení pomocí záhlaví sloupců mřížky</span><span class="sxs-lookup"><span data-stu-id="5488b-141">Using grid column headers for more advanced filtering and sorting</span></span>
<span data-ttu-id="5488b-142">Vylepšení vyhledávání popsaná v předchozích dvou částech značně zlepšují možnosti procházení řádků při vyhledávání typu „začíná na“, které se týká polí **ID** nebo **Název**.</span><span class="sxs-lookup"><span data-stu-id="5488b-142">The lookup enhancements discussed in the previous two sections greatly improve a user's ability to navigate the rows in a lookup based on a "begins with" search of the **ID** or **Name** field in the lookup.</span></span> <span data-ttu-id="5488b-143">Existují však situace, ve kterých je k nalezení správného řádku nutné použít pokročilejší filtrování nebo řazení.</span><span class="sxs-lookup"><span data-stu-id="5488b-143">However, there are situations in which more advanced filtering (or sorting) is needed to find the correct row.</span></span> <span data-ttu-id="5488b-144">V těchto případech musí uživatel použít možnosti filtrování a řazení v záhlavích sloupců mřížky vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5488b-144">In these situations, the user needs to use the filtering and sorting options in the grid column headers inside the lookup.</span></span> <span data-ttu-id="5488b-145">Jako příklad si uvedeme zaměstnance, který zadává řádek prodejní objednávky a potřebuje jako produkt najít správnou položku typu „cable“ (kabel).</span><span class="sxs-lookup"><span data-stu-id="5488b-145">For example, consider an employee entering a sales order line who needs to locate the right "cable" as the product.</span></span> <span data-ttu-id="5488b-146">Pokud do pole **Číslo položky** zadá „cable“, správnou položku nenajde, protože žádné názvy produktů začínající na „cable“ neexistují.</span><span class="sxs-lookup"><span data-stu-id="5488b-146">Typing "cable" into the **Item number** control isn't helpful, as there are no product names that begin with "cable."</span></span> 

![emptyitemlookup](./media/emptyitemlookup.png) 

<span data-ttu-id="5488b-148">Místo toho je třeba hodnotu ovládacího prvku vyhledávání vymazat, otevřít rozevírací nabídku vyhledávání a filtrovat ji pomocí záhlaví sloupce mřížky, jak je uvedeno níže.</span><span class="sxs-lookup"><span data-stu-id="5488b-148">Instead, the user needs to clear the value of the lookup control, open the lookup drop-down menu, and filter the drop-down menu using the grid column header, as shown below.</span></span> <span data-ttu-id="5488b-149">Možnosti filtrování a řazení lze zobrazit jednoduchým kliknutím (nebo klepnutím) na požadované záhlaví sloupce.</span><span class="sxs-lookup"><span data-stu-id="5488b-149">A mouse (or touch) user can simply click (or touch) any column header to access the filtering and sorting options for that column.</span></span> <span data-ttu-id="5488b-150">Na klávesnici stačí stisknout podruhé zkratku **Alt**+**Šipka** **dolů** a přesunout tak výběr do rozevírací nabídky. Potom lze pomocí tabulátoru vybrat správný sloupec a stisknutím klávesové zkratky **Ctrl**+**G** otevřít rozevírací nabídku záhlaví sloupce mřížky.</span><span class="sxs-lookup"><span data-stu-id="5488b-150">For a keyboard user, the user simply needs to press **Alt**+**Down** **arrow** a second time to move focus into the drop-down menu, after which the user can tab to the correct column, and then press **Ctrl**+**G** to open the grid column header drop-down menu.</span></span> 

<span data-ttu-id="5488b-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span><span class="sxs-lookup"><span data-stu-id="5488b-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span></span> 

<span data-ttu-id="5488b-152">Po použití filtru (viz následující obrázek) může uživatel najít a vybrat řádek jako obvykle.</span><span class="sxs-lookup"><span data-stu-id="5488b-152">After the filter has been applied (see the image below), the user can find and select the row as usual.</span></span> 

![filtereditemlookup](./media/filtereditemlookup.png)





---
title: Úprava průvodců a šablon zaškolení v aplikaci Dynamics 365 Talent - Onboard
description: V tomto tématu je vysvětleno, jak přidat aktivity a další informace do průvodců a šablon zaškolení v aplikaci Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897113"
---
# <a name="edit-onboarding-guides-and-templates"></a><span data-ttu-id="a1d91-103">Úprava průvodců a šablon zaškolení</span><span class="sxs-lookup"><span data-stu-id="a1d91-103">Edit onboarding guides and templates</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a1d91-104">Po vytvoření průvodce nebo šablony zaškolení v aplikaci Microsoft Dynamics 365 Talent: Onboard je nutné přidat úvod, aktivity, kontakty a zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1d91-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="a1d91-105">Onboard umožňuje zahrnout do průvodců zaškolením bohatý obsah včetně následujících možností:</span><span class="sxs-lookup"><span data-stu-id="a1d91-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="a1d91-106">Videa na YouTube</span><span class="sxs-lookup"><span data-stu-id="a1d91-106">YouTube videos</span></span>
- <span data-ttu-id="a1d91-107">Prezentace Microsoft Sway</span><span class="sxs-lookup"><span data-stu-id="a1d91-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="a1d91-108">Aplikace Microsoft PowerApps</span><span class="sxs-lookup"><span data-stu-id="a1d91-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="a1d91-109">Videa na Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="a1d91-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="a1d91-110">Formuláře Microsoft Forms</span><span class="sxs-lookup"><span data-stu-id="a1d91-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="a1d91-111">Prvky IFrame, které obsahují webový obsah</span><span class="sxs-lookup"><span data-stu-id="a1d91-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="a1d91-112">Úprava úvodů nebo aktivit importovaných ze šablony</span><span class="sxs-lookup"><span data-stu-id="a1d91-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="a1d91-113">Pokud vytvoříte průvodce zaškolením ze šablony nebo pokud importujete aktivity z jedné šablony do druhé, zobrazí se u importovaných aktivit tlačítko **zámku**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="a1d91-114">Označují se jako *spravované aktivity*.</span><span class="sxs-lookup"><span data-stu-id="a1d91-114">These are called *managed activities*.</span></span>

<span data-ttu-id="a1d91-115">[![Spravované aktivity](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="a1d91-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="a1d91-116">Když vyberete spravovanou aktivitu, uvidíte v její horní části zdrojovou šablonu.</span><span class="sxs-lookup"><span data-stu-id="a1d91-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="a1d91-117">[![Zdroj spravované aktivity](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="a1d91-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="a1d91-118">Když upravíte aktivitu v šabloně, Onboard populuje změny do všech šablon a neodeslaných průvodců založených na dané šabloně.</span><span class="sxs-lookup"><span data-stu-id="a1d91-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="a1d91-119">Pokud vyberete neodeslaného průvodce na základě upravené šablony a poté vyberete kartu **Aktivity** v průvodci, zobrazí se upozornění, že se průvodce změnil.</span><span class="sxs-lookup"><span data-stu-id="a1d91-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="a1d91-120">Chcete-li oznámení zrušit, vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="a1d91-121">[![Oznámení o změně](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="a1d91-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="a1d91-122">Vedle aktualizovaných aktivit se zobrazí černá tečka.</span><span class="sxs-lookup"><span data-stu-id="a1d91-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="a1d91-123">[![Změněná aktivita](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="a1d91-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="a1d91-124">Spravované aktivity nelze upravovat mimo původní šablonu, s výjimkou přidání nabyvatele, data splatnosti nebo jiných informací do pravé části aktivity.</span><span class="sxs-lookup"><span data-stu-id="a1d91-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="a1d91-125">Chcete-li upravit spravovanou aktivitu nebo nechcete, aby aktivita přijímala aktualizace z šablony, ze které pochází, vyberte pro danou aktivitu tlačítko **zámku**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="a1d91-126">Tlačítko **zámku** zmizí.</span><span class="sxs-lookup"><span data-stu-id="a1d91-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="a1d91-127">Tato aktivita již nebude spravována původní šablonou a nebude již moci získávat aktualizace z této šablony.</span><span class="sxs-lookup"><span data-stu-id="a1d91-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="a1d91-128">Aktualizace provedené v aktivitě nemají vliv na původní šablonu.</span><span class="sxs-lookup"><span data-stu-id="a1d91-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="a1d91-129">Odstraníte-li aktivitu z průvodce a provedete změny ze šablony tohoto průvoce, aktivita zůstane v průvodci odstraněná.</span><span class="sxs-lookup"><span data-stu-id="a1d91-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="a1d91-130">Kontakty a zdroje nejsou spravovány šablonami.</span><span class="sxs-lookup"><span data-stu-id="a1d91-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="a1d91-131">Kromě toho nejsou tyto oddíly spravovány, takže pokud přidáte nebo upravíte oddíl v šabloně, změny nebudou vloženy do žádných průvodců nebo šablon, které tuto šablonu používají.</span><span class="sxs-lookup"><span data-stu-id="a1d91-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="a1d91-132">Přidáte-li do šablony nové aktivity, budou nové aktivity přesunuty do průvodců a šablon na základě této šablony a nové aktivity se zobrazí nahoře.</span><span class="sxs-lookup"><span data-stu-id="a1d91-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="a1d91-133">Import aktivit z jiné šablony</span><span class="sxs-lookup"><span data-stu-id="a1d91-133">Import activities from another template</span></span>

<span data-ttu-id="a1d91-134">Do průvoce nebo šablony můžete importovat aktivity z jedné nebo více šablon.</span><span class="sxs-lookup"><span data-stu-id="a1d91-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="a1d91-135">Vyberte průvodce nebo šablonu, které chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="a1d91-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="a1d91-136">Vyberte karu **Aktivity**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="a1d91-137">V části vpravo vyberte kartu **Import**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="a1d91-138">[![Aktivity importu](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="a1d91-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="a1d91-139">Chcete-li zobrazit náhled úkolů na nové kartě v prohlížeči, vyberte tlačítko **Otevřít na nové kartě** v libovolné šabloně.</span><span class="sxs-lookup"><span data-stu-id="a1d91-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="a1d91-140">[![Import aktivit](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="a1d91-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="a1d91-141">Požadovanou šablonu přetáhněte na místo v šabloně průvodce, kde se mají zobrazovat aktivity.</span><span class="sxs-lookup"><span data-stu-id="a1d91-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="a1d91-142">Pokračujte v úpravách příručky nebo šablony.</span><span class="sxs-lookup"><span data-stu-id="a1d91-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="a1d91-143">Importované aktivity budou obsahovat tlačítko **zámku**, které označuje, že tyto aktivity jsou spravovány šablonou, ze které jste importovali.</span><span class="sxs-lookup"><span data-stu-id="a1d91-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="a1d91-144">Po provedení změn importované šablony se tyto aktivity aktualizují v šabloně, do které byly importovány.</span><span class="sxs-lookup"><span data-stu-id="a1d91-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="a1d91-145">Změny však nebudou automaticky vloženy do žádných průvodců vytvořených ze šablony, do které jste importovali data.</span><span class="sxs-lookup"><span data-stu-id="a1d91-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="a1d91-146">Zadání změn ze šablony do jiných šablon nebo průvodců</span><span class="sxs-lookup"><span data-stu-id="a1d91-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="a1d91-147">Pokud upravíte šablonu, která obsahuje aktivity používané v jiných šablonách nebo průvodcích, musíte tyto změny použít, pokud je chcete zobrazit v jiných šablonách nebo průvodcích.</span><span class="sxs-lookup"><span data-stu-id="a1d91-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="a1d91-148">Pokud si nejste jisti, zda jsou aktivity šablony použity v jiných šablonách nebo průvodcích, vyberte kartu **Použito na** k zobrazení, kde se tyto aktivity zobrazují.</span><span class="sxs-lookup"><span data-stu-id="a1d91-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="a1d91-149">[![Zobrazení, kde se používají průvodci a šablony](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="a1d91-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="a1d91-150">Postup použití změn:</span><span class="sxs-lookup"><span data-stu-id="a1d91-150">To push your changes:</span></span>

1. <span data-ttu-id="a1d91-151">Uložte změny výběrem tlačítka **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="a1d91-152">Pokud tak neučiníte, budete vyzváni k uložení změn v následujícím kroku.</span><span class="sxs-lookup"><span data-stu-id="a1d91-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="a1d91-153">Vyberte **Použít tyto změny**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="a1d91-154">Přidání nebo úprava úvodu</span><span class="sxs-lookup"><span data-stu-id="a1d91-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="a1d91-155">Na kartě **Úvod** zadejte název průvodce a otevřenou zprávu.</span><span class="sxs-lookup"><span data-stu-id="a1d91-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="a1d91-156">Chcete-li použít vzorový text, vyberte **Použít tuto zprávu**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="a1d91-157">[![Karta Úvod v šabloně zaškolení](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="a1d91-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="a1d91-158">Pomocí tlačítek pro formátování můžete vyvolat text podle potřeby nebo přidat obrázky nebo odkazy.</span><span class="sxs-lookup"><span data-stu-id="a1d91-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="a1d91-159">Práci uložte výběrem možnosti **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="a1d91-160">Přidání nebo úprava aktivit</span><span class="sxs-lookup"><span data-stu-id="a1d91-160">Add or edit activities</span></span>

1. <span data-ttu-id="a1d91-161">Na kartě **Aktivity** přetáhněte položky z pravé části do oblasti pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="a1d91-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="a1d91-162">Chcete-li průvodce uspořádat do oddílů, přetáhněte položku **Nový oddíl** do oblasti pro úpravy a zadejte název a volitelný popis oddílu.</span><span class="sxs-lookup"><span data-stu-id="a1d91-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="a1d91-163">Přidání nové sekce do průvodce zaškolením nebo šablony</span><span class="sxs-lookup"><span data-stu-id="a1d91-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="a1d91-164">Chcete-li přidat aktivity pro nově přijatého zaměstnance k dokončení, přetáhněte položku **Nová aktivita** do oblasti pro úpravy a zadejte název a popis aktivity.</span><span class="sxs-lookup"><span data-stu-id="a1d91-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="a1d91-165">Přidání nové aktivity do průvodce zaškolením nebo šablony</span><span class="sxs-lookup"><span data-stu-id="a1d91-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="a1d91-166">Přidání bohatého obsahu do průvodce zaškolením:</span><span class="sxs-lookup"><span data-stu-id="a1d91-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="a1d91-167">Chcete-li přidat video YouTube, přetáhněte položku **YouTube** do oblasti pro úpravy, zadejte název a popis aktivity a zadejte adresu URL videa na YouTube.</span><span class="sxs-lookup"><span data-stu-id="a1d91-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="a1d91-168">Chcete-li přidat prezentaci Sway nebo zpravodaj, přetáhněte položku **Sway** do oblasti pro úpravy, zadejte název a popis aktivity a zadejte vloženou adresu URL pro prezentaci Sway nebo zpravodaj.</span><span class="sxs-lookup"><span data-stu-id="a1d91-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="a1d91-169">Chcete-li přidat aplikaci Microsoft Power Apps, přetáhněte položku **Power Apps** do oblasti pro úpravy, zadejte název a popis aktivity a vyberte aplikaci Power Apps nebo zadejte ID aplikace Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a1d91-169">To add a Microsoft Power Apps app, drag the **Power Apps** item to the editing area, enter a name and description for the activity, and either select the Power Apps app or enter the Power Apps app ID.</span></span>
    - <span data-ttu-id="a1d91-170">Chcete-li přidat video Microsoft Stream, přetáhněte položku **Microsoft Stream** do oblasti pro úpravy, zadejte název a popis aktivity a zadejte adresu URL videa na Microsoft Stream.</span><span class="sxs-lookup"><span data-stu-id="a1d91-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="a1d91-171">Chcete-li přidat formulář Microsoft Forms, přetáhněte položku **Microsoft Forms** do oblasti pro úpravy, zadejte název a popis aktivity, zadejte adresu URL formuláře Microsoft Forms a určete velikost oblasti obrazovky.</span><span class="sxs-lookup"><span data-stu-id="a1d91-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="a1d91-172">Chcete-li přidat iframe obsahující webový obsah, přetáhněte položku **Webový obsah (iframe)** do oblasti pro úpravy, zadejte název a popis aktivity, zadejte adresu URL webového obsahu a určete velikost oblasti obrazovky.</span><span class="sxs-lookup"><span data-stu-id="a1d91-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="a1d91-173">Přidání bohatého obsahu do průvodce zaškolením nebo šablony</span><span class="sxs-lookup"><span data-stu-id="a1d91-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="a1d91-174">Volitelné: v oblasti napravo od každé aktivity přiřaďte tuto aktivitu konkrétní osobě nebo roli, přidejte datum splatnosti a kontaktní osobu a přiřaďte barvu kategorie.</span><span class="sxs-lookup"><span data-stu-id="a1d91-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="a1d91-175">Když přiřadíte aktivitu osobě nebo roli, bude úkol vytvořen pro každou jednotlivou osobu.</span><span class="sxs-lookup"><span data-stu-id="a1d91-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="a1d91-176">Tento úkol se zobrazí v nabídce **Úkoly** v aplikaci Onboard.</span><span class="sxs-lookup"><span data-stu-id="a1d91-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="a1d91-177">[![Přiřazení aktivity v průvodci nebo šabloně zaškolení](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="a1d91-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="a1d91-178">Práci uložte výběrem možnosti **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="a1d91-179">Chcete-li odstranit aktivitu nebo oddíl, vyberte tlačítko **Odstranit** (symbol odpadkového koše) v pravém horním rohu aktivity nebo oddílu.</span><span class="sxs-lookup"><span data-stu-id="a1d91-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="a1d91-180">Chcete-li změnit pořadí aktivit a oddílů, přetáhněte je do nového umístění.</span><span class="sxs-lookup"><span data-stu-id="a1d91-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="a1d91-181">Přidání nebo úprava kontaktů</span><span class="sxs-lookup"><span data-stu-id="a1d91-181">Add or edit contacts</span></span>

<span data-ttu-id="a1d91-182">Můžete přidat kontaktní osobu, která může nově přijatému zaměstnanci dosahovat úspěchů od prvního dne.</span><span class="sxs-lookup"><span data-stu-id="a1d91-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="a1d91-183">Těmito kontakty mohou být náboroví pracovníci, kolegové z týmu, kamarádi při zaškolení, mentoři, správci a zaměstnanci podpory IT.</span><span class="sxs-lookup"><span data-stu-id="a1d91-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="a1d91-184">Na kartě **Kontakty** vyberte možnost **Nový kontakt**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="a1d91-185">V dialogovém okně **Přidat člena týmu** zadejte jméno nebo e-mailovou adresu kontaktní osoby, zadejte krátký popis, který vysvětluje, jakým způsobem může kontaktní osoba pomoci nově přijatému zaměstnanci a poté vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="a1d91-186">Přidání kontaktů do průvodce zaškolením nebo šablony</span><span class="sxs-lookup"><span data-stu-id="a1d91-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="a1d91-187">Případně můžete vybrat jeden nebo více kontaktů v nabídce **Návrhy.**</span><span class="sxs-lookup"><span data-stu-id="a1d91-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="a1d91-188">Práci uložte výběrem možnosti **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="a1d91-189">Chcete-li odstranit kontakt, vyberte tlačítko **Odstranit** (symbol odpadkového koše) napravo od kontaktu.</span><span class="sxs-lookup"><span data-stu-id="a1d91-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="a1d91-190">Chcete-li upravit kontakt, vyberte tlačítko **Upravit** (symbol pera) napravo od kontaktu.</span><span class="sxs-lookup"><span data-stu-id="a1d91-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="a1d91-191">Přidání nebo úprava zdrojů</span><span class="sxs-lookup"><span data-stu-id="a1d91-191">Add or edit resources</span></span>

<span data-ttu-id="a1d91-192">V rámci vlastního průvodce zaškolením můžete přidat užitečné soubory, mapy a odkazy do části **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="a1d91-193">Na kartě **Zdroje** vyberte možnost **Nový zdroj**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="a1d91-194">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="a1d91-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="a1d91-195">Chcete-li přidat soubor, vyberte kartu **Soubor** a přetáhněte jej do vymezené oblasti.</span><span class="sxs-lookup"><span data-stu-id="a1d91-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="a1d91-196">(Případně můžete kliknout na libovolné místo v této oblasti a vyhledat soubor v počítači nebo vybrat možnost **Procházet OneDrive**.) Zadejte název souboru a poté klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="a1d91-197">Pokud chcete přidat odkaz, vyberte kartu **Odkaz**, zadejte název a adresu odkazu a vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="a1d91-198">Pokud chcete přidat mapu, vyberte kartu **Mapa**, zadejte název a adresu mapy a vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="a1d91-199">Onboard bude obsahovat mapu zadané adresy.</span><span class="sxs-lookup"><span data-stu-id="a1d91-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="a1d91-200">Přidání prostředku do průvodce zaškolením nebo šablony</span><span class="sxs-lookup"><span data-stu-id="a1d91-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="a1d91-201">Práci uložte výběrem možnosti **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a1d91-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="a1d91-202">Chcete-li odstranit zdroj, vyberte tlačítko **Odstranit** (symbol odpadkového koše) napravo od zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1d91-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="a1d91-203">Chcete-li upravit zdroj, vyberte tlačítko **Upravit** (symbol pera) napravo od zdroje.</span><span class="sxs-lookup"><span data-stu-id="a1d91-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a1d91-204">Další kroky</span><span class="sxs-lookup"><span data-stu-id="a1d91-204">Next steps</span></span>

- [<span data-ttu-id="a1d91-205">Sdílení obsahu s jinými přispěvateli</span><span class="sxs-lookup"><span data-stu-id="a1d91-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="a1d91-206">Zobrazit stav úkolů a zaškolení zaměstnanců</span><span class="sxs-lookup"><span data-stu-id="a1d91-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="a1d91-207">Vytvořit náborové týmy v Onboard</span><span class="sxs-lookup"><span data-stu-id="a1d91-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="a1d91-208">Viz také</span><span class="sxs-lookup"><span data-stu-id="a1d91-208">See also</span></span>

- [<span data-ttu-id="a1d91-209">Vyzkoušejte nebo kupte aplikaci Onboard</span><span class="sxs-lookup"><span data-stu-id="a1d91-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="a1d91-210">Co je nového a co se změnilo v aplikaci Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="a1d91-210">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="a1d91-211">Plány vydání</span><span class="sxs-lookup"><span data-stu-id="a1d91-211">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="a1d91-212">Získání podpory pro Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="a1d91-212">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)

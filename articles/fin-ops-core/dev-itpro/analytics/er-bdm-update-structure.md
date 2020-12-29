---
title: Aktualizace struktury šablony obchodního dokumentu
description: Toto téma vysvětluje, jak aktualizovat strukturu šablony obchodního dokumentu pomocí funkce správy obchodních dokumentů.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: fd279b28c43e22bec6bf814845fe97828bc96d81
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681321"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="fb804-103">Aktualizace struktury šablony obchodního dokumentu</span><span class="sxs-lookup"><span data-stu-id="fb804-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fb804-104">V podokně **Struktura šablony** editoru šablon [správy obchodních dokumentů](er-business-document-management.md) můžete upravit šablonu obchodního dokumentu [přidáváním nových polí](er-bdm-add-field-to-excel-template.md) do šablony v aplikaci Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fb804-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="fb804-105">Struktura šablony je poté automaticky aktualizována v Dynamics 365 Finance, takže odráží změny, které jste provedli v podokně **Struktura šablony**.</span><span class="sxs-lookup"><span data-stu-id="fb804-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="fb804-106">Šablonu můžete také upravit pomocí online funkcí aplikací Office 365.</span><span class="sxs-lookup"><span data-stu-id="fb804-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="fb804-107">Do upravitelného listu můžete například přidat novou pojmenovanou položku, jakou je obrázek nebo tvar.</span><span class="sxs-lookup"><span data-stu-id="fb804-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="fb804-108">V tomto případě se struktura šablony v aplikaci Finance automaticky neaktualizuje a položka, kterou jste přidali, se nezobrazí v podokně **Struktura šablony**.</span><span class="sxs-lookup"><span data-stu-id="fb804-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="fb804-109">Aktualizujte strukturu šablony ručně v aplikaci Finance výběrem příkazu **Aktualizovat strukturu** na stránce editoru šablon.</span><span class="sxs-lookup"><span data-stu-id="fb804-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="fb804-110">Chcete-li získat další informace o této funkci, dokončete následující příklad.</span><span class="sxs-lookup"><span data-stu-id="fb804-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="fb804-111">Příklad: Aktualizace struktury šablony obchodního dokumentu</span><span class="sxs-lookup"><span data-stu-id="fb804-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="fb804-112">Tento příklad ukazuje, jak může správce systému aktualizovat strukturu šablony obchodního dokumentu v aplikaci Finance po úpravě šablony v aplikaci Office Online.</span><span class="sxs-lookup"><span data-stu-id="fb804-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="fb804-113">V následujících částech jsou vysvětleny příslušné kroky.</span><span class="sxs-lookup"><span data-stu-id="fb804-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="fb804-114">Připravte šablonu obchodního dokumentu k úpravám</span><span class="sxs-lookup"><span data-stu-id="fb804-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="fb804-115">Proveďte následující procedury v části [Přehled správy obchodních dokumentů](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="fb804-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="fb804-116">Konfigurace parametrů ER</span><span class="sxs-lookup"><span data-stu-id="fb804-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="fb804-117">Import řešení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="fb804-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="fb804-118">Povolení správy obchodních dokumentů</span><span class="sxs-lookup"><span data-stu-id="fb804-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="fb804-119">Konfigurace parametrů</span><span class="sxs-lookup"><span data-stu-id="fb804-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="fb804-120">Úprava šablony obchodního dokumentu</span><span class="sxs-lookup"><span data-stu-id="fb804-120">Edit a business document template</span></span>

1. <span data-ttu-id="fb804-121">V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.</span><span class="sxs-lookup"><span data-stu-id="fb804-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="fb804-122">Na stránce **Vytvořit novou šablonu** vyberte šablonu **Volná faktura (ukázka ER) (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="fb804-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="fb804-123">Vyberte příkaz **Vytvořit dokument**.</span><span class="sxs-lookup"><span data-stu-id="fb804-123">Select **Create document**.</span></span>
4. <span data-ttu-id="fb804-124">Do pole **Název** zadejte **FTI ukázka Litware**.</span><span class="sxs-lookup"><span data-stu-id="fb804-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="fb804-125">Výběrem **OK** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="fb804-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb804-126">Pokud jste se ještě nepřihlásili do Office Online, budete [přesměrováni na přihlašovací stránku Office 365](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page).</span><span class="sxs-lookup"><span data-stu-id="fb804-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page).</span></span> <span data-ttu-id="fb804-127">Chcete-li se vrátit do prostředí Finance, vyberte tlačítko **Zpět** v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="fb804-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="fb804-128">Nová šablona se otevře v režimu úprav ve vloženém ovládacím prvku Excel Online na stránce editoru šablon.</span><span class="sxs-lookup"><span data-stu-id="fb804-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="fb804-129">[![Použití pracovního prostoru pro správu obchodních dokumentů k úpravám šablony obchodního dokumentu](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="fb804-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="fb804-130">Kontrola aktuální struktury upravitelné šablony</span><span class="sxs-lookup"><span data-stu-id="fb804-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="fb804-131">V aplikaci Excel Online na kartě pásu karet **Zobrazit** vyberte ve skupině **Zobrazit** možnost **Mřížky**.</span><span class="sxs-lookup"><span data-stu-id="fb804-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="fb804-132">V upravitelné šabloně vyberte obdélník nad názvem šablony.</span><span class="sxs-lookup"><span data-stu-id="fb804-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="fb804-133">Tento obdélník tvoří obrázek s názvem **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="fb804-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="fb804-134">Pokud je skryté podokno **Struktura šablony**, vyberte příkaz **Zobrazit strukturu**.</span><span class="sxs-lookup"><span data-stu-id="fb804-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="fb804-135">V podokně **Struktura šablony** rozbalte položky **Zpráva \> Faktura \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="fb804-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="fb804-136">Všimněte si, že ve struktuře šablon ve Finance je položka **rptHeaderCompLogo** prezentována jako podřízená vůči položce **Zpráva \> Faktura \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="fb804-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="fb804-137">[![Použití pracovního prostoru pro správu obchodních dokumentů ke kontrole aktuální struktury upravitelné šablony](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="fb804-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="fb804-138">Aktualizace struktury šablony obchodního dokumentu odstraněním obrázku</span><span class="sxs-lookup"><span data-stu-id="fb804-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="fb804-139">V aplikaci Excel Online vyberte v upravitelné šabloně obrázek **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="fb804-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="fb804-140">Jedním z následujících kroků odstraňte vybraný obrázek z upravitelné šablony:</span><span class="sxs-lookup"><span data-stu-id="fb804-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="fb804-141">Stiskněte klávesu **Delete** na klávesnici.</span><span class="sxs-lookup"><span data-stu-id="fb804-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="fb804-142">Vyberte a podržte na obrázek (nebo na něm klikněte pravým tlačítkem) a poté vyberte možnost **Vyjmout**.</span><span class="sxs-lookup"><span data-stu-id="fb804-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb804-143">Položka **rptHeaderCompLogo** je aktuálně stále přítomná ve struktuře šablony v aplikaci Finance, přestože obrázek již není součástí šablony aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="fb804-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="fb804-144">Výběrem položky **Aktualizovat strukturu** synchronizujte strukturu upravitelné šablony v aplikacích Excel a Finance.</span><span class="sxs-lookup"><span data-stu-id="fb804-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="fb804-145">V podokně **Struktura šablony** rozbalte položky **Zpráva \> Faktura \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="fb804-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="fb804-146">Všimněte si, že položka **rptHeaderCompLogo** již není součástí struktury šablony v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="fb804-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="fb804-147">[![Použití pracovního prostoru pro správu obchodních dokumentů k odstranění obrázku z šablony obchodního dokumentu](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="fb804-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="fb804-148">Aktualizace struktury šablony obchodního dokumentu přidáním obrázku</span><span class="sxs-lookup"><span data-stu-id="fb804-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="fb804-149">V aplikaci Excel Online na kartě pásu karet **Vložit** vyberte ve skupině **Ilustrace** možnost **Obrázek**.</span><span class="sxs-lookup"><span data-stu-id="fb804-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="fb804-150">Zvolte možnost **Vybrat soubor**, přejděte k obrázku, který chcete přidat, vyberte jej a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb804-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="fb804-151">Vyberte možnost **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="fb804-151">Select **Insert**.</span></span>
4. <span data-ttu-id="fb804-152">Posunujte nový obrázek, dokud nebude na správném místě.</span><span class="sxs-lookup"><span data-stu-id="fb804-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="fb804-153">Ve výchozím nastavení Excel pojmenuje obrázek.</span><span class="sxs-lookup"><span data-stu-id="fb804-153">By default, Excel names the picture.</span></span> <span data-ttu-id="fb804-154">Obrázek může dostat třeba název **Obrázek 2**.</span><span class="sxs-lookup"><span data-stu-id="fb804-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="fb804-155">Výběrem položky **Aktualizovat strukturu** synchronizujte strukturu upravitelné šablony v aplikacích Excel a Finance.</span><span class="sxs-lookup"><span data-stu-id="fb804-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="fb804-156">V podokně **Struktura šablony** rozbalte položky **Zpráva \> Faktura \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="fb804-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="fb804-157">Všimněte si, že nový obrázek je nyní položkou struktury šablony v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="fb804-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="fb804-158">[![Použití pracovního prostoru pro správu obchodních dokumentů k přidání obrázku do šablony obchodního dokumentu](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="fb804-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="fb804-159">Související odkazy</span><span class="sxs-lookup"><span data-stu-id="fb804-159">Related links</span></span>

[<span data-ttu-id="fb804-160">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="fb804-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="fb804-161">Přehled správy obchodních dokumentů</span><span class="sxs-lookup"><span data-stu-id="fb804-161">Business document management overview</span></span>](er-business-document-management.md)

---
title: Přidání nových polí do šablony obchodního dokumentu v aplikaci Microsoft Excel
description: Toto téma obsahuje informace o tom, jak přidávat nová pole do šablony obchodního dokumentu v aplikaci Microsoft Excel pomocí funkce správy obchodních dokumentů.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 8c3a905c90f5dd4ad3487f004a958c0dcd52115d
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893240"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="7c902-103">Přidání nových polí do šablony obchodního dokumentu v aplikaci Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="7c902-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7c902-104">Můžete přidat nová pole do šablony, která se používá ke generování obchodních dokumentů ve formátu Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7c902-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="7c902-105">Tato pole lze přidat jako zástupné symboly, které se používají k vyplňování vygenerovaných dokumentů s požadovanými informacemi z aplikace.</span><span class="sxs-lookup"><span data-stu-id="7c902-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="7c902-106">U každého přidávaného pole můžete také určit vazbu na zdroje dat a určit, která data aplikace budou zadána do pole v případě, že šablona slouží ke generování obchodních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="7c902-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="7c902-107">Chcete-li získat další informace o této funkci, vyplňte příklad tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="7c902-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="7c902-108">Tento příklad ukazuje, jak aktualizovat šablonu tak, aby vyplnila pole ve vygenerovaných formulářích volných faktur.</span><span class="sxs-lookup"><span data-stu-id="7c902-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="7c902-109">Konfigurace správy obchodních dokumentů k úpravě šablon</span><span class="sxs-lookup"><span data-stu-id="7c902-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="7c902-110">Vzhledem k tomu, že je Správa obchodních dokumentů (BDM) sestavena na [přehledu elektronického výkaznictví](general-electronic-reporting.md), musíte před zahájením práce s BDM nakonfigurovat požadované parametry ER a BDM.</span><span class="sxs-lookup"><span data-stu-id="7c902-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="7c902-111">Přihlaste se k instanci aplikace Microsoft Dynamics 365 Finance jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="7c902-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="7c902-112">Proveďte následující kroky v příkladu v tématu [Přehled správy obchodních dokladů](er-business-document-management.md):</span><span class="sxs-lookup"><span data-stu-id="7c902-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="7c902-113">Proveďte konfiguraci parametrů ER.</span><span class="sxs-lookup"><span data-stu-id="7c902-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="7c902-114">Zapněte BDM.</span><span class="sxs-lookup"><span data-stu-id="7c902-114">Turn on BDM.</span></span>

<span data-ttu-id="7c902-115">Nyní můžete začít používat BDM pro úpravy šablon obchodních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="7c902-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="7c902-116">Import řešení ER obsahujících šablonu</span><span class="sxs-lookup"><span data-stu-id="7c902-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="7c902-117">Příklad v tomto postupu používá oficiálně publikované řešení ER.</span><span class="sxs-lookup"><span data-stu-id="7c902-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="7c902-118">Konfigurace ER je nutné importovat do aktuální instance modulu finance.</span><span class="sxs-lookup"><span data-stu-id="7c902-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="7c902-119">Konfigurace formátu ER **Volná textová faktura (Excel)** tohoto řešení obsahuje šablonu obchodního dokumentu ve formátu aplikace Excel, který lze upravovat pomocí BDM.</span><span class="sxs-lookup"><span data-stu-id="7c902-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="7c902-120">Importuje nejnovější verzi této konfigurace formátu ER ze služby Microsoft Dynamics Lifecycle Service (LCS).</span><span class="sxs-lookup"><span data-stu-id="7c902-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="7c902-121">Odpovídající datové modely ER a konfigurace mapování modelu ER budou importovány automaticky.</span><span class="sxs-lookup"><span data-stu-id="7c902-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="7c902-122">Další informace o tom, jak importovat konfigurace elektronického výkaznictví naleznete v tématu [Správa životního cyklu konfigurace elektronického výkaznictví](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="7c902-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Stránka Knihovna sdíleného majetku LCS](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="7c902-124">Úprava šablony řešení ER</span><span class="sxs-lookup"><span data-stu-id="7c902-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="7c902-125">Přihlaste se jako uživatel s přístupem do pracovního prostoru **Řízení obchodního dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="7c902-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="7c902-126">Otevřete pracovní prostor **Správa obchodních dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="7c902-126">Open the **Business document management** workspace.</span></span>

    ![Pracovní prostor správy obchodních dokumentů](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="7c902-128">V mřížce vyberte šablonu **Volná textová faktura (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="7c902-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="7c902-129">V pravém podokně vyberte možnost **Nová šablona** a vytvořte novou šablonu, která bude založena na vybrané šabloně.</span><span class="sxs-lookup"><span data-stu-id="7c902-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="7c902-130">Do pole **Název** zadejte **Volná textová faktura (Excel) Contoso** jako nadpis nové šablony.</span><span class="sxs-lookup"><span data-stu-id="7c902-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="7c902-131">Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.</span><span class="sxs-lookup"><span data-stu-id="7c902-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="7c902-132">Otevře se stránka Editor šablony BDM.</span><span class="sxs-lookup"><span data-stu-id="7c902-132">The BDM template editor page appears.</span></span> <span data-ttu-id="7c902-133">V rámci vloženého ovládacího prvku můžete použít Microsoft 365 pro úpravu vybrané šablony online.</span><span class="sxs-lookup"><span data-stu-id="7c902-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![Stránka Editor šablony BDM](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="7c902-135">Přidání popisku nového pole do šablony</span><span class="sxs-lookup"><span data-stu-id="7c902-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="7c902-136">Na stránce editor šablon BDM na pásu karet aplikace Excel zaškrtněte na kartě **Zobrazení** políčka **Záhlaví a mřížky** pro upravitelnou šablonu aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="7c902-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Zaškrtnutá políčka záhlaví a mřížky](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="7c902-138">Vyberte buňky **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="7c902-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="7c902-139">Na pásu karet aplikace Excel vyberte na kartě **Domů** položky **Sloučit a vycentrovat** ke sloučení vybraných buněk do nově sloučené buňky **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="7c902-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="7c902-140">Ve sloučené **buňce E8:F8** zadejte **adresu URL**.</span><span class="sxs-lookup"><span data-stu-id="7c902-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="7c902-141">Vyberte sloučenou buňku **E7:F7**, vyberte **Kopírovat formát**, pak vyberte sloučenou buňku **E8:F8**, chcete-li ji naformátovat stejným způsobem jako sloučená buňka **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="7c902-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Popisek nového pole přidaný do šablony](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="7c902-143">Formátování šablony do vyhrazení místa pro nové pole</span><span class="sxs-lookup"><span data-stu-id="7c902-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="7c902-144">Na stránce editor šablon BDM vyberte sloučenou buňku **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="7c902-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="7c902-145">Na pásu karet aplikace Excel vyberte na kartě **Domů** položky **Sloučit a vycentrovat** ke sloučení vybraných buněk do nově sloučené buňky **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="7c902-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="7c902-146">Vyberte sloučenou buňku **G7:H7**, vyberte **Kopírovat formát**, pak vyberte sloučenou buňku **G8:H8**, chcete-li ji naformátovat stejným způsobem jako sloučená buňka **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="7c902-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Místo rezervované pro nové pole](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="7c902-148">V poli **Název** vyberte **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="7c902-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="7c902-149">Rozsah **CompanyInfo** aktuální šablony aplikace Excel obsahuje všechna pole, která se používají k vyplnění záhlaví vygenerované sestavy informacemi o aktuální společnosti jako prodávající strany.</span><span class="sxs-lookup"><span data-stu-id="7c902-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![Vybraný rozsah CompanyInfo](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="7c902-151">Přidání nového pole do šablony</span><span class="sxs-lookup"><span data-stu-id="7c902-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="7c902-152">Na stránce **Editor šablon BDM** v podokně akcí vyberte **Zobrazit formát**.</span><span class="sxs-lookup"><span data-stu-id="7c902-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="7c902-153">V podokně **struktura šablony** vyberte možnost **přidat**.</span><span class="sxs-lookup"><span data-stu-id="7c902-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7c902-154">Je nutné upravit část šablony, kterou chcete použít jako nové pole.</span><span class="sxs-lookup"><span data-stu-id="7c902-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="7c902-155">Tuto úpravu jste již provedli formátováním sloučené buňky **G8: H8**.</span><span class="sxs-lookup"><span data-stu-id="7c902-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Přidání nového pole do šablony](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="7c902-157">Pokud chcete přidat nové pole jako buňku v šabloně, vyberte **Excel\Buňka**.</span><span class="sxs-lookup"><span data-stu-id="7c902-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="7c902-158">Chcete-li do šablony přidat nový rozsah, můžete vybrat **Excel\Rozsah**.</span><span class="sxs-lookup"><span data-stu-id="7c902-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="7c902-159">Zadaná oblast může obsahovat více buněk.</span><span class="sxs-lookup"><span data-stu-id="7c902-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="7c902-160">Tyto buňky můžete přidat později.</span><span class="sxs-lookup"><span data-stu-id="7c902-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="7c902-161">Všimněte si, že součást šablony **CompanyInfo** je automaticky vybrána v podokně **Struktura šablony**, protože se jedná o nejvíce vhodnou nadřazenou komponentu v aktuální struktuře šablon pro pole, které přidáváte.</span><span class="sxs-lookup"><span data-stu-id="7c902-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="7c902-162">Do pole **rozsah aplikace Excel** zadejte **CompanyURL_Value**.</span><span class="sxs-lookup"><span data-stu-id="7c902-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="7c902-163">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c902-163">Select **OK**.</span></span>

    ![Pole CompanyURL_Value přidané do struktury šablony](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="7c902-165">V podokně **Struktura šablony** vyberte tlačítko se třemi tečkami (...) a pak vyberte **Zobrazit vazby**.</span><span class="sxs-lookup"><span data-stu-id="7c902-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Zobrazit vybrané vazby](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="7c902-167">V podokně **struktura šablony** se nyní zobrazují zdroje dat, které jsou k dispozici ve formátu základního ER.</span><span class="sxs-lookup"><span data-stu-id="7c902-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="7c902-168">Vyberte **CompanyInfo_Value** jako pole, které chcete svázat se zdrojem dat podkladového formátu ER.</span><span class="sxs-lookup"><span data-stu-id="7c902-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="7c902-169">V části **Zdroje dat** podokna **Struktura šablony** rozbalte **Model \> InvoiceBase \> CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="7c902-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="7c902-170">V části **CompanyInfo** vyberte položku **WebsiteURI**.</span><span class="sxs-lookup"><span data-stu-id="7c902-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![Vybraná položka WebsiteURI](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="7c902-172">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="7c902-172">Select **Bind**.</span></span>
11. <span data-ttu-id="7c902-173">V podokně **struktura šablony** vyberte možnost **Uložit** a poté zavřete stránku Editor šablon BDM.</span><span class="sxs-lookup"><span data-stu-id="7c902-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="7c902-174">V pracovním prostoru **Správa obchodních dokumentů** se na kartě **šablona** v pravém podokně zobrazí aktualizovaná šablona.</span><span class="sxs-lookup"><span data-stu-id="7c902-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="7c902-175">V mřížce si povšimněte, že pole **Stav** pro upravenou šablonu bylo změněno na **koncept** a pole **Revize** již není prázdné.</span><span class="sxs-lookup"><span data-stu-id="7c902-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="7c902-176">Tyto změny označují, že byl zahájen proces úpravy této šablony.</span><span class="sxs-lookup"><span data-stu-id="7c902-176">These changes indicate that the process of editing this template has been started.</span></span>

![Upravená šablona v pracovním prostoru Správa obchodních dokumentů](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="7c902-178">Kontrola nastavení společnosti</span><span class="sxs-lookup"><span data-stu-id="7c902-178">Review company settings</span></span>

1.  <span data-ttu-id="7c902-179">Přejděte do části **Správa organizace \> Organizace \> Právnické osoby**.</span><span class="sxs-lookup"><span data-stu-id="7c902-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="7c902-180">Na pevné záložce **Kontaktní informace** zkontrolujte, zda je zadána adresa URL společnosti.</span><span class="sxs-lookup"><span data-stu-id="7c902-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Adresa URL společnosti zadaná na stránce právnické osoby](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="7c902-182">Generování obchodních dokumentů pro otestování aktualizované šablony</span><span class="sxs-lookup"><span data-stu-id="7c902-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="7c902-183">V aplikaci změňte společnost na **USMF** a přejděte na **Pohledávky \> Faktury \> Všechny faktury s volným textem**.</span><span class="sxs-lookup"><span data-stu-id="7c902-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="7c902-184">Vyberte fakturu **FTI-00000002** a poté vyberte možnost **Správa tisku**.</span><span class="sxs-lookup"><span data-stu-id="7c902-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="7c902-185">V levém podokně rozbalte položky **Modul – pohledávky \> Dokumenty \> Volné faktury**.</span><span class="sxs-lookup"><span data-stu-id="7c902-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="7c902-186">V části **Volná textová faktura** vyberte úroveň **Původní dokument** k určení rozsahu faktur pro zpracování.</span><span class="sxs-lookup"><span data-stu-id="7c902-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="7c902-187">V pravém podokně v poli **Formát sestavy** vyberte pro určenou úroveň dokumentu **volnou textovou fakturu (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="7c902-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Vybraná volná textová šablona (Excel) Contoso](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="7c902-189">Stisknutím klávesy **Esc** zavřete aktuální stránku.</span><span class="sxs-lookup"><span data-stu-id="7c902-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="7c902-190">Vyberte **Tisk \> Vybrané**.</span><span class="sxs-lookup"><span data-stu-id="7c902-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="7c902-191">Stáhněte vygenerovaný dokument a otevřete jej v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="7c902-191">Download the generated document, and open it in Excel.</span></span>

    ![Volná textová faktura v aplikaci Excel](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="7c902-193">Upravená šablona slouží k vygenerování sestavy volné faktury pro vybranou položku.</span><span class="sxs-lookup"><span data-stu-id="7c902-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="7c902-194">Chcete-li analyzovat, jak je tato sestava ovlivněna změnami, které jste provedli v šabloně, můžete tuto sestavu spustit v jedné relaci aplikace bezprostředně po změně šablony v jiné relaci aplikace.</span><span class="sxs-lookup"><span data-stu-id="7c902-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="7c902-195">Související odkazy</span><span class="sxs-lookup"><span data-stu-id="7c902-195">Related links</span></span>

[<span data-ttu-id="7c902-196">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="7c902-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="7c902-197">Přehled správy obchodních dokumentů</span><span class="sxs-lookup"><span data-stu-id="7c902-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="7c902-198">Návrh konfigurace pro generování sestav ve formátu OPENXML</span><span class="sxs-lookup"><span data-stu-id="7c902-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)

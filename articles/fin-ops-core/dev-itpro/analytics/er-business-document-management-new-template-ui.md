---
title: Uživatelské rozhraní ve stylu Microsoft Office v modulu Správa obchodních dokumentů
description: Toto téma obsahuje informace o tom, jak používat nové uživatelské rozhraní ve funkci správy obchodních dokumentů v rozhraní elektronického výkaznictví (ER).
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881029"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="afc1c-103">Uživatelské rozhraní ve stylu Microsoft Office v modulu Správa obchodních dokumentů</span><span class="sxs-lookup"><span data-stu-id="afc1c-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afc1c-104">Správa obchodních dokumentů a umožňuje podnikovým uživatelům upravovat šablony obchodních dokumentů pomocí služby Microsoft 365 nebo příslušné desktopové aplikace Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="afc1c-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="afc1c-105">Úpravy mohou zahrnovat změny návrhu nebo nová nasazení, nebo uživatelé mohou přidávat zástupné symboly, které budou zahrnovat další data, aniž by bylo nutné změnit zdrojový kód.</span><span class="sxs-lookup"><span data-stu-id="afc1c-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="afc1c-106">Další informace o způsobu práce se správou obchodních dokumentů naleznete v tématu [Přehled správy obchodních dokumentů](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="afc1c-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="afc1c-107">Nové uživatelské rozhraní pro dokumenty je jasnější a má pohodlnější používání.</span><span class="sxs-lookup"><span data-stu-id="afc1c-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="afc1c-108">V oblasti **obchodního dokumentu** jsou zobrazeny pouze ty šablony, které jsou k dispozici pro aktuálního poskytovatele.</span><span class="sxs-lookup"><span data-stu-id="afc1c-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="afc1c-109">V předchozím uživatelském rozhraní karta **Šablona** obsahovala všechny šablony, které byly k dispozici libovolným poskytovatelům.</span><span class="sxs-lookup"><span data-stu-id="afc1c-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="afc1c-110">Také se zobrazily všechny šablony, které vytvořil a upravil jakýkoli uživatel, který měl stejnou roli.</span><span class="sxs-lookup"><span data-stu-id="afc1c-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="afc1c-111">Tlačítko **Nový dokument** můžete použít k vytváření a úpravě šablony v konfiguraci formátu elektronického výkaznictví, kterou poskytuje jiný poskytovatel.</span><span class="sxs-lookup"><span data-stu-id="afc1c-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="afc1c-112">V příkladu v tomto tématu je poskytovatelem Microsoft.</span><span class="sxs-lookup"><span data-stu-id="afc1c-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="afc1c-113">Alternativně můžete vytvořit šablonu nahráním vlastní šablony ve formátu Excel.</span><span class="sxs-lookup"><span data-stu-id="afc1c-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="afc1c-114">Video [Vytvoření nového obchodního dokumentu pomocí správy obchodních dokumentů](https://youtu.be/gAIYl-mM_pw) (zobrazeno výše) je zahrnuto v souboru[seznamu skladeb Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), který je k dispozici na YouTube.</span><span class="sxs-lookup"><span data-stu-id="afc1c-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="afc1c-115">Zpřístupnění nového uživatelského rozhraní dokumentu v modulu Správa obchodních dokumentů</span><span class="sxs-lookup"><span data-stu-id="afc1c-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="afc1c-116">Chcete-li začít používat nové uživatelské rozhraní dokumentu v modulu správa obchodních dokumentů, je třeba zapnout funkci **Prostředí UI podobné systému Office pro správu obchodního dokumentu** v pracovním prostoru **správy funkcí**.</span><span class="sxs-lookup"><span data-stu-id="afc1c-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="afc1c-117">Chcete-li tuto funkci zapnout pro všechny právnické osoby, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="afc1c-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="afc1c-118">V pracovním prostoru **Správa funkcí** na kartě **Vše** vyberte v seznamu funkci **Prostředí UI podobné systému Office pro správu obchodního dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="afc1c-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="afc1c-119">Výběrem možnosti **Povolit nyní** zapněte vybranou funkci.</span><span class="sxs-lookup"><span data-stu-id="afc1c-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="afc1c-120">K nové funkci budete mít přístup po aktualizaci stránky.</span><span class="sxs-lookup"><span data-stu-id="afc1c-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="afc1c-121">Úprava šablon vlastněných ostatními poskytovateli</span><span class="sxs-lookup"><span data-stu-id="afc1c-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="afc1c-122">V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.</span><span class="sxs-lookup"><span data-stu-id="afc1c-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Pracovní prostor správy obchodních dokumentů](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="afc1c-124">Na kartě **Vybrat** vyberte dokument, který chcete použít jako šablonu, a poté vyberte možnost **Vytvořit dokument**.</span><span class="sxs-lookup"><span data-stu-id="afc1c-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Dialogové okno obchodních dokumentů](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="afc1c-126">V novém dialogovém okně v poli **Název** změňte požadovaným způsobem název.</span><span class="sxs-lookup"><span data-stu-id="afc1c-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="afc1c-127">Text názvu se použije k pojmenování nové konfigurace formátu elektronického výkaznictví, která je automaticky vytvořena.</span><span class="sxs-lookup"><span data-stu-id="afc1c-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="afc1c-128">Verze konceptu této konfigurace **(Kopie sestavy FTI odběratele (GER)**) bude obsahovat upravenou šablonu a bude automaticky označena pro spuštění tohoto formátu elektronického výkaznictví pro aktuálního uživatele.</span><span class="sxs-lookup"><span data-stu-id="afc1c-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="afc1c-129">Původní šablona ze základní konfigurace formátu elektronického výkaznictví bude použita ke spuštění tohoto formátu elektronického výkaznictví pro každého jiného uživatele.</span><span class="sxs-lookup"><span data-stu-id="afc1c-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="afc1c-130">V poli **Název** změňte název první revize upravitelné šablony, která bude automaticky vytvořena.</span><span class="sxs-lookup"><span data-stu-id="afc1c-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="afc1c-131">V poli **Komentář** aktualizujte poznámky pro revizi upravitelné šablony, která bude automaticky vytvořena.</span><span class="sxs-lookup"><span data-stu-id="afc1c-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="afc1c-132">Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.</span><span class="sxs-lookup"><span data-stu-id="afc1c-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dialogové okno vytvoření dokumentu](./media/BDM_overview_new_template3.png)

<span data-ttu-id="afc1c-134">Tlačítko **Nový dokument** se používá pro vytváření úpravy šablony v konfiguraci formátu elektronického výkaznictví, kterou poskytuje jiný poskytovatel.</span><span class="sxs-lookup"><span data-stu-id="afc1c-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="afc1c-135">V tomto příkladu je poskytovatelem Microsoft.</span><span class="sxs-lookup"><span data-stu-id="afc1c-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="afc1c-136">Když vyberete **Nový dokument**, zobrazí se všechny šablony vlastněné aktuálními a jinými poskytovateli.</span><span class="sxs-lookup"><span data-stu-id="afc1c-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="afc1c-137">Po výběru bude šablona otevřena pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="afc1c-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="afc1c-138">Upravená šablona bude poté uložena do nové konfigurace formátu elektronického výkaznictví, která bude automaticky vygenerována.</span><span class="sxs-lookup"><span data-stu-id="afc1c-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="afc1c-139">Nahrajte šablonu, která používá existující formát aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="afc1c-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="afc1c-140">Před odesláním šablony postupujte podle těchto pokynů a poskytněte požadované informace.</span><span class="sxs-lookup"><span data-stu-id="afc1c-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="afc1c-141">V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.</span><span class="sxs-lookup"><span data-stu-id="afc1c-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Pracovní prostor správy obchodních dokumentů](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="afc1c-143">Na stránce **Vytvořit novou šablonu** na kartě **Nahrát** na kartě **Šablona** vyberte možnost **Procházet** k vyhledání a výběru souboru Excel, který chcete použít jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="afc1c-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="afc1c-144">V části **Šablona** se pole **Název** a **Popis** vyplňují automaticky.</span><span class="sxs-lookup"><span data-stu-id="afc1c-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="afc1c-145">Určují název a popis nové konfigurace formátu ER, která se automaticky vytvoří.</span><span class="sxs-lookup"><span data-stu-id="afc1c-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="afc1c-146">V případě potřeby můžete tato pole upravit.</span><span class="sxs-lookup"><span data-stu-id="afc1c-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="afc1c-147">V části **Typ dokumentu** do pole **Název** zadejte typ obchodního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="afc1c-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="afc1c-148">Tato hodnota se použije k vyhledání správného zdroje dat (tj. konfigurace modelu ER).</span><span class="sxs-lookup"><span data-stu-id="afc1c-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Karta Šablona](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="afc1c-150">Na kartě **Zdroj dat** na rychlé kartě **Filtr** vyberte **Použít filtr**.</span><span class="sxs-lookup"><span data-stu-id="afc1c-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="afc1c-151">V části **Zdroj dat** je pole **Název** vyplněno automaticky nebo můžete hodnotu vybrat ručně.</span><span class="sxs-lookup"><span data-stu-id="afc1c-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="afc1c-152">Pomocí filtru můžete vyhledat název příslušného zdroje dat podle názvu, popisu, kódu země/oblasti a typu obchodního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="afc1c-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Karta zdroje dat](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="afc1c-154">Karta **Filtr** se používá k vyhledání správného zdroje dat (tj. konfigurace modelu ER).</span><span class="sxs-lookup"><span data-stu-id="afc1c-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="afc1c-155">Můžete upravit všechna pole filtru a vyhledat nejvhodnější zdroj dat pro dokument, který nahráváte.</span><span class="sxs-lookup"><span data-stu-id="afc1c-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="afc1c-156">Podmínky na kartě **Filtr** se používají jako podmínky **OR**.</span><span class="sxs-lookup"><span data-stu-id="afc1c-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="afc1c-157">Na kartě **Mapování** vyberte **Automaticky zjistit**.</span><span class="sxs-lookup"><span data-stu-id="afc1c-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="afc1c-158">Pole **Definice kořene** je vyplněno automaticky nebo můžete hodnotu vybrat ručně.</span><span class="sxs-lookup"><span data-stu-id="afc1c-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="afc1c-159">Tato karta zobrazuje mapování konce pro prvky ze šablony a modelu.</span><span class="sxs-lookup"><span data-stu-id="afc1c-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Karta Mapování](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="afc1c-161">Mapování v části **Struktura šablony** používá úplnou shodu štítků nebo popisů ve zdroji dat v jazyce uživatele a v názvu buňky v šabloně.</span><span class="sxs-lookup"><span data-stu-id="afc1c-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="afc1c-162">Vyberte **Vytvořit dokument** k potvrzení, že chcete vytvořit šablonu a zahájit proces úprav.</span><span class="sxs-lookup"><span data-stu-id="afc1c-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="afc1c-163">Další informace naleznete v tématu [Přehled správy obchodních dokumentů](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="afc1c-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="afc1c-164">Pokud v elektronickém vykazování není poskytovatel, můžete ho vytvořit.</span><span class="sxs-lookup"><span data-stu-id="afc1c-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="afc1c-165">Pokud neexistuje žádný aktivní poskytovatel, můžete jej aktivovat.</span><span class="sxs-lookup"><span data-stu-id="afc1c-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="afc1c-166">Chcete-li vytvořit poskytovatele, změňte název poskytovatele v poli **Název**, aktualizujte internetovou adresu nového poskytovatele v poli **Internetová adresa** a vyberte **OK** k potvrzení.</span><span class="sxs-lookup"><span data-stu-id="afc1c-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![Vytvoření nového poskytovatele v BDM](./media/bdm_create_provider.png)
    
- <span data-ttu-id="afc1c-168">Chcete-li aktivovat stávajícího poskytovatele, vyberte jeho jméno v poli **Poskytovatel konfigurace** a vyberte **OK** k nastavení poskytovatele jako aktivního.</span><span class="sxs-lookup"><span data-stu-id="afc1c-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![Aktivace poskytovatele v BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="afc1c-170">Každá šablona BDM bude odkazovat na zprostředkovatele jako na autora konfigurace.</span><span class="sxs-lookup"><span data-stu-id="afc1c-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="afc1c-171">Proto je pro šablonu vyžadován aktivní poskytovatel.</span><span class="sxs-lookup"><span data-stu-id="afc1c-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

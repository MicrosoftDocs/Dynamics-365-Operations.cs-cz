---
title: Nové uživatelské rozhraní dokumentu v modulu Správa obchodních dokumentů
description: Toto téma obsahuje informace o tom, jak používat nové uživatelské rozhraní dokumentu (UI) ve funkci správy obchodních dokumentů rámce elektronického výkaznictví.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681345"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="b571a-103">Nové uživatelské rozhraní dokumentu v modulu Správa obchodních dokumentů</span><span class="sxs-lookup"><span data-stu-id="b571a-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b571a-104">Správa obchodních dokumentů a umožňuje podnikovým uživatelům upravovat šablony obchodních dokumentů pomocí služby Microsoft 365 nebo příslušné desktopové aplikace Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="b571a-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="b571a-105">Úpravy mohou zahrnovat změny návrhu nebo nová nasazení, nebo uživatelé mohou přidávat zástupné symboly, které budou zahrnovat další data, aniž by bylo nutné změnit zdrojový kód.</span><span class="sxs-lookup"><span data-stu-id="b571a-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="b571a-106">Další informace o způsobu práce se správou obchodních dokumentů naleznete v tématu [Přehled správy obchodních dokumentů](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="b571a-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="b571a-107">Nové uživatelské rozhraní pro dokumenty je jasnější a má pohodlnější používání.</span><span class="sxs-lookup"><span data-stu-id="b571a-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="b571a-108">V oblasti **obchodního dokumentu** jsou zobrazeny pouze ty šablony, které jsou k dispozici pro aktuálního poskytovatele.</span><span class="sxs-lookup"><span data-stu-id="b571a-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="b571a-109">Tlačítko **Nový dokument** umožňuje uživatelům vytvářet a upravovat šablonu v konfiguraci formátu elektronického výkaznictví, kterou poskytuje jiný poskytovatel.</span><span class="sxs-lookup"><span data-stu-id="b571a-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="b571a-110">V příkladu v tomto tématu je poskytovatelem Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b571a-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="b571a-111">Zpřístupnění nového uživatelského rozhraní dokumentu v modulu Správa obchodních dokumentů</span><span class="sxs-lookup"><span data-stu-id="b571a-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="b571a-112">Chcete-li začít používat nové uživatelské rozhraní dokumentu v modulu správa obchodních dokumentů, je třeba zapnout funkci **Prostředí UI podobné systému Office pro správu obchodního dokumentu** v pracovním prostoru **správy funkcí**.</span><span class="sxs-lookup"><span data-stu-id="b571a-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="b571a-113">Chcete-li tuto funkci zapnout pro všechny právnické osoby, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="b571a-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="b571a-114">V pracovním prostoru **Správa funkcí** na kartě **Nová** vyberte v seznamu funkci **Prostředí UI podobné systému Office pro správu obchodního dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="b571a-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="b571a-115">Výběrem možnosti **Povolit nyní** zapněte vybranou funkci.</span><span class="sxs-lookup"><span data-stu-id="b571a-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="b571a-116">K nové funkci budete mít přístup po aktualizaci stránky.</span><span class="sxs-lookup"><span data-stu-id="b571a-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="b571a-117">Úprava šablon vlastněných ostatními poskytovateli</span><span class="sxs-lookup"><span data-stu-id="b571a-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="b571a-118">V pracovním prostoru **správy obchodních dokumentů** vyberte **Nový dokument**.</span><span class="sxs-lookup"><span data-stu-id="b571a-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Pracovní prostor správy obchodních dokumentů](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="b571a-120">V dialogovém okně vyberte dokument, který chcete použít jako šablonu, a poté vyberte možnost **Vytvořit dokument**.</span><span class="sxs-lookup"><span data-stu-id="b571a-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Dialogové okno obchodních dokumentů](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="b571a-122">V novém dialogovém okně v poli **Název** změňte požadovaným způsobem název.</span><span class="sxs-lookup"><span data-stu-id="b571a-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="b571a-123">Text názvu se použije k pojmenování nové konfigurace formátu elektronického výkaznictví, která je automaticky vytvořena.</span><span class="sxs-lookup"><span data-stu-id="b571a-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="b571a-124">Verze konceptu této konfigurace **(Kopie sestavy FTI odběratele (GER)**) bude obsahovat upravenou šablonu a bude automaticky označena pro spuštění tohoto formátu elektronického výkaznictví pro aktuálního uživatele.</span><span class="sxs-lookup"><span data-stu-id="b571a-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="b571a-125">Původní šablona ze základní konfigurace formátu elektronického výkaznictví bude použita ke spuštění tohoto formátu elektronického výkaznictví pro každého jiného uživatele.</span><span class="sxs-lookup"><span data-stu-id="b571a-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="b571a-126">V poli **Název** změňte název první revize upravitelné šablony, která bude automaticky vytvořena.</span><span class="sxs-lookup"><span data-stu-id="b571a-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="b571a-127">V poli **Komentář** aktualizujte poznámky pro revizi upravitelné šablony, která bude automaticky vytvořena.</span><span class="sxs-lookup"><span data-stu-id="b571a-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="b571a-128">Klepnutím na tlačítko **OK** potvrďte zahájení procesu úprav.</span><span class="sxs-lookup"><span data-stu-id="b571a-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dialogové okno vytvoření dokumentu](./media/BDM_overview_new_template3.png)

<span data-ttu-id="b571a-130">Tlačítko **Nový dokument** se používá pro vytváření úpravy šablony v konfiguraci formátu elektronického výkaznictví, kterou poskytuje jiný poskytovatel.</span><span class="sxs-lookup"><span data-stu-id="b571a-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="b571a-131">V tomto příkladu je poskytovatelem Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b571a-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="b571a-132">Když vyberete **Nový dokument**, zobrazí se všechny šablony vlastněné aktuálními a jinými poskytovateli.</span><span class="sxs-lookup"><span data-stu-id="b571a-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="b571a-133">Po výběru bude šablona otevřena pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="b571a-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="b571a-134">Upravená šablona bude poté uložena do nové konfigurace formátu elektronického výkaznictví, která bude automaticky vygenerována.</span><span class="sxs-lookup"><span data-stu-id="b571a-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="b571a-135">Další informace naleznete v tématu [Přehled správy obchodních dokumentů](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="b571a-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

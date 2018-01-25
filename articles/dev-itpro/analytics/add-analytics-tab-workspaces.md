---
title: "Přidání analýz do pracovního prostoru pomocí Power BI Embedded"
description: "Toto téma popisuje, jak vložit sestavu Power BI na kartě Analýzy v pracovním prostoru."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: 9447b0d9eedbdd56f1e221a48f687a94a19d31c4
ms.contentlocale: cs-cz
ms.lasthandoff: 01/25/2018

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="b3568-103">Přidání analýz do pracovního prostoru pomocí Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="b3568-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b3568-104">Tato funkce je podporována v aplikaci Dynamics 365 for Finance and Operations (verze 7.2 a novější).</span><span class="sxs-lookup"><span data-stu-id="b3568-104">This feature is supported in Dynamics 365 for Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="b3568-105">Úvod</span><span class="sxs-lookup"><span data-stu-id="b3568-105">Introduction</span></span>
<span data-ttu-id="b3568-106">Toto téma popisuje, jak vložit sestavu Microsoft Power BI na kartě **Analýzy** v pracovním prostoru.</span><span class="sxs-lookup"><span data-stu-id="b3568-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="b3568-107">V uvedeném příkladu rozšíříme pracovní prostor **Správa rezervací** v aplikaci Správa vozového parku na kartě **Analýzy** tak, aby zahrnovala analytický pracovní prostor.</span><span class="sxs-lookup"><span data-stu-id="b3568-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b3568-108">Požadavky</span><span class="sxs-lookup"><span data-stu-id="b3568-108">Prerequisites</span></span>
+ <span data-ttu-id="b3568-109">Přístup k prostředí pro vývojáře, kde běží aktualizace Platform 8 nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="b3568-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="b3568-110">Analytická sestava (soubor .pbix) vytvořená pomocí Microsoft Power BI Desktop, která obsahuje datový model, jehož zdrojem je databáze úložiště Entity.</span><span class="sxs-lookup"><span data-stu-id="b3568-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="b3568-111">Přehled</span><span class="sxs-lookup"><span data-stu-id="b3568-111">Overview</span></span>
<span data-ttu-id="b3568-112">Ať rozšíříte existující pracovní prostor aplikace nebo zadáte nový pracovní prostor, můžete použít vložené analytické zobrazení ke kvalifikovaným a interaktivním zobrazením vašich obchodních údajích.</span><span class="sxs-lookup"><span data-stu-id="b3568-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="b3568-113">Proces přidání karty analytického pracovního prostoru má čtyři kroky.</span><span class="sxs-lookup"><span data-stu-id="b3568-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="b3568-114">Přidejte soubor .pbix jako prostředek Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b3568-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="b3568-115">Definujte kartu analytického pracovního prostoru.</span><span class="sxs-lookup"><span data-stu-id="b3568-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="b3568-116">Vložte prostředek .pbix prostředků na kartu pracovní prostor.</span><span class="sxs-lookup"><span data-stu-id="b3568-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="b3568-117">Volitelné: Přidejte rozšíření pro přizpůsobení zobrazení.</span><span class="sxs-lookup"><span data-stu-id="b3568-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="b3568-118">Další informace o postupu vytváření analytických sestav naleznete v tématu [Úvod do práce s počítačem Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="b3568-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="b3568-119">Tato stránka je skvělý zdroj informací, které pomáhají vytvořit přinutit řešení generování analytických sestav.</span><span class="sxs-lookup"><span data-stu-id="b3568-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="b3568-120">Přidejte soubor .pbix jako prostředek</span><span class="sxs-lookup"><span data-stu-id="b3568-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="b3568-121">Dříve než začnete, musíte vytvořit nebo získat sestavu Power BI, kterou vložíte do pracovního prostoru.</span><span class="sxs-lookup"><span data-stu-id="b3568-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="b3568-122">Další informace o postupu vytváření analytických sestav naleznete v tématu [Úvod do práce s počítačem Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="b3568-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span>
 
<span data-ttu-id="b3568-123">Tento postup slouží k přidání souboru .pbix jako artefaktů projektu Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b3568-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="b3568-124">Vytvořte nový projekt v příslušném modelu.</span><span class="sxs-lookup"><span data-stu-id="b3568-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="b3568-125">V Průzkumníku řešení vyberte projekt, klepněte pravým tlačítkem myši a poté vyberte **Přidat** > **Nová položka**.</span><span class="sxs-lookup"><span data-stu-id="b3568-125">In Solution Explorer, select the project, right-click, and then select **Add** > **New Item**.</span></span>
3. <span data-ttu-id="b3568-126">V dialogovém okně **Přidat novou položku**, v části **Operační artefakty**, vyberte šablonu **Prostředek**.</span><span class="sxs-lookup"><span data-stu-id="b3568-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="b3568-127">Zadejte název, který se použije k odkazování na sestavu v metadatech X ++ a klepněte na tlačítko **přidat**.</span><span class="sxs-lookup"><span data-stu-id="b3568-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Dialogové okno Přidat novou položku](media/analytical-workspace-add.png)

5. <span data-ttu-id="b3568-129">Najděte soubor .pbix, který obsahuje definici analytické sestavy, a klepněte na tlačítko **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="b3568-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Dialogové okno Vybrat soubor zdrojů](media/analytical-workspace-select-resource.png)
  
<span data-ttu-id="b3568-131">Poté, co jako prostředek Dynamics 365 nepřidáte .pbix soubor, můžete vložit sestavy pracovní prostory a přidat přímé odkazy pomocí položky nabídky.</span><span class="sxs-lookup"><span data-stu-id="b3568-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="b3568-132">Přidat ovládací prvek karty s pracovním prostorem aplikace</span><span class="sxs-lookup"><span data-stu-id="b3568-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="b3568-133">V tomto příkladu doporučujeme rozšířit pracovní prostor **řízení rezervací** v modelu Správa vozového parku přidáním karty **Analýzy** kartu pro definici formuláře **FMClerkWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="b3568-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>
 
<span data-ttu-id="b3568-134">Následující obrázek znázorňuje, jak formulář **FMClerkWorkspace** vypadá v Návrháři v aplikaci Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b3568-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![Formulář FMClerkWorkspace před změnami](media/analytical-workspace-definition-before.png)

<span data-ttu-id="b3568-136">Pomocí následujícího postupu rozšířit definici formuláře pracovního prostoru **Řízení rezervací**.</span><span class="sxs-lookup"><span data-stu-id="b3568-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="b3568-137">Otevřete návrhář formuláře k rozšíření definice návrhu.</span><span class="sxs-lookup"><span data-stu-id="b3568-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="b3568-138">V definici návrhu vyberte nejvyšší prvek označený **Návrhu | Vzor: Pracovní prostor operační**.</span><span class="sxs-lookup"><span data-stu-id="b3568-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="b3568-139">Klepněte pravým tlačítkem myši a poté vyberte **Nová** > **Karta** pro přidání nového ovládacího prvku s názvem **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="b3568-139">Right-click, and then select **New** > **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="b3568-140">V návrháři formuláře vyberte **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="b3568-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="b3568-141">Klepněte pravým tlačítkem myši a poté vyberte **Stránka Nová karta**. Tím přidáte novou kartu.</span><span class="sxs-lookup"><span data-stu-id="b3568-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="b3568-142">Přejmenujte stránku karty, například na **Pracovní prostor**.</span><span class="sxs-lookup"><span data-stu-id="b3568-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="b3568-143">V návrháři formuláře vyberte **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="b3568-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="b3568-144">Klikněte pravým tlačítkem myši a poté vyberte **Stránka Nová karta**.</span><span class="sxs-lookup"><span data-stu-id="b3568-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="b3568-145">Přejmenujte stránku karty, například na **Analýza**.</span><span class="sxs-lookup"><span data-stu-id="b3568-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="b3568-146">V návrháři formuláře vyberte **Analýz (Stránka Karta)**.</span><span class="sxs-lookup"><span data-stu-id="b3568-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="b3568-147">Nastavte vlastnost **Titulek** na **Analýza**.</span><span class="sxs-lookup"><span data-stu-id="b3568-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="b3568-148">Klepněte pravým tlačítkem myši na ovládací prvek a poté vyberte **Nová** > **Skupina** pro přidání nové skupiny ovládacích prvků.</span><span class="sxs-lookup"><span data-stu-id="b3568-148">Right-click the control, and then select **New** > **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="b3568-149">Přejmenujte skupinu formuláře, například na **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="b3568-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="b3568-150">V návrháři formuláře vyberte **PanoramaBody (karta)** a přetáhněte ovládací prvek na kartu **Pracovní prostor**.</span><span class="sxs-lookup"><span data-stu-id="b3568-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="b3568-151">V definici návrhu vyberte nejvyšší prvek označený **Návrhu | Vzor: Pracovní prostor operační**.</span><span class="sxs-lookup"><span data-stu-id="b3568-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="b3568-152">Klikněte pravým tlačítkem a vyberte **Odebrat vzor**.</span><span class="sxs-lookup"><span data-stu-id="b3568-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="b3568-153">Znovu klikněte pravým tlačítkem a vyberte **Přidat vzor** > **Pracovní prostor s kartami**.</span><span class="sxs-lookup"><span data-stu-id="b3568-153">Right-click again, and then select **Add pattern** > **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="b3568-154">Vytvořit nové sestavení pro ověření provedených změn.</span><span class="sxs-lookup"><span data-stu-id="b3568-154">Perform a build to verify your changes.</span></span>
 
<span data-ttu-id="b3568-155">Následující obrázek znázorňuje, jak návrh vypadá poté, co tyto změny se projeví.</span><span class="sxs-lookup"><span data-stu-id="b3568-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace po provedení změn](media/analytical-workspace-definition-after.png)

<span data-ttu-id="b3568-157">Poté, co jste přidali ovládací prvky formuláře, které budou použity pro sestavu pracovního prostoru, je nutné definovat velikost nadřazenému ovládacímu prvku tak, aby se přizpůsobilo rozvržení.</span><span class="sxs-lookup"><span data-stu-id="b3568-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="b3568-158">Ve výchozím bude v sestavě viditelná stránka **Podokno Filtry** a **Karta**.</span><span class="sxs-lookup"><span data-stu-id="b3568-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="b3568-159">Můžete však změnit viditelnost zobrazení těchto ovládacích prvků v závislosti na příjemci cílové sestavy.</span><span class="sxs-lookup"><span data-stu-id="b3568-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>
 
> [!NOTE]
> <span data-ttu-id="b3568-160">Pro vložené pracovní prostory doporučujeme použití rozšíření ke skrytí stránky **Podokno Filtry** i **Karta**.</span><span class="sxs-lookup"><span data-stu-id="b3568-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>
 
<span data-ttu-id="b3568-161">Nyní jste dokončili úlohu rozšíření definice formuláře aplikace.</span><span class="sxs-lookup"><span data-stu-id="b3568-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="b3568-162">Další informace o tom, jak používáte rozšíření přizpůsobení naleznete v tématu [přizpůsobení: rozšíření a vrstvy](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="b3568-162">For more information about how to use extensions to do customizations, see  [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="b3568-163">Přidání obchodní logiky X ++ pro vložení ovládacího prvku prohlížeče</span><span class="sxs-lookup"><span data-stu-id="b3568-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="b3568-164">Pomocí těchto kroků přidejte obchodní logiku, která inicializuje ovládací prvek prohlížeče sestav, který je vložen do pracovního prostoru **řízení rezervací**.</span><span class="sxs-lookup"><span data-stu-id="b3568-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="b3568-165">Otevřete návrhář formuláře **FMClerkWorkspace** k rozšíření definice návrhu.</span><span class="sxs-lookup"><span data-stu-id="b3568-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="b3568-166">Stisknutím klávesy F7 přejděte ke kódu za definicí kódu.</span><span class="sxs-lookup"><span data-stu-id="b3568-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="b3568-167">Přidejte následující kód X++:</span><span class="sxs-lookup"><span data-stu-id="b3568-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="b3568-168">Vytvořit nové sestavení pro ověření provedených změn.</span><span class="sxs-lookup"><span data-stu-id="b3568-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="b3568-169">Nyní jste dokončili úkol přidání obchodní logiky v ovládacím prvku prohlížeče sestavy.</span><span class="sxs-lookup"><span data-stu-id="b3568-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="b3568-170">Následující obrázek znázorňuje, jak pracovní prostor vypadá poté, co se tyto změny projeví.</span><span class="sxs-lookup"><span data-stu-id="b3568-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Sestava vložená do pracovního prostoru](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="b3568-172">Můžete zobrazit stávající operační zobrazení pomocí záložek pracovního prostor pod nadpisem stránky.</span><span class="sxs-lookup"><span data-stu-id="b3568-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="b3568-173">Odkaz</span><span class="sxs-lookup"><span data-stu-id="b3568-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="b3568-174">Metoda PBIReportHelper.initializeReportControl</span><span class="sxs-lookup"><span data-stu-id="b3568-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="b3568-175">Tento oddíl obsahuje informace o pomocnících třídy, která se používá k vložení do ovládacího prvku skupiny sestavy Power BI (zdroj .pbix).</span><span class="sxs-lookup"><span data-stu-id="b3568-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="b3568-176">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3568-176">Syntax</span></span>
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="b3568-177">Parametry</span><span class="sxs-lookup"><span data-stu-id="b3568-177">Parameters</span></span>

| <span data-ttu-id="b3568-178">Jméno</span><span class="sxs-lookup"><span data-stu-id="b3568-178">Name</span></span> | <span data-ttu-id="b3568-179">popis</span><span class="sxs-lookup"><span data-stu-id="b3568-179">Description</span></span> |
|---|---|
| <span data-ttu-id="b3568-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="b3568-180">resourceName</span></span> | <span data-ttu-id="b3568-181">Název zdroje .pbix </span><span class="sxs-lookup"><span data-stu-id="b3568-181">The name of the .pbix resource.</span></span> |
| <span data-ttu-id="b3568-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="b3568-182">formGroupControl</span></span> | <span data-ttu-id="b3568-183">Ovládací prvek skupiny formuláře pro použití sestavy Power BI.</span><span class="sxs-lookup"><span data-stu-id="b3568-183">The form group control to apply the Power BI report control to.</span></span> |
| <span data-ttu-id="b3568-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="b3568-184">defaultPageName</span></span> | <span data-ttu-id="b3568-185">Výchozí název stránky.</span><span class="sxs-lookup"><span data-stu-id="b3568-185">The default page name.</span></span> |
| <span data-ttu-id="b3568-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="b3568-186">showFilterPane</span></span> | <span data-ttu-id="b3568-187">Logická hodnota, která určuje, zda má být podokno filtru zobrazené (**true**) nebo skryté (**false**).</span><span class="sxs-lookup"><span data-stu-id="b3568-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="b3568-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="b3568-188">showNavPane</span></span> | <span data-ttu-id="b3568-189">Logická hodnota, která určuje, zda má být navigační podokno zobrazené (**true**) nebo skryté (**false**).</span><span class="sxs-lookup"><span data-stu-id="b3568-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="b3568-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="b3568-190">defaultFilters</span></span> | <span data-ttu-id="b3568-191">Výchozí filtry pro sestavu Power BI.</span><span class="sxs-lookup"><span data-stu-id="b3568-191">The default filters for the Power BI report.</span></span> |


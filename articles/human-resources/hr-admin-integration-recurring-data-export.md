---
title: Vytvoření aplikace pro export opakujících se dat
description: Tento článek ukazuje, jak vytvořit logic app v Microsoft Azure, která exportuje data z Microsoft Dynamics 365 Human Resources na opakujícím se plánu.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a4a963bcfe5932f5642b43751ccd96c472fec0d9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054997"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="27243-103">Vytvoření aplikace pro export opakujících se dat</span><span class="sxs-lookup"><span data-stu-id="27243-103">Create a recurring data export app</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="27243-104">Tento článek ukazuje, jak vytvořit logic app v Microsoft Azure, která exportuje data z Microsoft Dynamics 365 Human Resources na opakujícím se plánu.</span><span class="sxs-lookup"><span data-stu-id="27243-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="27243-105">Výukový kurz využívá pro export dat rozhraní API REST balíčku DMF aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27243-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="27243-106">Po exportu dat uloží logic app exportovaný balíček dat do složky Microsoft OneDrive pro firmy.</span><span class="sxs-lookup"><span data-stu-id="27243-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="27243-107">Scénáře obchodu</span><span class="sxs-lookup"><span data-stu-id="27243-107">Business scenario</span></span>

<span data-ttu-id="27243-108">V jednom typickém obchodním scénáři pro integrace Microsoft Dynamics 365 je nutné data exportovat do podrřízeného systému v opakovaném plánu.</span><span class="sxs-lookup"><span data-stu-id="27243-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="27243-109">Tento výukový program ukazuje, jak exportovat všechny záznamy pracovníka z Microsoft Dynamics 365 Human Resources a uložit seznam pracovníků do složky OneDrive pro firmy.</span><span class="sxs-lookup"><span data-stu-id="27243-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="27243-110">Konkrétní data, která jsou exportována v tomto kurzu a cíl exportovaných dat, jsou pouze příklady.</span><span class="sxs-lookup"><span data-stu-id="27243-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="27243-111">Lze je snadno změnit tak, aby splňovaly vaše obchodní potřeby.</span><span class="sxs-lookup"><span data-stu-id="27243-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="27243-112">Použité technologie</span><span class="sxs-lookup"><span data-stu-id="27243-112">Technologies used</span></span>

<span data-ttu-id="27243-113">Tento výukový kurz používá následující technologie:</span><span class="sxs-lookup"><span data-stu-id="27243-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="27243-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – Hlavní zdroj dat pro pracovníky, kteří budou exportováni.</span><span class="sxs-lookup"><span data-stu-id="27243-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="27243-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – technologie, která poskytuje orchestraci a plánování opakovaného exportu.</span><span class="sxs-lookup"><span data-stu-id="27243-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="27243-116">**[Konektory](/azure/connectors/apis-list)** – technologie, která se používá k propojení logic app s požadovanými koncovými body.</span><span class="sxs-lookup"><span data-stu-id="27243-116">**[Connectors](/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="27243-117">Konektor [HTTP s Azure AD](/connectors/webcontents/)</span><span class="sxs-lookup"><span data-stu-id="27243-117">[HTTP with Azure AD](/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="27243-118">Konektor [OneDrive pro firmy](/azure/connectors/connectors-create-api-onedriveforbusiness)</span><span class="sxs-lookup"><span data-stu-id="27243-118">[OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="27243-119">**[Rozhraní REST API balíčku DMF](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – technologie, která slouží k aktivaci exportu a sledování jejího průběhu.</span><span class="sxs-lookup"><span data-stu-id="27243-119">**[DMF package REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="27243-120">**[OneDrive pro firmy](https://onedrive.live.com/about/business/)** – cíl pro exportované pracovníky.</span><span class="sxs-lookup"><span data-stu-id="27243-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="27243-121">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="27243-121">Prerequisites</span></span>

<span data-ttu-id="27243-122">Před zahájením cvičení v tomto kurzu je nutné mít k dispozici následující položky:</span><span class="sxs-lookup"><span data-stu-id="27243-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="27243-123">Prostředí Human Resources, které má oprávnění na úrovni správce v daném prostředí</span><span class="sxs-lookup"><span data-stu-id="27243-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="27243-124">[Předplatné Azure](https://azure.microsoft.com/free/) pro hostování logic app</span><span class="sxs-lookup"><span data-stu-id="27243-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="27243-125">Cvičení</span><span class="sxs-lookup"><span data-stu-id="27243-125">The exercise</span></span>

<span data-ttu-id="27243-126">Na konci tohoto cvičení budete mít logic app, která je připojena k prostředí Human Resources a ke svému účtu OneDrive pro firmy.</span><span class="sxs-lookup"><span data-stu-id="27243-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="27243-127">Logic app exportuje balíček dat z Human Resources, počká na dokončení exportu, stáhne exportovaný balíček dat a uloží jej do složky OneDrive pro firmy, kterou jste určili.</span><span class="sxs-lookup"><span data-stu-id="27243-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="27243-128">Dokončená logic app se bude podobat následující ilustraci.</span><span class="sxs-lookup"><span data-stu-id="27243-128">The completed logic app will resemble the following illustration.</span></span>

![Přehled logic app](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="27243-130">Krok 1: Vytvoření projektu exportu dat v Human Resources</span><span class="sxs-lookup"><span data-stu-id="27243-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="27243-131">V aplikaci Human Resources vytvořte projekt exportu dat, který exportuje pracovníky.</span><span class="sxs-lookup"><span data-stu-id="27243-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="27243-132">Nazvěte projekt **Export pracovníků** a ujistěte se, že je možnost **Generovat balíček dat** nastaven na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="27243-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="27243-133">Přidejte do projektu jednu entitu (**Pracovník**) a vyberte formát, do kterého chcete exportovat.</span><span class="sxs-lookup"><span data-stu-id="27243-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="27243-134">(V tomto výukovém kurzu se používá formát Microsoft Excel.)</span><span class="sxs-lookup"><span data-stu-id="27243-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Datový projekt exportu pracovníků](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="27243-136">Zapamatujte si název projektu exportu dat.</span><span class="sxs-lookup"><span data-stu-id="27243-136">Remember the name of the data export project.</span></span> <span data-ttu-id="27243-137">Budete ho potřebovat při vytváření logic app v dalším kroku.</span><span class="sxs-lookup"><span data-stu-id="27243-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="27243-138">Krok 2: Vytvoření logic app</span><span class="sxs-lookup"><span data-stu-id="27243-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="27243-139">Sada cvičení zahrnuje vytvoření logic app.</span><span class="sxs-lookup"><span data-stu-id="27243-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="27243-140">Na portálu Azure vytvořte logic app.</span><span class="sxs-lookup"><span data-stu-id="27243-140">In the Azure portal, create a logic app.</span></span>

    ![Stránka vytvoření logic app](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="27243-142">V aplikaci Logic Apps Designer začněte s prázdnou logic app.</span><span class="sxs-lookup"><span data-stu-id="27243-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="27243-143">Přidejte [aktivační událost plánu opakování](/azure/connectors/connectors-native-recurrence) pro spuštění logic app každých 24 hodin (nebo podle zvoleného plánu).</span><span class="sxs-lookup"><span data-stu-id="27243-143">Add a [Recurrence Schedule trigger](/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Dialogové okno opakování](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="27243-145">Volejte [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API pro naplánování exportu vašeho datového balíčku.</span><span class="sxs-lookup"><span data-stu-id="27243-145">Call the [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="27243-146">Použijte akci **Vyvolat požadavek HTTP** z HTTP s konektorem Azure AD.</span><span class="sxs-lookup"><span data-stu-id="27243-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="27243-147">**Základní adresa URL zdroje** : adresa URL vašeho prostředí Human Resources (Nezahrnujte informace o cestě a oboru názvů.)</span><span class="sxs-lookup"><span data-stu-id="27243-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="27243-148">**URI zdroje Azure AD:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="27243-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="27243-149">Služba Human Resources ještě neposkytuje konektor, který vystavuje všechna rozhraní API, která tvoří rozhraní REST API balíčku DMF, jako například **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="27243-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="27243-150">Místo toho je nutné volat rozhraní API pomocí nezpracovaných požadavků HTTPS prostřednictvím protokolu HTTP s konektorem Azure AD.</span><span class="sxs-lookup"><span data-stu-id="27243-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="27243-151">Tento konektor používá Azure Active Directory (Azure AD) pro ověřování a autorizaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27243-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP s konektorem Azure AD](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="27243-153">Přihlaste se ke svému prostředí Human Resources prostřednictvím protokolu HTTP s konektorem Azure AD.</span><span class="sxs-lookup"><span data-stu-id="27243-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="27243-154">Nastavte požadavek HTTP **POST** na volání **ExportToPackage** DMF REST API.</span><span class="sxs-lookup"><span data-stu-id="27243-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="27243-155">**Metoda:** POST</span><span class="sxs-lookup"><span data-stu-id="27243-155">**Method:** POST</span></span>
        - <span data-ttu-id="27243-156">**URL adresa požadavku:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="27243-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="27243-157">**Tělo požadavku:**</span><span class="sxs-lookup"><span data-stu-id="27243-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Vyvolat akci požadavku HTTP](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="27243-159">Můžete chtít přejmenovat každý krok tak, aby byl výstižnější než výchozí název, **Vyvolat požadavek HTTP**.</span><span class="sxs-lookup"><span data-stu-id="27243-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="27243-160">Tento krok můžete například přejmenovat na **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="27243-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="27243-161">[Inicializujte proměnnou](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) pro uložení stavu spuštění požadavku **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="27243-161">[Initialize a variable](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Akce inicializace proměnné](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="27243-163">Počkejte, než bude stav spuštění exportu dat **Úspěšný**.</span><span class="sxs-lookup"><span data-stu-id="27243-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="27243-164">Přidejte [do smyčky](/azure/logic-apps/logic-apps-control-flow-loops#until-loop), což se opakuje, než bude hodnota proměnné **ExecutionStatus** **Úspěšné**.</span><span class="sxs-lookup"><span data-stu-id="27243-164">Add an [Until loop](/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="27243-165">Přidejte akci **zpoždění**, která počká pět sekund předtím, než se dotazuje na stav aktuálního spuštění exportu.</span><span class="sxs-lookup"><span data-stu-id="27243-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Kontejner do smyčky](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="27243-167">Nastavte počet limitů na **15** a počkejte na dokončení exportu maximálně 75 sekund (15 iterací x 5 sekund).</span><span class="sxs-lookup"><span data-stu-id="27243-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="27243-168">Pokud export trvá déle, upravte podle potřeby počet limitů.</span><span class="sxs-lookup"><span data-stu-id="27243-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="27243-169">Přidejte akci **Vyvolat požadavek HTTP** pro volání [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API a nastavte proměnnou **ExecutionStatus** na výsledek odpovědi **GetExecutionSummaryStatus**.</span><span class="sxs-lookup"><span data-stu-id="27243-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="27243-170">Tato ukázka neprovádí kontrolu chyb.</span><span class="sxs-lookup"><span data-stu-id="27243-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="27243-171">Rozhraní API **GetExecutionSummaryStatus** může vracet neúspěšné stavy terminálu (ostatní stavy, než **úspěšné**).</span><span class="sxs-lookup"><span data-stu-id="27243-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="27243-172">Další informace naleznete v [dokumentaci k rozhraní API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="27243-172">For more information, see the [API documentation](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="27243-173">**Metoda:** POST</span><span class="sxs-lookup"><span data-stu-id="27243-173">**Method:** POST</span></span>
        - <span data-ttu-id="27243-174">**URL adresa požadavku:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="27243-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="27243-175">**Tělo požadavku:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="27243-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="27243-176">Je možné, že budete muset zadat hodnotu **Tělo požadavku** v zobrazení kódu nebo v editoru funkcí v návrháři.</span><span class="sxs-lookup"><span data-stu-id="27243-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![Vyvolat akci požadavku HTTP 2](media/integration-logic-app-get-execution-status-step.png)

        ![Nastavení akce proměnné](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="27243-179">Hodnota akce **Nastavení proměnné** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) se bude lišit od hodnoty těla pro **Vyvolat požadavek HTTP 2**, a to i v případě, že návrhář zobrazí hodnoty stejným způsobem.</span><span class="sxs-lookup"><span data-stu-id="27243-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="27243-180">Získejte URL adresu stažení exportovaného balíčku.</span><span class="sxs-lookup"><span data-stu-id="27243-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="27243-181">Přidejte akci **Vyvolat požadavek HTTP** pro volání [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span><span class="sxs-lookup"><span data-stu-id="27243-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="27243-182">**Metoda:** POST</span><span class="sxs-lookup"><span data-stu-id="27243-182">**Method:** POST</span></span>
        - <span data-ttu-id="27243-183">**URL adresa požadavku:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="27243-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="27243-184">**Tělo požadavku:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="27243-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![Akce GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="27243-186">Stáhněte exportovaný balíček.</span><span class="sxs-lookup"><span data-stu-id="27243-186">Download the exported package.</span></span>

    - <span data-ttu-id="27243-187">Přidejte požadavek HTTP **GET** (vestavěnou [akci konektoru HTTP](/azure/connectors/connectors-native-http)) a stáhněte balíček z URL adresy, která se vrátila v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="27243-187">Add an HTTP **GET** request (a built-in [HTTP connector action](/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="27243-188">**Metoda:** GET</span><span class="sxs-lookup"><span data-stu-id="27243-188">**Method:** GET</span></span>
        - <span data-ttu-id="27243-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="27243-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="27243-190">Je možné, že budete muset zadat hodnotu **URI** v zobrazení kódu nebo v editoru funkcí v návrháři.</span><span class="sxs-lookup"><span data-stu-id="27243-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![Akce HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="27243-192">Tento požadavek nevyžaduje žádné další ověření, protože adresa URL, kterou vrací **GetExportedPackageUrl** API, zahrnuje token podpisů sdílených přístupů, který uděluje přístup ke stažení souboru.</span><span class="sxs-lookup"><span data-stu-id="27243-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="27243-193">Uložte stažený balíček pomocí konektoru [OneDrive pro firmy](/azure/connectors/connectors-create-api-onedriveforbusiness).</span><span class="sxs-lookup"><span data-stu-id="27243-193">Save the downloaded package by using the [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="27243-194">Přidejteakci [vytvoření souboru](/connectors/onedriveforbusinessconnector/#create-file)  OneDrive pro firmy.</span><span class="sxs-lookup"><span data-stu-id="27243-194">Add a OneDrive for Business [Create File](/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="27243-195">Podle potřeby se připojte ke svému účtu OneDrive pro firmy.</span><span class="sxs-lookup"><span data-stu-id="27243-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="27243-196">**Cesta ke složce**: složka podle vašeho výběru</span><span class="sxs-lookup"><span data-stu-id="27243-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="27243-197">**Název souboru:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="27243-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="27243-198">**Obsah souboru:** tělo z předchozího kroku (dynamický obsah)</span><span class="sxs-lookup"><span data-stu-id="27243-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Akce vytvoření souboru](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="27243-200">Krok 3: Testování logic app</span><span class="sxs-lookup"><span data-stu-id="27243-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="27243-201">Chcete-li testovat logic app, vyberte v návrháři tlačítko **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="27243-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="27243-202">Uvidíte, že kroky spuštění logic app budou spuštěny.</span><span class="sxs-lookup"><span data-stu-id="27243-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="27243-203">Po 30 až 40 sekundách by mělo být spuštění logic app dokončeno a složka OneDrive pro firmy by měla obsahovat nový soubor balíčku, který obsahuje exportované pracovníky.</span><span class="sxs-lookup"><span data-stu-id="27243-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="27243-204">Pokud je u některého kroku hlášeno selhání, vyberte v návrháři neúspěšný krok a zkontrolujte pole **Vstupy** a **Výstupy**.</span><span class="sxs-lookup"><span data-stu-id="27243-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="27243-205">Proveďte ladění a upravte krok podle potřeby, aby se chyby opravily.</span><span class="sxs-lookup"><span data-stu-id="27243-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="27243-206">Následující obrázek ukazuje, jak vypadá aplikace Logic Apps Designer, když jsou všechny kroky logic app úspěšně spuštěny.</span><span class="sxs-lookup"><span data-stu-id="27243-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Úspěšné spuštění logic app](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="27243-208">Souhrn</span><span class="sxs-lookup"><span data-stu-id="27243-208">Summary</span></span>

<span data-ttu-id="27243-209">V tomto návodu jste se seznámili s použitím llogic app k exportu dat z Human Resources a k uložení exportovaných dat do složky OneDrive pro firmy.</span><span class="sxs-lookup"><span data-stu-id="27243-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="27243-210">Kroky v tomto výukovém programu můžete upravit podle potřeb firmy.</span><span class="sxs-lookup"><span data-stu-id="27243-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
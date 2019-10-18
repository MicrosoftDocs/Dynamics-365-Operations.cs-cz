---
title: Správa životního cyklu konfigurace elektronického vykazování
description: Toto téma popisuje způsob správy životního cyklu konfigurací elektronického výkaznictví pro řešení Microsoft Dynamics 365 Finance.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6206b3a1ac298af98e4b69b6800b9a493658c4ea
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181282"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="b0e62-103">Správa životního cyklu konfigurace elektronického vykazování</span><span class="sxs-lookup"><span data-stu-id="b0e62-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0e62-104">Toto téma popisuje způsob správy životního cyklu konfigurací elektronického výkaznictví pro řešení Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b0e62-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="b0e62-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="b0e62-105">Overview</span></span>

<span data-ttu-id="b0e62-106">Elektronické výkaznictví je modul pro podporu elektronických dokumentů specifických pro danou zemi a požadovaných zákonem.</span><span class="sxs-lookup"><span data-stu-id="b0e62-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="b0e62-107">Obecně platí, že Elektronické výkaznictví předpokládá schopnost provádět následující činnosti pro jeden elektronický dokument.</span><span class="sxs-lookup"><span data-stu-id="b0e62-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="b0e62-108">Další podrobnosti získáte v tématu [Přehled elektronického vykazování](general-electronic-reporting.md)</span><span class="sxs-lookup"><span data-stu-id="b0e62-108">For more details, see [Electronic reporting overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="b0e62-109">Návrh šablony pro elektronický dokument:</span><span class="sxs-lookup"><span data-stu-id="b0e62-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="b0e62-110">Identifikace požadovaných zdrojů dat, které lze zpřístupnit v tomto dokumentu:</span><span class="sxs-lookup"><span data-stu-id="b0e62-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="b0e62-111">Základní data, například datové tabulky, datové entity a třídy.</span><span class="sxs-lookup"><span data-stu-id="b0e62-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="b0e62-112">Vlastnosti určité pro proces jako datum provedení a čas a časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="b0e62-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="b0e62-113">Vstupní parametry uživatele definované koncovým uživatelem při spuštění.</span><span class="sxs-lookup"><span data-stu-id="b0e62-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="b0e62-114">Definování prvků nezbytných pro dokument a také jejich topologie pro určení konečného formátu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b0e62-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="b0e62-115">Konfigurace požadovaného toku dat z vybraného zdroje dat pro definování prvků dokumentu prostřednictvím součástí formátu vazeb datového zdroje dokumentu a určení logiky procesu řízení.</span><span class="sxs-lookup"><span data-stu-id="b0e62-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="b0e62-116">Zpřístupněte šablonu tak, aby ji možné použít v jiných instancích:</span><span class="sxs-lookup"><span data-stu-id="b0e62-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="b0e62-117">Převeďte šablonu dokumentu, která byla vytvořena v aplikaci Dynamics AX, na konfiguraci elektronického výkaznictví, a exportujte konfiguraci z aktuální instance aplikace jako balíček XML, který může být uložen lokálně nebo v rámci LCS.</span><span class="sxs-lookup"><span data-stu-id="b0e62-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="b0e62-118">Převeďte konfiguraci elektronického výkaznictví jako šablonu dokumentu aplikace.</span><span class="sxs-lookup"><span data-stu-id="b0e62-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="b0e62-119">Importujte balíček XML, který je uložen místně nebo v rámci LCS do aktuální instance.</span><span class="sxs-lookup"><span data-stu-id="b0e62-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="b0e62-120">Upravte šablonu elektronického dokumentu:</span><span class="sxs-lookup"><span data-stu-id="b0e62-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="b0e62-121">Přeneste šablonu z LCS do aktuální instance jako konfiguraci elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b0e62-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="b0e62-122">Návrh vlastní verze konfigurace elektronického výkaznictví a uchování odkazu na základní verzi.</span><span class="sxs-lookup"><span data-stu-id="b0e62-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="b0e62-123">Integrujte šablonu v konkrétním obchodním procesu tak, aby byly k dispozici v aplikaci:</span><span class="sxs-lookup"><span data-stu-id="b0e62-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="b0e62-124">Konfigurujte nastavení aplikace tak, aby aplikace začala používat konfiguraci elektronického výkaznictví (vytvořte odkaz na tuto konfiguraci v parametru souvisejícím s procesem).</span><span class="sxs-lookup"><span data-stu-id="b0e62-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="b0e62-125">Například odkazujte na konfiguraci elektronického výkaznictví v konkrétní metodě platby závazků s cílem vygenerovat zprávu pro elektronickou platbu pro zpracování faktur.</span><span class="sxs-lookup"><span data-stu-id="b0e62-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="b0e62-126">Použití šablony v určitém obchodním procesu:</span><span class="sxs-lookup"><span data-stu-id="b0e62-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="b0e62-127">Spusťte konfiguraci služby ER do určitého obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="b0e62-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="b0e62-128">Například odkazujte na konfiguraci elektronického výkaznictví ke zpracování fakturu, když je vybraná metoda platby, která odkazuje na konfiguraci ER.</span><span class="sxs-lookup"><span data-stu-id="b0e62-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="b0e62-129">Koncepty</span><span class="sxs-lookup"><span data-stu-id="b0e62-129">Concepts</span></span>
<span data-ttu-id="b0e62-130">Následující role a související aktivity jsou přidruženy k životním cyklu konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b0e62-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="b0e62-131">Role</span><span class="sxs-lookup"><span data-stu-id="b0e62-131">Role</span></span>                                       | <span data-ttu-id="b0e62-132">Aktivity</span><span class="sxs-lookup"><span data-stu-id="b0e62-132">Activities</span></span>                                                      | <span data-ttu-id="b0e62-133">popis</span><span class="sxs-lookup"><span data-stu-id="b0e62-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="b0e62-134">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="b0e62-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="b0e62-135">Vytvořte a spravujte součásti elektronického výkaznictví (modelů a formáty).</span><span class="sxs-lookup"><span data-stu-id="b0e62-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="b0e62-136">Obchodní pracovník, který navrhuje modely specifické pro doménu elektronického výkaznictví, navrhuje také požadované šablony pro elektronické dokumenty a vhodně je prováže.</span><span class="sxs-lookup"><span data-stu-id="b0e62-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="b0e62-137">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="b0e62-137">Electronic reporting developer</span></span>             | <span data-ttu-id="b0e62-138">Vytvořte a spravujte mapování datového modelu.</span><span class="sxs-lookup"><span data-stu-id="b0e62-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="b0e62-139">Specialista, který vybere požadované zdroje dat Finance a naváže je modely dat specifických pro doménu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b0e62-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="b0e62-140">Účetní supervizor</span><span class="sxs-lookup"><span data-stu-id="b0e62-140">Accounting supervisor</span></span>                      | <span data-ttu-id="b0e62-141">Nakonfigurujte nastavení týkajícího se procesu, které odkazuje na artefakty elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b0e62-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="b0e62-142">Například role **Účetní supervizor**, která umožňuje použít nastavení konfigurace elektronického výkaznictví pro konkrétní účty metodu plateb závazků s cílem vygenerovat zprávu elektronické platby pro zpracování faktur.</span><span class="sxs-lookup"><span data-stu-id="b0e62-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="b0e62-143">Úředník plateb závazků</span><span class="sxs-lookup"><span data-stu-id="b0e62-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="b0e62-144">Použijte artefakty elektronického výkaznictví v určitém obchodním procesu.</span><span class="sxs-lookup"><span data-stu-id="b0e62-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="b0e62-145">Například role **Úředník pro platby závazků**, která umožňuje vygenerovat zprávy elektronických plateb pro zpracování faktur na základě formátu elektronického výkaznictví nastaveného pro konkrétní způsob platby.</span><span class="sxs-lookup"><span data-stu-id="b0e62-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="b0e62-146">Životní cyklus vývoje konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="b0e62-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="b0e62-147">Z následujících důvodů doporučujeme navrhovat konfigurace elektronického výkaznictví ve vývojovém prostředí v oddělené instanci aplikace Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b0e62-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="b0e62-148">Uživatelé mají buď role **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**, kteří mohou upravovat konfigurace a spouštět je pro účely testování.</span><span class="sxs-lookup"><span data-stu-id="b0e62-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="b0e62-149">To může způsobit volání metod tříd a tabulek, které mohou být potenciálně škodlivé pro obchodní data a výkon použití instance.</span><span class="sxs-lookup"><span data-stu-id="b0e62-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="b0e62-150">Volání metod tříd a tabulek jako zdroje dat elektronického výkaznictví nejsou omezeny vstupními body a jsou zaznamenány do obsahu společnosti.</span><span class="sxs-lookup"><span data-stu-id="b0e62-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="b0e62-151">Proto citlivá obchodná data mohou zobrazovat uživatelé mající buď roli **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="b0e62-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="b0e62-152">Konfigurace elektronického výkaznictví navržené ve vývojovém prostředí je možné odeslat do testovacího prostředí pro hodnocení konfigurace (správný proces integrace, správnost výsledků, výkonnost) a kontrola kvality (správnost role řídící přístupová práva, dělení zodpovědnosti atd.).</span><span class="sxs-lookup"><span data-stu-id="b0e62-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="b0e62-153">Pro tento účel lze použít funkce, které umožňují výměnu konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b0e62-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="b0e62-154">Ověřené konfigurace elektronického výkaznictví je možné uložit buď do LCS pro sdílení se službami odběratelů nebo do výrobního prostředí pro interní použití, jak ukazuje následující ilustrace.</span><span class="sxs-lookup"><span data-stu-id="b0e62-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![Životní cyklus elektronického výkaznictví](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="b0e62-156">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b0e62-156">Additional resources</span></span>

[<span data-ttu-id="b0e62-157">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="b0e62-157">Electronic reporting overview</span></span>](general-electronic-reporting.md)

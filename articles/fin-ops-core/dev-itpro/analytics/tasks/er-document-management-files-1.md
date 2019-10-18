---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 1 - Příprava datového modelu)
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3bd01f7aa1ef95230c37458a5676111a5efa23c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182547"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1-prepare-data-model"></a><span data-ttu-id="db182-103">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 1: Příprava datového modelu)</span><span class="sxs-lookup"><span data-stu-id="db182-103">ER Use Document Management files in format outputs (Part 1: Prepare data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db182-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="db182-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="db182-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="db182-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="db182-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="db182-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="db182-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="db182-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="db182-108">Získání přístupu k seznamu konfigurací poskytovaných společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="db182-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="db182-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="db182-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="db182-110">Ujistěte se, že poskytovatel 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="db182-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="db182-111">je k dispozici a označen jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="db182-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="db182-112">Vyberte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="db182-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="db182-113">Poskytovatel</span><span class="sxs-lookup"><span data-stu-id="db182-113">provider.</span></span>
3. <span data-ttu-id="db182-114">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="db182-114">Click Repositories.</span></span>
    * <span data-ttu-id="db182-115">Pokud již existuje úložiště typu Zdroje operace, přeskočte zbývající kroky aktuální dílčí úlohy.</span><span class="sxs-lookup"><span data-stu-id="db182-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="db182-116">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="db182-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="db182-117">V poli Typ úložiště konfigurace zadejte "Provozní prostředky".</span><span class="sxs-lookup"><span data-stu-id="db182-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="db182-118">Klikněte na Vytvořit úložiště.</span><span class="sxs-lookup"><span data-stu-id="db182-118">Click Create repository.</span></span>
7. <span data-ttu-id="db182-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="db182-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="db182-120">Získání konfigurace modelu odběratele poskytnuté společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="db182-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="db182-121">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="db182-121">Click Show filters.</span></span>
2. <span data-ttu-id="db182-122">Použijte následující filtry: Zadejte hodnotu filtru Provozní prostředky do pole Název pomocí operátoru filtru "začíná na". Jako hodnotu filtru do pole popis zadejte "" pomocí operátoru filtru "začíná na".</span><span class="sxs-lookup"><span data-stu-id="db182-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="db182-123">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="db182-123">Click Show filters.</span></span>
4. <span data-ttu-id="db182-124">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="db182-124">Click Open.</span></span>
5. <span data-ttu-id="db182-125">Ve stromovém zobrazení vyberte možnost CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="db182-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="db182-126">Vyberte konfiguraci modelu "Model faktury odběratele" k importu.</span><span class="sxs-lookup"><span data-stu-id="db182-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="db182-127">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="db182-127">Click Import.</span></span>
    * <span data-ttu-id="db182-128">Klikněte na Import pro verzi 1 vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="db182-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="db182-129">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="db182-129">Click Yes.</span></span>
8. <span data-ttu-id="db182-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="db182-130">Close the page.</span></span>
9. <span data-ttu-id="db182-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="db182-131">Close the page.</span></span>
10. <span data-ttu-id="db182-132">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="db182-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="db182-133">Ve stromovém zobrazení vyberte možnost CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="db182-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="db182-134">Vytvořte odvozený model na podporu přístupu k souborům správy dokumentů.</span><span class="sxs-lookup"><span data-stu-id="db182-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="db182-135">Vytvoříte vlastní konfiguraci modelu faktury odběratele vyplývající z konfigurace dodávané společností Microsoft.</span><span class="sxs-lookup"><span data-stu-id="db182-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="db182-136">Pomocí této konfigurace budete implementovat přístup k souborům Správy dokumentů a zpřístupníte je pro elektronické dokumenty, které vytvoříte na základě tohoto modelu.</span><span class="sxs-lookup"><span data-stu-id="db182-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="db182-137">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="db182-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="db182-138">V poli Nový zadejte „Odvodit z názvu: Model faktury zákazníka, Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="db182-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="db182-139">Zadejte hodnotu Model faktury odběratele (vlastní) do pole Název.</span><span class="sxs-lookup"><span data-stu-id="db182-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="db182-140">Model faktury odběratele (vlastní)</span><span class="sxs-lookup"><span data-stu-id="db182-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="db182-141">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="db182-141">Click Create configuration.</span></span>


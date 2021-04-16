---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 1 - Příprava datového modelu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví (ER) na použití souborů (příloh) správy dokumentů ve výstupu ER. (část 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b265c9af0635e6c9fb6295f7e8e4e353b2a5ba5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754931"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="04d06-104">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 1 - Příprava datového modelu)</span><span class="sxs-lookup"><span data-stu-id="04d06-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04d06-105">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="04d06-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="04d06-106">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="04d06-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="04d06-107">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="04d06-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="04d06-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="04d06-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="04d06-109">Získání přístupu k seznamu konfigurací poskytovaných společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="04d06-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="04d06-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="04d06-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="04d06-111">Ujistěte se, že poskytovatel 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="04d06-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="04d06-112">je k dispozici a označen jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="04d06-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="04d06-113">Vyberte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="04d06-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="04d06-114">Poskytovatel</span><span class="sxs-lookup"><span data-stu-id="04d06-114">provider.</span></span>
3. <span data-ttu-id="04d06-115">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="04d06-115">Click Repositories.</span></span>

    <span data-ttu-id="04d06-116">Pokud již existuje úložiště typu Zdroje operace, přeskočte zbývající kroky aktuální dílčí úlohy.</span><span class="sxs-lookup"><span data-stu-id="04d06-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="04d06-117">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="04d06-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="04d06-118">V poli Typ úložiště konfigurace zadejte "Provozní prostředky".</span><span class="sxs-lookup"><span data-stu-id="04d06-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="04d06-119">Klikněte na Vytvořit úložiště.</span><span class="sxs-lookup"><span data-stu-id="04d06-119">Click Create repository.</span></span>
7. <span data-ttu-id="04d06-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="04d06-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="04d06-121">Získání konfigurace modelu odběratele poskytnuté společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="04d06-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="04d06-122">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="04d06-122">Click Show filters.</span></span>
2. <span data-ttu-id="04d06-123">Použijte následující filtry: Zadejte hodnotu filtru Provozní prostředky do pole Název pomocí operátoru filtru "začíná na". Jako hodnotu filtru do pole popis zadejte "" pomocí operátoru filtru "začíná na".</span><span class="sxs-lookup"><span data-stu-id="04d06-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="04d06-124">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="04d06-124">Click Show filters.</span></span>
4. <span data-ttu-id="04d06-125">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="04d06-125">Click Open.</span></span>
5. <span data-ttu-id="04d06-126">Ve stromovém zobrazení vyberte možnost CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="04d06-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="04d06-127">Vyberte konfiguraci modelu "Model faktury odběratele" k importu.</span><span class="sxs-lookup"><span data-stu-id="04d06-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="04d06-128">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="04d06-128">Click Import.</span></span>

    <span data-ttu-id="04d06-129">Klikněte na Import pro verzi 1 vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="04d06-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="04d06-130">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="04d06-130">Click Yes.</span></span>
8. <span data-ttu-id="04d06-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="04d06-131">Close the page.</span></span>
9. <span data-ttu-id="04d06-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="04d06-132">Close the page.</span></span>
10. <span data-ttu-id="04d06-133">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="04d06-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="04d06-134">Ve stromovém zobrazení vyberte možnost CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="04d06-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="04d06-135">Vytvořte odvozený model na podporu přístupu k souborům správy dokumentů.</span><span class="sxs-lookup"><span data-stu-id="04d06-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="04d06-136">Vytvoříte vlastní konfiguraci modelu faktury odběratele vyplývající z konfigurace dodávané společností Microsoft.</span><span class="sxs-lookup"><span data-stu-id="04d06-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="04d06-137">Pomocí této konfigurace budete implementovat přístup k souborům Správy dokumentů a zpřístupníte je pro elektronické dokumenty, které vytvoříte na základě tohoto modelu.</span><span class="sxs-lookup"><span data-stu-id="04d06-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="04d06-138">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="04d06-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="04d06-139">V poli Nový zadejte „Odvodit z názvu: Model faktury zákazníka, Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="04d06-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="04d06-140">Zadejte hodnotu Model faktury odběratele (vlastní) do pole Název.</span><span class="sxs-lookup"><span data-stu-id="04d06-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="04d06-141">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="04d06-141">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
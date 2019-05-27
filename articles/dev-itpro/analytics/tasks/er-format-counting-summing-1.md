---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 1 - Vytvoření formátu)
description: Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1f925ef8d772189a505f2793de1176756866bf4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544626"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1-create-format"></a><span data-ttu-id="10b40-103">Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 1: Vytvoření formátu)</span><span class="sxs-lookup"><span data-stu-id="10b40-103">ER Configure format to do counting and summing (Part 1: Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10b40-104">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="10b40-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="10b40-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="10b40-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="10b40-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="10b40-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="10b40-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="10b40-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="10b40-108">Získání přístupu k seznamu konfigurací poskytovaných společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="10b40-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="10b40-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="10b40-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="10b40-110">Ujistěte se, že poskytovatel 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="10b40-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="10b40-111">je k dispozici a označen jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="10b40-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="10b40-112">Vyberte poskytovatele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="10b40-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="10b40-113"> </span><span class="sxs-lookup"><span data-stu-id="10b40-113">provider.</span></span>
3. <span data-ttu-id="10b40-114">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="10b40-114">Click Repositories.</span></span>
    * <span data-ttu-id="10b40-115">Pokud již existuje úložiště typu Zdroje operace, přeskočte zbývající kroky aktuální dílčí úlohy.</span><span class="sxs-lookup"><span data-stu-id="10b40-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="10b40-116">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="10b40-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="10b40-117">V poli Typ úložiště konfigurace zadejte "Provozní prostředky".</span><span class="sxs-lookup"><span data-stu-id="10b40-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="10b40-118">Klikněte na Vytvořit úložiště.</span><span class="sxs-lookup"><span data-stu-id="10b40-118">Click Create repository.</span></span>
7. <span data-ttu-id="10b40-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="10b40-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="10b40-120">Získání konfigurací Intrastat dodaných společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="10b40-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="10b40-121">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="10b40-121">Click Open.</span></span>
2. <span data-ttu-id="10b40-122">Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="10b40-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="10b40-123">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="10b40-123">Click Import.</span></span>
    * <span data-ttu-id="10b40-124">Klikněte na Import pro verzi 1.1 vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="10b40-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="10b40-125">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="10b40-125">Click Yes.</span></span>
5. <span data-ttu-id="10b40-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="10b40-126">Close the page.</span></span>
6. <span data-ttu-id="10b40-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="10b40-127">Close the page.</span></span>
7. <span data-ttu-id="10b40-128">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="10b40-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="10b40-129">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="10b40-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="10b40-130">Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="10b40-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


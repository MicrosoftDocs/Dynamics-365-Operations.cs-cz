--- 
title: "Vytvoření formátu pro počítání a sčítání pro elektronické výkaznictví (ER)"
description: "Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: cac3748182ba27735264acc947403d7b857f1b6e
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-formate-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="18e7e-103">Vytvoření formátu pro počítání a sčítání pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="18e7e-103">Create formate for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18e7e-104">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="18e7e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="18e7e-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="18e7e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="18e7e-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="18e7e-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="18e7e-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="18e7e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="18e7e-108">Získání přístupu k seznamu konfigurací poskytovaných společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="18e7e-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="18e7e-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="18e7e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="18e7e-110">Ujistěte se, že poskytovatel 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="18e7e-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="18e7e-111">je k dispozici a označen jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="18e7e-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="18e7e-112">Vyberte poskytovatele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="18e7e-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="18e7e-113"> </span><span class="sxs-lookup"><span data-stu-id="18e7e-113">provider.</span></span>
3. <span data-ttu-id="18e7e-114">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="18e7e-114">Click Repositories.</span></span>
    * <span data-ttu-id="18e7e-115">Pokud již existuje úložiště typu Zdroje operace, přeskočte zbývající kroky aktuální dílčí úlohy.</span><span class="sxs-lookup"><span data-stu-id="18e7e-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="18e7e-116">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="18e7e-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="18e7e-117">V poli Typ úložiště konfigurace zadejte "Provozní prostředky".</span><span class="sxs-lookup"><span data-stu-id="18e7e-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="18e7e-118">Klikněte na Vytvořit úložiště.</span><span class="sxs-lookup"><span data-stu-id="18e7e-118">Click Create repository.</span></span>
7. <span data-ttu-id="18e7e-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="18e7e-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="18e7e-120">Získání konfigurací Intrastat dodaných společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="18e7e-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="18e7e-121">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="18e7e-121">Click Open.</span></span>
2. <span data-ttu-id="18e7e-122">Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="18e7e-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="18e7e-123">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="18e7e-123">Click Import.</span></span>
    * <span data-ttu-id="18e7e-124">Klikněte na Import pro verzi 1.1 vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="18e7e-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="18e7e-125">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="18e7e-125">Click Yes.</span></span>
5. <span data-ttu-id="18e7e-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="18e7e-126">Close the page.</span></span>
6. <span data-ttu-id="18e7e-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="18e7e-127">Close the page.</span></span>
7. <span data-ttu-id="18e7e-128">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="18e7e-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="18e7e-129">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="18e7e-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="18e7e-130">Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="18e7e-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



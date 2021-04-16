---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 1 - Vytvoření formátu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví tak, aby počítal a sčítal na základě dat již vygenerovaného textového výstupu. (část 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f1db144b2bfafa72abeaa92c6b21de717e4acbf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749038"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="67776-104">Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 1 - Vytvoření formátu)</span><span class="sxs-lookup"><span data-stu-id="67776-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67776-105">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="67776-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="67776-106">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="67776-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="67776-107">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="67776-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="67776-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="67776-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="67776-109">Získání přístupu k seznamu konfigurací poskytovaných společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="67776-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="67776-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="67776-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="67776-111">Ujistěte se, že poskytovatel 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="67776-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="67776-112">je k dispozici a označen jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="67776-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="67776-113">Vyberte poskytovatele 'Litware, Inc'.</span><span class="sxs-lookup"><span data-stu-id="67776-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="67776-114"> </span><span class="sxs-lookup"><span data-stu-id="67776-114">provider.</span></span>
3. <span data-ttu-id="67776-115">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="67776-115">Click Repositories.</span></span>
    * <span data-ttu-id="67776-116">Pokud již existuje úložiště typu Zdroje operace, přeskočte zbývající kroky aktuální dílčí úlohy.</span><span class="sxs-lookup"><span data-stu-id="67776-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="67776-117">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="67776-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="67776-118">V poli Typ úložiště konfigurace zadejte "Provozní prostředky".</span><span class="sxs-lookup"><span data-stu-id="67776-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="67776-119">Klikněte na Vytvořit úložiště.</span><span class="sxs-lookup"><span data-stu-id="67776-119">Click Create repository.</span></span>
7. <span data-ttu-id="67776-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="67776-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="67776-121">Získání konfigurací Intrastat dodaných společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="67776-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="67776-122">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="67776-122">Click Open.</span></span>
2. <span data-ttu-id="67776-123">Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="67776-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="67776-124">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="67776-124">Click Import.</span></span>
    * <span data-ttu-id="67776-125">Klikněte na Import pro verzi 1.1 vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="67776-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="67776-126">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="67776-126">Click Yes.</span></span>
5. <span data-ttu-id="67776-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="67776-127">Close the page.</span></span>
6. <span data-ttu-id="67776-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="67776-128">Close the page.</span></span>
7. <span data-ttu-id="67776-129">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="67776-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="67776-130">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="67776-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="67776-131">Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="67776-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
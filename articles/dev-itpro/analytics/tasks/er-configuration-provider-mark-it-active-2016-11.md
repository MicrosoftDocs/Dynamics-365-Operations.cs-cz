--- 
title: "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního pro elektronické výkaznictví (ER)"
description: "Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="16bc5-103">Vytvoření poskytovatele konfigurace a jeho označení jako aktivního pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="16bc5-103">Create a configuration providand mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16bc5-104">Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="16bc5-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="16bc5-105">Každá konfigurace ER bude odkazovat na zprostředkovatele jako na autora konfigurace.</span><span class="sxs-lookup"><span data-stu-id="16bc5-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="16bc5-106">V tomto příkladu vytvoříte konfiguraci poskytovatele pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace poskytovatele ER se sdílí mezi všemi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="16bc5-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="16bc5-107">Vytvoření poskytovatele</span><span class="sxs-lookup"><span data-stu-id="16bc5-107">Create a provider</span></span>
1. <span data-ttu-id="16bc5-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="16bc5-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="16bc5-109">Klikněte na Poskytovatelé konfigurace.</span><span class="sxs-lookup"><span data-stu-id="16bc5-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="16bc5-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="16bc5-110">Click New.</span></span>
    * <span data-ttu-id="16bc5-111">Záznam poskytovatele má jedinečný název a adresu URL.</span><span class="sxs-lookup"><span data-stu-id="16bc5-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="16bc5-112">Pokud záznam pro společnosti Litware, Inc. (http://www.litware.com) již existuje, zkontrolujte obsah této stránky a přeskočte tento postup.</span><span class="sxs-lookup"><span data-stu-id="16bc5-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="16bc5-113">Zadejte Litware, Inc. do pole Název.</span><span class="sxs-lookup"><span data-stu-id="16bc5-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="16bc5-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="16bc5-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="16bc5-115">V poli internetové adresy zadejte "http://www.litware.com".</span><span class="sxs-lookup"><span data-stu-id="16bc5-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="16bc5-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="16bc5-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="16bc5-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="16bc5-117">Click Save.</span></span>
7. <span data-ttu-id="16bc5-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="16bc5-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="16bc5-119">Výběr ve formě aktivního poskytovatele</span><span class="sxs-lookup"><span data-stu-id="16bc5-119">Select as an active provider</span></span>
1. <span data-ttu-id="16bc5-120">Vyberte poskytovatele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="16bc5-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="16bc5-121">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="16bc5-121">Click Set active.</span></span>



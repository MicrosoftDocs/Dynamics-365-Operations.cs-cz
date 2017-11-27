--- 
title: "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního pro elektronické výkaznictví (ER)"
description: "Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
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
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: 2dfa04f280249884af2a237807fb283059444a6c
ms.contentlocale: cs-cz
ms.lasthandoff: 11/02/2017

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="6e72c-103">Vytvoření poskytovatele konfigurace a jeho označení jako aktivního pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="6e72c-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e72c-104">Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může vytvořit poskytovatele konfigurace pro elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6e72c-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="6e72c-105">Každá konfigurace ER bude odkazovat na zprostředkovatele jako na autora konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6e72c-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="6e72c-106">V tomto příkladu vytvoříte konfiguraci poskytovatele pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace poskytovatele ER se sdílí mezi všemi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="6e72c-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="6e72c-107">Vytvoření poskytovatele</span><span class="sxs-lookup"><span data-stu-id="6e72c-107">Create a provider</span></span>
1. <span data-ttu-id="6e72c-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6e72c-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6e72c-109">Klikněte na Poskytovatelé konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6e72c-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="6e72c-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="6e72c-110">Click New.</span></span>
    * <span data-ttu-id="6e72c-111">Záznam poskytovatele má jedinečný název a adresu URL.</span><span class="sxs-lookup"><span data-stu-id="6e72c-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="6e72c-112">Pokud záznam pro společnosti Litware, Inc. (http://www.litware.com) již existuje, zkontrolujte obsah této stránky a přeskočte tento postup.</span><span class="sxs-lookup"><span data-stu-id="6e72c-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="6e72c-113">Zadejte Litware, Inc. do pole Název.</span><span class="sxs-lookup"><span data-stu-id="6e72c-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="6e72c-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6e72c-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="6e72c-115">V poli internetové adresy zadejte "http://www.litware.com".</span><span class="sxs-lookup"><span data-stu-id="6e72c-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="6e72c-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="6e72c-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="6e72c-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6e72c-117">Click Save.</span></span>
7. <span data-ttu-id="6e72c-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6e72c-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="6e72c-119">Výběr ve formě aktivního poskytovatele</span><span class="sxs-lookup"><span data-stu-id="6e72c-119">Select as an active provider</span></span>
1. <span data-ttu-id="6e72c-120">Vyberte poskytovatele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6e72c-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="6e72c-121">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="6e72c-121">Click Set active.</span></span>



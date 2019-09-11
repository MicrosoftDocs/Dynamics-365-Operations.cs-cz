---
title: Vytvoření nových uživatelů
description: Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916477"
---
# <a name="create-new-users"></a><span data-ttu-id="0ba3e-103">Vytvoření nových uživatelů</span><span class="sxs-lookup"><span data-stu-id="0ba3e-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ba3e-104">Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="0ba3e-105">K dokončení tohoto postupu pro přidání uživatele do systému musíte být správcem systému.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="0ba3e-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="0ba3e-107">Přidat nového uživatele</span><span class="sxs-lookup"><span data-stu-id="0ba3e-107">Add a new user</span></span>
1. <span data-ttu-id="0ba3e-108">Přejděte na **Navigační podokno > Moduly > Správa systému > Uživatelé > Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="0ba3e-109">V **podokně akcí** klikněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="0ba3e-110">Zadejte hodnotu do pole **ID uživatele**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="0ba3e-111">Zadejte jednoznačný identifikátor uživatele.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="0ba3e-112">ID uživatele je povinné.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-112">A user ID is required.</span></span>  
4. <span data-ttu-id="0ba3e-113">Do pole **Uživatelské jméno** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="0ba3e-114">Zadejte jméno uživatele.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="0ba3e-115">Zadejte hodnotu do pole **Doména**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="0ba3e-116">Zadejte doménu uživatele.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="0ba3e-117">Zadejte hodnotu do pole **Alias**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="0ba3e-118">Zadejte alias uživatele.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="0ba3e-119">V poli **Společnost** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0ba3e-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="0ba3e-121">V sekci **Role uživatele** klikněte na **Přiřadit role**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="0ba3e-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="0ba3e-123">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-123">Click **OK**.</span></span>
12. <span data-ttu-id="0ba3e-124">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="0ba3e-125">Importovat uživatele</span><span class="sxs-lookup"><span data-stu-id="0ba3e-125">Import users</span></span>
1. <span data-ttu-id="0ba3e-126">V **podokně akcí** klikněte na možnost **Importovat uživatele**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="0ba3e-127">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="0ba3e-128">Klikněte na možnost **Importovat uživatele**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-128">Click **Import users**.</span></span>
4. <span data-ttu-id="0ba3e-129">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-129">Click **Close**.</span></span>


---
title: Vytvoření nových uživatelů
description: Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558704"
---
# <a name="create-new-users"></a><span data-ttu-id="97fd6-103">Vytvoření nových uživatelů</span><span class="sxs-lookup"><span data-stu-id="97fd6-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97fd6-104">Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.</span><span class="sxs-lookup"><span data-stu-id="97fd6-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="97fd6-105">K dokončení tohoto postupu pro přidání uživatele do systému musíte být správcem systému.</span><span class="sxs-lookup"><span data-stu-id="97fd6-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="97fd6-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="97fd6-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="97fd6-107">Přidat nového uživatele</span><span class="sxs-lookup"><span data-stu-id="97fd6-107">Add a new user</span></span>
1. <span data-ttu-id="97fd6-108">Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="97fd6-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="97fd6-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="97fd6-109">Click New.</span></span>
3. <span data-ttu-id="97fd6-110">Zadejte hodnotu do pole ID uživatele.</span><span class="sxs-lookup"><span data-stu-id="97fd6-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="97fd6-111">Zadejte jednoznačný identifikátor uživatele.</span><span class="sxs-lookup"><span data-stu-id="97fd6-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="97fd6-112">ID uživatele je povinné.</span><span class="sxs-lookup"><span data-stu-id="97fd6-112">A user ID is required.</span></span>  
4. <span data-ttu-id="97fd6-113">Do pole Uživatelské jméno zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="97fd6-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="97fd6-114">Zadejte jméno uživatele.</span><span class="sxs-lookup"><span data-stu-id="97fd6-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="97fd6-115">Zadejte hodnotu do pole Doména.</span><span class="sxs-lookup"><span data-stu-id="97fd6-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="97fd6-116">Zadejte doménu uživatele.</span><span class="sxs-lookup"><span data-stu-id="97fd6-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="97fd6-117">Zadejte hodnotu do pole Alias.</span><span class="sxs-lookup"><span data-stu-id="97fd6-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="97fd6-118">Zadejte alias uživatele.</span><span class="sxs-lookup"><span data-stu-id="97fd6-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="97fd6-119">V poli Společnost kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="97fd6-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="97fd6-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="97fd6-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="97fd6-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="97fd6-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="97fd6-122">Vyberte společnost uživatele.</span><span class="sxs-lookup"><span data-stu-id="97fd6-122">Select the user's company</span></span>  
10. <span data-ttu-id="97fd6-123">Klikněte na možnost Přiřadit role.</span><span class="sxs-lookup"><span data-stu-id="97fd6-123">Click Assign roles.</span></span>
11. <span data-ttu-id="97fd6-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="97fd6-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="97fd6-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="97fd6-125">Click OK.</span></span>
13. <span data-ttu-id="97fd6-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="97fd6-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="97fd6-127">Importovat uživatele</span><span class="sxs-lookup"><span data-stu-id="97fd6-127">Import users</span></span>
1. <span data-ttu-id="97fd6-128">Klikněte na možnost Importovat uživatele.</span><span class="sxs-lookup"><span data-stu-id="97fd6-128">Click Import users.</span></span>
2. <span data-ttu-id="97fd6-129">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="97fd6-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="97fd6-130">Klikněte na možnost Importovat uživatele.</span><span class="sxs-lookup"><span data-stu-id="97fd6-130">Click Import users.</span></span>
4. <span data-ttu-id="97fd6-131">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="97fd6-131">Click Close.</span></span>


---
title: Přiřazení uživatelů k rolím zabezpečení
description: Uživatelé musí být přiřazeni k rolím zabezpečení, aby měli přístup k aplikacím Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180960"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="6e745-103">Přiřazení uživatelů k rolím zabezpečení</span><span class="sxs-lookup"><span data-stu-id="6e745-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e745-104">Chcete-li použít cokoli jiného než společné funkce, je nutné, aby byly uživatelům přiřazeny k role zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="6e745-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="6e745-105">Tento postup vysvětluje způsob, jakým správce systému může automaticky přiřadit uživatele k rolím automaticky na základě obchodních dat.</span><span class="sxs-lookup"><span data-stu-id="6e745-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="6e745-106">Automatické přiřazení uživatelů k rolím</span><span class="sxs-lookup"><span data-stu-id="6e745-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="6e745-107">Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.</span><span class="sxs-lookup"><span data-stu-id="6e745-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="6e745-108">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="6e745-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="6e745-109">Vyberte roli, pro kterou chcete konfigurovat pravidlo.</span><span class="sxs-lookup"><span data-stu-id="6e745-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="6e745-110">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="6e745-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="6e745-111">Kliknutím na možnost **Přidat pravidlo** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6e745-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="6e745-112">V seznamu **Vybrat dotaz** najděte a vyberte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="6e745-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="6e745-113">Vyberte dotaz, který chcete použít pro toto pravidlo.</span><span class="sxs-lookup"><span data-stu-id="6e745-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="6e745-114">V seznamu **Název pravidla členství** klikněte na odkaz ve vybraném řádku.</span><span class="sxs-lookup"><span data-stu-id="6e745-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6e745-115">Klikněte na **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="6e745-115">Click **Edit query**.</span></span> <span data-ttu-id="6e745-116">Podle potřeby upravte dotaz.</span><span class="sxs-lookup"><span data-stu-id="6e745-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="6e745-117">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e745-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="6e745-118">Vyloučení uživatelů z automatického přiřazení k roli</span><span class="sxs-lookup"><span data-stu-id="6e745-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="6e745-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6e745-119">Close the page.</span></span>
2. <span data-ttu-id="6e745-120">Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.</span><span class="sxs-lookup"><span data-stu-id="6e745-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="6e745-121">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="6e745-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="6e745-122">Vyberte požadovanou roli.</span><span class="sxs-lookup"><span data-stu-id="6e745-122">Select a role.</span></span> <span data-ttu-id="6e745-123">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="6e745-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="6e745-124">V nabídce **role přiřazené uživatelům** vyberte možnost **Ručně přiřadit nebo vyloučit uživatele.**</span><span class="sxs-lookup"><span data-stu-id="6e745-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="6e745-125">V seznamu **Přiřadit nebo nebo vyloučit uživatele z role** vyberte vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="6e745-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="6e745-126">Vyberte uživatele.</span><span class="sxs-lookup"><span data-stu-id="6e745-126">Select a user.</span></span>  
6. <span data-ttu-id="6e745-127">V **podokně akcí** vyberte možnost **Vyloučit z role**.</span><span class="sxs-lookup"><span data-stu-id="6e745-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="6e745-128">Kliknutím na **Vyloučit z role** vyloučíte vybrané uživatele z role.</span><span class="sxs-lookup"><span data-stu-id="6e745-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="6e745-129">Pokud chcete vyloučení odebrat, vyberte uživatele, pro kterého chcete vyloučení odebrat, a klepněte na tlačítko **Vynulovat stav**.</span><span class="sxs-lookup"><span data-stu-id="6e745-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="6e745-130">Při odebírání vyloučení obnovením stavu uživatele se role uživatele znovu automaticky přiřadí.</span><span class="sxs-lookup"><span data-stu-id="6e745-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="6e745-131">Uživatel však při vynulování stavu není okamžitě přiřazen k roli nebo z ní vyloučen.</span><span class="sxs-lookup"><span data-stu-id="6e745-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="6e745-132">Místo toho je uživateli přiřazena role nebo je z role odebrán při příštím spuštění pravidel pro automatické přiřazení role.</span><span class="sxs-lookup"><span data-stu-id="6e745-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

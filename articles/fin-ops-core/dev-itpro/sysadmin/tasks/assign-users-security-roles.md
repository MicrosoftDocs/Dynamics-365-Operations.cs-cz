---
title: Přiřazení uživatelů k rolím zabezpečení
description: Pro přístup k aplikacím Finance and Operations musí být uživateli přiřazeni k rolím zabezpečení.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
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
ms.openlocfilehash: 0744f45ac91dfb9b5aae35091e3675202c9144f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143531"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="70ab6-103">Přiřazení uživatelů k rolím zabezpečení</span><span class="sxs-lookup"><span data-stu-id="70ab6-103">Assign users to security roles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="70ab6-104">Chcete-li použít cokoli jiného než společné funkce, je nutné, aby byly uživatelům přiřazeny k role zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="70ab6-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="70ab6-105">Tento postup vysvětluje způsob, jakým správce systému může automaticky přiřadit uživatele k rolím automaticky na základě obchodních dat.</span><span class="sxs-lookup"><span data-stu-id="70ab6-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="70ab6-106">Automatické přiřazení uživatelů k rolím</span><span class="sxs-lookup"><span data-stu-id="70ab6-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="70ab6-107">Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.</span><span class="sxs-lookup"><span data-stu-id="70ab6-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="70ab6-108">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="70ab6-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="70ab6-109">Vyberte roli, pro kterou chcete konfigurovat pravidlo.</span><span class="sxs-lookup"><span data-stu-id="70ab6-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="70ab6-110">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="70ab6-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="70ab6-111">Kliknutím na možnost **Přidat pravidlo** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="70ab6-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="70ab6-112">V seznamu **Vybrat dotaz** najděte a vyberte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="70ab6-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="70ab6-113">Vyberte dotaz, který chcete použít pro toto pravidlo.</span><span class="sxs-lookup"><span data-stu-id="70ab6-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="70ab6-114">V seznamu **Název pravidla členství** klikněte na odkaz ve vybraném řádku.</span><span class="sxs-lookup"><span data-stu-id="70ab6-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="70ab6-115">Klikněte na **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="70ab6-115">Click **Edit query**.</span></span> <span data-ttu-id="70ab6-116">Podle potřeby upravte dotaz.</span><span class="sxs-lookup"><span data-stu-id="70ab6-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="70ab6-117">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="70ab6-117">Click **OK**.</span></span>
8. <span data-ttu-id="70ab6-118">Klikněte na **Spustit automatické přiřazení role**.</span><span class="sxs-lookup"><span data-stu-id="70ab6-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="70ab6-119">Přejděte na **Navigační podokno > Moduly > Správa systému > Uživatelé > Uživatelé** (nejlépe na kartě samostatného prohlížeče).</span><span class="sxs-lookup"><span data-stu-id="70ab6-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="70ab6-120">Zkontrolujte role přiřazené různým uživatelům a potvrďte, že dotaz na přiřazení role byl správný.</span><span class="sxs-lookup"><span data-stu-id="70ab6-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="70ab6-121">V případě potřeby je upravte a spusťte znovu.</span><span class="sxs-lookup"><span data-stu-id="70ab6-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="70ab6-122">Vyloučení uživatelů z automatického přiřazení k roli</span><span class="sxs-lookup"><span data-stu-id="70ab6-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="70ab6-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="70ab6-123">Close the page.</span></span>
2. <span data-ttu-id="70ab6-124">Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.</span><span class="sxs-lookup"><span data-stu-id="70ab6-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="70ab6-125">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="70ab6-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="70ab6-126">Vyberte požadovanou roli.</span><span class="sxs-lookup"><span data-stu-id="70ab6-126">Select a role.</span></span> <span data-ttu-id="70ab6-127">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="70ab6-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="70ab6-128">V nabídce **role přiřazené uživatelům** vyberte možnost **Ručně přiřadit nebo vyloučit uživatele.**</span><span class="sxs-lookup"><span data-stu-id="70ab6-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="70ab6-129">V seznamu **Přiřadit nebo nebo vyloučit uživatele z role** vyberte vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="70ab6-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="70ab6-130">Vyberte uživatele.</span><span class="sxs-lookup"><span data-stu-id="70ab6-130">Select a user.</span></span>  
6. <span data-ttu-id="70ab6-131">V **podokně akcí** vyberte možnost **Vyloučit z role**.</span><span class="sxs-lookup"><span data-stu-id="70ab6-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="70ab6-132">Kliknutím na **Vyloučit z role** vyloučíte vybrané uživatele z role.</span><span class="sxs-lookup"><span data-stu-id="70ab6-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="70ab6-133">Pokud chcete vyloučení odebrat, vyberte uživatele, pro kterého chcete vyloučení odebrat, a klepněte na tlačítko **Vynulovat stav**.</span><span class="sxs-lookup"><span data-stu-id="70ab6-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="70ab6-134">Při odebírání vyloučení obnovením stavu uživatele se role uživatele znovu automaticky přiřadí.</span><span class="sxs-lookup"><span data-stu-id="70ab6-134">When you remove an exclusion by resetting the user's status, the user's role is again assigned automatically.</span></span> <span data-ttu-id="70ab6-135">Uživatel však při vynulování stavu není okamžitě přiřazen k roli nebo z ní vyloučen.</span><span class="sxs-lookup"><span data-stu-id="70ab6-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="70ab6-136">Místo toho je uživateli přiřazena role nebo je z role odebrán při příštím spuštění pravidel pro automatické přiřazení role.</span><span class="sxs-lookup"><span data-stu-id="70ab6-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

---
title: Přiřazení uživatelů k rolím zabezpečení
description: Pro přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations Enterprise edition musí být uživateli přiřazeni k rolím zabezpečení.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851352"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="e5be3-103">Přiřazení uživatelů k rolím zabezpečení</span><span class="sxs-lookup"><span data-stu-id="e5be3-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5be3-104">Pro přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations Enterprise edition musí být uživateli přiřazeni k rolím zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="e5be3-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="e5be3-105">Tento postup vysvětluje způsob, jakým správce systému může přiřadit uživatele k rolím automaticky na základě obchodních dat.</span><span class="sxs-lookup"><span data-stu-id="e5be3-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="e5be3-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e5be3-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="e5be3-107">Automatické přiřazení uživatelů k rolím</span><span class="sxs-lookup"><span data-stu-id="e5be3-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="e5be3-108">Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.</span><span class="sxs-lookup"><span data-stu-id="e5be3-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="e5be3-109">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="e5be3-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="e5be3-110">Vyberte roli, pro kterou chcete konfigurovat pravidlo.</span><span class="sxs-lookup"><span data-stu-id="e5be3-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="e5be3-111">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="e5be3-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="e5be3-112">Kliknutím na možnost **Přidat pravidlo** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e5be3-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="e5be3-113">V seznamu **Vybrat dotaz** najděte a vyberte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="e5be3-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="e5be3-114">Vyberte dotaz, který chcete použít pro toto pravidlo.</span><span class="sxs-lookup"><span data-stu-id="e5be3-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="e5be3-115">V seznamu **Název pravidla členství** klikněte na odkaz ve vybraném řádku.</span><span class="sxs-lookup"><span data-stu-id="e5be3-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e5be3-116">Klikněte na **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="e5be3-116">Click **Edit query**.</span></span> <span data-ttu-id="e5be3-117">Podle potřeby upravte dotaz.</span><span class="sxs-lookup"><span data-stu-id="e5be3-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="e5be3-118">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e5be3-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="e5be3-119">Vyloučení uživatelů z automatického přiřazení k roli</span><span class="sxs-lookup"><span data-stu-id="e5be3-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="e5be3-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e5be3-120">Close the page.</span></span>
2. <span data-ttu-id="e5be3-121">Přejděte do **Navigačního podokna > Moduly > Správa systému > Zabezpečení > Přiřadit uživatele k rolím**.</span><span class="sxs-lookup"><span data-stu-id="e5be3-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="e5be3-122">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="e5be3-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="e5be3-123">Vyberte požadovanou roli.</span><span class="sxs-lookup"><span data-stu-id="e5be3-123">Select a role.</span></span> <span data-ttu-id="e5be3-124">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="e5be3-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="e5be3-125">V nabídce **role přiřazené uživatelům** vyberte možnost **Ručně přiřadit nebo vyloučit uživatele.**</span><span class="sxs-lookup"><span data-stu-id="e5be3-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="e5be3-126">V seznamu **Přiřadit nebo nebo vyloučit uživatele z role** vyberte vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="e5be3-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="e5be3-127">Vyberte uživatele.</span><span class="sxs-lookup"><span data-stu-id="e5be3-127">Select a user.</span></span>  
6. <span data-ttu-id="e5be3-128">V **podokně akcí** vyberte možnost **Vyloučit z role**.</span><span class="sxs-lookup"><span data-stu-id="e5be3-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="e5be3-129">Kliknutím na **Vyloučit z role** vyloučíte vybrané uživatele z role.</span><span class="sxs-lookup"><span data-stu-id="e5be3-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="e5be3-130">Pokud chcete vyloučení odebrat, vyberte uživatele, pro kterého chcete vyloučení odebrat, a klepněte na tlačítko **Vynulovat stav**.</span><span class="sxs-lookup"><span data-stu-id="e5be3-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="e5be3-131">Při odebírání vyloučení obnovením stavu uživatele se role uživatele znovu automaticky přiřadí.</span><span class="sxs-lookup"><span data-stu-id="e5be3-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="e5be3-132">Uživatel však při vynulování stavu není okamžitě přiřazen k roli nebo z ní vyloučen.</span><span class="sxs-lookup"><span data-stu-id="e5be3-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="e5be3-133">Místo toho je uživateli přiřazena role nebo je z role odebrán při příštím spuštění pravidel pro automatické přiřazení role.</span><span class="sxs-lookup"><span data-stu-id="e5be3-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

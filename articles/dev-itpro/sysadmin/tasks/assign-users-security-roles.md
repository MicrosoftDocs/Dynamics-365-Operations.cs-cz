---
title: Přiřazení uživatelů k rolím zabezpečení
description: Pro přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations Enterprise edition musí být uživateli přiřazeni k rolím zabezpečení.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556702"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="c4012-103">Přiřazení uživatelů k rolím zabezpečení</span><span class="sxs-lookup"><span data-stu-id="c4012-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4012-104">Pro přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations Enterprise edition musí být uživateli přiřazeni k rolím zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="c4012-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="c4012-105">Tento postup vysvětluje způsob, jakým správce systému může přiřadit uživatele k rolím automaticky na základě obchodních dat.</span><span class="sxs-lookup"><span data-stu-id="c4012-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="c4012-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="c4012-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="c4012-107">Automatické přiřazení uživatelů k rolím</span><span class="sxs-lookup"><span data-stu-id="c4012-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="c4012-108">Přejděte na Správa systému > Zabezpečení > Přiřadit uživatele k rolím.</span><span class="sxs-lookup"><span data-stu-id="c4012-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="c4012-109">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="c4012-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="c4012-110">Vyberte roli, pro kterou chcete konfigurovat pravidlo.</span><span class="sxs-lookup"><span data-stu-id="c4012-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="c4012-111">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="c4012-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="c4012-112">Klepnutím na možnost Přidat pravidlo otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c4012-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="c4012-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c4012-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c4012-114">Vyberte dotaz, který chcete použít pro toto pravidlo.</span><span class="sxs-lookup"><span data-stu-id="c4012-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="c4012-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c4012-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c4012-116">Klikněte na možnost Upravit dotaz.</span><span class="sxs-lookup"><span data-stu-id="c4012-116">Click Edit query.</span></span>
    * <span data-ttu-id="c4012-117">Podle potřeby upravte dotaz.</span><span class="sxs-lookup"><span data-stu-id="c4012-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="c4012-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c4012-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="c4012-119">Vyloučení uživatelů z automatického přiřazení k roli</span><span class="sxs-lookup"><span data-stu-id="c4012-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="c4012-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c4012-120">Close the page.</span></span>
2. <span data-ttu-id="c4012-121">Přejděte na Správa systému > Zabezpečení > Přiřadit uživatele k rolím.</span><span class="sxs-lookup"><span data-stu-id="c4012-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="c4012-122">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="c4012-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="c4012-123">Vyberte požadovanou roli.</span><span class="sxs-lookup"><span data-stu-id="c4012-123">Select a role.</span></span> <span data-ttu-id="c4012-124">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="c4012-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="c4012-125">Klikněte na Ručně přiřadit nebo vyloučit uživatele.</span><span class="sxs-lookup"><span data-stu-id="c4012-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="c4012-126">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="c4012-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c4012-127">Vyberte uživatele.</span><span class="sxs-lookup"><span data-stu-id="c4012-127">Select a user.</span></span>  
6. <span data-ttu-id="c4012-128">Klikněte na Vyloučit z role.</span><span class="sxs-lookup"><span data-stu-id="c4012-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="c4012-129">Kliknutím na Vyloučit z role vyloučíte vybrané uživatele z role.</span><span class="sxs-lookup"><span data-stu-id="c4012-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="c4012-130">Pokud chcete vyloučení odebrat, vyberte uživatele, pro kterého chcete vyloučení odebrat, a klepněte na tlačítko Vynulovat stav.</span><span class="sxs-lookup"><span data-stu-id="c4012-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="c4012-131">Při odebírání vyloučení obnovením stavu uživatele se role uživatele znovu automaticky přiřadí.</span><span class="sxs-lookup"><span data-stu-id="c4012-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="c4012-132">Uživatel však při vynulování stavu není okamžitě přiřazen k roli nebo z ní vyloučen.</span><span class="sxs-lookup"><span data-stu-id="c4012-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="c4012-133">Místo toho je uživateli přiřazena role nebo je z role odebrán při příštím spuštění pravidel pro automatické přiřazení role.</span><span class="sxs-lookup"><span data-stu-id="c4012-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


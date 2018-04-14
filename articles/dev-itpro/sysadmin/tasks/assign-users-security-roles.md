--- 
title: "Přiřadit uživatelů k rolím zabezpečení"
description: "Uživatelé musí být přiřazeni k rolím zabezpečení, aby měli přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c7f35f57223798e91fc2a81c0821a2dc81512624
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="3a0da-103">Přiřazení uživatelů k rolím zabezpečení</span><span class="sxs-lookup"><span data-stu-id="3a0da-103">Assign users to security roles</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a0da-104">Uživatelé musí být přiřazeni k rolím zabezpečení, aby měli přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3a0da-104">To access Microsoft Dynamics 365 for Finance and Operations, users must be assigned to security roles.</span></span> <span data-ttu-id="3a0da-105">Tento postup vysvětluje způsob, jakým správce systému může přiřadit uživatele k rolím automaticky na základě obchodních dat.</span><span class="sxs-lookup"><span data-stu-id="3a0da-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="3a0da-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="3a0da-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="3a0da-107">Automatické přiřazení uživatelů k rolím</span><span class="sxs-lookup"><span data-stu-id="3a0da-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="3a0da-108">Přejděte na Správa systému > Zabezpečení > Přiřadit uživatele k rolím.</span><span class="sxs-lookup"><span data-stu-id="3a0da-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="3a0da-109">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="3a0da-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="3a0da-110">Vyberte roli, pro kterou chcete konfigurovat pravidlo.</span><span class="sxs-lookup"><span data-stu-id="3a0da-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="3a0da-111">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="3a0da-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="3a0da-112">Klepnutím na možnost Přidat pravidlo otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="3a0da-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="3a0da-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="3a0da-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a0da-114">Vyberte dotaz, který chcete použít pro toto pravidlo.</span><span class="sxs-lookup"><span data-stu-id="3a0da-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="3a0da-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="3a0da-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3a0da-116">Klikněte na možnost Upravit dotaz.</span><span class="sxs-lookup"><span data-stu-id="3a0da-116">Click Edit query.</span></span>
    * <span data-ttu-id="3a0da-117">Podle potřeby upravte dotaz.</span><span class="sxs-lookup"><span data-stu-id="3a0da-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="3a0da-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="3a0da-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="3a0da-119">Vyloučení uživatelů z automatického přiřazení k roli</span><span class="sxs-lookup"><span data-stu-id="3a0da-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="3a0da-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3a0da-120">Close the page.</span></span>
2. <span data-ttu-id="3a0da-121">Přejděte na Správa systému > Zabezpečení > Přiřadit uživatele k rolím.</span><span class="sxs-lookup"><span data-stu-id="3a0da-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="3a0da-122">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="3a0da-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="3a0da-123">Vyberte požadovanou roli.</span><span class="sxs-lookup"><span data-stu-id="3a0da-123">Select a role.</span></span> <span data-ttu-id="3a0da-124">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="3a0da-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="3a0da-125">Klikněte na Ručně přiřadit nebo vyloučit uživatele.</span><span class="sxs-lookup"><span data-stu-id="3a0da-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="3a0da-126">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="3a0da-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3a0da-127">Vyberte uživatele.</span><span class="sxs-lookup"><span data-stu-id="3a0da-127">Select a user.</span></span>  
6. <span data-ttu-id="3a0da-128">Klikněte na Vyloučit z role.</span><span class="sxs-lookup"><span data-stu-id="3a0da-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="3a0da-129">Kliknutím na Vyloučit z role vyloučíte vybrané uživatele z role.</span><span class="sxs-lookup"><span data-stu-id="3a0da-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="3a0da-130">Pokud chcete vyloučení odebrat, vyberte uživatele, pro kterého chcete vyloučení odebrat, a klepněte na tlačítko Vynulovat stav.</span><span class="sxs-lookup"><span data-stu-id="3a0da-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="3a0da-131">Při odebírání vyloučení obnovením stavu uživatele se role uživatele znovu automaticky přiřadí.</span><span class="sxs-lookup"><span data-stu-id="3a0da-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="3a0da-132">Uživatel však při vynulování stavu není okamžitě přiřazen k roli nebo z ní vyloučen.</span><span class="sxs-lookup"><span data-stu-id="3a0da-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="3a0da-133">Místo toho je uživateli přiřazena role nebo je z role odebrán při příštím spuštění pravidel pro automatické přiřazení role.</span><span class="sxs-lookup"><span data-stu-id="3a0da-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  



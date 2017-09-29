--- 
title: "Přiřadit uživatelů k rolím zabezpečení"
description: "Uživatelé musí být přiřazeni k rolím zabezpečení, aby měli přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations, edice Enterprise."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 551048af26f46d334c562d1968963aed262a5e03
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="341ab-103">Přiřadit uživatelů k rolím zabezpečení</span><span class="sxs-lookup"><span data-stu-id="341ab-103">Assign users to security roles</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="341ab-104">Uživatelé musí být přiřazeni k rolím zabezpečení, aby měli přístup k aplikaci Microsoft Dynamics 365 for Finance and Operations, edice Enterprise.</span><span class="sxs-lookup"><span data-stu-id="341ab-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="341ab-105">Tento postup vysvětluje způsob, jakým správce systému může přiřadit uživatele k rolím automaticky na základě obchodních dat.</span><span class="sxs-lookup"><span data-stu-id="341ab-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="341ab-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="341ab-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="341ab-107">Automatické přiřazení uživatelů k rolím</span><span class="sxs-lookup"><span data-stu-id="341ab-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="341ab-108">Přejděte na Správa systému > Zabezpečení > Přiřadit uživatele k rolím.</span><span class="sxs-lookup"><span data-stu-id="341ab-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="341ab-109">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="341ab-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="341ab-110">Vyberte roli, pro kterou chcete konfigurovat pravidlo.</span><span class="sxs-lookup"><span data-stu-id="341ab-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="341ab-111">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="341ab-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="341ab-112">Klepnutím na možnost Přidat pravidlo otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="341ab-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="341ab-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="341ab-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="341ab-114">Vyberte dotaz, který chcete použít pro toto pravidlo.</span><span class="sxs-lookup"><span data-stu-id="341ab-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="341ab-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="341ab-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="341ab-116">Klikněte na možnost Upravit dotaz.</span><span class="sxs-lookup"><span data-stu-id="341ab-116">Click Edit query.</span></span>
    * <span data-ttu-id="341ab-117">Podle potřeby upravte dotaz.</span><span class="sxs-lookup"><span data-stu-id="341ab-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="341ab-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="341ab-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="341ab-119">Vyloučení uživatelů z automatického přiřazení k roli</span><span class="sxs-lookup"><span data-stu-id="341ab-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="341ab-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="341ab-120">Close the page.</span></span>
2. <span data-ttu-id="341ab-121">Přejděte na Správa systému > Zabezpečení > Přiřadit uživatele k rolím.</span><span class="sxs-lookup"><span data-stu-id="341ab-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="341ab-122">Ve stromovém zobrazení vyberte „Vedoucí účetní“.</span><span class="sxs-lookup"><span data-stu-id="341ab-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="341ab-123">Vyberte požadovanou roli.</span><span class="sxs-lookup"><span data-stu-id="341ab-123">Select a role.</span></span> <span data-ttu-id="341ab-124">V tomto příkladu vyberte vedoucí účetní.</span><span class="sxs-lookup"><span data-stu-id="341ab-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="341ab-125">Klikněte na Ručně přiřadit nebo vyloučit uživatele.</span><span class="sxs-lookup"><span data-stu-id="341ab-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="341ab-126">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="341ab-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="341ab-127">Vyberte uživatele.</span><span class="sxs-lookup"><span data-stu-id="341ab-127">Select a user.</span></span>  
6. <span data-ttu-id="341ab-128">Klikněte na Vyloučit z role.</span><span class="sxs-lookup"><span data-stu-id="341ab-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="341ab-129">Kliknutím na Vyloučit z role vyloučíte vybrané uživatele z role.</span><span class="sxs-lookup"><span data-stu-id="341ab-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="341ab-130">Pokud chcete vyloučení odebrat, vyberte uživatele, pro kterého chcete vyloučení odebrat, a klepněte na tlačítko Vynulovat stav.</span><span class="sxs-lookup"><span data-stu-id="341ab-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="341ab-131">Při odebírání vyloučení obnovením stavu uživatele se role uživatele znovu automaticky přiřadí.</span><span class="sxs-lookup"><span data-stu-id="341ab-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="341ab-132">Uživatel však při vynulování stavu není okamžitě přiřazen k roli nebo z ní vyloučen.</span><span class="sxs-lookup"><span data-stu-id="341ab-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="341ab-133">Místo toho je uživateli přiřazena role nebo je z role odebrán při příštím spuštění pravidel pro automatické přiřazení role.</span><span class="sxs-lookup"><span data-stu-id="341ab-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  



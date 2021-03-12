---
title: Identifikace a vyřešení konfliktů v dělení zodpovědnosti
description: Toto téma vysvětluje, jak identifikovat a vyřešit konflikty v dělení zodpovědnosti.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deff97c7728db91089d3ea834d15de738da500fa
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826361"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="6933b-103">Identifikace a vyřešení konfliktů v dělení zodpovědnosti</span><span class="sxs-lookup"><span data-stu-id="6933b-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6933b-104">Toto téma vysvětluje, jak identifikovat a vyřešit konflikty v dělení zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="6933b-104">This topic explains how to identify and resolve conflicts in segregation of duties.</span></span> <span data-ttu-id="6933b-105">Můžete nastavit pravidla k oddělení zodpovědností, které musí být prováděny různými uživateli.</span><span class="sxs-lookup"><span data-stu-id="6933b-105">You can set up rules to separate duties that must be performed by different users.</span></span> <span data-ttu-id="6933b-106">Tento koncept se nazývá dělení zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="6933b-106">This concept is named segregation of duties.</span></span> <span data-ttu-id="6933b-107">Pokud definice role zabezpečení nebo přiřazení role uživatele porušuje pravidla, konflikt je zaznamenán.</span><span class="sxs-lookup"><span data-stu-id="6933b-107">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="6933b-108">Všechny konflikty musí vyřešit správce.</span><span class="sxs-lookup"><span data-stu-id="6933b-108">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="6933b-109">Chcete-li zjistit a vyřešit konflikty, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="6933b-109">Complete the following procedure to identify and resolve conflicts.</span></span>

<span data-ttu-id="6933b-110">Po přidání pravidla ověřte, zda jsou všechny existující role kompatibilní.</span><span class="sxs-lookup"><span data-stu-id="6933b-110">After a rule has been added, verify that all existing roles are compliant.</span></span> 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="6933b-111">Ověření, zda existující role a zodpovědnosti vyhovují novým pravidlům pro dělení zodpovědnosti</span><span class="sxs-lookup"><span data-stu-id="6933b-111">Verify that existing roles and duties comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="6933b-112">Přejděte do nabídky **Správa systému** > **Zabezpečení** > **Dělení zodpovědnosti** > **Pravidla dělení zodpovědnosti**.</span><span class="sxs-lookup"><span data-stu-id="6933b-112">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
3. <span data-ttu-id="6933b-113">Zvolte **Ověřit zodpovědnosti a role**.</span><span class="sxs-lookup"><span data-stu-id="6933b-113">Select **Validate duties and roles**.</span></span> <span data-ttu-id="6933b-114">Pokud jakákoli role porušila pravidla, zobrazí se zpráva obsahující název pravidla, roli a názvy konfliktních zodpovědností.</span><span class="sxs-lookup"><span data-stu-id="6933b-114">If any roles violate the rules, a message is displayed that contains the name of the rule, the role, and the names of the conflicting duties.</span></span> <span data-ttu-id="6933b-115">Konfliktní role musí být upraveny pomocí **Konfigurace zabezpečení** a nemůže zahrnovat konfliktní zodpovědnosti.</span><span class="sxs-lookup"><span data-stu-id="6933b-115">Conflicting roles must be modified using **Security configuration** and can't include conflicting duties.</span></span> <span data-ttu-id="6933b-116">Pokud vybrané pravidlo není porušeno žádnou rolí, zpráva zobrazí informaci, že všechny role jsou kompatibilní.</span><span class="sxs-lookup"><span data-stu-id="6933b-116">If no roles violate the selected rule, a message indicates that all roles comply.</span></span>   

> [!NOTE]
> <span data-ttu-id="6933b-117">Ověření se provádí pouze pro vybrané pravidlo.</span><span class="sxs-lookup"><span data-stu-id="6933b-117">The validation is only performed for the selected rule.</span></span> <span data-ttu-id="6933b-118">Je důležité ověřit dodržování předpisů pro každé pravidlo.</span><span class="sxs-lookup"><span data-stu-id="6933b-118">It is important to validate compliance for each rule.</span></span>   

<span data-ttu-id="6933b-119">Když vytvoříte nebo upravíte roli, pravidla pro oddělení povinností se automaticky vynucují.</span><span class="sxs-lookup"><span data-stu-id="6933b-119">When you create or modify a role, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="6933b-120">Roli nemůžete přiřadit konfliktní povinnosti.</span><span class="sxs-lookup"><span data-stu-id="6933b-120">You cannot assign conflicting duties to a role.</span></span>

<span data-ttu-id="6933b-121">Dále ověřte, zda jsou všechna existující přiřazení rolí kompatibilní.</span><span class="sxs-lookup"><span data-stu-id="6933b-121">Next, verify that all existing role assignments are compliant.</span></span>

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="6933b-122">Ověření, zda přiřazení rolí uživatelů vyhovují novým pravidlům pro dělení zodpovědnosti</span><span class="sxs-lookup"><span data-stu-id="6933b-122">Verify that user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="6933b-123">Přejděte do nabídky **Správa systému > Zabezpečení > Dělení zodpovědnosti > Ověřit plnění přiřazení role uživatele**.</span><span class="sxs-lookup"><span data-stu-id="6933b-123">Go to **System administration > Security > Segregation of duties > Verify compliance of user-role assignments**.</span></span>
2. <span data-ttu-id="6933b-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="6933b-124">Select **OK**.</span></span> <span data-ttu-id="6933b-125">Oznámení zobrazí výsledky ověření.</span><span class="sxs-lookup"><span data-stu-id="6933b-125">A notification displays the results of the validation.</span></span> <span data-ttu-id="6933b-126">Konflikty jsou zaznamenávány na stránce **Nevyřešené konflikty dělení zodpovědnosti**.</span><span class="sxs-lookup"><span data-stu-id="6933b-126">Conflicts are logged on the **Segregation of duties unresolved conflicts** page.</span></span>   

<span data-ttu-id="6933b-127">Když přiřadíte uživatele rolím, pravidla pro dělení zodpovědnosti se automaticky vynucují.</span><span class="sxs-lookup"><span data-stu-id="6933b-127">When you assign users to roles, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="6933b-128">Pokud se pokusíte přiřadit uživatele k rolím, které obsahují konfliktní povinnosti, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="6933b-128">If you try to assign a user to roles that contain conflicting duties, you receive an error message.</span></span> <span data-ttu-id="6933b-129">Poté musíte konflikt vyřešit odmítnutím nebo povolením dalšího přiřazení role.</span><span class="sxs-lookup"><span data-stu-id="6933b-129">You must then resolve the conflict by denying or allowing the additional role assignment.</span></span> <span data-ttu-id="6933b-130">Další role bude přidělena po povolení přiřazení.</span><span class="sxs-lookup"><span data-stu-id="6933b-130">The additional role will be assigned after the assignment is allowed.</span></span> 

> [!NOTE]
> <span data-ttu-id="6933b-131">Konflikty nejsou aktuálně ověřeny pro uživatele, kterým jsou přiřazeny role na základě skupin domén služby Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6933b-131">Conflicts are currently not verified for users that are assigned roles based on the Active Directory Domain groups.</span></span>

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="6933b-132">Zobrazení a vyřešení konfliktních přiřazení rolí uživatelů</span><span class="sxs-lookup"><span data-stu-id="6933b-132">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="6933b-133">Přejděte do nabídky **Správa systému** > **Zabezpečení** > **Dělení zodpovědnosti** > **Nevyřešené konflikty dělení zodpovědnosti**.</span><span class="sxs-lookup"><span data-stu-id="6933b-133">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties unresolved conflicts**.</span></span> 
2. <span data-ttu-id="6933b-134">Vyberte konflikt a vyberte některou z následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="6933b-134">Select a conflict, and then select one of the following actions:</span></span> 

  - <span data-ttu-id="6933b-135">**Odepřít přiřazení** – Odepře přiřazení uživatele k další roli zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="6933b-135">**Deny assignment**: This will deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="6933b-136">Pokud odmítnete automatické přiřazení role, uživatel bude označen jako vyloučený z role.</span><span class="sxs-lookup"><span data-stu-id="6933b-136">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="6933b-137">Vyloučenému uživateli není udělen přístup, který je přidružený k roli, a uživatel nemůže být přiřazen k roli, dokud správce vyloučení neodstraní.</span><span class="sxs-lookup"><span data-stu-id="6933b-137">The excluded user isn't granted the access associated with the role and can't be assigned to the role until the administrator removes the exclusion.</span></span> 
-  <span data-ttu-id="6933b-138">**Povolit přiřazení** Přepíše konflikt a povolí přiřazení uživatele k další roli zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="6933b-138">**Allow assignment**: This will override the conflict and allow the user to be assigned to the additional security role.</span></span> <span data-ttu-id="6933b-139">Pokud přepíšete konflikt, je nutné zadat důvod do pole **Důvod pro přepsání**.</span><span class="sxs-lookup"><span data-stu-id="6933b-139">If you override a conflict, you must enter a reason in the **Reason for override** field.</span></span> <span data-ttu-id="6933b-140">Všechna přepsaná přiřazení rolí lze zobrazit na stránce **Rozdělení konfliktů povinností**.</span><span class="sxs-lookup"><span data-stu-id="6933b-140">All overridden role assignments can be viewed on the **Segregation of duties conflicts** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="6933b-141">Pokud je u stejného uživatele uvedeno několik konfliktů, vyberte záznam uživatele a vyhodnoťte přiřazené role na stránce **Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="6933b-141">If several conflicts are listed for the same user, select the user record and evaluate assigned roles on the **Users** page.</span></span> <span data-ttu-id="6933b-142">Abyste se tomuto konfliktu vyhnuli, ověřte každé pravidlo po jeho přidání nebo úpravě.</span><span class="sxs-lookup"><span data-stu-id="6933b-142">To avoid this conflict, validate each rule after it's added or modified.</span></span>

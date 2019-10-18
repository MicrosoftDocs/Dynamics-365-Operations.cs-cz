---
title: Vytvoření nových uživatelů
description: Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
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
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180937"
---
# <a name="create-new-users"></a><span data-ttu-id="4fbb7-103">Vytvoření nových uživatelů</span><span class="sxs-lookup"><span data-stu-id="4fbb7-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4fbb7-104">Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="4fbb7-105">Přiřazení uživatele k licenci (pouze nové typy licencí)</span><span class="sxs-lookup"><span data-stu-id="4fbb7-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="4fbb7-106">Pro zákazníky, kteří se nacházejí v jednom z nových typů licencí, které byly přidány v říjnu 2019, je nutné, aby byli uživatelé přiřazeni k licenci.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="4fbb7-107">Uživatelé, kteří jsou přiřazeni k licenci, jsou automaticky přidáni jako uživatelé systému, kteří při prvním přihlášení nemají žádné role.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="4fbb7-108">Uživatelé, kteří nejsou přidruženi k licenci, obdrží zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="4fbb7-109">Správci systému mohou [přiřazovat licence uživatelům](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) v [centru správy Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="4fbb7-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="4fbb7-110">Přidat nového uživatele</span><span class="sxs-lookup"><span data-stu-id="4fbb7-110">Add a new user</span></span>
1. <span data-ttu-id="4fbb7-111">Přejděte do nabídky **Správa systému \> Uživatelé \> Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="4fbb7-112">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="4fbb7-113">Do pole **ID uživatele** zadejte jedinečný identifikátor uživatele.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="4fbb7-114">ID uživatele je povinné.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-114">A user ID is required.</span></span>  
4. <span data-ttu-id="4fbb7-115">Do pole **Jméno uživatele** zadejte jméno uživatele.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="4fbb7-116">Do pole **Doména** zadejte doménu daného uživatele.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="4fbb7-117">Do pole **Alias** zadejte alias uživatele.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="4fbb7-118">V poli **Společnost** zvolte požadovanou společnost.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="4fbb7-119">Na pevné záložce **Role uživatele** vyberte možnost **Přiřadit role** a [přiřaďte je uživatelům k rolím zabezpečení](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="4fbb7-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="4fbb7-120">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-120">Select **OK**.</span></span>
10. <span data-ttu-id="4fbb7-121">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="4fbb7-122">Importovat uživatele</span><span class="sxs-lookup"><span data-stu-id="4fbb7-122">Import users</span></span>
1. <span data-ttu-id="4fbb7-123">V podokně akcí klikněte na možnost **Import uživatele**.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="4fbb7-124">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4fbb7-125">Vybrat **Importovat uživatele**.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-125">Select **Import users**.</span></span>
4. <span data-ttu-id="4fbb7-126">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="4fbb7-126">Select **Close**.</span></span>


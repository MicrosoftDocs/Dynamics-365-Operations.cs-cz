---
title: Vytvoření nových uživatelů
description: Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e84130ff2b1cf83b7d2b95eefc72175dc57743c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982495"
---
# <a name="create-new-users"></a><span data-ttu-id="58225-103">Vytvoření nových uživatelů</span><span class="sxs-lookup"><span data-stu-id="58225-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58225-104">Uživatelé jsou interní zaměstnanci ve vaší organizaci nebo externí zákazníci a dodavatelé, kteří v rámci své práce vyžadují přístup k systému.</span><span class="sxs-lookup"><span data-stu-id="58225-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="58225-105">Přiřazení uživatele k licenci (pouze nové typy licencí)</span><span class="sxs-lookup"><span data-stu-id="58225-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="58225-106">Pro zákazníky, kteří se nacházejí v jednom z nových typů licencí, které byly přidány v říjnu 2019, je nutné, aby byli uživatelé přiřazeni k licenci.</span><span class="sxs-lookup"><span data-stu-id="58225-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="58225-107">Uživatelé, kteří jsou přiřazeni k licenci, jsou automaticky přidáni jako uživatelé systému, kteří při prvním přihlášení nemají žádné role.</span><span class="sxs-lookup"><span data-stu-id="58225-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="58225-108">Správci systému mohou [přiřazovat licence uživatelům](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) v [centru správy Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="58225-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="58225-109">Přiřazení externího uživatele k licenci (pouze nové typy licencí)</span><span class="sxs-lookup"><span data-stu-id="58225-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="58225-110">Uživatelé, kteří jsou externí vůči klientovi, do kterého bylo prostředí nasazeno, je třeba reprezentovat v adresáři hostitelského klienta (Azure Active Directory (Azure AD)), aby jim mohly být přiřazeny licence.</span><span class="sxs-lookup"><span data-stu-id="58225-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="58225-111">Tito externí uživatelé by měli být přidáni do klienta v Azure AD jako uživatelé typu Host a poté jim přiřazovat příslušné licence.</span><span class="sxs-lookup"><span data-stu-id="58225-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="58225-112">Další informace naleznete v tématu [Přidání uživatelů spolupráce B2B Azure Active Directory na portálu Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="58225-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="58225-113">Přidat nového uživatele</span><span class="sxs-lookup"><span data-stu-id="58225-113">Add a new user</span></span>
1. <span data-ttu-id="58225-114">Přejděte do nabídky **Správa systému \> Uživatelé \> Uživatelé** .</span><span class="sxs-lookup"><span data-stu-id="58225-114">Go to **System administration \> Users \> Users** .</span></span>
2. <span data-ttu-id="58225-115">V podokně akcí zvolte **Nový** .</span><span class="sxs-lookup"><span data-stu-id="58225-115">On the Action Pane, select **New** .</span></span>
3. <span data-ttu-id="58225-116">Do pole **ID uživatele** zadejte jedinečný identifikátor uživatele.</span><span class="sxs-lookup"><span data-stu-id="58225-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="58225-117">ID uživatele je povinné.</span><span class="sxs-lookup"><span data-stu-id="58225-117">A user ID is required.</span></span>  
4. <span data-ttu-id="58225-118">Do pole **Jméno uživatele** zadejte jméno uživatele.</span><span class="sxs-lookup"><span data-stu-id="58225-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="58225-119">Do pole **Doména** zadejte doménu daného uživatele.</span><span class="sxs-lookup"><span data-stu-id="58225-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="58225-120">Do pole **Alias** zadejte alias uživatele.</span><span class="sxs-lookup"><span data-stu-id="58225-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="58225-121">V poli **Společnost** zvolte požadovanou společnost.</span><span class="sxs-lookup"><span data-stu-id="58225-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="58225-122">Na pevné kartě **Role uživatele** vyberte možnost **Přiřadit role** , chcete-li uživatelům přiřadit role zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="58225-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="58225-123">Další informace viz [Přiřadit uživatelům role zabezpečení](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="58225-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="58225-124">Vyberte **OK** .</span><span class="sxs-lookup"><span data-stu-id="58225-124">Select **OK** .</span></span>
10. <span data-ttu-id="58225-125">Zvolte **Uložit** .</span><span class="sxs-lookup"><span data-stu-id="58225-125">Select **Save** .</span></span>

## <a name="import-users"></a><span data-ttu-id="58225-126">Importovat uživatele</span><span class="sxs-lookup"><span data-stu-id="58225-126">Import users</span></span>
1. <span data-ttu-id="58225-127">Přejděte do nabídky **Správa systému \> Uživatelé \> Uživatelé** .</span><span class="sxs-lookup"><span data-stu-id="58225-127">Go to **System administration \> Users \> Users** .</span></span>
2. <span data-ttu-id="58225-128">V podokně akcí klikněte na možnost **Import uživatele** .</span><span class="sxs-lookup"><span data-stu-id="58225-128">On the Action Pane, select **Import users** .</span></span>
3. <span data-ttu-id="58225-129">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="58225-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="58225-130">Vybrat **Importovat uživatele** .</span><span class="sxs-lookup"><span data-stu-id="58225-130">Select **Import users** .</span></span>
5. <span data-ttu-id="58225-131">Vyberte **Zavřít** .</span><span class="sxs-lookup"><span data-stu-id="58225-131">Select **Close** .</span></span>


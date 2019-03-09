---
title: Uživatel nebyl nalezen v nástroji pro výběr osob v aplikacích Attract nebo Onboard
description: Toto téma vysvětluje, jak postupovat, když se uživatelé v klientovi společnosti nezobrazují v nástroji pro výběr osob v aplikacích Dynamics 365 for Talent Attract nebo Onboard.
author: ChrisChua
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: chrichua
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2d4a74ee2cc65153c1f9fdc1b42c2fc440d188d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303638"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="b42ad-103">Uživatelé Azure Active Directory nenalezení v nástroji pro výběr osob</span><span class="sxs-lookup"><span data-stu-id="b42ad-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="b42ad-104">Výdej</span><span class="sxs-lookup"><span data-stu-id="b42ad-104">Issue</span></span>

<span data-ttu-id="b42ad-105">Někteří platní uživatelé v aplikaci Microsoft Azure Active Directory (Azure AD) pro klienta se nezobrazují při hledání jména v nástroji pro výběr osob v aplikacích Dynamics 365 for Talent Attract nebo Onboard.</span><span class="sxs-lookup"><span data-stu-id="b42ad-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in the Dynamics 365 for Talent Attract or Onboard applications.</span></span>

## <a name="cause"></a><span data-ttu-id="b42ad-106">Příčina</span><span class="sxs-lookup"><span data-stu-id="b42ad-106">Cause</span></span>

<span data-ttu-id="b42ad-107">Některé typy uživatelů nejsou aktuálně podporovány v aplikacích Attract či Onboard.</span><span class="sxs-lookup"><span data-stu-id="b42ad-107">Certain user types are not currently supported in the Attract and Onboard applications.</span></span> <span data-ttu-id="b42ad-108">Ověřte, zda uživatel není typem hosta Azure AD B2B.</span><span class="sxs-lookup"><span data-stu-id="b42ad-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="b42ad-109">Informace o typu uživatele lze najít v listu Azure Active Directory na portálu Azure.</span><span class="sxs-lookup"><span data-stu-id="b42ad-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="b42ad-110">Další informace o Azure B2B naleznete v tématu [Co je přístup uživatele typu host v Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="b42ad-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="b42ad-111">U uživatelů jiných než B2B jsou určití uživatelé, kteří mohou mít neúplnou vlastnost Typ uživatele na objektu **Uživatel**.</span><span class="sxs-lookup"><span data-stu-id="b42ad-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="b42ad-112">To lze ověřit a opravit pomocí modulu Azure AD Powershell.</span><span class="sxs-lookup"><span data-stu-id="b42ad-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="b42ad-113">Další informace naleznete v tématu [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="b42ad-113">For more information, see [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="b42ad-114">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="b42ad-114">Resolution</span></span>

<span data-ttu-id="b42ad-115">K dokončení následujících kroků pro vyřešení problému musíte mít oprávnění globálního správce na klientovi Azure Active Directory nebo oprávnění pro **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="b42ad-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="b42ad-116">Pro ověření typu uživatele ovlivněného uživatele.</span><span class="sxs-lookup"><span data-stu-id="b42ad-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="b42ad-117">Příkaz vrátí následující informace.</span><span class="sxs-lookup"><span data-stu-id="b42ad-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="b42ad-118">Všimněte si vlastnosti **UserType** u uživatele.</span><span class="sxs-lookup"><span data-stu-id="b42ad-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="b42ad-119">Pokud je **UserType** prázdný, není například ani Člen ani Host, aktualizujte **UserType** pomocí následujícího příkazu.</span><span class="sxs-lookup"><span data-stu-id="b42ad-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
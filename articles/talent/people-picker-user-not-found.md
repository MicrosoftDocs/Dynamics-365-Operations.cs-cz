---
title: Uživatel nebyl nalezen v nástroji pro výběr osob v aplikacích Attract nebo Onboard
description: Toto téma vysvětluje, jak postupovat, když se uživatelé v klientovi společnosti nezobrazují v nástroji pro výběr osob v aplikacích Dynamics 365 for Talent Attract nebo Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "859498"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Uživatelé Azure Active Directory nenalezení v nástroji pro výběr osob

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Výdej

Někteří platní uživatelé v aplikaci Microsoft Azure Active Directory (Azure AD) pro klienta se nezobrazují při hledání jména v nástroji pro výběr osob v aplikacích Dynamics 365 for Talent Attract nebo Onboard.

## <a name="cause"></a>Příčina

Některé typy uživatelů nejsou aktuálně podporovány v aplikacích Attract či Onboard. Ověřte, zda uživatel není typem hosta Azure AD B2B. Informace o typu uživatele lze najít v listu Azure Active Directory na portálu Azure.

Další informace o Azure B2B naleznete v tématu [Co je přístup uživatele typu host v Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).

U uživatelů jiných než B2B jsou určití uživatelé, kteří mohou mít neúplnou vlastnost Typ uživatele na objektu **Uživatel**. To lze ověřit a opravit pomocí modulu Azure AD Powershell. Další informace naleznete v tématu [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>Rozlišení

K dokončení následujících kroků pro vyřešení problému musíte mít oprávnění globálního správce na klientovi Azure Active Directory nebo oprávnění pro **User.ReadWrite.All**.

Pro ověření typu uživatele ovlivněného uživatele.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Příkaz vrátí následující informace.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Všimněte si vlastnosti **UserType** u uživatele. Pokud je **UserType** prázdný, není například ani Člen ani Host, aktualizujte **UserType** pomocí následujícího příkazu.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```

---
title: Správa uživatelů e-Commerce a rolí
description: V tomto tématu je vysvětleno, jak udělit uživatelům přístup k vývojovému prostředí vašeho webu Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 44b02f262136c0d970ca9eee3e5e63ef6dc8ccb7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794276"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="16faf-103">Správa uživatelů e-Commerce a rolí</span><span class="sxs-lookup"><span data-stu-id="16faf-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="16faf-104">V tomto tématu je vysvětleno, jak udělit uživatelům přístup k vývojovému prostředí vašeho webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="16faf-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="16faf-105">Chcete-li pomoci řídit uživatelský přístup a udělit uživatelům oprávnění k provádění konkrétních úkolů, používá vývojové prostředí na webu skupiny zabezpečení, které vytvoříte v Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="16faf-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="16faf-106">Nejprve přiřaďte novou nebo existující skupinu zabezpečení z Azure AD k jednotlivým rolím ve vývojovém prostředí.</span><span class="sxs-lookup"><span data-stu-id="16faf-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="16faf-107">Poté přiřadíte nebo odvoláte oprávnění pro jednotlivé uživatele tím, že přidáte tyto uživatele do příslušné skupiny zabezpečení nebo je odeberete ze skupiny zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="16faf-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="16faf-108">Přehled rolí ve vývojovém prostředí</span><span class="sxs-lookup"><span data-stu-id="16faf-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="16faf-109">Vývojové prostředí Dynamics 365 for Commerce podporuje následující role.</span><span class="sxs-lookup"><span data-stu-id="16faf-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="16faf-110">Role</span><span class="sxs-lookup"><span data-stu-id="16faf-110">Role</span></span>                 | <span data-ttu-id="16faf-111">Popis</span><span class="sxs-lookup"><span data-stu-id="16faf-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="16faf-112">Správce systému</span><span class="sxs-lookup"><span data-stu-id="16faf-112">System Administrator</span></span> | <span data-ttu-id="16faf-113">Uživatelé s touto rolí mají všechna oprávnění pro všechny nástroje a pro všechna hodnocení a recenze.</span><span class="sxs-lookup"><span data-stu-id="16faf-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="16faf-114">Mohou také vytvářet weby.</span><span class="sxs-lookup"><span data-stu-id="16faf-114">They can also create sites.</span></span> |
| <span data-ttu-id="16faf-115">Správce</span><span class="sxs-lookup"><span data-stu-id="16faf-115">Administrator</span></span>   | <span data-ttu-id="16faf-116">Uživatelé s touto rolí mají všechna oprávnění pro všechny nástroje a RnR v dané struktuře webu.</span><span class="sxs-lookup"><span data-stu-id="16faf-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="16faf-117">Webový výrobce</span><span class="sxs-lookup"><span data-stu-id="16faf-117">Web Producer</span></span>         | <span data-ttu-id="16faf-118">Uživatelé s touto rolí mohou vytvářet stránky, fragmenty a šablony, odesílat a spravovat aktiva a obohacovat produkty a kategorie.</span><span class="sxs-lookup"><span data-stu-id="16faf-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="16faf-119">Prohlížeč</span><span class="sxs-lookup"><span data-stu-id="16faf-119">Reader</span></span>               | <span data-ttu-id="16faf-120">Uživatelé s touto rolí mohou zobrazit stránky, šablony, aktiva, fragmenty, rozvržení a nastavení, ale nesmí provádět žádné změny.</span><span class="sxs-lookup"><span data-stu-id="16faf-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="16faf-121">Moderátor RnR</span><span class="sxs-lookup"><span data-stu-id="16faf-121">RnR Moderator</span></span>        | <span data-ttu-id="16faf-122">Uživatelé s touto rolí mohou moderovat recenzování produktů.</span><span class="sxs-lookup"><span data-stu-id="16faf-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="16faf-123">Role Správce systému</span><span class="sxs-lookup"><span data-stu-id="16faf-123">System Administrator role</span></span>

<span data-ttu-id="16faf-124">Pokud zřizujete Dynamics 365 Commerce v prostředí služby Microsoft Dynamics Lifecycle Services (LCS), budete požádáni o poskytnutí skupiny zabezpečení pro roli **Správce systému**.</span><span class="sxs-lookup"><span data-stu-id="16faf-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="16faf-125">Tato role se poté automaticky použije na všechny weby, které vytvoříte v prostředí, které konfigurujete.</span><span class="sxs-lookup"><span data-stu-id="16faf-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="16faf-126">Skupinu zabezpečení pro tuto roli lze aktualizovat pouze v rámci LCS.</span><span class="sxs-lookup"><span data-stu-id="16faf-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="16faf-127">Na stránce **Správa webu** pro všechny weby se zobrazí pouze pro čtení a slouží pouze k informačním účelům.</span><span class="sxs-lookup"><span data-stu-id="16faf-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="16faf-128">Role správce</span><span class="sxs-lookup"><span data-stu-id="16faf-128">Administrator role</span></span>

<span data-ttu-id="16faf-129">Při vytváření nového webu v rámci Commerce budete požádáni o poskytnutí skupiny zabezpečení pro roli **Správce**.</span><span class="sxs-lookup"><span data-stu-id="16faf-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="16faf-130">Přehled oprávnění, která tato role uděluje, naleznete v tabulce uvedené výše v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="16faf-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="16faf-131">Přidat nebo aktualizovat skupiny zabezpečení</span><span class="sxs-lookup"><span data-stu-id="16faf-131">Add or update security groups</span></span>

<span data-ttu-id="16faf-132">Po vytvoření webu mohou k vývojovému prostředí daného webu přistupovat pouze uživatelé, kteří jsou ve skupinách zabezpečení a mají role **Správce systému** a **Správce**.</span><span class="sxs-lookup"><span data-stu-id="16faf-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="16faf-133">Chcete-li přiřadit uživatele k rolím **Tvůrce webu**, **Moderátor RnR** a **Prohlížeč**, je nutné těmto rolím přiřadit skupiny zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="16faf-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="16faf-134">Chcete-li přidat skupinu zabezpečení do role nebo aktualizovat skupinu zabezpečení, která je aktuálně přiřazena k roli, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="16faf-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="16faf-135">Přejděte na web, který chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="16faf-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="16faf-136">V **Správě webu** otevřete stránku **Zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="16faf-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="16faf-137">Vyberte roli, kterou chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="16faf-137">Select the role to modify.</span></span>
1. <span data-ttu-id="16faf-138">Přidejte skupiny zabezpečení k rolím nebo odeberte skupiny zabezpečení z rolí.</span><span class="sxs-lookup"><span data-stu-id="16faf-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16faf-139">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="16faf-139">Additional resources</span></span>

[<span data-ttu-id="16faf-140">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="16faf-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="16faf-141">Zvažování optimalizace webového vyhledávače pro váš web</span><span class="sxs-lookup"><span data-stu-id="16faf-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="16faf-142">Správa zásad zabezpečení obsahu (CSP)</span><span class="sxs-lookup"><span data-stu-id="16faf-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
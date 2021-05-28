---
title: Během počátečního nasazení nelze konfigurovat skupinu zabezpečení pro Tvůrce webů Commerce
description: Toto téma obsahuje pokyny pro řešení potíží, které mohou pomoci, když skupina zabezpečení Microsoft Azure Active Directory (Azure AD) pro Tvůrce webů Commerce se při vytváření komponent elektronického obchodování nezobrazuje jako volba Microsoft Dynamics Lifecycle Services (LCS) během počátečního nasazení nového tenanta elektronického obchodování.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d29e560d0f7b2bbc2415d7a0f6fe18f2ca17dc7c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020725"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="6c4a0-103">Během počátečního nasazení nelze konfigurovat skupinu zabezpečení pro Tvůrce webů Commerce</span><span class="sxs-lookup"><span data-stu-id="6c4a0-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c4a0-104">Toto téma obsahuje pokyny pro řešení potíží, které mohou pomoci, když skupina zabezpečení Microsoft Azure Active Directory (Azure AD) pro Tvůrce webů Commerce se při vytváření komponent elektronického obchodování nezobrazuje jako volba Microsoft Dynamics Lifecycle Services (LCS) během počátečního nasazení nového tenanta elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="6c4a0-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="6c4a0-105">popis</span><span class="sxs-lookup"><span data-stu-id="6c4a0-105">Description</span></span>

<span data-ttu-id="6c4a0-106">Když vytvoříte komponenty elektronického obchodování jako součást procesu nasazení nového tenanta elektronického obchodu, který zahrnuje komponentu Tvůrce webu Commerce, skupina zabezpečení Azure AD se v dialogovém okně nezobrazí jako možnost.</span><span class="sxs-lookup"><span data-stu-id="6c4a0-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="6c4a0-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="6c4a0-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="6c4a0-108">Zřízení uživatele webu elektronického obchodu ve správném tenantovi</span><span class="sxs-lookup"><span data-stu-id="6c4a0-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="6c4a0-109">Přejděte na [portál Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="6c4a0-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="6c4a0-110">Pod tenantem, pro který byl zřízen projekt LCS pro váš web elektronického obchodování, postupujte podle pokynů v části [Vytvoření základní skupiny a přidání členů pomocí Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="6c4a0-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="6c4a0-111">Přejděte do [LCS](https://lcs.dynamics.com/) a přihlaste se pomocí účtu, který sdílí stejného tenanta jako skupina zabezpečení Azure AD, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="6c4a0-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="6c4a0-112">Účet musí mít přístup k prohlížení skupiny zabezpečení Azure AD.</span><span class="sxs-lookup"><span data-stu-id="6c4a0-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="6c4a0-113">Proveďte kroky nastavení a nakonfigurujte web elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="6c4a0-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="6c4a0-114">Když zřídíte komponenty elektronického obchodování, skupina zabezpečení by se nyní měla zobrazit jako možnost v dialogovém okně.</span><span class="sxs-lookup"><span data-stu-id="6c4a0-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="6c4a0-115">Chcete-li zajistit, aby bylo pole v dialogovém okně vyplněno seznamem skupin zabezpečení, musíte vybrat **Enter** poté, co zadáte název skupiny zabezpečení Azure AD, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="6c4a0-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="6c4a0-116">Výsledky hledání zobrazí seznam všech skupin zabezpečení Azure AD, které začínají hledaným textem a ke kterým má uživatel přístup.</span><span class="sxs-lookup"><span data-stu-id="6c4a0-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="6c4a0-117">Můžete použít kratší hledaný výraz, abyste získali širší výsledky vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6c4a0-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c4a0-118">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="6c4a0-118">Additional resources</span></span>

[<span data-ttu-id="6c4a0-119">Vytvoření základní skupiny a přidání členů pomocí Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6c4a0-119">Create a basic group and add members using Azure Active Directory</span></span>](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="6c4a0-120">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="6c4a0-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)
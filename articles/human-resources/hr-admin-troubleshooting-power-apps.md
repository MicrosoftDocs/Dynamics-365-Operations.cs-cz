---
title: Nelze vytvořit prostředí v centru pro správu Power Apps
description: Tento článek vysvětluje, jak postupovat, když správce nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec63148364022fe5b8c40d855856eec232af3e48
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463953"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="7db8d-103">Nelze vytvořit prostředí v centru pro správu Power Apps</span><span class="sxs-lookup"><span data-stu-id="7db8d-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7db8d-104">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="7db8d-104">**Issue**</span></span>

- <span data-ttu-id="7db8d-105">Správce klienta/prostředí nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="7db8d-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="7db8d-106">Uživatel nemá licenci, která dává právo vytvářet prostředí.</span><span class="sxs-lookup"><span data-stu-id="7db8d-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="7db8d-107">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="7db8d-107">**Solution**</span></span>

<span data-ttu-id="7db8d-108">Ujistěte se, že správce tenanta přidělil platnou licenci Power Apps P2 pro uživatele vytvářejícího prostředí.</span><span class="sxs-lookup"><span data-stu-id="7db8d-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="7db8d-109">Následující plány služeb Microsoft Dynamics poskytují oprávnění k vytváření prostředí:</span><span class="sxs-lookup"><span data-stu-id="7db8d-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="7db8d-110">Celkové skladová jednotka zásob produktu (SKU)</span><span class="sxs-lookup"><span data-stu-id="7db8d-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="7db8d-111">Servisní plán Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="7db8d-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="7db8d-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="7db8d-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="7db8d-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7db8d-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="7db8d-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="7db8d-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="7db8d-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7db8d-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="7db8d-116">Všimněte si, že různé skladové jednotky aplikace Microsoft Office také poskytují toto právo, společně se samostatnými SKU Power Apps plánu 2.</span><span class="sxs-lookup"><span data-stu-id="7db8d-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="7db8d-117">Důležité je, že jedna z těchto skladových jednotek zásob musí být přítomná.</span><span class="sxs-lookup"><span data-stu-id="7db8d-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="7db8d-118">Přejděte na [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="7db8d-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="7db8d-119">Vytvořte prostředí podle pokynů v části [Zřízení Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="7db8d-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
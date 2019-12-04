---
title: Nelze vytvořit prostředí v centru pro správu Power Apps
description: Toto téma vysvětluje, jak postupovat, když správce nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
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
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5923c59ab5dde13fed0483972e76634031404fd8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773212"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="e578b-103">Nelze vytvořit prostředí v centru pro správu Power Apps</span><span class="sxs-lookup"><span data-stu-id="e578b-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e578b-104">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="e578b-104">**Issue**</span></span>

- <span data-ttu-id="e578b-105">Správce klienta/prostředí nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e578b-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="e578b-106">Licence, která uživateli poskytuje právo provádět krok vytváření prostředí, nebyla přiřazena přímo uživateli, který provádí tento krok.</span><span class="sxs-lookup"><span data-stu-id="e578b-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="e578b-107">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="e578b-107">**Solution**</span></span>

<span data-ttu-id="e578b-108">Ujistěte se, že správce klienta přidělil platnou licenci Power Apps P2 přímo uživateli, který provede krok vytvoření prostředí.</span><span class="sxs-lookup"><span data-stu-id="e578b-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="e578b-109">Zde jsou servisní plány Microsoft Dynamics, které poskytují toto právo.</span><span class="sxs-lookup"><span data-stu-id="e578b-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="e578b-110">Celkové skladová jednotka zásob produktu (SKU)</span><span class="sxs-lookup"><span data-stu-id="e578b-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="e578b-111">Servisní plán Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="e578b-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="e578b-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="e578b-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="e578b-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e578b-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="e578b-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="e578b-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="e578b-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="e578b-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="e578b-116">Všimněte si, že různé skladové jednotky aplikace Microsoft Office také poskytují toto právo, společně se samostatnými SKU Power Apps plánu 2.</span><span class="sxs-lookup"><span data-stu-id="e578b-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="e578b-117">Důležité je, že jedna z těchto skladových jednotek zásob musí být přítomná.</span><span class="sxs-lookup"><span data-stu-id="e578b-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="e578b-118">Přejděte na [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="e578b-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="e578b-119">Vytvořte prostředí podle pokynů v části [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="e578b-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

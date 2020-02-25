---
title: Nelze vytvořit prostředí v centru pro správu Power Apps
description: Tento článek vysvětluje, jak postupovat, když správce nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: f4c75706183a3d6c961852395e464d46ba3ec1f2
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008322"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="68df4-103">Nelze vytvořit prostředí v centru pro správu Power Apps</span><span class="sxs-lookup"><span data-stu-id="68df4-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="68df4-104">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="68df4-104">**Issue**</span></span>

- <span data-ttu-id="68df4-105">Správce klienta/prostředí nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="68df4-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="68df4-106">Licence, která uživateli poskytuje právo provádět krok vytváření prostředí, nebyla přiřazena přímo uživateli, který provádí tento krok.</span><span class="sxs-lookup"><span data-stu-id="68df4-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="68df4-107">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="68df4-107">**Solution**</span></span>

<span data-ttu-id="68df4-108">Ujistěte se, že správce klienta přidělil platnou licenci Power Apps P2 přímo uživateli, který provede krok vytvoření prostředí.</span><span class="sxs-lookup"><span data-stu-id="68df4-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="68df4-109">Zde jsou servisní plány Microsoft Dynamics, které poskytují toto právo.</span><span class="sxs-lookup"><span data-stu-id="68df4-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="68df4-110">Celkové skladová jednotka zásob produktu (SKU)</span><span class="sxs-lookup"><span data-stu-id="68df4-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="68df4-111">Servisní plán Power Apps P2</span><span class="sxs-lookup"><span data-stu-id="68df4-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="68df4-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="68df4-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="68df4-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="68df4-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="68df4-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="68df4-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="68df4-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="68df4-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="68df4-116">Všimněte si, že různé skladové jednotky aplikace Microsoft Office také poskytují toto právo, společně se samostatnými SKU Power Apps plánu 2.</span><span class="sxs-lookup"><span data-stu-id="68df4-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="68df4-117">Důležité je, že jedna z těchto skladových jednotek zásob musí být přítomná.</span><span class="sxs-lookup"><span data-stu-id="68df4-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="68df4-118">Přejděte na [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="68df4-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="68df4-119">Vytvořte prostředí podle pokynů v části [Zřízení Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="68df4-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

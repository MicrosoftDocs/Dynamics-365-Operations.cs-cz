---
title: "Nelze vytvořit prostředí v centru pro správu PowerApps"
description: "Toto téma vysvětluje, jak postupovat, když správce nemůže vytvořit prostředí v centru pro správu Microsoft PowerApps."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="aeade-103">Nelze vytvořit prostředí v centru pro správu PowerApps</span><span class="sxs-lookup"><span data-stu-id="aeade-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aeade-104">**Problém**</span><span class="sxs-lookup"><span data-stu-id="aeade-104">**Issue**</span></span>

- <span data-ttu-id="aeade-105">Správce klienta/prostředí nemůže vytvořit prostředí v centru pro správu Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="aeade-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="aeade-106">Licence, která uživateli poskytuje právo provádět krok vytváření prostředí, nebyla přiřazena přímo uživateli, který provádí tento krok.</span><span class="sxs-lookup"><span data-stu-id="aeade-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="aeade-107">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="aeade-107">**Solution**</span></span>

<span data-ttu-id="aeade-108">Ujistěte se, že správce klienta přidělil platnou licenci PowerApps P2 přímo uživateli, který provede krok vytvoření prostředí.</span><span class="sxs-lookup"><span data-stu-id="aeade-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="aeade-109">Zde je servisní plány Microsoft Dynamics, které poskytují toto právo.</span><span class="sxs-lookup"><span data-stu-id="aeade-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="aeade-110">Celkové skladová jednotka zásob produktu (SKU)</span><span class="sxs-lookup"><span data-stu-id="aeade-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="aeade-111">Servisní plán PowerApps P2</span><span class="sxs-lookup"><span data-stu-id="aeade-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="aeade-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="aeade-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="aeade-113">PowerApps pro Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="aeade-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="aeade-114">Microsoft Dynamics 365 Plán, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="aeade-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="aeade-115">PowerApps pro Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="aeade-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="aeade-116">Všimněte si, že různé skladové jednotky aplikace Microsoft Office také poskytují toto právo, společně se samostatnými SKU PowerApps Plan 2</span><span class="sxs-lookup"><span data-stu-id="aeade-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="aeade-117">Důležité je, že jedna z těchto skladových jednotek zásob musí být přítomná.</span><span class="sxs-lookup"><span data-stu-id="aeade-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="aeade-118">Přejděte na [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="aeade-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="aeade-119">Vytvořte prostředí podle pokynů v části [Zřízení aplikace Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="aeade-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


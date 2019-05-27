---
title: Nelze vytvořit prostředí v centru pro správu PowerApps
description: Toto téma vysvětluje, jak postupovat, když správce nemůže vytvořit prostředí v centru pro správu Microsoft PowerApps.
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
ms.openlocfilehash: 97d44dc034cb8097fc0ecf9ac4e485425f097102
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517481"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="9d801-103">Nelze vytvořit prostředí v centru pro správu PowerApps</span><span class="sxs-lookup"><span data-stu-id="9d801-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d801-104">**Problém**</span><span class="sxs-lookup"><span data-stu-id="9d801-104">**Issue**</span></span>

- <span data-ttu-id="9d801-105">Správce klienta/prostředí nemůže vytvořit prostředí v centru pro správu Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="9d801-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="9d801-106">Licence, která uživateli poskytuje právo provádět krok vytváření prostředí, nebyla přiřazena přímo uživateli, který provádí tento krok.</span><span class="sxs-lookup"><span data-stu-id="9d801-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="9d801-107">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="9d801-107">**Solution**</span></span>

<span data-ttu-id="9d801-108">Ujistěte se, že správce klienta přidělil platnou licenci PowerApps P2 přímo uživateli, který provede krok vytvoření prostředí.</span><span class="sxs-lookup"><span data-stu-id="9d801-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="9d801-109">Zde jsou servisní plány Microsoft Dynamics, které poskytují toto právo.</span><span class="sxs-lookup"><span data-stu-id="9d801-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="9d801-110">Celkové skladová jednotka zásob produktu (SKU)</span><span class="sxs-lookup"><span data-stu-id="9d801-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="9d801-111">Servisní plán PowerApps P2</span><span class="sxs-lookup"><span data-stu-id="9d801-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="9d801-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="9d801-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="9d801-113">PowerApps pro Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9d801-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="9d801-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="9d801-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="9d801-115">PowerApps pro Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9d801-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="9d801-116">Všimněte si, že různé skladové jednotky aplikace Microsoft Office také poskytují toto právo, společně se samostatnými SKU PowerApps Plan 2</span><span class="sxs-lookup"><span data-stu-id="9d801-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="9d801-117">Důležité je, že jedna z těchto skladových jednotek zásob musí být přítomná.</span><span class="sxs-lookup"><span data-stu-id="9d801-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="9d801-118">Přejděte na [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="9d801-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="9d801-119">Vytvořte prostředí podle pokynů v části [Zřízení aplikace Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="9d801-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Commerce
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443911"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="b71b0-103">Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b71b0-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b71b0-104">Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b71b0-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="b71b0-105">*Odstraněná* funkce již není k dispozici v produktu.</span><span class="sxs-lookup"><span data-stu-id="b71b0-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="b71b0-106">*Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.</span><span class="sxs-lookup"><span data-stu-id="b71b0-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="b71b0-107">Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování.</span><span class="sxs-lookup"><span data-stu-id="b71b0-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="b71b0-108">Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="b71b0-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="b71b0-109">Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b71b0-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a><span data-ttu-id="b71b0-110">Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.11</span><span class="sxs-lookup"><span data-stu-id="b71b0-110">Features removed or deprecated in the Commerce 10.0.11 release</span></span>
### <a name="data-action-hooks"></a><span data-ttu-id="b71b0-111">Zavěšení datových akcí</span><span class="sxs-lookup"><span data-stu-id="b71b0-111">Data action hooks</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="b71b0-112">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="b71b0-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b71b0-113">Funkce háčků datových akcí byla zastaralá kvůli problémům s výkonem.</span><span class="sxs-lookup"><span data-stu-id="b71b0-113">The data action hooks feature has been deprecated due to performance issues.</span></span> |
| <span data-ttu-id="b71b0-114">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="b71b0-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b71b0-115">Doporučuje se místo toho použít [přepisy akce dat](../e-commerce-extensibility/data-action-overrides.md) ke změně obchodní logiky ve vrstvě akce dat.</span><span class="sxs-lookup"><span data-stu-id="b71b0-115">It is recommended to instead use [data action overrides](../e-commerce-extensibility/data-action-overrides.md) to modify business logic in the data action layer.</span></span>|
| <span data-ttu-id="b71b0-116">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="b71b0-116">**Product areas affected**</span></span>         | <span data-ttu-id="b71b0-117">Akce dat rozšiřitelnosti elektronického obchodování</span><span class="sxs-lookup"><span data-stu-id="b71b0-117">E-Commerce extensibility data actions</span></span> |
| <span data-ttu-id="b71b0-118">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="b71b0-118">**Deployment option**</span></span>              | <span data-ttu-id="b71b0-119">Vše</span><span class="sxs-lookup"><span data-stu-id="b71b0-119">All</span></span> |
| <span data-ttu-id="b71b0-120">**Stav**</span><span class="sxs-lookup"><span data-stu-id="b71b0-120">**Status**</span></span>                         | <span data-ttu-id="b71b0-121">Zastaralé: k verzi 10.0.11</span><span class="sxs-lookup"><span data-stu-id="b71b0-121">Deprecated: As of release 10.0.11</span></span> |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="b71b0-122">Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.10</span><span class="sxs-lookup"><span data-stu-id="b71b0-122">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="b71b0-123">Operace POS 803 – Vyzvednutí a příjem</span><span class="sxs-lookup"><span data-stu-id="b71b0-123">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="b71b0-124">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="b71b0-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b71b0-125">Operace stahování a přijímání jsou zastaralé kvůli novému přepracování operací.</span><span class="sxs-lookup"><span data-stu-id="b71b0-125">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="b71b0-126">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="b71b0-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b71b0-127">Ano.</span><span class="sxs-lookup"><span data-stu-id="b71b0-127">Yes.</span></span> <span data-ttu-id="b71b0-128">Je nahrazen dvěma novými operacemi POS: příchozí operace (804) a odchozí operace (805).</span><span class="sxs-lookup"><span data-stu-id="b71b0-128">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="b71b0-129">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="b71b0-129">**Product areas affected**</span></span>         | <span data-ttu-id="b71b0-130">Aplikace Pokladní místo (POS)</span><span class="sxs-lookup"><span data-stu-id="b71b0-130">Point of sale (POS) application</span></span> |
| <span data-ttu-id="b71b0-131">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="b71b0-131">**Deployment option**</span></span>              | <span data-ttu-id="b71b0-132">Vše</span><span class="sxs-lookup"><span data-stu-id="b71b0-132">All</span></span> |
| <span data-ttu-id="b71b0-133">**Stav**</span><span class="sxs-lookup"><span data-stu-id="b71b0-133">**Status**</span></span>                         | <span data-ttu-id="b71b0-134">Zastaralé: Od vydání 10.0.10 již operace vyzvednutí a přijetí nebude mít žádné nové aktualizace funkcí.</span><span class="sxs-lookup"><span data-stu-id="b71b0-134">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="b71b0-135">V budoucích verzích budou pro tuto operaci provedeny pouze kritické opravy chyb.</span><span class="sxs-lookup"><span data-stu-id="b71b0-135">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="b71b0-136">Doporučuje se, aby všichni zákazníci přešli na nové [příchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) a [odchozí operace](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), které budou nadále součástí našeho dlouhodobého přehledu aplikací.</span><span class="sxs-lookup"><span data-stu-id="b71b0-136">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="b71b0-137">Odebrané nebo zastaralé funkce v aplikaci Commerce verze 10.0.7</span><span class="sxs-lookup"><span data-stu-id="b71b0-137">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="b71b0-138">Rozhraní API obchodu GetProductAvailabilities a GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="b71b0-138">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="b71b0-139">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="b71b0-139">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b71b0-140">Byla vytvořena nová optimalizovaná rozhraní API nahrazující rozhraní API GetProductAvailabilities a GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="b71b0-140">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="b71b0-141">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="b71b0-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b71b0-142">Ano: Nahrazuje je rozhraní API GetEstimatedAvailability a GetEstimatedProductWarehouseAvailability.</span><span class="sxs-lookup"><span data-stu-id="b71b0-142">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="b71b0-143">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="b71b0-143">**Product areas affected**</span></span>         | <span data-ttu-id="b71b0-144">Sada SDK pro elektronický obchod</span><span class="sxs-lookup"><span data-stu-id="b71b0-144">e-Commerce application SDK</span></span> |
| <span data-ttu-id="b71b0-145">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="b71b0-145">**Deployment option**</span></span>              | <span data-ttu-id="b71b0-146">Vše</span><span class="sxs-lookup"><span data-stu-id="b71b0-146">All</span></span> |
| <span data-ttu-id="b71b0-147">**Stav**</span><span class="sxs-lookup"><span data-stu-id="b71b0-147">**Status**</span></span>                         | <span data-ttu-id="b71b0-148">Ukončeno: Od vydání 10.0.7 nebudou investovány žádné technické prostředky do rozhraní API GetProductAvailabilities a GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="b71b0-148">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="b71b0-149">Organizace, které používají tato API ve svých implementacích elektronického obchodování, by měly přejít na nová rozhraní API GetEstimatedAvailability a GetEstimatedProductWarehouseAvailability a povolit [Funkci pro optimalizaci dostupnosti produktu](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="b71b0-149">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="b71b0-150">Předchozí oznámení o odebraných nebo zastaralých funkcích</span><span class="sxs-lookup"><span data-stu-id="b71b0-150">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="b71b0-151">Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="b71b0-151">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>

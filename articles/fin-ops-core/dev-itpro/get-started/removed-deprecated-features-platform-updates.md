---
title: Odebrané nebo zastaralé funkce platformy
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z aktualizací platformy aplikací Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087876"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="5ebdc-103">Odebrané nebo zastaralé funkce platformy</span><span class="sxs-lookup"><span data-stu-id="5ebdc-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ebdc-104">Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z aktualizací platformy aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5ebdc-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="5ebdc-105">*Odstraněná* funkce již není k dispozici v produktu.</span><span class="sxs-lookup"><span data-stu-id="5ebdc-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="5ebdc-106">*Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.</span><span class="sxs-lookup"><span data-stu-id="5ebdc-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="5ebdc-107">Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování.</span><span class="sxs-lookup"><span data-stu-id="5ebdc-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ebdc-108">Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="5ebdc-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="5ebdc-109">Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5ebdc-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="5ebdc-110">Aktualizace platformy 32</span><span class="sxs-lookup"><span data-stu-id="5ebdc-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="5ebdc-111">Dialogové okno pro změnu požadavku workflowu již neobsahuje rozevírací seznam pro výběr uživatele.</span><span class="sxs-lookup"><span data-stu-id="5ebdc-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="5ebdc-112">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="5ebdc-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="5ebdc-113">Jednalo se o bezpečnostní problém, protože požadavek na změnu mohl být odeslán nežádoucímu uživateli.</span><span class="sxs-lookup"><span data-stu-id="5ebdc-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="5ebdc-114">Šlo také o problém s využitelností, protože aplikace nutila uživatele určit, kdo je původce workflowu, a ručně jej vybrat.</span><span class="sxs-lookup"><span data-stu-id="5ebdc-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="5ebdc-115">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="5ebdc-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="5ebdc-116">Ne</span><span class="sxs-lookup"><span data-stu-id="5ebdc-116">No</span></span> |
| <span data-ttu-id="5ebdc-117">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="5ebdc-117">**Product areas affected**</span></span>         | <span data-ttu-id="5ebdc-118">Workflow</span><span class="sxs-lookup"><span data-stu-id="5ebdc-118">Workflow</span></span> |
| <span data-ttu-id="5ebdc-119">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="5ebdc-119">**Deployment option**</span></span>              | <span data-ttu-id="5ebdc-120">Vše</span><span class="sxs-lookup"><span data-stu-id="5ebdc-120">All</span></span> |
| <span data-ttu-id="5ebdc-121">**Stav**</span><span class="sxs-lookup"><span data-stu-id="5ebdc-121">**Status**</span></span>                         | <span data-ttu-id="5ebdc-122">Rozevírací seznam pro výběr uživatelů byl odebrán z dialogového okna pro změnu požadavku v aktualizaci platformy 32.</span><span class="sxs-lookup"><span data-stu-id="5ebdc-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="5ebdc-123">Požadavky na změnu požadavku budou automaticky odeslány původci, jak bylo zamýšleno.</span><span class="sxs-lookup"><span data-stu-id="5ebdc-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="5ebdc-124">Další informace o této funkci naleznete v tématu [Akce v procesech schválení workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="5ebdc-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="5ebdc-125">Předchozí oznámení o odebraných nebo zastaralých funkcích</span><span class="sxs-lookup"><span data-stu-id="5ebdc-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="5ebdc-126">Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="5ebdc-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>


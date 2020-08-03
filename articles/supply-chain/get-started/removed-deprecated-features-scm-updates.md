---
title: Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Supply Chain Management
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění v Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597109"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="6413d-103">Odstraněné nebo zastaralé funkce v aplikaci Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6413d-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6413d-104">Toto téma bude aktualizováno podle nově odebraných nebo zastaralých funkcí pro Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6413d-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="6413d-105">*Odstraněná* funkce již není k dispozici v produktu.</span><span class="sxs-lookup"><span data-stu-id="6413d-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="6413d-106">*Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.</span><span class="sxs-lookup"><span data-stu-id="6413d-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="6413d-107">Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování.</span><span class="sxs-lookup"><span data-stu-id="6413d-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="6413d-108">Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="6413d-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="6413d-109">Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6413d-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="6413d-110">Odebrané nebo zastaralé funkce ve verzi Supply Chain Management 10.0.11</span><span class="sxs-lookup"><span data-stu-id="6413d-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="6413d-111">Použití integrovaného modulu hlavního plánování Supply Chain Management pro scénáře distribuce</span><span class="sxs-lookup"><span data-stu-id="6413d-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="6413d-112">**Důvod pro zrušení/odstranění**</span><span class="sxs-lookup"><span data-stu-id="6413d-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="6413d-113">Pro zvýšení výkonu a minimalizaci zatížení databáze SQL během hlavních plánovacích relací je vestavěný hlavní plánovací modul Supply Chain Management nahrazen optimalizací plánování.</span><span class="sxs-lookup"><span data-stu-id="6413d-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="6413d-114">Optimalizace plánování umožňuje rychlé spouštění plánů, které lze provádět i během úředních hodin.</span><span class="sxs-lookup"><span data-stu-id="6413d-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="6413d-115">To umožňuje plánovačům okamžitě reagovat na změny poptávky nebo parametrů plánování.</span><span class="sxs-lookup"><span data-stu-id="6413d-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="6413d-116">**Nahrazeno jinou funkcí?**</span><span class="sxs-lookup"><span data-stu-id="6413d-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="6413d-117">Ano, optimalizace plánování nahradí předdefinovaný hlavní modul plánování Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6413d-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="6413d-118">**Ovlivněné oblasti produktu**</span><span class="sxs-lookup"><span data-stu-id="6413d-118">**Product areas affected**</span></span>         | <span data-ttu-id="6413d-119">Supply Chain Management - hlavní plánování</span><span class="sxs-lookup"><span data-stu-id="6413d-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="6413d-120">**Možnost nasazení**</span><span class="sxs-lookup"><span data-stu-id="6413d-120">**Deployment option**</span></span>              | <span data-ttu-id="6413d-121">Pouze cloud.</span><span class="sxs-lookup"><span data-stu-id="6413d-121">Cloud only.</span></span> <span data-ttu-id="6413d-122">Všimněte si, že optimalizace plánování není podporována u místních nasazení.</span><span class="sxs-lookup"><span data-stu-id="6413d-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="6413d-123">**Stav**</span><span class="sxs-lookup"><span data-stu-id="6413d-123">**Status**</span></span>                         | <span data-ttu-id="6413d-124">Zastaralé.</span><span class="sxs-lookup"><span data-stu-id="6413d-124">Deprecated.</span></span> <span data-ttu-id="6413d-125">Od dubna April 2021 nebudou scénáře distribuce dále podporovány v integrovaném modulu hlavního plánování Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6413d-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="6413d-126">U distribučních scénářů musí zákazníci pro výpočet hlavního plánování použít Optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="6413d-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="6413d-127">Další informace naleznete v tématu [Dokumentace optimalizace plánování](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="6413d-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="6413d-128">Zákazníci s místním nasazením Dynamics 365 Supply Chain Management mohou i nadále používat hlavní plánovací modul Supply Chain Management pro scénáře distribuce po dubnu 2021.</span><span class="sxs-lookup"><span data-stu-id="6413d-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="6413d-129">Nebudou však poskytována žádná další vylepšení funkcí.</span><span class="sxs-lookup"><span data-stu-id="6413d-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="6413d-130">Předchozí oznámení o odebraných nebo zastaralých funkcích</span><span class="sxs-lookup"><span data-stu-id="6413d-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="6413d-131">Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="6413d-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>

---
title: Přehled správy technických změn
description: Toto téma poskytuje přehled správy technických změn, která vám pomůže plánovat a spravovat verzování produktu a spravovat životní cykly produktu a technických změn.
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: f1aa04b472eaef7ed398f08a05d46bac2d589561
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514343"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="f1947-103">Přehled správy technických změn</span><span class="sxs-lookup"><span data-stu-id="f1947-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="f1947-104">Souhrn funkce</span><span class="sxs-lookup"><span data-stu-id="f1947-104">Feature summary</span></span>

<span data-ttu-id="f1947-105">Dnešní výrobci vyžadují silnou správu dat produktu, řízení verzí a správu technických změn, aby uspěli ve světě neustále se snižujících životních cyklů produktů, zvýšených požadavků na kvalitu a spolehlivost a zvýšeného zaměření na bezpečnost produktů.</span><span class="sxs-lookup"><span data-stu-id="f1947-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="f1947-106">Správa technických změn přináší strukturu a disciplínu do procesu správy dat produktu a umožňuje, aby byly produkty definovány, uvolňovány a revidovány kontrolovaným způsobem, který je podporován pracovními postupy.</span><span class="sxs-lookup"><span data-stu-id="f1947-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="f1947-107">Prostřednictvím verzí produktu a správy technických změn můžete dokumentovat, hodnotit dopad a aplikovat technické změny během celého životního cyklu produktu.</span><span class="sxs-lookup"><span data-stu-id="f1947-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="f1947-108">Správa technických změn vám pomáhá plánovat a spravovat verzování produktu a spravovat životní cykly produktu a technických změn.</span><span class="sxs-lookup"><span data-stu-id="f1947-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="f1947-109">Zde je seznam jejich hlavních funkcí:</span><span class="sxs-lookup"><span data-stu-id="f1947-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="f1947-110">Verzování produktu</span><span class="sxs-lookup"><span data-stu-id="f1947-110">Product versioning</span></span>
- <span data-ttu-id="f1947-111">Vylepšená funkce uvolňování produktu, která vám umožní udržovat hlavní data produktu v jedné právnické osobě (technická společnost) a publikovat plně nakonfigurovaný uvolněný produkt do jiných právnických společností.</span><span class="sxs-lookup"><span data-stu-id="f1947-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="f1947-112">Pravidla pro ověřování, zda jsou požadované informace zadány před aktivací verze produktu (kontroly připravenosti).</span><span class="sxs-lookup"><span data-stu-id="f1947-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="f1947-113">Vylepšená správa životního cyklu produktu prostřednictvím detailní kontroly nad tím, kdy lze uvolněný produkt použít v konkrétních obchodních procesech.</span><span class="sxs-lookup"><span data-stu-id="f1947-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="f1947-114">Požadavky na technické změny, které jsou podporovány pracovními postupy</span><span class="sxs-lookup"><span data-stu-id="f1947-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="f1947-115">Příkazy k technickým změnám, které jsou podporovány pracovními postupy</span><span class="sxs-lookup"><span data-stu-id="f1947-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="f1947-116">Předchozí video ([Možnosti správy změn v Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) je součástí [seznamu videí o Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), které jsou k dispozici na YouTube.</span><span class="sxs-lookup"><span data-stu-id="f1947-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-engineering-change-management-for-your-system"></a><span data-ttu-id="f1947-117">Zapněte pro svůj systém správu technických změn</span><span class="sxs-lookup"><span data-stu-id="f1947-117">Turn on engineering change management for your system</span></span>

<span data-ttu-id="f1947-118">Nejprve zapněte správu technických změn podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="f1947-118">First, turn on engineering change management by following these steps.</span></span>

1. <span data-ttu-id="f1947-119">Přejděte na [Správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f1947-119">Go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
1. <span data-ttu-id="f1947-120">Zkontrolovat aktualizace.</span><span class="sxs-lookup"><span data-stu-id="f1947-120">Check for updates.</span></span>
1. <span data-ttu-id="f1947-121">Zapněte funkci s názvem **Správa technických změn**.</span><span class="sxs-lookup"><span data-stu-id="f1947-121">Turn on the feature that is named **Engineering Change Management**.</span></span>

<span data-ttu-id="f1947-122">Dále zapněte konfigurační klíč **Správa technických změn** podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="f1947-122">Next, turn on the **Engineering Change Management** configuration key by following these steps.</span></span>

1. <span data-ttu-id="f1947-123">Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f1947-123">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="f1947-124">Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.</span><span class="sxs-lookup"><span data-stu-id="f1947-124">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="f1947-125">Rozbalte uzel **Obchod** a vyberte zaškrtávací políčko **Řízení technických změn**.</span><span class="sxs-lookup"><span data-stu-id="f1947-125">Expand the **Trade** node, and select the **Engineering Change Management** check box.</span></span>
1. <span data-ttu-id="f1947-126">Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f1947-126">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

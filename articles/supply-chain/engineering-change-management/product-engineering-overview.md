---
title: Přehled správy technických změn
description: Toto téma poskytuje přehled správy technických změn, která vám pomůže plánovat a spravovat verzování produktu a spravovat životní cykly produktu a technických změn.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d9430fe02abe58f37d2bfd1431b4da61527d0834
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115042"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="66f7d-103">Přehled správy technických změn</span><span class="sxs-lookup"><span data-stu-id="66f7d-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="66f7d-104">Souhrn funkce</span><span class="sxs-lookup"><span data-stu-id="66f7d-104">Feature summary</span></span>

<span data-ttu-id="66f7d-105">Dnešní výrobci vyžadují silnou správu dat produktu, řízení verzí a správu technických změn, aby uspěli ve světě neustále se snižujících životních cyklů produktů, zvýšených požadavků na kvalitu a spolehlivost a zvýšeného zaměření na bezpečnost produktů.</span><span class="sxs-lookup"><span data-stu-id="66f7d-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="66f7d-106">Správa technických změn přináší strukturu a disciplínu do procesu správy dat produktu a umožňuje, aby byly produkty definovány, uvolňovány a revidovány kontrolovaným způsobem, který je podporován pracovními postupy.</span><span class="sxs-lookup"><span data-stu-id="66f7d-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="66f7d-107">Prostřednictvím verzí produktu a správy technických změn můžete dokumentovat, hodnotit dopad a aplikovat technické změny během celého životního cyklu produktu.</span><span class="sxs-lookup"><span data-stu-id="66f7d-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="66f7d-108">Správa technických změn vám pomáhá plánovat a spravovat verzování produktu a spravovat životní cykly produktu a technických změn.</span><span class="sxs-lookup"><span data-stu-id="66f7d-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="66f7d-109">Zde je seznam jejich hlavních funkcí:</span><span class="sxs-lookup"><span data-stu-id="66f7d-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="66f7d-110">Verzování produktu</span><span class="sxs-lookup"><span data-stu-id="66f7d-110">Product versioning</span></span>
- <span data-ttu-id="66f7d-111">Vylepšená funkce uvolňování produktu, která vám umožní udržovat hlavní data produktu v jedné právnické osobě (technická společnost) a publikovat plně nakonfigurovaný uvolněný produkt do jiných právnických společností.</span><span class="sxs-lookup"><span data-stu-id="66f7d-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="66f7d-112">Pravidla pro ověřování, zda jsou požadované informace zadány před aktivací verze produktu (kontroly připravenosti).</span><span class="sxs-lookup"><span data-stu-id="66f7d-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="66f7d-113">Vylepšená správa životního cyklu produktu prostřednictvím detailní kontroly nad tím, kdy lze uvolněný produkt použít v konkrétních obchodních procesech.</span><span class="sxs-lookup"><span data-stu-id="66f7d-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="66f7d-114">Požadavky na technické změny, které jsou podporovány pracovními postupy</span><span class="sxs-lookup"><span data-stu-id="66f7d-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="66f7d-115">Příkazy k technickým změnám, které jsou podporovány pracovními postupy</span><span class="sxs-lookup"><span data-stu-id="66f7d-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="66f7d-116">Předchozí video ([Možnosti správy změn v Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) je součástí [seznamu videí o Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), které jsou k dispozici na YouTube.</span><span class="sxs-lookup"><span data-stu-id="66f7d-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="66f7d-117">Zapnutí funkcí správy technických změn a dimenze verzí pro systém</span><span class="sxs-lookup"><span data-stu-id="66f7d-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="66f7d-118">Než budete moci používat funkci správy technických změn, musíte povolit funkci *správy technických změn* a její konfigurační klíč.</span><span class="sxs-lookup"><span data-stu-id="66f7d-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="66f7d-119">Pokud chcete také sledovat dimenzi verze produktů v transakcích (volitelně), musíte povolit také funkci *Dimenze verze produktu* a její konfigurační klíč.</span><span class="sxs-lookup"><span data-stu-id="66f7d-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="66f7d-120">Správci mohou funkce zapnout provedením následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="66f7d-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="66f7d-121">Přejděte do [Správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="66f7d-121">Go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace.</span></span>
1. <span data-ttu-id="66f7d-122">Zkontrolovat aktualizace.</span><span class="sxs-lookup"><span data-stu-id="66f7d-122">Check for updates.</span></span>
1. <span data-ttu-id="66f7d-123">Zapněte funkci s názvem *Správa technických změn*.</span><span class="sxs-lookup"><span data-stu-id="66f7d-123">Turn on the feature that is named *Engineering Change Management*.</span></span>
1. <span data-ttu-id="66f7d-124">Chcete-li ji použít, zapněte také funkci s názvem *Verze dimenze produktu*.</span><span class="sxs-lookup"><span data-stu-id="66f7d-124">If you want to use it, also turn on the feature that is named *Product dimension version*.</span></span>

<span data-ttu-id="66f7d-125">Správci mohou zapnout konfigurační klíče provedením následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="66f7d-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="66f7d-126">Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="66f7d-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="66f7d-127">Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.</span><span class="sxs-lookup"><span data-stu-id="66f7d-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="66f7d-128">Rozbalte uzel **Obchod**.</span><span class="sxs-lookup"><span data-stu-id="66f7d-128">Expand the **Trade** node.</span></span>
1. <span data-ttu-id="66f7d-129">Povolte konfigurační klíč pro hlavní funkci výběrem zaškrtávacího políčka **Správa technických změn**.</span><span class="sxs-lookup"><span data-stu-id="66f7d-129">Enable the configuration key for the main feature by selecting the **Engineering Change Management** checkbox.</span></span>
1. <span data-ttu-id="66f7d-130">Rozbalte uzel **Řízení technických změn** a podle potřeby zaškrtněte nebo zrušte zaškrtnutí následujících políček (v závislosti na funkcích, které chcete použít):</span><span class="sxs-lookup"><span data-stu-id="66f7d-130">Expand the **Engineering Change Management** node, and select or clear the following checkboxes as required (depending on the features that you want to use):</span></span>

    - <span data-ttu-id="66f7d-131">**Hledání atributů** - Zaškrtnutím tohoto políčka povolíte [funkce vyhledávání atributů](engineering-attributes-and-search.md).</span><span class="sxs-lookup"><span data-stu-id="66f7d-131">**Attribute search** – Select this checkbox to enable the [attribute search feature](engineering-attributes-and-search.md).</span></span> <span data-ttu-id="66f7d-132">Doporučujeme tuto funkci povolit, ale pokud ji nepoužíváte, můžete toto zaškrtávací políčko zrušit.</span><span class="sxs-lookup"><span data-stu-id="66f7d-132">We recommend enabling this feature, but you can clear this checkbox if you won't use it.</span></span>
    - <span data-ttu-id="66f7d-133">**Řízení změn pro procesní výrobu** - Toto políčko zaškrtněte, pokud chcete pomocí funkcí správy technických změn spravovat změny ve vzorcích pro procesní výrobu.</span><span class="sxs-lookup"><span data-stu-id="66f7d-133">**Change management for process manufacturing** – Select this checkbox if you want to use Engineering change management features to manage changes in formulas for process manufacturing.</span></span> <span data-ttu-id="66f7d-134">Pokud vzorce nemusíte spravovat, můžete toto zaškrtávací políčko zrušit.</span><span class="sxs-lookup"><span data-stu-id="66f7d-134">If you don't have to manage formulas, you can clear this checkbox.</span></span> <span data-ttu-id="66f7d-135">Další informace viz [Spravujte změny v recepturách a jejich látkách](manage-formula-changes.md).</span><span class="sxs-lookup"><span data-stu-id="66f7d-135">For more information, see [Manage changes in formulas and their ingredients](manage-formula-changes.md).</span></span>

1. <span data-ttu-id="66f7d-136">Chcete-li také použít dimenzi verze, zaškrtněte také políčko **Dimenze produktu - verze**.</span><span class="sxs-lookup"><span data-stu-id="66f7d-136">If you also want to use the version dimension, then select the **Product dimension - Version** checkbox.</span></span> <span data-ttu-id="66f7d-137">(Toto zaškrtávací políčko je dále v seznamu, není vnořeno pod uzlem **Správa technických změn**.)</span><span class="sxs-lookup"><span data-stu-id="66f7d-137">(This checkbox is further down the list, not nested under the **Engineering Change Management** node.)</span></span>
1. <span data-ttu-id="66f7d-138">Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="66f7d-138">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66f7d-139">Od dubna 2022 budou licenční klíče pro jak **Správu technických změn**, tak pro **Rozměr produktu - verze** ve výchozím nastavení povoleny pro všechny nové instalace, ale v případě potřeby je stále budete moci deaktivovat.</span><span class="sxs-lookup"><span data-stu-id="66f7d-139">Starting in April 2022, the license keys for both **Engineering Change Management** and **Product dimension - Version** will be enabled by default for all new installations, but you will still be able to disable them if needed.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

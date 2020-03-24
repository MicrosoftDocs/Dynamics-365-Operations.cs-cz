---
title: Přehled dvojího zapisování
description: Toto téma obsahuje přehled dvojího zapisování. Dvojí zapisování je infrastruktura poskytující prakticky v reálném čase mezi aplikacemi řízených modelem Microsoft Dynamics 365 a Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c4a643d4981364cea5b549118c201ac8a9798e02
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113867"
---
# <a name="dual-write-overview"></a><span data-ttu-id="4cfbc-104">Přehled dvojího zapisování</span><span class="sxs-lookup"><span data-stu-id="4cfbc-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a><span data-ttu-id="4cfbc-105">Co je dvojí zapisování?</span><span class="sxs-lookup"><span data-stu-id="4cfbc-105">What is dual-write?</span></span>

<span data-ttu-id="4cfbc-106">Dvojí zapisování je předpřipravená infrastruktura poskytující prakticky v reálném čase mezi aplikacemi řízených modelem v Microsoft Dynamics 365 a Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="4cfbc-107">Při zpracování dat o zákaznících, produktech, osobách a operacích mimo hranice aplikací jsou všechna oddělení v organizaci oprávněna.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="4cfbc-108">Dvojí zapisování poskytuje pevně spojenou obousměrnou integraci mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="4cfbc-109">Jakákoli změna dat v aplikacích Finance and Operations způsobí zápis do aplikace Common Data Service a jakákoli změna dat v Common Data Service způsobí zápis do aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="4cfbc-110">Tento automatizovaný tok dat poskytuje integrované uživatelské prostředí pro celé aplikace.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Datový vztah mezi aplikacemi](media/dual-write-overview.jpg)

<span data-ttu-id="4cfbc-112">Dvojí zápis má dva aspekty: aspekt *infrastruktury* a aspekt *aplikace*.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="4cfbc-113">Infrastruktura</span><span class="sxs-lookup"><span data-stu-id="4cfbc-113">Infrastructure</span></span>

<span data-ttu-id="4cfbc-114">Infrastruktura dvojího zapisování je rozšiřitelná a spolehlivá a obsahuje následující klíčové funkce:</span><span class="sxs-lookup"><span data-stu-id="4cfbc-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="4cfbc-115">Synchronní a obousměrný tok dat mezi aplikacemi</span><span class="sxs-lookup"><span data-stu-id="4cfbc-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="4cfbc-116">Synchronizace spolu s režimy přehrát, pozastavit a catchup pro podporu systému při režimech online a offline/asynchronní.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="4cfbc-117">Možnost synchronizace počátečních dat mezi aplikacemi</span><span class="sxs-lookup"><span data-stu-id="4cfbc-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="4cfbc-118">Konsolidované zobrazení protokolů aktivit a chyb pro správce dat</span><span class="sxs-lookup"><span data-stu-id="4cfbc-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="4cfbc-119">Možnost konfigurovat vlastní výstrahy a prahové hodnoty a přihlásit se k odběru oznámení</span><span class="sxs-lookup"><span data-stu-id="4cfbc-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="4cfbc-120">Intuitivní uživatelské rozhraní (UI) pro filtrování a transformace</span><span class="sxs-lookup"><span data-stu-id="4cfbc-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="4cfbc-121">Schopnost nastavit a zobrazit závislosti a vztahy entity</span><span class="sxs-lookup"><span data-stu-id="4cfbc-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="4cfbc-122">Rozšiřitelnost pro standardní i pro vlastní entity a mapy</span><span class="sxs-lookup"><span data-stu-id="4cfbc-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="4cfbc-123">Spolehlivé řízení životního cyklu aplikací</span><span class="sxs-lookup"><span data-stu-id="4cfbc-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="4cfbc-124">Přednastavené možnosti nastavení pro nové odběratele</span><span class="sxs-lookup"><span data-stu-id="4cfbc-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="4cfbc-125">Přihláška</span><span class="sxs-lookup"><span data-stu-id="4cfbc-125">Application</span></span>

<span data-ttu-id="4cfbc-126">Dvojí zapisování vytvoří mapování mezi koncepty v aplikacích Finance and Operations a koncepty v aplikacích řízených modelem v Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="4cfbc-127">Tato integrace podporuje následující scénáře:</span><span class="sxs-lookup"><span data-stu-id="4cfbc-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="4cfbc-128">Integrovaná hlavní data odběratelů</span><span class="sxs-lookup"><span data-stu-id="4cfbc-128">Integrated customer master</span></span>
+ <span data-ttu-id="4cfbc-129">Přístup k věrnostním kartám odběratelů a k bodům odměny</span><span class="sxs-lookup"><span data-stu-id="4cfbc-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="4cfbc-130">Sjednocené prostředí základního produktu</span><span class="sxs-lookup"><span data-stu-id="4cfbc-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="4cfbc-131">Povědomí o organizační hierarchii</span><span class="sxs-lookup"><span data-stu-id="4cfbc-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="4cfbc-132">Integrovaná hlavní data dodavatelů</span><span class="sxs-lookup"><span data-stu-id="4cfbc-132">Integrated vendor master</span></span>
+ <span data-ttu-id="4cfbc-133">Přístup k referenčním datům financování a daně</span><span class="sxs-lookup"><span data-stu-id="4cfbc-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="4cfbc-134">Práce modulu ceny na požádání</span><span class="sxs-lookup"><span data-stu-id="4cfbc-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="4cfbc-135">Integrované prostředí zpeněžení</span><span class="sxs-lookup"><span data-stu-id="4cfbc-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="4cfbc-136">Schopnost poskytovat interní majetek i aktiva pro odběratele prostřednictvím agentů polí</span><span class="sxs-lookup"><span data-stu-id="4cfbc-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="4cfbc-137">Integrované prostředí vynucení platby</span><span class="sxs-lookup"><span data-stu-id="4cfbc-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="4cfbc-138">Integrované aktivity a poznámky pro data a dokumenty odběratelů</span><span class="sxs-lookup"><span data-stu-id="4cfbc-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="4cfbc-139">Možnost vyhledat dostupnost a podrobnosti zásob na skladě</span><span class="sxs-lookup"><span data-stu-id="4cfbc-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="4cfbc-140">Prostředí P2C</span><span class="sxs-lookup"><span data-stu-id="4cfbc-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="4cfbc-141">Schopnost zpracovávat více adres a rolí prostřednictvím koncepce strany</span><span class="sxs-lookup"><span data-stu-id="4cfbc-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="4cfbc-142">Správa jednoho zdroje pro uživatele</span><span class="sxs-lookup"><span data-stu-id="4cfbc-142">Single source management for users</span></span>
+ <span data-ttu-id="4cfbc-143">Integrované kanály pro maloobchod a marketing</span><span class="sxs-lookup"><span data-stu-id="4cfbc-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="4cfbc-144">Zviditelnění promoakcí a slev</span><span class="sxs-lookup"><span data-stu-id="4cfbc-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="4cfbc-145">Funkce požadavku na služby</span><span class="sxs-lookup"><span data-stu-id="4cfbc-145">Request-for-service functions</span></span>
+ <span data-ttu-id="4cfbc-146">Zjednodušené servisní operace</span><span class="sxs-lookup"><span data-stu-id="4cfbc-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="4cfbc-147">Hlavní důvody pro použití dvojího zapisování</span><span class="sxs-lookup"><span data-stu-id="4cfbc-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="4cfbc-148">Dvojí zapisování poskytuje integraci dat mezi aplikacemi Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="4cfbc-149">Toto robustní rozhraní spojuje prostředí a umožňuje různým obchodním aplikacím vzájemnou spolupráci.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="4cfbc-150">Zde jsou uvedeny hlavní důvody, proč byste měli používat dvojí zápis:</span><span class="sxs-lookup"><span data-stu-id="4cfbc-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="4cfbc-151">Dvojí zapisování poskytuje úzce spojenou, prakticky v reálném čase a obousměrnou integraci mezi aplikacemi Finance and Operations a aplikacemi řízenými modelem v aplikaci Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="4cfbc-152">Tato integrace činí z Microsoft Dynamics 365 univerzální nástroj pro všechna vaše obchodní řešení.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="4cfbc-153">Zákazníci, kteří používají Dynamics 365 Finance a Dynamics 365 Supply Chain Management, ale používají řešení pro řízení vztahů se zákazníky (CRM) jiného typu než nabízí společnost Microsoft, přecházení k Dynamics 365 díky podpoře dvojího zapisování.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="4cfbc-154">Data od odběratelů, produktů, operací, projektů a Internetu věcí (IoT) automaticky proudí do Common Data Service pomocí dvojího zapisování.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="4cfbc-155">Toto připojení je velmi užitečné pro podniky, které se zajímaní o rozšíření Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="4cfbc-156">Infrastruktura dvojího zapisování se řídí podle principu "bez kódu/nízký kód".</span><span class="sxs-lookup"><span data-stu-id="4cfbc-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="4cfbc-157">Chcete-li rozšířit standardní mapy tabulek a tabulek a zahrnout vlastní mapy, je nezbytné pouze minimální úsilí.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="4cfbc-158">Dvojí zapisování podporuje režim online i režim offline.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="4cfbc-159">Společnost Microsoft je jediná společnost nabízející podporu pro režimy online a offline.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="4cfbc-160">Co znamená dvojí zapisování pro uživatele a architekty produktů CRM?</span><span class="sxs-lookup"><span data-stu-id="4cfbc-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="4cfbc-161">Dvojí zapisování automatizuje tok dat mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="4cfbc-162">V budoucích verzích budou pojmy v aplikacích řízených modelem v aplikaci Dynamics 365 (například odběratel, kontakt, nabídka a objednávka) odstupňovány pro zákazníky se středním podílem na trhu a s vyšším podílem na trhu.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="4cfbc-163">V prvním vydání je většina automatizace zpracována řešeními dvojího zápisu.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="4cfbc-164">V příštích verzích se tyto řešení stanou součástí aplikace Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="4cfbc-165">Pochopíte-li nadcházející změny v aplikaci Common Data Service, můžete v dlouhodobém období ušetřit úsilí.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="4cfbc-166">Následují některé zásadní změny:</span><span class="sxs-lookup"><span data-stu-id="4cfbc-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="4cfbc-167">Common Data Service bude mít nové koncepce, jako je například společnost nebo smluvní strana.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="4cfbc-168">Tyto koncepce budou mít vliv na všechny aplikace vytvořené na Common Data Service, například Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service a Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="4cfbc-169">Aktivity a poznámky jsou sjednoceny a rozšířeny tak, aby podporovaly C1 (uživatelé systému) i C2 (zákazníci v systému).</span><span class="sxs-lookup"><span data-stu-id="4cfbc-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="4cfbc-170">Následují některé nadcházející změny v Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="4cfbc-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="4cfbc-171">Datový typ desetinné číslo nahradí datový typ peníze.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="4cfbc-172">Datum vyčerpání bude podporovat minulá, současná a budoucí data na stejném místě.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="4cfbc-173">Pro měnu a směnné kurzy bude existovat více podpor a bude revidováno rozhraní (API) pro aplikaci **Směnný kurz**.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="4cfbc-174">Převody jednotek budou podporovány.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="4cfbc-175">Další informace o nadcházejících změnách naleznete v tématu [Data v Common Data Service - fáze 1 a 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span><span class="sxs-lookup"><span data-stu-id="4cfbc-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span></span>

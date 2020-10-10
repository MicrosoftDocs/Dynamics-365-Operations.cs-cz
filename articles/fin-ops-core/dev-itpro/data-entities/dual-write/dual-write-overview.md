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
ms.openlocfilehash: 1eb5e4ea8d086baeee686ccb3d044b3ef9d2a4fa
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818565"
---
# <a name="dual-write-overview"></a><span data-ttu-id="83a0b-104">Přehled dvojího zapisování</span><span class="sxs-lookup"><span data-stu-id="83a0b-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="83a0b-105">Co je dvojí zapisování?</span><span class="sxs-lookup"><span data-stu-id="83a0b-105">What is dual-write?</span></span>

<span data-ttu-id="83a0b-106">Dvojí zapisování je předpřipravená infrastruktura poskytující prakticky v reálném čase mezi aplikacemi pro zapojení zákazníků a aplikacemi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="83a0b-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="83a0b-107">Při zpracování dat o zákaznících, produktech, osobách a operacích mimo hranice aplikací jsou všechna oddělení v organizaci oprávněna.</span><span class="sxs-lookup"><span data-stu-id="83a0b-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="83a0b-108">Dvojí zapisování poskytuje pevně spojenou obousměrnou integraci mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="83a0b-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="83a0b-109">Jakákoli změna dat v aplikacích Finance and Operations způsobí zápis do aplikace Common Data Service a jakákoli změna dat v Common Data Service způsobí zápis do aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="83a0b-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="83a0b-110">Tento automatizovaný tok dat poskytuje integrované uživatelské prostředí pro celé aplikace.</span><span class="sxs-lookup"><span data-stu-id="83a0b-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Datový vztah mezi aplikacemi](media/dual-write-overview.jpg)

<span data-ttu-id="83a0b-112">Dvojí zápis má dva aspekty: aspekt *infrastruktury* a aspekt *aplikace*.</span><span class="sxs-lookup"><span data-stu-id="83a0b-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="83a0b-113">Infrastruktura</span><span class="sxs-lookup"><span data-stu-id="83a0b-113">Infrastructure</span></span>

<span data-ttu-id="83a0b-114">Infrastruktura dvojího zapisování je rozšiřitelná a spolehlivá a obsahuje následující klíčové funkce:</span><span class="sxs-lookup"><span data-stu-id="83a0b-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="83a0b-115">Synchronní a obousměrný tok dat mezi aplikacemi</span><span class="sxs-lookup"><span data-stu-id="83a0b-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="83a0b-116">Synchronizace spolu s režimy přehrát, pozastavit a catchup pro podporu systému při režimech online a offline/asynchronní.</span><span class="sxs-lookup"><span data-stu-id="83a0b-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="83a0b-117">Možnost synchronizace počátečních dat mezi aplikacemi</span><span class="sxs-lookup"><span data-stu-id="83a0b-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="83a0b-118">Kombinované zobrazení protokolů aktivit a chyb pro správce dat</span><span class="sxs-lookup"><span data-stu-id="83a0b-118">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="83a0b-119">Možnost konfigurovat vlastní výstrahy a prahové hodnoty a přihlásit se k odběru oznámení</span><span class="sxs-lookup"><span data-stu-id="83a0b-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="83a0b-120">Intuitivní uživatelské rozhraní (UI) pro filtrování a transformace</span><span class="sxs-lookup"><span data-stu-id="83a0b-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="83a0b-121">Schopnost nastavit a zobrazit závislosti a vztahy entity</span><span class="sxs-lookup"><span data-stu-id="83a0b-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="83a0b-122">Rozšiřitelnost pro standardní i pro vlastní entity a mapy</span><span class="sxs-lookup"><span data-stu-id="83a0b-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="83a0b-123">Spolehlivé řízení životního cyklu aplikací</span><span class="sxs-lookup"><span data-stu-id="83a0b-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="83a0b-124">Přednastavené možnosti nastavení pro nové odběratele</span><span class="sxs-lookup"><span data-stu-id="83a0b-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="83a0b-125">Přihláška</span><span class="sxs-lookup"><span data-stu-id="83a0b-125">Application</span></span>

<span data-ttu-id="83a0b-126">Duální zápis vytvoří mapování mezi koncepty v aplikacích Finance and Operations a koncepty v aplikacích pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="83a0b-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="83a0b-127">Tato integrace podporuje následující scénáře:</span><span class="sxs-lookup"><span data-stu-id="83a0b-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="83a0b-128">Integrovaná hlavní data odběratelů</span><span class="sxs-lookup"><span data-stu-id="83a0b-128">Integrated customer master</span></span>
+ <span data-ttu-id="83a0b-129">Přístup k věrnostním kartám odběratelů a k bodům odměny</span><span class="sxs-lookup"><span data-stu-id="83a0b-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="83a0b-130">Sjednocené prostředí základního produktu</span><span class="sxs-lookup"><span data-stu-id="83a0b-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="83a0b-131">Povědomí o organizační hierarchii</span><span class="sxs-lookup"><span data-stu-id="83a0b-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="83a0b-132">Integrovaná hlavní data dodavatelů</span><span class="sxs-lookup"><span data-stu-id="83a0b-132">Integrated vendor master</span></span>
+ <span data-ttu-id="83a0b-133">Přístup k referenčním datům financování a daně</span><span class="sxs-lookup"><span data-stu-id="83a0b-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="83a0b-134">Práce modulu ceny na požádání</span><span class="sxs-lookup"><span data-stu-id="83a0b-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="83a0b-135">Integrované prostředí zpeněžení</span><span class="sxs-lookup"><span data-stu-id="83a0b-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="83a0b-136">Schopnost poskytovat interní majetek i aktiva pro odběratele prostřednictvím agentů polí</span><span class="sxs-lookup"><span data-stu-id="83a0b-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="83a0b-137">Integrované prostředí vynucení platby</span><span class="sxs-lookup"><span data-stu-id="83a0b-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="83a0b-138">Integrované aktivity a poznámky pro data a dokumenty odběratelů</span><span class="sxs-lookup"><span data-stu-id="83a0b-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="83a0b-139">Možnost vyhledat dostupnost a podrobnosti zásob na skladě</span><span class="sxs-lookup"><span data-stu-id="83a0b-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="83a0b-140">Prostředí P2C</span><span class="sxs-lookup"><span data-stu-id="83a0b-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="83a0b-141">Schopnost zpracovávat více adres a rolí prostřednictvím koncepce strany</span><span class="sxs-lookup"><span data-stu-id="83a0b-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="83a0b-142">Správa jednoho zdroje pro uživatele</span><span class="sxs-lookup"><span data-stu-id="83a0b-142">Single source management for users</span></span>
+ <span data-ttu-id="83a0b-143">Integrované kanály pro maloobchod a marketing</span><span class="sxs-lookup"><span data-stu-id="83a0b-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="83a0b-144">Zviditelnění promoakcí a slev</span><span class="sxs-lookup"><span data-stu-id="83a0b-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="83a0b-145">Funkce požadavku na služby</span><span class="sxs-lookup"><span data-stu-id="83a0b-145">Request-for-service functions</span></span>
+ <span data-ttu-id="83a0b-146">Zjednodušené servisní operace</span><span class="sxs-lookup"><span data-stu-id="83a0b-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="83a0b-147">Hlavní důvody pro použití dvojího zapisování</span><span class="sxs-lookup"><span data-stu-id="83a0b-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="83a0b-148">Dvojí zapisování poskytuje integraci dat mezi aplikacemi Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="83a0b-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="83a0b-149">Toto robustní rozhraní spojuje prostředí a umožňuje různým obchodním aplikacím vzájemnou spolupráci.</span><span class="sxs-lookup"><span data-stu-id="83a0b-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="83a0b-150">Zde jsou uvedeny hlavní důvody, proč byste měli používat dvojí zápis:</span><span class="sxs-lookup"><span data-stu-id="83a0b-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="83a0b-151">Dvojí zapisování poskytuje úzce spojenou, prakticky v reálném čase a obousměrnou integraci mezi aplikacemi Finance and Operations a aplikacemi řízenými modelem v aplikaci Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="83a0b-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="83a0b-152">Tato integrace činí z Microsoft Dynamics 365 univerzální nástroj pro všechna vaše obchodní řešení.</span><span class="sxs-lookup"><span data-stu-id="83a0b-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="83a0b-153">Zákazníci, kteří používají Dynamics 365 Finance a Dynamics 365 Supply Chain Management, ale používají řešení pro řízení vztahů se zákazníky (CRM) jiného typu než nabízí společnost Microsoft, přecházení k Dynamics 365 díky podpoře dvojího zapisování.</span><span class="sxs-lookup"><span data-stu-id="83a0b-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="83a0b-154">Data od odběratelů, produktů, operací, projektů a Internetu věcí (IoT) automaticky proudí do Common Data Service pomocí dvojího zapisování.</span><span class="sxs-lookup"><span data-stu-id="83a0b-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="83a0b-155">Toto připojení je užitečné pro podniky, které se zajímaní o rozšíření Power Platform.</span><span class="sxs-lookup"><span data-stu-id="83a0b-155">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="83a0b-156">Infrastruktura dvojího zapisování se řídí podle principu "bez kódu/nízký kód".</span><span class="sxs-lookup"><span data-stu-id="83a0b-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="83a0b-157">Chcete-li rozšířit standardní mapy tabulek a tabulek a zahrnout vlastní mapy, je nezbytné pouze minimální úsilí.</span><span class="sxs-lookup"><span data-stu-id="83a0b-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="83a0b-158">Dvojí zapisování podporuje režim online i režim offline.</span><span class="sxs-lookup"><span data-stu-id="83a0b-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="83a0b-159">Společnost Microsoft je jediná společnost nabízející podporu pro režimy online a offline.</span><span class="sxs-lookup"><span data-stu-id="83a0b-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="83a0b-160">Co znamená duální zápis pro vývojáře a architekty aplikací pro zapojení zákazníků?</span><span class="sxs-lookup"><span data-stu-id="83a0b-160">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="83a0b-161">Duální zápis automatizuje tok dat mezi aplikacemi Finance and Operations a aplikacemi pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="83a0b-161">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="83a0b-162">Duální zápis se skládá ze dvou řešení AppSource, která jsou nainstalována na Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="83a0b-162">Dual-write consists of two AppSource solutions that are installed on Common Data Service.</span></span> <span data-ttu-id="83a0b-163">Tato řešení rozšiřují schéma entity, moduly plugin a pracovní postupy v Common Data Service, aby mohly škálovat na velikost ERP.</span><span class="sxs-lookup"><span data-stu-id="83a0b-163">The solutions expand the entity schema, plugins, and workflows on Common Data Service so that they can scale to ERP size.</span></span> <span data-ttu-id="83a0b-164">Pro úspěšnou implementaci musí vývojáři a architekti aplikací pro zapojení zákazníků tyto změny pochopit a spolupracovat se svými protějšky v aplikacích Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="83a0b-164">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="83a0b-165">Kvůli vytvoření parity s aplikacemi Finance and Operations provádí duální zápis některé zásadní změny ve schématu Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="83a0b-165">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Common Data Service schema.</span></span> <span data-ttu-id="83a0b-166">Pokud plánu rozumíte, můžete se v budoucnu vyhnout úpravám návrhu a vývoje.</span><span class="sxs-lookup"><span data-stu-id="83a0b-166">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="83a0b-167">Když je instalován balíček duálního zápisu AppSource, Common Data Service bude mít nové koncety, jako je společnost nebo zainteresovaná strana.</span><span class="sxs-lookup"><span data-stu-id="83a0b-167">When the dual-write AppSource package is installed, Common Data Service will have new concepts such as company and party.</span></span> <span data-ttu-id="83a0b-168">Tyto koncepty pomáhají aplikacím postaveným na Common Data Service, včetně Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service a Dynamics 365 Field Service, bezproblémově komunikovat s aplikacemi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="83a0b-168">These concepts help applications built on Common Data Service, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="83a0b-169">Aktivity a poznámky jsou sjednoceny a rozšířeny tak, aby podporovaly C1 (uživatelé systému) i C2 (zákazníci v systému).</span><span class="sxs-lookup"><span data-stu-id="83a0b-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="83a0b-170">Aby se zabránilo ztrátě dat při přenosu měny mezi aplikacemi Finance and Operations a Common Data Service, budete moci rozšířit počet desetinných míst v datovém typu měny aplikací pro zapojení zákazníků.</span><span class="sxs-lookup"><span data-stu-id="83a0b-170">To prevent data loss during currency transmission between Finance and Operations apps and the Common Data Service, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="83a0b-171">Tato funkce automaticky přenese existující záznamy do nového rozšířeného stavu ve vrstvě metadat.</span><span class="sxs-lookup"><span data-stu-id="83a0b-171">The feature autotranslates existing records to the new extended state at the metadata layer.</span></span> <span data-ttu-id="83a0b-172">Během tohoto procesu je hodnota měny převedena na desítková data, nikoli na peněžní, a hodnota měny podporuje 10 desetinných míst.</span><span class="sxs-lookup"><span data-stu-id="83a0b-172">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="83a0b-173">Pro tuto funkci je třeba se registrovat a organizace, které nepotřebují více než 4 desetinná místa přesnosti, se registrovat nemusí.</span><span class="sxs-lookup"><span data-stu-id="83a0b-173">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="83a0b-174">Další informace viz [Migrace datového typu měny pro duální zápis](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="83a0b-174">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="83a0b-175">[Platnost od](../../dev-tools/date-effectivity.md) bude přidán do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="83a0b-175">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Common Data Service.</span></span> <span data-ttu-id="83a0b-176">Bude podporovat minulá, současná a budoucí data ve stejné entitě.</span><span class="sxs-lookup"><span data-stu-id="83a0b-176">It will support past, present, and future data on the same entity.</span></span>

+ <span data-ttu-id="83a0b-177">[Převody jednotek](../../../../supply-chain/pim/tasks/manage-unit-measure.md) produktu jsou podporovány pro produkty, nabídky, objednávky a faktury.</span><span class="sxs-lookup"><span data-stu-id="83a0b-177">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="83a0b-178">Další informace o nadcházejících změnách najdete v části [Co je nového nebo co se změnilo ohledně duálního zápisu](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="83a0b-178">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>


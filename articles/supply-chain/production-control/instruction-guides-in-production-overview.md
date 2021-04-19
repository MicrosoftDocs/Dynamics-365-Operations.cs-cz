---
title: Poskytování příruček v hybridní realitě pro pracovníky ve výrobě
description: Toto téma vysvětluje, jak modul řízení výroby v Microsoft Dynamics 365 Supply Chain Management integrovat s Dynamics 365 Guides.
author: cabeln
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 59fe3996013737198d4fbc86d64f8ef9dbe035e4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829347"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="94d87-103">Poskytování příruček v hybridní realitě pro pracovníky ve výrobě</span><span class="sxs-lookup"><span data-stu-id="94d87-103">Provide mixed-reality Guides for workers in production</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="94d87-104">Pracovníci ve výrobních procesech využijí relevantní pokyny, které jsou jim poskytovány ve správný čas v souvislosti s jejich prací.</span><span class="sxs-lookup"><span data-stu-id="94d87-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="94d87-105">*Pokyny* se používají v několika oblastech práce, mezi které patří: montáž, servis, provozu, certifikace a bezpečnost.</span><span class="sxs-lookup"><span data-stu-id="94d87-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="94d87-106">Průběžná instruktáž ve všech těchto základních firemních funkcích pomůže pracovníkům dosáhnout lepších výsledků a lépe pracovat.</span><span class="sxs-lookup"><span data-stu-id="94d87-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="94d87-107">Úvod</span><span class="sxs-lookup"><span data-stu-id="94d87-107">Introduction</span></span>

<span data-ttu-id="94d87-108">Pokyny můžete poskytovat různými způsoby.</span><span class="sxs-lookup"><span data-stu-id="94d87-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="94d87-109">Jeden dodávaný efektivní systém využívá [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="94d87-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="94d87-110">Dynamics 365 Guides dokáže vaše zaměstnance posílit pomocí praktického učení.</span><span class="sxs-lookup"><span data-stu-id="94d87-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="94d87-111">Můžete definovat standardizované procesy s podrobnými pokyny, které vaše zaměstnance navedou na potřebné nástroje a součásti a ukážou jim, jak tyto nástroje používat v reálných pracovních situacích.</span><span class="sxs-lookup"><span data-stu-id="94d87-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="94d87-112">Příručky můžete připojit k různým aspektům řízení výroby, mezi které patří:</span><span class="sxs-lookup"><span data-stu-id="94d87-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="94d87-113">Prostředky</span><span class="sxs-lookup"><span data-stu-id="94d87-113">Resources</span></span>](#resources)
- [<span data-ttu-id="94d87-114">Skupiny prostředků</span><span class="sxs-lookup"><span data-stu-id="94d87-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="94d87-115">Uvolněné produkty</span><span class="sxs-lookup"><span data-stu-id="94d87-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="94d87-116">Receptury</span><span class="sxs-lookup"><span data-stu-id="94d87-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="94d87-117">Verze receptury</span><span class="sxs-lookup"><span data-stu-id="94d87-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="94d87-118">Kusovníky</span><span class="sxs-lookup"><span data-stu-id="94d87-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="94d87-119">Verze kusovníků</span><span class="sxs-lookup"><span data-stu-id="94d87-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="94d87-120">Postupy</span><span class="sxs-lookup"><span data-stu-id="94d87-120">Routes</span></span>](#routes)
- [<span data-ttu-id="94d87-121">Verze postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="94d87-122">Vztahy operací postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="94d87-123">Příručky můžete rovněž připojit ke správě majetku.</span><span class="sxs-lookup"><span data-stu-id="94d87-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="94d87-124">Další informace o této možnosti najdete v tématu [Integrace Dynamics 365 Supply Chain Management (Správa majetku) s Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="94d87-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="94d87-125">Když si pracovník v první linii vybere prostřednictvím Supply Chain Management v dílně nějaký úkol, uvidí na úkolovém lístku [příslušné příručky](#logic).</span><span class="sxs-lookup"><span data-stu-id="94d87-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="94d87-126">Když si pracovník vybere konkrétní příručku, ukáže se na obrazovce kód QR příslušné příručky.</span><span class="sxs-lookup"><span data-stu-id="94d87-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="94d87-127">Pracovník pak pomocí svých HoloLens naskenuje kód QR, který spustí aplikaci Guides a zobrazí požadované pokyny.</span><span class="sxs-lookup"><span data-stu-id="94d87-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="94d87-128">V následujících pododdílech je popsáno několik vybraných scénářů, ve kterých mohou firmy z různých odvětví vidět největší hodnotu při použití aplikace Guides k prezentaci pokynů pro výrobu.</span><span class="sxs-lookup"><span data-stu-id="94d87-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="94d87-129">Sestavení</span><span class="sxs-lookup"><span data-stu-id="94d87-129">Assembly</span></span>

<span data-ttu-id="94d87-130">![Použití aplikace Guides při montáži](media/instruction-guides-hero-assembly.png "Použití aplikace Guides při servisu")</span><span class="sxs-lookup"><span data-stu-id="94d87-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="94d87-131">Pokyny v montážních operacích ukazují pracovníkům potřebné nástroje a součásti a způsob, jakým se používají v reálných pracovních situacích.</span><span class="sxs-lookup"><span data-stu-id="94d87-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="94d87-132">Manažeři výroby mohou vytvářet a přiřazovat příručky například pro [výrobní postupy](routes-operations.md), [vztahy mezi operacemi](routes-operations.md#operation-relations) nebo [kusovníky](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="94d87-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="94d87-133">V dílně najdou pracovníci příslušné pokyny u odpovídající operace.</span><span class="sxs-lookup"><span data-stu-id="94d87-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="94d87-134">Servis</span><span class="sxs-lookup"><span data-stu-id="94d87-134">Service</span></span>

<span data-ttu-id="94d87-135">![Použití aplikace Guides při servisu](media/instruction-guides-hero-service.png "Použití aplikace Guides při servisu")</span><span class="sxs-lookup"><span data-stu-id="94d87-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="94d87-136">Vybavte techniky pokyny v místě výkonu práce, což eliminuje potřebu plánování dalších návštěv.</span><span class="sxs-lookup"><span data-stu-id="94d87-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="94d87-137">Manažeři servisu mohou příručky přiřadit například ke konkrétním [produktům](../../commerce/product.md), které podstupují posouzení kvality.</span><span class="sxs-lookup"><span data-stu-id="94d87-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="94d87-138">Kvalita</span><span class="sxs-lookup"><span data-stu-id="94d87-138">Quality</span></span>

<span data-ttu-id="94d87-139">![Použití aplikace Guides při kontrole kvality](media/instruction-guides-hero-quality.png "Použití aplikace Guides při kontrole kvality")</span><span class="sxs-lookup"><span data-stu-id="94d87-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="94d87-140">Při zavádění nových procesů můžete přeměnou znalostí zaměstnanců na opakovaně použitelný nástroj zajistit větší konzistenci.</span><span class="sxs-lookup"><span data-stu-id="94d87-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="94d87-141">Manažeři kvality mohou příručky přiřadit například ke konkrétním [produktům](../../commerce/product.md), které podstupují posouzení kvality.</span><span class="sxs-lookup"><span data-stu-id="94d87-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="94d87-142">Certifikáty</span><span class="sxs-lookup"><span data-stu-id="94d87-142">Certifications</span></span>

<span data-ttu-id="94d87-143">![Použití aplikace Guides při úkolech spojených s certifikací](media/instruction-guides-hero-certification.png "Použití aplikace Guides při úkolech spojených s certifikací")</span><span class="sxs-lookup"><span data-stu-id="94d87-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="94d87-144">Rychlou identifikací toho, kdo a kde potřebuje pomoc, můžete zajistit, aby každý zaměstnanec splňoval vysoké standardy.</span><span class="sxs-lookup"><span data-stu-id="94d87-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="94d87-145">Bezpečnost</span><span class="sxs-lookup"><span data-stu-id="94d87-145">Safety</span></span>

<span data-ttu-id="94d87-146">![Použití aplikace Guides v pokynech pro bezpečnost práce](media/instruction-guides-hero-safety.png "Použití aplikace Guides v pokynech pro bezpečnost práce")</span><span class="sxs-lookup"><span data-stu-id="94d87-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="94d87-147">Připravte pokyny, které procházejí nebezpečné postupy virtuálně předtím, než se realizují ve fyzickém prostředí.</span><span class="sxs-lookup"><span data-stu-id="94d87-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="94d87-148">Díky hybridní realitě mohou pracovníci nebezpečné postupy zažít virtuálně.</span><span class="sxs-lookup"><span data-stu-id="94d87-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="94d87-149">Vedoucí výroby mohou připravit specializované pokyny pro manipulaci s nebezpečným materiálem nebo choulostivé manipulační postupy a přiřadit je k [vyráběným položkám](../../commerce/product.md), [postupům](routes-operations.md) a [operacím](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="94d87-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="94d87-150">Začínáme s pokyny a aplikací Guides</span><span class="sxs-lookup"><span data-stu-id="94d87-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="94d87-151">Chcete-li povolit pokyny ve výrobních procesech, nabízí Supply Chain Management integraci s Dynamics 365 Guides.</span><span class="sxs-lookup"><span data-stu-id="94d87-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="94d87-152">K vytváření, údržbě a přiřazování pokynů v hybridní realitě k výrobním prostředkům a práci se vyžaduje licencovaná a nainstalovaná instance aplikace Guides.</span><span class="sxs-lookup"><span data-stu-id="94d87-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="94d87-153">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="94d87-153">Prerequisites</span></span>

<span data-ttu-id="94d87-154">Abyste mohli tuto funkci používat, musí váš systém obsahovat:</span><span class="sxs-lookup"><span data-stu-id="94d87-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="94d87-155">Dynamics 365 Supply Chain Management verze 10.0.15 nebo novější</span><span class="sxs-lookup"><span data-stu-id="94d87-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="94d87-156">[Duální zápis](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) pro aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="94d87-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="94d87-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) verze 400.0.1.48 nebo novější</span><span class="sxs-lookup"><span data-stu-id="94d87-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="94d87-158">Zapnutí funkce</span><span class="sxs-lookup"><span data-stu-id="94d87-158">Turn on the feature</span></span>

<span data-ttu-id="94d87-159">Chcete-li tuto funkci ve svém systému zpřístupnit, musíte povolit její konfigurační klíče.</span><span class="sxs-lookup"><span data-stu-id="94d87-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="94d87-160">Stačí, když to uděláte jen jednou.</span><span class="sxs-lookup"><span data-stu-id="94d87-160">You only need to do this once.</span></span> <span data-ttu-id="94d87-161">Jako správce musíte provést následující postup:</span><span class="sxs-lookup"><span data-stu-id="94d87-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="94d87-162">Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="94d87-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="94d87-163">Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.</span><span class="sxs-lookup"><span data-stu-id="94d87-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="94d87-164">Rozbalte oddíl **Hybridní realita** a zaškrtněte políčko **Příručka v hybridní realitě**.</span><span class="sxs-lookup"><span data-stu-id="94d87-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="94d87-165">Rozbalte oddíl **Řízení výroby** a zaškrtněte políčko **Výrobní pokyny**.</span><span class="sxs-lookup"><span data-stu-id="94d87-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="94d87-166">Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="94d87-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="94d87-167">Konfigurace způsobu, jakým se aplikace Guides zobrazuje v dílně</span><span class="sxs-lookup"><span data-stu-id="94d87-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="94d87-168">Chcete-li nakonfigurovat, jak se aplikace Guides bude zobrazovat v dílně, přejděte na **Hybridní realita \>Dynamics 365 Guides\> Konfigurovat integraci aplikace Guides**.</span><span class="sxs-lookup"><span data-stu-id="94d87-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="94d87-169">![Konfigurace integrace aplikace Guides ve výrobě](media/instruction-guides-configure-integration.png "Konfigurace integrace aplikace Guides ve výrobě")</span><span class="sxs-lookup"><span data-stu-id="94d87-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="94d87-170">Nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="94d87-170">Set the following fields:</span></span>

- <span data-ttu-id="94d87-171">**URL adresa Microsoft Dataverse** - Zadejte adresu URL pro prostředí Microsoft Dataverse, ve kterém vytvářet své průvodce.</span><span class="sxs-lookup"><span data-stu-id="94d87-171">**Microsoft Dataverse URL** - Specify the URL for the Microsoft Dataverse environment where you create your Guides.</span></span> <span data-ttu-id="94d87-172">Formát je „contoso.crm4.dynamics.com“, kde první část adresy URL je obvykle pojmenována po vaší organizaci (například „contoso.“), Druhá část je specifická pro datovou oblast vašeho prostředí (například „crm4.“) a poslední částí je doména (například „dynamics.com“).</span><span class="sxs-lookup"><span data-stu-id="94d87-172">The format is "contoso.crm4.dynamics.com", where the first part of the URL is typically named after your organization (such as "contoso."), the second part is specific to the data region of your environment (such as "crm4."), and the last part is the domain (such as "dynamics.com").</span></span> <span data-ttu-id="94d87-173">Jedním ze způsobů, jak najít správnou adresu URL, je přechod na [home.dynamics.com](https://home.dynamics.com/) a otevření aplikace Guides.</span><span class="sxs-lookup"><span data-stu-id="94d87-173">One way to find the right URL is to go to [home.dynamics.com](https://home.dynamics.com/) and then open your Guides app.</span></span> <span data-ttu-id="94d87-174">Po otevření aplikace Guides se adresa URL zobrazí v panelu adresy vašeho prohlížeče (vezměte pouze základní adresu URL, která by se měla podobat předchozímu příkladu).</span><span class="sxs-lookup"><span data-stu-id="94d87-174">When Guides opens, you will see the URL in the address bar of your browser (only take the base URL, which should resemble the previous example).</span></span> <span data-ttu-id="94d87-175">Tato hodnota se používá k vytvoření adres vašich příruček a bude zakódována do kódů QR.</span><span class="sxs-lookup"><span data-stu-id="94d87-175">This value is used to compose addresses for your guides and will be encoded into the QR codes."</span></span>
- <span data-ttu-id="94d87-176">**Velikost kódu QR** – nastavte velikost vykresleného kódu QR.</span><span class="sxs-lookup"><span data-stu-id="94d87-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="94d87-177">Doporučujeme zvolit velikost, která vyplní většinu vaší obrazovky, ale ne více.</span><span class="sxs-lookup"><span data-stu-id="94d87-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="94d87-178">Vhodná hodnota je zpravidla *15*.</span><span class="sxs-lookup"><span data-stu-id="94d87-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="94d87-179">**Úroveň opravy chyb kódu QR** – nastavte členitost kódu QR.</span><span class="sxs-lookup"><span data-stu-id="94d87-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="94d87-180">Vyšší členitost pomáhá zvýšit spolehlivost kódu, ale **Velikost kódu QR** musí být dostatečně velká, aby podporovala detaily vyžadované vámi vybranou úrovní opravy.</span><span class="sxs-lookup"><span data-stu-id="94d87-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>

> [!TIP]
> - <span data-ttu-id="94d87-181">Kódy QR, které jsou pro váš displej příliš velké, se budou déle vykreslovat a následně se zmenší, aby se vešly na displej.</span><span class="sxs-lookup"><span data-stu-id="94d87-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="94d87-182">Tím nic nezískáte.</span><span class="sxs-lookup"><span data-stu-id="94d87-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="94d87-183">Kódy QR, které jsou příliš malé, mohou snížit schopnost HoloLens správně načíst kód v některých prostředích.</span><span class="sxs-lookup"><span data-stu-id="94d87-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="94d87-184">Doporučujeme otestovat nastavení pro každé zařízení, které bude kódy QR zobrazovat uživatelům HoloLens.</span><span class="sxs-lookup"><span data-stu-id="94d87-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="94d87-185">Zvolte nastavení, které zajistí dostatečnou čitelnost v prostředí vaší dílny.</span><span class="sxs-lookup"><span data-stu-id="94d87-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="94d87-186">Získání přehledu přiřazení všech příruček</span><span class="sxs-lookup"><span data-stu-id="94d87-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="94d87-187">Na stránce **Všechny příručky** si můžete prohlédnout seznam všech dostupných příruček ve vaší organizaci a jejich přiřazení k výrobním procesům a prostředkům.</span><span class="sxs-lookup"><span data-stu-id="94d87-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="94d87-188">Otevřete ji tak, že přejdete na **Hybridní realita \> Příručky \> Všechny příručky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="94d87-189">V horní části seznamu se zobrazují všechny dostupné příručky a pole, které můžete použít k filtrování seznamu.</span><span class="sxs-lookup"><span data-stu-id="94d87-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="94d87-190">V dolní části seznamu se zobrazují všechna přiřazení příručky a panel nástrojů pro jejich správu.</span><span class="sxs-lookup"><span data-stu-id="94d87-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="94d87-191">![Správa příruček](media/instruction-guides-allguides.png "Správa příruček")</span><span class="sxs-lookup"><span data-stu-id="94d87-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="94d87-192">V následujících oddílech jsou popsány typy objektů, ke kterým můžete příručky přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="94d87-193">Každá přiřazená příručka obsahuje pokyny, které se automaticky připojí k příslušným výrobním úkolům a budou dostupné v dílně.</span><span class="sxs-lookup"><span data-stu-id="94d87-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="94d87-194">Přidružení příručky k prostředku</span><span class="sxs-lookup"><span data-stu-id="94d87-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="94d87-195">Přidáním příručky k [prostředku](operations-resources.md) nabídnete tuto příručku v kontextu relevantních výrobních úkolů.</span><span class="sxs-lookup"><span data-stu-id="94d87-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="94d87-196">Typický scénář využívající prostředky</span><span class="sxs-lookup"><span data-stu-id="94d87-196">Typical scenario using resources</span></span>

<span data-ttu-id="94d87-197">K nějakému stroji můžete například připojit příručku s obecnými pokyny k obsluze a bezpečnosti práce.</span><span class="sxs-lookup"><span data-stu-id="94d87-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="94d87-198">Tato příručka pak bude dostupná u každého úkolu, který se na tomto stroji bude provádět.</span><span class="sxs-lookup"><span data-stu-id="94d87-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="94d87-199">Přidání příručky k prostředku</span><span class="sxs-lookup"><span data-stu-id="94d87-199">Add a Guide to a resource</span></span>

<span data-ttu-id="94d87-200">Příručku přidáte k prostředku takto:</span><span class="sxs-lookup"><span data-stu-id="94d87-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="94d87-201">Přejděte na **Řízení výroby \> Nastavení \> Prostředky \> Prostředky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="94d87-202">V podokně seznamu vyberte prostředek, ke kterému chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-203">Rozbalte pevnou záložku **Přidružené příručky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="94d87-204">Na panelu nástrojů **Přidružené příručky** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="94d87-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="94d87-205">Do mřížky je přidán nový řádek.</span><span class="sxs-lookup"><span data-stu-id="94d87-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="94d87-206">Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="94d87-207">Pokud máte velký počet příruček, můžete filtrováním seznamu najít tu, kterou hledáte.</span><span class="sxs-lookup"><span data-stu-id="94d87-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="94d87-208">![Správa příruček](media/instruction-guides-allguides.png "Správa příruček")</span><span class="sxs-lookup"><span data-stu-id="94d87-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="94d87-209">Přidružení příručky ke skupině prostředků</span><span class="sxs-lookup"><span data-stu-id="94d87-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="94d87-210">Příručky můžete přidat ke [skupinám prostředků](tasks/define-discrete-manufacturing-resource-group.md), pokud je používáte ke správě skupin strojů, výrobních linek nebo pracovních buněk.</span><span class="sxs-lookup"><span data-stu-id="94d87-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="94d87-211">Typické scénáře využívající skupiny prostředků</span><span class="sxs-lookup"><span data-stu-id="94d87-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="94d87-212">**Příklad 1:** Definovali jste skupinu prostředků pro několik strojů stejného modelu.</span><span class="sxs-lookup"><span data-stu-id="94d87-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="94d87-213">Místo přiřazení příslušné příručky s pokyny k obsluze modelu stroje ke každému příslušnému prostředku byste mohli přiřadit příručku ke skupině prostředků, která obsahuje tento model stroje.</span><span class="sxs-lookup"><span data-stu-id="94d87-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="94d87-214">**Příklad 2:** Definovali jste skupinu prostředků pro pracovní buňku, která obsahuje různé stroje, a máte příručku, která poskytuje obecné pokyny pro údržbu této pracovní buňky.</span><span class="sxs-lookup"><span data-stu-id="94d87-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="94d87-215">Tato příručka platí pro jakoukoli výrobní činnost v této pracovní buňce.</span><span class="sxs-lookup"><span data-stu-id="94d87-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="94d87-216">Přidání příručky ke skupině prostředků</span><span class="sxs-lookup"><span data-stu-id="94d87-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="94d87-217">Příručku přidáte ke skupině prostředků takto:</span><span class="sxs-lookup"><span data-stu-id="94d87-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="94d87-218">Přejděte na **Řízení výroby \> Nastavení \> Prostředky \> Skupiny prostředků**.</span><span class="sxs-lookup"><span data-stu-id="94d87-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="94d87-219">V podokně seznamu vyberte skupinu prostředků, ke které chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-220">Rozbalte pevnou záložku **Přidružené příručky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="94d87-221">Na panelu nástrojů **Přidružené příručky** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="94d87-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="94d87-222">Do mřížky je přidán nový řádek.</span><span class="sxs-lookup"><span data-stu-id="94d87-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="94d87-223">Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="94d87-224">Pokud máte velký počet příruček, můžete filtrováním seznamu najít tu, kterou hledáte.</span><span class="sxs-lookup"><span data-stu-id="94d87-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="94d87-225">![Přidání příručky ke skupině prostředků](media/instruction-guides-resourcegroup.png "Přidání příručky ke skupině prostředků")</span><span class="sxs-lookup"><span data-stu-id="94d87-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="94d87-226">Přidružení příručky k uvolněnému produktu</span><span class="sxs-lookup"><span data-stu-id="94d87-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="94d87-227">Příručku můžete přidat k libovolnému [uvolněnému produktu](../pim/tasks/create-released-product-single-company.md).</span><span class="sxs-lookup"><span data-stu-id="94d87-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="94d87-228">Typický scénář využívající uvolněné produkty</span><span class="sxs-lookup"><span data-stu-id="94d87-228">Typical scenario using released products</span></span>

<span data-ttu-id="94d87-229">Příručky na úrovni produktu poskytují pracovníkům v dílně pokyny týkající se obsluhy nebo manipulace s konkrétním uvolněným produktem nebo položkou.</span><span class="sxs-lookup"><span data-stu-id="94d87-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="94d87-230">Přidání příručky k uvolněnému produktu</span><span class="sxs-lookup"><span data-stu-id="94d87-230">Add a Guide to a released product</span></span>

<span data-ttu-id="94d87-231">Příručku přidáte k uvolněnému produktu takto:</span><span class="sxs-lookup"><span data-stu-id="94d87-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="94d87-232">Přejděte na **Řízení informací o výrobě \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="94d87-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="94d87-233">Otevřete produkt, ke kterému chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-234">V podokně akcí otevřete kartu **Inženýr** a ve skupině **Zobrazení** vyberte **Přidružené příručky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="94d87-235">Otevře se stránka **Přidružené příručky** pro vybraný produkt.</span><span class="sxs-lookup"><span data-stu-id="94d87-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="94d87-236">Výběrem možnosti **Přidat** v podokně akcí přidejte nový řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="94d87-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="94d87-237">Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="94d87-238">![Přidání příručky k uvolněnému produktu](media/instruction-guides-ReleasedProduct-AddGuides.png "Přidání příručky k uvolněnému produktu")</span><span class="sxs-lookup"><span data-stu-id="94d87-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="94d87-239">Přidružení příručky k receptuře</span><span class="sxs-lookup"><span data-stu-id="94d87-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="94d87-240">Příručku můžete přidat k libovolné [receptuře](bill-of-material-bom.md#formulas-co-products-and-by-products).</span><span class="sxs-lookup"><span data-stu-id="94d87-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="94d87-241">Typický scénář využívající receptury</span><span class="sxs-lookup"><span data-stu-id="94d87-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="94d87-242">Příručky na úrovni receptury poskytují pracovníkům v dílně pokyny pro manipulaci v kontextu receptury.</span><span class="sxs-lookup"><span data-stu-id="94d87-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="94d87-243">Příručky lze přiřadit rovněž k verzím receptury.</span><span class="sxs-lookup"><span data-stu-id="94d87-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="94d87-244">Pokyny relevantní pro výrobní procesy založené na receptuře můžete přiřadit k postupu, verzi postupu nebo vztahům operací postupu.</span><span class="sxs-lookup"><span data-stu-id="94d87-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="94d87-245">Příručky nelze momentálně připojit k jednotlivým řádkům receptury.</span><span class="sxs-lookup"><span data-stu-id="94d87-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="94d87-246">Přidání příručky k receptuře</span><span class="sxs-lookup"><span data-stu-id="94d87-246">Add a Guide to a formula</span></span>

<span data-ttu-id="94d87-247">Příručku přidáte k receptuře takto:</span><span class="sxs-lookup"><span data-stu-id="94d87-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="94d87-248">Přejděte na **Řízení informací o produktech \> Kusovníky a receptury \> Receptury**.</span><span class="sxs-lookup"><span data-stu-id="94d87-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="94d87-249">Otevřete recepturu, ke které chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-250">Otevřete kartu **Záhlaví** nad horní pevnou záložkou.</span><span class="sxs-lookup"><span data-stu-id="94d87-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="94d87-251">Rozbalte pevnou záložku **Přidružené příručky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="94d87-252">Na panelu nástrojů **Přidružené příručky** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="94d87-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="94d87-253">Do mřížky je přidán nový řádek.</span><span class="sxs-lookup"><span data-stu-id="94d87-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="94d87-254">Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="94d87-255">![Přidání příručky k receptuře](media/instruction-guides-Formula.png "Přidání příručky k receptuře")</span><span class="sxs-lookup"><span data-stu-id="94d87-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="94d87-256">Přidružení příručky k verzi receptury</span><span class="sxs-lookup"><span data-stu-id="94d87-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="94d87-257">Příručku můžete přidat k libovolné [verzi receptury](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="94d87-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="94d87-258">Typický scénář využívající verze receptury</span><span class="sxs-lookup"><span data-stu-id="94d87-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="94d87-259">Příručky připojené k individuální verzi receptury poskytují pracovníkům v dílně pokyny, které vysvětlují výrobu dané verze receptury.</span><span class="sxs-lookup"><span data-stu-id="94d87-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="94d87-260">Pokyny relevantní pro výrobní procesy založené na této verzi receptury můžete přiřadit k postupu, verzi postupu nebo vztahům operací postupu.</span><span class="sxs-lookup"><span data-stu-id="94d87-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="94d87-261">Příručky nelze momentálně připojit k jednotlivým řádkům receptury.</span><span class="sxs-lookup"><span data-stu-id="94d87-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="94d87-262">Přidání příručky k verzi receptury</span><span class="sxs-lookup"><span data-stu-id="94d87-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="94d87-263">Příručku přidáte k verzi receptury takto:</span><span class="sxs-lookup"><span data-stu-id="94d87-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="94d87-264">Přejděte na **Řízení informací o produktech \> Kusovníky a receptury \> Receptury**.</span><span class="sxs-lookup"><span data-stu-id="94d87-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="94d87-265">Otevřete recepturu obsahující verzi, ke které chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-266">Otevřete kartu **Záhlaví** nad horní pevnou záložkou.</span><span class="sxs-lookup"><span data-stu-id="94d87-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="94d87-267">Na pevné záložce **Verze receptury** vyberte verzi, ke které chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-268">Na panelu nástrojů **Verze receptury** vyberte **Přidružené příručky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="94d87-269">![Otevření příruček přidružených k vybrané verzi receptury](media/instruction-guides-FormulaVersion.png "Otevření příruček přidružených k vybrané verzi receptury")</span><span class="sxs-lookup"><span data-stu-id="94d87-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="94d87-270">Otevře se stránka **Přidružené příručky** pro verzi receptury.</span><span class="sxs-lookup"><span data-stu-id="94d87-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="94d87-271">Výběrem možnosti **Přidat** v podokně akcí přidejte nový řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="94d87-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="94d87-272">Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="94d87-273">![Přidání příručky k verzi receptury](media/instruction-guides-FormulaVersionAddGuide.png "Přidání příručky k verzi receptury")</span><span class="sxs-lookup"><span data-stu-id="94d87-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="94d87-274">Přidružení příručky ke kusovníku</span><span class="sxs-lookup"><span data-stu-id="94d87-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="94d87-275">Příručku můžete přidat k libovolnému [kusovníku](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="94d87-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="94d87-276">Typický scénář využívající kusovníky</span><span class="sxs-lookup"><span data-stu-id="94d87-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="94d87-277">Příručky připojené ke kusovníku poskytují pracovníkům v dílně pokyny, které vysvětlují, jak připravit a zacházet s materiálem z kusovníku.</span><span class="sxs-lookup"><span data-stu-id="94d87-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="94d87-278">Příručky lze přiřadit rovněž k verzím kusovníku.</span><span class="sxs-lookup"><span data-stu-id="94d87-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="94d87-279">Příručky nelze momentálně připojit k jednotlivým řádkům kusovníku.</span><span class="sxs-lookup"><span data-stu-id="94d87-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="94d87-280">Přidání příručky ke kusovníku</span><span class="sxs-lookup"><span data-stu-id="94d87-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="94d87-281">Příručku přidáte ke kusovníku takto:</span><span class="sxs-lookup"><span data-stu-id="94d87-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="94d87-282">Přejděte na **Řízení informací o výrobě \> Kusovníky a receptury \> Kusovníky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="94d87-283">Otevřete kusovník, ke kterému chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-284">Otevřete kartu **Záhlaví** nad horní pevnou záložkou.</span><span class="sxs-lookup"><span data-stu-id="94d87-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="94d87-285">Rozbalte pevnou záložku **Přidružené příručky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="94d87-286">Na panelu nástrojů **Přidružené příručky** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="94d87-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="94d87-287">Do mřížky je přidán nový řádek.</span><span class="sxs-lookup"><span data-stu-id="94d87-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="94d87-288">Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="94d87-289">![Přidání příručky ke kusovníku](media/instruction-guides-BOM.png "Přidání příručky ke kusovníku")</span><span class="sxs-lookup"><span data-stu-id="94d87-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="94d87-290">Přidružení příručky k verzi kusovníku</span><span class="sxs-lookup"><span data-stu-id="94d87-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="94d87-291">Příručku můžete přidat k libovolné [verzi kusovníku](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="94d87-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="94d87-292">Typický scénář využívající verze kusovníku</span><span class="sxs-lookup"><span data-stu-id="94d87-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="94d87-293">Příručky připojené k individuální verzi kusovníku poskytují pracovníkům v dílně pokyny, které vysvětlují, jak připravit a zacházet s materiálem pro verzi kusovníku, která se liší od obecného kusovníku nebo jeho jiných verzí.</span><span class="sxs-lookup"><span data-stu-id="94d87-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="94d87-294">Příručky nelze momentálně připojit k jednotlivým řádkům kusovníku.</span><span class="sxs-lookup"><span data-stu-id="94d87-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="94d87-295">Přidání příručky k verzi kusovníku</span><span class="sxs-lookup"><span data-stu-id="94d87-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="94d87-296">Příručku přidáte k verzi kusovníku takto:</span><span class="sxs-lookup"><span data-stu-id="94d87-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="94d87-297">Přejděte na **Řízení informací o výrobě \> Kusovníky a receptury \> Kusovníky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="94d87-298">Otevřete kusovník obsahující verzi, ke které chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-299">Otevřete kartu **Záhlaví** nad horní pevnou záložkou.</span><span class="sxs-lookup"><span data-stu-id="94d87-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="94d87-300">Na pevné záložce **Verze kusovníku** vyberte verzi, ke které chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-301">Na panelu nástrojů **Verze kusovníku** vyberte **Přidružené příručky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="94d87-302">![Otevření příruček přidružených k vybrané verzi kusovníku](media/instruction-guides-BOMVersion.png "Otevření příruček přidružených k vybrané verzi kusovníku")</span><span class="sxs-lookup"><span data-stu-id="94d87-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="94d87-303">Otevře se stránka **Přidružené příručky** pro verzi kusovníku.</span><span class="sxs-lookup"><span data-stu-id="94d87-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="94d87-304">Výběrem možnosti **Přidat** v podokně akcí přidejte nový řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="94d87-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="94d87-305">Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="94d87-306">![Přidání příručky k verzi kusovníku](media/instruction-guides-BOMVersionAddGuide.png "Přidání příručky k verzi kusovníku")</span><span class="sxs-lookup"><span data-stu-id="94d87-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="94d87-307">Přidružení příručky k postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-307">Associate a Guide to a route</span></span>

<span data-ttu-id="94d87-308">Příručku můžete přidat k libovolnému [postupu](routes-operations.md).</span><span class="sxs-lookup"><span data-stu-id="94d87-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="94d87-309">Typický scénář využívající postupy</span><span class="sxs-lookup"><span data-stu-id="94d87-309">Typical scenario using routes</span></span>

<span data-ttu-id="94d87-310">Pomocí postupů se zpravidla určuje, jak se má vyrobit určitý uvolněný produkt na základě kusovníku nebo verze kusovníku a se sadou prostředků nebo skupinami prostředků.</span><span class="sxs-lookup"><span data-stu-id="94d87-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="94d87-311">Přiřazením příručky k postupu poskytnete podrobné pokyny pro příslušný výrobní proces.</span><span class="sxs-lookup"><span data-stu-id="94d87-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="94d87-312">Přidání příručky k postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-312">Add a Guide to a route</span></span>

<span data-ttu-id="94d87-313">Příručku přidáte k postupu takto:</span><span class="sxs-lookup"><span data-stu-id="94d87-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="94d87-314">Přejděte na **Řízení výroby \> Všechny postupy**.</span><span class="sxs-lookup"><span data-stu-id="94d87-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="94d87-315">Otevřete postup, ke kterému chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-316">Rozbalte pevnou záložku **Přidružené příručky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="94d87-317">Na panelu nástrojů **Přidružené příručky** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="94d87-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="94d87-318">Do mřížky je přidán nový řádek.</span><span class="sxs-lookup"><span data-stu-id="94d87-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="94d87-319">Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="94d87-320">![Přidání příručky k postupu](media/instruction-guides-Route.png "Přidání příručky k postupu")</span><span class="sxs-lookup"><span data-stu-id="94d87-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="94d87-321">Přidružení příručky k verzi postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="94d87-322">Příručku můžete přidat k libovolné [verzi postupu](routes-operations.md#route-versions).</span><span class="sxs-lookup"><span data-stu-id="94d87-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="94d87-323">Typický scénář využívající verze postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-323">Typical scenario using route versions</span></span>

<span data-ttu-id="94d87-324">Verze postupů se obvykle používají k určení variant výrobních procesů založených na existujícím postupu.</span><span class="sxs-lookup"><span data-stu-id="94d87-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="94d87-325">Ke každé verzi postupu můžete přiřadit odlišné příručky.</span><span class="sxs-lookup"><span data-stu-id="94d87-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="94d87-326">Přidání příručky k verzi postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-326">Add a Guide to a route version</span></span>

<span data-ttu-id="94d87-327">Příručku přidáte k verzi postupu takto:</span><span class="sxs-lookup"><span data-stu-id="94d87-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="94d87-328">Přejděte na **Řízení výroby \> Všechny postupy**.</span><span class="sxs-lookup"><span data-stu-id="94d87-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="94d87-329">Otevřete postup, ke kterému chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-330">Na pevné záložce **Verze** vyberte verzi, ke které chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-331">Na panelu nástrojů **Verze** vyberte **Přidružené příručky**.</span><span class="sxs-lookup"><span data-stu-id="94d87-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="94d87-332">![Otevření příruček přidružených k vybrané verzi postupu](media/instruction-guides-RouteVersion.png "Otevření příruček přidružených k vybrané verzi postupu")</span><span class="sxs-lookup"><span data-stu-id="94d87-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="94d87-333">Otevře se stránka **Přidružené příručky** pro verzi kusovníku.</span><span class="sxs-lookup"><span data-stu-id="94d87-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="94d87-334">Výběrem možnosti **Přidat** v podokně akcí přidejte nový řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="94d87-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="94d87-335">Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="94d87-336">![Přidání příručky k verzi postupu](media/instruction-guides-RouteVersionAddGuide.png "Přidání příručky k verzi postupu")</span><span class="sxs-lookup"><span data-stu-id="94d87-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="94d87-337">Přidružení příručky ke vztahu operace postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="94d87-338">Příručku můžete přidat k libovolnému [vztahu operace postupu](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="94d87-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="94d87-339">Typický scénář využívající vztahy operací postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="94d87-340">Vztahy operací představují nejkonkrétnější způsob přidání pokynů k procesu produktu a jeho souvisejícím operacím.</span><span class="sxs-lookup"><span data-stu-id="94d87-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="94d87-341">Můžete zadat pokyny pro každou operaci postupu a odlišné pokyny pro jakýkoli typ kontextu vztahu určený pro postup, například pro konkrétní položky, konfigurace a další.</span><span class="sxs-lookup"><span data-stu-id="94d87-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="94d87-342">Můžete rovněž určit, na které fáze operace se tyto pokyny vztahují (například nastavení, řazení do fronty, zpracování nebo dopravu).</span><span class="sxs-lookup"><span data-stu-id="94d87-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="94d87-343">Pokud zadáte příručky pro několik vztahů operací postupu, zobrazí se v dílně pro vygenerovaný úkol jen příručka z nejkonkrétnějšího vztahu.</span><span class="sxs-lookup"><span data-stu-id="94d87-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="94d87-344">Přidání příručky ke vztahu operace postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="94d87-345">Příručku přidáte ke vztahu operace postupu takto:</span><span class="sxs-lookup"><span data-stu-id="94d87-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="94d87-346">Přejděte na **Řízení výroby \> Všechny postupy**.</span><span class="sxs-lookup"><span data-stu-id="94d87-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="94d87-347">Otevřete postup, ke kterému chcete přiřadit příručku.</span><span class="sxs-lookup"><span data-stu-id="94d87-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="94d87-348">V podokně akcí otevřete kartu **Postup** a ve skupině **Údržba** vyberte **Podrobnosti postupu**.</span><span class="sxs-lookup"><span data-stu-id="94d87-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="94d87-349">Otevře se stránka **Podrobnosti postupu** pro vybraný postup.</span><span class="sxs-lookup"><span data-stu-id="94d87-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="94d87-350">V horní mřížce vyberte operaci, ke které chcete poskytnout pokyny.</span><span class="sxs-lookup"><span data-stu-id="94d87-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="94d87-351">V dolní mřížce vyberte konkrétní vztah (nebo obecný vztah **Vše**).</span><span class="sxs-lookup"><span data-stu-id="94d87-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="94d87-352">![Výběr operace a následně vztahu](media/instruction-guides-RouteOperationRelation.png "Výběr operace a následně vztahu")</span><span class="sxs-lookup"><span data-stu-id="94d87-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="94d87-353">Nad dolní mřížkou otevřete kartu **Přidružené příručky**. ![Karta Přidružené příručky](media/instruction-guides-RouteOperationRelation-AddGuide.png "Karta Přidružené příručky")</span><span class="sxs-lookup"><span data-stu-id="94d87-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="94d87-354">Výběrem možnosti **Přidat** na panelu nástrojů v horní části dolní mřížky přidejte do mřížky nový řádek.</span><span class="sxs-lookup"><span data-stu-id="94d87-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="94d87-355">Na novém řádku použijte rozevírací seznam ve sloupci **Název** a zvolte příručku, kterou chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="94d87-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="94d87-356">Ve zbytku řádku zaškrtněte políčko pro každý kontext, ve kterém má být vybraná příručka dostupná.</span><span class="sxs-lookup"><span data-stu-id="94d87-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="94d87-357">Pro každou fázi jednotlivých operací můžete přidat jednu nebo více příruček.</span><span class="sxs-lookup"><span data-stu-id="94d87-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="94d87-358">Výběr příruček z realizačního rozhraní dílny</span><span class="sxs-lookup"><span data-stu-id="94d87-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="94d87-359">Když si pracovník otevře v realizačním rozhraní dílny seznam úkolů, najde Supply Chain Management příslušné příručky pro zobrazené úkoly.</span><span class="sxs-lookup"><span data-stu-id="94d87-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="94d87-360">Tlačítkem **Příručky** si zobrazí relevantní příručky.</span><span class="sxs-lookup"><span data-stu-id="94d87-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="94d87-361">![Tlačítko Příručky v realizačním rozhraní dílny](media/instruction-guides-Shopfloor1.png "Tlačítko Příručky v realizačním rozhraní dílny")</span><span class="sxs-lookup"><span data-stu-id="94d87-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="94d87-362">Pak si nasadí HoloLens a zpřístupní příslušnou příručku pohledem na kód QR a aktivací příslušné příručky.</span><span class="sxs-lookup"><span data-stu-id="94d87-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="94d87-363">![Kód QR pro přístup k příručce pomocí HoloLens](media/instruction-guides-Shopfloor2.png "Kód QR pro přístup k příručce pomocí HoloLens")</span><span class="sxs-lookup"><span data-stu-id="94d87-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="94d87-364">Logika pro výběr příruček</span><span class="sxs-lookup"><span data-stu-id="94d87-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="94d87-365">Příručky můžete přidat k následujícím výrobním datům:</span><span class="sxs-lookup"><span data-stu-id="94d87-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="94d87-366">Prostředky</span><span class="sxs-lookup"><span data-stu-id="94d87-366">Resources</span></span>](#resources)
- [<span data-ttu-id="94d87-367">Skupiny prostředků</span><span class="sxs-lookup"><span data-stu-id="94d87-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="94d87-368">Uvolněné produkty</span><span class="sxs-lookup"><span data-stu-id="94d87-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="94d87-369">Receptury</span><span class="sxs-lookup"><span data-stu-id="94d87-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="94d87-370">Verze receptury</span><span class="sxs-lookup"><span data-stu-id="94d87-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="94d87-371">Kusovníky</span><span class="sxs-lookup"><span data-stu-id="94d87-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="94d87-372">Verze kusovníků</span><span class="sxs-lookup"><span data-stu-id="94d87-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="94d87-373">Postupy</span><span class="sxs-lookup"><span data-stu-id="94d87-373">Routes</span></span>](#routes)
- [<span data-ttu-id="94d87-374">Verze postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="94d87-375">Vztahy operací postupu</span><span class="sxs-lookup"><span data-stu-id="94d87-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="94d87-376">Když Supply Chain Management vygeneruje úkoly pro výrobu, shromáždí z těchto zdrojů příslušné příručky.</span><span class="sxs-lookup"><span data-stu-id="94d87-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="94d87-377">Vezměte na vědomí následující důležitá pravidla.</span><span class="sxs-lookup"><span data-stu-id="94d87-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="94d87-378">Pokud připojíte verzi kusovníku nebo verzi receptury k postupu nebo výrobní zakázce, zobrazí se u úkolu všechny příručky připojené k této verzi a také příručky připojené k nadřazenému kusovníku nebo receptuře této verze.</span><span class="sxs-lookup"><span data-stu-id="94d87-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="94d87-379">Pokud připojíte verzi postupu k výrobní zakázce, zobrazí se u úkolu všechny příručky připojené k této verzi a také příručky připojené k nadřazenému postupu této verze.</span><span class="sxs-lookup"><span data-stu-id="94d87-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="94d87-380">Pokud definujete několik vztahů operací postupu, které obsahují vztah *Vše*, a přiřadíte k nim příručky, zobrazí se u úkolu jen příručky z nejkonkrétnějšího vztahu.</span><span class="sxs-lookup"><span data-stu-id="94d87-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="94d87-381">![Schéma řešení relevantních příruček](media/instruction-guides-Resolve.png "Schéma řešení relevantních příruček")</span><span class="sxs-lookup"><span data-stu-id="94d87-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
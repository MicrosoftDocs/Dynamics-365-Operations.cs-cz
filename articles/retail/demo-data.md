---
title: "Rozložení obrazovky ukázkových dat v MPOS/CPOS"
description: "Toto téma poskytuje informace o rozvrženích obrazovky, která jsou zahrnuta se sadou ukázkových dat v uživatelském prostředí pokladních míst (POS) v aplikaci Microsoft Dynamics 365 for Retail."
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 41bd135c1b891841bd147d8ff9c905d49319b88e
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="demo-data-screen-layouts-in-mposcpos"></a><span data-ttu-id="c1bb8-103">Rozložení obrazovky ukázkových dat v MPOS/CPOS</span><span class="sxs-lookup"><span data-stu-id="c1bb8-103">Demo data screen layouts in MPOS/CPOS</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="c1bb8-104">Toto téma poskytuje informace o rozvrženích obrazovky, která jsou zahrnuta se sadou ukázkových dat v uživatelském prostředí pokladních míst (POS) v aplikaci Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="c1bb8-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="c1bb8-105">Overview</span></span>

<span data-ttu-id="c1bb8-106">Vzorová rozvržení obrazovky zahrnutá v ukázkových datech Retail poskytují obsah, který je optimalizován pro různé maloobchodní segmenty, role pracovníků skladu a zařízení.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-106">The sample screen layouts that are included with Retail demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="c1bb8-107">Jedno rozvržení může obsahovat několik velikostí rozvržení a kombinací mřížek tlačítek, aby se zajistilo pokrytí pro případy, kdy se zaměstnanci obchodu pohybují mezi zařízeními a stanicemi.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="c1bb8-108">Toto téma zdůrazňuje rozdíly mezi těmito rozloženími, operace, které tato rozložení poskytují, a celkovou uživatelskou zkušenost.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![Rozvržení ukázkových dat mezi zařízeními](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="c1bb8-110">Podrobný rozbor ID rozvržení obrazovky</span><span class="sxs-lookup"><span data-stu-id="c1bb8-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="c1bb8-111">Chcete-li nalézt rozvržení obrazovky v aplikaci Retail, přejděte na **Retail** > **Nastavení kanálu** > **Nastavení POS** > **POS** > **Rozvržení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-111">To find screen layouts in Retail, go to **Retail** > **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>

![Stránky rozvržení obrazovky v aplikaci Retail](../retail/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="c1bb8-113">ID rozložení obrazovky může obsahovat maximálně 10 znaků.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="c1bb8-114">ID je řetězec, který se skládá ze tří částí informací, v tomto pořadí:</span><span class="sxs-lookup"><span data-stu-id="c1bb8-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="c1bb8-115">Společnost</span><span class="sxs-lookup"><span data-stu-id="c1bb8-115">Company</span></span>
2. <span data-ttu-id="c1bb8-116">Verze rozvržení</span><span class="sxs-lookup"><span data-stu-id="c1bb8-116">Layout version</span></span>
3. <span data-ttu-id="c1bb8-117">Osoba</span><span class="sxs-lookup"><span data-stu-id="c1bb8-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="c1bb8-118">Společnost</span><span class="sxs-lookup"><span data-stu-id="c1bb8-118">Company</span></span>

| <span data-ttu-id="c1bb8-119">Dopis</span><span class="sxs-lookup"><span data-stu-id="c1bb8-119">Letter</span></span> | <span data-ttu-id="c1bb8-120">Společnost</span><span class="sxs-lookup"><span data-stu-id="c1bb8-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="c1bb8-121">A</span><span class="sxs-lookup"><span data-stu-id="c1bb8-121">A</span></span>      | <span data-ttu-id="c1bb8-122">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c1bb8-122">Adventure Works</span></span> |
| <span data-ttu-id="c1bb8-123">F</span><span class="sxs-lookup"><span data-stu-id="c1bb8-123">F</span></span>      | <span data-ttu-id="c1bb8-124">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c1bb8-124">Fabrikam</span></span>        |
| <span data-ttu-id="c1bb8-125">o</span><span class="sxs-lookup"><span data-stu-id="c1bb8-125">C</span></span>      | <span data-ttu-id="c1bb8-126">Contoso</span><span class="sxs-lookup"><span data-stu-id="c1bb8-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="c1bb8-127">Verze rozvržení</span><span class="sxs-lookup"><span data-stu-id="c1bb8-127">Layout version</span></span>

| <span data-ttu-id="c1bb8-128">Číslo verze</span><span class="sxs-lookup"><span data-stu-id="c1bb8-128">Version number</span></span> | <span data-ttu-id="c1bb8-129">popis</span><span class="sxs-lookup"><span data-stu-id="c1bb8-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1bb8-130">3</span><span class="sxs-lookup"><span data-stu-id="c1bb8-130">3</span></span>              | <span data-ttu-id="c1bb8-131">Základní verze, která podporuje více velikostí obrazovky pro různá zařízení a poměry stran</span><span class="sxs-lookup"><span data-stu-id="c1bb8-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="c1bb8-132">3.1</span><span class="sxs-lookup"><span data-stu-id="c1bb8-132">3.1</span></span>            | <span data-ttu-id="c1bb8-133">Základní verze, která obsahuje další podporu pro panel **Doporučené produkty**</span><span class="sxs-lookup"><span data-stu-id="c1bb8-133">The base version that has additional support for the **Recommended products** panel</span></span>        |

### <a name="persona"></a><span data-ttu-id="c1bb8-134">Osoba</span><span class="sxs-lookup"><span data-stu-id="c1bb8-134">Persona</span></span>

| <span data-ttu-id="c1bb8-135">Zkratka</span><span class="sxs-lookup"><span data-stu-id="c1bb8-135">Abbreviation</span></span> | <span data-ttu-id="c1bb8-136">Osoba</span><span class="sxs-lookup"><span data-stu-id="c1bb8-136">Persona</span></span>       | <span data-ttu-id="c1bb8-137">Obsah</span><span class="sxs-lookup"><span data-stu-id="c1bb8-137">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="c1bb8-138">CSH</span><span class="sxs-lookup"><span data-stu-id="c1bb8-138">CSH</span></span>          | <span data-ttu-id="c1bb8-139">Pokladník</span><span class="sxs-lookup"><span data-stu-id="c1bb8-139">Cashier</span></span>       | <span data-ttu-id="c1bb8-140">Rozvržení pokladníka zahrnuje všechny operace související s transakcí, jako jsou například objednávky odběratele, vrácení, slevy, anulování a dárkové poukazy.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-140">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="c1bb8-141">Tato rozvržení rovněž zahrnují denní úkoly pro řízení zásob, jako jsou kontroly ceny, vyhledávání zásob a počty na skladě.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-141">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="c1bb8-142">Je rovněž poskytnuta základní správa směn pro počáteční částky, pozastavení směn a čas.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-142">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="c1bb8-143">MGR</span><span class="sxs-lookup"><span data-stu-id="c1bb8-143">MGR</span></span>          | <span data-ttu-id="c1bb8-144">Manažer obchodu</span><span class="sxs-lookup"><span data-stu-id="c1bb8-144">Store Manager</span></span> | <span data-ttu-id="c1bb8-145">Rozvržení manažera obchodu zahrnují všechny operace související s transakcí, které se nacházejí v rozvržení pokladního, ale také zahrnují přepsání daně.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-145">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="c1bb8-146">Tato rozvržení rovněž zahrnují denní úkoly pro řízení zásob, jako jsou kontroly ceny, vyhledávání zásob a počty na skladě.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-146">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="c1bb8-147">Správa směn poskytuje spuštění, pozastavení a uzavření směn.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-147">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="c1bb8-148">Dále rozvržení zahrnuje operace zásuvky pro položky, odebrání, návraty, výkazy úhrad a odvody do trezoru a do banky.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-148">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="c1bb8-149">Nakonec tato rozložení zahrnují přístup k sestavám výkonnosti a povolují tisk sestav X a Y.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-149">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="c1bb8-150">STK</span><span class="sxs-lookup"><span data-stu-id="c1bb8-150">STK</span></span>          | <span data-ttu-id="c1bb8-151">Pracovník skladu</span><span class="sxs-lookup"><span data-stu-id="c1bb8-151">Stock Clerk</span></span>   | <span data-ttu-id="c1bb8-152">Rozvržení pracovníka skladu jsou optimalizována pro řízení zásob.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-152">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="c1bb8-153">Mohou zahrnovat přístup ke každodenním úkolům pro kontroly ceny, vyhledávání zásob, výdej a příjem, počty na skladě a demontáž sady.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-153">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="c1bb8-154">Tato rozvržení poskytují také základní operace směny pro čas a pozastavení směny.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-154">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="c1bb8-155">Ačkoliv tato rozvržení slouží zejména pro administrativní úlohy, pracovníci skladu mají k dispozici stejné operace jako pokladníci pro obrazovky transakcí.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-155">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="c1bb8-156">Příklad rozvržení</span><span class="sxs-lookup"><span data-stu-id="c1bb8-156">Example layout</span></span>

<span data-ttu-id="c1bb8-157">Následuje příklad ID rozvržení obrazovky pro společnost Fabrikam, verze rozvržení 3, a osobu manažera obchodu:</span><span class="sxs-lookup"><span data-stu-id="c1bb8-157">Here is an example of a screen layout ID for the Fabrikam company, layout version 3, and the Store Manager persona:</span></span>

<span data-ttu-id="c1bb8-158">F3MGR</span><span class="sxs-lookup"><span data-stu-id="c1bb8-158">F3MGR</span></span>

<span data-ttu-id="c1bb8-159">Následující obrázek znázorňuje příklad uvítací obrazovky manažera obchodu Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-159">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![Uvítací obrazovka pro manažera obchodu Fabrikam](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="c1bb8-161">Velikosti rozvržení</span><span class="sxs-lookup"><span data-stu-id="c1bb8-161">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="c1bb8-162">Úplné a kompaktní rozvržení</span><span class="sxs-lookup"><span data-stu-id="c1bb8-162">Full vs. compact layouts</span></span>

<span data-ttu-id="c1bb8-163">Rozvržení obrazovky může mít konfigurace pro úplné i kompaktní zařízení.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-163">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="c1bb8-164">Uživatel může být přiřazen k jednomu rozvržení obrazovky, které bude fungovat v různých velikostech a formátech v obchodě.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-164">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="c1bb8-165">**Moderní POS - Úplné** - Úplná rozložení jsou obvykle nejvhodnější pro větší displeje, jako mají například PC monitory nebo tablety.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-165">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="c1bb8-166">Uživatelé mohou vybrat prvky uživatelského rozhraní, které rozvržení zahrnuje, určit velikost a umístění těchto prvků a nakonfigurovat jejich podrobné vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-166">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="c1bb8-167">Plná rozložení podporují konfigurace na výšku a na šířku.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-167">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="c1bb8-168">**Modern POS - Kompaktní -** - Kompaktní rozložení jsou obvykle nejvhodnější pro telefony a malé tablety.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-168">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="c1bb8-169">Možnosti návrhu jsou omezeny pro kompaktní zařízení.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-169">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="c1bb8-170">Uživatelé mohou konfigurovat sloupce a pole pro podokna stvrzenek a součtů.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-170">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="c1bb8-171">Rozlišení obrazovky, která jsou k dispozici</span><span class="sxs-lookup"><span data-stu-id="c1bb8-171">Screen resolutions that are provided</span></span>

<span data-ttu-id="c1bb8-172">Následující tabulka zobrazuje velikosti rozvržení, které jsou k dispozici pro typická rozlišení obrazovky.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-172">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="c1bb8-173">Typ rozvržení</span><span class="sxs-lookup"><span data-stu-id="c1bb8-173">Layout type</span></span> | <span data-ttu-id="c1bb8-174">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="c1bb8-174">Resolution</span></span> | <span data-ttu-id="c1bb8-175">Poměr stran</span><span class="sxs-lookup"><span data-stu-id="c1bb8-175">Aspect ratio</span></span> | <span data-ttu-id="c1bb8-176">Cílový displej</span><span class="sxs-lookup"><span data-stu-id="c1bb8-176">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="c1bb8-177">Komprimovat\*</span><span class="sxs-lookup"><span data-stu-id="c1bb8-177">Compact\*</span></span>   | <span data-ttu-id="c1bb8-178">480 × 853</span><span class="sxs-lookup"><span data-stu-id="c1bb8-178">480 × 853</span></span>  | <span data-ttu-id="c1bb8-179">16:9</span><span class="sxs-lookup"><span data-stu-id="c1bb8-179">16:9</span></span>         | <span data-ttu-id="c1bb8-180">Telefony</span><span class="sxs-lookup"><span data-stu-id="c1bb8-180">Phones</span></span>                  |
| <span data-ttu-id="c1bb8-181">Plné</span><span class="sxs-lookup"><span data-stu-id="c1bb8-181">Full</span></span>        | <span data-ttu-id="c1bb8-182">1024 × 768</span><span class="sxs-lookup"><span data-stu-id="c1bb8-182">1024 × 768</span></span> | <span data-ttu-id="c1bb8-183">4:3</span><span class="sxs-lookup"><span data-stu-id="c1bb8-183">4:3</span></span>          | <span data-ttu-id="c1bb8-184">Tablety</span><span class="sxs-lookup"><span data-stu-id="c1bb8-184">Tablets</span></span>                 |
| <span data-ttu-id="c1bb8-185">Plné\*</span><span class="sxs-lookup"><span data-stu-id="c1bb8-185">Full\*</span></span>      | <span data-ttu-id="c1bb8-186">1280 × 720</span><span class="sxs-lookup"><span data-stu-id="c1bb8-186">1280 × 720</span></span> | <span data-ttu-id="c1bb8-187">16:9</span><span class="sxs-lookup"><span data-stu-id="c1bb8-187">16:9</span></span>         | <span data-ttu-id="c1bb8-188">Tablety</span><span class="sxs-lookup"><span data-stu-id="c1bb8-188">Tablets</span></span>                 |
| <span data-ttu-id="c1bb8-189">Plné</span><span class="sxs-lookup"><span data-stu-id="c1bb8-189">Full</span></span>        | <span data-ttu-id="c1bb8-190">1366 × 768</span><span class="sxs-lookup"><span data-stu-id="c1bb8-190">1366 × 768</span></span> | <span data-ttu-id="c1bb8-191">16:9</span><span class="sxs-lookup"><span data-stu-id="c1bb8-191">16:9</span></span>         | <span data-ttu-id="c1bb8-192">Tablety, větší obrazovky</span><span class="sxs-lookup"><span data-stu-id="c1bb8-192">Tablets, larger screens</span></span> |
| <span data-ttu-id="c1bb8-193">Plné</span><span class="sxs-lookup"><span data-stu-id="c1bb8-193">Full</span></span>        | <span data-ttu-id="c1bb8-194">1440 × 960</span><span class="sxs-lookup"><span data-stu-id="c1bb8-194">1440 × 960</span></span> | <span data-ttu-id="c1bb8-195">3:2</span><span class="sxs-lookup"><span data-stu-id="c1bb8-195">3:2</span></span>          | <span data-ttu-id="c1bb8-196">Tablety, větší obrazovky</span><span class="sxs-lookup"><span data-stu-id="c1bb8-196">Tablets, larger screens</span></span> |

<span data-ttu-id="c1bb8-197">\* Tyto dodatečné velikosti rozvržení jsou k dispozici pouze v rozvrženích Fabrikam a Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-197">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>


>[!TIP]
> <span data-ttu-id="c1bb8-198">POS automaticky vybere velikost rozvržení, v závislosti na nejbližší velikosti, která je k dispozici pro rozlišení obrazovky aktuálního okna aplikace.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-198">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="c1bb8-199">Pokud chcete nalézt ID rozvržení obrazovky a rozlišení rozvržení, která jsou aktuálně používána v Retail Modern POS (MPOS) nebo v Retail Cloud POS (CPOS), otevřete stránku **Nastavení** a nahlédněte do části **Informace o relaci**.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-199">To find the screen layout ID and layout resolution that are currently used, in Retail Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="c1bb8-200">Můžete také vidět skutečné rozlišení okna vaší aktuální aplikace nebo rámce prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-200">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="c1bb8-201">Jakmile máte tyto informace, lze vyhledat zdroj obsahu rozvržení v aplikaci Retail přechodem na **Nastavení kanálu** > **Nastavení POS** > **POS** > **Rozvržení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-201">After you have this information, you can find the source of the layout content in Retail by going to **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span>


![Rozvržení obrazovky a rozlišení rozvržení/velikosti v aplikaci Retail a v POS](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="c1bb8-203">Společnosti a značky</span><span class="sxs-lookup"><span data-stu-id="c1bb8-203">Companies and brands</span></span>

<span data-ttu-id="c1bb8-204">Každá fiktivní společnost je zacílena na jiný maloobchodní segment a obsahuje katalogy produktů, které jsou uzpůsobeny trhu společnosti.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-204">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="c1bb8-205">Každá společnost používá jedinečnou vizuální značku, která doprovází její produkty.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-205">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="c1bb8-206">Prvky firemní značky zahrnují barvy zvýraznění, tmavé nebo světlé motivy a průvodní fotografie, poskytující realistický zážitek.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-206">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="c1bb8-207">Segmenty společnosti a vizuální vlastnosti</span><span class="sxs-lookup"><span data-stu-id="c1bb8-207">Company segment and visual characteristics</span></span>

| <span data-ttu-id="c1bb8-208">Společnost</span><span class="sxs-lookup"><span data-stu-id="c1bb8-208">Company</span></span>         | <span data-ttu-id="c1bb8-209">Skl. místo</span><span class="sxs-lookup"><span data-stu-id="c1bb8-209">Location</span></span> | <span data-ttu-id="c1bb8-210">Segment </span><span class="sxs-lookup"><span data-stu-id="c1bb8-210">Segment</span></span>        | <span data-ttu-id="c1bb8-211">Zvýraznění</span><span class="sxs-lookup"><span data-stu-id="c1bb8-211">Accent</span></span> | <span data-ttu-id="c1bb8-212">Motiv</span><span class="sxs-lookup"><span data-stu-id="c1bb8-212">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="c1bb8-213">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c1bb8-213">Adventure Works</span></span> | <span data-ttu-id="c1bb8-214">Seattle</span><span class="sxs-lookup"><span data-stu-id="c1bb8-214">Seattle</span></span>  | <span data-ttu-id="c1bb8-215">Sportovní zboží</span><span class="sxs-lookup"><span data-stu-id="c1bb8-215">Sporting Goods</span></span> | <span data-ttu-id="c1bb8-216">Modrá</span><span class="sxs-lookup"><span data-stu-id="c1bb8-216">Blue</span></span>   | <span data-ttu-id="c1bb8-217">Tmavý</span><span class="sxs-lookup"><span data-stu-id="c1bb8-217">Dark</span></span>  |
| <span data-ttu-id="c1bb8-218">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c1bb8-218">Fabrikam</span></span>        | <span data-ttu-id="c1bb8-219">Houston</span><span class="sxs-lookup"><span data-stu-id="c1bb8-219">Houston</span></span>  | <span data-ttu-id="c1bb8-220">Móda</span><span class="sxs-lookup"><span data-stu-id="c1bb8-220">Fashion</span></span>        | <span data-ttu-id="c1bb8-221">Zelená</span><span class="sxs-lookup"><span data-stu-id="c1bb8-221">Green</span></span>  | <span data-ttu-id="c1bb8-222">Light</span><span class="sxs-lookup"><span data-stu-id="c1bb8-222">Light</span></span> |
| <span data-ttu-id="c1bb8-223">Contoso</span><span class="sxs-lookup"><span data-stu-id="c1bb8-223">Contoso</span></span>         | <span data-ttu-id="c1bb8-224">Boston</span><span class="sxs-lookup"><span data-stu-id="c1bb8-224">Boston</span></span>   | <span data-ttu-id="c1bb8-225">Elektronika</span><span class="sxs-lookup"><span data-stu-id="c1bb8-225">Electronics</span></span>    | <span data-ttu-id="c1bb8-226">Červená</span><span class="sxs-lookup"><span data-stu-id="c1bb8-226">Red</span></span>    | <span data-ttu-id="c1bb8-227">Tmavý</span><span class="sxs-lookup"><span data-stu-id="c1bb8-227">Dark</span></span>  |


>[!NOTE]
> <span data-ttu-id="c1bb8-228">Společnosti Adventure Works a Fabrikam jsou dvě přední značkové společnosti.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-228">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="c1bb8-229">Contoso je k dispozici, ale nebyla poskytnuta všechna rozvržení.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-229">Contoso is available, but not all layouts have been provided.</span></span>


<span data-ttu-id="c1bb8-230">Následující obrázky ukazují příklady uvítací stránky a stránky transakcí pro tři fiktivní společnosti.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-230">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="c1bb8-231">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c1bb8-231">Adventure Works</span></span>

![Uvítací stránka ukázkových dat pro společnost Adventure Works](../retail/media/demo-screen-layouts-fig-4-1a.png)

![Stránka transakcí ukázkových dat pro společnost Adventure Works](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="c1bb8-234">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c1bb8-234">Fabrikam</span></span>

![Uvítací stránka ukázkových dat pro společnost Fabrikam](../retail/media/demo-screen-layouts-fig-4-2a.png)

![Stránka transakcí ukázkových dat pro společnost Fabrikam](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="c1bb8-237">Contoso</span><span class="sxs-lookup"><span data-stu-id="c1bb8-237">Contoso</span></span>

![Rozvržení ukázkových dat pro společnost Contoso](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="c1bb8-239">Matice přihlášení uživatele</span><span class="sxs-lookup"><span data-stu-id="c1bb8-239">User sign in matrix</span></span>

<span data-ttu-id="c1bb8-240">Pro různá rozvržení obrazovky byli zadáni uživatelé.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-240">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="c1bb8-241">Pomocí následující tabulky byste měli být schopni se dostat na jakoukoliv obrazovku.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-241">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="c1bb8-242">Pouze se přihlaste pomocí příslušného ID operátora.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-242">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="c1bb8-243">Společnost</span><span class="sxs-lookup"><span data-stu-id="c1bb8-243">Company</span></span>         | <span data-ttu-id="c1bb8-244">ID rozvržení obrazovky</span><span class="sxs-lookup"><span data-stu-id="c1bb8-244">Screen layout ID</span></span> | <span data-ttu-id="c1bb8-245">Osoba</span><span class="sxs-lookup"><span data-stu-id="c1bb8-245">Persona</span></span>          | <span data-ttu-id="c1bb8-246">ID operátora</span><span class="sxs-lookup"><span data-stu-id="c1bb8-246">Operator IDs</span></span>           |
|-----------------|------------------|---------------   |------------------------|
| <span data-ttu-id="c1bb8-247">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c1bb8-247">Adventure Works</span></span> | <span data-ttu-id="c1bb8-248">A3MGR</span><span class="sxs-lookup"><span data-stu-id="c1bb8-248">A3MGR</span></span>            | <span data-ttu-id="c1bb8-249">Manažer obchodu</span><span class="sxs-lookup"><span data-stu-id="c1bb8-249">Store Manager</span></span>    | <span data-ttu-id="c1bb8-250">000154, 000137, 000073</span><span class="sxs-lookup"><span data-stu-id="c1bb8-250">000154, 000137, 000073</span></span> |
| <span data-ttu-id="c1bb8-251">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c1bb8-251">Adventure Works</span></span> | <span data-ttu-id="c1bb8-252">A3CSH</span><span class="sxs-lookup"><span data-stu-id="c1bb8-252">A3CSH</span></span>            | <span data-ttu-id="c1bb8-253">Pokladník</span><span class="sxs-lookup"><span data-stu-id="c1bb8-253">Cashier</span></span>          | <span data-ttu-id="c1bb8-254">000150, 000175, 000165</span><span class="sxs-lookup"><span data-stu-id="c1bb8-254">000150, 000175, 000165</span></span> |
| <span data-ttu-id="c1bb8-255">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="c1bb8-255">Adventure Works</span></span> | <span data-ttu-id="c1bb8-256">A3STK</span><span class="sxs-lookup"><span data-stu-id="c1bb8-256">A3STK</span></span>            | <span data-ttu-id="c1bb8-257">Pracovník skladu</span><span class="sxs-lookup"><span data-stu-id="c1bb8-257">Stock Clerk</span></span>      | <span data-ttu-id="c1bb8-258">000155, 000181, 000152</span><span class="sxs-lookup"><span data-stu-id="c1bb8-258">000155, 000181, 000152</span></span> |
| <span data-ttu-id="c1bb8-259">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c1bb8-259">Fabrikam</span></span>        | <span data-ttu-id="c1bb8-260">F3MGR</span><span class="sxs-lookup"><span data-stu-id="c1bb8-260">F3MGR</span></span>            | <span data-ttu-id="c1bb8-261">Manažer obchodu</span><span class="sxs-lookup"><span data-stu-id="c1bb8-261">Store Manager</span></span>    | <span data-ttu-id="c1bb8-262">000160, 000168, 000163</span><span class="sxs-lookup"><span data-stu-id="c1bb8-262">000160, 000168, 000163</span></span> |
| <span data-ttu-id="c1bb8-263">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c1bb8-263">Fabrikam</span></span>        | <span data-ttu-id="c1bb8-264">F3CSH</span><span class="sxs-lookup"><span data-stu-id="c1bb8-264">F3CSH</span></span>            | <span data-ttu-id="c1bb8-265">Pokladník</span><span class="sxs-lookup"><span data-stu-id="c1bb8-265">Cashier</span></span>          | <span data-ttu-id="c1bb8-266">000161, 000113, 000114</span><span class="sxs-lookup"><span data-stu-id="c1bb8-266">000161, 000113, 000114</span></span> |
| <span data-ttu-id="c1bb8-267">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="c1bb8-267">Fabrikam</span></span>        | <span data-ttu-id="c1bb8-268">F3STK</span><span class="sxs-lookup"><span data-stu-id="c1bb8-268">F3STK</span></span>            | <span data-ttu-id="c1bb8-269">Pracovník skladu</span><span class="sxs-lookup"><span data-stu-id="c1bb8-269">Stock Clerk</span></span>      | <span data-ttu-id="c1bb8-270">000164, 000112, 000123</span><span class="sxs-lookup"><span data-stu-id="c1bb8-270">000164, 000112, 000123</span></span> |
| <span data-ttu-id="c1bb8-271">Contoso</span><span class="sxs-lookup"><span data-stu-id="c1bb8-271">Contoso</span></span>         | <span data-ttu-id="c1bb8-272">C3MGR</span><span class="sxs-lookup"><span data-stu-id="c1bb8-272">C3MGR</span></span>            | <span data-ttu-id="c1bb8-273">Manažer obchodu</span><span class="sxs-lookup"><span data-stu-id="c1bb8-273">Store Manager</span></span>    | <span data-ttu-id="c1bb8-274">000100, 000111</span><span class="sxs-lookup"><span data-stu-id="c1bb8-274">000100, 000111</span></span>         |
| <span data-ttu-id="c1bb8-275">Contoso</span><span class="sxs-lookup"><span data-stu-id="c1bb8-275">Contoso</span></span>         | <span data-ttu-id="c1bb8-276">C3CSH</span><span class="sxs-lookup"><span data-stu-id="c1bb8-276">C3CSH</span></span>            | <span data-ttu-id="c1bb8-277">Pokladník</span><span class="sxs-lookup"><span data-stu-id="c1bb8-277">Cashier</span></span>          | <span data-ttu-id="c1bb8-278">000110, 000120</span><span class="sxs-lookup"><span data-stu-id="c1bb8-278">000110, 000120</span></span>         |
| <span data-ttu-id="c1bb8-279">Contoso</span><span class="sxs-lookup"><span data-stu-id="c1bb8-279">Contoso</span></span>         | <span data-ttu-id="c1bb8-280">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c1bb8-280">Not applicable</span></span>   | <span data-ttu-id="c1bb8-281">Pracovník skladu</span><span class="sxs-lookup"><span data-stu-id="c1bb8-281">Stock Clerk</span></span>      | <span data-ttu-id="c1bb8-282">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="c1bb8-282">Not applicable</span></span>         |


>[!TIP]
> <span data-ttu-id="c1bb8-283">Abyste dosáhli nejlepších výsledků, aktivujte pokladnu v odpovídajícím umístění obchodu a nastavte společnosti na společnost osoby, kterou chcete použít při přihlášení.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-283">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="c1bb8-284">Tímto způsobem zajistíte, že vizuální profil a obrázky týkajíc se značky budou sjednoceny napříč uživatelskými možnostmi.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-284">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="c1bb8-285">Například pokud chcete zobrazit Fabrikam rozvržení pro pokladníka, musíte aktivovat pokladnu obchodu v Houstonu.</span><span class="sxs-lookup"><span data-stu-id="c1bb8-285">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->


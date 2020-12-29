---
title: Návrh rozhraní pro provádění výrobního provozu
description: Toto téma popisuje, jak navrhnout obsah uživatelského rozhraní pro každou konfiguraci.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664265"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="23036-103">Návrh rozhraní pro provádění výrobního provozu</span><span class="sxs-lookup"><span data-stu-id="23036-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="23036-104">Můžete navrhnout obsah uživatelského rozhraní pro každou konfiguraci používanou rozhraním pro provádění výrobního provozu.</span><span class="sxs-lookup"><span data-stu-id="23036-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="23036-105">Například pracovníci v jedné pracovní buňce možná budou muset být schopni otevřít pracovní pokyny ve výrobním provozu, zatímco v jiné pracovní buňce nejsou pokyny potřeba.</span><span class="sxs-lookup"><span data-stu-id="23036-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="23036-106">V takovém případě by měly být vytvořeny dvě konfigurace, jedna s tlačítkem pro otevírání příloh dokumentů a druhá bez tohoto tlačítka.</span><span class="sxs-lookup"><span data-stu-id="23036-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="23036-107">Návrh karty</span><span class="sxs-lookup"><span data-stu-id="23036-107">Design a tab</span></span>

<span data-ttu-id="23036-108">Na stránce **Konfigurace provádění výrobního provozu** můžete vytvářet a konfigurovat karty výběrem **Návrh karet** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="23036-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="23036-109">Každá karta je rozdělena do čtyř částí, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="23036-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="23036-110">![Rozložení karty](media/pfe-tab-layout.png "Rozložení karty")</span><span class="sxs-lookup"><span data-stu-id="23036-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="23036-111">Na obrázku jsou zobrazeny následující prvky:</span><span class="sxs-lookup"><span data-stu-id="23036-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="23036-112">Primární panel nástrojů</span><span class="sxs-lookup"><span data-stu-id="23036-112">Primary toolbar</span></span>
1. <span data-ttu-id="23036-113">Sekundární panel nástrojů</span><span class="sxs-lookup"><span data-stu-id="23036-113">Secondary toolbar</span></span>
1. <span data-ttu-id="23036-114">Hlavní zobrazení</span><span class="sxs-lookup"><span data-stu-id="23036-114">Main view</span></span>
1. <span data-ttu-id="23036-115">Podrobné zobrazení</span><span class="sxs-lookup"><span data-stu-id="23036-115">Detailed view</span></span>

<span data-ttu-id="23036-116">Chcete-li vytvořit a konfigurovat novou kartu, postupujte dle těchto kroků:</span><span class="sxs-lookup"><span data-stu-id="23036-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="23036-117">Přejděte na **Řízení výroby &gt; Nastavení &gt; Provádění výroby**.</span><span class="sxs-lookup"><span data-stu-id="23036-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="23036-118">Vyberte **Návrh karet** na panelu akcí a otevřete stránku **Návrh karet**.</span><span class="sxs-lookup"><span data-stu-id="23036-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="23036-119">![Stránka Návrh karet](media/pfe-design-tabs.png "Stránka Návrh karet")</span><span class="sxs-lookup"><span data-stu-id="23036-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="23036-120">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="23036-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="23036-121">V záhlaví stránky proveďte následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="23036-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="23036-122">**Název karty** - Zadejte název karty.</span><span class="sxs-lookup"><span data-stu-id="23036-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="23036-123">**Hlavní zobrazení** - Vyberte mezi dvěma předdefinovanými seznamy úloh (*Aktivní úlohy* nebo *Všechny úlohy*).</span><span class="sxs-lookup"><span data-stu-id="23036-123">**Main view** - Select between the two pre-defined job lists (*Active jobs* or *All jobs*).</span></span>
    - <span data-ttu-id="23036-124">**Zobrazení podrobností** - Vyberte mezi prázdnou hodnotou nebo **Podrobnosti o úloze**.</span><span class="sxs-lookup"><span data-stu-id="23036-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="23036-125">Pokud vyberete prázdnou hodnotu, na kartě nebude žádné podrobné zobrazení. Pokud vyberete **Podrobnosti o úloze**, podrobné zobrazení bude obsahovat podrobný popis úlohy vybrané v seznamu úloh v hlavním zobrazení.</span><span class="sxs-lookup"><span data-stu-id="23036-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="23036-126">V části **Primární panel nástrojů** vyberte, která tlačítka by měla být k dispozici na primárním panelu nástrojů.</span><span class="sxs-lookup"><span data-stu-id="23036-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="23036-127">Sloupec **Dostupné akce** zobrazuje seznam všech tlačítek, která lze přidat.</span><span class="sxs-lookup"><span data-stu-id="23036-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="23036-128">Sloupec **Vybrané akce** zobrazuje seznam všech tlačítek, která jsou součástí aktuální konfigurace.</span><span class="sxs-lookup"><span data-stu-id="23036-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="23036-129">Pomocí tlačítek mezi sloupci můžete podle potřeby přesouvat vybrané položky mezi sloupci.</span><span class="sxs-lookup"><span data-stu-id="23036-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="23036-130">Použijte tlačítka nahoru a dolů vedle sloupce **Vybrané akce** pro ovládání pořadí, v jakém jsou tlačítka zobrazena v uživatelském rozhraní.</span><span class="sxs-lookup"><span data-stu-id="23036-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="23036-131">V části **Sekundární** **panel nástrojů** vyberte, která tlačítka by měla být k dispozici na sekundárním panelu nástrojů.</span><span class="sxs-lookup"><span data-stu-id="23036-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="23036-132">Sloupec **Dostupné akce** zobrazuje seznam všech tlačítek, která lze přidat.</span><span class="sxs-lookup"><span data-stu-id="23036-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="23036-133">Sloupec **Vybrané akce** zobrazuje seznam všech tlačítek, která jsou součástí aktuální konfigurace.</span><span class="sxs-lookup"><span data-stu-id="23036-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="23036-134">Pomocí tlačítek mezi sloupci můžete podle potřeby přesouvat vybrané položky mezi sloupci.</span><span class="sxs-lookup"><span data-stu-id="23036-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="23036-135">Použijte tlačítka nahoru a dolů vedle sloupce **Vybrané akce** pro ovládání pořadí, v jakém jsou tlačítka zobrazena v uživatelském rozhraní.</span><span class="sxs-lookup"><span data-stu-id="23036-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="23036-136">Přiřazení karty ke konfiguraci</span><span class="sxs-lookup"><span data-stu-id="23036-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="23036-137">Poté, co jste navrhli všechny karty, které potřebujete, můžete je přidružit ke konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="23036-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="23036-138">Přejděte do nabídky **Řízení výroby &gt; Nastavení &gt; Konfigurace provádění výrobního provozu**.</span><span class="sxs-lookup"><span data-stu-id="23036-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="23036-139">![Konfigurovat provedení výrobního provozu](media/pfe-config-prod-floor-execution.png "Konfigurovat provedení výrobního provozu")</span><span class="sxs-lookup"><span data-stu-id="23036-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="23036-140">Na záložce s náhledem **Volba karty** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="23036-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="23036-141">Do mřížky je přidán nový řádek.</span><span class="sxs-lookup"><span data-stu-id="23036-141">A new row is added to the grid.</span></span> <span data-ttu-id="23036-142">U tohoto nového řádku vyberte název karty, kterou chcete přidat do konfigurace.</span><span class="sxs-lookup"><span data-stu-id="23036-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="23036-143">Podle potřeby pokračujte v přidávání dalších karet.</span><span class="sxs-lookup"><span data-stu-id="23036-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="23036-144">Použijte tlačítka **Nahoru** a **Dolů** na panelu nástrojů a uspořádejte karty podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="23036-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="23036-145">Karty se budou zobrazovat zleva doprava v pořadí uvedeném na výše uvedeném snímku obrazovky (karta nahoře je zobrazena vlevo).</span><span class="sxs-lookup"><span data-stu-id="23036-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>

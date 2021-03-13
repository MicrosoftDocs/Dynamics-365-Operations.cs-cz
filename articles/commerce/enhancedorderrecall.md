---
title: Operace odvolání objednávky v POS
description: Toto téma vysvětluje funkce, které jsou dostupné u vylepšených stránek pro odvolání objednávek v POS.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010067"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="de5d8-103">Operace odvolání objednávky v POS</span><span class="sxs-lookup"><span data-stu-id="de5d8-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de5d8-104">Operace **Odvolat objednávku** v pokladním místě (POS) Commerce nabízí aktualizované funkce hledání a filtrování objednávek a specifické informace o objednávce.</span><span class="sxs-lookup"><span data-stu-id="de5d8-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="de5d8-105">Tato funkce je k dispozici ve verzích Commerce 10.0.15 a novějších.</span><span class="sxs-lookup"><span data-stu-id="de5d8-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="de5d8-106">Tuto funkčnost povolíte tak, že zapnete funkci **Vylepšená operace odvolání objednávky v POS** v pracovním prostoru **Správa funkcí** v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="de5d8-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="de5d8-107">Po povolení této funkce zvažte aktualizaci [rozložení obrazovek](pos-screen-layouts.md) v POS, abyste využili některé ze změněných funkcí.</span><span class="sxs-lookup"><span data-stu-id="de5d8-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="de5d8-108">Konfigurace tlačítka operace **Odvolání objednávky** umožňuje organizacím nasadit tuto operaci s předdefinovaným zobrazením.</span><span class="sxs-lookup"><span data-stu-id="de5d8-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Konfigurace mřížky tlačítek](media/recallorderbuttongrid.png)

<span data-ttu-id="de5d8-110">K dispozici jsou následující možnosti zobrazení.</span><span class="sxs-lookup"><span data-stu-id="de5d8-110">The display options are as follows.</span></span>
- <span data-ttu-id="de5d8-111">**Žádné** – tato možnost nasadí tuto operaci bez konkrétního zobrazení.</span><span class="sxs-lookup"><span data-stu-id="de5d8-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="de5d8-112">Když uživatel otevře operaci s touto konfigurací, bude vyzván k vyhledání objednávek nebo k výběru z předdefinovaného filtru objednávek.</span><span class="sxs-lookup"><span data-stu-id="de5d8-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="de5d8-113">**Objednávky k plnění** – když uživatel zahájí tuto operaci, automaticky se spustí dotaz, který vyhledá a zobrazí seznam objednávek, které má obchod splnit.</span><span class="sxs-lookup"><span data-stu-id="de5d8-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="de5d8-114">Tyto objednávky jsou nakonfigurovány pro výdej v obchodě nebo dodávku z obchodu, přičemž řádky těchto objednávek ještě nebyly vydány nebo zabaleny.</span><span class="sxs-lookup"><span data-stu-id="de5d8-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="de5d8-115">**Objednávky k vydání** – když uživatel zahájí tuto operaci, automaticky se spustí dotaz, který vyhledá a zobrazí seznam objednávek, které jsou nakonfigurovány pro výdej v aktuálním obchodě uživatele.</span><span class="sxs-lookup"><span data-stu-id="de5d8-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="de5d8-116">**Objednávky k dodávce** – když uživatel zahájí tuto operaci, automaticky se spustí dotaz, který vyhledá a zobrazí seznam objednávek, které jsou nakonfigurovány pro dodávku z aktuálního obchodu uživatele.</span><span class="sxs-lookup"><span data-stu-id="de5d8-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="de5d8-117">Pokud uživatel zahájí operaci **Odvolat objednávku** z POS, když je zobrazení je nakonfigurováno na **Žádné**, bude moci objednávky vyhledat a načíst jedním z následujících způsobů.</span><span class="sxs-lookup"><span data-stu-id="de5d8-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="de5d8-118">Naskenuje čárové kódy objednávek.</span><span class="sxs-lookup"><span data-stu-id="de5d8-118">Scan order barcodes.</span></span> <span data-ttu-id="de5d8-119">Tím se vyhledají shody s poli pro číslo objednávky, odkaz na kanál a ID účtenky.</span><span class="sxs-lookup"><span data-stu-id="de5d8-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="de5d8-120">Vybere ikonu **Hledat objednávky** nebo **Hledat a filtrovat** na panelu aplikace a pomocí filtračního mechanizmu vyhledá objednávky, které splňují kritéria filtru.</span><span class="sxs-lookup"><span data-stu-id="de5d8-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="de5d8-121">Zvolí z předdefinovaného filtru v rozevírací nabídce **Zobrazit objednávky** (objednávky k plnění, objednávky k vydání nebo objednávky k dodávce).</span><span class="sxs-lookup"><span data-stu-id="de5d8-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![Hlavní nabídka odvolání objednávky](media/recallordermain.png)

<span data-ttu-id="de5d8-123">Po uplatnění kritérií hledání zobrazí aplikace seznam odpovídajících prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="de5d8-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![Podrobnosti odvolání objednávky](media/orderrecalldetail.png)

<span data-ttu-id="de5d8-125">Výběrem objednávky v seznamu může uživatel zobrazit další podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="de5d8-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="de5d8-126">Informační panel na pravé straně obrazovky zobrazuje specifika vybrané objednávky, včetně podrobností o řádku objednávky, doručení a plnění.</span><span class="sxs-lookup"><span data-stu-id="de5d8-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="de5d8-127">Na panelu aplikace může uživatel vybrat některou operaci.</span><span class="sxs-lookup"><span data-stu-id="de5d8-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="de5d8-128">V závislosti na stavu objednávky nemusí být některé operace povoleny.</span><span class="sxs-lookup"><span data-stu-id="de5d8-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="de5d8-129">**Vrátit** – provede vrácení jedné nebo více faktur souvisejících s vybranou objednávkou odběratele.</span><span class="sxs-lookup"><span data-stu-id="de5d8-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="de5d8-130">**Storno** – vystaví úplné zrušení vybrané prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="de5d8-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="de5d8-131">**Splnit** – přenese uživatele na stránku pro splnění objednávky, která bude předfiltrována na vybranou objednávku.</span><span class="sxs-lookup"><span data-stu-id="de5d8-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="de5d8-132">Zobrazí se pouze řádky vybrané objednávky, které jsou otevřené pro splnění obchodem uživatele.</span><span class="sxs-lookup"><span data-stu-id="de5d8-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="de5d8-133">**Upravit** – umožňuje uživatelům provádět změny ve vybrané objednávce odběratele.</span><span class="sxs-lookup"><span data-stu-id="de5d8-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="de5d8-134">**Vydat** – spustí tok vydání, který uživateli umožňuje vybrat produkty, které mají být vydány, a vytvoří prodejní transakci výdeje.</span><span class="sxs-lookup"><span data-stu-id="de5d8-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>

---
title: Operace odvolání objednávky v POS
description: Toto téma vysvětluje funkce, které jsou dostupné u vylepšených stránek pro odvolání objednávek v POS.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f7ad4f53917bb607afe84a2c457518c3f8f7a08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799098"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="0d26f-103">Operace odvolání objednávky v POS</span><span class="sxs-lookup"><span data-stu-id="0d26f-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d26f-104">Operace **Odvolat objednávku** v pokladním místě (POS) Commerce nabízí aktualizované funkce hledání a filtrování objednávek a specifické informace o objednávce.</span><span class="sxs-lookup"><span data-stu-id="0d26f-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="0d26f-105">Tato funkce je k dispozici ve verzích Commerce 10.0.15 a novějších.</span><span class="sxs-lookup"><span data-stu-id="0d26f-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="0d26f-106">Tuto funkčnost povolíte tak, že zapnete funkci **Vylepšená operace odvolání objednávky v POS** v pracovním prostoru **Správa funkcí** v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="0d26f-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="0d26f-107">Po povolení této funkce zvažte aktualizaci [rozložení obrazovek](pos-screen-layouts.md) v POS, abyste využili některé ze změněných funkcí.</span><span class="sxs-lookup"><span data-stu-id="0d26f-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="0d26f-108">Konfigurace tlačítka operace **Odvolání objednávky** umožňuje organizacím nasadit tuto operaci s předdefinovaným zobrazením.</span><span class="sxs-lookup"><span data-stu-id="0d26f-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Konfigurace mřížky tlačítek](media/recallorderbuttongrid.png)

<span data-ttu-id="0d26f-110">K dispozici jsou následující možnosti zobrazení.</span><span class="sxs-lookup"><span data-stu-id="0d26f-110">The display options are as follows.</span></span>
- <span data-ttu-id="0d26f-111">**Žádné** – tato možnost nasadí tuto operaci bez konkrétního zobrazení.</span><span class="sxs-lookup"><span data-stu-id="0d26f-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="0d26f-112">Když uživatel otevře operaci s touto konfigurací, bude vyzván k vyhledání objednávek nebo k výběru z předdefinovaného filtru objednávek.</span><span class="sxs-lookup"><span data-stu-id="0d26f-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="0d26f-113">**Objednávky k plnění** – když uživatel zahájí tuto operaci, automaticky se spustí dotaz, který vyhledá a zobrazí seznam objednávek, které má aktuální obchod uživatele splnit.</span><span class="sxs-lookup"><span data-stu-id="0d26f-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the user's current store.</span></span> <span data-ttu-id="0d26f-114">Tyto objednávky jsou nakonfigurovány pro výdej v obchodě nebo dodávku z obchodu, přičemž řádky těchto objednávek ještě nebyly vydány nebo zabaleny.</span><span class="sxs-lookup"><span data-stu-id="0d26f-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="0d26f-115">**Objednávky k vydání** – když uživatel zahájí tuto operaci, automaticky se spustí dotaz, který vyhledá a zobrazí seznam objednávek, které jsou nakonfigurovány pro výdej v aktuálním obchodě uživatele.</span><span class="sxs-lookup"><span data-stu-id="0d26f-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="0d26f-116">**Objednávky k dodávce** – když uživatel zahájí tuto operaci, automaticky se spustí dotaz, který vyhledá a zobrazí seznam objednávek, které jsou nakonfigurovány pro dodávku z aktuálního obchodu uživatele.</span><span class="sxs-lookup"><span data-stu-id="0d26f-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="0d26f-117">Pokud uživatel zahájí operaci **Odvolat objednávku** z POS, když je zobrazení je nakonfigurováno na **Žádné**, bude moci objednávky vyhledat a načíst jedním z následujících způsobů.</span><span class="sxs-lookup"><span data-stu-id="0d26f-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="0d26f-118">Naskenuje čárové kódy objednávek.</span><span class="sxs-lookup"><span data-stu-id="0d26f-118">Scan order barcodes.</span></span> <span data-ttu-id="0d26f-119">Tím se vyhledají shody s poli pro číslo objednávky, odkaz na kanál a ID účtenky.</span><span class="sxs-lookup"><span data-stu-id="0d26f-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="0d26f-120">Vybere ikonu **Hledat objednávky** nebo **Hledat a filtrovat** na panelu aplikace a pomocí filtračního mechanizmu vyhledá objednávky, které splňují kritéria filtru.</span><span class="sxs-lookup"><span data-stu-id="0d26f-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="0d26f-121">Zvolí z předdefinovaného filtru v rozevírací nabídce **Zobrazit objednávky** (objednávky k plnění, objednávky k vydání nebo objednávky k dodávce).</span><span class="sxs-lookup"><span data-stu-id="0d26f-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![Hlavní nabídka odvolání objednávky](media/recallordermain.png)

<span data-ttu-id="0d26f-123">Po uplatnění kritérií hledání zobrazí aplikace seznam odpovídajících prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="0d26f-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span> <span data-ttu-id="0d26f-124">Je důležité si uvědomit, že při použití možností vyhledávání/filtrování nemusí být načtené objednávky objednávkami propojenými s aktuálním obchodem uživatele.</span><span class="sxs-lookup"><span data-stu-id="0d26f-124">It's important to note that when using the search/filter options, the orders retrieved do not have to be orders linked to the user's current store.</span></span> <span data-ttu-id="0d26f-125">Tento vyhledávací proces načte a zobrazí jakoukoli objednávku zákazníka, která odpovídá kritériím vyhledávání, i když byla objednávka vytvořena nebo nastavena tak, aby byla splněna v jiném obchodě/kanálu nebo skladem.</span><span class="sxs-lookup"><span data-stu-id="0d26f-125">This search process will retrieve and display any customer order that matches the search criteria, even if the order was created or set to be fulfilled by another store/channel or warehouse location.</span></span>

![Podrobnosti odvolání objednávky](media/orderrecalldetail.png)

<span data-ttu-id="0d26f-127">Výběrem objednávky v seznamu může uživatel zobrazit další podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="0d26f-127">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="0d26f-128">Informační panel na pravé straně obrazovky zobrazuje specifika vybrané objednávky, včetně podrobností o řádku objednávky, doručení a plnění.</span><span class="sxs-lookup"><span data-stu-id="0d26f-128">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="0d26f-129">Na panelu aplikace může uživatel vybrat některou operaci.</span><span class="sxs-lookup"><span data-stu-id="0d26f-129">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="0d26f-130">V závislosti na stavu objednávky nemusí být některé operace povoleny.</span><span class="sxs-lookup"><span data-stu-id="0d26f-130">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="0d26f-131">**Vrácení** – Zahájí proces vytváření vrácení u některého z fakturovaných produktů u vybrané objednávky zákazníka.</span><span class="sxs-lookup"><span data-stu-id="0d26f-131">**Return** – Initiates the process of creating a return for any of the invoiced products on the selected customer order.</span></span>

- <span data-ttu-id="0d26f-132">**Storno** – vystaví úplné zrušení vybrané prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0d26f-132">**Cancel** – Issue a full cancellation of the selected sales order.</span></span> <span data-ttu-id="0d26f-133">Tato možnost nebude k dispozici u objednávek iniciovaných prostřednictvím kanálu call centra a nelze ji použít k částečnému zrušení objednávky.</span><span class="sxs-lookup"><span data-stu-id="0d26f-133">This option will not be available for orders initiated through a call center channel and cannot be used to partially cancel an order.</span></span>

- <span data-ttu-id="0d26f-134">**Splnit** – přenese uživatele na stránku pro splnění objednávky, která bude předfiltrována na vybranou objednávku.</span><span class="sxs-lookup"><span data-stu-id="0d26f-134">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="0d26f-135">Zobrazí se pouze řádky vybrané objednávky, které jsou otevřené pro splnění obchodem uživatele.</span><span class="sxs-lookup"><span data-stu-id="0d26f-135">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="0d26f-136">**Upravit** – umožňuje uživatelům provádět změny ve vybrané objednávce odběratele.</span><span class="sxs-lookup"><span data-stu-id="0d26f-136">**Edit** – Allows users to make changes to the selected customer order.</span></span> <span data-ttu-id="0d26f-137">Objednávky lze upravovat pouze v [určitých scénářích](customer-orders-overview.md#edit-an-existing-customer-order).</span><span class="sxs-lookup"><span data-stu-id="0d26f-137">Orders are only editable in [certain scenarios](customer-orders-overview.md#edit-an-existing-customer-order).</span></span>

- <span data-ttu-id="0d26f-138">**Vyzvednutí** – Tato možnost bude k dispozici, pokud má objednávka jeden nebo více řádků určených k vyzvednutí v aktuálním obchodě uživatele.</span><span class="sxs-lookup"><span data-stu-id="0d26f-138">**Pick up** – This option will be available if the order has one or more lines designated for pickup at the user's current store.</span></span> <span data-ttu-id="0d26f-139">Tato operace spustí tok vydání, který uživateli umožňuje vybrat produkty, které mají být vydány, a vytvoří prodejní transakci výdeje.</span><span class="sxs-lookup"><span data-stu-id="0d26f-139">This operation launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>

## <a name="add-notifications-to-the-recall-order-operation"></a><span data-ttu-id="0d26f-140">Přidání oznámení k operaci zrušení objednávky</span><span class="sxs-lookup"><span data-stu-id="0d26f-140">Add notifications to the recall order operation</span></span>

<span data-ttu-id="0d26f-141">Ve verzi 10.0.18 a novější můžete nakonfigurovat oznámení POS a živá upozornění na dlaždice pro operaci **Zrušení objednávky**, pokud je to požadováno.</span><span class="sxs-lookup"><span data-stu-id="0d26f-141">In version 10.0.18 and later, you can configure POS notifications and live tile alerts for the **Order Recall** operation if desired.</span></span> <span data-ttu-id="0d26f-142">Další informace viz [Zobrazit oznámení o objednávce v prodejním místě (POS)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="0d26f-142">For more information, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>  

[!INCLUDE[footer-include](../includes/footer-banner.md)]

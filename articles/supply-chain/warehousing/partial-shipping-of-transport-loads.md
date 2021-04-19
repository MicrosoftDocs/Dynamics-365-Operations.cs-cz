---
title: Částečná dodávka nákladu přepravy
description: Toto téma vysvětluje, jak můžete částečně expedovat vytížení a odložení plánování vytížení kapacity.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 179a784f1f02ed0840ba5219c350e274272b59eb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818937"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="ed66f-103">Částečná dodávka nákladu přepravy</span><span class="sxs-lookup"><span data-stu-id="ed66f-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ed66f-104">Nastavením částečné dodávky náklady lze zpracovat náklady, kde kapacitu nelze určit, dokud nebudou všechny řádky prodeje přidány k nákladu.</span><span class="sxs-lookup"><span data-stu-id="ed66f-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="ed66f-105">Proces pak může být dokončen, když je známý přesný počet palet.</span><span class="sxs-lookup"><span data-stu-id="ed66f-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="ed66f-106">Z tohoto důvodu není nutné rozhodnout, které palety budou přiřazeny ke kterému přenosu až do okamžiku, kdy je přeprava fyzicky nakládána mimo fázované zásoby.</span><span class="sxs-lookup"><span data-stu-id="ed66f-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="ed66f-107">Tato funkce je alternativou dodržování pevnější struktury, kde je třeba určit, které palety budou přiřazeny které přepravě před vyskladněním nebo nakládkou.</span><span class="sxs-lookup"><span data-stu-id="ed66f-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="ed66f-108">Uživatelé mohou místo toho nakonfigurovat jednotlivé náklady pro potvrzení částečné dodávky.</span><span class="sxs-lookup"><span data-stu-id="ed66f-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="ed66f-109">Poté mohou být provedeny přepravy pro tyto náklady.</span><span class="sxs-lookup"><span data-stu-id="ed66f-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="ed66f-110">Proto může oddělení plánování přepravy plánovat náklady, aniž by musely zohlednit kapacitu jednotlivých přeprav.</span><span class="sxs-lookup"><span data-stu-id="ed66f-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="ed66f-111">V době nakládky mohou pracovníci definovat novou zátěž přepravy, na kterou lze paletu naložit.</span><span class="sxs-lookup"><span data-stu-id="ed66f-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="ed66f-112">Případně mohou identifikovat stávající náklad přepravy.</span><span class="sxs-lookup"><span data-stu-id="ed66f-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="ed66f-113">Tato data lze zaznamenat pomocí mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="ed66f-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="ed66f-114">Několik pracovníků skladu proto může naložit zásob ze stejných nebo různých nákladů na stejnou dodávku.</span><span class="sxs-lookup"><span data-stu-id="ed66f-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="ed66f-115">Náklady lze poté úplně nebo částečně expedovat.</span><span class="sxs-lookup"><span data-stu-id="ed66f-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="ed66f-116">Aby bylo možné naložit zásoby z nakládky do konkrétní přepravní nakládky a nakládku částečně expedovat, je nutné vygenerovat práci pomocí třídy nakládky v pracovní šabloně.</span><span class="sxs-lookup"><span data-stu-id="ed66f-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="ed66f-117">Běžná práce výdeje typu **výdej** nelze naložit pro přepravu, například na dodávku.</span><span class="sxs-lookup"><span data-stu-id="ed66f-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="ed66f-118">Nastavení nakládek pro přepravu částečných dodávek</span><span class="sxs-lookup"><span data-stu-id="ed66f-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="ed66f-119">Nastavení nakládek pro přepravu částečných dodávek se skládá z následujících postupů.</span><span class="sxs-lookup"><span data-stu-id="ed66f-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="ed66f-120">Nastavení strategie vytížení</span><span class="sxs-lookup"><span data-stu-id="ed66f-120">Set the loading strategy</span></span>

<span data-ttu-id="ed66f-121">Je nutné povolit částečnou nakládku nastavením strategie nakládky.</span><span class="sxs-lookup"><span data-stu-id="ed66f-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="ed66f-122">Po vytvoření nakládky můžete nastavit strategii nakládání.</span><span class="sxs-lookup"><span data-stu-id="ed66f-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="ed66f-123">Vyberte **řízení skladu** \> **Nakládky** \> **Všechny nakládky**.</span><span class="sxs-lookup"><span data-stu-id="ed66f-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="ed66f-124">Vyberte nakládku a klikněte na **záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="ed66f-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="ed66f-125">V poli **Strategie nakládky** vyberte **Povolena částečná nakládka**.</span><span class="sxs-lookup"><span data-stu-id="ed66f-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="ed66f-126">Vytvoření položky nabídky pro nakládku pro přepravu</span><span class="sxs-lookup"><span data-stu-id="ed66f-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="ed66f-127">Je nutné vytvořit novou položku nabídky, která umožňuje dopravovat náklady, které mají být naloženy.</span><span class="sxs-lookup"><span data-stu-id="ed66f-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="ed66f-128">Nakládka pro přepravu umožňuje seskupit pracovní řádky z jedné nebo několika nakládek.</span><span class="sxs-lookup"><span data-stu-id="ed66f-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="ed66f-129">Vše, co je přidáno k přepravní nakládce, pak lze expedovat pomocí mobilního skeneru.</span><span class="sxs-lookup"><span data-stu-id="ed66f-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="ed66f-130">Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="ed66f-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="ed66f-131">Vyberte **Nový** a poté v poli **Režim** vyberte **Práce**.</span><span class="sxs-lookup"><span data-stu-id="ed66f-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="ed66f-132">Nastavte hodnotu možnosti **Použít stávající práci** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ed66f-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="ed66f-133">Na kartě **Obecné** v poli **Směřuje** vyberte **Nakládka pro přepravu**.</span><span class="sxs-lookup"><span data-stu-id="ed66f-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="ed66f-134">Pro povolení potvrzení expedice na snímače mobilního zařízení v poli **Povolený typ potvrzení expedice** vyberte **Přeprava nákladu**.</span><span class="sxs-lookup"><span data-stu-id="ed66f-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="ed66f-135">Potvrdit expedici přepravy nákladu z klienta</span><span class="sxs-lookup"><span data-stu-id="ed66f-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="ed66f-136">Toto nastavení umožňuje potvrdit expedici nákladu obsahující úplný náklad nebo částečný náklad.</span><span class="sxs-lookup"><span data-stu-id="ed66f-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="ed66f-137">Vyberte **řízení skladu** \> **Nakládky** \> **Přeprava nakládky**.</span><span class="sxs-lookup"><span data-stu-id="ed66f-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="ed66f-138">V podokně akcí na kartě **Expedovat a přijmout** ve skupině **Potvrdit** vyberte **Přeprava**.</span><span class="sxs-lookup"><span data-stu-id="ed66f-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
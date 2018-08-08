---
title: "Nastavení výdejů v seskupení"
description: "Toto téma popisuje, jak nastavit výdej v seskupení a způsob použití potvrzení položek s výdejem v seskupení."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: a7adec850cfb473b0bfc9536dcb1ef1cfd74129a
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a><span data-ttu-id="30bb2-103">Nastavení výdejů v seskupení</span><span class="sxs-lookup"><span data-stu-id="30bb2-103">Set up cluster picking</span></span>

<span data-ttu-id="30bb2-104">Toto téma popisuje, jak umožnit zaměstnancům používat mobilní zařízení k seskupování výdejní práce do seskupení, takže mohou vyskladňovat zboží z jednoho místa pro několik pracovních objednávek současně.</span><span class="sxs-lookup"><span data-stu-id="30bb2-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="30bb2-105">Tento úkon se nazývá *výdej v seskupení*.</span><span class="sxs-lookup"><span data-stu-id="30bb2-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="30bb2-106">O výdeji v seskupení</span><span class="sxs-lookup"><span data-stu-id="30bb2-106">About cluster picking</span></span>

<span data-ttu-id="30bb2-107">Po uvolnění pracovních příkazů do skladu, pracovník použije mobilní zařízení k přiřazení objednávek k seskupení.</span><span class="sxs-lookup"><span data-stu-id="30bb2-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="30bb2-108">Seskupení bude organizovat výdejní práci pracovníka.</span><span class="sxs-lookup"><span data-stu-id="30bb2-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="30bb2-109">Když je pracovní objednávka přiřazena k seskupení, pracovník musí používat výdej v seskupení k provádění práce výdeje pro danou objednávku.</span><span class="sxs-lookup"><span data-stu-id="30bb2-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="30bb2-110">Pracovník nemůže použít jinou metodu výdeje.</span><span class="sxs-lookup"><span data-stu-id="30bb2-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="30bb2-111">Je-li pracovní objednávka přiřazena seskupení omylem, musí pracovník rozdělit seskupení a znovu jej vytvořit.</span><span class="sxs-lookup"><span data-stu-id="30bb2-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="30bb2-112">V případě potřeby pracovník může předat seskupení jinému pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="30bb2-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="30bb2-113">Tím se změní stav seskupení na Předáno.</span><span class="sxs-lookup"><span data-stu-id="30bb2-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="30bb2-114">Používá-li pracovník mobilní zařízení k označení, že je práce výdeje a příjmu dokončena, musí potvrdit dodávku nebo náklad v klientovi aplikace Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="30bb2-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the Dynamics 365 for Finance and Operations client.</span></span>

## <a name="set-up-cluster-picking"></a><span data-ttu-id="30bb2-115">Nastavení výdejů v seskupení</span><span class="sxs-lookup"><span data-stu-id="30bb2-115">Set up cluster picking</span></span>

<span data-ttu-id="30bb2-116">Chcete-li povolit výdej v seskupení, je nutné nastavit následující:</span><span class="sxs-lookup"><span data-stu-id="30bb2-116">To enable cluster picking, you must set up the following:</span></span>

-   <span data-ttu-id="30bb2-117">**Profily seskupení** – Určují, zda automaticky generovat ID seskupení, počet pozic, které mají být použity, kdy mají být seskupení rozdělena a jak řadit a ověřovat práci výdeje.</span><span class="sxs-lookup"><span data-stu-id="30bb2-117">**Cluster profiles** – Specify whether to automatically generate cluster IDs, the number of positions to use, when to break clusters, and how to sequence and verify the picking work.</span></span>

-   <span data-ttu-id="30bb2-118">**Šablony práce** – Definování způsobu vytváření práce výdeje pro výdej v seskupení.</span><span class="sxs-lookup"><span data-stu-id="30bb2-118">**Work templates** – Define how to create the picking work for cluster picking.</span></span>

-   <span data-ttu-id="30bb2-119">**Směrnice skladového místa** – Určují, odkud zboží vyskladňovat a kam ho dávat.</span><span class="sxs-lookup"><span data-stu-id="30bb2-119">**Location directives** – Specify where to pick items from, and where to put them.</span></span>

-   <span data-ttu-id="30bb2-120">**Položky nabídky mobilního zařízení** – Konfigurace položky nabídky mobilního zařízení pro použití stávající práce, která se řídí výdejem v seskupení.</span><span class="sxs-lookup"><span data-stu-id="30bb2-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="30bb2-121">Potom je nutné přidat položku nabídky do nabídky mobilního zařízení tak, aby se zobrazila v mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="30bb2-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

-   <span data-ttu-id="30bb2-122">**Parametry řízení skladu** – Zadání číselné řady, která se použije, pokud chcete generovat identifikátory pro seskupení.</span><span class="sxs-lookup"><span data-stu-id="30bb2-122">**Warehouse management parameters** – Specify the number sequence to use if you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="30bb2-123">Nastavení profilu seskupení</span><span class="sxs-lookup"><span data-stu-id="30bb2-123">Set up a cluster profile</span></span>

<span data-ttu-id="30bb2-124">Chcete-li nastavit profil seskupení, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="30bb2-124">To set up a cluster profile, follow these steps:</span></span>

1.  <span data-ttu-id="30bb2-125">Klikněte na **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Profily seskupení**.</span><span class="sxs-lookup"><span data-stu-id="30bb2-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \> **Cluster profiles**.</span></span>

2.  <span data-ttu-id="30bb2-126">Kliknutím na **Nový** vytvořte nový profil.</span><span class="sxs-lookup"><span data-stu-id="30bb2-126">Click **New** to create a new profile.</span></span>

3.  <span data-ttu-id="30bb2-127">Klikněte na tlačítko **Vytvořit seskupení** a pod položkou **Řazení seskupení** klikněte na **Nové** pro nastavení kritérií třídění pro seskupení.</span><span class="sxs-lookup"><span data-stu-id="30bb2-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="30bb2-128">Kritéria řazení řídí pořadí, ve kterém bude pracovník provádět práci výdeje.</span><span class="sxs-lookup"><span data-stu-id="30bb2-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="30bb2-129">Můžete přidat tolik kritérií, kolik potřebujete.</span><span class="sxs-lookup"><span data-stu-id="30bb2-129">You can add as many criteria as needed.</span></span>

4.  <span data-ttu-id="30bb2-130">V poli **Pořadové číslo** zadejte číslo pro definování pořadí, ve kterém se kritéria třídění zpracují.</span><span class="sxs-lookup"><span data-stu-id="30bb2-130">In the **Sequence number** field, enter a number to define the order in which the sorting criteria are processed.</span></span>

5.  <span data-ttu-id="30bb2-131">V poli **Název pole** vyberte pole, které určuje řazení.</span><span class="sxs-lookup"><span data-stu-id="30bb2-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="30bb2-132">Vyberete-li například pole **WMSLocationId**, práce bude seřazena podle umístění.</span><span class="sxs-lookup"><span data-stu-id="30bb2-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

6.  <span data-ttu-id="30bb2-133">V poli **Třídění** vyberte jednu z následujících možností.</span><span class="sxs-lookup"><span data-stu-id="30bb2-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="30bb2-134">**Parametr**</span><span class="sxs-lookup"><span data-stu-id="30bb2-134">**Option**</span></span>     | <span data-ttu-id="30bb2-135">**Popis**</span><span class="sxs-lookup"><span data-stu-id="30bb2-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30bb2-136">**Vzestupně**</span><span class="sxs-lookup"><span data-stu-id="30bb2-136">**Ascending**</span></span>  | <span data-ttu-id="30bb2-137">Práce výdeje je řazena ve vzestupném pořadí na základě kritérií třídění.</span><span class="sxs-lookup"><span data-stu-id="30bb2-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="30bb2-138">Používáte-li například pole **WMSLocationId** jako kritérium třídění a ID skladových míst jsou 1, 2, 3 a 4, výdeje bude nejprve ze skladového místa 4.</span><span class="sxs-lookup"><span data-stu-id="30bb2-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="30bb2-139">**Sestupně**</span><span class="sxs-lookup"><span data-stu-id="30bb2-139">**Descending**</span></span> | <span data-ttu-id="30bb2-140">Práce výdeje je řazena v sestupném pořadí na základě kritérií třídění.</span><span class="sxs-lookup"><span data-stu-id="30bb2-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="30bb2-141">Používáte-li například pole **WMSLocationId** jako kritérium třídění a ID skladových míst jsou 1, 2, 3 a 4, výdeje bude nejprve ze skladového místa 1.</span><span class="sxs-lookup"><span data-stu-id="30bb2-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="30bb2-142">Potvrzení položky</span><span class="sxs-lookup"><span data-stu-id="30bb2-142">Item confirmation</span></span>

<span data-ttu-id="30bb2-143">Při použití výdeje v seskupení je velmi důležité potvrzení položek k ověření položek, které jsou přidány do seskupení.</span><span class="sxs-lookup"><span data-stu-id="30bb2-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="30bb2-144">Při výdeji v seskupení můžete ověřit položky během procesu výdeje v seskupení.</span><span class="sxs-lookup"><span data-stu-id="30bb2-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="30bb2-145">Nastavení vychází z nastavení čárového kódu produktu.</span><span class="sxs-lookup"><span data-stu-id="30bb2-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="30bb2-146">Nastavení ověření položek s výdejem v seskupení</span><span class="sxs-lookup"><span data-stu-id="30bb2-146">Set up item verification with cluster picking</span></span>

1.  <span data-ttu-id="30bb2-147">V položce nabídky mobilního zařízení otevřete formulář nastavení pro potvrzení práce: **Řízení skladu** \> **Řízení skladu** \> **Nastavení** \> **Mobilní zařízení** \> **Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="30bb2-147">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** \> **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>

2.  <span data-ttu-id="30bb2-148">Z položky nabídky mobilního zařízení otevřete **Nastavení potvrzení práce**.</span><span class="sxs-lookup"><span data-stu-id="30bb2-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="30bb2-149">Možnost **Potvrzení produktu** umožňuje ověřit jednotlivé skladové položky z mobilního zařízení při naskenování.</span><span class="sxs-lookup"><span data-stu-id="30bb2-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>


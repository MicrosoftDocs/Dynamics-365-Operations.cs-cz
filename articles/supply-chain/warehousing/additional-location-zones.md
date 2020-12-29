---
title: Další zóny skladového místa
description: Toto téma poskytuje přehled nových zón skladového místa, jež byly přidány do systému Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424179"
---
# <a name="additional-location-zones"></a><span data-ttu-id="54bdb-103">Další zóny skladového místa</span><span class="sxs-lookup"><span data-stu-id="54bdb-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54bdb-104">V programu Microsoft Dynamics 365 Supply Chain Management jsou při zadávání nové zóny k dispozici tři pole.</span><span class="sxs-lookup"><span data-stu-id="54bdb-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="54bdb-105">Vedoucí skladu je mohou použít k definování dalších skladových organizací nebo rozvržení.</span><span class="sxs-lookup"><span data-stu-id="54bdb-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="54bdb-106">Pole nové zóny lze nastavit buď ručně nebo pomocí průvodce **Nastavení skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="54bdb-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="54bdb-107">Lze je použít v jakémkoli dotazu nebo při filtrování využívajícím tabulku Skladová místa.</span><span class="sxs-lookup"><span data-stu-id="54bdb-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="54bdb-108">K použití polí zón není nutné žádné další nastavení.</span><span class="sxs-lookup"><span data-stu-id="54bdb-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="54bdb-109">Zapnutí funkce Další zóna skladového místa</span><span class="sxs-lookup"><span data-stu-id="54bdb-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="54bdb-110">Než můžete použít funkci *Další zóna skladového místa*, musíte ji v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="54bdb-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="54bdb-111">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="54bdb-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="54bdb-112">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="54bdb-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="54bdb-113">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="54bdb-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="54bdb-114">**Název funkce:** *Další zóna skladového místa*</span><span class="sxs-lookup"><span data-stu-id="54bdb-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="54bdb-115">Používání zón skladového místa</span><span class="sxs-lookup"><span data-stu-id="54bdb-115">Use location zones</span></span>

1. <span data-ttu-id="54bdb-116">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Průvodce nastavením skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="54bdb-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="54bdb-117">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="54bdb-117">Set the following values:</span></span>

    - <span data-ttu-id="54bdb-118">V poli **Sklad** zvolte _62_.</span><span class="sxs-lookup"><span data-stu-id="54bdb-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="54bdb-119">V poli **ID zóny** vyberte hodnotu _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="54bdb-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="54bdb-120">V poli **Další zóna 1** vyberte hodnotu _VYSKLZÓNA1_.</span><span class="sxs-lookup"><span data-stu-id="54bdb-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="54bdb-121">V poli **Další zóna 2** vyberte hodnotu _WEBSHOP1_.</span><span class="sxs-lookup"><span data-stu-id="54bdb-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="54bdb-122">V poli **ID profilu skladového místa** vyberte hodnotu _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="54bdb-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="54bdb-123">Vyberte řádek **Podlaha**.</span><span class="sxs-lookup"><span data-stu-id="54bdb-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="54bdb-124">Do pole **Od čísla** zadejte hodnotu _1_.</span><span class="sxs-lookup"><span data-stu-id="54bdb-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="54bdb-125">Do pole **Do čísla** zadejte hodnotu _3_.</span><span class="sxs-lookup"><span data-stu-id="54bdb-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="54bdb-126">Vyberte řádek **Ulička**.</span><span class="sxs-lookup"><span data-stu-id="54bdb-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="54bdb-127">Do pole **Od čísla** zadejte hodnotu _1_.</span><span class="sxs-lookup"><span data-stu-id="54bdb-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="54bdb-128">Do pole **Do čísla** zadejte hodnotu _5_.</span><span class="sxs-lookup"><span data-stu-id="54bdb-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="54bdb-129">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="54bdb-129">Select **Create**.</span></span>
8. <span data-ttu-id="54bdb-130">Obdržíte zprávy uvádějící, že byla přidána nová skladová místa.</span><span class="sxs-lookup"><span data-stu-id="54bdb-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="54bdb-131">Tlačítkem **Zobrazit zprávy** tyto zprávy zobrazíte.</span><span class="sxs-lookup"><span data-stu-id="54bdb-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="54bdb-132">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Umístění**.</span><span class="sxs-lookup"><span data-stu-id="54bdb-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="54bdb-133">Nová skladová místa se zobrazí v seznamu a jsou k dispozici všechna pole zóny (tj. pole existující zóny i pole nové další zóny).</span><span class="sxs-lookup"><span data-stu-id="54bdb-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>

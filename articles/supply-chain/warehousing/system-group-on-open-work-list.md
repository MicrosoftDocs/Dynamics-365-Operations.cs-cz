---
title: "Systémové seskupení na otevřeném seznamu úkolů"
description: "Toto téma popisuje, jak filtrovat seznam otevřené práce u mobilního zařízení."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6403fea54be4036f7a15c05b46f70d258d97c3e2
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="cac77-103">Systémové seskupení na otevřeném seznamu úkolů</span><span class="sxs-lookup"><span data-stu-id="cac77-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cac77-104">Pomocí pole seskupení systému můžete filtrovat seznam otevřené práci bez nutnosti upravovat položku nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="cac77-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="cac77-105">V příslušných případech funguje seskupování systému k filtrování pracovního seznamu u jednoho pole záhlaví práce.</span><span class="sxs-lookup"><span data-stu-id="cac77-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="cac77-106">Systémové seskupení nelze použít k filtrování na úrovni polí řádku.</span><span class="sxs-lookup"><span data-stu-id="cac77-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="cac77-107">Nastavení systémového seskupení v otevřeném seznamu úkolů</span><span class="sxs-lookup"><span data-stu-id="cac77-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="cac77-108">Tyto kroky slouží k nastavení systémového seskupení v otevřeném seznamu úkolů.</span><span class="sxs-lookup"><span data-stu-id="cac77-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="cac77-109">Z položky nabídky mobilního zařízení vyberte **Režim: Nepřímý** a **Kód aktivity: Zobrazit otevřený pracovní seznam**.</span><span class="sxs-lookup"><span data-stu-id="cac77-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="cac77-110">K dispozici jsou následující možnosti.</span><span class="sxs-lookup"><span data-stu-id="cac77-110">The following options become available.</span></span> <span data-ttu-id="cac77-111">Tyto možnosti jsou požadovány pro systémové seskupení v otevřeném pracovním seznamu.</span><span class="sxs-lookup"><span data-stu-id="cac77-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="cac77-112">Parametr</span><span class="sxs-lookup"><span data-stu-id="cac77-112">Option</span></span>        | <span data-ttu-id="cac77-113">popis</span><span class="sxs-lookup"><span data-stu-id="cac77-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="cac77-114">Povolit seskupení systému</span><span class="sxs-lookup"><span data-stu-id="cac77-114">Allow system grouping</span></span>   | <span data-ttu-id="cac77-115">Umožňuje seskupení systému pro vybranou položku pracovního seznamu.</span><span class="sxs-lookup"><span data-stu-id="cac77-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="cac77-116">Pole systémového seskupení</span><span class="sxs-lookup"><span data-stu-id="cac77-116">System grouping field</span></span>   | <span data-ttu-id="cac77-117">K dispozici pouze v případě, že je možnost **Povolit systémovou práci** nastavena na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="cac77-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="cac77-118">Vyberte pole, které určuje způsob seskupení práce pro pracovníky.</span><span class="sxs-lookup"><span data-stu-id="cac77-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="cac77-119">Pokud například vyberete pole **ShipmentId**, pracovník naskenuje ID dodávky pro seskupení práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="cac77-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="cac77-120">Všechna práce pro dodávku bude přiřazena pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="cac77-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="cac77-121">Toto pole vyžaduje, abyste vytvořili položku nabídky pro stávající práci, která je seskupena podle systému.</span><span class="sxs-lookup"><span data-stu-id="cac77-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="cac77-122">Pole **Popisek systémového seskupení** použijte k informování pracovníka, co kontrolovat.</span><span class="sxs-lookup"><span data-stu-id="cac77-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="cac77-123">Popisek systémového seskupení</span><span class="sxs-lookup"><span data-stu-id="cac77-123">System grouping label</span></span>   | <span data-ttu-id="cac77-124">K dispozici pouze v případě, že je možnost **Povolit systémovou práci** nastavena na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="cac77-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="cac77-125">Zadejte informace pro pracovníka o tom, co kontrolovat při seskupení práce vyskladnění v aplikaci .</span><span class="sxs-lookup"><span data-stu-id="cac77-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="cac77-126">Používáte-li například pole **ShipmentId** pro seskupení práce výdeje podle dodávky, měli byste do pole zadat ID dodávky.</span><span class="sxs-lookup"><span data-stu-id="cac77-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="cac77-127">Toto pole vyžaduje, abyste vytvořili položku nabídky pro stávající práci, která je seskupena podle systému.</span><span class="sxs-lookup"><span data-stu-id="cac77-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="cac77-128">Je nutné zaškrtnout pole definující seskupení v poli **systémové seskupení**.</span><span class="sxs-lookup"><span data-stu-id="cac77-128">You must also select the field to group by in the **System grouping** field.</span></span>|


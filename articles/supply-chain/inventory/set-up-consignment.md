---
title: Konfigurace zásilky
description: Toto téma vysvětluje, jak nakonfigurovat operace příchozí skladové zásilky.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 24500ff46cc77ca8fa59c0c16427d9f05f33a87e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "308706"
---
# <a name="set-up-consignment"></a><span data-ttu-id="9045e-103">Konfigurace zásilky</span><span class="sxs-lookup"><span data-stu-id="9045e-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9045e-104">Toto téma vysvětluje, jak nakonfigurovat operace příchozí skladové zásilky.</span><span class="sxs-lookup"><span data-stu-id="9045e-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="9045e-105">Zásoby dodávky jsou zásoby, které vlastní dodavatel, ale jsou uloženy ve vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="9045e-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="9045e-106">Až budete připraveni spotřebovat nebo použít zásoby, převezmete vlastnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="9045e-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="9045e-107">Toto téma popisuje potřebné nastavení pro umožnění procesy dodávky.</span><span class="sxs-lookup"><span data-stu-id="9045e-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="9045e-108">Další informace o procesech dodávek naleznete v tématu [Zásilka](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="9045e-108">For more information about consignment processes, see [Consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="9045e-109">Vlastníci zásob</span><span class="sxs-lookup"><span data-stu-id="9045e-109">Inventory owners</span></span>
<span data-ttu-id="9045e-110">Aby bylo možné zaznamenat fyzickou zásilku zásob, je třeba definovat dodavatele vlastníka.</span><span class="sxs-lookup"><span data-stu-id="9045e-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="9045e-111">To se provádí na stránce **Vlastník zásob**.</span><span class="sxs-lookup"><span data-stu-id="9045e-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="9045e-112">Při výběru **Účet dodavatele** se generují výchozí hodnoty pro pole **Název** a **Vlastník**.</span><span class="sxs-lookup"><span data-stu-id="9045e-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="9045e-113">Hodnota v poli **Vlastník** se zobrazí dodavateli, takže ji můžete změnit v případě, že název účtu dodavatele se špatně rozpoznává externím uživatelům.</span><span class="sxs-lookup"><span data-stu-id="9045e-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="9045e-114">Je možné upravit pole **Vlastník**, ale pouze do okamžiku, když ukládáte záznam **Vlastník zásob**.</span><span class="sxs-lookup"><span data-stu-id="9045e-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="9045e-115">Pole **Název** se vyplňuje s názvem strany, k níž je přidružen účet dodavatele, a nemůže být změněno.</span><span class="sxs-lookup"><span data-stu-id="9045e-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="9045e-116">[![vlastníci-zásob](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="9045e-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="9045e-117">Skupina sledovací dimenze</span><span class="sxs-lookup"><span data-stu-id="9045e-117">Tracking dimension group</span></span>
<span data-ttu-id="9045e-118">Položky, které chcete použít v procesech dodávky, musí být přidruženy k **Skupina sledovací dimenze** kde dimenze **Vlastník** je nastavena na **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="9045e-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="9045e-119">Dimenze vlastníka má vždy vybrané možnosti **Fyzické zásoby** a **Finanční zásoby**.</span><span class="sxs-lookup"><span data-stu-id="9045e-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="9045e-120">Nikdy není vybrána možnost **Plán disponibility podle dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="9045e-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="9045e-121">[![skupina-sledovací-dimenze](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="9045e-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="9045e-122">Deník změn vlastnictví zásob</span><span class="sxs-lookup"><span data-stu-id="9045e-122">Inventory ownership change journal</span></span>
<span data-ttu-id="9045e-123">Deník **Změny vlastnictví zásob**se používá k zaznamenání k přesunu vlastnictví dodávek zásob od dodavatele na stávající právnickou osobu, která ho využívá.</span><span class="sxs-lookup"><span data-stu-id="9045e-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="9045e-124">Stejně jako jakýkoliv deník zásob musí být označen názvem deníku zásob.</span><span class="sxs-lookup"><span data-stu-id="9045e-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="9045e-125">Tyto názvy jsou vytvářeny na stránce **Názvy deníků zásob**, kde **Typ deníku** musí být nastaven na **Změny vlastnictví**.</span><span class="sxs-lookup"><span data-stu-id="9045e-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="9045e-126">[![Deník-změn-vlastnictví-zásob](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="9045e-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="9045e-127">Dodavatelská spolupráce v procesech zásilky</span><span class="sxs-lookup"><span data-stu-id="9045e-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="9045e-128">Pokud vaši dodavatelé využívají rozhraní dodavatelské spolupráce, mohou ho využívat ke sledování spotřeby zásob vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="9045e-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="9045e-129">Další informace o nastavení dodavatelů pro použití dodavatelské spolupráce naleznete v tématu [Konfigurace zabezpečení pro uživatele portálu Spolupráce dodavatele](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="9045e-129">For more information about setting up vendors to use vendor collaboration, see [Configuration of security for vendor collaboration users](../procurement/configure-security-vendor-portal-users.md).</span></span>

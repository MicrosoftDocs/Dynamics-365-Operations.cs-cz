---
title: Konfigurace zásilky
description: Toto téma vysvětluje, jak nakonfigurovat operace příchozí skladové zásilky.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 00102f5c7a043c5ca22458a53b1445c57c61957c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209556"
---
# <a name="set-up-consignment"></a><span data-ttu-id="c2de4-103">Konfigurace zásilky</span><span class="sxs-lookup"><span data-stu-id="c2de4-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2de4-104">Toto téma vysvětluje, jak nakonfigurovat operace příchozí skladové zásilky.</span><span class="sxs-lookup"><span data-stu-id="c2de4-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="c2de4-105">Zásoby dodávky jsou zásoby, které vlastní dodavatel, ale jsou uloženy ve vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="c2de4-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="c2de4-106">Až budete připraveni spotřebovat nebo použít zásoby, převezmete vlastnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="c2de4-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="c2de4-107">Toto téma popisuje potřebné nastavení pro umožnění procesy dodávky.</span><span class="sxs-lookup"><span data-stu-id="c2de4-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="c2de4-108">Další informace o procesech dodávek naleznete v tématu [Nastavení zásilky](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="c2de4-108">For more information about consignment processes, see [Set up consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="c2de4-109">Vlastníci zásob</span><span class="sxs-lookup"><span data-stu-id="c2de4-109">Inventory owners</span></span>
<span data-ttu-id="c2de4-110">Aby bylo možné zaznamenat fyzickou zásilku zásob, je třeba definovat dodavatele vlastníka.</span><span class="sxs-lookup"><span data-stu-id="c2de4-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="c2de4-111">To se provádí na stránce **Vlastník zásob**.</span><span class="sxs-lookup"><span data-stu-id="c2de4-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="c2de4-112">Při výběru **Účet dodavatele** se generují výchozí hodnoty pro pole **Název** a **Vlastník**.</span><span class="sxs-lookup"><span data-stu-id="c2de4-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="c2de4-113">Hodnota v poli **Vlastník** se zobrazí dodavateli, takže ji můžete změnit v případě, že název účtu dodavatele se špatně rozpoznává externím uživatelům.</span><span class="sxs-lookup"><span data-stu-id="c2de4-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="c2de4-114">Je možné upravit pole **Vlastník**, ale pouze do okamžiku, když ukládáte záznam **Vlastník zásob**.</span><span class="sxs-lookup"><span data-stu-id="c2de4-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="c2de4-115">Pole **Název** se vyplňuje s názvem strany, k níž je přidružen účet dodavatele, a nemůže být změněno.</span><span class="sxs-lookup"><span data-stu-id="c2de4-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="c2de4-116">[![vlastníci-zásob](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="c2de4-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="c2de4-117">Skupina sledovací dimenze</span><span class="sxs-lookup"><span data-stu-id="c2de4-117">Tracking dimension group</span></span>
<span data-ttu-id="c2de4-118">Položky, které chcete použít v procesech dodávky, musí být přidruženy k **Skupina sledovací dimenze** kde dimenze **Vlastník** je nastavena na **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="c2de4-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="c2de4-119">Dimenze vlastníka má vždy vybrané možnosti **Fyzické zásoby** a **Finanční zásoby**.</span><span class="sxs-lookup"><span data-stu-id="c2de4-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="c2de4-120">Nikdy není vybrána možnost **Plán disponibility podle dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="c2de4-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="c2de4-121">[![skupina-sledovací-dimenze](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="c2de4-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="c2de4-122">Deník změn vlastnictví zásob</span><span class="sxs-lookup"><span data-stu-id="c2de4-122">Inventory ownership change journal</span></span>
<span data-ttu-id="c2de4-123">Deník **Změny vlastnictví zásob** se používá k zaznamenání k přesunu vlastnictví dodávek zásob od dodavatele na stávající právnickou osobu, která ho využívá.</span><span class="sxs-lookup"><span data-stu-id="c2de4-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="c2de4-124">Stejně jako jakýkoliv deník zásob musí být označen názvem deníku zásob.</span><span class="sxs-lookup"><span data-stu-id="c2de4-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="c2de4-125">Tyto názvy jsou vytvářeny na stránce **Názvy deníků zásob**, kde **Typ deníku** musí být nastaven na **Změny vlastnictví**.</span><span class="sxs-lookup"><span data-stu-id="c2de4-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="c2de4-126">[![Deník-změn-vlastnictví-zásob](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="c2de4-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="c2de4-127">Dodavatelská spolupráce v procesech zásilky</span><span class="sxs-lookup"><span data-stu-id="c2de4-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="c2de4-128">Pokud vaši dodavatelé využívají rozhraní dodavatelské spolupráce, mohou ho využívat ke sledování spotřeby zásob vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="c2de4-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="c2de4-129">Další informace o nastavení dodavatelů pro použití dodavatelské spolupráce naleznete v tématu [Zabezpečení uživatele dodavatelského portálu](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="c2de4-129">For more information about setting up vendors to use vendor collaboration, see [Vendor portal user security](../procurement/configure-security-vendor-portal-users.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
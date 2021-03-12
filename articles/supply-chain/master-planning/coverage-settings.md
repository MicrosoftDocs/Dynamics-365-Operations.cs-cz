---
title: Nastavení distponibility
description: Toto téma poskytuje informace o nastavení disponibility, které hlavní plánování používá k výpočtu požadavků na položky.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0aaacf28701542d329afedd8206a12f7c11b7ac7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999974"
---
# <a name="coverage-settings"></a><span data-ttu-id="7d17d-103">Nastavení distponibility</span><span class="sxs-lookup"><span data-stu-id="7d17d-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d17d-104">Při hlavním plánování se používá nastavení disponibility k výpočtu požadavků na položku.</span><span class="sxs-lookup"><span data-stu-id="7d17d-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="7d17d-105">Existuje několik způsobů, jak zadat nastavení disponibility:</span><span class="sxs-lookup"><span data-stu-id="7d17d-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="7d17d-106">Nastavte disponibilitu skupiny.</span><span class="sxs-lookup"><span data-stu-id="7d17d-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="7d17d-107">Můžete vytvořit skupinu disponibility, která obsahuje nastavení pro všechny produkty spojené s touto skupinou disponibility.</span><span class="sxs-lookup"><span data-stu-id="7d17d-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="7d17d-108">Přejděte na **Hlavní plánování &gt; Nastavení &gt; Disponibilita &gt; Skupiny disponibility** a vytvořte tak skupinu disponibility.</span><span class="sxs-lookup"><span data-stu-id="7d17d-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="7d17d-109">Můžete propojit skupinu disponibility s produktem.</span><span class="sxs-lookup"><span data-stu-id="7d17d-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="7d17d-110">Pokud je odkaz na konkrétní pracoviště, sklad nebo dimenze produktu, použijte pole **Skupina disponibility** na stránce **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="7d17d-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="7d17d-111">Pokud je propojení obecné, bez ohledu na dimenze produktu, použijte pole **Skupina disponibility** na pevné záložce **Plán** stránky **Podrobnosti o produktu**.</span><span class="sxs-lookup"><span data-stu-id="7d17d-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="7d17d-112">Pokud ve výchozím nastavení nespojíte skupinu disponibility s produktem, hlavní plánování bude používat obecnou skupinu disponibility, která je určena na stránce **Parametry hlavního plánování**.</span><span class="sxs-lookup"><span data-stu-id="7d17d-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="7d17d-113">Nastavte disponibilitu produktu.</span><span class="sxs-lookup"><span data-stu-id="7d17d-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="7d17d-114">Nastavení pokrytí lze vytvořit pro určitý produkt.</span><span class="sxs-lookup"><span data-stu-id="7d17d-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="7d17d-115">Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="7d17d-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="7d17d-116">Vyberte produkt a pak v podokně akcí na kartě **Plán** ve **skupině disponibility** zvolte **Disponibilita položky** pro otevření stránky **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="7d17d-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="7d17d-117">Je-li produkt již spojen se skupinou disponibility, můžete nastavení skupiny disponibility přepsat v poli **Přepsat**.</span><span class="sxs-lookup"><span data-stu-id="7d17d-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="7d17d-118">Nastavení disponibility na stránce **Disponibilita položky** má přednost před nastavením na stránce **Skupina disponibility**.</span><span class="sxs-lookup"><span data-stu-id="7d17d-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="7d17d-119">Nastavení disponibility produktu pomocí průvodce.</span><span class="sxs-lookup"><span data-stu-id="7d17d-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="7d17d-120">Průvodce vás provede jednotlivými kroky procesu nastavení parametrů disponibility primární položky.</span><span class="sxs-lookup"><span data-stu-id="7d17d-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="7d17d-121">Na stránce **Disponibilita položky** v podokně akcí zvolte **Průvodce** a otevřete **Průvodce disponibilitou položky**.</span><span class="sxs-lookup"><span data-stu-id="7d17d-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="7d17d-122">Nastavení disponibility pro skupinu dimenzí.</span><span class="sxs-lookup"><span data-stu-id="7d17d-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="7d17d-123">Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="7d17d-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="7d17d-124">Na stránce **Podrobnosti o uvolněném produktu** na záložce s náhledem **Obecné** v části **Správa** zvolte odkaz v poli **Skupina dimenze úložiště**.</span><span class="sxs-lookup"><span data-stu-id="7d17d-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="7d17d-125">Na stránce **Skupiny dimenze úložiště** vyberte zaškrtávací pole **Plán disponibility podle dimenzí** a vytvořte tak nastavení disponibility pro dimenzi ve skupině dimenzí úložiště.</span><span class="sxs-lookup"><span data-stu-id="7d17d-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="7d17d-126">Pole **Plán disponibility podle dimenzí** musí mít vybráno pro všechny dimenze produktu, jako je například konfigurace, barva, velikost nebo styl.</span><span class="sxs-lookup"><span data-stu-id="7d17d-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="7d17d-127">Kódy pokrytí</span><span class="sxs-lookup"><span data-stu-id="7d17d-127">Coverage codes</span></span>

<span data-ttu-id="7d17d-128">Hlavní plánování lze nakonfigurovat tak, aby používalo různé metody doplnění.</span><span class="sxs-lookup"><span data-stu-id="7d17d-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="7d17d-129">Metody doplnění nebo metody určení velikosti šarží jsou techniky používanými systémem ke stanovení velikosti dávky pro nakoupené nebo vyráběné položky.</span><span class="sxs-lookup"><span data-stu-id="7d17d-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="7d17d-130">Každá metoda doplnění je přiřazena k jednomu z následujících kódů pokrytí:</span><span class="sxs-lookup"><span data-stu-id="7d17d-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="7d17d-131">**Ruční** - určení velikosti šarže, při kterém systém nenavrhuje nákup, převod nebo výrobní objednávky pro danou položku.</span><span class="sxs-lookup"><span data-stu-id="7d17d-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="7d17d-132">Plánovač pro danou položku bude mít na starosti vytváření požadovaných objednávek pro doplnění položky.</span><span class="sxs-lookup"><span data-stu-id="7d17d-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="7d17d-133">**Podle požadavku** – velikost šarže, při které systém vytváří plánovaný nákup, převod nebo výrobní zakázku podle požadavků na položku.</span><span class="sxs-lookup"><span data-stu-id="7d17d-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="7d17d-134">Obvykle se používá pro nákladné položky s nárazovou poptávkou.</span><span class="sxs-lookup"><span data-stu-id="7d17d-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="7d17d-135">**Za období** - určení velikosti šarže, které kombinuje všechny požadavky na období do jedné objednávky pro danou položku.</span><span class="sxs-lookup"><span data-stu-id="7d17d-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="7d17d-136">Zakázka bude naplánována pro první den období a její množství bude plnit čisté požadavky během stanoveného období.</span><span class="sxs-lookup"><span data-stu-id="7d17d-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="7d17d-137">Toto období začíná první poptávkou položky a pokrývá určenou délku v čase.</span><span class="sxs-lookup"><span data-stu-id="7d17d-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="7d17d-138">Další období bude začínat následujícími požadavky položky.</span><span class="sxs-lookup"><span data-stu-id="7d17d-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="7d17d-139">**Min/max** – metoda velikosti šarže, která obsahuje doplnění zásob na určitou úroveň, pokud je odhadovaná zásoba nižší než prahová hodnota.</span><span class="sxs-lookup"><span data-stu-id="7d17d-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="7d17d-140">Množství doplnění bude rozdíl mezi maximální úrovní a předpokládanou úrovní zásob na skladě.</span><span class="sxs-lookup"><span data-stu-id="7d17d-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="7d17d-141">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7d17d-141">Additional resources</span></span>

[<span data-ttu-id="7d17d-142">Přehled hlavních plánů</span><span class="sxs-lookup"><span data-stu-id="7d17d-142">Master plans overview</span></span>](master-plans.md)

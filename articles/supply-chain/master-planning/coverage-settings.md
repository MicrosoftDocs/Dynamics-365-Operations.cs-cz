---
title: Nastavení distponibility
description: Toto téma poskytuje informace o nastavení disponibility, které hlavní plánování používá k výpočtu požadavků na položky.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538887"
---
# <a name="coverage-settings"></a><span data-ttu-id="19ea8-103">Nastavení distponibility</span><span class="sxs-lookup"><span data-stu-id="19ea8-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19ea8-104">Při hlavním plánování se používá nastavení disponibility k výpočtu požadavků na položku.</span><span class="sxs-lookup"><span data-stu-id="19ea8-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="19ea8-105">Existuje několik způsobů, jak zadat nastavení disponibility:</span><span class="sxs-lookup"><span data-stu-id="19ea8-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="19ea8-106">Nastavte disponibilitu skupiny.</span><span class="sxs-lookup"><span data-stu-id="19ea8-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="19ea8-107">Můžete vytvořit skupinu disponibility, která obsahuje nastavení pro všechny produkty spojené s touto skupinou disponibility.</span><span class="sxs-lookup"><span data-stu-id="19ea8-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="19ea8-108">Přejděte na **Hlavní plánování &gt; Nastavení &gt; Disponibilita &gt; Skupiny disponibility** a vytvořte tak skupinu disponibility.</span><span class="sxs-lookup"><span data-stu-id="19ea8-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="19ea8-109">Můžete propojit skupinu disponibility s produktem.</span><span class="sxs-lookup"><span data-stu-id="19ea8-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="19ea8-110">Pokud je odkaz na konkrétní pracoviště, sklad nebo dimenze produktu, použijte pole **Skupina disponibility** na stránce **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="19ea8-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="19ea8-111">Pokud je propojení obecné, bez ohledu na dimenze produktu, použijte pole **Skupina disponibility** na pevné záložce **Plán** stránky **Podrobnosti o produktu**.</span><span class="sxs-lookup"><span data-stu-id="19ea8-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="19ea8-112">Pokud ve výchozím nastavení nespojíte skupinu disponibility s produktem, hlavní plánování bude používat obecnou skupinu disponibility, která je určena na stránce **Parametry hlavního plánování**.</span><span class="sxs-lookup"><span data-stu-id="19ea8-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="19ea8-113">Nastavte disponibilitu produktu.</span><span class="sxs-lookup"><span data-stu-id="19ea8-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="19ea8-114">Nastavení pokrytí lze vytvořit pro určitý produkt.</span><span class="sxs-lookup"><span data-stu-id="19ea8-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="19ea8-115">Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="19ea8-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="19ea8-116">Vyberte produkt a pak v podokně akcí na kartě **Plán** ve **skupině disponibility** zvolte **Disponibilita položky** pro otevření stránky **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="19ea8-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="19ea8-117">Je-li produkt již spojen se skupinou disponibility, můžete nastavení skupiny disponibility přepsat v poli **Přepsat**.</span><span class="sxs-lookup"><span data-stu-id="19ea8-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="19ea8-118">Nastavení disponibility na stránce**Disponibilita položky** má přednost před nastavením na stránce **Skupina disponibility**.</span><span class="sxs-lookup"><span data-stu-id="19ea8-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="19ea8-119">Nastavení disponibility produktu pomocí průvodce.</span><span class="sxs-lookup"><span data-stu-id="19ea8-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="19ea8-120">Průvodce vás provede jednotlivými kroky procesu nastavení parametrů disponibility primární položky.</span><span class="sxs-lookup"><span data-stu-id="19ea8-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="19ea8-121">Na stránce **Disponibilita položky** v podokně akcí zvolte **Průvodce** a otevřete **Průvodce disponibilitou položky**.</span><span class="sxs-lookup"><span data-stu-id="19ea8-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="19ea8-122">Nastavení disponibility pro skupinu dimenzí.</span><span class="sxs-lookup"><span data-stu-id="19ea8-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="19ea8-123">Přejděte na **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="19ea8-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="19ea8-124">Na stránce **Podrobnosti o uvolněném produktu** na záložce s náhledem **Obecné** v části **Správa** zvolte odkaz v poli **Skupina dimenze úložiště**.</span><span class="sxs-lookup"><span data-stu-id="19ea8-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="19ea8-125">Na stránce **Skupiny dimenze úložiště** vyberte zaškrtávací pole **Plán disponibility podle dimenzí** a vytvořte tak nastavení disponibility pro dimenzi ve skupině dimenzí úložiště.</span><span class="sxs-lookup"><span data-stu-id="19ea8-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="19ea8-126">Pole **Plán disponibility podle dimenzí** musí mít vybráno pro všechny dimenze produktu, jako je například konfigurace, barva, velikost nebo styl.</span><span class="sxs-lookup"><span data-stu-id="19ea8-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19ea8-127">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="19ea8-127">Additional resources</span></span>

[<span data-ttu-id="19ea8-128">Hlavní plány</span><span class="sxs-lookup"><span data-stu-id="19ea8-128">Master plans</span></span>](master-plans.md)

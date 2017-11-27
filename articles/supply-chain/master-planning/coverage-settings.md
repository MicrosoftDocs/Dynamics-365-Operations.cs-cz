---
title: "Nastavení pokrytí"
description: "Při hlavním plánování se používá nastavení disponibility k výpočtu požadavků na položku."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bd85f89917659ac9c94590bace765b2123d6e556
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="coverage-settings"></a><span data-ttu-id="61e25-103">Nastavení pokrytí</span><span class="sxs-lookup"><span data-stu-id="61e25-103">Coverage settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="61e25-104">Při hlavním plánování se používá nastavení disponibility k výpočtu požadavků na položku.</span><span class="sxs-lookup"><span data-stu-id="61e25-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="61e25-105">Existuje několik způsobů, jak zadat nastavení disponibility:</span><span class="sxs-lookup"><span data-stu-id="61e25-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="61e25-106">Nastavte disponibilitu skupiny.</span><span class="sxs-lookup"><span data-stu-id="61e25-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="61e25-107">Můžete vytvořit skupinu disponibility, která obsahuje nastavení pro všechny produkty spojené s touto skupinou disponibility.</span><span class="sxs-lookup"><span data-stu-id="61e25-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="61e25-108">Klikněte na tlačítko **Hlavní plánování &gt; Nastavení &gt; Disponibilita &gt; Skupiny disponibility** a vytvořte tak skupinu disponibility.</span><span class="sxs-lookup"><span data-stu-id="61e25-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="61e25-109">Můžete propojit skupinu disponibility s produktem.</span><span class="sxs-lookup"><span data-stu-id="61e25-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="61e25-110">Pokud je odkaz na konkrétní pracoviště, sklad nebo dimenze produktu, použijte pole **Skupina disponibility** na stránce **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="61e25-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="61e25-111">Pokud je propojení obecné, bez ohledu na dimenze produktu, použijte **Skupina disponibility** na pevné záložce **Plán** na stránce **Podrobnosti o produktu**.</span><span class="sxs-lookup"><span data-stu-id="61e25-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="61e25-112">Pokud nespojíte skupinu disponibility s produktem, hlavní plánování bude ve výchozím nastavení používat **Obecná skupina disponibility**, která je určena na stránce **Parametry hlavního plánování**.</span><span class="sxs-lookup"><span data-stu-id="61e25-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="61e25-113">Nastavte disponibilitu produktu.</span><span class="sxs-lookup"><span data-stu-id="61e25-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="61e25-114">Nastavení pokrytí lze vytvořit pro určitý produkt.</span><span class="sxs-lookup"><span data-stu-id="61e25-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="61e25-115">Klikněte na možnosti **Řízení informací o produktech &gt; Produkty &gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="61e25-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="61e25-116">Vyberte produkt v **podokně akcí** na kartě **Plán** a ve **skupině disponibility**otevřete kliknutím na tlačítko **Disponibilita položky** stránku **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="61e25-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="61e25-117">Je-li produkt již spojen se skupinou disponibility, můžete nastavení skupiny disponibility přepsat v poli **Přepsat**.</span><span class="sxs-lookup"><span data-stu-id="61e25-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="61e25-118">Nastavení disponibility na stránce**Disponibilita položky** má přednost před nastavením na stránce **Skupina disponibility**.</span><span class="sxs-lookup"><span data-stu-id="61e25-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="61e25-119">Nastavení disponibility produktu pomocí průvodce.</span><span class="sxs-lookup"><span data-stu-id="61e25-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="61e25-120">Průvodce vám pomůže nastavit parametry disponibility pro hlavní položku krok za krokem.</span><span class="sxs-lookup"><span data-stu-id="61e25-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="61e25-121">Na stránce **Disponibilita položky** klepnutím na **Průvodce** otevřete **Průvodce disponibilitou položky**.</span><span class="sxs-lookup"><span data-stu-id="61e25-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

-   <span data-ttu-id="61e25-122">Nastavení disponibility pro skupinu dimenzí.</span><span class="sxs-lookup"><span data-stu-id="61e25-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="61e25-123">Klikněte na **Řízení informací o produktech &gt; Společné &gt; Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="61e25-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="61e25-124">Na stránce **Podrobnosti o uvolněném produktu **na kartě **Hlavní** ve skupině **Správa** klikněte na odkaz **Skupina dimenze úložiště**.</span><span class="sxs-lookup"><span data-stu-id="61e25-124">On the **Released product detail **page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="61e25-125">Na stránce **Skupina dimenze úložiště** vyberte pole **Plán disponibility podle dimenzí** a vytvořte tak nastavení disponibility pro dimenzi ve skupině dimenzí úložiště.</span><span class="sxs-lookup"><span data-stu-id="61e25-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="61e25-126">Všechny dimenze produktu, například jako konfigurace, barva, velikost nebo styl, musí mít vybráno pole **Plán disponibility podle dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="61e25-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="61e25-127">Viz také</span><span class="sxs-lookup"><span data-stu-id="61e25-127">See also</span></span>
--------

[<span data-ttu-id="61e25-128">Hlavní plány</span><span class="sxs-lookup"><span data-stu-id="61e25-128">Master plans</span></span>](master-plans.md)





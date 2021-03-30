---
title: Konfigurace kanálu pro použití hierarchie navigace sítě
description: Toto téma popisuje, jak konfigurovat kanál pro použití hierarchie navigace kanálu v aplikaci Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ceb6aa65c2ed5bc8d4224bdaf7095fba769181e8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220575"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="deca8-103">Konfigurace kanálu pro použití hierarchie navigace sítě</span><span class="sxs-lookup"><span data-stu-id="deca8-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="deca8-104">Toto téma popisuje, jak konfigurovat kanál pro použití hierarchie navigace kanálu v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="deca8-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="deca8-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="deca8-105">Overview</span></span>

<span data-ttu-id="deca8-106">Hierarchie navigace kanálů uspořádá produkty do kategorií, aby je bylo možné procházet na stránkách e-Commerce nebo v prodejních místech (POS).</span><span class="sxs-lookup"><span data-stu-id="deca8-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="deca8-107">Maloobchodní a online kanály musí být nakonfigurovány s hierarchií navigačních kanálů.</span><span class="sxs-lookup"><span data-stu-id="deca8-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="deca8-108">Konfigurace kanálu</span><span class="sxs-lookup"><span data-stu-id="deca8-108">Configure the channel</span></span>

<span data-ttu-id="deca8-109">Chcete-li konfigurovat kanál pro použití hierarchie navigace sítě, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="deca8-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="deca8-110">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.</span><span class="sxs-lookup"><span data-stu-id="deca8-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="deca8-111">Vyberte kanál, který chcete konfigurovat.</span><span class="sxs-lookup"><span data-stu-id="deca8-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="deca8-112">V podokně akcí zvolte **Nastavit metadata atributu**.</span><span class="sxs-lookup"><span data-stu-id="deca8-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="deca8-113">V rozevíracím seznamu **Hierarchie kategorií** vyberte patřičnou hierarchii navigace kanálu.</span><span class="sxs-lookup"><span data-stu-id="deca8-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="deca8-114">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="deca8-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="deca8-115">V položce **Skupina atributů** přidejte všechny skupiny atributů, které budou globálními atributy pro všechny uzly.</span><span class="sxs-lookup"><span data-stu-id="deca8-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="deca8-116">Následující obrázek ukazuje, jak konfigurovat kanál pro použití hierarchie navigace sítě.</span><span class="sxs-lookup"><span data-stu-id="deca8-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Příklad konfigurace kanálu](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="deca8-118">Nastavit metadata atributu</span><span class="sxs-lookup"><span data-stu-id="deca8-118">Set attribute metadata</span></span>

<span data-ttu-id="deca8-119">Nastavení metadat atributu umožní konfiguraci atributů v každém uzlu.</span><span class="sxs-lookup"><span data-stu-id="deca8-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="deca8-120">Pro nastavení metadat atributů postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="deca8-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="deca8-121">V podokně akcí zvolte **Nastavit metadata atributu**.</span><span class="sxs-lookup"><span data-stu-id="deca8-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="deca8-122">Pro každý uzel vyberte **Atributy produktu kanálu**.</span><span class="sxs-lookup"><span data-stu-id="deca8-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="deca8-123">Nastavte **Zobrazit atribut na kanálu** na **Ano** a **Lze upřesnit** na **Ano**, chcete-li povolit zpřesnění na daném kanálu.</span><span class="sxs-lookup"><span data-stu-id="deca8-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="deca8-124">Po nakonfigurování každého uzlu podle potřeby vyberte v **Podokně akcí** tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="deca8-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="deca8-125">Vyberte **X** v pravém horním rohu, chcete-li ukončit tuto obrazovku a vrátit se zpět na stránku **Kategorie kanálu a atributy produktu**.</span><span class="sxs-lookup"><span data-stu-id="deca8-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="deca8-126">Následující obrázek znázorňuje ukázkovou sadu atributů produktu kanálu nakonfigurovaných v uzlu kategorie kanálu.</span><span class="sxs-lookup"><span data-stu-id="deca8-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Atributy kanálu v uzlu kategorie kanálu](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="deca8-128">Publikovat změny</span><span class="sxs-lookup"><span data-stu-id="deca8-128">Publish changes</span></span>

<span data-ttu-id="deca8-129">Změny se projeví až po publikování změn.</span><span class="sxs-lookup"><span data-stu-id="deca8-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="deca8-130">Změny se publikují tímto způsobem.</span><span class="sxs-lookup"><span data-stu-id="deca8-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="deca8-131">V podokně akcí vyberte možnost **Publikovat aktualizace kanálů**.</span><span class="sxs-lookup"><span data-stu-id="deca8-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="deca8-132">V podokně **Publikovat aktualizace kanálů** vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="deca8-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="deca8-133">Následující obrázek ukazuje, jak publikovat aktualizace kanálů.</span><span class="sxs-lookup"><span data-stu-id="deca8-133">The following image shows how to publish channel updates.</span></span>

![Publikovat aktualizace kanálů](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="deca8-135">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="deca8-135">Additional resources</span></span>

[<span data-ttu-id="deca8-136">Vytvoření hierarchie navigace sítě</span><span class="sxs-lookup"><span data-stu-id="deca8-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
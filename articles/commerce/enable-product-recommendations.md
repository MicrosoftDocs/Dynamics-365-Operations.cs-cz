---
title: Povolit doporučení produktu
description: V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770132"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="2404e-103">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="2404e-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2404e-104">V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2404e-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="2404e-105">Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="2404e-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="2404e-106">Předběžná kontrola doporučení</span><span class="sxs-lookup"><span data-stu-id="2404e-106">Recommendations pre-check</span></span>
<span data-ttu-id="2404e-107">Před povolením berte prosím na vědomí, že doporučení produktů jsou podporována pouze u zákazníků F&O podporujících sestavení 10.0.6, kteří migrovali své úložiště pomocí BDL.</span><span class="sxs-lookup"><span data-stu-id="2404e-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="2404e-108">Dále zkontrolujte, zda byly povoleny ukazatele RetailSale.</span><span class="sxs-lookup"><span data-stu-id="2404e-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="2404e-109">Další informace o tomto procesu nastavení naleznete [zde.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="2404e-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="2404e-110">Zapnutí doporučení</span><span class="sxs-lookup"><span data-stu-id="2404e-110">Turn on recommendations</span></span>

<span data-ttu-id="2404e-111">Chcete-li zapnout doporučení produktu, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="2404e-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="2404e-112">Přejděte na **Maloobchod** &gt; **Doporučení produktů** &gt; **Parametry doporučení**.</span><span class="sxs-lookup"><span data-stu-id="2404e-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="2404e-113">V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.</span><span class="sxs-lookup"><span data-stu-id="2404e-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="2404e-114">Nastavte možnost **Povolit doporučení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="2404e-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![Povolení doporučení produktu](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="2404e-116">Tento postup spustí proces generování seznamů doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="2404e-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="2404e-117">Před tím, než jsou seznamy k dispozici, může uběhnou až několik hodin. Zobrazí se na pokladním místě (POS) nebo v řešení Dynamics 365 for Commerce.</span><span class="sxs-lookup"><span data-stu-id="2404e-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="2404e-118">Konfigurace parametrů seznamu doporučení</span><span class="sxs-lookup"><span data-stu-id="2404e-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="2404e-119">Ve výchozím nastavení poskytují seznamy doporučení produktů na bázi AI-ML navrhované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="2404e-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="2404e-120">Výchozí navrhované hodnoty lze změnit tak, aby vyhovovaly toku vašeho podniku.</span><span class="sxs-lookup"><span data-stu-id="2404e-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="2404e-121">Další informace o tom, jak změnit výchozí parametry, naleznete v části [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="2404e-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="2404e-122">Zobrazení doporučení na zařízeních POS</span><span class="sxs-lookup"><span data-stu-id="2404e-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="2404e-123">Po povolení doporučení v administrativě je nutné přidat panel doporučení na řídicí obrazovku POS pomocí nástroje pro rozložení.</span><span class="sxs-lookup"><span data-stu-id="2404e-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="2404e-124">Informace o tomto procesu naleznete [zde.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="2404e-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="2404e-125">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2404e-125">Additional resources</span></span>

[<span data-ttu-id="2404e-126">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="2404e-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="2404e-127">Přidání seznamů doporučení produktu na stránky</span><span class="sxs-lookup"><span data-stu-id="2404e-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="2404e-128">Přidání panelu doporučení do zařízení POS</span><span class="sxs-lookup"><span data-stu-id="2404e-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)



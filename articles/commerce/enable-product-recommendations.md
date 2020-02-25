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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024949"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="7d9f3-103">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="7d9f3-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7d9f3-104">V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="7d9f3-105">Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="7d9f3-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="7d9f3-106">Předběžná kontrola doporučení</span><span class="sxs-lookup"><span data-stu-id="7d9f3-106">Recommendations pre-check</span></span>

<span data-ttu-id="7d9f3-107">Před povolením berte prosím na vědomí, že doporučení produktů jsou podporována pouze u zákazníků Commerce, kteří migrovali své úložiště pomocí Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="7d9f3-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="7d9f3-108">Postup při povolení ADLS naleznete v tématu [Jak povolit ADLS v prostředí Dynamics 365](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7d9f3-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="7d9f3-109">Dále zkontrolujte, zda byly povoleny ukazatele RetailSale.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="7d9f3-110">Další informace o tomto procesu nastavení naleznete [zde.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="7d9f3-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="7d9f3-111">Zapnutí doporučení</span><span class="sxs-lookup"><span data-stu-id="7d9f3-111">Turn on recommendations</span></span>

<span data-ttu-id="7d9f3-112">Chcete-li zapnout doporučení produktu, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="7d9f3-113">Přejděte na **Retail a Commerce &gt; Doporučení produktů &gt; Parametry doporučení**.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="7d9f3-114">V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="7d9f3-115">Nastavte možnost **Povolit doporučení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Povolení doporučení produktu](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="7d9f3-117">Tento postup spustí proces generování seznamů doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="7d9f3-118">Před tím, než jsou seznamy k dispozici, může uběhnou až několik hodin. Zobrazí se na pokladním místě (POS) nebo v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="7d9f3-119">Konfigurace parametrů seznamu doporučení</span><span class="sxs-lookup"><span data-stu-id="7d9f3-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="7d9f3-120">Ve výchozím nastavení poskytují seznamy doporučení produktů na bázi AI-ML navrhované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="7d9f3-121">Výchozí navrhované hodnoty lze změnit tak, aby vyhovovaly toku vašeho podniku.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="7d9f3-122">Další informace o tom, jak změnit výchozí parametry, naleznete v části [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="7d9f3-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="7d9f3-123">Zobrazení doporučení na zařízeních POS</span><span class="sxs-lookup"><span data-stu-id="7d9f3-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="7d9f3-124">Po povolení doporučení v administrativě Commerce je nutné přidat panel doporučení na řídicí obrazovku POS pomocí nástroje pro rozložení.</span><span class="sxs-lookup"><span data-stu-id="7d9f3-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="7d9f3-125">Více o tomto procesu se dozvíte v části [Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="7d9f3-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="7d9f3-126">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="7d9f3-126">Enable personalized recommendations</span></span>

<span data-ttu-id="7d9f3-127">Další informace o získání přizpůsobených doporučení získáte v tématu [Povolení přizpůsobených doporučení produktů](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="7d9f3-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d9f3-128">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7d9f3-128">Additional resources</span></span>

[<span data-ttu-id="7d9f3-129">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="7d9f3-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="7d9f3-130">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="7d9f3-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="7d9f3-131">Přidání seznamů doporučení produktu na stránky</span><span class="sxs-lookup"><span data-stu-id="7d9f3-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="7d9f3-132">Přidání panelu doporučení do zařízení POS</span><span class="sxs-lookup"><span data-stu-id="7d9f3-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="7d9f3-133">Přehled modulu kolekce produktů</span><span class="sxs-lookup"><span data-stu-id="7d9f3-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="7d9f3-134">Povolení ADLS v prostředí Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7d9f3-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)


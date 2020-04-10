---
title: Povolit doporučení produktu
description: V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154406"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="ea6df-103">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="ea6df-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea6df-104">V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ea6df-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="ea6df-105">Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ea6df-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="ea6df-106">Předběžná kontrola doporučení</span><span class="sxs-lookup"><span data-stu-id="ea6df-106">Recommendations pre-check</span></span>

<span data-ttu-id="ea6df-107">Před povolením berte prosím na vědomí, že doporučení produktů jsou podporována pouze u zákazníků Commerce, kteří migrovali své úložiště pomocí Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="ea6df-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="ea6df-108">Postup při povolení ADLS naleznete v tématu [Jak povolit ADLS v prostředí Dynamics 365](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ea6df-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="ea6df-109">Dále zkontrolujte, zda byly povoleny ukazatele RetailSale.</span><span class="sxs-lookup"><span data-stu-id="ea6df-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="ea6df-110">Další informace o tomto procesu nastavení naleznete [zde.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="ea6df-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="ea6df-111">Zapnutí doporučení</span><span class="sxs-lookup"><span data-stu-id="ea6df-111">Turn on recommendations</span></span>

<span data-ttu-id="ea6df-112">Chcete-li zapnout doporučení produktu, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="ea6df-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="ea6df-113">Přejděte na **Retail a Commerce &gt; Doporučení produktů &gt; Parametry doporučení**.</span><span class="sxs-lookup"><span data-stu-id="ea6df-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="ea6df-114">V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.</span><span class="sxs-lookup"><span data-stu-id="ea6df-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="ea6df-115">Nastavte možnost **Povolit doporučení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ea6df-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![Povolení doporučení produktu](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="ea6df-117">Tento postup spustí proces generování seznamů doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="ea6df-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="ea6df-118">Před tím, než jsou seznamy k dispozici, může uběhnou až několik hodin. Zobrazí se na pokladním místě (POS) nebo v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ea6df-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="ea6df-119">Konfigurace parametrů seznamu doporučení</span><span class="sxs-lookup"><span data-stu-id="ea6df-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="ea6df-120">Ve výchozím nastavení poskytují seznamy doporučení produktů na bázi AI-ML navrhované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="ea6df-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="ea6df-121">Výchozí navrhované hodnoty lze změnit tak, aby vyhovovaly toku vašeho podniku.</span><span class="sxs-lookup"><span data-stu-id="ea6df-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="ea6df-122">Další informace o tom, jak změnit výchozí parametry, naleznete v části [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="ea6df-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="ea6df-123">Zobrazení doporučení na zařízeních POS</span><span class="sxs-lookup"><span data-stu-id="ea6df-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="ea6df-124">Po povolení doporučení v administrativě Commerce je nutné přidat panel doporučení na řídicí obrazovku POS pomocí nástroje pro rozložení.</span><span class="sxs-lookup"><span data-stu-id="ea6df-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="ea6df-125">Více o tomto procesu se dozvíte v části [Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="ea6df-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="ea6df-126">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="ea6df-126">Enable personalized recommendations</span></span>

<span data-ttu-id="ea6df-127">Další informace o získání přizpůsobených doporučení získáte v tématu [Povolení přizpůsobených doporučení produktů](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ea6df-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea6df-128">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="ea6df-128">Additional resources</span></span>

[<span data-ttu-id="ea6df-129">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="ea6df-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ea6df-130">Povolení ADLS v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ea6df-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ea6df-131">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="ea6df-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ea6df-132">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="ea6df-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ea6df-133">Přidat doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="ea6df-133">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ea6df-134">Přidání doporučení na obrazovku transakce</span><span class="sxs-lookup"><span data-stu-id="ea6df-134">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ea6df-135">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="ea6df-135">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ea6df-136">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="ea6df-136">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ea6df-137">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="ea6df-137">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ea6df-138">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="ea6df-138">Product recommendations FAQ</span></span>](faq-recommendations.md)


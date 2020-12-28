---
title: Povolit doporučení produktu
description: V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
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
ms.openlocfilehash: b201e5481cfaf5bb6cd64a89cdb6b5a91f31447f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410666"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="09bfd-103">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="09bfd-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09bfd-104">V tomto tématu je vysvětleno, jak vytvořit doporučení produktu založená na strojovém učení na základě umělé inteligence (AI-ML) pro zákazníky Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="09bfd-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="09bfd-105">Další informace o seznamech doporučených produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="09bfd-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="09bfd-106">Předběžná kontrola doporučení</span><span class="sxs-lookup"><span data-stu-id="09bfd-106">Recommendations pre-check</span></span>

<span data-ttu-id="09bfd-107">Před povolením berte na vědomí, že doporučení produktů jsou podporována pouze u zákazníků Commerce, kteří migrovali své úložiště pomocí Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="09bfd-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="09bfd-108">Před povolením doporučení musí být v administravě povoleny následující konfigurace:</span><span class="sxs-lookup"><span data-stu-id="09bfd-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="09bfd-109">Ujistěte se, že Azure Data Lake Storage bylo zakoupeno a úspěšně ověřeno v prostředí.</span><span class="sxs-lookup"><span data-stu-id="09bfd-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="09bfd-110">Další informace naleznete v tématu [Ujistěte se, že Azure Data Lake Storage bylo zakoupeno a úspěšně ověřeno v prostředí](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="09bfd-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="09bfd-111">Zkontrolujte, zda byla aktualizace úložiště entity automatizovaná.</span><span class="sxs-lookup"><span data-stu-id="09bfd-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="09bfd-112">Další informace naleznete v tématu [Zajistěte, aby aktualizace úložiště entity byla automatizovaná](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="09bfd-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="09bfd-113">Potvrďte, že konfigurace identity Azure AD obsahuje záznam pro doporučení.</span><span class="sxs-lookup"><span data-stu-id="09bfd-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="09bfd-114">Další informace o tom, jak provést tuto akci, je následující.</span><span class="sxs-lookup"><span data-stu-id="09bfd-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="09bfd-115">Dále zkontrolujte, zda byly povoleny ukazatele RetailSale.</span><span class="sxs-lookup"><span data-stu-id="09bfd-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="09bfd-116">Další informace o tomto nastavení procesu naleznete v tématu [Práce s opatřeními](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="09bfd-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="09bfd-117">Konfigurace identity Azure AD</span><span class="sxs-lookup"><span data-stu-id="09bfd-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="09bfd-118">Tento krok je vyžadován pro všechny zákazníky, kteří provozují infrastrukturu jako konfiguraci služby (IaaS).</span><span class="sxs-lookup"><span data-stu-id="09bfd-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="09bfd-119">U zákazníků, kteří provozují prostředky v rámci služby (SF), by tento krok měl být automaticky a doporučujeme ověřit, zda je nastavení nakonfigurováno očekávaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="09bfd-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="09bfd-120">Nastavení</span><span class="sxs-lookup"><span data-stu-id="09bfd-120">Setup</span></span>

1. <span data-ttu-id="09bfd-121">V administrativě vyhledejte stránku **Aplikace Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="09bfd-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="09bfd-122">Ověřte, zda existuje položka pro "RecommendationSystemApplication-1".</span><span class="sxs-lookup"><span data-stu-id="09bfd-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="09bfd-123">Pokud položka neexistuje, přidejte novou položku s následujícími informacemi:</span><span class="sxs-lookup"><span data-stu-id="09bfd-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="09bfd-124">**ID klienta** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="09bfd-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="09bfd-125">**Název** -RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="09bfd-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="09bfd-126">**ID uživatele** – RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="09bfd-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="09bfd-127">Uložit a zavřít stránku.</span><span class="sxs-lookup"><span data-stu-id="09bfd-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="09bfd-128">Zapnutí doporučení</span><span class="sxs-lookup"><span data-stu-id="09bfd-128">Turn on recommendations</span></span>

<span data-ttu-id="09bfd-129">Chcete-li zapnout doporučení produktu, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="09bfd-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="09bfd-130">V centrále Commerce vyhledejte **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="09bfd-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="09bfd-131">Volbou **Vše** zobrazíte seznam dostupných funkcí.</span><span class="sxs-lookup"><span data-stu-id="09bfd-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="09bfd-132">Do vyhledávacího pole zadejte **Doporučení**.</span><span class="sxs-lookup"><span data-stu-id="09bfd-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="09bfd-133">Vyberte funkci **Doporučení k produktu**.</span><span class="sxs-lookup"><span data-stu-id="09bfd-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="09bfd-134">V podokně vlastností **Doporučení produktů** vyberte **Ihned povolit**.</span><span class="sxs-lookup"><span data-stu-id="09bfd-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![Zapnutí doporučení](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="09bfd-136">Tento postup spustí proces generování seznamů doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="09bfd-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="09bfd-137">Mže trvat až několik hodin, než jsou seznamy k dispozici a lze je zobrazit na pokladním místě (POS) nebo v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="09bfd-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="09bfd-138">Konfigurace parametrů seznamu doporučení</span><span class="sxs-lookup"><span data-stu-id="09bfd-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="09bfd-139">Ve výchozím nastavení poskytují seznamy doporučení produktů na bázi AI-ML navrhované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="09bfd-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="09bfd-140">Výchozí navrhované hodnoty lze změnit tak, aby vyhovovaly toku vašeho podniku.</span><span class="sxs-lookup"><span data-stu-id="09bfd-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="09bfd-141">Další informace o tom, jak změnit výchozí parametry, naleznete v části [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="09bfd-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="09bfd-142">Zobrazení doporučení na zařízeních POS</span><span class="sxs-lookup"><span data-stu-id="09bfd-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="09bfd-143">Po povolení doporučení v administrativě Commerce je nutné přidat panel doporučení na řídicí obrazovku POS pomocí nástroje pro rozložení.</span><span class="sxs-lookup"><span data-stu-id="09bfd-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="09bfd-144">Více o tomto procesu se dozvíte v části [Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="09bfd-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="09bfd-145">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="09bfd-145">Enable personalized recommendations</span></span>

<span data-ttu-id="09bfd-146">V aplikaci Dynamics 365 Commerce mohou maloobchodní prodejci vytvářet přizpůsobená doporučení k produktu (označované také jako individuální nastavení).</span><span class="sxs-lookup"><span data-stu-id="09bfd-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="09bfd-147">Tímto způsobem lze přičlenit individuální doporučení do online prostředí zákazníků a na pokladním místě.</span><span class="sxs-lookup"><span data-stu-id="09bfd-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="09bfd-148">Je-li funkce přizpůsobení zapnuta, může systém přidružit nákup a informace o produktu uživatele ke generování doporučení pro jednotlivé produkty.</span><span class="sxs-lookup"><span data-stu-id="09bfd-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="09bfd-149">Další informace o přizpůsobených doporučení získáte v tématu [Povolení přizpůsobených doporučení](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="09bfd-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09bfd-150">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="09bfd-150">Additional resources</span></span>

[<span data-ttu-id="09bfd-151">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="09bfd-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="09bfd-152">Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="09bfd-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="09bfd-153">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="09bfd-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="09bfd-154">Povolit doporučení typu „podobný vzhled“</span><span class="sxs-lookup"><span data-stu-id="09bfd-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="09bfd-155">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="09bfd-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="09bfd-156">Přidat doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="09bfd-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="09bfd-157">Přidání doporučení na obrazovku transakce</span><span class="sxs-lookup"><span data-stu-id="09bfd-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="09bfd-158">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="09bfd-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="09bfd-159">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="09bfd-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="09bfd-160">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="09bfd-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="09bfd-161">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="09bfd-161">Product recommendations FAQ</span></span>](faq-recommendations.md)


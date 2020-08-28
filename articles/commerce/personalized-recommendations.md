---
title: Povolení doporučení přizpůsobeného produktu
description: V tomto tématu je popsán způsob vytváření individuálních doporučení produktu pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4103096f23e5568cc2bf64f21720c7c16d3e0cd1
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664851"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="75e5d-103">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="75e5d-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="75e5d-104">V tomto tématu je popsán způsob vytváření individuálních doporučení produktu pro zákazníky Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="75e5d-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="75e5d-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="75e5d-105">Overview</span></span>

<span data-ttu-id="75e5d-106">V aplikaci Dynamics 365 Commerce mohou maloobchodní prodejci vytvářet přizpůsobená doporučení k produktu (označované také jako individuální nastavení).</span><span class="sxs-lookup"><span data-stu-id="75e5d-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="75e5d-107">Tímto způsobem lze přičlenit individuální doporučení do online prostředí zákazníků a na pokladním místě (POS).</span><span class="sxs-lookup"><span data-stu-id="75e5d-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="75e5d-108">Je-li funkce přizpůsobení zapnuta, může systém přidružit nákup a informace o produktu uživatele ke generování doporučení pro jednotlivé produkty.</span><span class="sxs-lookup"><span data-stu-id="75e5d-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="75e5d-109">Předpoklady přizpůsobení</span><span class="sxs-lookup"><span data-stu-id="75e5d-109">Personalization prerequisites</span></span>

<span data-ttu-id="75e5d-110">Před tím, než zpřístupníte individuální doporučení produktu zákazníkům, mějte na paměti, že doporučení k produktům jsou podporována pouze pro uživatele z Commerce, kteří migrovali své úložiště do služby Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="75e5d-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="75e5d-111">Aby mohli zákazníci obdržet přizpůsobená doporučení produktů, musí maloobchodníci [zapnout doporučení produktu](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="75e5d-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="75e5d-112">Zapnete-li doporučení produktu, bude také zapnuto přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="75e5d-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="75e5d-113">Pokud však přizpůsobení vypnete, nevypnete ostatní typy doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="75e5d-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="75e5d-114">Další informace o doporučeních produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="75e5d-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="75e5d-115">Zapnutí individuálního nastavení</span><span class="sxs-lookup"><span data-stu-id="75e5d-115">Turn on personalization</span></span>

<span data-ttu-id="75e5d-116">Chcete-li zapnout přizpůsobení, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="75e5d-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="75e5d-117">Přejděte na **Maloobchod a velkoobchod \> Doporučení produktů \> Parametry doporučení**.</span><span class="sxs-lookup"><span data-stu-id="75e5d-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="75e5d-118">V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.</span><span class="sxs-lookup"><span data-stu-id="75e5d-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="75e5d-119">Nastavte možnost **Povolit přizpůsobení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="75e5d-119">Set the **Enable personalization** option to **Yes**.</span></span>

![Zapnutí individuálního nastavení](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="75e5d-121">Po zapnutí přizpůsobení se spustí proces generování seznamu doporučení pro individuální produkt.</span><span class="sxs-lookup"><span data-stu-id="75e5d-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="75e5d-122">Je možné, že tyto seznamy budou k dispozici a budou viditelné online a v POS.</span><span class="sxs-lookup"><span data-stu-id="75e5d-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="75e5d-123">Přizpůsobené seznamy</span><span class="sxs-lookup"><span data-stu-id="75e5d-123">Personalized lists</span></span>

<span data-ttu-id="75e5d-124">Služba doporučení kromě přizpůsobení stávajících seznamů generovaných počítačem umožňuje přizpůsobení možností zjišťování produktů, a to online i v POS.</span><span class="sxs-lookup"><span data-stu-id="75e5d-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="75e5d-125">Po zapnutí přizpůsobení mohou maloobchodní prodejci zobrazit přizpůsobené seznamy výběrů pro vás online nebo seznamy Doporučení pro zákazníky na terminálech POS.</span><span class="sxs-lookup"><span data-stu-id="75e5d-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="75e5d-126">Maloobchodní prodejci mohou také použít přizpůsobení pro stávající seznamy doporučení produktů a poskytovat funkce pro přístup k obecnému nařízení o ochraně osobních údajů (GDPR) pro ověřené uživatele.</span><span class="sxs-lookup"><span data-stu-id="75e5d-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="75e5d-127">Pokud vypnete přizpůsobení, vypnete také tyto funkce.</span><span class="sxs-lookup"><span data-stu-id="75e5d-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="75e5d-128">Online seznamy výběrů pro vás</span><span class="sxs-lookup"><span data-stu-id="75e5d-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="75e5d-129">Seznam výběrů pro vás je seznam strojového učení umělé inteligence (AI-ML), který ověřenému uživateli ukazuje přizpůsobený seznam navrhovaných produktů.</span><span class="sxs-lookup"><span data-stu-id="75e5d-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="75e5d-130">Tento seznam je založen na historii nákupů omnikanálu uživatele.</span><span class="sxs-lookup"><span data-stu-id="75e5d-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="75e5d-131">Přizpůsobená doporučení jsou dynamicky aktualizována, protože uživatel provádí více nákupů.</span><span class="sxs-lookup"><span data-stu-id="75e5d-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="75e5d-132">Tento typ seznamu také podporuje filtrování kategorií, takže maloobchodní prodejci mohou na základě navigačních hierarchií zobrazit přední výběry.</span><span class="sxs-lookup"><span data-stu-id="75e5d-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="75e5d-133">Dříve než může být seznam výběrů pro vás zobrazen na libovolné stránce elektronického obchodu, musí být splněny následující požadavky uživatele:</span><span class="sxs-lookup"><span data-stu-id="75e5d-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="75e5d-134">Uživatelé musí být přihlášeni.</span><span class="sxs-lookup"><span data-stu-id="75e5d-134">Users must be signed in.</span></span> <span data-ttu-id="75e5d-135">Anonymní uživatelé neuvidí přizpůsobená doporučení.</span><span class="sxs-lookup"><span data-stu-id="75e5d-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="75e5d-136">Uživatelé musí mít na svém účtu alespoň jeden nákup.</span><span class="sxs-lookup"><span data-stu-id="75e5d-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="75e5d-137">Uživatelé musí souhlasit s přijetím individuálních doporučení.</span><span class="sxs-lookup"><span data-stu-id="75e5d-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="75e5d-138">Na následujícím obrázku je znázorněn příklad seznamu výběrů pro vás na stránce online obchodu.</span><span class="sxs-lookup"><span data-stu-id="75e5d-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Seznam Online výběry pro vás](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="75e5d-140">Seznamy Doporučeno pro zákazníka v POS</span><span class="sxs-lookup"><span data-stu-id="75e5d-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="75e5d-141">Pokud maloobchodní prodejci chtějí vylepšit své zkušenosti se získáváním klientů, mohou přizpůsobit existující stránky podrobností o odběrateli přidáním kontextové části Doporučená pro zákazníka.</span><span class="sxs-lookup"><span data-stu-id="75e5d-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="75e5d-142">Na následujícím obrázku je znázorněn příklad seznamu Doporučeno pro zákazníka na terminálu POS.</span><span class="sxs-lookup"><span data-stu-id="75e5d-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Seznamy Doporučeno pro zákazníka v POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="75e5d-144">Použít přizpůsobení u existujících seznamů doporučení</span><span class="sxs-lookup"><span data-stu-id="75e5d-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="75e5d-145">Maloobchodní prodejci mohou použít přizpůsobení pro stávající seznamy doporučení, jako například nový, vytváření trendů, nejprodávanější, lidem se také líbí a často nakupované společně.</span><span class="sxs-lookup"><span data-stu-id="75e5d-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="75e5d-146">Pokud je přizpůsobení použito u existujících seznamů, položky, které byly dříve zakoupeny, jsou z těchto seznamů odebrány.</span><span class="sxs-lookup"><span data-stu-id="75e5d-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="75e5d-147">Výchozí verze existujících seznamů jsou zobrazeny pro anonymní uživatele i pro uživatele, kteří se odhlásili od příjmu přizpůsobených doporučení.</span><span class="sxs-lookup"><span data-stu-id="75e5d-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="75e5d-148">Maloobchodní prodejci proto nemusí ručně udržovat samostatné stránky.</span><span class="sxs-lookup"><span data-stu-id="75e5d-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="75e5d-149">Například přihlášený uživatel již nakoupil černé hodinky a hnědé pracovní boty, které se zobrazují v seznamu Trendy - výchozí na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="75e5d-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="75e5d-150">Z toho vyplývá, že se uživateli zobrazí nové produkty místo těchto produktů, jak je uvedeno v seznamu "trendy-přizpůsobení".</span><span class="sxs-lookup"><span data-stu-id="75e5d-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Použití individuálního nastavení](./media/applypersonalization.png)

<span data-ttu-id="75e5d-152">Chcete-li použít přizpůsobení pro existující seznam doporučení v modulu Commerce Site Builder, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="75e5d-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="75e5d-153">Otevře existující stránku konfigurátoru webu, která obsahuje modul pro shromažďování produktů.</span><span class="sxs-lookup"><span data-stu-id="75e5d-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="75e5d-154">V levém navigačním podokně vyberte modul inkasa produktu.</span><span class="sxs-lookup"><span data-stu-id="75e5d-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="75e5d-155">V pravém navigačním podokně v části **Produkty** vyberte seznam.</span><span class="sxs-lookup"><span data-stu-id="75e5d-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="75e5d-156">V dialogovém okně **Vybrat konfiguraci seznamu produktů** vyberte v části **Typ** typ seznamu.</span><span class="sxs-lookup"><span data-stu-id="75e5d-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="75e5d-157">Zaškrtněte políčko **Použít přizpůsobení** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="75e5d-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Aplikace přizpůsobení na seznam trendů](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="75e5d-159">Uložte fragment stránky, dokončete úpravy a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="75e5d-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="75e5d-160">Po publikování stránky budou přihlášeným uživatelům zobrazeny přizpůsobené seznamy trendů.</span><span class="sxs-lookup"><span data-stu-id="75e5d-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75e5d-161">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="75e5d-161">Additional resources</span></span>

[<span data-ttu-id="75e5d-162">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="75e5d-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="75e5d-163">Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="75e5d-163">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="75e5d-164">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="75e5d-164">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="75e5d-165">Povolit doporučení typu „podobný vzhled“</span><span class="sxs-lookup"><span data-stu-id="75e5d-165">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="75e5d-166">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="75e5d-166">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="75e5d-167">Přidat doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="75e5d-167">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="75e5d-168">Přidání doporučení na obrazovku transakce</span><span class="sxs-lookup"><span data-stu-id="75e5d-168">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="75e5d-169">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="75e5d-169">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="75e5d-170">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="75e5d-170">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="75e5d-171">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="75e5d-171">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="75e5d-172">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="75e5d-172">Product recommendations FAQ</span></span>](faq-recommendations.md)

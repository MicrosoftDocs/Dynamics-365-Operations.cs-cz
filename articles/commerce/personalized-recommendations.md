---
title: Povolení doporučení přizpůsobeného produktu
description: V tomto tématu je popsán způsob vytváření individuálních doporučení produktu pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: be460ec5ce8a9a625dc1a80f761bea9e2ab2f632
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477653"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="350d5-103">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="350d5-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="350d5-104">V tomto tématu je popsán způsob vytváření individuálních doporučení produktu pro zákazníky Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="350d5-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="350d5-105">V aplikaci Dynamics 365 Commerce mohou maloobchodní prodejci vytvářet přizpůsobená doporučení k produktu (označované také jako individuální nastavení).</span><span class="sxs-lookup"><span data-stu-id="350d5-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="350d5-106">Tímto způsobem lze přičlenit individuální doporučení do online prostředí zákazníků a na pokladním místě (POS).</span><span class="sxs-lookup"><span data-stu-id="350d5-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="350d5-107">Je-li funkce přizpůsobení zapnuta, může systém přidružit nákup a informace o produktu uživatele ke generování doporučení pro jednotlivé produkty.</span><span class="sxs-lookup"><span data-stu-id="350d5-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="350d5-108">Předpoklady přizpůsobení</span><span class="sxs-lookup"><span data-stu-id="350d5-108">Personalization prerequisites</span></span>

<span data-ttu-id="350d5-109">Před tím, než zpřístupníte individuální doporučení produktu zákazníkům, mějte na paměti, že doporučení k produktům jsou podporována pouze pro uživatele z Commerce, kteří migrovali své úložiště do služby Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="350d5-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="350d5-110">Aby mohli zákazníci obdržet přizpůsobená doporučení produktů, musí maloobchodníci [zapnout doporučení produktu](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="350d5-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="350d5-111">Zapnete-li doporučení produktu, bude také zapnuto přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="350d5-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="350d5-112">Pokud však přizpůsobení vypnete, nevypnete ostatní typy doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="350d5-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="350d5-113">Další informace o doporučeních produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="350d5-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="350d5-114">Zapnutí individuálního nastavení</span><span class="sxs-lookup"><span data-stu-id="350d5-114">Turn on personalization</span></span>

<span data-ttu-id="350d5-115">Chcete-li zapnout přizpůsobení, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="350d5-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="350d5-116">V centrále Commerce vyhledejte **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="350d5-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="350d5-117">Volbou **Vše** zobrazíte seznam dostupných funkcí.</span><span class="sxs-lookup"><span data-stu-id="350d5-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="350d5-118">Do vyhledávacího pole zadejte **Doporučení**.</span><span class="sxs-lookup"><span data-stu-id="350d5-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="350d5-119">Vyberte funkci **Přizpůsobená doporučení produktu**.</span><span class="sxs-lookup"><span data-stu-id="350d5-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="350d5-120">V podokně vlastností **Přizpůsobená doporučení produktu** vyberte **Ihned povolit**.</span><span class="sxs-lookup"><span data-stu-id="350d5-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Zapnutí individuálního nastavení](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="350d5-122">Po zapnutí přizpůsobení se spustí proces generování seznamu doporučení pro individuální produkt.</span><span class="sxs-lookup"><span data-stu-id="350d5-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="350d5-123">Je možné, že tyto seznamy budou k dispozici a budou viditelné online a v POS.</span><span class="sxs-lookup"><span data-stu-id="350d5-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="350d5-124">Přizpůsobené seznamy</span><span class="sxs-lookup"><span data-stu-id="350d5-124">Personalized lists</span></span>

<span data-ttu-id="350d5-125">Služba doporučení kromě přizpůsobení stávajících seznamů generovaných počítačem umožňuje přizpůsobení možností zjišťování produktů, a to online i v POS.</span><span class="sxs-lookup"><span data-stu-id="350d5-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="350d5-126">Po zapnutí přizpůsobení mohou maloobchodní prodejci zobrazit přizpůsobené seznamy výběrů pro vás online nebo seznamy Doporučení pro zákazníky na terminálech POS.</span><span class="sxs-lookup"><span data-stu-id="350d5-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="350d5-127">Maloobchodní prodejci mohou také použít přizpůsobení pro stávající seznamy doporučení produktů a poskytovat funkce pro přístup k obecnému nařízení o ochraně osobních údajů (GDPR) pro ověřené uživatele.</span><span class="sxs-lookup"><span data-stu-id="350d5-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="350d5-128">Pokud vypnete přizpůsobení, vypnete také tyto funkce.</span><span class="sxs-lookup"><span data-stu-id="350d5-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="350d5-129">Online seznamy výběrů pro vás</span><span class="sxs-lookup"><span data-stu-id="350d5-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="350d5-130">Seznam výběrů pro vás je seznam strojového učení umělé inteligence (AI-ML), který ověřenému uživateli ukazuje přizpůsobený seznam navrhovaných produktů.</span><span class="sxs-lookup"><span data-stu-id="350d5-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="350d5-131">Tento seznam je založen na historii nákupů omnikanálu uživatele.</span><span class="sxs-lookup"><span data-stu-id="350d5-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="350d5-132">Přizpůsobená doporučení jsou dynamicky aktualizována, protože uživatel provádí více nákupů.</span><span class="sxs-lookup"><span data-stu-id="350d5-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="350d5-133">Tento typ seznamu také podporuje filtrování kategorií, takže maloobchodní prodejci mohou na základě navigačních hierarchií zobrazit přední výběry.</span><span class="sxs-lookup"><span data-stu-id="350d5-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="350d5-134">Dříve než může být seznam výběrů pro vás zobrazen na libovolné stránce elektronického obchodu, musí být splněny následující požadavky uživatele:</span><span class="sxs-lookup"><span data-stu-id="350d5-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="350d5-135">Uživatelé musí být přihlášeni.</span><span class="sxs-lookup"><span data-stu-id="350d5-135">Users must be signed in.</span></span> <span data-ttu-id="350d5-136">Anonymní uživatelé neuvidí přizpůsobená doporučení.</span><span class="sxs-lookup"><span data-stu-id="350d5-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="350d5-137">Uživatelé musí mít na svém účtu alespoň jeden nákup.</span><span class="sxs-lookup"><span data-stu-id="350d5-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="350d5-138">Uživatelé musí souhlasit s přijetím individuálních doporučení.</span><span class="sxs-lookup"><span data-stu-id="350d5-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="350d5-139">Na následujícím obrázku je znázorněn příklad seznamu výběrů pro vás na stránce online obchodu.</span><span class="sxs-lookup"><span data-stu-id="350d5-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Seznam Online výběry pro vás](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="350d5-141">Seznamy Doporučeno pro zákazníka v POS</span><span class="sxs-lookup"><span data-stu-id="350d5-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="350d5-142">Pokud maloobchodní prodejci chtějí vylepšit své zkušenosti se získáváním klientů, mohou přizpůsobit existující stránky podrobností o odběrateli přidáním kontextové části Doporučená pro zákazníka.</span><span class="sxs-lookup"><span data-stu-id="350d5-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="350d5-143">Na následujícím obrázku je znázorněn příklad seznamu Doporučeno pro zákazníka na terminálu POS.</span><span class="sxs-lookup"><span data-stu-id="350d5-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Seznamy Doporučeno pro zákazníka v POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="350d5-145">Použít přizpůsobení u existujících seznamů doporučení</span><span class="sxs-lookup"><span data-stu-id="350d5-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="350d5-146">Maloobchodní prodejci mohou použít přizpůsobení pro stávající seznamy doporučení, jako například nový, vytváření trendů, nejprodávanější, lidem se také líbí a často nakupované společně.</span><span class="sxs-lookup"><span data-stu-id="350d5-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="350d5-147">Pokud je přizpůsobení použito u existujících seznamů, položky, které byly dříve zakoupeny, jsou z těchto seznamů odebrány.</span><span class="sxs-lookup"><span data-stu-id="350d5-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="350d5-148">Výchozí verze existujících seznamů jsou zobrazeny pro anonymní uživatele i pro uživatele, kteří se odhlásili od příjmu přizpůsobených doporučení.</span><span class="sxs-lookup"><span data-stu-id="350d5-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="350d5-149">Maloobchodní prodejci proto nemusí ručně udržovat samostatné stránky.</span><span class="sxs-lookup"><span data-stu-id="350d5-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="350d5-150">Například přihlášený uživatel již nakoupil černé hodinky a hnědé pracovní boty, které se zobrazují v seznamu Trendy - výchozí na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="350d5-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="350d5-151">Z toho vyplývá, že se uživateli zobrazí nové produkty místo těchto produktů, jak je uvedeno v seznamu "trendy-přizpůsobení".</span><span class="sxs-lookup"><span data-stu-id="350d5-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Použití individuálního nastavení](./media/applypersonalization.png)

<span data-ttu-id="350d5-153">Chcete-li použít přizpůsobení pro existující seznam doporučení v modulu Commerce Site Builder, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="350d5-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="350d5-154">Otevře existující stránku konfigurátoru webu, která obsahuje modul pro shromažďování produktů.</span><span class="sxs-lookup"><span data-stu-id="350d5-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="350d5-155">V levém navigačním podokně vyberte modul inkasa produktu.</span><span class="sxs-lookup"><span data-stu-id="350d5-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="350d5-156">V pravém navigačním podokně v části **Produkty** vyberte seznam.</span><span class="sxs-lookup"><span data-stu-id="350d5-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="350d5-157">V dialogovém okně **Vybrat konfiguraci seznamu produktů** vyberte v části **Typ** typ seznamu.</span><span class="sxs-lookup"><span data-stu-id="350d5-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="350d5-158">Zaškrtněte políčko **Použít přizpůsobení** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="350d5-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Aplikace přizpůsobení na seznam trendů](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="350d5-160">Uložte fragment stránky, dokončete úpravy a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="350d5-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="350d5-161">Po publikování stránky budou přihlášeným uživatelům zobrazeny přizpůsobené seznamy trendů.</span><span class="sxs-lookup"><span data-stu-id="350d5-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="350d5-162">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="350d5-162">Additional resources</span></span>

[<span data-ttu-id="350d5-163">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="350d5-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="350d5-164">Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="350d5-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="350d5-165">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="350d5-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="350d5-166">Povolit doporučení typu „podobný vzhled“</span><span class="sxs-lookup"><span data-stu-id="350d5-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="350d5-167">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="350d5-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="350d5-168">Přidat doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="350d5-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="350d5-169">Přidání doporučení na obrazovku transakce</span><span class="sxs-lookup"><span data-stu-id="350d5-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="350d5-170">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="350d5-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="350d5-171">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="350d5-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="350d5-172">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="350d5-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="350d5-173">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="350d5-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

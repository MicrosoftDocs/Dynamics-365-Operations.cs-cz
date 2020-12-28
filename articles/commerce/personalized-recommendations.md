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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a61ef0720839d371701f2f0a1fdec7e85a5feb7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410754"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="f644a-103">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="f644a-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f644a-104">V tomto tématu je popsán způsob vytváření individuálních doporučení produktu pro zákazníky Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f644a-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f644a-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="f644a-105">Overview</span></span>

<span data-ttu-id="f644a-106">V aplikaci Dynamics 365 Commerce mohou maloobchodní prodejci vytvářet přizpůsobená doporučení k produktu (označované také jako individuální nastavení).</span><span class="sxs-lookup"><span data-stu-id="f644a-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="f644a-107">Tímto způsobem lze přičlenit individuální doporučení do online prostředí zákazníků a na pokladním místě (POS).</span><span class="sxs-lookup"><span data-stu-id="f644a-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="f644a-108">Je-li funkce přizpůsobení zapnuta, může systém přidružit nákup a informace o produktu uživatele ke generování doporučení pro jednotlivé produkty.</span><span class="sxs-lookup"><span data-stu-id="f644a-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="f644a-109">Předpoklady přizpůsobení</span><span class="sxs-lookup"><span data-stu-id="f644a-109">Personalization prerequisites</span></span>

<span data-ttu-id="f644a-110">Před tím, než zpřístupníte individuální doporučení produktu zákazníkům, mějte na paměti, že doporučení k produktům jsou podporována pouze pro uživatele z Commerce, kteří migrovali své úložiště do služby Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f644a-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="f644a-111">Aby mohli zákazníci obdržet přizpůsobená doporučení produktů, musí maloobchodníci [zapnout doporučení produktu](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="f644a-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f644a-112">Zapnete-li doporučení produktu, bude také zapnuto přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="f644a-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="f644a-113">Pokud však přizpůsobení vypnete, nevypnete ostatní typy doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="f644a-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="f644a-114">Další informace o doporučeních produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="f644a-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="f644a-115">Zapnutí individuálního nastavení</span><span class="sxs-lookup"><span data-stu-id="f644a-115">Turn on personalization</span></span>

<span data-ttu-id="f644a-116">Chcete-li zapnout přizpůsobení, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="f644a-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="f644a-117">V centrále Commerce vyhledejte **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="f644a-117">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="f644a-118">Volbou **Vše** zobrazíte seznam dostupných funkcí.</span><span class="sxs-lookup"><span data-stu-id="f644a-118">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="f644a-119">Do vyhledávacího pole zadejte **Doporučení**.</span><span class="sxs-lookup"><span data-stu-id="f644a-119">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="f644a-120">Vyberte funkci **Přizpůsobená doporučení produktu**.</span><span class="sxs-lookup"><span data-stu-id="f644a-120">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="f644a-121">V podokně vlastností **Přizpůsobená doporučení produktu** vyberte **Ihned povolit**.</span><span class="sxs-lookup"><span data-stu-id="f644a-121">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Zapnutí individuálního nastavení](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="f644a-123">Po zapnutí přizpůsobení se spustí proces generování seznamu doporučení pro individuální produkt.</span><span class="sxs-lookup"><span data-stu-id="f644a-123">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="f644a-124">Je možné, že tyto seznamy budou k dispozici a budou viditelné online a v POS.</span><span class="sxs-lookup"><span data-stu-id="f644a-124">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="f644a-125">Přizpůsobené seznamy</span><span class="sxs-lookup"><span data-stu-id="f644a-125">Personalized lists</span></span>

<span data-ttu-id="f644a-126">Služba doporučení kromě přizpůsobení stávajících seznamů generovaných počítačem umožňuje přizpůsobení možností zjišťování produktů, a to online i v POS.</span><span class="sxs-lookup"><span data-stu-id="f644a-126">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="f644a-127">Po zapnutí přizpůsobení mohou maloobchodní prodejci zobrazit přizpůsobené seznamy výběrů pro vás online nebo seznamy Doporučení pro zákazníky na terminálech POS.</span><span class="sxs-lookup"><span data-stu-id="f644a-127">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="f644a-128">Maloobchodní prodejci mohou také použít přizpůsobení pro stávající seznamy doporučení produktů a poskytovat funkce pro přístup k obecnému nařízení o ochraně osobních údajů (GDPR) pro ověřené uživatele.</span><span class="sxs-lookup"><span data-stu-id="f644a-128">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="f644a-129">Pokud vypnete přizpůsobení, vypnete také tyto funkce.</span><span class="sxs-lookup"><span data-stu-id="f644a-129">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="f644a-130">Online seznamy výběrů pro vás</span><span class="sxs-lookup"><span data-stu-id="f644a-130">Online "Picks for you" lists</span></span>

<span data-ttu-id="f644a-131">Seznam výběrů pro vás je seznam strojového učení umělé inteligence (AI-ML), který ověřenému uživateli ukazuje přizpůsobený seznam navrhovaných produktů.</span><span class="sxs-lookup"><span data-stu-id="f644a-131">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="f644a-132">Tento seznam je založen na historii nákupů omnikanálu uživatele.</span><span class="sxs-lookup"><span data-stu-id="f644a-132">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="f644a-133">Přizpůsobená doporučení jsou dynamicky aktualizována, protože uživatel provádí více nákupů.</span><span class="sxs-lookup"><span data-stu-id="f644a-133">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="f644a-134">Tento typ seznamu také podporuje filtrování kategorií, takže maloobchodní prodejci mohou na základě navigačních hierarchií zobrazit přední výběry.</span><span class="sxs-lookup"><span data-stu-id="f644a-134">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="f644a-135">Dříve než může být seznam výběrů pro vás zobrazen na libovolné stránce elektronického obchodu, musí být splněny následující požadavky uživatele:</span><span class="sxs-lookup"><span data-stu-id="f644a-135">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="f644a-136">Uživatelé musí být přihlášeni.</span><span class="sxs-lookup"><span data-stu-id="f644a-136">Users must be signed in.</span></span> <span data-ttu-id="f644a-137">Anonymní uživatelé neuvidí přizpůsobená doporučení.</span><span class="sxs-lookup"><span data-stu-id="f644a-137">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="f644a-138">Uživatelé musí mít na svém účtu alespoň jeden nákup.</span><span class="sxs-lookup"><span data-stu-id="f644a-138">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="f644a-139">Uživatelé musí souhlasit s přijetím individuálních doporučení.</span><span class="sxs-lookup"><span data-stu-id="f644a-139">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="f644a-140">Na následujícím obrázku je znázorněn příklad seznamu výběrů pro vás na stránce online obchodu.</span><span class="sxs-lookup"><span data-stu-id="f644a-140">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Seznam Online výběry pro vás](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="f644a-142">Seznamy Doporučeno pro zákazníka v POS</span><span class="sxs-lookup"><span data-stu-id="f644a-142">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="f644a-143">Pokud maloobchodní prodejci chtějí vylepšit své zkušenosti se získáváním klientů, mohou přizpůsobit existující stránky podrobností o odběrateli přidáním kontextové části Doporučená pro zákazníka.</span><span class="sxs-lookup"><span data-stu-id="f644a-143">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="f644a-144">Na následujícím obrázku je znázorněn příklad seznamu Doporučeno pro zákazníka na terminálu POS.</span><span class="sxs-lookup"><span data-stu-id="f644a-144">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Seznamy Doporučeno pro zákazníka v POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="f644a-146">Použít přizpůsobení u existujících seznamů doporučení</span><span class="sxs-lookup"><span data-stu-id="f644a-146">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="f644a-147">Maloobchodní prodejci mohou použít přizpůsobení pro stávající seznamy doporučení, jako například nový, vytváření trendů, nejprodávanější, lidem se také líbí a často nakupované společně.</span><span class="sxs-lookup"><span data-stu-id="f644a-147">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="f644a-148">Pokud je přizpůsobení použito u existujících seznamů, položky, které byly dříve zakoupeny, jsou z těchto seznamů odebrány.</span><span class="sxs-lookup"><span data-stu-id="f644a-148">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="f644a-149">Výchozí verze existujících seznamů jsou zobrazeny pro anonymní uživatele i pro uživatele, kteří se odhlásili od příjmu přizpůsobených doporučení.</span><span class="sxs-lookup"><span data-stu-id="f644a-149">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="f644a-150">Maloobchodní prodejci proto nemusí ručně udržovat samostatné stránky.</span><span class="sxs-lookup"><span data-stu-id="f644a-150">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="f644a-151">Například přihlášený uživatel již nakoupil černé hodinky a hnědé pracovní boty, které se zobrazují v seznamu Trendy - výchozí na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="f644a-151">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="f644a-152">Z toho vyplývá, že se uživateli zobrazí nové produkty místo těchto produktů, jak je uvedeno v seznamu "trendy-přizpůsobení".</span><span class="sxs-lookup"><span data-stu-id="f644a-152">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Použití individuálního nastavení](./media/applypersonalization.png)

<span data-ttu-id="f644a-154">Chcete-li použít přizpůsobení pro existující seznam doporučení v modulu Commerce Site Builder, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="f644a-154">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f644a-155">Otevře existující stránku konfigurátoru webu, která obsahuje modul pro shromažďování produktů.</span><span class="sxs-lookup"><span data-stu-id="f644a-155">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="f644a-156">V levém navigačním podokně vyberte modul inkasa produktu.</span><span class="sxs-lookup"><span data-stu-id="f644a-156">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="f644a-157">V pravém navigačním podokně v části **Produkty** vyberte seznam.</span><span class="sxs-lookup"><span data-stu-id="f644a-157">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="f644a-158">V dialogovém okně **Vybrat konfiguraci seznamu produktů** vyberte v části **Typ** typ seznamu.</span><span class="sxs-lookup"><span data-stu-id="f644a-158">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="f644a-159">Zaškrtněte políčko **Použít přizpůsobení** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f644a-159">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Aplikace přizpůsobení na seznam trendů](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="f644a-161">Uložte fragment stránky, dokončete úpravy a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="f644a-161">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="f644a-162">Po publikování stránky budou přihlášeným uživatelům zobrazeny přizpůsobené seznamy trendů.</span><span class="sxs-lookup"><span data-stu-id="f644a-162">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f644a-163">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f644a-163">Additional resources</span></span>

[<span data-ttu-id="f644a-164">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="f644a-164">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="f644a-165">Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f644a-165">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="f644a-166">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="f644a-166">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="f644a-167">Povolit doporučení typu „podobný vzhled“</span><span class="sxs-lookup"><span data-stu-id="f644a-167">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="f644a-168">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="f644a-168">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="f644a-169">Přidat doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="f644a-169">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="f644a-170">Přidání doporučení na obrazovku transakce</span><span class="sxs-lookup"><span data-stu-id="f644a-170">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="f644a-171">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="f644a-171">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="f644a-172">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="f644a-172">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="f644a-173">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="f644a-173">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="f644a-174">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="f644a-174">Product recommendations FAQ</span></span>](faq-recommendations.md)

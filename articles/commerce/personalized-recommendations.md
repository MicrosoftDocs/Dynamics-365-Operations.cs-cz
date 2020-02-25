---
title: Povolení doporučení přizpůsobeného produktu
description: V tomto tématu je popsán způsob vytváření individuálních doporučení produktu pro zákazníky Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
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
ms.openlocfilehash: 6b3c6140b8bd3ea15458223c0f61810421d0b2bc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025232"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="69433-103">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="69433-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="69433-104">V tomto tématu je popsán způsob vytváření individuálních doporučení produktu pro zákazníky Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="69433-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="69433-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="69433-105">Overview</span></span>

<span data-ttu-id="69433-106">V aplikaci Dynamics 365 Commerce mohou maloobchodní prodejci vytvářet přizpůsobená doporučení k produktu (označované také jako individuální nastavení).</span><span class="sxs-lookup"><span data-stu-id="69433-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="69433-107">Tímto způsobem lze přičlenit individuální doporučení do online prostředí zákazníků a na pokladním místě (POS).</span><span class="sxs-lookup"><span data-stu-id="69433-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="69433-108">Je-li funkce přizpůsobení zapnuta, může systém přidružit nákup a informace o produktu uživatele ke generování doporučení pro jednotlivé produkty.</span><span class="sxs-lookup"><span data-stu-id="69433-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="69433-109">Předpoklady přizpůsobení</span><span class="sxs-lookup"><span data-stu-id="69433-109">Personalization prerequisites</span></span>

<span data-ttu-id="69433-110">Před tím, než zpřístupníte individuální doporučení produktu zákazníkům, mějte na paměti, že doporučení k produktům jsou podporována pouze pro uživatele z Commerce, kteří migrovali své úložiště do služby Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="69433-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="69433-111">Aby mohli zákazníci obdržet přizpůsobená doporučení produktů, musí maloobchodníci [zapnout doporučení produktu](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="69433-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="69433-112">Zapnete-li doporučení produktu, bude také zapnuto přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="69433-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="69433-113">Pokud však přizpůsobení vypnete, nevypnete ostatní typy doporučení produktů.</span><span class="sxs-lookup"><span data-stu-id="69433-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="69433-114">Další informace o doporučeních produktů naleznete v tématu [Přehled doporučení produktu](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="69433-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="69433-115">Zapnutí individuálního nastavení</span><span class="sxs-lookup"><span data-stu-id="69433-115">Turn on personalization</span></span>

<span data-ttu-id="69433-116">Chcete-li zapnout přizpůsobení, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="69433-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="69433-117">Přejděte na **Maloobchod a velkoobchod \> Doporučení produktů \> Parametry doporučení**.</span><span class="sxs-lookup"><span data-stu-id="69433-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="69433-118">V seznamu sdílených parametrů maloobchodního prodeje vyberte **Seznamy doporučení**.</span><span class="sxs-lookup"><span data-stu-id="69433-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="69433-119">Nastavte možnost **Povolit přizpůsobení** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="69433-119">Set the **Enable personalization** option to **Yes**.</span></span>

![Zapnutí individuálního nastavení](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="69433-121">Po zapnutí přizpůsobení se spustí proces generování seznamu doporučení pro individuální produkt.</span><span class="sxs-lookup"><span data-stu-id="69433-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="69433-122">Je možné, že tyto seznamy budou k dispozici a budou viditelné online a v POS.</span><span class="sxs-lookup"><span data-stu-id="69433-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="69433-123">Přizpůsobené seznamy</span><span class="sxs-lookup"><span data-stu-id="69433-123">Personalized lists</span></span>

<span data-ttu-id="69433-124">Služba doporučení kromě přizpůsobení stávajících seznamů generovaných počítačem umožňuje přizpůsobení možností zjišťování produktů, a to online i v POS.</span><span class="sxs-lookup"><span data-stu-id="69433-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="69433-125">Po zapnutí přizpůsobení mohou maloobchodní prodejci zobrazit přizpůsobené seznamy výběrů pro vás online nebo seznamy Doporučení pro zákazníky na terminálech POS.</span><span class="sxs-lookup"><span data-stu-id="69433-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="69433-126">Maloobchodní prodejci mohou také použít přizpůsobení pro stávající seznamy doporučení produktů a poskytovat funkce pro přístup k obecnému nařízení o ochraně osobních údajů (GDPR) pro ověřené uživatele.</span><span class="sxs-lookup"><span data-stu-id="69433-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="69433-127">Pokud vypnete přizpůsobení, vypnete také tyto funkce.</span><span class="sxs-lookup"><span data-stu-id="69433-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="69433-128">Online seznamy výběrů pro vás</span><span class="sxs-lookup"><span data-stu-id="69433-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="69433-129">Seznam výběrů pro vás je seznam strojového učení umělé inteligence (AI-ML), který ověřenému uživateli ukazuje přizpůsobený seznam navrhovaných produktů.</span><span class="sxs-lookup"><span data-stu-id="69433-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="69433-130">Tento seznam je založen na historii nákupů omnikanálu uživatele.</span><span class="sxs-lookup"><span data-stu-id="69433-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="69433-131">Přizpůsobená doporučení jsou dynamicky aktualizována, protože uživatel provádí více nákupů.</span><span class="sxs-lookup"><span data-stu-id="69433-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="69433-132">Tento typ seznamu také podporuje filtrování kategorií, takže maloobchodní prodejci mohou na základě navigačních hierarchií zobrazit přední výběry.</span><span class="sxs-lookup"><span data-stu-id="69433-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="69433-133">Dříve než může být seznam výběrů pro vás zobrazen na libovolné stránce elektronického obchodu, musí být splněny následující požadavky uživatele:</span><span class="sxs-lookup"><span data-stu-id="69433-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="69433-134">Uživatelé musí být přihlášeni.</span><span class="sxs-lookup"><span data-stu-id="69433-134">Users must be signed in.</span></span> <span data-ttu-id="69433-135">Anonymní uživatelé neuvidí přizpůsobená doporučení.</span><span class="sxs-lookup"><span data-stu-id="69433-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="69433-136">Uživatelé musí mít na svém účtu alespoň jeden nákup.</span><span class="sxs-lookup"><span data-stu-id="69433-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="69433-137">Uživatelé musí souhlasit s přijetím individuálních doporučení.</span><span class="sxs-lookup"><span data-stu-id="69433-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="69433-138">Na následujícím obrázku je znázorněn příklad seznamu výběrů pro vás na stránce online obchodu.</span><span class="sxs-lookup"><span data-stu-id="69433-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Seznam Online výběry pro vás](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="69433-140">Seznamy Doporučeno pro zákazníka v POS</span><span class="sxs-lookup"><span data-stu-id="69433-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="69433-141">Pokud maloobchodní prodejci chtějí vylepšit své zkušenosti se získáváním klientů, mohou přizpůsobit existující stránky podrobností o odběrateli přidáním kontextové části Doporučená pro zákazníka.</span><span class="sxs-lookup"><span data-stu-id="69433-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="69433-142">Na následujícím obrázku je znázorněn příklad seznamu Doporučeno pro zákazníka na terminálu POS.</span><span class="sxs-lookup"><span data-stu-id="69433-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Seznamy Doporučeno pro zákazníka v POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="69433-144">Použít přizpůsobení u existujících seznamů doporučení</span><span class="sxs-lookup"><span data-stu-id="69433-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="69433-145">Maloobchodní prodejci mohou použít přizpůsobení pro stávající seznamy doporučení, jako například nový, vytváření trendů, nejprodávanější, lidem se také líbí a často nakupované společně.</span><span class="sxs-lookup"><span data-stu-id="69433-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="69433-146">Pokud je přizpůsobení použito u existujících seznamů, položky, které byly dříve zakoupeny, jsou z těchto seznamů odebrány.</span><span class="sxs-lookup"><span data-stu-id="69433-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="69433-147">Výchozí verze existujících seznamů jsou zobrazeny pro anonymní uživatele i pro uživatele, kteří se odhlásili od příjmu přizpůsobených doporučení.</span><span class="sxs-lookup"><span data-stu-id="69433-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="69433-148">Maloobchodní prodejci proto nemusí ručně udržovat samostatné stránky.</span><span class="sxs-lookup"><span data-stu-id="69433-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="69433-149">Například přihlášený uživatel již nakoupil černé hodinky a hnědé pracovní boty, které se zobrazují v seznamu Trendy - výchozí na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="69433-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="69433-150">Z toho vyplývá, že se uživateli zobrazí nové produkty místo těchto produktů, jak je uvedeno v seznamu "trendy-přizpůsobení".</span><span class="sxs-lookup"><span data-stu-id="69433-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Použití individuálního nastavení](./media/applypersonalization.png)

<span data-ttu-id="69433-152">Chcete-li použít přizpůsobení pro existující seznam doporučení v modulu Commerce Site Builder, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="69433-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="69433-153">Otevře existující stránku konfigurátoru webu, která obsahuje modul pro shromažďování produktů.</span><span class="sxs-lookup"><span data-stu-id="69433-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="69433-154">V levém navigačním podokně vyberte modul inkasa produktu.</span><span class="sxs-lookup"><span data-stu-id="69433-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="69433-155">V pravém navigačním podokně v části **Produkty** vyberte seznam.</span><span class="sxs-lookup"><span data-stu-id="69433-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="69433-156">V dialogovém okně **Vybrat konfiguraci seznamu produktů** vyberte v části **Typ** typ seznamu.</span><span class="sxs-lookup"><span data-stu-id="69433-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="69433-157">Zaškrtněte políčko **Použít přizpůsobení** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="69433-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Aplikace přizpůsobení na seznam trendů](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="69433-159">Uložte fragment stránky, dokončete úpravy a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="69433-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="69433-160">Po publikování stránky budou přihlášeným uživatelům zobrazeny přizpůsobené seznamy trendů.</span><span class="sxs-lookup"><span data-stu-id="69433-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69433-161">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="69433-161">Additional resources</span></span>

[<span data-ttu-id="69433-162">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="69433-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="69433-163">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="69433-163">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="69433-164">GDPR a doporučení produktů</span><span class="sxs-lookup"><span data-stu-id="69433-164">GDPR and product recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="69433-165">Přidání seznamů doporučení produktu na stránky</span><span class="sxs-lookup"><span data-stu-id="69433-165">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="69433-166">Přidání panelu doporučení do zařízení POS</span><span class="sxs-lookup"><span data-stu-id="69433-166">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="69433-167">Přehled modulu kolekce produktů</span><span class="sxs-lookup"><span data-stu-id="69433-167">Product collection module overview</span></span>](product-collection-module-overview.md)

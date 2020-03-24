---
title: Odhlášení přizpůsobených doporučení
description: V tomto tématu je vysvětleno, jak můžete zákazníkům vymezit přijetí individuálních doporučení v Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: a6d2388e863135c2b6d51af915b606a56f0603a8
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127737"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="87a3f-103">Odhlášení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="87a3f-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="87a3f-104">V tomto tématu je vysvětleno, jak můžete zákazníkům vymezit přijetí individuálních doporučení v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="87a3f-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="87a3f-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="87a3f-105">Overview</span></span>

<span data-ttu-id="87a3f-106">Při vytváření účtu jsou noví zákazníci automaticky nastaveni na příjem individuálních doporučení.</span><span class="sxs-lookup"><span data-stu-id="87a3f-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="87a3f-107">Aplikace Dynamics 365 Commerce však poskytuje různé způsoby, jak mohou maloobchodní prodejci nechat uživatele odhlásit se z příjmu těchto doporučení a omezili zpracování jejich osobních údajů.</span><span class="sxs-lookup"><span data-stu-id="87a3f-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="87a3f-108">Ověření uživatelé, kteří se odhlašují od individuálních doporučení, okamžitě zastaví zobrazování přizpůsobených seznamů.</span><span class="sxs-lookup"><span data-stu-id="87a3f-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="87a3f-109">Kromě toho budou z modelů individuálních doporučení odebrány všechny osobní údaje získané pro individuální nastavení.</span><span class="sxs-lookup"><span data-stu-id="87a3f-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="87a3f-110">Další informace o povolení přizpůsobených doporučení produktů získáte v tématu [Povolení přizpůsobených doporučení produktů](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="87a3f-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="87a3f-111">Způsoby, jak maloobchodní prodejci mohou uplatnit možnost odhlášení</span><span class="sxs-lookup"><span data-stu-id="87a3f-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="87a3f-112">Maloobchodní prodejci mají tři možnosti, jak uplatnit možnost odhlášení.</span><span class="sxs-lookup"><span data-stu-id="87a3f-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="87a3f-113">Odhlášení jménem uživatelů</span><span class="sxs-lookup"><span data-stu-id="87a3f-113">Opting out on behalf of users</span></span>

<span data-ttu-id="87a3f-114">V modulu Správa účtu v obchodu v administrativě aplikace Commerce se maloobchodníci mohou odhlašovat jménem uživatelů.</span><span class="sxs-lookup"><span data-stu-id="87a3f-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="87a3f-115">Na administrativní domovské stránce hledejte **Všichni zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="87a3f-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="87a3f-116">Vyhledejte a vyberte zákazníka a pak vyberte pevnou záložku **maloobchod**.</span><span class="sxs-lookup"><span data-stu-id="87a3f-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Pevná záložka maloobchod](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="87a3f-118">V části **Ochrana osobních údajů** nastavte možnost **Zakázat individuální nastavení** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="87a3f-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Nastavení ochrany osobních údajů](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="87a3f-120">Zvolte **Uložit** a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="87a3f-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="87a3f-121">Použití funkce odhlášení na základě modulu</span><span class="sxs-lookup"><span data-stu-id="87a3f-121">Module-based opt-out experience</span></span>

<span data-ttu-id="87a3f-122">Maloobchodní prodejci mohou sami umožnit ověřeným uživatelům odhlašovat individuální doporučení.</span><span class="sxs-lookup"><span data-stu-id="87a3f-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="87a3f-123">Chcete-li tyto možnosti odhlášení poskytnout, přidejte do stránek profilu účtu odběratele modul odhlášení uživatele.</span><span class="sxs-lookup"><span data-stu-id="87a3f-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="87a3f-124">Vlastní rozšíření</span><span class="sxs-lookup"><span data-stu-id="87a3f-124">Custom extensions</span></span>

<span data-ttu-id="87a3f-125">Maloobchodní prodejci mohou vytvářet svá vlastní rozšíření pro správu možnosti odhlášení pro uživatele.</span><span class="sxs-lookup"><span data-stu-id="87a3f-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="87a3f-126">Další informace naleznete v tématu [Volání rozhraní API serveru](e-commerce-extensibility/call-retail-server-apis.md) a [Rozšiřitelnost online kanálu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="87a3f-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="87a3f-127">Získejte digitální kopii přizpůsobených údajů doporučení jménem ověřeného uživatele</span><span class="sxs-lookup"><span data-stu-id="87a3f-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="87a3f-128">Zákazníci mohou požadovat získání digitální kopie svých osobních údajů a také zobrazit výsledky exportovaného zobrazení jejich doporučení.</span><span class="sxs-lookup"><span data-stu-id="87a3f-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="87a3f-129">Pokud si tuto informaci zákazník vyžádá, musí prodejce vytvořit přizpůsobené rozšíření, které volá rozhraní API maloobchodního serveru a dotazuje se na úplné výsledky ze seznamu **Výběry pro vás**, a to na základě ID zákazníka.</span><span class="sxs-lookup"><span data-stu-id="87a3f-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="87a3f-130">Výsledky mohou být exportovány ve formátu hodnot oddělených čárkami (CSV) a sdíleny se zákazníkem.</span><span class="sxs-lookup"><span data-stu-id="87a3f-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="87a3f-131">V následujícím příkladu je ukázáno, jak může maloobchodník provést tento úkol.</span><span class="sxs-lookup"><span data-stu-id="87a3f-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="87a3f-132">Maloobchodní prodejce vytváří vlastní rozšíření, které vybírá data osobních doporučení jménem uživatele.</span><span class="sxs-lookup"><span data-stu-id="87a3f-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="87a3f-133">Informace o tom, jak vytvářet moduly, klonovat existující moduly, volat rozhraní API maloobchodního serveru a volat akce s daty, naleznete v tématu [Rozšiřitelnost online kanálu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="87a3f-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="87a3f-134">Vlastní rozšíření uskuteční volání do klíčové akce s daty **get-recommendations** a předá do ní požadované informace na základě požadavků seznamu.</span><span class="sxs-lookup"><span data-stu-id="87a3f-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="87a3f-135">V případě seznamu **Výběr pro vás** je nutné, aby rozšíření předávalo správný název seznamu a ID odběratele k akci dat.</span><span class="sxs-lookup"><span data-stu-id="87a3f-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="87a3f-136">Jedním ze způsobů, jak vytvořit vlastní rozšíření, je klonování existujícího modulu shromažďování produktů, který slouží k vrácení výsledků doporučení.</span><span class="sxs-lookup"><span data-stu-id="87a3f-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="87a3f-137">Naklonováním tohoto existujícího modulu může maloobchodní prodejce změnit existující kód a přidat nové tlačítko, které exportuje výsledky doporučení do souboru CSV.</span><span class="sxs-lookup"><span data-stu-id="87a3f-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="87a3f-138">Další informace naleznete v tématu [klonování modulu startovní sady](e-commerce-extensibility/clone-starter-module.md) a [Moduly kolekcí produktů](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="87a3f-138">For more information, see [Clone a starter kit module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="87a3f-139">Chcete-li zobrazit úplné zobrazení knihovny rozhraní API maloobchodního serveru, naleznete informace v tématu [Rozhraní API zákazníka a spotřebitele maloobchodního serveru](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="87a3f-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="87a3f-140">Po vytvoření vlastního rozšíření může maloobchodní prodejce exportovat soubor CSV se všemi výsledky doporučení na základě jedinečného ID zákazníka ověřeného uživatele.</span><span class="sxs-lookup"><span data-stu-id="87a3f-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="87a3f-141">Maloobchodní prodejce může sdílet exportovaný soubor CSV, který obsahuje úplný osobní seznam doporučených produktů s ověřeným uživatelem.</span><span class="sxs-lookup"><span data-stu-id="87a3f-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87a3f-142">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="87a3f-142">Additional resources</span></span>

[<span data-ttu-id="87a3f-143">Přehled doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="87a3f-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="87a3f-144">Povolení ADLS v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="87a3f-144">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="87a3f-145">Povolit doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="87a3f-145">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="87a3f-146">Povolení přizpůsobených doporučení</span><span class="sxs-lookup"><span data-stu-id="87a3f-146">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="87a3f-147">Přidání seznamů doporučení na web e-Commerce</span><span class="sxs-lookup"><span data-stu-id="87a3f-147">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="87a3f-148">Přidat doporučení produktu v POS</span><span class="sxs-lookup"><span data-stu-id="87a3f-148">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="87a3f-149">Přidání doporučení na obrazovku transakce</span><span class="sxs-lookup"><span data-stu-id="87a3f-149">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="87a3f-150">Úprava výsledků doporučení AI-ML</span><span class="sxs-lookup"><span data-stu-id="87a3f-150">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="87a3f-151">Ručně vytvořit uspořádaná doporučení</span><span class="sxs-lookup"><span data-stu-id="87a3f-151">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="87a3f-152">Vytvořit doporučení s ukázkovými daty</span><span class="sxs-lookup"><span data-stu-id="87a3f-152">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="87a3f-153">Často kladené dotazy k doporučení produktu</span><span class="sxs-lookup"><span data-stu-id="87a3f-153">Product recommendations FAQ</span></span>](faq-recommendations.md)

---
title: Správa hodnocení a recenzí
description: V tomto tématu je vysvětlen způsob správy hodnocení a recenzí pomocí nástroje Microsoft Dynamics 365 Commerce pro moderování hodnocení a recenzí.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027235"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="ace8c-103">Správa hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="ace8c-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ace8c-104">V tomto tématu je vysvětlen způsob správy hodnocení a recenzí pomocí nástroje Microsoft Dynamics 365 Commerce pro moderování hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="ace8c-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="ace8c-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="ace8c-105">Overview</span></span>

<span data-ttu-id="ace8c-106">Dynamics 365 Commerce použije Microsoft Azure Cognitive Service k automatickému moderování recenzí pomocí redigování slov.</span><span class="sxs-lookup"><span data-stu-id="ace8c-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="ace8c-107">Moderátoři mohou kromě toho používat nástroj pro moderování hodnocení a recenzí pro následující ruční úkoly:</span><span class="sxs-lookup"><span data-stu-id="ace8c-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="ace8c-108">Moderování recenzí tím, že na ně odpovíte nebo je odeberete.</span><span class="sxs-lookup"><span data-stu-id="ace8c-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="ace8c-109">Odstranění recenzí zákazníka na žádost zákazníka.</span><span class="sxs-lookup"><span data-stu-id="ace8c-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="ace8c-110">Hromadný import hodnocení a recenzí pro všechny produkty do šablony Microsoft Power BI, aby bylo možné analyzovat trendy hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="ace8c-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="ace8c-111">Přístup k funkcím pro moderování hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="ace8c-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="ace8c-112">Chcete-li získat přístup k funkcím hodnocení a recenzí v nástroji Správa serverů elektronického obchodování, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ace8c-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="ace8c-113">Přihlaste se do [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="ace8c-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="ace8c-114">Otevřete projekt obsahující prostředí, ve kterém chcete provést inicializaci elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="ace8c-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="ace8c-115">V části **Prostředí** vyberte prostředí.</span><span class="sxs-lookup"><span data-stu-id="ace8c-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="ace8c-116">V části **Funkce prostředí** vyberte **Správa maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="ace8c-117">Na kartě **elektronické obchodování** v části **Odkazy** vyberte **nástroj pro správu webu služby e-commerce**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="ace8c-118">Přečíst recenzi</span><span class="sxs-lookup"><span data-stu-id="ace8c-118">Read a review</span></span> 

1. <span data-ttu-id="ace8c-119">Přejděte na **Domů \> Recenze \> Moderování**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="ace8c-120">Pomocí vyhledávacího pole v pravém horním rohu stránky můžete filtrovat recenze, které jsou zobrazeny podle ID produktu, názvu produktu nebo textu recenze.</span><span class="sxs-lookup"><span data-stu-id="ace8c-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="ace8c-121">Další filtry umožňují omezit recenze podle období, hodnocení, kanálu nebo stavu sledování (přijaté, zodpovězené nebo nahlášené).</span><span class="sxs-lookup"><span data-stu-id="ace8c-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Domovská stránka moderování](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="ace8c-123">Odpověď na recenzi</span><span class="sxs-lookup"><span data-stu-id="ace8c-123">Respond to a review</span></span> 

<span data-ttu-id="ace8c-124">V některých případech zákazníci, kteří nakoupili produkt, vyjádřili pokojenost nebo nespokojenosti, nebo neznají způsob používání produktu.</span><span class="sxs-lookup"><span data-stu-id="ace8c-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="ace8c-125">Jako moderátor můžete odeslat odpověď na recenzi.</span><span class="sxs-lookup"><span data-stu-id="ace8c-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="ace8c-126">Tato odpověď se zobrazí spolu s recenzí na webu.</span><span class="sxs-lookup"><span data-stu-id="ace8c-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="ace8c-127">Chcete-li odpovědět na recenzi, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="ace8c-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="ace8c-128">Přejděte na **Domů \> Recenze \> Moderování**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="ace8c-129">Najít a vybrat revizi, která vyžaduje odpověď.</span><span class="sxs-lookup"><span data-stu-id="ace8c-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="ace8c-130">V podokně vlastnosti vpravo vyberte možnost **přidat odpověď.**</span><span class="sxs-lookup"><span data-stu-id="ace8c-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="ace8c-131">Zadejte text odpovědi a název, který má být zobrazen pro respondenta.</span><span class="sxs-lookup"><span data-stu-id="ace8c-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="ace8c-132">Výchozí název respondenta je **Moderátor**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="ace8c-133">Po dokončení zvolte **Odeslat odpověď**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-133">When you've finished, select **Post response**.</span></span>

![Odpověď na recenzi](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="ace8c-135">Odstranění recenze</span><span class="sxs-lookup"><span data-stu-id="ace8c-135">Take down a review</span></span> 

<span data-ttu-id="ace8c-136">Někdy existuje důvod, proč moderátoři z obchodních důvodů odstraní recenze zákazníků.</span><span class="sxs-lookup"><span data-stu-id="ace8c-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="ace8c-137">Chcete-li odstranit recenzi, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="ace8c-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="ace8c-138">Přejděte na **Domů \> Recenze \> Moderování**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="ace8c-139">Vyhledejte a vyberte recenzi, kterou je třeba odstranit.</span><span class="sxs-lookup"><span data-stu-id="ace8c-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="ace8c-140">V podokně vlastnosti napravo vyberte důvod odstranění a poté vyberte možnost **odebrat**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="ace8c-141">Odstranění recenzí zákazníka na žádost zákazníka.</span><span class="sxs-lookup"><span data-stu-id="ace8c-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="ace8c-142">Někdy si zákazníci přejí, aby jejich hodnocení a recenze byly trvale smazány z webové stránky elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="ace8c-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="ace8c-143">Moderátor, který obdrží požadavek na odebrání od zákazníka, může odebrat data odběratele pomocí funkce kontroly odstranění.</span><span class="sxs-lookup"><span data-stu-id="ace8c-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="ace8c-144">Chcete-li vyhledat a odstranit data odběratele, moderátor potřebuje e-mailovou adresu, kterou odběratel používá k přihlášení a poskytnutí recenzí.</span><span class="sxs-lookup"><span data-stu-id="ace8c-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="ace8c-145">Chcete-li vyhledat a odstranit data o odběrateli, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="ace8c-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="ace8c-146">Přejděte na **Domů \> Recenze \> Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="ace8c-147">V poli **Hledat uživatele podle e-mailové adresy** zadejte e-mailovou adresu odběratele a pak vyberte **hledat**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="ace8c-148">Pokud má zákazník nějakou aktivitu týkající se recenzí (např. podání recenze, hlasování o užitečnosti recenzí jiného zákazníka nebo komentáře o recenzi jiného zákazníka), zobrazí se výsledky.</span><span class="sxs-lookup"><span data-stu-id="ace8c-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="ace8c-149">Pro každou položku existuje tlačítko **odstranit.**</span><span class="sxs-lookup"><span data-stu-id="ace8c-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="ace8c-150">Pro každou položku, kterou je třeba odstranit, vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="ace8c-151">Po zobrazení výzvy k potvrzení vyberte možnost **Ano.**</span><span class="sxs-lookup"><span data-stu-id="ace8c-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Odstranění dat zákazníků](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="ace8c-153">Může trvat až sedm dní, než budou data zcela odstraněna ze systému.</span><span class="sxs-lookup"><span data-stu-id="ace8c-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="ace8c-154">Moderátoři by měli informovat zákazníky o této prodlevě.</span><span class="sxs-lookup"><span data-stu-id="ace8c-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="ace8c-155">Pokud uživatelé změnili své jméno v nastavení účtu, může se ve výsledcích hledání zobrazit více položek.</span><span class="sxs-lookup"><span data-stu-id="ace8c-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="ace8c-156">V takovém přípdě, chcete-li data zákazníka zcela odstranit, musí moderátor pro každou položku vybrat možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="ace8c-157">Stáhnout data hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="ace8c-157">Download ratings and reviews data</span></span>

<span data-ttu-id="ace8c-158">Nástroj pro moderování hodnocení a recenzí umožňuje moderátorům importovat hodnocení a recenzovat data hromadně, aby mohli analyzovat trendy.</span><span class="sxs-lookup"><span data-stu-id="ace8c-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="ace8c-159">K dispozici je šablona Power BI, která obsahuje základní metriky.</span><span class="sxs-lookup"><span data-stu-id="ace8c-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="ace8c-160">Moderátoři mohou tuto šablonu použít k připojení hromadně importovaných dat a k zobrazení řídicího panelu.</span><span class="sxs-lookup"><span data-stu-id="ace8c-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="ace8c-161">Nemusí vytvářet vlastní řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="ace8c-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="ace8c-162">Moderátoři mohou také upravit šablonu Power BI tak, aby vyhovovala jejich specifickým potřebám.</span><span class="sxs-lookup"><span data-stu-id="ace8c-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="ace8c-163">Chcete-li stáhnout data hodnocení a recenzí, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ace8c-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="ace8c-164">Přejděte na **Domů \> Recenze \> Vykazování**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="ace8c-165">Chcete-li stáhnout data hodnocení a recenzí hromadně ve formátu hodnot oddělených čárkou (CSV), vyberte možnost **Stáhnout recenze**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="ace8c-166">Zobrazení trendů hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="ace8c-166">View ratings and reviews trends</span></span>

<span data-ttu-id="ace8c-167">Moderátoři mohou stáhnout šablonu Power BI, aby mohli sledovat trendy v řídicím panelu.</span><span class="sxs-lookup"><span data-stu-id="ace8c-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="ace8c-168">Chcete-li zobrazit trendy hodnocení a recenzí, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="ace8c-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="ace8c-169">Přejděte na **Domů \> Recenze \> Vykazování**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="ace8c-170">Vyberte **Šablonu PowerBI** ke stažení šablony.</span><span class="sxs-lookup"><span data-stu-id="ace8c-170">Select **PowerBI template** to download the template.</span></span>

    ![Stáhnutí šablony Power BI](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="ace8c-172">Otevře staženou šablonu pomocí aplikace Power BI.</span><span class="sxs-lookup"><span data-stu-id="ace8c-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="ace8c-173">Zavřete dialogové okno **Přístup k webovému obsahu**, které se zobrazí, a poté zavřete zobrazenou chybovou zprávu "Obnovit".</span><span class="sxs-lookup"><span data-stu-id="ace8c-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="ace8c-174">Přejděte na **Domovskou stránku**, vberte **Upravit dotazy** a pak vyberte **Nastavení zdroje dat**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="ace8c-175">V dialogovém okně **Nastavení zdroje dat** vyberte možnost **Změnit zdroj**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="ace8c-176">V poli **Adresa URL** zadejte cestu k datům recenzí, která jste stáhli v předchozím postupu (například **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="ace8c-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Pole Adresa URL v dialogovém okně hodnot oddělených čárkou](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="ace8c-178">Vyberte možnost **OK** a pak zvolte **Použít změny**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="ace8c-179">Použijete-li změny ve zdroji dat, bude provedena za jednu až dvě minuty.</span><span class="sxs-lookup"><span data-stu-id="ace8c-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="ace8c-180">Chcete-li zobrazit hodnocení a recenze trendů, vyberte volbu **List trendů**.</span><span class="sxs-lookup"><span data-stu-id="ace8c-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trendy hodnocení a recenzí](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="ace8c-182">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ace8c-182">Additional resources</span></span>

[<span data-ttu-id="ace8c-183">Přehled hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="ace8c-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="ace8c-184">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="ace8c-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="ace8c-185">Konfigurace hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="ace8c-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="ace8c-186">Synchronizace hodnocení produktů v Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="ace8c-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)

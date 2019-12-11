---
title: Správa hodnocení a recenzí
description: V tomto tématu je vysvětlen způsob správy hodnocení a recenzí pomocí nástroje Microsoft Dynamics 365 Commerce pro moderování hodnocení a recenzí.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698019"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="28ce9-103">Správa hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="28ce9-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="28ce9-104">V tomto tématu je vysvětlen způsob správy hodnocení a recenzí pomocí nástroje Microsoft Dynamics 365 Commerce pro moderování hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="28ce9-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="28ce9-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="28ce9-105">Overview</span></span>

<span data-ttu-id="28ce9-106">Dynamics 365 Commerce použije Microsoft Azure Cognitive Service k automatickému moderování recenzí pomocí redigování slov.</span><span class="sxs-lookup"><span data-stu-id="28ce9-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="28ce9-107">Moderátoři mohou kromě toho používat nástroj pro moderování hodnocení a recenzí pro následující ruční úkoly:</span><span class="sxs-lookup"><span data-stu-id="28ce9-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="28ce9-108">Moderování recenzí tím, že na ně odpovíte nebo je odeberete.</span><span class="sxs-lookup"><span data-stu-id="28ce9-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="28ce9-109">Odstranění recenzí zákazníka na žádost zákazníka.</span><span class="sxs-lookup"><span data-stu-id="28ce9-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="28ce9-110">Hromadný import hodnocení a recenzí pro všechny produkty do šablony Microsoft Power BI, aby bylo možné analyzovat trendy hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="28ce9-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="28ce9-111">Přečíst recenzi</span><span class="sxs-lookup"><span data-stu-id="28ce9-111">Read a review</span></span> 

1. <span data-ttu-id="28ce9-112">Přejděte na **Domů \> Recenze \> Moderování**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="28ce9-113">Pomocí vyhledávacího pole v pravém horním rohu stránky můžete filtrovat recenze, které jsou zobrazeny podle ID produktu, názvu produktu nebo textu recenze.</span><span class="sxs-lookup"><span data-stu-id="28ce9-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="28ce9-114">Další filtry umožňují omezit recenze podle období, hodnocení, kanálu nebo stavu sledování (přijaté, zodpovězené nebo nahlášené).</span><span class="sxs-lookup"><span data-stu-id="28ce9-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Domovská stránka moderování](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="28ce9-116">Odpověď na recenzi</span><span class="sxs-lookup"><span data-stu-id="28ce9-116">Respond to a review</span></span> 

<span data-ttu-id="28ce9-117">V některých případech zákazníci, kteří nakoupili produkt, vyjádřili pokojenost nebo nespokojenosti, nebo neznají způsob používání produktu.</span><span class="sxs-lookup"><span data-stu-id="28ce9-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="28ce9-118">Jako moderátor můžete odeslat odpověď na recenzi.</span><span class="sxs-lookup"><span data-stu-id="28ce9-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="28ce9-119">Tato odpověď se zobrazí spolu s recenzí na webu.</span><span class="sxs-lookup"><span data-stu-id="28ce9-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="28ce9-120">Chcete-li odpovědět na recenzi, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="28ce9-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="28ce9-121">Přejděte na **Domů \> Recenze \> Moderování**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="28ce9-122">Najít a vybrat revizi, která vyžaduje odpověď.</span><span class="sxs-lookup"><span data-stu-id="28ce9-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="28ce9-123">V podokně vlastnosti vpravo vyberte možnost **přidat odpověď.**</span><span class="sxs-lookup"><span data-stu-id="28ce9-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="28ce9-124">Zadejte text odpovědi a název, který má být zobrazen pro respondenta.</span><span class="sxs-lookup"><span data-stu-id="28ce9-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="28ce9-125">Výchozí název respondenta je **Moderátor**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="28ce9-126">Po dokončení zvolte **Odeslat odpověď**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-126">When you've finished, select **Post response**.</span></span>

![Odpověď na recenzi](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="28ce9-128">Odstranění recenze</span><span class="sxs-lookup"><span data-stu-id="28ce9-128">Take down a review</span></span> 

<span data-ttu-id="28ce9-129">Někdy existuje důvod, proč moderátoři z obchodních důvodů odstraní recenze zákazníků.</span><span class="sxs-lookup"><span data-stu-id="28ce9-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="28ce9-130">Chcete-li odstranit recenzi, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="28ce9-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="28ce9-131">Přejděte na **Domů \> Recenze \> Moderování**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="28ce9-132">Vyhledejte a vyberte recenzi, kterou je třeba odstranit.</span><span class="sxs-lookup"><span data-stu-id="28ce9-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="28ce9-133">V podokně vlastnosti napravo vyberte důvod odstranění a poté vyberte možnost **odebrat**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="28ce9-134">Odstranění recenzí zákazníka na žádost zákazníka.</span><span class="sxs-lookup"><span data-stu-id="28ce9-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="28ce9-135">Někdy si zákazníci přejí, aby jejich hodnocení a recenze byly trvale smazány z webové stránky elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="28ce9-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="28ce9-136">Moderátor, který obdrží požadavek na odebrání od zákazníka, může odebrat data odběratele pomocí funkce kontroly odstranění.</span><span class="sxs-lookup"><span data-stu-id="28ce9-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="28ce9-137">Chcete-li vyhledat a odstranit data odběratele, moderátor potřebuje e-mailovou adresu, kterou odběratel používá k přihlášení a poskytnutí recenzí.</span><span class="sxs-lookup"><span data-stu-id="28ce9-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="28ce9-138">Chcete-li vyhledat a odstranit data o odběrateli, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="28ce9-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="28ce9-139">Přejděte na **Domů \> Recenze \> Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="28ce9-140">V poli **Hledat uživatele podle e-mailové adresy** zadejte e-mailovou adresu odběratele a pak vyberte **hledat**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="28ce9-141">Pokud má zákazník nějakou aktivitu týkající se recenzí (např. podání recenze, hlasování o užitečnosti recenzí jiného zákazníka nebo komentáře o recenzi jiného zákazníka), zobrazí se výsledky.</span><span class="sxs-lookup"><span data-stu-id="28ce9-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="28ce9-142">Pro každou položku existuje tlačítko **odstranit.**</span><span class="sxs-lookup"><span data-stu-id="28ce9-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="28ce9-143">Pro každou položku, kterou je třeba odstranit, vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="28ce9-144">Po zobrazení výzvy k potvrzení vyberte možnost **Ano.**</span><span class="sxs-lookup"><span data-stu-id="28ce9-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Odstranění dat zákazníků](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="28ce9-146">Může trvat až sedm dní, než budou data zcela odstraněna ze systému.</span><span class="sxs-lookup"><span data-stu-id="28ce9-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="28ce9-147">Moderátoři by měli informovat zákazníky o této prodlevě.</span><span class="sxs-lookup"><span data-stu-id="28ce9-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="28ce9-148">Pokud uživatelé změnili své jméno v nastavení účtu, může se ve výsledcích hledání zobrazit více položek.</span><span class="sxs-lookup"><span data-stu-id="28ce9-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="28ce9-149">V takovém přípdě, chcete-li data zákazníka zcela odstranit, musí moderátor pro každou položku vybrat možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="28ce9-150">Stáhnout data hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="28ce9-150">Download ratings and reviews data</span></span>

<span data-ttu-id="28ce9-151">Nástroj pro moderování hodnocení a recenzí umožňuje moderátorům importovat hodnocení a recenzovat data hromadně, aby mohli analyzovat trendy.</span><span class="sxs-lookup"><span data-stu-id="28ce9-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="28ce9-152">K dispozici je šablona Power BI, která obsahuje základní metriky.</span><span class="sxs-lookup"><span data-stu-id="28ce9-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="28ce9-153">Moderátoři mohou tuto šablonu použít k připojení hromadně importovaných dat a k zobrazení řídicího panelu.</span><span class="sxs-lookup"><span data-stu-id="28ce9-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="28ce9-154">Nemusí vytvářet vlastní řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="28ce9-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="28ce9-155">Moderátoři mohou také upravit šablonu Power BI tak, aby vyhovovala jejich specifickým potřebám.</span><span class="sxs-lookup"><span data-stu-id="28ce9-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="28ce9-156">Chcete-li stáhnout data hodnocení a recenzí, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="28ce9-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="28ce9-157">Přejděte na **Domů \> Recenze \> Vykazování**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="28ce9-158">Chcete-li stáhnout data hodnocení a recenzí hromadně ve formátu hodnot oddělených čárkou (CSV), vyberte možnost **Stáhnout recenze**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="28ce9-159">Zobrazení trendů hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="28ce9-159">View ratings and reviews trends</span></span>

<span data-ttu-id="28ce9-160">Moderátoři mohou stáhnout šablonu Power BI, aby mohli sledovat trendy v řídicím panelu.</span><span class="sxs-lookup"><span data-stu-id="28ce9-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="28ce9-161">Chcete-li zobrazit trendy hodnocení a recenzí, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="28ce9-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="28ce9-162">Přejděte na **Domů \> Recenze \> Vykazování**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="28ce9-163">Vyberte **Šablonu PowerBI** ke stažení šablony.</span><span class="sxs-lookup"><span data-stu-id="28ce9-163">Select **PowerBI template** to download the template.</span></span>

    ![Stáhnutí šablony Power BI](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="28ce9-165">Otevře staženou šablonu pomocí aplikace Power BI.</span><span class="sxs-lookup"><span data-stu-id="28ce9-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="28ce9-166">Zavřete dialogové okno **Přístup k webovému obsahu**, které se zobrazí, a poté zavřete zobrazenou chybovou zprávu "Obnovit".</span><span class="sxs-lookup"><span data-stu-id="28ce9-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="28ce9-167">Přejděte na **Domovskou stránku**, vberte **Upravit dotazy** a pak vyberte **Nastavení zdroje dat**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="28ce9-168">V dialogovém okně **Nastavení zdroje dat** vyberte možnost **Změnit zdroj**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="28ce9-169">V poli **Adresa URL** zadejte cestu k datům recenzí, která jste stáhli v předchozím postupu (například **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="28ce9-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Pole Adresa URL v dialogovém okně hodnot oddělených čárkou](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="28ce9-171">Vyberte možnost **OK** a pak zvolte **Použít změny**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="28ce9-172">Použijete-li změny ve zdroji dat, bude provedena za jednu až dvě minuty.</span><span class="sxs-lookup"><span data-stu-id="28ce9-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="28ce9-173">Chcete-li zobrazit hodnocení a recenze trendů, vyberte volbu **List trendů**.</span><span class="sxs-lookup"><span data-stu-id="28ce9-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trendy hodnocení a recenzí](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="28ce9-175">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="28ce9-175">Additional resources</span></span>

[<span data-ttu-id="28ce9-176">Přehled hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="28ce9-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="28ce9-177">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="28ce9-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="28ce9-178">Konfigurace hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="28ce9-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="28ce9-179">Synchronizace hodnocení produktů v Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="28ce9-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)

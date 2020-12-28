---
title: Správa hodnocení a recenzí
description: V tomto tématu je vysvětleno, jak spravovat hodnocení a recenze v konfigurátoru webu Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 3fc88bc5a5868dce7c0539bf3f0ddc5b751e7b75
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410805"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="12da8-103">Správa hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="12da8-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12da8-104">V tomto tématu je vysvětleno, jak spravovat hodnocení a recenze v konfigurátoru webu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="12da8-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="12da8-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="12da8-105">Overview</span></span>

<span data-ttu-id="12da8-106">Dynamics 365 Commerce použije Microsoft Azure Cognitive Service k automatickému moderování recenzí pomocí redigování slov.</span><span class="sxs-lookup"><span data-stu-id="12da8-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="12da8-107">Kromě toho mohou moderátoři použít konfigurátor webu Dynamics 365 Commerce k implementaci následujících ručních úkolů:</span><span class="sxs-lookup"><span data-stu-id="12da8-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="12da8-108">Moderování recenzí tím, že na ně odpovíte nebo je odeberete.</span><span class="sxs-lookup"><span data-stu-id="12da8-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="12da8-109">Odstranění recenzí zákazníka na žádost zákazníka.</span><span class="sxs-lookup"><span data-stu-id="12da8-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="12da8-110">Hromadný import hodnocení a recenzí pro všechny produkty do šablony Microsoft Power BI, aby bylo možné analyzovat trendy hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="12da8-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="12da8-111">Přečíst recenzi</span><span class="sxs-lookup"><span data-stu-id="12da8-111">Read a review</span></span> 

<span data-ttu-id="12da8-112">Pokud si chcete přečíst recenzi v konfigurátoru webu v Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="12da8-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="12da8-113">Přejděte na **Domů \> Recenze \> Moderování**.</span><span class="sxs-lookup"><span data-stu-id="12da8-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="12da8-114">Pomocí vyhledávacího pole v pravém horním rohu stránky můžete filtrovat recenze, které jsou zobrazeny podle ID produktu, názvu produktu nebo textu recenze.</span><span class="sxs-lookup"><span data-stu-id="12da8-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="12da8-115">Další filtry umožňují omezit recenze podle období, hodnocení, kanálu nebo stavu sledování (přijaté, zodpovězené nebo nahlášené).</span><span class="sxs-lookup"><span data-stu-id="12da8-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Domovská stránka moderování](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="12da8-117">Odpověď na recenzi</span><span class="sxs-lookup"><span data-stu-id="12da8-117">Respond to a review</span></span> 

<span data-ttu-id="12da8-118">V některých případech zákazníci, kteří nakoupili produkt, vyjádřili pokojenost nebo nespokojenosti, nebo neznají způsob používání produktu.</span><span class="sxs-lookup"><span data-stu-id="12da8-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="12da8-119">Jako moderátor můžete odeslat odpověď na recenzi.</span><span class="sxs-lookup"><span data-stu-id="12da8-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="12da8-120">Tato odpověď se zobrazí spolu s recenzí na webu.</span><span class="sxs-lookup"><span data-stu-id="12da8-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="12da8-121">Pokud chcete odpovědět na recenzi v konfigurátoru webu v Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="12da8-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="12da8-122">Přejděte na **Domů \> Recenze \> Moderování**.</span><span class="sxs-lookup"><span data-stu-id="12da8-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="12da8-123">Najít a vybrat revizi, která vyžaduje odpověď.</span><span class="sxs-lookup"><span data-stu-id="12da8-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="12da8-124">V podokně vlastnosti vpravo vyberte možnost **přidat odpověď.**</span><span class="sxs-lookup"><span data-stu-id="12da8-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="12da8-125">Zadejte text odpovědi a název, který má být zobrazen pro respondenta.</span><span class="sxs-lookup"><span data-stu-id="12da8-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="12da8-126">Výchozí název respondenta je **Moderátor**.</span><span class="sxs-lookup"><span data-stu-id="12da8-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="12da8-127">Po dokončení zvolte **Odeslat odpověď**.</span><span class="sxs-lookup"><span data-stu-id="12da8-127">When you've finished, select **Post response**.</span></span>

![Odpověď na recenzi](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="12da8-129">Odstranění recenze</span><span class="sxs-lookup"><span data-stu-id="12da8-129">Take down a review</span></span> 

<span data-ttu-id="12da8-130">Někdy existuje důvod, proč moderátoři z obchodních důvodů odstraní recenze zákazníků.</span><span class="sxs-lookup"><span data-stu-id="12da8-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="12da8-131">Pokud chcete odstranit recenzi v konfigurátoru webu v Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="12da8-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="12da8-132">Přejděte na **Domů \> Recenze \> Moderování**.</span><span class="sxs-lookup"><span data-stu-id="12da8-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="12da8-133">Vyhledejte a vyberte recenzi, kterou je třeba odstranit.</span><span class="sxs-lookup"><span data-stu-id="12da8-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="12da8-134">V podokně vlastnosti napravo vyberte důvod odstranění v části **Odstranění recenze** a poté vyberte možnost **Odebrat**.</span><span class="sxs-lookup"><span data-stu-id="12da8-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="12da8-135">Odstranění recenzí zákazníka na žádost zákazníka.</span><span class="sxs-lookup"><span data-stu-id="12da8-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="12da8-136">Někdy si zákazníci přejí, aby jejich hodnocení a recenze byly trvale smazány z webové stránky elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="12da8-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="12da8-137">Moderátor, který obdrží požadavek na odebrání od zákazníka, může odebrat data odběratele pomocí funkce kontroly odstranění.</span><span class="sxs-lookup"><span data-stu-id="12da8-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="12da8-138">Chcete-li vyhledat a odstranit data odběratele, moderátor potřebuje e-mailovou adresu, kterou odběratel používá k přihlášení a poskytnutí recenzí.</span><span class="sxs-lookup"><span data-stu-id="12da8-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="12da8-139">Chcete-li vyhledat a odstranit data o odběrateli v konfigurátoru webu v Commerce, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="12da8-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="12da8-140">Přejděte na **Domů \> Recenze \> Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="12da8-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="12da8-141">V okně **Hledat uživatele podle e-mailové adresy** zadejte e-mailovou adresu odběratele a pak vyberte **hledat**.</span><span class="sxs-lookup"><span data-stu-id="12da8-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="12da8-142">Pokud má zákazník nějakou aktivitu týkající se recenzí (např. podání recenze, hlasování o užitečnosti recenzí jiného zákazníka nebo komentáře o recenzi jiného zákazníka), zobrazí se výsledky.</span><span class="sxs-lookup"><span data-stu-id="12da8-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="12da8-143">Pro každou položku existuje tlačítko **odstranit.**</span><span class="sxs-lookup"><span data-stu-id="12da8-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="12da8-144">Pro každou položku, kterou je třeba odstranit, vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="12da8-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="12da8-145">Po zobrazení výzvy k potvrzení vyberte možnost **Ano.**</span><span class="sxs-lookup"><span data-stu-id="12da8-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Odstranění dat zákazníků](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="12da8-147">Může trvat až sedm dní, než budou data zcela odstraněna ze systému.</span><span class="sxs-lookup"><span data-stu-id="12da8-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="12da8-148">Moderátoři by měli informovat zákazníky o této prodlevě.</span><span class="sxs-lookup"><span data-stu-id="12da8-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="12da8-149">Pokud uživatelé změnili své jméno v nastavení účtu, může se ve výsledcích hledání zobrazit více položek.</span><span class="sxs-lookup"><span data-stu-id="12da8-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="12da8-150">V takovém přípdě, chcete-li data zákazníka zcela odstranit, musí moderátor pro každou položku vybrat možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="12da8-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="12da8-151">Stáhnout data hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="12da8-151">Download ratings and reviews data</span></span>

<span data-ttu-id="12da8-152">Konfigurátor webu v Commerce umožňuje moderátorům importovat hodnocení a recenzovat data hromadně, aby mohli analyzovat trendy.</span><span class="sxs-lookup"><span data-stu-id="12da8-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="12da8-153">K dispozici je šablona Power BI, která obsahuje základní metriky.</span><span class="sxs-lookup"><span data-stu-id="12da8-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="12da8-154">Moderátoři mohou tuto šablonu použít k připojení hromadně importovaných dat a k zobrazení řídicího panelu.</span><span class="sxs-lookup"><span data-stu-id="12da8-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="12da8-155">Nemusí vytvářet vlastní řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="12da8-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="12da8-156">Moderátoři mohou také upravit šablonu Power BI tak, aby vyhovovala jejich specifickým potřebám.</span><span class="sxs-lookup"><span data-stu-id="12da8-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="12da8-157">Chcete-li stáhnout data hodnocení a recenzí v konfigurátoru webu v Commerce, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="12da8-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="12da8-158">Přejděte na **Domů \> Recenze \> Vykazování**.</span><span class="sxs-lookup"><span data-stu-id="12da8-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="12da8-159">Chcete-li stáhnout data hodnocení a recenzí hromadně ve formátu hodnot oddělených čárkou (CSV), vyberte možnost **Stáhnout data recenzí**.</span><span class="sxs-lookup"><span data-stu-id="12da8-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="12da8-160">Zobrazení trendů hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="12da8-160">View ratings and reviews trends</span></span>

<span data-ttu-id="12da8-161">Moderátoři mohou stáhnout šablonu Power BI, aby mohli sledovat trendy v řídicím panelu.</span><span class="sxs-lookup"><span data-stu-id="12da8-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="12da8-162">Chcete-li si zobrazit trendy hodnocení a recenzí v konfigurátoru webu v Commerce, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="12da8-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="12da8-163">Přejděte na **Domů \> Recenze \> Vykazování**.</span><span class="sxs-lookup"><span data-stu-id="12da8-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="12da8-164">Vyberte **Šablonu PowerBI** ke stažení šablony.</span><span class="sxs-lookup"><span data-stu-id="12da8-164">Select **PowerBI template** to download the template.</span></span>

    ![Stáhnout šablonu Power BI](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="12da8-166">Otevře staženou šablonu pomocí aplikace Power BI.</span><span class="sxs-lookup"><span data-stu-id="12da8-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="12da8-167">Zavřete dialogové okno **Přístup k webovému obsahu**, které se zobrazí, a poté zavřete zobrazenou chybovou zprávu "Obnovit".</span><span class="sxs-lookup"><span data-stu-id="12da8-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="12da8-168">Přejděte na **Domovskou stránku**, vberte **Upravit dotazy** a pak vyberte **Nastavení zdroje dat**.</span><span class="sxs-lookup"><span data-stu-id="12da8-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="12da8-169">V dialogovém okně **Nastavení zdroje dat** vyberte možnost **Změnit zdroj**.</span><span class="sxs-lookup"><span data-stu-id="12da8-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="12da8-170">V poli **Adresa URL** zadejte cestu k datům recenzí, která jste stáhli v předchozím postupu (například **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="12da8-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Pole Adresa URL v dialogovém okně hodnot oddělených čárkou](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="12da8-172">Vyberte možnost **OK** a pak zvolte **Použít změny**.</span><span class="sxs-lookup"><span data-stu-id="12da8-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="12da8-173">Použijete-li změny ve zdroji dat, bude provedena za jednu až dvě minuty.</span><span class="sxs-lookup"><span data-stu-id="12da8-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="12da8-174">Chcete-li zobrazit hodnocení a recenze trendů, vyberte volbu **List trendů**.</span><span class="sxs-lookup"><span data-stu-id="12da8-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trendy hodnocení a recenzí](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="12da8-176">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="12da8-176">Additional resources</span></span>

[<span data-ttu-id="12da8-177">Přehled hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="12da8-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="12da8-178">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="12da8-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="12da8-179">Konfigurace hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="12da8-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="12da8-180">Synchronizace hodnocení produktů v Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="12da8-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)

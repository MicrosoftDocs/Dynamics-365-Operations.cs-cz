---
title: Synchronizace hodnocení produktů v Dynamics 365 Commerce
description: Toto téma popisuje, jak synchronizovat hodnocení produktu v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ab6de4bfa619df74bafc5511affddd516bdb34f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260302"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="18ad1-103">Synchronizace hodnocení produktů v Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="18ad1-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18ad1-104">Toto téma popisuje, jak synchronizovat hodnocení produktu v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="18ad1-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="18ad1-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="18ad1-105">Overview</span></span>

<span data-ttu-id="18ad1-106">Chcete-li využívat hodnocení produktů v omnikanálech, jako je například na pokladním místě (POS) a v kontaktních střediscích, musí být hodnocení produktů ze služby hodnocení a recenzí importována do databáze velkoobchodní sítě.</span><span class="sxs-lookup"><span data-stu-id="18ad1-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="18ad1-107">Pokud jsou hodnocení produktů k dispozici v omnikanálech, mohou zákazníkům pomoci při jejich interakci s prodejcem.</span><span class="sxs-lookup"><span data-stu-id="18ad1-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="18ad1-108">Toto téma popisuje následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="18ad1-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="18ad1-109">Nakonfigurujte **úlohu synchronizace hodnocení produktu** jako dávkovou úlohu a synchronizujte hodnocení produktu ze **služby hodnocení a recenzí**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="18ad1-110">Ověřte, že dávková úloha synchronizace hodnocení produktu proběhla úspěšně.</span><span class="sxs-lookup"><span data-stu-id="18ad1-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="18ad1-111">Zajistěte dostupnost hodnocení produktu na POS.</span><span class="sxs-lookup"><span data-stu-id="18ad1-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="18ad1-112">Konfigurace maloobchodní dávkové úlohy k synchronizaci hodnocení produktu</span><span class="sxs-lookup"><span data-stu-id="18ad1-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18ad1-113">Dříve než začnete, zkontrolujte, zda je nainstalována verze Dynamics 365 Commerce 10.0.6 nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="18ad1-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="18ad1-114">Inicializujte velkoobchodní plánovač</span><span class="sxs-lookup"><span data-stu-id="18ad1-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="18ad1-115">Pro inicializaci velkoobchodního plánovače postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="18ad1-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="18ad1-116">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Inicializovat plánovač velkoobchodu**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="18ad1-117">Případně vyhledejte "inicializovat velkoobchodní plánovač".</span><span class="sxs-lookup"><span data-stu-id="18ad1-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="18ad1-118">V dialogovém okně **Inicializovat velkoobchodní plánovač** zkontrolujte, zda je možnost **Odstranit existující konfiguraci** nastavena na hodnotu **Ne**, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="18ad1-119">Ověřit dílčí úlohu RetailProductRating</span><span class="sxs-lookup"><span data-stu-id="18ad1-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="18ad1-120">Chcete-li ověřit, zda existuje dílčí úloha **RetailProductRating**, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="18ad1-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="18ad1-121">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Dílčí úlohy plánovače**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="18ad1-122">Případně vyhledejte "Plánovač dílčích úloh".</span><span class="sxs-lookup"><span data-stu-id="18ad1-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="18ad1-123">V seznamu dílčích úloh vyhledejte nebo vyhledejte dílčí úlohu **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="18ad1-124">Následující ilustrace znázorňuje příklad stránky odrobnosti dílčích úloh v Commerce.</span><span class="sxs-lookup"><span data-stu-id="18ad1-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![Podrobnosti o dílčí úloze RetailProductRating](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="18ad1-126">Pokud nenajdete dílčí úlohu **RetailProductRating**, je možné, že jste již před inicializací velkoobchodního plánovače spustili úlohu **Synchronizace hodnocení produktů** a **1040 CDX**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="18ad1-127">V takovém případě spusťte úlohu **Úplná synchronizace dat** provedením následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="18ad1-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="18ad1-128">Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Databáze kanálu**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="18ad1-129">Případně můžete vyhledat "Databáze kanálů".</span><span class="sxs-lookup"><span data-stu-id="18ad1-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="18ad1-130">Vyberte databázi kanálů, která má být synchronizována.</span><span class="sxs-lookup"><span data-stu-id="18ad1-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="18ad1-131">V podokně akcí vyberte **Úplná synchronizace dat**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="18ad1-132">V rozevíracím dialogovém okně **Vybrat plán distribuce** vyberte **1040 - produkty** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="18ad1-133">Zopakováním kroků předchozího postupu ověřte, zda byla vytvořena dílčí úloha **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="18ad1-134">Import hodnocení produktů</span><span class="sxs-lookup"><span data-stu-id="18ad1-134">Import product ratings</span></span>

<span data-ttu-id="18ad1-135">Chcete-li importovat hodnocení produktů do velkoobchodu ze služby hodnocení a recenze, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="18ad1-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="18ad1-136">Přejděte na **Retail and Commerce \> Nastavení centrály \> Velkoobchodní plánovač \> Úloha synchronizace hodnocení produktů**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="18ad1-137">Případně vyhledejte "Úloha synchronizace hodnocení produktů".</span><span class="sxs-lookup"><span data-stu-id="18ad1-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="18ad1-138">V dialogovém okně **Hodnocení vyžádaných produktů** na pevné záložce **Spustit na pozadí** vyberte **Opakování**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="18ad1-139">V dialogovém okně **Definovat opakování** nastavte způsob opakování.</span><span class="sxs-lookup"><span data-stu-id="18ad1-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="18ad1-140">(Doporučená hodnota je dvě hodiny.) Neplánujte opakování, které je menší než jedna hodina.</span><span class="sxs-lookup"><span data-stu-id="18ad1-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="18ad1-141">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-141">Select **OK**.</span></span>
1. <span data-ttu-id="18ad1-142">Nastavte **Dávkové zpracování** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="18ad1-143">Toto nastavení pomáhá zaručit, že budete moci auditovat protokoly a ověřit stav spuštění dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="18ad1-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="18ad1-144">Výběrem **OK** naplánujte dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="18ad1-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="18ad1-145">Následující ilustrace znázorňuje příklad konfigurace dílčích úloh v Commerce.</span><span class="sxs-lookup"><span data-stu-id="18ad1-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![Konfigurace dávkové úlohy hodnocení produktů pro synchronizaci](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="18ad1-147">Ověřte, že dávková úloha synchronizace hodnocení produktu proběhla úspěšně</span><span class="sxs-lookup"><span data-stu-id="18ad1-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="18ad1-148">Chcete-li ověřit, zda byla dávková úloha **Synchronizace hodnocení produktů** úspěšná, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="18ad1-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="18ad1-149">Přejděte na **Retail and Commerce \> Správce systému \> Dotazy \> Dávkové úlohy** nebo, pokud používáte skladovou jednotku (SKU) pouze pro Commerce, **Retail and Commerce \> Dotazy a sestavy \> Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="18ad1-150">Případně vyhledejte "Dávkové úlohy."</span><span class="sxs-lookup"><span data-stu-id="18ad1-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="18ad1-151">Chcete-li zobrazit podrobné informace o dávkové úloze, v seznamu dávkové úlohy ve sloupci **Popis úlohy** vyhledejte popis, který obsahuje "Hodnocení vyžádaného produktu."</span><span class="sxs-lookup"><span data-stu-id="18ad1-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="18ad1-152">Vyberte ID úlohy pro zobrazení podrobností dávkové úlohy, jako je například plánované datum a čas zahájení a text opakování.</span><span class="sxs-lookup"><span data-stu-id="18ad1-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="18ad1-153">Na následujícím obrázku je znázorněn příklad podrobností dávkové úlohy v Commerce, když je dávková úloha naplánována na spuštění v intervalech dvou hodin.</span><span class="sxs-lookup"><span data-stu-id="18ad1-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![Podrobnosti dávkové úlohy Synchronizace hodnocení produktů](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="18ad1-155">Zajistěte dostupnost hodnocení produktu na POS</span><span class="sxs-lookup"><span data-stu-id="18ad1-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="18ad1-156">Řešení pro hodnocení a recenze v Dynamics 365 Commerce je omnikanálové řešení.</span><span class="sxs-lookup"><span data-stu-id="18ad1-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="18ad1-157">Hodnocení produktů však není ve výchozím nastavení v POS zobrazeno.</span><span class="sxs-lookup"><span data-stu-id="18ad1-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="18ad1-158">Chcete-li zákazníkům pomoci v obchodech vidět hodnocení a recenze, pokud jim pomáhají pracovníci obchodu, musíte hodnocení produktů zapnout v POS.</span><span class="sxs-lookup"><span data-stu-id="18ad1-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="18ad1-159">Chcete-li zapnout hodnocení produktů v POS, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="18ad1-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="18ad1-160">Přejděte na možnost **Retail a Commerce \> Nastavení velkoobchodu \> Parametry \> Parametry velkoobchodu**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="18ad1-161">Případně můžete vyhledat "Parametry velkoobchodu".</span><span class="sxs-lookup"><span data-stu-id="18ad1-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="18ad1-162">Na kartě **Konfigurační parametry** vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="18ad1-163">Zadejte název, například **RatingsAndReviews.EnableProductRatingsForRetailStores**, a nastavte hodnotu na **true**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="18ad1-164">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-164">Select **Save**.</span></span>
1. <span data-ttu-id="18ad1-165">Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="18ad1-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="18ad1-166">Případně můžete vyhledat hodnotu "Plán distribuce".</span><span class="sxs-lookup"><span data-stu-id="18ad1-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="18ad1-167">V seznamu úloh vyberte **1110** (**Globální konfigurace**) a pak vyberte možnost **Spustit nyní.**</span><span class="sxs-lookup"><span data-stu-id="18ad1-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="18ad1-168">Po úspěšném spuštění úlohy ověřte, zda jsou nyní v POS zobrazena hodnocení produktů.</span><span class="sxs-lookup"><span data-stu-id="18ad1-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="18ad1-169">Na následujícím obrázku je znázorněn příklad konfigurace parametrů velkoobchodu, které zapínají hodnocení produktů na POS.</span><span class="sxs-lookup"><span data-stu-id="18ad1-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![Konfigurace parametrů velkoobchodu pro hodnocení produktů v POS](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="18ad1-171">Následující obrázek znázorňuje příklad hodnocení produktů na POS.</span><span class="sxs-lookup"><span data-stu-id="18ad1-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Hodnocení produktů na POS](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="18ad1-173">Následující obrázek znázorňuje příklad hodnocení produktů v kanálech kontaktního střediska.</span><span class="sxs-lookup"><span data-stu-id="18ad1-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Hodnocení produktu v kanálu kontaktního střediska](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="18ad1-175">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="18ad1-175">Additional resources</span></span>

[<span data-ttu-id="18ad1-176">Přehled hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="18ad1-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="18ad1-177">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="18ad1-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="18ad1-178">Správa hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="18ad1-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="18ad1-179">Konfigurace hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="18ad1-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Řídicí panel Správy využití
description: Toto téma vysvětluje, jak pomocí řídicího panelu Správa využití monitorovat používání služby elektronické fakturace a být v souladu s předpisy.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130499"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="ba83e-103">Řídicí panel Správy využití</span><span class="sxs-lookup"><span data-stu-id="ba83e-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba83e-104">Řídicí panel **Správa využití** vám pomůže sledovat využití služby elektronické fakturace, a proto pomůže vaší organizaci zůstat v souladu s podmínkami měsíčního využití.</span><span class="sxs-lookup"><span data-stu-id="ba83e-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="ba83e-105">Dodržování přepisů se určuje výpočtem objemu podání a jeho porovnáním se získaným objemem podání, aby se identifikovaly odchylky mezi získaným objemem a použitým objemem.</span><span class="sxs-lookup"><span data-stu-id="ba83e-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="ba83e-106">Řídicí panel obsahuje následující indikátory:</span><span class="sxs-lookup"><span data-stu-id="ba83e-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="ba83e-107">Jeden indikátor nákladů, který můžete použít ke sledování spotřeby pro účely dodržování licenčních podmínek:</span><span class="sxs-lookup"><span data-stu-id="ba83e-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="ba83e-108">Využití za měsíc (export)</span><span class="sxs-lookup"><span data-stu-id="ba83e-108">Usage per month (export)</span></span>

- <span data-ttu-id="ba83e-109">Tři provozní indikátory, které můžete použít ke sledování využití služby elektronické fakturace pro účely správy:</span><span class="sxs-lookup"><span data-stu-id="ba83e-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="ba83e-110">Využití podle funkce</span><span class="sxs-lookup"><span data-stu-id="ba83e-110">Usage by feature</span></span>
    - <span data-ttu-id="ba83e-111">Využití podle prostředí</span><span class="sxs-lookup"><span data-stu-id="ba83e-111">Usage by environment</span></span>
    - <span data-ttu-id="ba83e-112">Využití za měsíc (import)</span><span class="sxs-lookup"><span data-stu-id="ba83e-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="ba83e-113">Rozsah měření</span><span class="sxs-lookup"><span data-stu-id="ba83e-113">Measurement scope</span></span>

- <span data-ttu-id="ba83e-114">Měrná jednotka:</span><span class="sxs-lookup"><span data-stu-id="ba83e-114">Unit of measure:</span></span> 

    <span data-ttu-id="ba83e-115">Řídicí panel **Správa využití** počítá odeslání obchodních dokumentů a importovaných elektronických faktur.</span><span class="sxs-lookup"><span data-stu-id="ba83e-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="ba83e-116">Organizace:</span><span class="sxs-lookup"><span data-stu-id="ba83e-116">Organization:</span></span> 

    <span data-ttu-id="ba83e-117">Počítání je shrnuto podle ID klienta vaší organizace bez ohledu na počet instancí Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management, nebo počet právnických osob, kde je povolena služba elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ba83e-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="ba83e-118">Ukazatel: Měsíční využití (export)</span><span class="sxs-lookup"><span data-stu-id="ba83e-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="ba83e-119">Tento indikátor poskytuje podrobnosti o elektronických fakturách, které vaše organizace vystavuje během definovaného období.</span><span class="sxs-lookup"><span data-stu-id="ba83e-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="ba83e-120">Rozsah</span><span class="sxs-lookup"><span data-stu-id="ba83e-120">Scope</span></span>
- <span data-ttu-id="ba83e-121">Počet obchodních dokumentů, které se odesílají z Finance a Supply Chain Management do služby elektronické fakturace, bez ohledu na počet řádků, které tyto obchodní dokumenty obsahují.</span><span class="sxs-lookup"><span data-stu-id="ba83e-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="ba83e-122">Počet odeslaných obchodních dokumentů, které jsou úspěšně zpracovány službou elektronická fakturace.</span><span class="sxs-lookup"><span data-stu-id="ba83e-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="ba83e-123">Dokument je považován za úspěšně zpracovaný, když je dokončen tok akcí definovaných v nastavení funkce.</span><span class="sxs-lookup"><span data-stu-id="ba83e-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="ba83e-124">Když je elektronická faktura odeslána do externí webové služby, počítání je nezávislé na výsledcích zpracování webové služby (přijato, odmítnuto nebo chyba ověření schématu).</span><span class="sxs-lookup"><span data-stu-id="ba83e-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="ba83e-125">Pokud webová služba přijala a odpověděla na požadavek služby elektronické fakturace, je odeslání považováno za platné počítání.</span><span class="sxs-lookup"><span data-stu-id="ba83e-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="ba83e-126">**Výjimka:** Obchodní dokumenty se nezapočítávají, pokud jsou znovu odeslány z Finance and Supply Chain Management do služby elektronické fakturace, například ve scénářích, kdy je pro změnu stavu elektronické faktury nutné opětovné odeslání stejného obchodního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="ba83e-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="ba83e-127">Například vystavení brazilské elektronické faktury (fiskálního dokumentu) se počítá jako platné, ale žádost o zrušení se nepočítá.</span><span class="sxs-lookup"><span data-stu-id="ba83e-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="ba83e-128">Výpočet</span><span class="sxs-lookup"><span data-stu-id="ba83e-128">Calculation</span></span>

<span data-ttu-id="ba83e-129">Výpočet zůstatku se počítá takto:</span><span class="sxs-lookup"><span data-stu-id="ba83e-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="ba83e-130">Zůstatek = zdarma + zakoupené - použité</span><span class="sxs-lookup"><span data-stu-id="ba83e-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="ba83e-131">Kde:</span><span class="sxs-lookup"><span data-stu-id="ba83e-131">Where:</span></span>

- <span data-ttu-id="ba83e-132">Zdarma:</span><span class="sxs-lookup"><span data-stu-id="ba83e-132">Free:</span></span>
  
    <span data-ttu-id="ba83e-133">Objem bchodních dokumentů, které může zákazník zdarma odeslat za měsíc.</span><span class="sxs-lookup"><span data-stu-id="ba83e-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="ba83e-134">Zahrnuje balíček 100 obchodních dokumentů, které lze odeslat službě elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ba83e-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="ba83e-135">Objem zdarma není kumulativní a zbývající zůstatek se nepřenesl do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="ba83e-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="ba83e-136">Zakoupené:</span><span class="sxs-lookup"><span data-stu-id="ba83e-136">Purchased:</span></span>
  
    <span data-ttu-id="ba83e-137">Balíček 1 000 obchodních dokumentů, které lze odeslat službě elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ba83e-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="ba83e-138">Tento balíček je nutné pro vaši organizaci získat každý měsíc.</span><span class="sxs-lookup"><span data-stu-id="ba83e-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="ba83e-139">Zakoupený objem není kumulativní a zbývající zůstatek se nepřenesl do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="ba83e-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="ba83e-140">Použito:</span><span class="sxs-lookup"><span data-stu-id="ba83e-140">Used:</span></span> 

    <span data-ttu-id="ba83e-141">Počet odeslání obchodních dokumentů do služby elektronické fakturace podle definovaných kritérií.</span><span class="sxs-lookup"><span data-stu-id="ba83e-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="ba83e-142">Pokud vaše organizace plánuje překročit měsíční objem 100 bezplatných podání, zakupte si maximální objem, abyste zajistili, že budete i nadále v souladu s licenčními zásadami společnosti Microsoft pro službu elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ba83e-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="ba83e-143">Aktuálně musí být zakoupený objem ručně zadán podle data pořízení jako více balíčků po 1 000 odesláních.</span><span class="sxs-lookup"><span data-stu-id="ba83e-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="ba83e-144">Indikátor: Využití podle funkce</span><span class="sxs-lookup"><span data-stu-id="ba83e-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="ba83e-145">Tento indikátor ukazuje využití funkcí elektronické fakturace pro vystavování elektronických faktur během definovaného období.</span><span class="sxs-lookup"><span data-stu-id="ba83e-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="ba83e-146">Výpočet:</span><span class="sxs-lookup"><span data-stu-id="ba83e-146">Calculation:</span></span>
  
    <span data-ttu-id="ba83e-147">Použité = Počet, kolikrát byla každá funkce elektronické fakturace použita při odesílání obchodních dokumentů službě elektronická fakturace.</span><span class="sxs-lookup"><span data-stu-id="ba83e-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="ba83e-148">Indikátor: Využití podle prostředí</span><span class="sxs-lookup"><span data-stu-id="ba83e-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="ba83e-149">Tento indikátor ukazuje využití prostředí služeb elektronické fakturace během definovaného období.</span><span class="sxs-lookup"><span data-stu-id="ba83e-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="ba83e-150">Výpočet:</span><span class="sxs-lookup"><span data-stu-id="ba83e-150">Calculation:</span></span>
    
    <span data-ttu-id="ba83e-151">Použité = Počet, kolikrát byla každé prostředí služby elektronické fakturace použita při odesílání obchodních dokumentů službě elektronická fakturace.</span><span class="sxs-lookup"><span data-stu-id="ba83e-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="ba83e-152">Ukazatel: Měsíční využití (import)</span><span class="sxs-lookup"><span data-stu-id="ba83e-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="ba83e-153">Tento indikátor ukazuje objem importu elektronických faktur službou elektronická fakturace do Finance a Supply Chain Management za definované období.</span><span class="sxs-lookup"><span data-stu-id="ba83e-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="ba83e-154">Rozsah:</span><span class="sxs-lookup"><span data-stu-id="ba83e-154">Scope:</span></span>

    <span data-ttu-id="ba83e-155">Elektronické faktury, které se importují do služby Finance a Supply Chain Management, bez ohledu na počet řádků, které tyto elektronické faktury obsahují.</span><span class="sxs-lookup"><span data-stu-id="ba83e-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="ba83e-156">Výpočet:</span><span class="sxs-lookup"><span data-stu-id="ba83e-156">Calculation:</span></span>

    <span data-ttu-id="ba83e-157">Přijato = Počet importovaných elektronických faktur do Finance a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ba83e-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="ba83e-158">Funkce</span><span class="sxs-lookup"><span data-stu-id="ba83e-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="ba83e-159">Nákup</span><span class="sxs-lookup"><span data-stu-id="ba83e-159">Purchase</span></span>

<span data-ttu-id="ba83e-160">Na kartě **Využití za měsíc (export)** vyberte **Nákup**, chcete-li ručně zaregistrovat množství získaných příspěvků.</span><span class="sxs-lookup"><span data-stu-id="ba83e-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="ba83e-161">Pro dané datum vyberte **Nový** a zadejte počet **Balíčků** získaných k tomuto datu.</span><span class="sxs-lookup"><span data-stu-id="ba83e-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="ba83e-162">**Množství** se počítá jako:</span><span class="sxs-lookup"><span data-stu-id="ba83e-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="ba83e-163">Množství = balíčky \* 1 000</span><span class="sxs-lookup"><span data-stu-id="ba83e-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="ba83e-164">Vypočítané **Množství** odráží v **Zakoupeno** z indikátoru **Využití za měsíc (export)**.</span><span class="sxs-lookup"><span data-stu-id="ba83e-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="ba83e-165">Aktualizace</span><span class="sxs-lookup"><span data-stu-id="ba83e-165">Update</span></span>

<span data-ttu-id="ba83e-166">V podokně akcí vyberte **Aktualizovat** k aktualizaci výpočtu a aktualizaci údajů zobrazených na stránce a v grafu.</span><span class="sxs-lookup"><span data-stu-id="ba83e-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="ba83e-167">Obnovit data historie</span><span class="sxs-lookup"><span data-stu-id="ba83e-167">Reset history data</span></span>

<span data-ttu-id="ba83e-168">V podokně akcí vyberte **Obnovit data historie**, chcete-li aktualizovat databázi, ze které se počítají ukazatele.</span><span class="sxs-lookup"><span data-stu-id="ba83e-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="ba83e-169">Řídicí panel **Správa využití** nezobrazuje peněžní částky.</span><span class="sxs-lookup"><span data-stu-id="ba83e-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="ba83e-170">Místo toho zobrazuje pouze objem počítaných odeslání a importovaných dokumentů.</span><span class="sxs-lookup"><span data-stu-id="ba83e-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

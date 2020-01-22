---
title: Konfigurace prostředí náhledu Commerce
description: Toto téma vysvětluje, jak konfigurovat ukázkové prostředí v Microsoft Dynamics 365 Commerce poté, co je zřízeno.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906132"
---
# <a name="configure-a-commerce-preview-environment"></a><span data-ttu-id="1efe1-103">Konfigurace prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="1efe1-103">Configure a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1efe1-104">Toto téma vysvětluje, jak konfigurovat ukázkové prostředí v Microsoft Dynamics 365 Commerce poté, co je zřízeno.</span><span class="sxs-lookup"><span data-stu-id="1efe1-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="1efe1-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="1efe1-105">Overview</span></span>

<span data-ttu-id="1efe1-106">Postupy v tomto tématu dokončete až po zřízení prostředí náhledu Commerce.</span><span class="sxs-lookup"><span data-stu-id="1efe1-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="1efe1-107">Informace o postupu zřízení prostředí náhledu Commerce najdete v části [Zřízení prostředí náhledu Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="1efe1-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="1efe1-108">Po kompletním zřízení prostředí náhledu Commerce je nutné dokončit další kroky konfigurace po zřízení, aby bylo možné začít posuzovat prostředí.</span><span class="sxs-lookup"><span data-stu-id="1efe1-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="1efe1-109">K dokončení těchto kroků je nutné použít prostředí Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce a Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="1efe1-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="1efe1-110">Než začnete</span><span class="sxs-lookup"><span data-stu-id="1efe1-110">Before you start</span></span>

1. <span data-ttu-id="1efe1-111">Přihlaste se do [portálu LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="1efe1-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="1efe1-112">Přejděte na svůj projekt.</span><span class="sxs-lookup"><span data-stu-id="1efe1-112">Go to your project.</span></span>
1. <span data-ttu-id="1efe1-113">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="1efe1-114">V seznamu vyberte své prostředí.</span><span class="sxs-lookup"><span data-stu-id="1efe1-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="1efe1-115">V informacích o prostředí vpravo vyberte **úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="1efe1-116">Kliknutím na **Přihlásit** otevřete nabídku a pak vyberte **Přihlásit se k prostředí**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="1efe1-117">Ujistěte se, že je v pravém horním rohu vybrána právnická osoba **USRT**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="1efe1-118">Konfigurace pokladního místa v LCS</span><span class="sxs-lookup"><span data-stu-id="1efe1-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="1efe1-119">Přidružení pracovníka k vaší identitě</span><span class="sxs-lookup"><span data-stu-id="1efe1-119">Associate a worker with your identity</span></span>

<span data-ttu-id="1efe1-120">Chcete-li pracovníka s vaší identitou přidružit k LCS, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="1efe1-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="1efe1-121">Pomocí nabídky vlevo přejděte na **Moduly \> Maloobchod \> Zaměstnanci \> Pracovníci**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="1efe1-122">V seznamu vyhledejte a vyberte následující záznam: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="1efe1-123">V podokně akcí zvolte **Maloobchod**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="1efe1-124">Vyberte **Stávající identita přidružení**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="1efe1-125">Do pole **E-mail** vpravo od **Hledání pomocí e-mailu** zadejte svou e-mailovou adresu.</span><span class="sxs-lookup"><span data-stu-id="1efe1-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="1efe1-126">Vyberte **Vyhledat**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-126">Select **Search**.</span></span>
1. <span data-ttu-id="1efe1-127">Vyberte záznam obsahující vaše jméno.</span><span class="sxs-lookup"><span data-stu-id="1efe1-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="1efe1-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-128">Select **OK**.</span></span>
1. <span data-ttu-id="1efe1-129">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="1efe1-130">Aktivovat Cloud POS</span><span class="sxs-lookup"><span data-stu-id="1efe1-130">Activate Cloud POS</span></span>

<span data-ttu-id="1efe1-131">Chcete-li aktivovat Cloud POS v LCS, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="1efe1-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="1efe1-132">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="1efe1-133">V seznamu vyberte své prostředí.</span><span class="sxs-lookup"><span data-stu-id="1efe1-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="1efe1-134">V informacích o prostředí vpravo vyberte **úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="1efe1-135">Vyberte **Přihlásit** k otevření nabídky a pak vyberte **Přihlásit ke cloudovému pokladnímu místu** k otevření pokladního místa (POS).</span><span class="sxs-lookup"><span data-stu-id="1efe1-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="1efe1-136">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-136">Select **Next**.</span></span>
1. <span data-ttu-id="1efe1-137">Přihlaste se pomocí účtu Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="1efe1-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="1efe1-138">V poli **Název obchodu** vyberte **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="1efe1-139">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-139">Select **Next**.</span></span>
1. <span data-ttu-id="1efe1-140">V **Registr a zařízení** vyberte **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="1efe1-141">Vyberte **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-141">Select **Activate**.</span></span> <span data-ttu-id="1efe1-142">Jste přihlášeni a přesměrováni na přihlašovací stránku POS.</span><span class="sxs-lookup"><span data-stu-id="1efe1-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="1efe1-143">Nyní se můžete přihlásit ke cloudovému POS pomocí ID operátora **000713** a hesla **123**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="1efe1-144">Nastavení webu v Commerce</span><span class="sxs-lookup"><span data-stu-id="1efe1-144">Set up your site in Commerce</span></span>

<span data-ttu-id="1efe1-145">Pokud chcete začít nastavovat náhled webu v Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="1efe1-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="1efe1-146">Přihlaste se k nástroji pro správu webu pomocí adresy URL, kterou jste si poznamenali při inicializaci e-Commerce během zřizování (viz [Inicializace e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="1efe1-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="1efe1-147">Vyberte web **Fabrikam** otevřete dialogové okno nastavení webu.</span><span class="sxs-lookup"><span data-stu-id="1efe1-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="1efe1-148">Vyberte doménu, kterou jste zadali při inicializaci platformy e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="1efe1-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="1efe1-149">Jako výchozí kanál vyberte **Rozšířený online obchod společnosti Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="1efe1-150">(Zkontrolujte, zda jste vybrali **rozšířený** online obchod.)</span><span class="sxs-lookup"><span data-stu-id="1efe1-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="1efe1-151">Jako výchozí jazyk vyberte **en-us**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="1efe1-152">Ponechte hodnotu pole **Cesta** tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="1efe1-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="1efe1-153">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-153">Select **OK**.</span></span> <span data-ttu-id="1efe1-154">Zobrazí se seznam stránek na webu.</span><span class="sxs-lookup"><span data-stu-id="1efe1-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="1efe1-155">Povolení úloh v programu Retail</span><span class="sxs-lookup"><span data-stu-id="1efe1-155">Enable jobs in Retail</span></span>

<span data-ttu-id="1efe1-156">Pokud chcete povolit úlohy v programu Retail, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="1efe1-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="1efe1-157">Přihlaste se k prostředí (HQ).</span><span class="sxs-lookup"><span data-stu-id="1efe1-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="1efe1-158">Pomocí nabídky vlevo přejděte na **Retail \> Dotazy a sestavy \> Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="1efe1-159">Zbývající kroky tohoto postupu musí být dokončeny pro každou z následujících úloh:</span><span class="sxs-lookup"><span data-stu-id="1efe1-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="1efe1-160">Zpracovat maloobchodní oznámení objednávky e-mailem</span><span class="sxs-lookup"><span data-stu-id="1efe1-160">Process retail order email notification</span></span>
    * <span data-ttu-id="1efe1-161">Dostupnost produktu</span><span class="sxs-lookup"><span data-stu-id="1efe1-161">Product availability</span></span>
    * <span data-ttu-id="1efe1-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="1efe1-162">P-0001</span></span>
    * <span data-ttu-id="1efe1-163">Synchronizovat úlohu objednávek</span><span class="sxs-lookup"><span data-stu-id="1efe1-163">Synchronize orders job</span></span>

1. <span data-ttu-id="1efe1-164">Pomocí rychlého filtru vyhledejte úlohu podle názvu.</span><span class="sxs-lookup"><span data-stu-id="1efe1-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="1efe1-165">Je-li stav úlohy nastaven na **Srážka**, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="1efe1-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="1efe1-166">Vybrat záznam.</span><span class="sxs-lookup"><span data-stu-id="1efe1-166">Select the record.</span></span>
    1. <span data-ttu-id="1efe1-167">V podokně akcí na kartě **Dávková úloha** vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="1efe1-168">Vyberte možnost **Čekání** a potom **OK**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="1efe1-169">Spuštění úplné synchronizace dat v programu Retail</span><span class="sxs-lookup"><span data-stu-id="1efe1-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="1efe1-170">Chcete-li spustit úplnou synchronizaci dat v programu Retail, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="1efe1-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="1efe1-171">Pomocí nabídky vlevo přejděte na **Moduly \> Retail \> Nastavení centrály \> Maloobchodní plánovač \> Databáze kanálů**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="1efe1-172">V seznamu nalevo je vybrán **Výchozí** kanál.</span><span class="sxs-lookup"><span data-stu-id="1efe1-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="1efe1-173">Vyberte jiný dostupný kanál.</span><span class="sxs-lookup"><span data-stu-id="1efe1-173">Select the other available channel.</span></span> <span data-ttu-id="1efe1-174">Tento kanál má název **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="1efe1-175">V podokně akcí vyberte **Úplná synchronizace dat**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="1efe1-176">Jako plán distribuce zadejte **9999**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="1efe1-177">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-177">Select **OK**.</span></span>
1. <span data-ttu-id="1efe1-178">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1efe1-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="1efe1-179">Testování informací o kreditní kartě za účelem provedení zkušebních nákupů</span><span class="sxs-lookup"><span data-stu-id="1efe1-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="1efe1-180">Chcete-li provést zkušební transakce na webu, můžete použít následující testovací kreditní kartu:</span><span class="sxs-lookup"><span data-stu-id="1efe1-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="1efe1-181">**Číslo karty:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="1efe1-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="1efe1-182">**Datum konce platnosti:** 10/20</span><span class="sxs-lookup"><span data-stu-id="1efe1-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="1efe1-183">**Ověřovací hodnota platební karty (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="1efe1-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1efe1-184">V žádném případě byste neměli používat informace o skutečné kreditní kartě na testovacím webu.</span><span class="sxs-lookup"><span data-stu-id="1efe1-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1efe1-185">Další kroky</span><span class="sxs-lookup"><span data-stu-id="1efe1-185">Next steps</span></span>

<span data-ttu-id="1efe1-186">Po dokončení postupu zřizování a konfigurace můžete vyhodnotit prostředí náhledu.</span><span class="sxs-lookup"><span data-stu-id="1efe1-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="1efe1-187">Pomocí adresy URL nástroje pro správu webu Commerce můžete přejít na práci s vytvářením.</span><span class="sxs-lookup"><span data-stu-id="1efe1-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="1efe1-188">Pomocí adresy URL nástroje pro správu webu zákazníka maloobchodu můžete přejít na práci s vytvářením.</span><span class="sxs-lookup"><span data-stu-id="1efe1-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="1efe1-189">Pokud chcete provést konfiguraci volitelných funkcí prostředí pro náhled Commerce, najdete informace v části [konfigurace volitelných funkcí prostředí pro náhled Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="1efe1-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1efe1-190">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="1efe1-190">Additional resources</span></span>

[<span data-ttu-id="1efe1-191">Přehled prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="1efe1-191">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="1efe1-192">Zřízení prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="1efe1-192">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="1efe1-193">Nastavení volitelných funkcí pro prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="1efe1-193">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="1efe1-194">Často kladené dotazy k prostředí náhledu Commerce</span><span class="sxs-lookup"><span data-stu-id="1efe1-194">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="1efe1-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="1efe1-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="1efe1-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="1efe1-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="1efe1-197">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="1efe1-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="1efe1-198">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1efe1-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="1efe1-199">Zdroje nápovědy pro Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="1efe1-199">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)

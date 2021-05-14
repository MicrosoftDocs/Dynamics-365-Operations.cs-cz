---
title: Konfigurace prostředí vyhodnocení aplikace Dynamics 365 Commerce
description: Toto téma vysvětluje, jak konfigurovat prostředí vyhodnocení Microsoft Dynamics 365 Commerce poté, co je zřízeno.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b291a6515c6a3ae7382ea2ad8024ca036489de19
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937031"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="de646-103">Konfigurace prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de646-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de646-104">Toto téma vysvětluje, jak konfigurovat prostředí vyhodnocení Microsoft Dynamics 365 Commerce poté, co je zřízeno.</span><span class="sxs-lookup"><span data-stu-id="de646-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="de646-105">Postupy v tomto tématu dokončete až po zřízení prostředí vyhodnocení Commerce.</span><span class="sxs-lookup"><span data-stu-id="de646-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="de646-106">Informace o postupu zřízení prostředí vyhodnocení Commerce najdete v části [Zřízení prostředí vyhodnocení Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="de646-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="de646-107">Po kompletním zřízení prostředí vyhodnocení Commerce je nutné dokončit další kroky konfigurace po zřízení, aby bylo možné začít posuzovat prostředí.</span><span class="sxs-lookup"><span data-stu-id="de646-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="de646-108">K dokončení těchto kroků je nutné použít prostředí Lifecycle Services (LCS) Microsoft Dynamics a Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="de646-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="de646-109">Než začnete</span><span class="sxs-lookup"><span data-stu-id="de646-109">Before you start</span></span>

1. <span data-ttu-id="de646-110">Přihlaste se do [portálu LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="de646-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="de646-111">Přejděte na svůj projekt.</span><span class="sxs-lookup"><span data-stu-id="de646-111">Go to your project.</span></span>
1. <span data-ttu-id="de646-112">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="de646-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="de646-113">V seznamu vyberte své prostředí.</span><span class="sxs-lookup"><span data-stu-id="de646-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="de646-114">V informacích o prostředí vpravo vyberte **Přihlášení k prostředí**.</span><span class="sxs-lookup"><span data-stu-id="de646-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="de646-115">Budete posláni do centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="de646-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="de646-116">Ujistěte se, že je v pravém horním rohu vybrána právnická osoba **USRT**.</span><span class="sxs-lookup"><span data-stu-id="de646-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="de646-117">Během činností po zřízení v centrále Commerce se ujistěte, že právnická osoba **USRT** je vždy vybrána.</span><span class="sxs-lookup"><span data-stu-id="de646-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="de646-118">Konfigurace pokladního místa</span><span class="sxs-lookup"><span data-stu-id="de646-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="de646-119">Přidružení pracovníka k vaší identitě</span><span class="sxs-lookup"><span data-stu-id="de646-119">Associate a worker with your identity</span></span>

<span data-ttu-id="de646-120">Chcete-li pracovníka s vaší identitou přidružit, postupujte následovně v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="de646-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="de646-121">Pomocí nabídky vlevo přejděte na **Moduly \> Retail and commerce \> Zaměstnanci \> Pracovníci**.</span><span class="sxs-lookup"><span data-stu-id="de646-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="de646-122">V seznamu vyhledejte a vyberte následující záznam: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="de646-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="de646-123">V podokně akcí klikněte na možnost **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="de646-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="de646-124">Vyberte **Stávající identita přidružení**.</span><span class="sxs-lookup"><span data-stu-id="de646-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="de646-125">Do pole **E-mail** vpravo od **Hledání pomocí e-mailu** zadejte svou e-mailovou adresu.</span><span class="sxs-lookup"><span data-stu-id="de646-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="de646-126">Vyberte **Vyhledat**.</span><span class="sxs-lookup"><span data-stu-id="de646-126">Select **Search**.</span></span>
1. <span data-ttu-id="de646-127">Vyberte záznam obsahující vaše jméno.</span><span class="sxs-lookup"><span data-stu-id="de646-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="de646-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="de646-128">Select **OK**.</span></span>
1. <span data-ttu-id="de646-129">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="de646-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="de646-130">Aktivovat Cloud POS</span><span class="sxs-lookup"><span data-stu-id="de646-130">Activate Cloud POS</span></span>

<span data-ttu-id="de646-131">Chcete-li aktivovat Cloud POS, postupujte následovně v LCS.</span><span class="sxs-lookup"><span data-stu-id="de646-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="de646-132">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="de646-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="de646-133">V seznamu vyberte své prostředí.</span><span class="sxs-lookup"><span data-stu-id="de646-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="de646-134">V informacích o prostředí vpravo vyberte **Přihlášení ke cloudovému pokladnímu místu**.</span><span class="sxs-lookup"><span data-stu-id="de646-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="de646-135">Vyberte **Další**, chcete-li otevřít dialogové okno **Než začneš**.</span><span class="sxs-lookup"><span data-stu-id="de646-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="de646-136">Nechte pole **Adresa URL serveru** tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="de646-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="de646-137">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="de646-137">Select **Next**.</span></span>
1. <span data-ttu-id="de646-138">Přihlaste se pomocí účtu Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="de646-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="de646-139">Pro **Jméno obchodu** vyberte **San Francisco** a poté vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="de646-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="de646-140">V **Registr a zařízení** vyberte **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="de646-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="de646-141">Vyberte **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="de646-141">Select **Activate**.</span></span> <span data-ttu-id="de646-142">Jste přihlášeni a přesměrováni na přihlašovací stránku POS.</span><span class="sxs-lookup"><span data-stu-id="de646-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="de646-143">Nyní se můžete přihlásit ke cloudovému POS pomocí ID operátora **000713** a hesla **123**.</span><span class="sxs-lookup"><span data-stu-id="de646-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="de646-144">Nastavení webu v Commerce</span><span class="sxs-lookup"><span data-stu-id="de646-144">Set up your site in Commerce</span></span>

<span data-ttu-id="de646-145">Pokud chcete začít nastavovat web vyhodnocení v Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="de646-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="de646-146">Přihlaste se k nástroji pro tvorbu webu pomocí adresy URL, kterou jste si poznamenali při inicializaci e-Commerce během zřizování (viz [Inicializace e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="de646-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="de646-147">Vyberte web **Fabrikam** otevřete dialogové okno nastavení webu.</span><span class="sxs-lookup"><span data-stu-id="de646-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="de646-148">Vyberte doménu, kterou jste zadali při inicializaci platformy e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="de646-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="de646-149">Jako výchozí kanál vyberte **Rozšířený online obchod společnosti Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="de646-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="de646-150">(Zkontrolujte, zda jste vybrali **rozšířený** online obchod.)</span><span class="sxs-lookup"><span data-stu-id="de646-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="de646-151">Jako výchozí jazyk vyberte **en-us**.</span><span class="sxs-lookup"><span data-stu-id="de646-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="de646-152">Ponechte hodnotu pole **Cesta** tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="de646-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="de646-153">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="de646-153">Select **OK**.</span></span> <span data-ttu-id="de646-154">Zobrazí se seznam stránek na webu.</span><span class="sxs-lookup"><span data-stu-id="de646-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="de646-155">Povolit úlohy</span><span class="sxs-lookup"><span data-stu-id="de646-155">Enable jobs</span></span>

<span data-ttu-id="de646-156">Pokud chcete povolit úlohy v Commerce, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="de646-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="de646-157">Přihlaste se k prostředí (HQ).</span><span class="sxs-lookup"><span data-stu-id="de646-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="de646-158">Pomocí nabídky vlevo přejděte na **Retail and commerce \> Dotazy a sestavy \> Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="de646-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="de646-159">Zbývající kroky tohoto postupu musí být dokončeny pro každou z následujících úloh:</span><span class="sxs-lookup"><span data-stu-id="de646-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="de646-160">Zpracovat maloobchodní oznámení objednávky e-mailem</span><span class="sxs-lookup"><span data-stu-id="de646-160">Process retail order email notification</span></span>
    * <span data-ttu-id="de646-161">Dostupnost produktu</span><span class="sxs-lookup"><span data-stu-id="de646-161">Product availability</span></span>
    * <span data-ttu-id="de646-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="de646-162">P-0001</span></span>
    * <span data-ttu-id="de646-163">Synchronizovat úlohu objednávek</span><span class="sxs-lookup"><span data-stu-id="de646-163">Synchronize orders job</span></span>

1. <span data-ttu-id="de646-164">Pomocí rychlého filtru vyhledejte úlohu podle názvu.</span><span class="sxs-lookup"><span data-stu-id="de646-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="de646-165">Je-li stav úlohy nastaven na **Probíhající**, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="de646-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="de646-166">Vybrat záznam.</span><span class="sxs-lookup"><span data-stu-id="de646-166">Select the record.</span></span>
    1. <span data-ttu-id="de646-167">V podokně akcí na kartě **Dávková úloha** vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="de646-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="de646-168">Vyberte **Ruší se** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="de646-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="de646-169">Volitelně můžete také nastavit interval opakování na jednu (1) minutu pro následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="de646-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="de646-170">Zpracovat úlohu maloobchodního oznámení objednávky e-mailem</span><span class="sxs-lookup"><span data-stu-id="de646-170">Process retail order email notification job</span></span>
* <span data-ttu-id="de646-171">úloha P-0001</span><span class="sxs-lookup"><span data-stu-id="de646-171">P-0001 job</span></span>
* <span data-ttu-id="de646-172">Synchronizovat úlohu objednávek</span><span class="sxs-lookup"><span data-stu-id="de646-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="de646-173">Spustit úplnou synchronizaci dat</span><span class="sxs-lookup"><span data-stu-id="de646-173">Run full data synchronization</span></span>

<span data-ttu-id="de646-174">Chcete-li spustit úplnou synchronizaci dat v Commerce, postupujte takto v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="de646-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="de646-175">Pomocí nabídky vlevo přejděte na **Moduly \> Retail and commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Databáze kanálů**.</span><span class="sxs-lookup"><span data-stu-id="de646-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="de646-176">Vyberte kanál, který je nazvaný **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="de646-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="de646-177">V podokně akcí vyberte **Úplná synchronizace dat**.</span><span class="sxs-lookup"><span data-stu-id="de646-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="de646-178">Jako plán distribuce zadejte **9999**.</span><span class="sxs-lookup"><span data-stu-id="de646-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="de646-179">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="de646-179">Select **OK**.</span></span>
1. <span data-ttu-id="de646-180">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="de646-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="de646-181">Testování informací o kreditní kartě za účelem provedení zkušebních nákupů</span><span class="sxs-lookup"><span data-stu-id="de646-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="de646-182">Chcete-li provést zkušební transakce na webu, můžete použít následující testovací kreditní kartu:</span><span class="sxs-lookup"><span data-stu-id="de646-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="de646-183">**Číslo karty:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="de646-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="de646-184">**Datum konce platnosti:** 10/20</span><span class="sxs-lookup"><span data-stu-id="de646-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="de646-185">**Ověřovací hodnota platební karty (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="de646-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de646-186">V žádném případě byste neměli používat informace o skutečné kreditní kartě na testovacím webu.</span><span class="sxs-lookup"><span data-stu-id="de646-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="de646-187">Další kroky</span><span class="sxs-lookup"><span data-stu-id="de646-187">Next steps</span></span>

<span data-ttu-id="de646-188">Po dokončení postupu zřizování a konfigurace můžete začít používat prostředí vyhodnocení.</span><span class="sxs-lookup"><span data-stu-id="de646-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="de646-189">Pomocí adresy URL nástroje pro tvorbu webu Commerce můžete přejít na práci s vytvářením.</span><span class="sxs-lookup"><span data-stu-id="de646-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="de646-190">Pomocí adresy URL webu Commerce přejděte do prostředí webu zákazníka maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="de646-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="de646-191">Pokud chcete provést konfiguraci volitelných funkcí prostředí vyhodnocení Commerce, najdete informace v části [konfigurace volitelných funkcí prostředí vyhodnocení Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="de646-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de646-192">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="de646-192">Additional resources</span></span>

[<span data-ttu-id="de646-193">Přehled prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de646-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="de646-194">Zřízení prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de646-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="de646-195">Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de646-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="de646-196">Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de646-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="de646-197">Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de646-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="de646-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="de646-198">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="de646-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="de646-199">Retail Cloud Scale Unit (RCSU)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="de646-200">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="de646-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="de646-201">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de646-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
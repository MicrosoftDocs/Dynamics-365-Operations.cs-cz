---
title: Konfigurace prostředí vyhodnocení Dynamics 365 Commerce
description: Toto téma vysvětluje, jak konfigurovat prostředí vyhodnocení Microsoft Dynamics 365 Commerce poté, co je zřízeno.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fa92a581a96de6bed26b4a0c6601ebd9d5088347
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993418"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="575a9-103">Konfigurace prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="575a9-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="575a9-104">Toto téma vysvětluje, jak konfigurovat prostředí vyhodnocení Microsoft Dynamics 365 Commerce poté, co je zřízeno.</span><span class="sxs-lookup"><span data-stu-id="575a9-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="575a9-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="575a9-105">Overview</span></span>

<span data-ttu-id="575a9-106">Postupy v tomto tématu dokončete až po zřízení prostředí vyhodnocení Commerce.</span><span class="sxs-lookup"><span data-stu-id="575a9-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="575a9-107">Informace o postupu zřízení prostředí vyhodnocení Commerce najdete v části [Zřízení prostředí vyhodnocení Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="575a9-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="575a9-108">Po kompletním zřízení prostředí vyhodnocení Commerce je nutné dokončit další kroky konfigurace po zřízení, aby bylo možné začít posuzovat prostředí.</span><span class="sxs-lookup"><span data-stu-id="575a9-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="575a9-109">K dokončení těchto kroků je nutné použít prostředí Lifecycle Services (LCS) Microsoft Dynamics a Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="575a9-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="575a9-110">Než začnete</span><span class="sxs-lookup"><span data-stu-id="575a9-110">Before you start</span></span>

1. <span data-ttu-id="575a9-111">Přihlaste se do [portálu LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="575a9-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="575a9-112">Přejděte na svůj projekt.</span><span class="sxs-lookup"><span data-stu-id="575a9-112">Go to your project.</span></span>
1. <span data-ttu-id="575a9-113">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="575a9-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="575a9-114">V seznamu vyberte své prostředí.</span><span class="sxs-lookup"><span data-stu-id="575a9-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="575a9-115">V informacích o prostředí vpravo vyberte **Přihlášení k prostředí**.</span><span class="sxs-lookup"><span data-stu-id="575a9-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="575a9-116">Budete posláni do centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="575a9-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="575a9-117">Ujistěte se, že je v pravém horním rohu vybrána právnická osoba **USRT**.</span><span class="sxs-lookup"><span data-stu-id="575a9-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="575a9-118">Během činností po zřízení v centrále Commerce se ujistěte, že právnická osoba **USRT** je vždy vybrána.</span><span class="sxs-lookup"><span data-stu-id="575a9-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="575a9-119">Konfigurace pokladního místa</span><span class="sxs-lookup"><span data-stu-id="575a9-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="575a9-120">Přidružení pracovníka k vaší identitě</span><span class="sxs-lookup"><span data-stu-id="575a9-120">Associate a worker with your identity</span></span>

<span data-ttu-id="575a9-121">Chcete-li pracovníka s vaší identitou přidružit, postupujte následovně v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="575a9-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="575a9-122">Pomocí nabídky vlevo přejděte na **Moduly \> Retail and commerce \> Zaměstnanci \> Pracovníci**.</span><span class="sxs-lookup"><span data-stu-id="575a9-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="575a9-123">V seznamu vyhledejte a vyberte následující záznam: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="575a9-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="575a9-124">V podokně akcí klikněte na možnost **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="575a9-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="575a9-125">Vyberte **Stávající identita přidružení**.</span><span class="sxs-lookup"><span data-stu-id="575a9-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="575a9-126">Do pole **E-mail** vpravo od **Hledání pomocí e-mailu** zadejte svou e-mailovou adresu.</span><span class="sxs-lookup"><span data-stu-id="575a9-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="575a9-127">Vyberte **Vyhledat**.</span><span class="sxs-lookup"><span data-stu-id="575a9-127">Select **Search**.</span></span>
1. <span data-ttu-id="575a9-128">Vyberte záznam obsahující vaše jméno.</span><span class="sxs-lookup"><span data-stu-id="575a9-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="575a9-129">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="575a9-129">Select **OK**.</span></span>
1. <span data-ttu-id="575a9-130">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="575a9-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="575a9-131">Aktivovat Cloud POS</span><span class="sxs-lookup"><span data-stu-id="575a9-131">Activate Cloud POS</span></span>

<span data-ttu-id="575a9-132">Chcete-li aktivovat Cloud POS, postupujte následovně v LCS.</span><span class="sxs-lookup"><span data-stu-id="575a9-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="575a9-133">V horní nabídce vyberte možnost **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="575a9-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="575a9-134">V seznamu vyberte své prostředí.</span><span class="sxs-lookup"><span data-stu-id="575a9-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="575a9-135">V informacích o prostředí vpravo vyberte **Přihlášení ke cloudovému pokladnímu místu**.</span><span class="sxs-lookup"><span data-stu-id="575a9-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="575a9-136">Vyberte **Další**, chcete-li otevřít dialogové okno **Než začneš**.</span><span class="sxs-lookup"><span data-stu-id="575a9-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="575a9-137">Nechte pole **Adresa URL serveru** tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="575a9-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="575a9-138">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="575a9-138">Select **Next**.</span></span>
1. <span data-ttu-id="575a9-139">Přihlaste se pomocí účtu Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="575a9-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="575a9-140">Pro **Jméno obchodu** vyberte **San Francisco** a poté vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="575a9-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="575a9-141">V **Registr a zařízení** vyberte **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="575a9-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="575a9-142">Vyberte **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="575a9-142">Select **Activate**.</span></span> <span data-ttu-id="575a9-143">Jste přihlášeni a přesměrováni na přihlašovací stránku POS.</span><span class="sxs-lookup"><span data-stu-id="575a9-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="575a9-144">Nyní se můžete přihlásit ke cloudovému POS pomocí ID operátora **000713** a hesla **123**.</span><span class="sxs-lookup"><span data-stu-id="575a9-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="575a9-145">Nastavení webu v Commerce</span><span class="sxs-lookup"><span data-stu-id="575a9-145">Set up your site in Commerce</span></span>

<span data-ttu-id="575a9-146">Pokud chcete začít nastavovat web vyhodnocení v Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="575a9-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="575a9-147">Přihlaste se k nástroji pro tvorbu webu pomocí adresy URL, kterou jste si poznamenali při inicializaci e-Commerce během zřizování (viz [Inicializace e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="575a9-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="575a9-148">Vyberte web **Fabrikam** otevřete dialogové okno nastavení webu.</span><span class="sxs-lookup"><span data-stu-id="575a9-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="575a9-149">Vyberte doménu, kterou jste zadali při inicializaci platformy e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="575a9-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="575a9-150">Jako výchozí kanál vyberte **Rozšířený online obchod společnosti Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="575a9-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="575a9-151">(Zkontrolujte, zda jste vybrali **rozšířený** online obchod.)</span><span class="sxs-lookup"><span data-stu-id="575a9-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="575a9-152">Jako výchozí jazyk vyberte **en-us**.</span><span class="sxs-lookup"><span data-stu-id="575a9-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="575a9-153">Ponechte hodnotu pole **Cesta** tak, jak je.</span><span class="sxs-lookup"><span data-stu-id="575a9-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="575a9-154">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="575a9-154">Select **OK**.</span></span> <span data-ttu-id="575a9-155">Zobrazí se seznam stránek na webu.</span><span class="sxs-lookup"><span data-stu-id="575a9-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="575a9-156">Povolit úlohy</span><span class="sxs-lookup"><span data-stu-id="575a9-156">Enable jobs</span></span>

<span data-ttu-id="575a9-157">Pokud chcete povolit úlohy v Commerce, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="575a9-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="575a9-158">Přihlaste se k prostředí (HQ).</span><span class="sxs-lookup"><span data-stu-id="575a9-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="575a9-159">Pomocí nabídky vlevo přejděte na **Retail and commerce \> Dotazy a sestavy \> Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="575a9-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="575a9-160">Zbývající kroky tohoto postupu musí být dokončeny pro každou z následujících úloh:</span><span class="sxs-lookup"><span data-stu-id="575a9-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="575a9-161">Zpracovat maloobchodní oznámení objednávky e-mailem</span><span class="sxs-lookup"><span data-stu-id="575a9-161">Process retail order email notification</span></span>
    * <span data-ttu-id="575a9-162">Dostupnost produktu</span><span class="sxs-lookup"><span data-stu-id="575a9-162">Product availability</span></span>
    * <span data-ttu-id="575a9-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="575a9-163">P-0001</span></span>
    * <span data-ttu-id="575a9-164">Synchronizovat úlohu objednávek</span><span class="sxs-lookup"><span data-stu-id="575a9-164">Synchronize orders job</span></span>

1. <span data-ttu-id="575a9-165">Pomocí rychlého filtru vyhledejte úlohu podle názvu.</span><span class="sxs-lookup"><span data-stu-id="575a9-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="575a9-166">Je-li stav úlohy nastaven na **Probíhající**, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="575a9-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="575a9-167">Vybrat záznam.</span><span class="sxs-lookup"><span data-stu-id="575a9-167">Select the record.</span></span>
    1. <span data-ttu-id="575a9-168">V podokně akcí na kartě **Dávková úloha** vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="575a9-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="575a9-169">Vyberte **Ruší se** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="575a9-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="575a9-170">Volitelně můžete také nastavit interval opakování na jednu (1) minutu pro následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="575a9-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="575a9-171">Zpracovat úlohu maloobchodního oznámení objednávky e-mailem</span><span class="sxs-lookup"><span data-stu-id="575a9-171">Process retail order email notification job</span></span>
* <span data-ttu-id="575a9-172">úloha P-0001</span><span class="sxs-lookup"><span data-stu-id="575a9-172">P-0001 job</span></span>
* <span data-ttu-id="575a9-173">Synchronizovat úlohu objednávek</span><span class="sxs-lookup"><span data-stu-id="575a9-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="575a9-174">Spustit úplnou synchronizaci dat</span><span class="sxs-lookup"><span data-stu-id="575a9-174">Run full data synchronization</span></span>

<span data-ttu-id="575a9-175">Chcete-li spustit úplnou synchronizaci dat v Commerce, postupujte takto v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="575a9-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="575a9-176">Pomocí nabídky vlevo přejděte na **Moduly \> Retail and commerce \> Nastavení centrály \> Plánovač velkoobchodu \> Databáze kanálů**.</span><span class="sxs-lookup"><span data-stu-id="575a9-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="575a9-177">Vyberte kanál, který je nazvaný **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="575a9-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="575a9-178">V podokně akcí vyberte **Úplná synchronizace dat**.</span><span class="sxs-lookup"><span data-stu-id="575a9-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="575a9-179">Jako plán distribuce zadejte **9999**.</span><span class="sxs-lookup"><span data-stu-id="575a9-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="575a9-180">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="575a9-180">Select **OK**.</span></span>
1. <span data-ttu-id="575a9-181">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="575a9-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="575a9-182">Testování informací o kreditní kartě za účelem provedení zkušebních nákupů</span><span class="sxs-lookup"><span data-stu-id="575a9-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="575a9-183">Chcete-li provést zkušební transakce na webu, můžete použít následující testovací kreditní kartu:</span><span class="sxs-lookup"><span data-stu-id="575a9-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="575a9-184">**Číslo karty:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="575a9-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="575a9-185">**Datum konce platnosti:** 10/20</span><span class="sxs-lookup"><span data-stu-id="575a9-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="575a9-186">**Ověřovací hodnota platební karty (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="575a9-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="575a9-187">V žádném případě byste neměli používat informace o skutečné kreditní kartě na testovacím webu.</span><span class="sxs-lookup"><span data-stu-id="575a9-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="575a9-188">Další kroky</span><span class="sxs-lookup"><span data-stu-id="575a9-188">Next steps</span></span>

<span data-ttu-id="575a9-189">Po dokončení postupu zřizování a konfigurace můžete začít používat prostředí vyhodnocení.</span><span class="sxs-lookup"><span data-stu-id="575a9-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="575a9-190">Pomocí adresy URL nástroje pro tvorbu webu Commerce můžete přejít na práci s vytvářením.</span><span class="sxs-lookup"><span data-stu-id="575a9-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="575a9-191">Pomocí adresy URL webu Commerce přejděte do prostředí webu zákazníka maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="575a9-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="575a9-192">Pokud chcete provést konfiguraci volitelných funkcí prostředí vyhodnocení Commerce, najdete informace v části [konfigurace volitelných funkcí prostředí vyhodnocení Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="575a9-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="575a9-193">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="575a9-193">Additional resources</span></span>

[<span data-ttu-id="575a9-194">Přehled prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="575a9-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="575a9-195">Zřízení prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="575a9-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="575a9-196">Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="575a9-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="575a9-197">Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="575a9-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="575a9-198">Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="575a9-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="575a9-199">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="575a9-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="575a9-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="575a9-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="575a9-201">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="575a9-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="575a9-202">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="575a9-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

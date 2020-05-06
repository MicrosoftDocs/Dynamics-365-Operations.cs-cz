---
title: Konfigurace „Nákup online, vyzvednutí v obchodě“ (BOPIS) v prostředí Dynamics 365 Commerce
description: Tohle téma vysvětluje, jak konfigurovat proces „nákup online, vyzvednutí v obchodě“ (BOPIS) v prostředí Microsoft Dynamics 365 Commerce po jeho zřízení.
author: rubendel
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 956d66d09885d4d54655ce25b3aa7ba6a9c34cf4
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282789"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="de345-103">Konfigurace „Nákup online, vyzvednutí v obchodě“ (BOPIS) v prostředí Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de345-103">Configure BOPIS in a Dynamics 365 Commerce environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="de345-104">Tohle téma vysvětluje, jak konfigurovat proces „nákup online, vyzvednutí v obchodě“ (BOPIS) v prostředí Microsoft Dynamics 365 Commerce po zřízení tohoto prostředí.</span><span class="sxs-lookup"><span data-stu-id="de345-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="de345-105">Předpoklad</span><span class="sxs-lookup"><span data-stu-id="de345-105">Prerequisite</span></span>

<span data-ttu-id="de345-106">Postupy v tomto tématu dokončete až po zřízení a konfiguraci prostředí Commerce verze Preview.</span><span class="sxs-lookup"><span data-stu-id="de345-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned and configured.</span></span> <span data-ttu-id="de345-107">Informace o zřízení a konfiguraci prostředí viz [Zřízení prostředí Preview aplikace Dynamics 365 Commerce](provisioning-guide.md) a [Konfigurace prostředí Preview aplikace Dynamics 365 Commerce](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="de345-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce preview environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce preview environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="de345-108">Po kompletním zřízení a konfiguraci prostředí Commerce můžete pomocí tohoto tématu povolit scénáře BOPIS.</span><span class="sxs-lookup"><span data-stu-id="de345-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="de345-109">Konfigurace POS</span><span class="sxs-lookup"><span data-stu-id="de345-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="de345-110">Konfigurace Modern POS</span><span class="sxs-lookup"><span data-stu-id="de345-110">Configure Modern POS</span></span>

<span data-ttu-id="de345-111">Scénáře BOPIS, které zahrnují platbu kreditní kartou, vyžadují hardwarovou stanici.</span><span class="sxs-lookup"><span data-stu-id="de345-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="de345-112">Hardwarová stanice je součástí klientů Modern POS pro Windows a Android.</span><span class="sxs-lookup"><span data-stu-id="de345-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="de345-113">Používáte-li Cloud POS nebo Modern POS pro iOS, musí být pokladní místo (POS) spárováno se sdílenou hardwarovou stanicí.</span><span class="sxs-lookup"><span data-stu-id="de345-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="de345-114">Toto téma vysvětluje, jak konfigurovat BOPIS pro klienty Windows a Android.</span><span class="sxs-lookup"><span data-stu-id="de345-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="de345-115">Informace o nastavení sdílené hardwarové stanice viz [Konfigurace a instalace maloobchodní hardwarové stanice](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="de345-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="de345-116">Přejděte na **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> Pokladny**.</span><span class="sxs-lookup"><span data-stu-id="de345-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="de345-117">Vyberte pokladnu **SANFRAN-5** a pak vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="de345-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="de345-118">Změňte hodnotu v poli **Hardwarový profil** z **HW002** na **HW001** a pak vyberte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="de345-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="de345-119">Abyste změny synchronizovali, přejděte na **Retail a Commerce \> IT pro Retail a Commerce \> Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="de345-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="de345-120">Vyberte plán distribuce **1090** a poté v podokně akcí vyberte možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="de345-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="de345-121">Vyberte možnost **Ano** a poté **OK**, abyste zahájili synchronizaci dat.</span><span class="sxs-lookup"><span data-stu-id="de345-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="de345-122">Instalace Modern POS</span><span class="sxs-lookup"><span data-stu-id="de345-122">Install Modern POS</span></span>

1. <span data-ttu-id="de345-123">Přejděte na **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> Zařízení**.</span><span class="sxs-lookup"><span data-stu-id="de345-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="de345-124">Vyberte zařízení **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="de345-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="de345-125">V podokně akcí zvolte **Stáhnout** a poté vyberte **Konfigurační soubor**.</span><span class="sxs-lookup"><span data-stu-id="de345-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="de345-126">Vyberte možnost **Stáhnout** a pak možnost **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="de345-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="de345-127">Po stažení souboru **ModernPOSSetup.exe** vyberte možnost **Otevřít soubor**.</span><span class="sxs-lookup"><span data-stu-id="de345-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Otevřít soubor](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="de345-129">Chcete-li projít instalačním procesem, vyberte možnost **Další**.</span><span class="sxs-lookup"><span data-stu-id="de345-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="de345-130">Po dokončení instalace vyberte možnost **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="de345-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="de345-131">Aktivace Modern POS</span><span class="sxs-lookup"><span data-stu-id="de345-131">Activate Modern POS</span></span>

1. <span data-ttu-id="de345-132">Na ploše systému Windows vyberte tlačítko **Start** a zadejte příkaz **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="de345-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="de345-133">Vyberte aplikaci **Retail Modern POS**, která zahájí aktivaci.</span><span class="sxs-lookup"><span data-stu-id="de345-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="de345-134">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="de345-134">Select **Next**.</span></span> <span data-ttu-id="de345-135">Pole **Adresa URL serveru**, **ID zařízení** a **Číslo pokladny** by měla být přednastavena pomocí informací z konfiguračního souboru, který jste stáhli v předchozí proceduře.</span><span class="sxs-lookup"><span data-stu-id="de345-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="de345-136">Vyberte **Aktivovat**.</span><span class="sxs-lookup"><span data-stu-id="de345-136">Select **Activate**.</span></span>
5. <span data-ttu-id="de345-137">Zobrazí se dialogové okno ověření.</span><span class="sxs-lookup"><span data-stu-id="de345-137">An authentication dialog box appears.</span></span> <span data-ttu-id="de345-138">Vyberte účet, který používá e-mailovou adresu, která byla dříve přidružena k pracovníkovi **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="de345-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de345-139">Pokud jste pracovníka s vaší identitou ještě nevytvořili, nebude aktivace úspěšná.</span><span class="sxs-lookup"><span data-stu-id="de345-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="de345-140">V takovém případě postupujte podle kroků v části „Přidružení pracovníka k vaší identitě“ v tématu [Konfigurace prostředí Preview aplikace Dynamics 365 Commerce](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="de345-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce preview environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="de345-141">Když se zobrazí výzva k povolení správy zařízení vaší organizací, vyberte **Pouze tato aplikace**.</span><span class="sxs-lookup"><span data-stu-id="de345-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="de345-142">Po dokončení aktivace vyberte možnost **Začít**.</span><span class="sxs-lookup"><span data-stu-id="de345-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="de345-143">Povolení BOPIS v Modern POS</span><span class="sxs-lookup"><span data-stu-id="de345-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="de345-144">Přihlaste se ke Modern POS s pomocí **000713** jako ID operátora a **123** jako hesla.</span><span class="sxs-lookup"><span data-stu-id="de345-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="de345-145">Když se přehrává úvodní návod, zaškrtněte obě políčka v levém dolním rohu dialogového okna a poté dialogové okno zavřete.</span><span class="sxs-lookup"><span data-stu-id="de345-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="de345-146">Nejste-li vyzváni k uzavření směny, posuňte se na **uvítací** stránce doprava, vyberte možnost **Zavřít směnu** a opět se přihlaste do POS.</span><span class="sxs-lookup"><span data-stu-id="de345-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="de345-147">Při výzvě vyberte možnost **Provést operace bez zásuvky**.</span><span class="sxs-lookup"><span data-stu-id="de345-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="de345-148">Na **uvítací** stránce se přesuňte doprava a vyberte operaci **Vybrat hardwarovou stanici**.</span><span class="sxs-lookup"><span data-stu-id="de345-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="de345-149">Vyberte **Spravovat**, nastavte možnost **Použít hardwarovou stanici** do polohy **Zapnuto** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="de345-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="de345-150">Odhlaste se ze systému POS a znovu se přihlaste.</span><span class="sxs-lookup"><span data-stu-id="de345-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="de345-151">Po přihlášení vyberte možnost **Otevřít novou směnu**a pak vyberte možnost **Zásuvka**.</span><span class="sxs-lookup"><span data-stu-id="de345-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="de345-152">Dokončení scénáře BOPIS</span><span class="sxs-lookup"><span data-stu-id="de345-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="de345-153">Vytvoření objednávky výkladní skříně pro výdej na skladě</span><span class="sxs-lookup"><span data-stu-id="de345-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="de345-154">Přejděte na adresu URL, kterou jste zadali v kroku [Inicializace e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) během konfigurace prostředí.</span><span class="sxs-lookup"><span data-stu-id="de345-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="de345-155">Vyberte položku a vyberte možnost **Přidat do nákupního košíku**.</span><span class="sxs-lookup"><span data-stu-id="de345-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="de345-156">Na stránce nákupní tašky vyberte položku **Vyzvednout** pro řádek objednávky, který jste právě přidali.</span><span class="sxs-lookup"><span data-stu-id="de345-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="de345-157">V dialogovém okně **Vyberte úložiště** zadejte hodnotu **San Francisco** a pak vyberte tlačítko **Hledat**.</span><span class="sxs-lookup"><span data-stu-id="de345-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="de345-158">V seznamu výsledků vyhledejte úložiště San Francisco a vyberte **Vyzvednout zde**.</span><span class="sxs-lookup"><span data-stu-id="de345-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="de345-159">Na stránce nákupní tašky vyberte možnost **Přejít k pokladně jako host**.</span><span class="sxs-lookup"><span data-stu-id="de345-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="de345-160">Chcete-li pokračovat k pokladně, je nutné potvrdit oznámení o souboru cookie.</span><span class="sxs-lookup"><span data-stu-id="de345-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="de345-161">Toto oznámení je zobrazeno v pruhu v horní části stránky pokladny.</span><span class="sxs-lookup"><span data-stu-id="de345-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="de345-162">Pro metodu platby platební kartou zadejte následující údaje:</span><span class="sxs-lookup"><span data-stu-id="de345-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="de345-163">**Jméno držitele karty**: zadejte libovolné jméno.</span><span class="sxs-lookup"><span data-stu-id="de345-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="de345-164">**Číslo karty:** zadejte **4111-1111-1111-1111**.</span><span class="sxs-lookup"><span data-stu-id="de345-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="de345-165">**Datum vypršení platnosti:** zadejte **10/20**.</span><span class="sxs-lookup"><span data-stu-id="de345-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="de345-166">**Ověřovací hodnota platební karty (CVV)**: zadejte **737**.</span><span class="sxs-lookup"><span data-stu-id="de345-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="de345-167">V žádném případě byste neměli používat informace o skutečné kreditní kartě na testovacím webu.</span><span class="sxs-lookup"><span data-stu-id="de345-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="de345-168">Pokračujte v placení zadáním fakturační adresy a pak vyberte možnost **Uložit a pokračovat**.</span><span class="sxs-lookup"><span data-stu-id="de345-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="de345-169">Jakmile bude objednávka připravena k podání, vyberte možnost **Pokladna**.</span><span class="sxs-lookup"><span data-stu-id="de345-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="de345-170">Synchronizace online objednávek s administrativní podporou</span><span class="sxs-lookup"><span data-stu-id="de345-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="de345-171">Informace o synchronizaci online objednávek naleznete v tématu [Zaúčtování online prodeje a plateb](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="de345-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="de345-172">Vyzvednutí objednávky v obchodě</span><span class="sxs-lookup"><span data-stu-id="de345-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="de345-173">Přihlaste se k systému POS.</span><span class="sxs-lookup"><span data-stu-id="de345-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="de345-174">Na **úvodní** obrazovce vyberte možnost **Plnění objednávek**.</span><span class="sxs-lookup"><span data-stu-id="de345-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="de345-175">V seznamu položek pro výdej vyberte řádek z objednávky, která byla podána online.</span><span class="sxs-lookup"><span data-stu-id="de345-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="de345-176">Zatímco je vybrán řádek objednávky, vyberte možnost **Vyzvednout**.</span><span class="sxs-lookup"><span data-stu-id="de345-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="de345-177">Položka řádku se přidá na obrazovku transakce a **$0,00** se zobrazí jako splatný zůstatek.</span><span class="sxs-lookup"><span data-stu-id="de345-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="de345-178">Vyberte splatný zůstatek **$0,00**nebo vyberte libovolný způsob platby k uzavření transakce.</span><span class="sxs-lookup"><span data-stu-id="de345-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="de345-179">Řešení potíží</span><span class="sxs-lookup"><span data-stu-id="de345-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="de345-180">Online objednávky načtené v POS mají nenulový splatný zůstatek.</span><span class="sxs-lookup"><span data-stu-id="de345-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="de345-181">Pokud je pro výdej v obchodě načtena objednávka, pokud splatné zůstatky nejsou 0 (nula), zkontrolujte, zda je používán Modern POS a zda je hardwarová stanice aktivní.</span><span class="sxs-lookup"><span data-stu-id="de345-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="de345-182">Pokud používáte Cloud POS nebo Modern POS pro iOS, ujistěte se, že je sdílená hardwarová stanice aktivní.</span><span class="sxs-lookup"><span data-stu-id="de345-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="de345-183">K načtení plateb, které byly provedeny v režimu online, je nutná nějaká forma aktivní hardwarové stanice.</span><span class="sxs-lookup"><span data-stu-id="de345-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="de345-184">Obecné problémy se záznamem platby</span><span class="sxs-lookup"><span data-stu-id="de345-184">General issues with payment capture</span></span>

<span data-ttu-id="de345-185">V případě všech obecných problémů byste jako první věc měli vždy prostudovat protokoly událostí hardwarových stanic pro Modern POS nebo službu IIS (Internet Information Services).</span><span class="sxs-lookup"><span data-stu-id="de345-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="de345-186">Tyto protokoly naleznete v následujících uzlech v protokolu událostí systému Windows:</span><span class="sxs-lookup"><span data-stu-id="de345-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="de345-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="de345-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="de345-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="de345-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de345-189">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="de345-189">Additional resources</span></span>

[<span data-ttu-id="de345-190">Přehled prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de345-190">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="de345-191">Zřízení prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de345-191">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="de345-192">Konfigurace volitelných funkcí pro prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de345-192">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="de345-193">Často kladené dotazy k prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de345-193">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="de345-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="de345-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="de345-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="de345-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="de345-196">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="de345-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="de345-197">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de345-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="de345-198">Konektor platby Adyen</span><span class="sxs-lookup"><span data-stu-id="de345-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="de345-199">Úspora nástrojů online plateb s konektorem Adyen</span><span class="sxs-lookup"><span data-stu-id="de345-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="de345-200">Přehled omnikanálových plateb</span><span class="sxs-lookup"><span data-stu-id="de345-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)

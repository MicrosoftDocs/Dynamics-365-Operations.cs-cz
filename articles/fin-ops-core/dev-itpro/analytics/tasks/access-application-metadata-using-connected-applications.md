---
title: Přístup k metadatům aplikace pomocí připojených aplikací
description: Kroky v tomto tématu vysvětlují, jak může uživatel služby Regulatory Configuration Service navrhnout nové mapování modelu elektronického výkaznictví (ER) pomocí metadat.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457d5760fb704b7a93ce16c081b7c5e6d0ff19c1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093323"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="727da-103">Přístup k metadatům aplikace pomocí připojených aplikací</span><span class="sxs-lookup"><span data-stu-id="727da-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="727da-104">Následující kroky vysvětlují, jak může uživatel služby Regulatory Configuration Service s rolí Správce systému nebo Návrhář elektronického výkaznictví navrhnout nové mapování modelu elektronického výkaznictví (ER) pomocí metadat v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="727da-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="727da-105">Přístup k metadatům aplikace bude probíhat online pomocí aplikace připojené k RCS.</span><span class="sxs-lookup"><span data-stu-id="727da-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="727da-106">Mapování modelu ER bude konfigurováno pro přístup k transakcím zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="727da-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="727da-107">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="727da-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="727da-108">Pokud jste nedokončili kroky uvedené v tématu [Přístup k metadatům aplikace pomocí konfigurace ER](access-application-metadata-er-configuration.md), přejděte na stránku [Příklady elektronického výkaznictví](https://go.microsoft.com/fwlink/?linkid=862266) a stáhněte a uložte následující konfigurace ER: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml a dokončete kroky v postupu.</span><span class="sxs-lookup"><span data-stu-id="727da-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="727da-109">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="727da-109">Prerequisites</span></span>
1. <span data-ttu-id="727da-110">Přejděte na **Všechny pracovní prostory** > **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="727da-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="727da-111">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="727da-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="727da-112">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="727da-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="727da-113">Získání požadovaných konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="727da-113">Get required ER configurations</span></span>
1. <span data-ttu-id="727da-114">Klikněte na **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="727da-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="727da-115">Pokud jste již provedli kroky v části [Přístup k metadatům aplikace pomocí konfigurace ER](access-application-metadata-er-configuration.md), již máte v aktuální instanci RCS všechny potřebné konfigurace ER (konfigurace metadat pro zahraniční obchod, model a mapování).</span><span class="sxs-lookup"><span data-stu-id="727da-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="727da-116">Zbývající kroky tohoto dílčího úkolu můžete vynechat.</span><span class="sxs-lookup"><span data-stu-id="727da-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="727da-117">Klikněte na **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="727da-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="727da-118">Klikněte na **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="727da-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="727da-119">Klikněte na **Procházet** a vyberte soubor **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="727da-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="727da-120">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="727da-120">Click **OK**.</span></span> 
7. <span data-ttu-id="727da-121">Klikněte na **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="727da-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="727da-122">Klikněte na **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="727da-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="727da-123">Klikněte na **Procházet** a vyberte soubor **Foreign trade model.xml**.</span><span class="sxs-lookup"><span data-stu-id="727da-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="727da-124">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="727da-124">Click **OK**.</span></span> 
11. <span data-ttu-id="727da-125">Klikněte na **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="727da-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="727da-126">Klikněte na **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="727da-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="727da-127">Klikněte na **Procházet** a vyberte soubor **Foreign trade mapping.xml**.</span><span class="sxs-lookup"><span data-stu-id="727da-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="727da-128">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="727da-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="727da-129">Registrace připojené aplikace</span><span class="sxs-lookup"><span data-stu-id="727da-129">Register a connected application</span></span>
1. <span data-ttu-id="727da-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="727da-130">Close the page.</span></span> 
2. <span data-ttu-id="727da-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="727da-131">Close the page.</span></span> 
3. <span data-ttu-id="727da-132">Přejděte na **Všechny pracovní prostory** > **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="727da-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="727da-133">Klikněte na **Připojené aplikace**.</span><span class="sxs-lookup"><span data-stu-id="727da-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="727da-134">Ujistěte se, že konfigurovaná aplikace založená na Azure založena a přístupná pro aktuálního uživatele RCS.</span><span class="sxs-lookup"><span data-stu-id="727da-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="727da-135">Rovněž je nutné, aby aktuální uživatel RCS měl přístup k vybrané aplikaci a byl zaregistrován jako uživatel této aplikace, který má roli poskytující oprávnění pro přístup k metadatům aplikace.</span><span class="sxs-lookup"><span data-stu-id="727da-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving them privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="727da-136">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="727da-136">Click **New**.</span></span> 
7. <span data-ttu-id="727da-137">Do pole **Název** zadejte 'MyConnectedApp'.</span><span class="sxs-lookup"><span data-stu-id="727da-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="727da-138">Do pole **Aplikace** zadejte https:// mycompany.operations.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="727da-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="727da-139">Do pole **Klient** zadejte ‘mycompany.onmicrosoft.com’.</span><span class="sxs-lookup"><span data-stu-id="727da-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="727da-140">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="727da-140">Click **Save**.</span></span> 
11. <span data-ttu-id="727da-141">Při kontrole připojení ke konfigurované aplikaci klikněte na stránce **Připojit ke vzdálené aplikaci na** odkaz **Kliknutím sem se připojte k vybrané aplikaci**.</span><span class="sxs-lookup"><span data-stu-id="727da-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="727da-142">Klikněte na **Zkontrolovat připojení**.</span><span class="sxs-lookup"><span data-stu-id="727da-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="727da-143">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="727da-143">Click **Close**.</span></span> 
14. <span data-ttu-id="727da-144">Po úspěšném ověření připojení budou podrobnosti o verzi a tenantu aktualizovány pro konfigurovanou aplikaci v aktuální mřížce.</span><span class="sxs-lookup"><span data-stu-id="727da-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="727da-145">Kontrola existující konfigurace mapování modelu ER</span><span class="sxs-lookup"><span data-stu-id="727da-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="727da-146">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="727da-146">Close the page.</span></span> 
2. <span data-ttu-id="727da-147">Klikněte na **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="727da-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="727da-148">Ve stromovém zobrazení rozbalte **Zahraniční obchodní model**.</span><span class="sxs-lookup"><span data-stu-id="727da-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="727da-149">Ve stromové struktuře vyberte **Model zahraničního obchodu\Mapování zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="727da-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="727da-150">Rozbalte oddíl **Předpoklady**.</span><span class="sxs-lookup"><span data-stu-id="727da-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="727da-151">V současné době toto mapování odkazuje na konfiguraci metadat.</span><span class="sxs-lookup"><span data-stu-id="727da-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="727da-152">Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo.</span><span class="sxs-lookup"><span data-stu-id="727da-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="727da-153">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="727da-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="727da-154">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="727da-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="727da-155">Ve stromovém zobrazení vyberte možnost **Dynamics 365 for Operations\Table records**.</span><span class="sxs-lookup"><span data-stu-id="727da-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="727da-156">Klikněte na možnost **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="727da-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="727da-157">V poli **Tabulka** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="727da-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="727da-158">V současné době toto mapování odkazuje na konfiguraci metadat.</span><span class="sxs-lookup"><span data-stu-id="727da-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="727da-159">Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo.</span><span class="sxs-lookup"><span data-stu-id="727da-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="727da-160">Klepněte na možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="727da-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="727da-161">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="727da-161">Close the page.</span></span> 
13. <span data-ttu-id="727da-162">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="727da-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="727da-163">Přiřazení připojené aplikace k mapování modelu</span><span class="sxs-lookup"><span data-stu-id="727da-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="727da-164">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="727da-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="727da-165">Vyberte aplikaci **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="727da-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="727da-166">V současné době toto mapování odkazuje na metadata vybrané připojené aplikace.</span><span class="sxs-lookup"><span data-stu-id="727da-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="727da-167">Pokud stejné mapování odkazuje na konfiguraci metadat a připojenou aplikaci současně, budou použita metadata připojené aplikace.</span><span class="sxs-lookup"><span data-stu-id="727da-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="727da-168">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="727da-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="727da-169">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="727da-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="727da-170">Ve stromovém zobrazení vyberte možnost **Dynamics 365 for Operations\Table records**.</span><span class="sxs-lookup"><span data-stu-id="727da-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="727da-171">Klikněte na možnost **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="727da-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="727da-172">V poli **Tabulka** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="727da-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="727da-173">Nyní byly nabídnuty více než dvě tabulky aplikace, protože toto mapování používá všechna metadata připojené aplikace, která je k ní přiřazena.</span><span class="sxs-lookup"><span data-stu-id="727da-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="727da-174">Klepněte na možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="727da-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="727da-175">Klikněte na tlačítko **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="727da-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="727da-176">Úspěšně jste provedli vázání prvků datového modelu s položkami datových zdrojů, které jsou popsány pomocí podrobností metadat připojené aplikace, která byla přiřazena pro toto mapování.</span><span class="sxs-lookup"><span data-stu-id="727da-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="727da-177">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="727da-177">Close the page.</span></span> 
11. <span data-ttu-id="727da-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="727da-178">Close the page.</span></span> 

<span data-ttu-id="727da-179">Potřebujete-li vyhodnotit mapování modelu pomocí metadat jiné verze aplikace, zaregistrujte jinou připojenou aplikaci, přiřaďte ji k tomuto mapování modelu a ověřte ji proti novým metadatům.</span><span class="sxs-lookup"><span data-stu-id="727da-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>

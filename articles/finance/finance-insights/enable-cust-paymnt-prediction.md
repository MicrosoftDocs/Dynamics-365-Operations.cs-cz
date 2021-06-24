---
title: Povolit předpovědi plateb od zákazníka (náhled)
description: Toto téma vysvětluje, jak zapnout a nakonfigurovat funkci předpovědi plateb zákazníka ve Finančních přehledech.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ae957f592ad9a1237817fec5d4172295f9a53020
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222578"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="bf6c9-103">Povolit předpovědi plateb od zákazníka (náhled)</span><span class="sxs-lookup"><span data-stu-id="bf6c9-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="bf6c9-104">Toto téma vysvětluje, jak zapnout a nakonfigurovat funkci předpovědi plateb zákazníka ve Finančních přehledech.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="bf6c9-105">Funkci zapnete v pracovním prostoru **Správa funkcí** a zadejte nastavení konfigurace na stránce **Parametry finančních přehledů**.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="bf6c9-106">Toto téma také obsahuje informace, které vám mohou pomoci tuto funkci efektivně využívat.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="bf6c9-107">Než dokončíte následující kroky, nezapomeňte provést nezbytné kroky v tématu [Konfigurace pro finanční přehledy](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="bf6c9-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="bf6c9-108">Použijte informace ze stránky prostředí v Microsoft Dynamics Lifecycle Services (LCS) pro připojení k primární instanci Azure SQL pro dané prostředí.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="bf6c9-109">Spuštěním následujícího příkazu Transact-SQL (T-SQL) zapněte testování pro prostředí sandboxu.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="bf6c9-110">(Možná budete muset zapnout přístup ke své IP adrese v LCS, než se budete moci vzdáleně připojit k aplikačnímu objektovému serveru \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="bf6c9-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="bf6c9-111">Tento krok přeskočte, pokud používáte verzi 10.0.20 nebo novější nebo pokud používáte nasazení Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-111">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="bf6c9-112">Tým finančních přehledů už měl testování zapnout za vás.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="bf6c9-113">Pokud nevidíte funkci v pracovním prostoru **Správa funkcí** nebo pokud při pokusu o zapnutí dojde k potížím, kontaktujte <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-113">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span> 

2. <span data-ttu-id="bf6c9-114">Zapněte funkci přehledy plateb zákazníků:</span><span class="sxs-lookup"><span data-stu-id="bf6c9-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="bf6c9-115">Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="bf6c9-116">Najděte funkci, která je pojmenována **Přehledy plateb zákazníků (náhled)**.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="bf6c9-117">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-117">Select **Enable now**.</span></span>

    <span data-ttu-id="bf6c9-118">Funkce Přehledy plateb zákazníků je nyní zapnutá a připravená ke konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="bf6c9-119">Konfigurujte funkci přehledy plateb zákazníků:</span><span class="sxs-lookup"><span data-stu-id="bf6c9-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="bf6c9-120">Přejděte na **Kredit a inkasa \> Nastavení \> Finanční přehledy \> Parametry finančních přehledů**.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="bf6c9-121">[![Stránka parametrů finančních přehledů před konfigurací funkce](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="bf6c9-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="bf6c9-122">Na stránce **Parametry finančních přehledů** na kartě **Přehledy plateb zákazníků** vyberte odkaz **Zobrazit datová pole použitá v predikčním modelu** pro otevření stránky **Datová pole pro predikční model**.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="bf6c9-123">Zde si můžete prohlédnout výchozí seznam polí, která se používají k vytvoření modelu predikce umělé inteligence (AI) pro předpovědi plateb zákazníků.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="bf6c9-124">Chcete-li k vytvoření predikčního modelu použít výchozí seznam polí, zavřete stránku **Datová pole pro predikční model** a poté na stránce **Parametry finančních přehledů** nastavte možnost **Povolit funkci** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="bf6c9-125">Zadejte období transakce "velmi pozdě" a definujte, co predikční kontejner **Velmi pozdě** znamená pro vaši obchodní činnost.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="bf6c9-126">U každé otevřené faktury systém předpovídá pravděpodobnost platby ve třech kontejnerech: **Včas**, **Pozdě** a **Velmi pozdě**.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="bf6c9-127">**Včas** - Tento kontejner zahrnuje platby, u nichž se předpokládá, že budou zaplaceny v den splatnosti transakce nebo před ním.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="bf6c9-128">**Pozdě** - Tento kontejner zahrnuje platby, u nichž se předpokládá, že budou zaplaceny po datu splatnosti transakce, ale před začátkem „velmi pozdního“ období transakce.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="bf6c9-129">**Velmi pozdě** - Tento kontejner zahrnuje platby, u nichž se předpokládá, že budou zaplaceny po začátku „velmi pozdního“ období transakce.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="bf6c9-130">Pokud změníte „velmi pozdní“ období transakce a vyberete **Změnit pozdní prhovou hodnotu** po vytvoření predikčního modelu AI pro platby odběratelům, stávající predikční model se odstraní a vytvoří se nový model.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="bf6c9-131">Nový predikční model přesune transakce do období „velmi pozdě“ na základě nastavení, která byla zadána k jeho definování.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="bf6c9-132">Poté, co dokončíte definování období transakce „velmi pozdě“, vyberte **Vytvořte predikční model** k vytvoření predikčního modelu.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="bf6c9-133">Část **Predikční model** na stránce **Parametry finančních přehledů** zobrazuje stav predikčního modelu.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="bf6c9-134">Kdykoli během vytváření predikčního modelu můžete vybrat **Obnovit vytváření modelu** a restartovat proces.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="bf6c9-135">Funkce byla nyní nakonfigurována a je připravena k použití.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="bf6c9-136">Poté, co byla funkce zapnuta a nakonfigurována a model predikce byl vytvořen a funguje, část **Predikční model** stránky **Parametry finančních přehledů** ukazuje přesnost modelu, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="bf6c9-137">[![Přesnost predikčního modelu na stránce parametrů finančních přehledů](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="bf6c9-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="bf6c9-138">Podrobnosti uvolnění</span><span class="sxs-lookup"><span data-stu-id="bf6c9-138">Release details</span></span>

<span data-ttu-id="bf6c9-139">Veřejný náhled finančních přehledů je k dispozici pro zkušební nasazení v USA, Evropě a Velké Británii.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="bf6c9-140">Microsoft postupně přidává podporu pro další regiony.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="bf6c9-141">Funkce veřejného náhledu mohou a měly by být zapnuty pouze v prostředích sandbox vrstvy 2.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="bf6c9-142">Modely nastavení a AI vytvořené v prostředí sandboxu nelze migrovat do produkčního prostředí.</span><span class="sxs-lookup"><span data-stu-id="bf6c9-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="bf6c9-143">Další informace viz [Doplňkové podmínky použití pro náhledy Microsoft Dynamics 365](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="bf6c9-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

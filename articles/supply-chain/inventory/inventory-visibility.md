---
title: Doplněk Viditelnost zásob
description: Toto téma popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114663"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="b51a8-103">Doplněk Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="b51a8-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="b51a8-104">Doplněk Viditelnost zásob je nezávislá a vysoce škálovatelná mikroslužba, která umožňuje sledování zásob na skladě v reálném čase, a tím poskytuje globální pohled na viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="b51a8-105">Všechny informace, které se vztahují k zásobám na skladě, se do služby exportují téměř v reálném čase prostřednictvím nízkoúrovňové integrace SQL.</span><span class="sxs-lookup"><span data-stu-id="b51a8-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="b51a8-106">Externí systémy přistupují ke službě prostřednictvím rozhraní API RESTful a dotazují se na praktické informace o daných sadách dimenzí, čímž získávají seznam dostupných pozic.</span><span class="sxs-lookup"><span data-stu-id="b51a8-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="b51a8-107">Viditelnost zásob je mikroslužba postavená na Microsoft Dataverse, což znamená, že ji můžete rozšířit pomocí vytváření Power Apps a použitím Power BI, a poskytovat přizpůsobené funkce pro splnění vašich obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="b51a8-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="b51a8-108">Je také možné upgradovat index za účelem provádění dotazů na zásoby.</span><span class="sxs-lookup"><span data-stu-id="b51a8-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="b51a8-109">Viditelnost zásob poskytuje možnosti konfigurace, které umožňují její integraci s více systémy třetích stran.</span><span class="sxs-lookup"><span data-stu-id="b51a8-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="b51a8-110">Podporuje standardizovanou dimenzi zásob, přizpůsobitelnou rozšiřitelnost a standardizované, konfigurovatelné vypočítané množství.</span><span class="sxs-lookup"><span data-stu-id="b51a8-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="b51a8-111">Toto téma popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management a jak používat jeho aplikační programovací rozhraní (API).</span><span class="sxs-lookup"><span data-stu-id="b51a8-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="b51a8-112">Instalace doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="b51a8-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="b51a8-113">Musíte nainstalovat doplněk Viditelnost zásob pomocí Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b51a8-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b51a8-114">LCS je portál pro spolupráci, který poskytuje prostředí a sadu pravidelně aktualizovaných služeb, které vám pomohou spravovat životní cyklus aplikace vašich aplikací Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b51a8-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="b51a8-115">Další informace naleznete v tématu [Zdroje Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="b51a8-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="b51a8-116">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="b51a8-116">Prerequisites</span></span>

<span data-ttu-id="b51a8-117">Před instalací doplňku Viditelnost zásob musíte provést následující:</span><span class="sxs-lookup"><span data-stu-id="b51a8-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="b51a8-118">Získejte implementační projekt LCS s alespoň jedním nasazeným prostředím.</span><span class="sxs-lookup"><span data-stu-id="b51a8-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="b51a8-119">Vygenerujte beta klíče pro vaši nabídku v LCS.</span><span class="sxs-lookup"><span data-stu-id="b51a8-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="b51a8-120">Povolte beta klíče pro vaši nabídku pro uživatele v LCS.</span><span class="sxs-lookup"><span data-stu-id="b51a8-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="b51a8-121">Kontaktujte produktový tým doplňku Viditelnost zásob společnosti Microsoft a sdělte jim ID prostředí, kam chcete nasadit doplněk Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="b51a8-122">Máte-li jakékoli dotazy týkající se těchto předpokladů, obraťte se na produktový tým doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="b51a8-123">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="b51a8-123">Install the add-in</span></span>

<span data-ttu-id="b51a8-124">Pro instalaci doplňku Viditelnost zásob proveďte následující:</span><span class="sxs-lookup"><span data-stu-id="b51a8-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="b51a8-125">Přihlaste se k portálu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="b51a8-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="b51a8-126">Na domovské stránce vyberte projekt, kde je nasazeno vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="b51a8-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="b51a8-127">Na stránce projektu vyberte prostředí, do kterého chcete doplněk nainstalovat.</span><span class="sxs-lookup"><span data-stu-id="b51a8-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="b51a8-128">Na stránce prostředí přejděte dolů, dokud neuvidíte sekci **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="b51a8-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="b51a8-129">Pokud sekce není viditelná, ujistěte se, že byly plně zpracovány nezbytné beta klíče.</span><span class="sxs-lookup"><span data-stu-id="b51a8-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="b51a8-130">V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="b51a8-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="b51a8-131">![Stránka prostředí v LCS](media/inventory-visibility-environment.png "Stránka prostředí v LCS")</span><span class="sxs-lookup"><span data-stu-id="b51a8-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="b51a8-132">Vyberte odkaz **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="b51a8-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="b51a8-133">Otevře se seznam dostupných doplňků.</span><span class="sxs-lookup"><span data-stu-id="b51a8-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="b51a8-134">Vyberte ze seznamu **Služba zásob**.</span><span class="sxs-lookup"><span data-stu-id="b51a8-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="b51a8-135">(Upozorňujeme, že toto může být nyní uvedeno jako **Doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management**.)</span><span class="sxs-lookup"><span data-stu-id="b51a8-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="b51a8-136">Zadejte hodnoty pro následující pole pro vaše prostředí:</span><span class="sxs-lookup"><span data-stu-id="b51a8-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="b51a8-137">**ID aplikace AAD**</span><span class="sxs-lookup"><span data-stu-id="b51a8-137">**AAD application ID**</span></span>
    - <span data-ttu-id="b51a8-138">**ID klienta AAD**</span><span class="sxs-lookup"><span data-stu-id="b51a8-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="b51a8-139">![Stránka nastavení doplňku](media/inventory-visibility-setup.png "Stránka nastavení doplňku")</span><span class="sxs-lookup"><span data-stu-id="b51a8-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="b51a8-140">Odsouhlaste smluvní podmínky výběrem zaškrtávacího políčka **Smluvní podmínky**.</span><span class="sxs-lookup"><span data-stu-id="b51a8-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="b51a8-141">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="b51a8-141">Select **Install**.</span></span> <span data-ttu-id="b51a8-142">Stav doplňku se zobrazí jako **Probíhá instalace**.</span><span class="sxs-lookup"><span data-stu-id="b51a8-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="b51a8-143">Po dokončení obnovte stránku, aby se zobrazila změna stavu **Nainstalováno**.</span><span class="sxs-lookup"><span data-stu-id="b51a8-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="b51a8-144">Získání tokenu služby zabezpečení</span><span class="sxs-lookup"><span data-stu-id="b51a8-144">Get a security service token</span></span>

<span data-ttu-id="b51a8-145">Token služby zabezpečení získáte takto:</span><span class="sxs-lookup"><span data-stu-id="b51a8-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="b51a8-146">Přihlaste se na Azure Portal a použijte jej k vyhledání `clientId` a `clientSecret` pro vaši aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b51a8-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="b51a8-147">Načtěte token Azure Active Directory (`aadToken`) odesláním požadavku HTTP s následujícími vlastnostmi:</span><span class="sxs-lookup"><span data-stu-id="b51a8-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="b51a8-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="b51a8-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="b51a8-149">**Metoda** - `GET`</span><span class="sxs-lookup"><span data-stu-id="b51a8-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="b51a8-150">**Obsah těla (údaje formuláře)**:</span><span class="sxs-lookup"><span data-stu-id="b51a8-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="b51a8-151">klíč</span><span class="sxs-lookup"><span data-stu-id="b51a8-151">key</span></span> | <span data-ttu-id="b51a8-152">hodnota</span><span class="sxs-lookup"><span data-stu-id="b51a8-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="b51a8-153">id klienta</span><span class="sxs-lookup"><span data-stu-id="b51a8-153">client_id</span></span> | <span data-ttu-id="b51a8-154">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="b51a8-154">${aadAppId}</span></span> |
        | <span data-ttu-id="b51a8-155">tajný klíč klienta</span><span class="sxs-lookup"><span data-stu-id="b51a8-155">client_secret</span></span> | <span data-ttu-id="b51a8-156">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="b51a8-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="b51a8-157">typ grantu</span><span class="sxs-lookup"><span data-stu-id="b51a8-157">grant_type</span></span> | <span data-ttu-id="b51a8-158">client_credentials</span><span class="sxs-lookup"><span data-stu-id="b51a8-158">client_credentials</span></span> |
        | <span data-ttu-id="b51a8-159">prostředek</span><span class="sxs-lookup"><span data-stu-id="b51a8-159">resource</span></span> | <span data-ttu-id="b51a8-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="b51a8-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="b51a8-161">Měli byste obdržet `aadToken` v odpovědi, která se podobá následujícímu příkladu.</span><span class="sxs-lookup"><span data-stu-id="b51a8-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="b51a8-162">Formulujte požadavek JSON, který se podobá následujícímu:</span><span class="sxs-lookup"><span data-stu-id="b51a8-162">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="b51a8-163">Kde:</span><span class="sxs-lookup"><span data-stu-id="b51a8-163">Where:</span></span>
    - <span data-ttu-id="b51a8-164">Hodnota `client_assertion` musí být `aadToken`, který jste obdrželi v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="b51a8-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="b51a8-165">Hodnota `context` musí být ID prostředí, do kterého chcete doplněk nasadit.</span><span class="sxs-lookup"><span data-stu-id="b51a8-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="b51a8-166">Nastavte všechny ostatní hodnoty, jak je znázorněno v příkladu.</span><span class="sxs-lookup"><span data-stu-id="b51a8-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="b51a8-167">Odešlete požadavek HTTP s následujícími vlastnostmi:</span><span class="sxs-lookup"><span data-stu-id="b51a8-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="b51a8-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="b51a8-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="b51a8-169">**Metoda** - `POST`</span><span class="sxs-lookup"><span data-stu-id="b51a8-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="b51a8-170">**Záhlaví HTTP** - Zahrňte verzi API (klíč je `Api-Version` a hodnota je `1.0`)</span><span class="sxs-lookup"><span data-stu-id="b51a8-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="b51a8-171">**Obsah těla** - Zahrňte požadavek JSON, který jste vytvořili v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="b51a8-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="b51a8-172">V odpovědi získáte `access_token`.</span><span class="sxs-lookup"><span data-stu-id="b51a8-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="b51a8-173">To je to, co potřebujete jako nosný token pro volání rozhraní API doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="b51a8-174">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="b51a8-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="b51a8-175">Odinstalace doplňku</span><span class="sxs-lookup"><span data-stu-id="b51a8-175">Uninstall the add-in</span></span>

<span data-ttu-id="b51a8-176">Chcete-li doplněk odinstalovat, vyberte **Odinstalovat**.</span><span class="sxs-lookup"><span data-stu-id="b51a8-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="b51a8-177">Obnovte LCS a doplněk Viditelnost zásob bude odebrán.</span><span class="sxs-lookup"><span data-stu-id="b51a8-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="b51a8-178">Proces odinstalace odebere registraci doplňku a také spustí úlohu k vyčištění všech obchodních dat uložených ve službě.</span><span class="sxs-lookup"><span data-stu-id="b51a8-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="b51a8-179">Veřejné rozhraní API doplňku Viditelnosti zásob</span><span class="sxs-lookup"><span data-stu-id="b51a8-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="b51a8-180">Veřejné rozhraní REST API doplňku Viditelnost zásob představuje několik konkrétních koncových bodů integrace.</span><span class="sxs-lookup"><span data-stu-id="b51a8-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="b51a8-181">Podporuje tři hlavní typy interakce:</span><span class="sxs-lookup"><span data-stu-id="b51a8-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="b51a8-182">Odesílání změn zásob na skladě do doplňku z externího systému.</span><span class="sxs-lookup"><span data-stu-id="b51a8-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="b51a8-183">Dotazování na aktuální množství zásob na skladě z externího systému.</span><span class="sxs-lookup"><span data-stu-id="b51a8-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="b51a8-184">Automatická synchronizace se zásobami na skladě v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b51a8-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="b51a8-185">Automatická synchronizace není součástí veřejného API, ale místo toho se zpracovává na pozadí pro prostředí, která mají povolený doplněk Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="b51a8-186">Ověřování</span><span class="sxs-lookup"><span data-stu-id="b51a8-186">Authentication</span></span>

<span data-ttu-id="b51a8-187">Token zabezpečení platformy se používá k volání doplňku Viditelnost zásob, takže musíte vygenerovat token Azure Active Directory pomocí vaší aplikace Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b51a8-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="b51a8-188">Další informace o tom, jak získat token zabezpečení, najdete v části [Instalace doplňku Viditelnost zásob](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="b51a8-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="b51a8-189">Konfigurace rozhraní API doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="b51a8-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="b51a8-190">Před použitím služby musíte dokončit konfigurace popsané v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="b51a8-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="b51a8-191">Konfigurace se může lišit v závislosti na podrobnostech vašeho prostředí.</span><span class="sxs-lookup"><span data-stu-id="b51a8-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="b51a8-192">Obsahuje primárně čtyři části:</span><span class="sxs-lookup"><span data-stu-id="b51a8-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="b51a8-193">Rozdělení</span><span class="sxs-lookup"><span data-stu-id="b51a8-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="b51a8-194">Konfigurace dimenzí</span><span class="sxs-lookup"><span data-stu-id="b51a8-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="b51a8-195">Indexace</span><span class="sxs-lookup"><span data-stu-id="b51a8-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="b51a8-196">Vlastní měrné systémy</span><span class="sxs-lookup"><span data-stu-id="b51a8-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="b51a8-197">Rozdělení</span><span class="sxs-lookup"><span data-stu-id="b51a8-197">Partitioning</span></span>

<span data-ttu-id="b51a8-198">Rozdělení může významně ovlivnit výkonnost rozhraní API doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="b51a8-199">Je vhodné definovat schéma, které umožňuje malá seskupení dat a přitom umožňuje smysluplné dotazy na data.</span><span class="sxs-lookup"><span data-stu-id="b51a8-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="b51a8-200">`organizationId` (`dataAreaId` v Supply Chain Management) bude vždy součástí rozdělení a ve výchozím nastavení je Viditelnost zásob nastavena na rozdělení podle dimenzí jako *Pracoviště + skladové místo*.</span><span class="sxs-lookup"><span data-stu-id="b51a8-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="b51a8-201">To znamená, že služba musí být vždy dotazována s těmito dimenzemi definovanými na filtrech.</span><span class="sxs-lookup"><span data-stu-id="b51a8-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="b51a8-202">*Pracoviště* a *Skladové místo* jsou dvě obecné výchozí dimenze ve Viditelnosti zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="b51a8-203">V aplikaci Supply Chain Management se tyto dimenze nazývají *Pracoviště* (`InventSiteId`) a *Sklad* (`InventLocationId`).</span><span class="sxs-lookup"><span data-stu-id="b51a8-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="b51a8-204">Konfigurace dimenzí</span><span class="sxs-lookup"><span data-stu-id="b51a8-204">Dimension configurations</span></span>

<span data-ttu-id="b51a8-205">Viditelnost zásob poskytne seznam obecných výchozích dimenzí umožňujících integraci více zdrojových systémů.</span><span class="sxs-lookup"><span data-stu-id="b51a8-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="b51a8-206">V následující tabulce jsou uvedeny dimenze zásob, které budou výchozími názvy dimenzí v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="b51a8-207">Typ dimenze</span><span class="sxs-lookup"><span data-stu-id="b51a8-207">Dimension type</span></span> | <span data-ttu-id="b51a8-208">Název dimenze</span><span class="sxs-lookup"><span data-stu-id="b51a8-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="b51a8-209">Produkt</span><span class="sxs-lookup"><span data-stu-id="b51a8-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="b51a8-210">Produkt</span><span class="sxs-lookup"><span data-stu-id="b51a8-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="b51a8-211">Produkt</span><span class="sxs-lookup"><span data-stu-id="b51a8-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="b51a8-212">Produkt</span><span class="sxs-lookup"><span data-stu-id="b51a8-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="b51a8-213">Sledování</span><span class="sxs-lookup"><span data-stu-id="b51a8-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="b51a8-214">Sledování</span><span class="sxs-lookup"><span data-stu-id="b51a8-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="b51a8-215">Skladové místo</span><span class="sxs-lookup"><span data-stu-id="b51a8-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="b51a8-216">Skladové místo</span><span class="sxs-lookup"><span data-stu-id="b51a8-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="b51a8-217">Stav zásob</span><span class="sxs-lookup"><span data-stu-id="b51a8-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="b51a8-218">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="b51a8-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="b51a8-219">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="b51a8-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="b51a8-220">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="b51a8-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="b51a8-221">Typ dimenze uvedený v předchozí tabulce slouží pouze pro informaci.</span><span class="sxs-lookup"><span data-stu-id="b51a8-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="b51a8-222">V doplňku Viditelnost zásob není nutné definovat typ dimenze.</span><span class="sxs-lookup"><span data-stu-id="b51a8-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="b51a8-223">Pokud vlastní dimenze existuje a je třeba ji přepnout na výchozí hodnotu, když je spotřebována doplňkem Viditelnost zásob, můžete nakonfigurovat název **Vlastní dimenze** v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="b51a8-224">Externí systémy přistupují k doplňku Viditelnost zásob prostřednictvím rozhraní RESTful API, která umožňují dotazování na informace o dostupnosti na skladě u daných sad dimenzí.</span><span class="sxs-lookup"><span data-stu-id="b51a8-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="b51a8-225">Pro integraci vám doplněk Viditelnost zásob umožňuje konfigurovat *externí zdroj dat kanálu* a zdrojovou dimenzi do *cílových dimenzí* v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="b51a8-226">Cílové dimenze by měly být jednou z následujících:</span><span class="sxs-lookup"><span data-stu-id="b51a8-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="b51a8-227">Výchozí dimenze v doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="b51a8-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="b51a8-228">Vlastní dimenze</span><span class="sxs-lookup"><span data-stu-id="b51a8-228">Custom dimensions</span></span>

<span data-ttu-id="b51a8-229">Účelem konfigurace dimenze je standardizovat integraci více systémů pro dotazování na dimenzích a publikování události s dimenzemi.</span><span class="sxs-lookup"><span data-stu-id="b51a8-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="b51a8-230">Indexace</span><span class="sxs-lookup"><span data-stu-id="b51a8-230">Indexing</span></span>

<span data-ttu-id="b51a8-231">Po většinu času bude dotaz na zásoby na skladě nejen na nejvyšší „celkové“ úrovni, ale možná budete chtít vidět výsledky agregované na základě dimenzí zásob.</span><span class="sxs-lookup"><span data-stu-id="b51a8-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="b51a8-232">Viditelnost zásob poskytuje flexibilitu tím, že umožňuje nastavit indexy, které jsou založeny na dimenzi nebo kombinaci dimenzí.</span><span class="sxs-lookup"><span data-stu-id="b51a8-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="b51a8-233">V současné době můžete indexy nakonfigurovat pouze na maximálně pět.</span><span class="sxs-lookup"><span data-stu-id="b51a8-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="b51a8-234">Před implementací musíte pečlivě zvážit, kterou dimenzi nebo kombinaci dimenzí použijete, abyste zajistili, že bude vyhovovat vašim obchodním potřebám.</span><span class="sxs-lookup"><span data-stu-id="b51a8-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="b51a8-235">Chcete-li se například dotazovat na produkty následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="b51a8-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="b51a8-236">Dotazujte se na agregované zásoby na skladě produktu podle dimenzí *Barva* a *Velikost*.</span><span class="sxs-lookup"><span data-stu-id="b51a8-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="b51a8-237">V některých případech se chcete pouze dotazovat na produkt celkem.</span><span class="sxs-lookup"><span data-stu-id="b51a8-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="b51a8-238">Měli byste dva indexy definované následovně:</span><span class="sxs-lookup"><span data-stu-id="b51a8-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="b51a8-239">Prázdná závorka se agreguje na základě ID produktu v oddílu.</span><span class="sxs-lookup"><span data-stu-id="b51a8-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="b51a8-240">Indexování definuje, jak můžete seskupit výsledky na základě nastavení dotazu `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="b51a8-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="b51a8-241">V tomto případě, pokud nedefinujete žádné hodnoty `groupBy`, získáte součty `productid`.</span><span class="sxs-lookup"><span data-stu-id="b51a8-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="b51a8-242">Jinak pokud definujete `groupBy` jako `groupBy=ColorId&groupBy=SizeId`, vrátí se vám více řádků na základě různých kombinací barev a velikostí v systému.</span><span class="sxs-lookup"><span data-stu-id="b51a8-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="b51a8-243">Kritéria dotazu můžete zadat do textu požadavku.</span><span class="sxs-lookup"><span data-stu-id="b51a8-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="b51a8-244">Zde je ukázkový dotaz na produkt s kombinací barev a velikostí.</span><span class="sxs-lookup"><span data-stu-id="b51a8-244">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="b51a8-245">Vlastní měrné systémy</span><span class="sxs-lookup"><span data-stu-id="b51a8-245">Custom measurement</span></span>

<span data-ttu-id="b51a8-246">Výchozí množství měrného systému jsou propojena se Supply Chain Management, můžete však chtít mít množství, které je tvořeno kombinací výchozích měrných systémů.</span><span class="sxs-lookup"><span data-stu-id="b51a8-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="b51a8-247">Chcete-li to provést, můžete mít konfiguraci vlastních množství, která budou přidána k výstupu dotazů na zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="b51a8-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="b51a8-248">Funkce jednoduše umožňuje definovat sadu měrných systémů, které budou přidány, anebo sadu měrných systémů, které budou odečteny, aby bylo možné vytvořit vlastní měrný systém.</span><span class="sxs-lookup"><span data-stu-id="b51a8-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="b51a8-249">Například s následující podmínkou dotazu nakonfigurujete vlastní množství měrné jednotky jako `MyCustomAvailableforReservation`, která má být spotřebována systémem spotřeby.</span><span class="sxs-lookup"><span data-stu-id="b51a8-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="b51a8-250">Systém spotřeby</span><span class="sxs-lookup"><span data-stu-id="b51a8-250">Consumption system</span></span> | <span data-ttu-id="b51a8-251">Vypočtené měrné jednotky</span><span class="sxs-lookup"><span data-stu-id="b51a8-251">Calculated measurers</span></span> | <span data-ttu-id="b51a8-252">Zdroj dat</span><span class="sxs-lookup"><span data-stu-id="b51a8-252">Data source</span></span> | <span data-ttu-id="b51a8-253">Modifikátor</span><span class="sxs-lookup"><span data-stu-id="b51a8-253">Modifier</span></span> | <span data-ttu-id="b51a8-254">Typ výpočtu modifikátoru</span><span class="sxs-lookup"><span data-stu-id="b51a8-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="b51a8-255">Sčítání</span><span class="sxs-lookup"><span data-stu-id="b51a8-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="b51a8-256">Sčítání</span><span class="sxs-lookup"><span data-stu-id="b51a8-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="b51a8-257">Odčítání</span><span class="sxs-lookup"><span data-stu-id="b51a8-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="b51a8-258">Sčítání</span><span class="sxs-lookup"><span data-stu-id="b51a8-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="b51a8-259">Odčítání</span><span class="sxs-lookup"><span data-stu-id="b51a8-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="b51a8-260">Sčítání</span><span class="sxs-lookup"><span data-stu-id="b51a8-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="b51a8-261">Sčítání</span><span class="sxs-lookup"><span data-stu-id="b51a8-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="b51a8-262">Odčítání</span><span class="sxs-lookup"><span data-stu-id="b51a8-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="b51a8-263">Odčítání</span><span class="sxs-lookup"><span data-stu-id="b51a8-263">Subtraction</span></span> |

<span data-ttu-id="b51a8-264">Takto dotaz na vlastní množství měrnou jednotku vrátí následující výstup.</span><span class="sxs-lookup"><span data-stu-id="b51a8-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="b51a8-265">Výstup `MyCustomAvailableforReservation` je založen na nastavení výpočtu ve vlastních měrných systémech jako:</span><span class="sxs-lookup"><span data-stu-id="b51a8-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="b51a8-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="b51a8-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="b51a8-267">Publikování změn množství na skladě</span><span class="sxs-lookup"><span data-stu-id="b51a8-267">Posting on-hand changes</span></span>

<span data-ttu-id="b51a8-268">Přesná adresa URL, na kterou bude událost publikována, bude záviset na vaší zeměpisné oblasti.</span><span class="sxs-lookup"><span data-stu-id="b51a8-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="b51a8-269">Bude mít formu:</span><span class="sxs-lookup"><span data-stu-id="b51a8-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="b51a8-270">Po ověření lze tuto adresu URL použít společně s metodou HTTP `POST` pro odesílání událostí změny zásob na skladě do služby.</span><span class="sxs-lookup"><span data-stu-id="b51a8-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="b51a8-271">Pro komunikaci se službami Dynamics 365 prostřednictvím požadavků HTTP se používá speciální záhlaví, které označuje ID prostředí instance Supply Chain Management, ke které jsou data propojena.</span><span class="sxs-lookup"><span data-stu-id="b51a8-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="b51a8-272">Například:</span><span class="sxs-lookup"><span data-stu-id="b51a8-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="b51a8-273">Zveřejnění dotazu na změny zásob na skladě - příklad 1</span><span class="sxs-lookup"><span data-stu-id="b51a8-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="b51a8-274">Tento příklad ukazuje scénář, ve kterém nastavíte konfiguraci dimenze v Power Apps.</span><span class="sxs-lookup"><span data-stu-id="b51a8-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="b51a8-275">Pomocí následujícího dotazu nakonfigurujte mapování dimenzí v Power Apps:</span><span class="sxs-lookup"><span data-stu-id="b51a8-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="b51a8-276">Nyní můžete určit `dimensionDataSource` a ve svých dotazech použít vlastní dimenze.</span><span class="sxs-lookup"><span data-stu-id="b51a8-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="b51a8-277">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="b51a8-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="b51a8-278">Zveřejnění dotazu na změny zásob na skladě - příklad 2</span><span class="sxs-lookup"><span data-stu-id="b51a8-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="b51a8-279">Tento příklad ukazuje scénář, kde pro konfiguraci dimenze v nejsou nastavena žádná mapování v Power Apps, takže publikování by mělo také použít základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="b51a8-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="b51a8-280">Všechny dimenze musí být základními dimenzemi, když má pole `dimensionDataSource` hodnotu null, je prázdné nebo má mezeru.</span><span class="sxs-lookup"><span data-stu-id="b51a8-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="b51a8-281">Vlastnosti pole dokumentu JSON</span><span class="sxs-lookup"><span data-stu-id="b51a8-281">JSON document field properties</span></span>

<span data-ttu-id="b51a8-282">Pole z dříve poskytnutých příkladů dotazů JSON mají vlastnosti uvedené v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="b51a8-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="b51a8-283">ID pole</span><span class="sxs-lookup"><span data-stu-id="b51a8-283">Field ID</span></span> | <span data-ttu-id="b51a8-284">popis</span><span class="sxs-lookup"><span data-stu-id="b51a8-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="b51a8-285">Jedinečné ID pro konkrétní událost změny.</span><span class="sxs-lookup"><span data-stu-id="b51a8-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="b51a8-286">Toto ID se používá k zajištění toho, že pokud komunikace se službou během publikování selže, opětovné odeslání události nebude mít za následek, že se v systému dvakrát započítá stejná událost.</span><span class="sxs-lookup"><span data-stu-id="b51a8-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="b51a8-287">Identifikátor organizace spojené s událostí.</span><span class="sxs-lookup"><span data-stu-id="b51a8-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="b51a8-288">To se mapuje na organizace Supply Chain Management nebo ID datové oblasti.</span><span class="sxs-lookup"><span data-stu-id="b51a8-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="b51a8-289">Identifikátor daného produktu.</span><span class="sxs-lookup"><span data-stu-id="b51a8-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="b51a8-290">Množství, o které je třeba změnit zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="b51a8-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="b51a8-291">Pokud by bylo například na polici přidáno 10 nových housek, byla by tato hodnota 10.</span><span class="sxs-lookup"><span data-stu-id="b51a8-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="b51a8-292">Pokud by pak byly 3 housky odebrány z police nebo prodány, byla by tato hodnota -3.</span><span class="sxs-lookup"><span data-stu-id="b51a8-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="b51a8-293">Zdroj dat dimenzí použitých v události změny publikování změny a dotazu.</span><span class="sxs-lookup"><span data-stu-id="b51a8-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="b51a8-294">Pokud zadáte zdroj dat, můžete použít vlastní dimenze ze zadaného zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="b51a8-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="b51a8-295">S konfigurací dimenzí může Viditelnost dat mapovat vlastní dimenze na obecné výchozí dimenze.</span><span class="sxs-lookup"><span data-stu-id="b51a8-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="b51a8-296">Pokud není zadán `dimensionDataSource`, můžete ve svých dotazech použít pouze obecné výchozí dimenze.</span><span class="sxs-lookup"><span data-stu-id="b51a8-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="b51a8-297">Dynamická sada párů klíč/hodnota.</span><span class="sxs-lookup"><span data-stu-id="b51a8-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="b51a8-298">Budou mapovány na některé dimenze v Supply Chain Management, ale můžete také přidat vlastní dimenze (jako *Zdroj*), což může naznačovat, že událost pocházela ze Supply Chain Managementu nebo externího systému.</span><span class="sxs-lookup"><span data-stu-id="b51a8-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="b51a8-299">Dotaz na aktuální zásoby na skladě</span><span class="sxs-lookup"><span data-stu-id="b51a8-299">Querying current on-hand</span></span>

<span data-ttu-id="b51a8-300">Koncový bod pro dotazování na aktuální zásoby na skladě bude mít podobnou adresu URL:</span><span class="sxs-lookup"><span data-stu-id="b51a8-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="b51a8-301">Bude dotazován pomocí metody HTTP `POST`.</span><span class="sxs-lookup"><span data-stu-id="b51a8-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="b51a8-302">Dotaz na aktuální zásoby na skladě - příklad 1</span><span class="sxs-lookup"><span data-stu-id="b51a8-302">Current on-hand query example 1</span></span>

<span data-ttu-id="b51a8-303">Tento příklad ukazuje scénář, ve kterém jste dokončili konfiguraci dimenze v Power Apps.</span><span class="sxs-lookup"><span data-stu-id="b51a8-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="b51a8-304">Pomocí následujícího dotazu nakonfigurujte mapování dimenzí v Power Apps:</span><span class="sxs-lookup"><span data-stu-id="b51a8-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="b51a8-305">Nyní můžete určit `dimensionDataSource` a ve svých dotazech použít vlastní dimenze.</span><span class="sxs-lookup"><span data-stu-id="b51a8-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="b51a8-306">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="b51a8-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="b51a8-307">Můžete určit `DimensionDataSource` v `filters` a zadat vlastní dimenze v `filters` i `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="b51a8-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="b51a8-308">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="b51a8-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="b51a8-309">Dotaz na aktuální zásoby na skladě - příklad 2</span><span class="sxs-lookup"><span data-stu-id="b51a8-309">Current on-hand query example 2</span></span>

<span data-ttu-id="b51a8-310">Tento příklad ukazuje scénář, kde pro konfiguraci dimenze v nejsou nastavena žádná mapování v Power Apps, takže publikování by mělo také použít základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="b51a8-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="b51a8-311">Všechny dimenze musí být základními dimenzemi, když má pole `dimensionDataSource` pod `filters` hodnotu null nebo mezeru.</span><span class="sxs-lookup"><span data-stu-id="b51a8-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="b51a8-312">Příklad výsledku vrácení</span><span class="sxs-lookup"><span data-stu-id="b51a8-312">Example return result</span></span>

<span data-ttu-id="b51a8-313">Dotazy zobrazené v předchozích příkladech by mohly vrátit takový výsledek.</span><span class="sxs-lookup"><span data-stu-id="b51a8-313">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="b51a8-314">Všimněte si, že pole množství jsou strukturována jako slovník měrných jednotek a jejich přidružených hodnot.</span><span class="sxs-lookup"><span data-stu-id="b51a8-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>

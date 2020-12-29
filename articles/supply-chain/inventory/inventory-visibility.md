---
title: Doplněk Viditelnost zásob
description: Toto téma popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625058"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="6d294-103">Doplněk Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="6d294-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6d294-104">Doplněk Viditelnost zásob je nezávislá a vysoce škálovatelná mikroslužba, která umožňuje sledování zásob na skladě v reálném čase, a tím poskytuje globální pohled na viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="6d294-105">Všechny informace, které se vztahují k zásobám na skladě, se do služby exportují téměř v reálném čase prostřednictvím nízkoúrovňové integrace SQL.</span><span class="sxs-lookup"><span data-stu-id="6d294-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="6d294-106">Externí systémy přistupují ke službě prostřednictvím rozhraní API RESTful a dotazují se na praktické informace o daných sadách dimenzí, čímž získávají seznam dostupných pozic.</span><span class="sxs-lookup"><span data-stu-id="6d294-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="6d294-107">Viditelnost zásob je mikroslužba postavená na Common Data Service, což znamená, že ji můžete rozšířit pomocí vytváření Power Apps a použitím Power BI, a poskytovat přizpůsobené funkce pro splnění vašich obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="6d294-107">Inventory Visibility is a microservice built on the Common Data Service, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="6d294-108">Je také možné upgradovat index za účelem provádění dotazů na zásoby.</span><span class="sxs-lookup"><span data-stu-id="6d294-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="6d294-109">Viditelnost zásob poskytuje možnosti konfigurace, které umožňují její integraci s více systémy třetích stran.</span><span class="sxs-lookup"><span data-stu-id="6d294-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="6d294-110">Podporuje standardizovanou dimenzi zásob, přizpůsobitelnou rozšiřitelnost a standardizované, konfigurovatelné vypočítané množství.</span><span class="sxs-lookup"><span data-stu-id="6d294-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="6d294-111">Toto téma popisuje, jak nainstalovat a nakonfigurovat doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management a jak používat jeho aplikační programovací rozhraní (API).</span><span class="sxs-lookup"><span data-stu-id="6d294-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="6d294-112">Instalace doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="6d294-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="6d294-113">Musíte nainstalovat doplněk Viditelnost zásob pomocí Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6d294-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6d294-114">LCS je portál pro spolupráci, který poskytuje prostředí a sadu pravidelně aktualizovaných služeb, které vám pomohou spravovat životní cyklus aplikace vašich aplikací Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6d294-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="6d294-115">Další informace naleznete v tématu [Zdroje Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="6d294-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6d294-116">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="6d294-116">Prerequisites</span></span>

<span data-ttu-id="6d294-117">Před instalací doplňku Viditelnost zásob musíte provést následující:</span><span class="sxs-lookup"><span data-stu-id="6d294-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="6d294-118">Získejte implementační projekt LCS s alespoň jedním nasazeným prostředím.</span><span class="sxs-lookup"><span data-stu-id="6d294-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="6d294-119">Vygenerujte beta klíče pro vaši nabídku v LCS.</span><span class="sxs-lookup"><span data-stu-id="6d294-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="6d294-120">Povolte beta klíče pro vaši nabídku pro uživatele v LCS.</span><span class="sxs-lookup"><span data-stu-id="6d294-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="6d294-121">Kontaktujte produktový tým doplňku Viditelnost zásob společnosti Microsoft a sdělte jim ID prostředí, kam chcete nasadit doplněk Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="6d294-122">Máte-li jakékoli dotazy týkající se těchto předpokladů, obraťte se na produktový tým doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="6d294-123">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="6d294-123">Install the add-in</span></span>

<span data-ttu-id="6d294-124">Pro instalaci doplňku Viditelnost zásob proveďte následující:</span><span class="sxs-lookup"><span data-stu-id="6d294-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="6d294-125">Přihlaste se k portálu [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="6d294-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="6d294-126">Na domovské stránce vyberte projekt, kde je nasazeno vaše prostředí.</span><span class="sxs-lookup"><span data-stu-id="6d294-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="6d294-127">Na stránce projektu vyberte prostředí, do kterého chcete doplněk nainstalovat.</span><span class="sxs-lookup"><span data-stu-id="6d294-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="6d294-128">Na stránce prostředí přejděte dolů, dokud neuvidíte sekci **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="6d294-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="6d294-129">Pokud sekce není viditelná, ujistěte se, že byly plně zpracovány nezbytné beta klíče.</span><span class="sxs-lookup"><span data-stu-id="6d294-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="6d294-130">V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="6d294-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="6d294-131">![Stránka prostředí v LCS](media/inventory-visibility-environment.png "Stránka prostředí v LCS")</span><span class="sxs-lookup"><span data-stu-id="6d294-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="6d294-132">Vyberte odkaz **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="6d294-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="6d294-133">Otevře se seznam dostupných doplňků.</span><span class="sxs-lookup"><span data-stu-id="6d294-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="6d294-134">Vyberte ze seznamu **Služba zásob**.</span><span class="sxs-lookup"><span data-stu-id="6d294-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="6d294-135">(Upozorňujeme, že toto může být nyní uvedeno jako **Doplněk Viditelnost zásob pro Dynamics 365 Supply Chain Management**.)</span><span class="sxs-lookup"><span data-stu-id="6d294-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="6d294-136">Zadejte hodnoty pro následující pole pro vaše prostředí:</span><span class="sxs-lookup"><span data-stu-id="6d294-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="6d294-137">**ID aplikace AAD**</span><span class="sxs-lookup"><span data-stu-id="6d294-137">**AAD application ID**</span></span>
    - <span data-ttu-id="6d294-138">**ID klienta AAD**</span><span class="sxs-lookup"><span data-stu-id="6d294-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="6d294-139">![Stránka nastavení doplňku](media/inventory-visibility-setup.png "Stránka nastavení doplňku")</span><span class="sxs-lookup"><span data-stu-id="6d294-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="6d294-140">Odsouhlaste smluvní podmínky výběrem zaškrtávacího políčka **Smluvní podmínky**.</span><span class="sxs-lookup"><span data-stu-id="6d294-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="6d294-141">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="6d294-141">Select **Install**.</span></span> <span data-ttu-id="6d294-142">Stav doplňku se zobrazí jako **Probíhá instalace**.</span><span class="sxs-lookup"><span data-stu-id="6d294-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="6d294-143">Po dokončení obnovte stránku, aby se zobrazila změna stavu **Nainstalováno**.</span><span class="sxs-lookup"><span data-stu-id="6d294-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="6d294-144">Získání tokenu služby zabezpečení</span><span class="sxs-lookup"><span data-stu-id="6d294-144">Get a security service token</span></span>

<span data-ttu-id="6d294-145">Chcete-li získat token služby zabezpečení, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="6d294-145">To get a security service token, do the following:</span></span>

1. <span data-ttu-id="6d294-146">Získejte `aadToken` a zavolejte koncový bod: https://securityservice.operations365.dynamics.com/token.</span><span class="sxs-lookup"><span data-stu-id="6d294-146">Get your `aadToken` and call the endpoint: https://securityservice.operations365.dynamics.com/token.</span></span>
1. <span data-ttu-id="6d294-147">Nahraďte `client_assertion` v textu za `aadToken`.</span><span class="sxs-lookup"><span data-stu-id="6d294-147">Replace the `client_assertion` in the body with your `aadToken`.</span></span>
1. <span data-ttu-id="6d294-148">Nahraďte kontext v textu prostředím, ve kterém chcete doplněk nasadit.</span><span class="sxs-lookup"><span data-stu-id="6d294-148">Replace the context in the body with the environment where you want to deploy the add-in.</span></span>
1. <span data-ttu-id="6d294-149">Nahraďte obor v textu následovně:</span><span class="sxs-lookup"><span data-stu-id="6d294-149">Replace the scope in the body with the following:</span></span>

    - <span data-ttu-id="6d294-150">Rozsah pro MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span><span class="sxs-lookup"><span data-stu-id="6d294-150">Scope for MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span></span>  
    <span data-ttu-id="6d294-151">(ID aplikace Azure Active Directory ID tenanta pro MCK naleznete v `appsettings.mck.json`.)</span><span class="sxs-lookup"><span data-stu-id="6d294-151">(You can find the Azure Active Directory application ID and tenant ID for MCK in `appsettings.mck.json`.)</span></span>
    - <span data-ttu-id="6d294-152">Rozsah pro PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span><span class="sxs-lookup"><span data-stu-id="6d294-152">Scope for PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span></span>  
    <span data-ttu-id="6d294-153">(ID aplikace Azure Active Directory ID tenanta pro PROD naleznete v `appsettings.prod.json`.)</span><span class="sxs-lookup"><span data-stu-id="6d294-153">(You can find the Azure Active Directory application ID and tenant ID for PROD in `appsettings.prod.json`.)</span></span>

    <span data-ttu-id="6d294-154">Výsledek by měl vypadat podobně jako v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="6d294-154">The result should resemble the following example.</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. <span data-ttu-id="6d294-155">V odpovědi získáte `access_token`.</span><span class="sxs-lookup"><span data-stu-id="6d294-155">You will get an `access_token` in response.</span></span> <span data-ttu-id="6d294-156">To je to, co potřebujete jako nosný token pro volání rozhraní API doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-156">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="6d294-157">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="6d294-157">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="6d294-158">Odinstalace doplňku</span><span class="sxs-lookup"><span data-stu-id="6d294-158">Uninstall the add-in</span></span>

<span data-ttu-id="6d294-159">Chcete-li doplněk odinstalovat, vyberte **Odinstalovat**.</span><span class="sxs-lookup"><span data-stu-id="6d294-159">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="6d294-160">Obnovte LCS a doplněk Viditelnost zásob bude odebrán.</span><span class="sxs-lookup"><span data-stu-id="6d294-160">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="6d294-161">Proces odinstalace odebere registraci doplňku a také spustí úlohu k vyčištění všech obchodních dat uložených ve službě.</span><span class="sxs-lookup"><span data-stu-id="6d294-161">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="6d294-162">Veřejné rozhraní API doplňku Viditelnosti zásob</span><span class="sxs-lookup"><span data-stu-id="6d294-162">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="6d294-163">Veřejné rozhraní REST API doplňku Viditelnost zásob představuje několik konkrétních koncových bodů integrace.</span><span class="sxs-lookup"><span data-stu-id="6d294-163">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="6d294-164">Podporuje tři hlavní typy interakce:</span><span class="sxs-lookup"><span data-stu-id="6d294-164">It supports three main interaction types:</span></span>

- <span data-ttu-id="6d294-165">Odesílání změn zásob na skladě do doplňku z externího systému.</span><span class="sxs-lookup"><span data-stu-id="6d294-165">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="6d294-166">Dotazování na aktuální množství zásob na skladě z externího systému.</span><span class="sxs-lookup"><span data-stu-id="6d294-166">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="6d294-167">Automatická synchronizace se zásobami na skladě v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6d294-167">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="6d294-168">Automatická synchronizace není součástí veřejného API, ale místo toho se zpracovává na pozadí pro prostředí, která mají povolený doplněk Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-168">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="6d294-169">Ověřování</span><span class="sxs-lookup"><span data-stu-id="6d294-169">Authentication</span></span>

<span data-ttu-id="6d294-170">Token zabezpečení platformy se používá k volání doplňku Viditelnost zásob, takže musíte vygenerovat token Azure Active Directory pomocí vaší aplikace Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6d294-170">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="6d294-171">Další informace o tom, jak získat token zabezpečení, najdete v části [Instalace doplňku Viditelnost zásob](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="6d294-171">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="6d294-172">Konfigurace rozhraní API doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="6d294-172">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="6d294-173">Před použitím služby musíte dokončit konfigurace popsané v následujících pododdílech.</span><span class="sxs-lookup"><span data-stu-id="6d294-173">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="6d294-174">Konfigurace se může lišit v závislosti na podrobnostech vašeho prostředí.</span><span class="sxs-lookup"><span data-stu-id="6d294-174">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="6d294-175">Obsahuje primárně čtyři části:</span><span class="sxs-lookup"><span data-stu-id="6d294-175">It primarily includes four parts:</span></span>

- [<span data-ttu-id="6d294-176">Rozdělení</span><span class="sxs-lookup"><span data-stu-id="6d294-176">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="6d294-177">Konfigurace dimenzí</span><span class="sxs-lookup"><span data-stu-id="6d294-177">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="6d294-178">Indexace</span><span class="sxs-lookup"><span data-stu-id="6d294-178">Indexing</span></span>](#indexing)
- [<span data-ttu-id="6d294-179">Vlastní měrné systémy</span><span class="sxs-lookup"><span data-stu-id="6d294-179">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="6d294-180">Rozdělení</span><span class="sxs-lookup"><span data-stu-id="6d294-180">Partitioning</span></span>

<span data-ttu-id="6d294-181">Rozdělení může významně ovlivnit výkonnost rozhraní API doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-181">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="6d294-182">Je vhodné definovat schéma, které umožňuje malá seskupení dat a přitom umožňuje smysluplné dotazy na data.</span><span class="sxs-lookup"><span data-stu-id="6d294-182">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="6d294-183">`organizationId` (`dataAreaId` v Supply Chain Management) bude vždy součástí rozdělení a ve výchozím nastavení je Viditelnost zásob nastavena na rozdělení podle dimenzí jako *Pracoviště + skladové místo*.</span><span class="sxs-lookup"><span data-stu-id="6d294-183">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="6d294-184">To znamená, že služba musí být vždy dotazována s těmito dimenzemi definovanými na filtrech.</span><span class="sxs-lookup"><span data-stu-id="6d294-184">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="6d294-185">*Pracoviště* a *Skladové místo* jsou dvě obecné výchozí dimenze ve Viditelnosti zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-185">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="6d294-186">V aplikaci Supply Chain Management se tyto dimenze nazývají *Pracoviště* (`InventSiteId`) a *Sklad* (`InventLocationId`).</span><span class="sxs-lookup"><span data-stu-id="6d294-186">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="6d294-187">Konfigurace dimenzí</span><span class="sxs-lookup"><span data-stu-id="6d294-187">Dimension configurations</span></span>

<span data-ttu-id="6d294-188">Viditelnost zásob poskytne seznam obecných výchozích dimenzí umožňujících integraci více zdrojových systémů.</span><span class="sxs-lookup"><span data-stu-id="6d294-188">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="6d294-189">V následující tabulce jsou uvedeny dimenze zásob, které budou výchozími názvy dimenzí v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-189">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="6d294-190">Typ dimenze</span><span class="sxs-lookup"><span data-stu-id="6d294-190">Dimension type</span></span> | <span data-ttu-id="6d294-191">Název dimenze</span><span class="sxs-lookup"><span data-stu-id="6d294-191">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="6d294-192">Produkt</span><span class="sxs-lookup"><span data-stu-id="6d294-192">Product</span></span> | `ColorId` |
| <span data-ttu-id="6d294-193">Produkt</span><span class="sxs-lookup"><span data-stu-id="6d294-193">Product</span></span> | `SizeId` |
| <span data-ttu-id="6d294-194">Produkt</span><span class="sxs-lookup"><span data-stu-id="6d294-194">Product</span></span> | `StyleId` |
| <span data-ttu-id="6d294-195">Produkt</span><span class="sxs-lookup"><span data-stu-id="6d294-195">Product</span></span> | `ConfigId` |
| <span data-ttu-id="6d294-196">Sledování</span><span class="sxs-lookup"><span data-stu-id="6d294-196">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="6d294-197">Sledování</span><span class="sxs-lookup"><span data-stu-id="6d294-197">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="6d294-198">Skladové místo</span><span class="sxs-lookup"><span data-stu-id="6d294-198">Location</span></span> | `LocationId` |
| <span data-ttu-id="6d294-199">Skladové místo</span><span class="sxs-lookup"><span data-stu-id="6d294-199">Location</span></span> | `SiteId` |
| <span data-ttu-id="6d294-200">Stav zásob</span><span class="sxs-lookup"><span data-stu-id="6d294-200">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="6d294-201">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="6d294-201">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="6d294-202">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="6d294-202">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="6d294-203">Specifické pro sklad</span><span class="sxs-lookup"><span data-stu-id="6d294-203">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="6d294-204">Typ dimenze uvedený v předchozí tabulce slouží pouze pro informaci.</span><span class="sxs-lookup"><span data-stu-id="6d294-204">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="6d294-205">V doplňku Viditelnost zásob není nutné definovat typ dimenze.</span><span class="sxs-lookup"><span data-stu-id="6d294-205">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="6d294-206">Pokud vlastní dimenze existuje a je třeba ji přepnout na výchozí hodnotu, když je spotřebována doplňkem Viditelnost zásob, můžete nakonfigurovat název **Vlastní dimenze** v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-206">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="6d294-207">Externí systémy přistupují k doplňku Viditelnost zásob prostřednictvím rozhraní RESTful API, která umožňují dotazování na informace o dostupnosti na skladě u daných sad dimenzí.</span><span class="sxs-lookup"><span data-stu-id="6d294-207">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="6d294-208">Pro integraci vám doplněk Viditelnost zásob umožňuje konfigurovat *externí zdroj dat kanálu* a zdrojovou dimenzi do *cílových dimenzí* v doplňku Viditelnost zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-208">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="6d294-209">Cílové dimenze by měly být jednou z následujících:</span><span class="sxs-lookup"><span data-stu-id="6d294-209">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="6d294-210">Výchozí dimenze v doplňku Viditelnost zásob</span><span class="sxs-lookup"><span data-stu-id="6d294-210">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="6d294-211">Vlastní dimenze</span><span class="sxs-lookup"><span data-stu-id="6d294-211">Custom dimensions</span></span>

<span data-ttu-id="6d294-212">Účelem konfigurace dimenze je standardizovat integraci více systémů pro dotazování na dimenzích a publikování události s dimenzemi.</span><span class="sxs-lookup"><span data-stu-id="6d294-212">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="6d294-213">Indexace</span><span class="sxs-lookup"><span data-stu-id="6d294-213">Indexing</span></span>

<span data-ttu-id="6d294-214">Po většinu času bude dotaz na zásoby na skladě nejen na nejvyšší „celkové“ úrovni, ale možná budete chtít vidět výsledky agregované na základě dimenzí zásob.</span><span class="sxs-lookup"><span data-stu-id="6d294-214">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="6d294-215">Viditelnost zásob poskytuje flexibilitu tím, že umožňuje nastavit indexy, které jsou založeny na dimenzi nebo kombinaci dimenzí.</span><span class="sxs-lookup"><span data-stu-id="6d294-215">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="6d294-216">V současné době můžete indexy nakonfigurovat pouze na maximálně pět.</span><span class="sxs-lookup"><span data-stu-id="6d294-216">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="6d294-217">Před implementací musíte pečlivě zvážit, kterou dimenzi nebo kombinaci dimenzí použijete, abyste zajistili, že bude vyhovovat vašim obchodním potřebám.</span><span class="sxs-lookup"><span data-stu-id="6d294-217">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="6d294-218">Chcete-li se například dotazovat na produkty následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="6d294-218">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="6d294-219">Dotazujte se na agregované zásoby na skladě produktu podle dimenzí *Barva* a *Velikost*.</span><span class="sxs-lookup"><span data-stu-id="6d294-219">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="6d294-220">V některých případech se chcete pouze dotazovat na produkt celkem.</span><span class="sxs-lookup"><span data-stu-id="6d294-220">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="6d294-221">Měli byste dva indexy definované následovně:</span><span class="sxs-lookup"><span data-stu-id="6d294-221">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="6d294-222">Prázdná závorka se agreguje na základě ID produktu v oddílu.</span><span class="sxs-lookup"><span data-stu-id="6d294-222">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="6d294-223">Indexování definuje, jak můžete seskupit výsledky na základě nastavení dotazu `groupBy`.</span><span class="sxs-lookup"><span data-stu-id="6d294-223">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="6d294-224">V tomto případě, pokud nedefinujete žádné hodnoty `groupBy`, získáte součty `productid`.</span><span class="sxs-lookup"><span data-stu-id="6d294-224">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="6d294-225">Jinak pokud definujete `groupBy` jako `groupBy=ColorId&groupBy=SizeId`, vrátí se vám více řádků na základě různých kombinací barev a velikostí v systému.</span><span class="sxs-lookup"><span data-stu-id="6d294-225">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="6d294-226">Kritéria dotazu můžete zadat do textu požadavku.</span><span class="sxs-lookup"><span data-stu-id="6d294-226">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="6d294-227">Zde je ukázkový dotaz na produkt s kombinací barev a velikostí.</span><span class="sxs-lookup"><span data-stu-id="6d294-227">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="6d294-228">Vlastní měrné systémy</span><span class="sxs-lookup"><span data-stu-id="6d294-228">Custom measurement</span></span>

<span data-ttu-id="6d294-229">Výchozí množství měrného systému jsou propojena se Supply Chain Management, můžete však chtít mít množství, které je tvořeno kombinací výchozích měrných systémů.</span><span class="sxs-lookup"><span data-stu-id="6d294-229">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="6d294-230">Chcete-li to provést, můžete mít konfiguraci vlastních množství, která budou přidána k výstupu dotazů na zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="6d294-230">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="6d294-231">Funkce jednoduše umožňuje definovat sadu měrných systémů, které budou přidány, anebo sadu měrných systémů, které budou odečteny, aby bylo možné vytvořit vlastní měrný systém.</span><span class="sxs-lookup"><span data-stu-id="6d294-231">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="6d294-232">Například s následující podmínkou dotazu nakonfigurujete vlastní množství měrné jednotky jako `MyCustomAvailableforReservation`, která má být spotřebována systémem spotřeby.</span><span class="sxs-lookup"><span data-stu-id="6d294-232">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="6d294-233">Systém spotřeby</span><span class="sxs-lookup"><span data-stu-id="6d294-233">Consumption system</span></span> | <span data-ttu-id="6d294-234">Vypočtené měrné jednotky</span><span class="sxs-lookup"><span data-stu-id="6d294-234">Calculated measurers</span></span> | <span data-ttu-id="6d294-235">Zdroj dat</span><span class="sxs-lookup"><span data-stu-id="6d294-235">Data source</span></span> | <span data-ttu-id="6d294-236">Modifikátor</span><span class="sxs-lookup"><span data-stu-id="6d294-236">Modifier</span></span> | <span data-ttu-id="6d294-237">Typ výpočtu modifikátoru</span><span class="sxs-lookup"><span data-stu-id="6d294-237">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="6d294-238">Sčítání</span><span class="sxs-lookup"><span data-stu-id="6d294-238">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="6d294-239">Sčítání</span><span class="sxs-lookup"><span data-stu-id="6d294-239">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="6d294-240">Odčítání</span><span class="sxs-lookup"><span data-stu-id="6d294-240">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="6d294-241">Sčítání</span><span class="sxs-lookup"><span data-stu-id="6d294-241">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="6d294-242">Odčítání</span><span class="sxs-lookup"><span data-stu-id="6d294-242">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="6d294-243">Sčítání</span><span class="sxs-lookup"><span data-stu-id="6d294-243">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="6d294-244">Sčítání</span><span class="sxs-lookup"><span data-stu-id="6d294-244">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="6d294-245">Odčítání</span><span class="sxs-lookup"><span data-stu-id="6d294-245">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="6d294-246">Odčítání</span><span class="sxs-lookup"><span data-stu-id="6d294-246">Subtraction</span></span> |

<span data-ttu-id="6d294-247">Takto dotaz na vlastní množství měrnou jednotku vrátí následující výstup.</span><span class="sxs-lookup"><span data-stu-id="6d294-247">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="6d294-248">Výstup `MyCustomAvailableforReservation` je založen na nastavení výpočtu ve vlastních měrných systémech jako:</span><span class="sxs-lookup"><span data-stu-id="6d294-248">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="6d294-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="6d294-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="6d294-250">Publikování změn množství na skladě</span><span class="sxs-lookup"><span data-stu-id="6d294-250">Posting on-hand changes</span></span>

<span data-ttu-id="6d294-251">Přesná adresa URL, na kterou bude událost publikována, bude záviset na vaší zeměpisné oblasti.</span><span class="sxs-lookup"><span data-stu-id="6d294-251">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="6d294-252">Bude mít formu:</span><span class="sxs-lookup"><span data-stu-id="6d294-252">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="6d294-253">Po ověření lze tuto adresu URL použít společně s metodou HTTP `POST` pro odesílání událostí změny zásob na skladě do služby.</span><span class="sxs-lookup"><span data-stu-id="6d294-253">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="6d294-254">Pro komunikaci se službami Dynamics 365 prostřednictvím požadavků HTTP se používá speciální záhlaví, které označuje ID prostředí instance Supply Chain Management, ke které jsou data propojena.</span><span class="sxs-lookup"><span data-stu-id="6d294-254">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="6d294-255">Například:</span><span class="sxs-lookup"><span data-stu-id="6d294-255">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="6d294-256">Zveřejnění dotazu na změny zásob na skladě - příklad 1</span><span class="sxs-lookup"><span data-stu-id="6d294-256">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="6d294-257">Tento příklad ukazuje scénář, ve kterém nastavíte konfiguraci dimenze v Power Apps.</span><span class="sxs-lookup"><span data-stu-id="6d294-257">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="6d294-258">Pomocí následujícího dotazu nakonfigurujte mapování dimenzí v Power Apps:</span><span class="sxs-lookup"><span data-stu-id="6d294-258">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="6d294-259">Nyní můžete určit `dimensionDataSource` a ve svých dotazech použít vlastní dimenze.</span><span class="sxs-lookup"><span data-stu-id="6d294-259">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="6d294-260">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="6d294-260">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="6d294-261">Zveřejnění dotazu na změny zásob na skladě - příklad 2</span><span class="sxs-lookup"><span data-stu-id="6d294-261">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="6d294-262">Tento příklad ukazuje scénář, kde pro konfiguraci dimenze v nejsou nastavena žádná mapování v Power Apps, takže publikování by mělo také použít základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="6d294-262">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="6d294-263">Všechny dimenze musí být základními dimenzemi, když má pole `dimensionDataSource` hodnotu null, je prázdné nebo má mezeru.</span><span class="sxs-lookup"><span data-stu-id="6d294-263">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="6d294-264">Vlastnosti pole dokumentu JSON</span><span class="sxs-lookup"><span data-stu-id="6d294-264">JSON document field properties</span></span>

<span data-ttu-id="6d294-265">Pole z dříve poskytnutých příkladů dotazů JSON mají vlastnosti uvedené v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="6d294-265">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="6d294-266">ID pole</span><span class="sxs-lookup"><span data-stu-id="6d294-266">Field ID</span></span> | <span data-ttu-id="6d294-267">popis</span><span class="sxs-lookup"><span data-stu-id="6d294-267">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="6d294-268">Jedinečné ID pro konkrétní událost změny.</span><span class="sxs-lookup"><span data-stu-id="6d294-268">A unique ID for the specific change event.</span></span> <span data-ttu-id="6d294-269">Toto ID se používá k zajištění toho, že pokud komunikace se službou během publikování selže, opětovné odeslání události nebude mít za následek, že se v systému dvakrát započítá stejná událost.</span><span class="sxs-lookup"><span data-stu-id="6d294-269">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="6d294-270">Identifikátor organizace spojené s událostí.</span><span class="sxs-lookup"><span data-stu-id="6d294-270">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="6d294-271">To se mapuje na organizace Supply Chain Management nebo ID datové oblasti.</span><span class="sxs-lookup"><span data-stu-id="6d294-271">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="6d294-272">Identifikátor daného produktu.</span><span class="sxs-lookup"><span data-stu-id="6d294-272">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="6d294-273">Množství, o které je třeba změnit zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="6d294-273">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="6d294-274">Pokud by bylo například na polici přidáno 10 nových housek, byla by tato hodnota 10.</span><span class="sxs-lookup"><span data-stu-id="6d294-274">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="6d294-275">Pokud by pak byly 3 housky odebrány z police nebo prodány, byla by tato hodnota -3.</span><span class="sxs-lookup"><span data-stu-id="6d294-275">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="6d294-276">Zdroj dat dimenzí použitých v události změny publikování změny a dotazu.</span><span class="sxs-lookup"><span data-stu-id="6d294-276">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="6d294-277">Pokud zadáte zdroj dat, můžete použít vlastní dimenze ze zadaného zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="6d294-277">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="6d294-278">S konfigurací dimenzí může Viditelnost dat mapovat vlastní dimenze na obecné výchozí dimenze.</span><span class="sxs-lookup"><span data-stu-id="6d294-278">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="6d294-279">Pokud není zadán `dimensionDataSource`, můžete ve svých dotazech použít pouze obecné výchozí dimenze.</span><span class="sxs-lookup"><span data-stu-id="6d294-279">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="6d294-280">Dynamická sada párů klíč/hodnota.</span><span class="sxs-lookup"><span data-stu-id="6d294-280">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="6d294-281">Budou mapovány na některé dimenze v Supply Chain Management, ale můžete také přidat vlastní dimenze (jako *Zdroj*), což může naznačovat, že událost pocházela ze Supply Chain Managementu nebo externího systému.</span><span class="sxs-lookup"><span data-stu-id="6d294-281">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="6d294-282">Dotaz na aktuální zásoby na skladě</span><span class="sxs-lookup"><span data-stu-id="6d294-282">Querying current on-hand</span></span>

<span data-ttu-id="6d294-283">Koncový bod pro dotazování na aktuální zásoby na skladě bude mít podobnou adresu URL:</span><span class="sxs-lookup"><span data-stu-id="6d294-283">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="6d294-284">Bude dotazován pomocí metody HTTP `POST`.</span><span class="sxs-lookup"><span data-stu-id="6d294-284">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="6d294-285">Dotaz na aktuální zásoby na skladě - příklad 1</span><span class="sxs-lookup"><span data-stu-id="6d294-285">Current on-hand query example 1</span></span>

<span data-ttu-id="6d294-286">Tento příklad ukazuje scénář, ve kterém jste dokončili konfiguraci dimenze v Power Apps.</span><span class="sxs-lookup"><span data-stu-id="6d294-286">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="6d294-287">Pomocí následujícího dotazu nakonfigurujte mapování dimenzí v Power Apps:</span><span class="sxs-lookup"><span data-stu-id="6d294-287">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="6d294-288">Nyní můžete určit `dimensionDataSource` a ve svých dotazech použít vlastní dimenze.</span><span class="sxs-lookup"><span data-stu-id="6d294-288">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="6d294-289">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="6d294-289">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="6d294-290">Můžete určit `DimensionDataSource` v `filters` a zadat vlastní dimenze v `filters` i `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="6d294-290">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="6d294-291">Systém automaticky převede vlastní dimenze na základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="6d294-291">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="6d294-292">Dotaz na aktuální zásoby na skladě - příklad 2</span><span class="sxs-lookup"><span data-stu-id="6d294-292">Current on-hand query example 2</span></span>

<span data-ttu-id="6d294-293">Tento příklad ukazuje scénář, kde pro konfiguraci dimenze v nejsou nastavena žádná mapování v Power Apps, takže publikování by mělo také použít základní dimenze.</span><span class="sxs-lookup"><span data-stu-id="6d294-293">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="6d294-294">Všechny dimenze musí být základními dimenzemi, když má pole `dimensionDataSource` pod `filters` hodnotu null nebo mezeru.</span><span class="sxs-lookup"><span data-stu-id="6d294-294">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="6d294-295">Příklad výsledku vrácení</span><span class="sxs-lookup"><span data-stu-id="6d294-295">Example return result</span></span>

<span data-ttu-id="6d294-296">Dotazy zobrazené v předchozích příkladech by mohly vrátit takový výsledek.</span><span class="sxs-lookup"><span data-stu-id="6d294-296">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="6d294-297">Všimněte si, že pole množství jsou strukturována jako slovník měrných jednotek a jejich přidružených hodnot.</span><span class="sxs-lookup"><span data-stu-id="6d294-297">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>

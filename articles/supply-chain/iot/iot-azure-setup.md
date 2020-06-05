---
title: Nastavení zdrojů Azure pro IoT Intelligence
description: Toto téma vysvětluje, jak vytvořit a konfigurovat zdroje Microsoft Azure, které potřebujete pro IoT Intelligence.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1f05f597f86df602c0e00af006b7ccf804f50929
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386495"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="fcb39-103">Nastavení zdrojů Azure pro IoT Intelligence</span><span class="sxs-lookup"><span data-stu-id="fcb39-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fcb39-104">Toto téma vysvětluje, jak vytvořit a konfigurovat zdroje Microsoft Azure, které potřebujete pro IoT Intelligence.</span><span class="sxs-lookup"><span data-stu-id="fcb39-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="fcb39-105">Vytvoření zdrojů Azure</span><span class="sxs-lookup"><span data-stu-id="fcb39-105">Create Azure resources</span></span>

<span data-ttu-id="fcb39-106">Takto vytvořte centrum IoT, Redis Cache a úložiště klíčů, ke kterým může přistupovat aplikace Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fcb39-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="fcb39-107">Ověření, za je ID aplikace první strany Microsoft Dynamics ERP Microservices na vašem klientovi</span><span class="sxs-lookup"><span data-stu-id="fcb39-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="fcb39-108">Chcete-li ověřit, že ID aplikace první strany pro Microsoft Dynamics ERP Microservices je na vašem klientovi, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="fcb39-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="fcb39-109">Přihlaste se do portálu Azure na <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="fcb39-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="fcb39-110">Přejděte na **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="fcb39-111">Přejděte na **Podnikové aplikace**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="fcb39-112">V poli **Typ aplikace** vyberte **Aplikace společnosti Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="fcb39-113">Do pole pro vyhledávání zadejte **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="fcb39-114">Ověřte, že je **Microsoft Dynamics ERP Microservices** v seznamu.</span><span class="sxs-lookup"><span data-stu-id="fcb39-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="fcb39-115">Ostatní aplikace mají podobné názvy.</span><span class="sxs-lookup"><span data-stu-id="fcb39-115">Other applications have similar names.</span></span> <span data-ttu-id="fcb39-116">Proto ověřte, že vyhledáte správnou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="fcb39-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="fcb39-117">ID aplikace je **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="fcb39-118">Pokud aplikace není v seznamu, musíte ji přidat ke svému klientovi:</span><span class="sxs-lookup"><span data-stu-id="fcb39-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="fcb39-119">V portálu Azure na panelu nástrojů vyberte tlačítko a otevřete Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="fcb39-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="fcb39-120">Spusťte příkaz **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="fcb39-121">Zadejte **Y** pro instalaci modulu.</span><span class="sxs-lookup"><span data-stu-id="fcb39-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="fcb39-122">Spusťte příkaz **Get-InstalledModule -Name "AzureAD"** k ověření, že je modul nainstalován.</span><span class="sxs-lookup"><span data-stu-id="fcb39-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="fcb39-123">Spusťte příkaz **Connect-AzureAD - Confirm** pro spuštění ověření.</span><span class="sxs-lookup"><span data-stu-id="fcb39-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="fcb39-124">Spusťte příkaz **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="fcb39-125">Nyní můžete opakovat kroky 1 až 6 a ověřit, že ID aplikace je ve vašem klientovi.</span><span class="sxs-lookup"><span data-stu-id="fcb39-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="fcb39-126">Vytvoření zdroje úložiště klíčů</span><span class="sxs-lookup"><span data-stu-id="fcb39-126">Create a key vault resource</span></span>

<span data-ttu-id="fcb39-127">Při vytváření zdroje úložiště klíčů postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="fcb39-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="fcb39-128">Na portálu Azure vytvořte nebo přejděte do skupiny zdrojů.</span><span class="sxs-lookup"><span data-stu-id="fcb39-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="fcb39-129">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-129">Select **Add**.</span></span>
3. <span data-ttu-id="fcb39-130">Na stránce **Nový** zadejte do vyhledávacího pole **Úložiště klíčů**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="fcb39-131">Pak vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-131">Then select **Create**.</span></span>
4. <span data-ttu-id="fcb39-132">Na stránce **Vytvoření úložiště** v poli **Úložiště klíčů** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="fcb39-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="fcb39-133">Zkontrolujte výchozí hodnoty a poté vyberte **Zkontrolovat a vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="fcb39-134">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-134">Select **Create**.</span></span>

<span data-ttu-id="fcb39-135">Úložiště klíčů se vytvoří na pozadí.</span><span class="sxs-lookup"><span data-stu-id="fcb39-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="fcb39-136">Vytvoření zdroje centra IoT</span><span class="sxs-lookup"><span data-stu-id="fcb39-136">Create an IoT hub resource</span></span>

<span data-ttu-id="fcb39-137">Při vytváření zdroje centra IoT postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="fcb39-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="fcb39-138">Vytvořte nebo přejděte na skupinu zdrojů.</span><span class="sxs-lookup"><span data-stu-id="fcb39-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="fcb39-139">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-139">Select **Add**.</span></span>
3. <span data-ttu-id="fcb39-140">Na stránce **Nový** zadejte do vyhledávacího pole **Centrum IoT**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="fcb39-141">Pak vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-141">Then select **Create**.</span></span>
4. <span data-ttu-id="fcb39-142">Do pole **Název centra IoT** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="fcb39-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="fcb39-143">Zkontrolujte výchozí hodnoty a poté vyberte **Zkontrolovat a vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="fcb39-144">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-144">Select **Create**.</span></span>

<span data-ttu-id="fcb39-145">Centrum IoT se vytvoří na pozadí.</span><span class="sxs-lookup"><span data-stu-id="fcb39-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="fcb39-146">Doporučujeme vytvořit pouze jeden zdroj centra IoT pro každé prostředí.</span><span class="sxs-lookup"><span data-stu-id="fcb39-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="fcb39-147">Vytvoření zdroje Redis Cache</span><span class="sxs-lookup"><span data-stu-id="fcb39-147">Create a Redis cache resource</span></span>

<span data-ttu-id="fcb39-148">Při vytváření zdroje Redis Cache postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="fcb39-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="fcb39-149">Vytvořte nebo přejděte na skupinu zdrojů.</span><span class="sxs-lookup"><span data-stu-id="fcb39-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="fcb39-150">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-150">Select **Add**.</span></span>
3. <span data-ttu-id="fcb39-151">Na stránce **Nový** zadejte do vyhledávacího pole **Azure Cache for Redis**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="fcb39-152">Pak vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-152">Then select **Create**.</span></span>
4. <span data-ttu-id="fcb39-153">Do pole **Název DNS** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="fcb39-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="fcb39-154">Zkontrolujte výchozí hodnoty a poté vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="fcb39-155">Redis Cache se vytvoří na pozadí.</span><span class="sxs-lookup"><span data-stu-id="fcb39-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="fcb39-156">Doporučujeme vytvořit pouze jeden zdroj Redis Cache pro každé prostředí.</span><span class="sxs-lookup"><span data-stu-id="fcb39-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="fcb39-157">Všechny zdroje byly nyní vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="fcb39-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="fcb39-158">Konfigurace zdrojů Azure</span><span class="sxs-lookup"><span data-stu-id="fcb39-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="fcb39-159">Konfigurace centra IoT</span><span class="sxs-lookup"><span data-stu-id="fcb39-159">Configure the IoT hub</span></span>

<span data-ttu-id="fcb39-160">Pro nakonfigurování centra IoT postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="fcb39-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="fcb39-161">Ve svých zdrojích vyberte zdroj centra IoT.</span><span class="sxs-lookup"><span data-stu-id="fcb39-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="fcb39-162">V levém navigačním podokně vyberte možnost **Vestavěné koncové body**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="fcb39-163">Pod možností **Skupiny spotřebitelů** vložte následující skupiny spotřebitelů.</span><span class="sxs-lookup"><span data-stu-id="fcb39-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="fcb39-164">Tyto skupiny spotřebitelů odpovídají vestavěným scénářům.</span><span class="sxs-lookup"><span data-stu-id="fcb39-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="fcb39-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="fcb39-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="fcb39-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="fcb39-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="fcb39-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="fcb39-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="fcb39-168">Konfigurace úložiště klíčů</span><span class="sxs-lookup"><span data-stu-id="fcb39-168">Configure the key vault</span></span>

<span data-ttu-id="fcb39-169">Pro konfiguraci úložiště klíčů postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="fcb39-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="fcb39-170">Ve svých zdrojích vyberte zdroj úložiště klíčů.</span><span class="sxs-lookup"><span data-stu-id="fcb39-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="fcb39-171">V levém navigačním podokně nalevo vyberte položku **Zásady přístupu**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="fcb39-172">Vyberte **Přidat zásadu přístupu**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="fcb39-173">Na stránce **Přidat zásadu přístupu** v poli **Oprávnění na základě tajných kódů** vyberte **Získat** a **Seznam**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="fcb39-174">Klikněte na **Výběr objektu zabezpečení**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="fcb39-175">V dialogovém okně **Objekt zabezpečení** vyhledejte a vyberte **Microsoft Dynamics ERP Microservices**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="fcb39-176">Zvolte **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-176">Then select **Select**.</span></span>
7. <span data-ttu-id="fcb39-177">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-177">Select **Add**.</span></span>
8. <span data-ttu-id="fcb39-178">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-178">Select **Save**.</span></span>

<span data-ttu-id="fcb39-179">Aplikace má nyní přístup k tajným klíčům v úložišti klíčů.</span><span class="sxs-lookup"><span data-stu-id="fcb39-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="fcb39-180">Uložení tajného klíče řetězce připojení centra IoT</span><span class="sxs-lookup"><span data-stu-id="fcb39-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="fcb39-181">Chcete-li uložit tajný klíč připojovacího řetězce centra IoT, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="fcb39-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="fcb39-182">Ve svých zdrojích vyberte zdroj centra IoT.</span><span class="sxs-lookup"><span data-stu-id="fcb39-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="fcb39-183">V levém navigačním podokně vyberte možnost **Vestavěné koncové body**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="fcb39-184">Zkopírujte hodnotu do pole **Koncový bod kompatibilní s centrem událostí**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="fcb39-185">Přejděte do zdroje úložiště klíčů.</span><span class="sxs-lookup"><span data-stu-id="fcb39-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="fcb39-186">V levém navigačním podokně vyberte položku **Tajné klíče**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="fcb39-187">Vyberte **Generovat/import**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="fcb39-188">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="fcb39-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="fcb39-189">V poli **Hodnota** vložte hodnotu koncového bodu, kterou jste zkopírovali dříve.</span><span class="sxs-lookup"><span data-stu-id="fcb39-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="fcb39-190">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="fcb39-191">Uložení tajného klíče řetězce připojení Redis Cache</span><span class="sxs-lookup"><span data-stu-id="fcb39-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="fcb39-192">Chcete-li uložit tajný klíč připojovacího řetězce centra Redis Cache, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="fcb39-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="fcb39-193">Ve svých zdrojích vyberte zdroj Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="fcb39-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="fcb39-194">Vyberte **Přístupové klíče**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="fcb39-195">Zkopírujte hodnotu do pole **Primární připojovací řetězec**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="fcb39-196">Přejděte do zdroje úložiště klíčů.</span><span class="sxs-lookup"><span data-stu-id="fcb39-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="fcb39-197">V levém navigačním podokně vyberte položku **Tajné klíče**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="fcb39-198">Vyberte **Generovat/import**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="fcb39-199">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="fcb39-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="fcb39-200">V poli **Hodnota** vložte hodnotu připojovacího řetězce, kterou jste zkopírovali dříve.</span><span class="sxs-lookup"><span data-stu-id="fcb39-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="fcb39-201">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="fcb39-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="fcb39-202">Kdykoli aktualizujete jeden z připojovacích řetězců, musíte také aktualizovat hodnoty tajných klíčů.</span><span class="sxs-lookup"><span data-stu-id="fcb39-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="fcb39-203">Nyní jste dokončili zřízení požadovaných zdrojů Azure.</span><span class="sxs-lookup"><span data-stu-id="fcb39-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="fcb39-204">Dalším krokem je [instalace doplňku IoT Intelligence v Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="fcb39-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

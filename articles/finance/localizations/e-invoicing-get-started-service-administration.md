---
title: Začínáme se správou služby doplňky elektronické fakturace
description: Toto téma poskytuje informace, jak začít s doplňkem elektronické fakturace.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592519"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="edbf6-103">Začínáme se správou služby doplňky elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="edbf6-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="edbf6-104">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="edbf6-104">Prerequisites</span></span>

<span data-ttu-id="edbf6-105">Než provedete postupy v tomto tématu, musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="edbf6-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="edbf6-106">Musíte mít přístup ke svému účtu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="edbf6-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="edbf6-107">Musíte mít projekt LCS, který obsahuje verzi 10.0.17 nebo novější nástroje Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="edbf6-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="edbf6-108">Kromě toho musí být tyto aplikace nasazeny v jedné z následujících geografických oblastí Azure:</span><span class="sxs-lookup"><span data-stu-id="edbf6-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="edbf6-109">Východní USA</span><span class="sxs-lookup"><span data-stu-id="edbf6-109">East US</span></span>
    - <span data-ttu-id="edbf6-110">USA – západ</span><span class="sxs-lookup"><span data-stu-id="edbf6-110">West US</span></span>
    - <span data-ttu-id="edbf6-111">Sever EU</span><span class="sxs-lookup"><span data-stu-id="edbf6-111">North EU</span></span>
    - <span data-ttu-id="edbf6-112">Západ EU</span><span class="sxs-lookup"><span data-stu-id="edbf6-112">West EU</span></span>

- <span data-ttu-id="edbf6-113">Musíte mít přístup ke svému účtu Dynamics 365 Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="edbf6-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="edbf6-114">Musíte aktivovat funkci Globalizace pro svůj účet RCS v modulu Správa funkcí.</span><span class="sxs-lookup"><span data-stu-id="edbf6-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="edbf6-115">Pro více informací viz [Regulatory Configuration Services (RCS) - funkce globalizace](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="edbf6-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="edbf6-116">Musíte vytvořit trezor klíčů a účet úložiště Azure.</span><span class="sxs-lookup"><span data-stu-id="edbf6-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="edbf6-117">Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="edbf6-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="edbf6-118">Nainstalujte doplněk pro mikroslužby ve službě Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="edbf6-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="edbf6-119">Přihlaste se k účtu LCS.</span><span class="sxs-lookup"><span data-stu-id="edbf6-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="edbf6-120">Vyberte dlaždici **Náhled správy funkcí**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="edbf6-121">V části **Funkce Public Preview** vyberte **služba elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="edbf6-122">Ujistěte se, zda je možnost **Funkce Preview zapnuta** nastavena na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="edbf6-123">Na řídicím panelu LCS vyberte svůj projekt nasazení LCS.</span><span class="sxs-lookup"><span data-stu-id="edbf6-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="edbf6-124">Projekt LCS musí být spuštěný.</span><span class="sxs-lookup"><span data-stu-id="edbf6-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="edbf6-125">Na kartě **Doplňky prostředí** vyberte **Nainstalujte nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="edbf6-126">Vyberte **Služby elektronické fakturace** a v poli **ID aplikace AAD** zadejte **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="edbf6-127">Toto je pevná hodnota.</span><span class="sxs-lookup"><span data-stu-id="edbf6-127">This is a fixed value.</span></span>
10. <span data-ttu-id="edbf6-128">V poli **ID klienta AAD** zadejte ID tenanta účtu předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="edbf6-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="edbf6-129">Zkontrolujte smluvní podmínky a poté zaškrtněte políčko.</span><span class="sxs-lookup"><span data-stu-id="edbf6-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="edbf6-130">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="edbf6-131">Nastavení parametrů pro integraci RCS s doplňkem elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="edbf6-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="edbf6-132">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="edbf6-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="edbf6-133">V pracovním prostoru **Elektronické výkaznictví** v části **Související odkazy** vyberte **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="edbf6-134">Na kartě **Služba elektronické fakturace** v poli **Identifikátor URI koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Azure, jak je znázorněno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="edbf6-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="edbf6-135">Geografie datového centra Azure</span><span class="sxs-lookup"><span data-stu-id="edbf6-135">Datacenter Azure geography</span></span> | <span data-ttu-id="edbf6-136">URI adresa koncového bodu služby</span><span class="sxs-lookup"><span data-stu-id="edbf6-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="edbf6-137">Východní USA</span><span class="sxs-lookup"><span data-stu-id="edbf6-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="edbf6-138">USA – západ</span><span class="sxs-lookup"><span data-stu-id="edbf6-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="edbf6-139">Sever EU</span><span class="sxs-lookup"><span data-stu-id="edbf6-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="edbf6-140">Západ EU</span><span class="sxs-lookup"><span data-stu-id="edbf6-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="edbf6-141">Ověřte, zda je pole **Id aplikace** nastaveno na **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="edbf6-142">Tato hodnota je pevná hodnota.</span><span class="sxs-lookup"><span data-stu-id="edbf6-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="edbf6-143">V poli **ID prostředí LCS** zadejte ID účtu předplatného LCS.</span><span class="sxs-lookup"><span data-stu-id="edbf6-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="edbf6-144">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="edbf6-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="edbf6-145">Vytvoření tajného kódu Key Vault</span><span class="sxs-lookup"><span data-stu-id="edbf6-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="edbf6-146">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="edbf6-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="edbf6-147">V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Doplněk elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="edbf6-148">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby** a potom vyberte **Parametry Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="edbf6-149">Vyberte možnost **Nový** k vytvoření tajného kódu trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="edbf6-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="edbf6-150">Do pole **Název** zadejte název tajného kódu trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="edbf6-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="edbf6-151">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="edbf6-152">Do pole **Identifikátoru URI Key Vault** vložte tajný kód z Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="edbf6-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="edbf6-153">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="edbf6-154">Vytvoření tajného kódu účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="edbf6-154">Create Storage account secret</span></span>

1. <span data-ttu-id="edbf6-155">Přejděte na **Správa systému** > **Nastavit** > **Parametry trezoru klíčů** a vyberte tajný klíč trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="edbf6-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="edbf6-156">V části **Certifikáty** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="edbf6-157">V poli **Název** zadejte název tajného klíče účtu úložiště a do pole **Popis** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="edbf6-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="edbf6-158">V poli **Typ** vyberte **Certifikát**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="edbf6-159">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="edbf6-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="edbf6-160">Vytvoření tajného klíče digitálního certifikátu</span><span class="sxs-lookup"><span data-stu-id="edbf6-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="edbf6-161">Přejděte na **Správa systému** > **Nastavit** > **Parametry trezoru klíčů** a vyberte tajný klíč trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="edbf6-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="edbf6-162">V části **Certifikáty** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="edbf6-163">V poli **Název** zadejte název tajného klíče digitálního certifikátu a do pole **Popis** zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="edbf6-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="edbf6-164">V poli **Typ** vyberte **Certifikát**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="edbf6-165">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="edbf6-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="edbf6-166">Vytvoření prostředí doplňku elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="edbf6-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="edbf6-167">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="edbf6-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="edbf6-168">V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Doplněk elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="edbf6-169">Vytvoření servisního prostředí</span><span class="sxs-lookup"><span data-stu-id="edbf6-169">Create a service environment</span></span>

1. <span data-ttu-id="edbf6-170">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="edbf6-171">Vyberte **Nový** pro vytvoření nového prostředí služby.</span><span class="sxs-lookup"><span data-stu-id="edbf6-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="edbf6-172">Do pole **Název** zadejte název prostředí elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="edbf6-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="edbf6-173">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="edbf6-174">V poli **Tajný klíč tokenu SAS úložiště** vyberte název tajného klíče účtu úložiště, který se musí použít k ověření přístupu k účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="edbf6-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="edbf6-175">V části **Uživatelé** vyberte **Přidat**, chcete-li přidat uživatele, který má povoleno odesílat elektronické faktury prostřednictvím prostředí a také se připojit k účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="edbf6-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="edbf6-176">Do pole **ID uživatele** zadejte alias uživatele.</span><span class="sxs-lookup"><span data-stu-id="edbf6-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="edbf6-177">Do pole **E-mail** zadejte e-mailovou adresu uživatele.</span><span class="sxs-lookup"><span data-stu-id="edbf6-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="edbf6-178">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-178">Select **Save**.</span></span>
8. <span data-ttu-id="edbf6-179">Pokud faktury pro vaši zemi/region vyžadují pro použití digitálních podpisů řetězec certifikátů, v podokně akcí vyberte **Parametry Key Vault** a poté zadejte **Sekvence certifikátů** a postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="edbf6-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="edbf6-180">Vyberte **Nový** k vytvoření sekvence certifikátů.</span><span class="sxs-lookup"><span data-stu-id="edbf6-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="edbf6-181">Do pole **Název** zadejte název sekvence certifikátů.</span><span class="sxs-lookup"><span data-stu-id="edbf6-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="edbf6-182">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="edbf6-183">V části **Certifikáty** vyberte **Přidat**, abyste přidali certifikát do sekvence.</span><span class="sxs-lookup"><span data-stu-id="edbf6-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="edbf6-184">Pomocí tlačítek **Nahoru** a **Dolů** změňte polohu certifikátu v řetězci.</span><span class="sxs-lookup"><span data-stu-id="edbf6-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="edbf6-185">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="edbf6-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="edbf6-186">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="edbf6-186">Close the page.</span></span>
9. <span data-ttu-id="edbf6-187">Na stránce **Prostředí služby** v podokně akcí vyberte **Publikovat**, chcete-li publikovat prostředí do cloudu.</span><span class="sxs-lookup"><span data-stu-id="edbf6-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="edbf6-188">Hodnota pole **Stav** se změní na **Publikováno**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="edbf6-189">Vytvoření propojené aplikace</span><span class="sxs-lookup"><span data-stu-id="edbf6-189">Create a connected application</span></span>

1. <span data-ttu-id="edbf6-190">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Propojené aplikace**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="edbf6-191">Zvolte **Nový** pro vytvoření propojené aplikace.</span><span class="sxs-lookup"><span data-stu-id="edbf6-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="edbf6-192">Do pole **Název** zadejte název aplikace, ke které se má provést připojení.</span><span class="sxs-lookup"><span data-stu-id="edbf6-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="edbf6-193">Do pole **Aplikace** zadejte adresu URL prostředí Finance and Supply Chain Management pro připojení.</span><span class="sxs-lookup"><span data-stu-id="edbf6-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="edbf6-194">Do pole **Klient** zadejte klienta prostředí Finance and Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="edbf6-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="edbf6-195">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-195">Select **Save**.</span></span>
6. <span data-ttu-id="edbf6-196">V podokně akcí vyberte **Zkontrolovat připojení**, abyste otestovali spojení s prostředím.</span><span class="sxs-lookup"><span data-stu-id="edbf6-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="edbf6-197">Poté stránku zavřete.</span><span class="sxs-lookup"><span data-stu-id="edbf6-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="edbf6-198">Propojení připojených aplikace s prostředím</span><span class="sxs-lookup"><span data-stu-id="edbf6-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="edbf6-199">Na stránce **Nastavení prostředí** vyberte **Nový** a přiřaďte připojenou aplikaci prostředí.</span><span class="sxs-lookup"><span data-stu-id="edbf6-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="edbf6-200">V poli **Připojená aplikace** vyberte připojenou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="edbf6-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="edbf6-201">V poli **Prostředí služby** vyberte prostředí služeb.</span><span class="sxs-lookup"><span data-stu-id="edbf6-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="edbf6-202">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="edbf6-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="edbf6-203">Nastavte integraci doplňku elektronické fakturace ve Finance a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="edbf6-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="edbf6-204">Zapněte funkci integrace doplňku elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="edbf6-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="edbf6-205">Přihlaste se k instanci Finance nebo Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="edbf6-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="edbf6-206">V pracovním prostoru **Správa funkcí** vyhledejte funkci **Integrace doplňku elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="edbf6-207">Pokud se tato funkce na stránce neobjeví, vyberte **Zkontrolovat aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="edbf6-208">Vyberte funkci a poté vyberte tlačítko **Povolit nyní**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="edbf6-209">Nastavte adresu URL koncového bodu služby</span><span class="sxs-lookup"><span data-stu-id="edbf6-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="edbf6-210">Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="edbf6-211">Na kartě **Služba odeslání** v poli **Identifikátor URL koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Azure, jak je znázorněno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="edbf6-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="edbf6-212">Geografie datového centra Azure</span><span class="sxs-lookup"><span data-stu-id="edbf6-212">Datacenter Azure geography</span></span> | <span data-ttu-id="edbf6-213">URL adresa koncového bodu služby</span><span class="sxs-lookup"><span data-stu-id="edbf6-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="edbf6-214">Východní USA</span><span class="sxs-lookup"><span data-stu-id="edbf6-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="edbf6-215">USA – západ</span><span class="sxs-lookup"><span data-stu-id="edbf6-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="edbf6-216">Sever EU</span><span class="sxs-lookup"><span data-stu-id="edbf6-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="edbf6-217">Západ EU</span><span class="sxs-lookup"><span data-stu-id="edbf6-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="edbf6-218">Do pole **Prostředí** zadejte název prostředí doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="edbf6-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="edbf6-219">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="edbf6-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

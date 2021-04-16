---
title: Začínáme se správou služby Elektronické fakturace
description: Toto téma poskytuje informace, jak začít s Elektronickou fakturací.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840141"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="20d97-103">Začínáme se správou služby Elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="20d97-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="20d97-104">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="20d97-104">Prerequisites</span></span>

<span data-ttu-id="20d97-105">Než provedete postupy v tomto tématu, musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="20d97-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="20d97-106">Musíte mít přístup ke svému účtu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="20d97-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="20d97-107">Musíte mít projekt LCS, který obsahuje verzi 10.0.17 nebo novější nástroje Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="20d97-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="20d97-108">Kromě toho musí být tyto aplikace nasazeny v jedné z následujících geografických oblastí Azure:</span><span class="sxs-lookup"><span data-stu-id="20d97-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="20d97-109">Východní USA</span><span class="sxs-lookup"><span data-stu-id="20d97-109">East US</span></span>
    - <span data-ttu-id="20d97-110">USA – západ</span><span class="sxs-lookup"><span data-stu-id="20d97-110">West US</span></span>
    - <span data-ttu-id="20d97-111">Sever EU</span><span class="sxs-lookup"><span data-stu-id="20d97-111">North EU</span></span>
    - <span data-ttu-id="20d97-112">Západ EU</span><span class="sxs-lookup"><span data-stu-id="20d97-112">West EU</span></span>

- <span data-ttu-id="20d97-113">Musíte mít přístup ke svému účtu Dynamics 365 Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="20d97-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="20d97-114">Musíte aktivovat funkci Globalizace pro svůj účet RCS v modulu Správa funkcí.</span><span class="sxs-lookup"><span data-stu-id="20d97-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="20d97-115">Pro více informací viz [Regulatory Configuration Services (RCS) - funkce globalizace](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="20d97-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="20d97-116">Musíte vytvořit trezor klíčů a účet úložiště Azure.</span><span class="sxs-lookup"><span data-stu-id="20d97-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="20d97-117">Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="20d97-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="20d97-118">Nainstalujte doplněk pro mikroslužby ve službě Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="20d97-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="20d97-119">Přihlaste se k účtu LCS.</span><span class="sxs-lookup"><span data-stu-id="20d97-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="20d97-120">Vyberte dlaždici **Náhled správy funkcí**.</span><span class="sxs-lookup"><span data-stu-id="20d97-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="20d97-121">V části **Funkce Public Preview** vyberte **služba elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="20d97-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="20d97-122">Ujistěte se, zda je možnost **Funkce Preview zapnuta** nastavena na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="20d97-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="20d97-123">Na řídicím panelu LCS vyberte svůj projekt nasazení LCS.</span><span class="sxs-lookup"><span data-stu-id="20d97-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="20d97-124">Projekt LCS musí být spuštěný.</span><span class="sxs-lookup"><span data-stu-id="20d97-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="20d97-125">Na kartě **Doplňky prostředí** vyberte **Nainstalujte nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="20d97-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="20d97-126">Vyberte **Služby elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="20d97-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="20d97-127">V poli **ID aplikace AAD** zadejte **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="20d97-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="20d97-128">Toto je pevná hodnota.</span><span class="sxs-lookup"><span data-stu-id="20d97-128">This is a fixed value.</span></span>
10. <span data-ttu-id="20d97-129">V poli **ID klienta AAD** zadejte ID tenanta účtu předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="20d97-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="20d97-130">Zkontrolujte smluvní podmínky a poté zaškrtněte políčko.</span><span class="sxs-lookup"><span data-stu-id="20d97-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="20d97-131">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="20d97-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="20d97-132">Nastavení parametrů pro integraci RCS s Elektronickou fakturací</span><span class="sxs-lookup"><span data-stu-id="20d97-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="20d97-133">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="20d97-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="20d97-134">V pracovním prostoru **Elektronické výkaznictví** v části **Související odkazy** vyberte **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="20d97-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="20d97-135">Na kartě **Služba elektronické fakturace** v poli **Identifikátor URI koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Azure, jak je znázorněno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="20d97-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="20d97-136">Geografie datového centra Azure</span><span class="sxs-lookup"><span data-stu-id="20d97-136">Datacenter Azure geography</span></span> | <span data-ttu-id="20d97-137">URI adresa koncového bodu služby</span><span class="sxs-lookup"><span data-stu-id="20d97-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="20d97-138">Východní USA</span><span class="sxs-lookup"><span data-stu-id="20d97-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="20d97-139">USA – západ</span><span class="sxs-lookup"><span data-stu-id="20d97-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="20d97-140">Sever EU</span><span class="sxs-lookup"><span data-stu-id="20d97-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="20d97-141">Západ EU</span><span class="sxs-lookup"><span data-stu-id="20d97-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="20d97-142">Ověřte, zda je pole **Id aplikace** nastaveno na **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="20d97-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="20d97-143">Tato hodnota je pevná hodnota.</span><span class="sxs-lookup"><span data-stu-id="20d97-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="20d97-144">V poli **ID prostředí LCS** zadejte ID prostředí LCS.</span><span class="sxs-lookup"><span data-stu-id="20d97-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="20d97-145">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="20d97-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="20d97-146">Vytvoření referencí úložiště klíčů</span><span class="sxs-lookup"><span data-stu-id="20d97-146">Create Key Vault references</span></span>

1. <span data-ttu-id="20d97-147">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="20d97-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="20d97-148">V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Elektronická fakturace**.</span><span class="sxs-lookup"><span data-stu-id="20d97-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="20d97-149">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby** a potom vyberte **Parametry Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="20d97-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="20d97-150">Vyberte možnost **Nová** k vytvoření reference trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="20d97-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="20d97-151">Do pole **Název** zadejte název reference trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="20d97-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="20d97-152">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="20d97-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="20d97-153">Do pole **URI trezoru klíčů** vložte tajný kód trezoru klíčů z Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="20d97-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="20d97-154">Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="20d97-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="20d97-155">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="20d97-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="20d97-156">Vytvoření tajného kódu účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="20d97-156">Create Storage account secret</span></span>

1. <span data-ttu-id="20d97-157">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby** >  **Parametry trezoru klíčů**.</span><span class="sxs-lookup"><span data-stu-id="20d97-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="20d97-158">Vyberte **Reference trezoru klíčů** a v části **Certifikáty** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="20d97-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="20d97-159">Do pole **Název** zadejte název tajného kódu účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="20d97-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="20d97-160">Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="20d97-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="20d97-161">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="20d97-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="20d97-162">V poli **Typ** vyberte **Tajný klíč**.</span><span class="sxs-lookup"><span data-stu-id="20d97-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="20d97-163">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="20d97-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="20d97-164">Vytvoření tajného klíče digitálního certifikátu</span><span class="sxs-lookup"><span data-stu-id="20d97-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="20d97-165">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby** a potom vyberte **Parametry trezoru klíčů**.</span><span class="sxs-lookup"><span data-stu-id="20d97-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="20d97-166">Vyberte **Reference trezoru klíčů** a poté v části **Certifikáty** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="20d97-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="20d97-167">Do pole **Název** zadejte název tajného kódu digitálního certifikátu.</span><span class="sxs-lookup"><span data-stu-id="20d97-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="20d97-168">Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="20d97-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="20d97-169">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="20d97-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="20d97-170">V poli **Typ** vyberte **Certifikát**.</span><span class="sxs-lookup"><span data-stu-id="20d97-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="20d97-171">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="20d97-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="20d97-172">Vytvoření servisního prostředí</span><span class="sxs-lookup"><span data-stu-id="20d97-172">Create a service environment</span></span>

1. <span data-ttu-id="20d97-173">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="20d97-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="20d97-174">V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Elektronická fakturace**.</span><span class="sxs-lookup"><span data-stu-id="20d97-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="20d97-175">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby**.</span><span class="sxs-lookup"><span data-stu-id="20d97-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="20d97-176">Vyberte **Nový** pro vytvoření nového prostředí služby.</span><span class="sxs-lookup"><span data-stu-id="20d97-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="20d97-177">Do pole **Název** zadejte název prostředí elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="20d97-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="20d97-178">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="20d97-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="20d97-179">V poli **Tajný klíč tokenu SAS úložiště** vyberte název tajného klíče účtu úložiště, který se musí použít k ověření přístupu k účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="20d97-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="20d97-180">V části **Uživatelé** vyberte **Přidat**, chcete-li přidat uživatele, který má povoleno odesílat elektronické faktury prostřednictvím prostředí a také se připojit k účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="20d97-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="20d97-181">Do pole **ID uživatele** zadejte alias uživatele.</span><span class="sxs-lookup"><span data-stu-id="20d97-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="20d97-182">Do pole **E-mail** zadejte e-mailovou adresu uživatele.</span><span class="sxs-lookup"><span data-stu-id="20d97-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="20d97-183">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="20d97-183">Select **Save**.</span></span>
10. <span data-ttu-id="20d97-184">Pokud faktury pro vaši zemi/region vyžadují pro použití digitálních podpisů řetězec certifikátů, v podokně akcí vyberte **Parametry Key Vault** a poté zadejte **Sekvence certifikátů** a postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="20d97-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="20d97-185">Vyberte **Nový** k vytvoření sekvence certifikátů.</span><span class="sxs-lookup"><span data-stu-id="20d97-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="20d97-186">Do pole **Název** zadejte název sekvence certifikátů.</span><span class="sxs-lookup"><span data-stu-id="20d97-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="20d97-187">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="20d97-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="20d97-188">V části **Certifikáty** vyberte **Přidat**, abyste přidali certifikát do sekvence.</span><span class="sxs-lookup"><span data-stu-id="20d97-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="20d97-189">Pomocí tlačítek **Nahoru** a **Dolů** změňte polohu certifikátu v řetězci.</span><span class="sxs-lookup"><span data-stu-id="20d97-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="20d97-190">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="20d97-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="20d97-191">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="20d97-191">Close the page.</span></span>
11. <span data-ttu-id="20d97-192">Na stránce **Prostředí služby** v podokně akcí vyberte **Publikovat**, chcete-li publikovat prostředí do cloudu.</span><span class="sxs-lookup"><span data-stu-id="20d97-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="20d97-193">Hodnota pole **Stav** se změní na **Publikováno**.</span><span class="sxs-lookup"><span data-stu-id="20d97-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="20d97-194">Vytvoření propojené aplikace</span><span class="sxs-lookup"><span data-stu-id="20d97-194">Create a connected application</span></span>

1. <span data-ttu-id="20d97-195">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Propojené aplikace**.</span><span class="sxs-lookup"><span data-stu-id="20d97-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="20d97-196">Zvolte **Nový** pro vytvoření propojené aplikace.</span><span class="sxs-lookup"><span data-stu-id="20d97-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="20d97-197">Do pole **Název** zadejte název aplikace, ke které se má provést připojení.</span><span class="sxs-lookup"><span data-stu-id="20d97-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="20d97-198">Do pole **Aplikace** zadejte adresu URL prostředí Finance and Supply Chain Management pro připojení.</span><span class="sxs-lookup"><span data-stu-id="20d97-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="20d97-199">Do pole **Klient** zadejte klienta prostředí Finance and Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="20d97-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="20d97-200">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="20d97-200">Select **Save**.</span></span>
6. <span data-ttu-id="20d97-201">V podokně akcí vyberte **Zkontrolovat připojení**, abyste otestovali spojení s prostředím.</span><span class="sxs-lookup"><span data-stu-id="20d97-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="20d97-202">Poté stránku zavřete.</span><span class="sxs-lookup"><span data-stu-id="20d97-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="20d97-203">Propojení připojených aplikace s prostředím</span><span class="sxs-lookup"><span data-stu-id="20d97-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="20d97-204">Na stránce **Nastavení prostředí** vyberte **Nový** a přiřaďte připojenou aplikaci prostředí.</span><span class="sxs-lookup"><span data-stu-id="20d97-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="20d97-205">V poli **Připojená aplikace** vyberte připojenou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="20d97-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="20d97-206">V poli **Prostředí služby** vyberte prostředí služeb.</span><span class="sxs-lookup"><span data-stu-id="20d97-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="20d97-207">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="20d97-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="20d97-208">Nastavte integraci doplňku elektronické fakturace ve Finance a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="20d97-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="20d97-209">Zapněte funkci integrace Elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="20d97-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="20d97-210">Přihlaste se k instanci Finance nebo Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="20d97-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="20d97-211">V pracovním prostoru **Správa funkcí** vyhledejte funkci **Integrace Elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="20d97-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="20d97-212">Pokud se tato funkce na stránce neobjeví, vyberte **Zkontrolovat aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="20d97-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="20d97-213">Vyberte funkci a poté vyberte tlačítko **Povolit nyní**.</span><span class="sxs-lookup"><span data-stu-id="20d97-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="20d97-214">Nastavte adresu URL koncového bodu služby</span><span class="sxs-lookup"><span data-stu-id="20d97-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="20d97-215">Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="20d97-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="20d97-216">Na kartě **Služba odeslání** v poli **Identifikátor URL koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Azure, jak je znázorněno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="20d97-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="20d97-217">Geografie datového centra Azure</span><span class="sxs-lookup"><span data-stu-id="20d97-217">Datacenter Azure geography</span></span> | <span data-ttu-id="20d97-218">URL adresa koncového bodu služby</span><span class="sxs-lookup"><span data-stu-id="20d97-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="20d97-219">Východní USA</span><span class="sxs-lookup"><span data-stu-id="20d97-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="20d97-220">USA – západ</span><span class="sxs-lookup"><span data-stu-id="20d97-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="20d97-221">Sever EU</span><span class="sxs-lookup"><span data-stu-id="20d97-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="20d97-222">Západ EU</span><span class="sxs-lookup"><span data-stu-id="20d97-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="20d97-223">Do pole **Prostředí** zadejte název prostředí služby, které je publikováno v Elektronické fakturaci.</span><span class="sxs-lookup"><span data-stu-id="20d97-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="20d97-224">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="20d97-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="20d97-225">Povolit testovacích klíčů</span><span class="sxs-lookup"><span data-stu-id="20d97-225">Enable Flighting keys</span></span>

<span data-ttu-id="20d97-226">Povolte testovací klíče pro Microsoft Dynamics 365 Finance nebo Microsoft Dynamics 365 Supply Chain Management verze 10.0.17 nebo starší.</span><span class="sxs-lookup"><span data-stu-id="20d97-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="20d97-227">ProveĎte následující příkaz SQL:</span><span class="sxs-lookup"><span data-stu-id="20d97-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="20d97-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="20d97-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="20d97-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="20d97-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="20d97-230">Proveďte příkaz IISreset pro všechny AOS.</span><span class="sxs-lookup"><span data-stu-id="20d97-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

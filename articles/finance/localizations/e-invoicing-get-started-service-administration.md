---
title: Začínáme se správou služby doplňky elektronické fakturace
description: Toto téma poskytuje informace, jak začít s doplňkem elektronické fakturace.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104353"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="479ba-103">Začínáme se správou služby doplňky elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="479ba-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="479ba-104">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="479ba-104">Prerequisites</span></span>

<span data-ttu-id="479ba-105">Než provedete postupy v tomto tématu, musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="479ba-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="479ba-106">Musíte mít přístup ke svému účtu Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="479ba-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="479ba-107">Musíte mít projekt LCS, který obsahuje verzi 10.0.13 nebo novější nástroje Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="479ba-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="479ba-108">Kromě toho musí být tyto aplikace nasazeny v jedné z následujících geografických oblastí Azure:</span><span class="sxs-lookup"><span data-stu-id="479ba-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="479ba-109">Východní USA</span><span class="sxs-lookup"><span data-stu-id="479ba-109">East US</span></span>
    - <span data-ttu-id="479ba-110">USA – západ</span><span class="sxs-lookup"><span data-stu-id="479ba-110">West US</span></span>
    - <span data-ttu-id="479ba-111">Sever EU</span><span class="sxs-lookup"><span data-stu-id="479ba-111">North EU</span></span>
    - <span data-ttu-id="479ba-112">Západ EU</span><span class="sxs-lookup"><span data-stu-id="479ba-112">West EU</span></span>

- <span data-ttu-id="479ba-113">Musíte mít přístup ke svému účtu Dynamics 365 Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="479ba-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="479ba-114">Musíte aktivovat funkci Globalizace pro svůj účet RCS v modulu Správa funkcí.</span><span class="sxs-lookup"><span data-stu-id="479ba-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="479ba-115">Pro více informací viz [Regulatory Configuration Services (RCS) - funkce globalizace](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="479ba-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="479ba-116">Musíte vytvořit trezor klíčů a účet úložiště Azure.</span><span class="sxs-lookup"><span data-stu-id="479ba-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="479ba-117">Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="479ba-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="479ba-118">Nainstalujte doplněk pro mikroslužby ve službě Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="479ba-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="479ba-119">Přihlaste se k účtu LCS.</span><span class="sxs-lookup"><span data-stu-id="479ba-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="479ba-120">Vyberte dlaždici **Náhled správy funkcí**.</span><span class="sxs-lookup"><span data-stu-id="479ba-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="479ba-121">V části **Funkce Public Preview** vyberte **služba elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="479ba-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="479ba-122">Ujistěte se, zda je možnost **Funkce Preview zapnuta** nastavena na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="479ba-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="479ba-123">Nastavení parametrů pro integraci RCS s doplňkem elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="479ba-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="479ba-124">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="479ba-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="479ba-125">V pracovním prostoru **Elektronické výkaznictví** v části **Související odkazy** vyberte **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="479ba-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="479ba-126">Na kartě **Služba elektronické fakturace** v poli **Identifikátor URI koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Azure, jak je znázorněno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="479ba-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="479ba-127">Geografie datového centra Azure</span><span class="sxs-lookup"><span data-stu-id="479ba-127">Datacenter Azure geography</span></span> | <span data-ttu-id="479ba-128">URI adresa koncového bodu služby</span><span class="sxs-lookup"><span data-stu-id="479ba-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="479ba-129">Východní USA</span><span class="sxs-lookup"><span data-stu-id="479ba-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="479ba-130">USA – západ</span><span class="sxs-lookup"><span data-stu-id="479ba-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="479ba-131">Sever EU</span><span class="sxs-lookup"><span data-stu-id="479ba-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="479ba-132">Západ EU</span><span class="sxs-lookup"><span data-stu-id="479ba-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="479ba-133">Ověřte, zda je pole **Id aplikace** nastaveno na **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="479ba-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="479ba-134">Tato hodnota je pevná hodnota.</span><span class="sxs-lookup"><span data-stu-id="479ba-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="479ba-135">V poli **ID prostředí LCS** zadejte ID účtu předplatného LCS.</span><span class="sxs-lookup"><span data-stu-id="479ba-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="479ba-136">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="479ba-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="479ba-137">Vytvoření tajného kódu Key Vault</span><span class="sxs-lookup"><span data-stu-id="479ba-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="479ba-138">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="479ba-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="479ba-139">V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Elektronická fakturace**.</span><span class="sxs-lookup"><span data-stu-id="479ba-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="479ba-140">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby** a potom vyberte **Parametry Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="479ba-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="479ba-141">Vyberte možnost **Nový** k vytvoření tajného kódu trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="479ba-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="479ba-142">Do pole **Název** zadejte název tajného kódu trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="479ba-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="479ba-143">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="479ba-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="479ba-144">Do pole **Identifikátoru URI Key Vault** vložte tajný kód z Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="479ba-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="479ba-145">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="479ba-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="479ba-146">Vytvoření tajného kódu účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="479ba-146">Create Storage account secret</span></span>

1. <span data-ttu-id="479ba-147">Na stránce **Parametry trezoru klíčů** v části **Certifikáty** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="479ba-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="479ba-148">Do pole **Název** zadejte název tajného kódu účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="479ba-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="479ba-149">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="479ba-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="479ba-150">V poli **Typ** vyberte **Certifikát**.</span><span class="sxs-lookup"><span data-stu-id="479ba-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="479ba-151">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="479ba-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="479ba-152">Vytvoření prostředí doplňku elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="479ba-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="479ba-153">Přihlaste se k účtu RCS.</span><span class="sxs-lookup"><span data-stu-id="479ba-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="479ba-154">V pracovním prostoru **Funkce globalizace** v části **Prostředí** vyberte dlaždici **Elektronická fakturace**.</span><span class="sxs-lookup"><span data-stu-id="479ba-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="479ba-155">Vytvoření servisního prostředí</span><span class="sxs-lookup"><span data-stu-id="479ba-155">Create a service environment</span></span>

1. <span data-ttu-id="479ba-156">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Prostředí služby**.</span><span class="sxs-lookup"><span data-stu-id="479ba-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="479ba-157">Vyberte **Nový** pro vytvoření nového prostředí služby.</span><span class="sxs-lookup"><span data-stu-id="479ba-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="479ba-158">Do pole **Název** zadejte název prostředí elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="479ba-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="479ba-159">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="479ba-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="479ba-160">V poli **Tajný klíč tokenu SAS úložiště** vyberte název certifikátu, který se musí použít k ověření přístupu k účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="479ba-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="479ba-161">V části **Uživatelé** vyberte **Přidat**, chcete-li přidat uživatele, který má povoleno odesílat elektronické faktury prostřednictvím prostředí a také se připojit k účtu úložiště.</span><span class="sxs-lookup"><span data-stu-id="479ba-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="479ba-162">Do pole **ID uživatele** zadejte alias uživatele.</span><span class="sxs-lookup"><span data-stu-id="479ba-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="479ba-163">Do pole **E-mail** zadejte e-mailovou adresu uživatele.</span><span class="sxs-lookup"><span data-stu-id="479ba-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="479ba-164">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="479ba-164">Select **Save**.</span></span>
8. <span data-ttu-id="479ba-165">Pokud faktury pro vaši zemi/region vyžadují pro použití digitálních podpisů řetězec certifikátů, v podokně akcí vyberte **Parametry Key Vault** a poté zadejte **Sekvence certifikátů** a postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="479ba-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="479ba-166">Vyberte **Nový** k vytvoření sekvence certifikátů.</span><span class="sxs-lookup"><span data-stu-id="479ba-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="479ba-167">Do pole **Název** zadejte název sekvence certifikátů.</span><span class="sxs-lookup"><span data-stu-id="479ba-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="479ba-168">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="479ba-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="479ba-169">V části **Certifikáty** vyberte **Přidat**, abyste přidali certifikát do sekvence.</span><span class="sxs-lookup"><span data-stu-id="479ba-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="479ba-170">Pomocí tlačítek **Nahoru** a **Dolů** změňte polohu certifikátu v řetězci.</span><span class="sxs-lookup"><span data-stu-id="479ba-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="479ba-171">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="479ba-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="479ba-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="479ba-172">Close the page.</span></span>
9. <span data-ttu-id="479ba-173">Na stránce **Prostředí služby** v podokně akcí vyberte **Publikovat**, chcete-li publikovat prostředí do cloudu.</span><span class="sxs-lookup"><span data-stu-id="479ba-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="479ba-174">Hodnota pole **Stav** se změní na **Publikováno**.</span><span class="sxs-lookup"><span data-stu-id="479ba-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="479ba-175">Vytvoření propojené aplikace</span><span class="sxs-lookup"><span data-stu-id="479ba-175">Create a connected application</span></span>

1. <span data-ttu-id="479ba-176">Na stránce **Nastavení prostředí** v podokně akcí vyberte **Propojené aplikace**.</span><span class="sxs-lookup"><span data-stu-id="479ba-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="479ba-177">Zvolte **Nový** pro vytvoření propojené aplikace.</span><span class="sxs-lookup"><span data-stu-id="479ba-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="479ba-178">Do pole **Název** zadejte název aplikace, ke které se má provést připojení.</span><span class="sxs-lookup"><span data-stu-id="479ba-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="479ba-179">Do pole **Aplikace** zadejte adresu URL prostředí Finance and Supply Chain Management pro připojení.</span><span class="sxs-lookup"><span data-stu-id="479ba-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="479ba-180">Do pole **Klient** zadejte klienta prostředí Finance and Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="479ba-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="479ba-181">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="479ba-181">Select **Save**.</span></span>
6. <span data-ttu-id="479ba-182">V podokně akcí vyberte **Zkontrolovat připojení**, abyste otestovali spojení s prostředím.</span><span class="sxs-lookup"><span data-stu-id="479ba-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="479ba-183">Poté stránku zavřete.</span><span class="sxs-lookup"><span data-stu-id="479ba-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="479ba-184">Propojení připojených aplikace s prostředím</span><span class="sxs-lookup"><span data-stu-id="479ba-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="479ba-185">Na stránce **Nastavení prostředí** vyberte **Nový** a přiřaďte připojenou aplikaci prostředí.</span><span class="sxs-lookup"><span data-stu-id="479ba-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="479ba-186">V poli **Připojená aplikace** vyberte připojenou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="479ba-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="479ba-187">V poli **Prostředí služby** vyberte prostředí služeb.</span><span class="sxs-lookup"><span data-stu-id="479ba-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="479ba-188">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="479ba-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="479ba-189">Nastavte integraci doplňku elektronické fakturace ve Finance a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="479ba-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="479ba-190">Zapněte funkci integrace doplňku elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="479ba-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="479ba-191">Přihlaste se k instanci Finance nebo Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="479ba-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="479ba-192">V pracovním prostoru **Správa funkcí** vyhledejte funkci **Integrace doplňku elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="479ba-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="479ba-193">Pokud se tato funkce na stránce neobjeví, vyberte **Zkontrolovat aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="479ba-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="479ba-194">Vyberte funkci a poté vyberte tlačítko **Povolit nyní**.</span><span class="sxs-lookup"><span data-stu-id="479ba-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="479ba-195">Nastavte adresu URL koncového bodu služby</span><span class="sxs-lookup"><span data-stu-id="479ba-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="479ba-196">Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="479ba-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="479ba-197">Na kartě **Služba odeslání** v poli **Identifikátor URL koncového bodu služby** zadejte příslušný koncový bod služby pro vaši geografii Azure, jak je znázorněno v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="479ba-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="479ba-198">Geografie datového centra Azure</span><span class="sxs-lookup"><span data-stu-id="479ba-198">Datacenter Azure geography</span></span> | <span data-ttu-id="479ba-199">URL adresa koncového bodu služby</span><span class="sxs-lookup"><span data-stu-id="479ba-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="479ba-200">Východní USA</span><span class="sxs-lookup"><span data-stu-id="479ba-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="479ba-201">USA – západ</span><span class="sxs-lookup"><span data-stu-id="479ba-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="479ba-202">Sever EU</span><span class="sxs-lookup"><span data-stu-id="479ba-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="479ba-203">Západ EU</span><span class="sxs-lookup"><span data-stu-id="479ba-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="479ba-204">Do pole **Prostředí** zadejte název prostředí doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="479ba-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="479ba-205">Zvolte **Uložit** a pak zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="479ba-205">Select **Save**, and then close the page.</span></span>

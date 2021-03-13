---
title: Komponenty pro správu doplňku elektronického fakturování
description: Toto téma poskytuje informace o komponentách, které souvisejí se správou doplňku elektronické fakturace.
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
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104355"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="8e083-103">Komponenty pro správu doplňku elektronického fakturování</span><span class="sxs-lookup"><span data-stu-id="8e083-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="8e083-104">Toto téma poskytuje informace o komponentách, které souvisejí se správou doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="8e083-105">Poskytuje také informace, jak konfigurovat službu doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="8e083-106">Azure</span><span class="sxs-lookup"><span data-stu-id="8e083-106">Azure</span></span>

<span data-ttu-id="8e083-107">Použijte Microsoft Azure k vytvoření tajných klíčů pro trezor klíčů a účet úložiště.</span><span class="sxs-lookup"><span data-stu-id="8e083-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="8e083-108">Potom použijte tajné klíče v konfiguraci doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="8e083-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="8e083-109">Lifecycle Services</span></span>

<span data-ttu-id="8e083-110">Pomocí Microsoft Dynamics Lifecycle Services (LCS) povolte doplněk pro mikroslužby pro váš projekt nasazení LCS.</span><span class="sxs-lookup"><span data-stu-id="8e083-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="8e083-111">V LCS vyberte dlaždici **Správa funkcí Preview** a poté zapněte funkci **Služba elektronické fakturace**.</span><span class="sxs-lookup"><span data-stu-id="8e083-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="8e083-112">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="8e083-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="8e083-113">Dynamics 365 Regulatory Configuration Services (RCS) je rozhraní, které se používá ke konfiguraci doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="8e083-114">Prostředky typu prostředí nebo funkce elektronické fakturace jsou vytvářeny, udržovány a hostovány v RCS.</span><span class="sxs-lookup"><span data-stu-id="8e083-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="8e083-115">Když jsou prostředky připraveny, jsou publikovány ve službě doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="8e083-116">Pro více informací o RCS viz [Regulatory Configuration Services (RCS) – funkce globalizace](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="8e083-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="8e083-117">Integrace s doplňkem elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="8e083-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="8e083-118">Než budete pomocí RCS moci konfigurovat elektronické faktury, musíte nakonfigurovat RCS tak, aby umožňovalo komunikaci s doplňkem elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="8e083-119">Tuto konfiguraci provedete na kartě **Doplněk elektronické fakturace** na stránce **Parametry elektronického vykazování**.</span><span class="sxs-lookup"><span data-stu-id="8e083-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="8e083-120">Koncový bod služby</span><span class="sxs-lookup"><span data-stu-id="8e083-120">Service endpoint</span></span>

<span data-ttu-id="8e083-121">Adresa URL koncového bodu doplňku elektronické fakturace se může lišit podle geografie datového centra Azure.</span><span class="sxs-lookup"><span data-stu-id="8e083-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="8e083-122">Následující tabulka uvádí dostupnost podle oblastí:</span><span class="sxs-lookup"><span data-stu-id="8e083-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="8e083-123">Geografie datového centra Azure</span><span class="sxs-lookup"><span data-stu-id="8e083-123">Azure datacenter geography</span></span> | <span data-ttu-id="8e083-124">URL adresa koncového bodu služby</span><span class="sxs-lookup"><span data-stu-id="8e083-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="8e083-125">Východní USA</span><span class="sxs-lookup"><span data-stu-id="8e083-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="8e083-126">USA – západ</span><span class="sxs-lookup"><span data-stu-id="8e083-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="8e083-127">Sever EU</span><span class="sxs-lookup"><span data-stu-id="8e083-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="8e083-128">Západ EU</span><span class="sxs-lookup"><span data-stu-id="8e083-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="8e083-129">ID přihlášky</span><span class="sxs-lookup"><span data-stu-id="8e083-129">Application ID</span></span>

<span data-ttu-id="8e083-130">ID aplikace je ID aplikace doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="8e083-131">V tomto případě je hodnota pevná: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="8e083-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="8e083-132">ID prostředí LCS</span><span class="sxs-lookup"><span data-stu-id="8e083-132">LCS environment ID</span></span>

<span data-ttu-id="8e083-133">ID prostředí LCS je ID předplatného LCS vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="8e083-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="8e083-134">Prostředí služby</span><span class="sxs-lookup"><span data-stu-id="8e083-134">Service environments</span></span>

<span data-ttu-id="8e083-135">Prostředí služeb jsou logické oddíly, které jsou vytvořeny na podporu provádění funkcí elektronické fakturace v doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="8e083-136">Tajné klíče zabezpečení a digitální certifikáty a správa (tj. přístupová oprávnění) musí být nakonfigurovány na úrovni prostředí služby.</span><span class="sxs-lookup"><span data-stu-id="8e083-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="8e083-137">Zákazníci mohou vytvořit tolik prostředí služeb, kolik chtějí.</span><span class="sxs-lookup"><span data-stu-id="8e083-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="8e083-138">Všechna prostředí služeb, která zákazník vytvoří, jsou na sobě navzájem nezávislá.</span><span class="sxs-lookup"><span data-stu-id="8e083-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="8e083-139">Prostředí služeb musí být vytvořena a udržována v RCS.</span><span class="sxs-lookup"><span data-stu-id="8e083-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="8e083-140">Když jsou prostředí služeb připraveny, musí být publikovány v doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="8e083-141">Stav prostředí služeb</span><span class="sxs-lookup"><span data-stu-id="8e083-141">Service environment status</span></span>

<span data-ttu-id="8e083-142">Prostředí služeb lze spravovat prostřednictvím stavu.</span><span class="sxs-lookup"><span data-stu-id="8e083-142">Service environments can be managed through status.</span></span> <span data-ttu-id="8e083-143">K dispozici jsou tyto možnosti:</span><span class="sxs-lookup"><span data-stu-id="8e083-143">The possible options are:</span></span>

- <span data-ttu-id="8e083-144">**Nepublikováno** – Prostředí bylo vytvořeno, ale dosud nebylo publikováno.</span><span class="sxs-lookup"><span data-stu-id="8e083-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="8e083-145">**Publikováno** – Prostředí bylo publikováno v doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="8e083-146">**Změněno** – Atributy publikovaného prostředí byly změněny, ale změny ještě nebyly publikovány.</span><span class="sxs-lookup"><span data-stu-id="8e083-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="8e083-147">Tajné klíče zákazníků</span><span class="sxs-lookup"><span data-stu-id="8e083-147">Customer secrets</span></span>

<span data-ttu-id="8e083-148">Doplňková služba elektronické fakturace je zodpovědná za ukládání všech vašich obchodních údajů v prostředcích Azure, které vlastní vaše společnost.</span><span class="sxs-lookup"><span data-stu-id="8e083-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="8e083-149">Abyste zajistili, že služba funguje správně a že ke všem obchodním datům, která jsou potřebná a generovaná doplňkem elektronické fakturace, přistupuje pouze doplněk, musíte vytvořit dva hlavní prostředky Azure:</span><span class="sxs-lookup"><span data-stu-id="8e083-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="8e083-150">Účet úložiště Azure (úložiště Blob), které bude uchovávat elektronické faktury</span><span class="sxs-lookup"><span data-stu-id="8e083-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="8e083-151">Trezor klíčů Azure, který bude uchovávat certifikáty a identifikátor URI (Uniform Resource Identifier) účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="8e083-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="8e083-152">Vyhrazený trezor klíčů a účet úložiště odběratele musí být výslovně přiděleny pro použití s doplňkem elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="8e083-153">Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="8e083-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="8e083-154">Uživatelé</span><span class="sxs-lookup"><span data-stu-id="8e083-154">Users</span></span>

<span data-ttu-id="8e083-155">Každé prostředí služeb musí obsahovat seznam uživatelů, kteří se mohou připojit z aplikací Dynamics 365 Finance a Dynamics 365 Supply Chain Management v doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="8e083-156">Publikování</span><span class="sxs-lookup"><span data-stu-id="8e083-156">Publication</span></span>

<span data-ttu-id="8e083-157">Prostředí služeb musí být publikovány v doplňku elektronické fakturace, než je možné je použít.</span><span class="sxs-lookup"><span data-stu-id="8e083-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="8e083-158">Aplikace Finance a Supply Chain Management mají přístup pouze k publikovaným prostředím.</span><span class="sxs-lookup"><span data-stu-id="8e083-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="8e083-159">Kromě toho musí být prostředí služeb publikováno, než se jakékoli aktualizace jeho atributů projeví ve službě elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="8e083-160">Připojené aplikace</span><span class="sxs-lookup"><span data-stu-id="8e083-160">Connected applications</span></span>

<span data-ttu-id="8e083-161">Připojené aplikace jsou instance aplikací Finance a Supply Chain Management, ke kterým byste se mohli chtít připojit prostřednictvím RCS.</span><span class="sxs-lookup"><span data-stu-id="8e083-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="8e083-162">Kromě adresy URL aplikace a jejího klienta obsahuje připojená aplikace pověření, která umožňují RCS připojit se k prostředí.</span><span class="sxs-lookup"><span data-stu-id="8e083-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="8e083-163">Prostřednictvím připojených aplikací můžete nakonfigurovat část funkce elektronické fakturace v aplikacích Finance a Supply Chain Management, aby byla funkční celá funkce elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="8e083-164">Finance a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8e083-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="8e083-165">Integrace s doplňkem elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="8e083-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="8e083-166">Než budete moci použít aplikace Finance a Supply Chain Management k vystavování elektronických faktur pomocí doplňku elektronické fakturace, musí být doplněk nakonfigurován tak, aby umožňoval komunikaci se službou.</span><span class="sxs-lookup"><span data-stu-id="8e083-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="8e083-167">Funkce integrace doplňku elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="8e083-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="8e083-168">Aby bylo možné povolit komunikaci mezi aplikacemi Finance a Supply Chain Management a doplňkem elektronické fakturace, musíte zapnout funkci **Integrace doplňku elektronické fakturace** v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="8e083-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="8e083-169">Koncový bod služby</span><span class="sxs-lookup"><span data-stu-id="8e083-169">Service endpoint</span></span>

<span data-ttu-id="8e083-170">Koncovým bodem služby je adresa URL, kde se nachází doplněk elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="8e083-171">Než budete moci vystavovat elektronické faktury, v aplikacích Finance a Supply Chain Management musí být nakonfigurován koncový bod služby, aby byla možná komunikace se službou.</span><span class="sxs-lookup"><span data-stu-id="8e083-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="8e083-172">Chcete-li nakonfigurovat koncový bod služby, přejděte na **Správa organizace \> Nastavení \> Parametr elektronického dokumentu** a poté na kartě **Služby odesílání** v poli **Adresa URL doplňku elektronické fakturace** zadejte adresu URL, jak je popsáno v tabulce v části **Koncový bod služby**.</span><span class="sxs-lookup"><span data-stu-id="8e083-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="8e083-173">Prostředí</span><span class="sxs-lookup"><span data-stu-id="8e083-173">Environments</span></span>

<span data-ttu-id="8e083-174">Název prostředí zadaný v aplikacích Finance and Supply Chain Management odkazuje na název prostředí vytvořeného v RCS a publikovaného v doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="8e083-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="8e083-175">Prostředí musí být nakonfigurováno na kartě **Služby odesílání** na stránce **Parametr elektronického dokumentu**, aby každý požadavek na vystavení elektronické faktury obsahoval prostředí, podle kterého může doplněk elektronické fakturace určit, která funkce elektronické fakturace má požadavek zpracovat.</span><span class="sxs-lookup"><span data-stu-id="8e083-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e083-176">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="8e083-176">Additional resources</span></span>

- [<span data-ttu-id="8e083-177">Konfigurace elektronických faktur v RCS</span><span class="sxs-lookup"><span data-stu-id="8e083-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="8e083-178">Vystavení elektronických faktur v aplikacích Finance a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8e083-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)

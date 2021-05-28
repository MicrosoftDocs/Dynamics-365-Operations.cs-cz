---
title: Součásti pro správu Elektronické fakturace
description: Toto téma poskytuje informace o součástech, které souvisejí se správou Elektronické fakturace.
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: 081d23c85d3555210b54597920a49e800ffe284b
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980916"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="ea7b7-103">Součásti pro správu Elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="ea7b7-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ea7b7-104">Toto téma poskytuje informace o součástech, které souvisejí se správou Elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="ea7b7-105">Obsahuje také informace o konfiguraci služby elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="ea7b7-106">Azure</span><span class="sxs-lookup"><span data-stu-id="ea7b7-106">Azure</span></span>

<span data-ttu-id="ea7b7-107">Použijte Microsoft Azure k vytvoření tajných klíčů pro trezor klíčů a účet úložiště.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="ea7b7-108">Potom použijte tajné klíče v konfiguraci Elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="ea7b7-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ea7b7-109">Lifecycle Services</span></span>

<span data-ttu-id="ea7b7-110">Pomocí Microsoft Dynamics Lifecycle Services (LCS) povolte mikroslužby pro váš projekt nasazení LCS.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="ea7b7-111">Instalace mikroslužeb v LCS vyžaduje alespoň virtuální počítač úrovně 2.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="ea7b7-112">Další informace o plánování prostředí naleznete v části [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="ea7b7-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="ea7b7-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="ea7b7-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="ea7b7-114">Dynamics 365 Regulatory Configuration Services (RCS) je rozhraní, které se používá ke konfiguraci Elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="ea7b7-115">Prostředky typu prostředí nebo funkce elektronické fakturace jsou vytvářeny, udržovány a hostovány v RCS.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="ea7b7-116">Když jsou prostředky připraveny, jsou publikovány ve službě elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="ea7b7-117">Registrace RCS viz [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="ea7b7-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="ea7b7-118">Pro více informací o RCS viz [Regulatory Configuration Services (RCS) – funkce globalizace](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="ea7b7-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="ea7b7-119">Integrace s Elektronickou fakturací</span><span class="sxs-lookup"><span data-stu-id="ea7b7-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="ea7b7-120">Než budete pomocí RCS moci konfigurovat elektronické faktury, musíte nakonfigurovat RCS tak, aby umožňovalo komunikaci s Elektronickou fakturací.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="ea7b7-121">Tuto konfiguraci provedete na kartě **Elektronická fakturace** na stránce **Parametry elektronického vykazování**.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="ea7b7-122">Koncový bod služby</span><span class="sxs-lookup"><span data-stu-id="ea7b7-122">Service endpoint</span></span>

<span data-ttu-id="ea7b7-123">Elektronická fakturace je k dispozici v několika geografických oblastech datového centra Azure.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="ea7b7-124">Následující tabulka uvádí dostupnost podle oblastí.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="ea7b7-125">Geografie datového centra Azure</span><span class="sxs-lookup"><span data-stu-id="ea7b7-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="ea7b7-126">Spojené státy americké</span><span class="sxs-lookup"><span data-stu-id="ea7b7-126">United States</span></span>              |
| <span data-ttu-id="ea7b7-127">Evropa</span><span class="sxs-lookup"><span data-stu-id="ea7b7-127">Europe</span></span>                     |
| <span data-ttu-id="ea7b7-128">Spojené království</span><span class="sxs-lookup"><span data-stu-id="ea7b7-128">United Kingdom</span></span>             |
| <span data-ttu-id="ea7b7-129">Asie</span><span class="sxs-lookup"><span data-stu-id="ea7b7-129">Asia</span></span>                       |

### <a name="service-environments"></a><span data-ttu-id="ea7b7-130">Prostředí služby</span><span class="sxs-lookup"><span data-stu-id="ea7b7-130">Service environments</span></span>

<span data-ttu-id="ea7b7-131">Prostředí služeb jsou logické oddíly, které jsou vytvořeny na podporu provádění funkcí elektronické fakturace v Elektronické fakturaci.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="ea7b7-132">Tajné klíče zabezpečení a digitální certifikáty a správa (tj. přístupová oprávnění) musí být nakonfigurovány na úrovni prostředí služby.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="ea7b7-133">Zákazníci mohou vytvořit tolik prostředí služeb, kolik chtějí.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="ea7b7-134">Všechna prostředí služeb, která zákazník vytvoří, jsou na sobě navzájem nezávislá.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="ea7b7-135">Prostředí služeb musí být vytvořena a udržována v RCS.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="ea7b7-136">Když jsou prostředí služeb připraveny, musí být publikovány v Elektronické fakturaci.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="ea7b7-137">Stav prostředí služeb</span><span class="sxs-lookup"><span data-stu-id="ea7b7-137">Service environment status</span></span>

<span data-ttu-id="ea7b7-138">Prostředí služeb lze spravovat prostřednictvím stavu.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-138">Service environments can be managed through status.</span></span> <span data-ttu-id="ea7b7-139">K dispozici jsou tyto možnosti:</span><span class="sxs-lookup"><span data-stu-id="ea7b7-139">The possible options are:</span></span>

- <span data-ttu-id="ea7b7-140">**Nepublikováno** – Prostředí bylo vytvořeno, ale dosud nebylo publikováno.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="ea7b7-141">**Publikováno** – Prostředí bylo publikováno v Elektronické fakturaci.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="ea7b7-142">**Změněno** – Atributy publikovaného prostředí byly změněny, ale změny ještě nebyly publikovány.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="ea7b7-143">Tajné klíče zákazníků</span><span class="sxs-lookup"><span data-stu-id="ea7b7-143">Customer secrets</span></span>

<span data-ttu-id="ea7b7-144">Služba elektronické fakturace je zodpovědná za ukládání všech vašich obchodních údajů v prostředcích Azure, které vlastní vaše společnost.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="ea7b7-145">Abyste zajistili, že služba funguje správně a že ke všem obchodním datům, která jsou potřebná a generovaná Elektronickou fakturací, se přistupuje správným způsobem, musíte vytvořit dva hlavní zdroje Azure:</span><span class="sxs-lookup"><span data-stu-id="ea7b7-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="ea7b7-146">Účet úložiště Azure (úložiště Blob), které bude uchovávat elektronické faktury</span><span class="sxs-lookup"><span data-stu-id="ea7b7-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="ea7b7-147">Trezor klíčů Azure, který bude uchovávat certifikáty a identifikátor URI (Uniform Resource Identifier) účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="ea7b7-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="ea7b7-148">Vyhrazený trezor klíčů a účet úložiště odběratele musí být výslovně přiděleny pro použití s Elektronickou fakturací.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="ea7b7-149">Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="ea7b7-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="ea7b7-150">Chcete-li sledovat stav vašeho trezoru klíčů a přijímat upozornění, nakonfigurujte Azure Monitor pro trezor klíčů.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="ea7b7-151">Povolením protokolování trezoru klíčů můžete sledovat, jak, kdy a kým je k vašim trezorům klíčů přistupováno.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="ea7b7-152">Další informace viz [Monitorování a varování pro Azure Key Vault](/azure/key-vault/general/alert) a [Jak povolit protokolování trezoru klíčů](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span><span class="sxs-lookup"><span data-stu-id="ea7b7-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="ea7b7-153">Osvědčeným postupem je pravidelně střídat tajné klíče.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="ea7b7-154">Další informace naleznete v [Dokumentace k tajným klíčům](/azure/key-vault/secrets/).</span><span class="sxs-lookup"><span data-stu-id="ea7b7-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="ea7b7-155">Uživatelé</span><span class="sxs-lookup"><span data-stu-id="ea7b7-155">Users</span></span>

<span data-ttu-id="ea7b7-156">Každé prostředí služeb musí obsahovat seznam uživatelů, kteří se mohou připojit z aplikací Dynamics 365 Finance a Dynamics 365 Supply Chain Management v Elektronické fakturaci.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="ea7b7-157">Publikování</span><span class="sxs-lookup"><span data-stu-id="ea7b7-157">Publication</span></span>

<span data-ttu-id="ea7b7-158">Prostředí služeb musí být publikovány v Elektronické fakturaci, než je možné je použít.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="ea7b7-159">Aplikace Finance a Supply Chain Management mají přístup pouze k publikovaným prostředím.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="ea7b7-160">Kromě toho musí být prostředí služeb publikováno, než se jakékoli aktualizace jeho atributů projeví ve službě elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="ea7b7-161">Připojené aplikace</span><span class="sxs-lookup"><span data-stu-id="ea7b7-161">Connected applications</span></span>

<span data-ttu-id="ea7b7-162">Připojené aplikace jsou instance aplikací Finance a Supply Chain Management, ke kterým byste se mohli chtít připojit prostřednictvím RCS.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="ea7b7-163">Kromě adresy URL aplikace a jejího klienta obsahuje připojená aplikace pověření, která umožňují RCS připojit se k prostředí.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="ea7b7-164">Prostřednictvím připojených aplikací můžete nakonfigurovat část funkce elektronické fakturace v aplikacích Finance a Supply Chain Management, aby byla funkční celá funkce elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="ea7b7-165">Finance a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ea7b7-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="ea7b7-166">Integrace s Elektronickou fakturací</span><span class="sxs-lookup"><span data-stu-id="ea7b7-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="ea7b7-167">Než budete moci použít aplikace Finance a Supply Chain Management k vystavování elektronických faktur pomocí Elektronické fakturace, musí být tato aplikace konfigurována tak, aby umožňovala komunikaci se službou.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="ea7b7-168">Funkce integrace Elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="ea7b7-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="ea7b7-169">Aby bylo možné povolit komunikaci mezi aplikacemi Finance a Supply Chain Management a Elektronickou fakturací, musíte zapnout funkci možnost **Integrace elektronické fakturace** v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="ea7b7-170">Koncový bod služby</span><span class="sxs-lookup"><span data-stu-id="ea7b7-170">Service endpoint</span></span>

<span data-ttu-id="ea7b7-171">Koncovým bodem služby je adresa URL, kde se nachází Elektronická fakturace.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="ea7b7-172">Než budete moci vystavovat elektronické faktury, v aplikacích Finance a Supply Chain Management musí být nakonfigurován koncový bod služby, aby byla možná komunikace se službou.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="ea7b7-173">Chcete-li nakonfigurovat koncový bod služby, přejděte na **Správa organizace \> Nastavení \> Parametr elektronického dokumentu** a poté na kartě **Služby odesílání** v poli **Adresa URL elektronické fakturace** zadejte adresu URL, jak je popsáno v tabulce v části **Koncový bod služby**.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="ea7b7-174">Prostředí</span><span class="sxs-lookup"><span data-stu-id="ea7b7-174">Environments</span></span>

<span data-ttu-id="ea7b7-175">Název prostředí zadaný v aplikacích Finance a Supply Chain Management odkazuje na název prostředí vytvořeného v RCS a publikovaného v Elektronické fakturaci.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="ea7b7-176">Prostředí musí být nakonfigurováno na kartě **Služby odesílání** na stránce **Parametr elektronického dokumentu**, aby každý požadavek na vystavení elektronické faktury obsahoval prostředí, podle kterého může Elektronická fakturace určit, která funkce elektronické fakturace má požadavek zpracovat.</span><span class="sxs-lookup"><span data-stu-id="ea7b7-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea7b7-177">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="ea7b7-177">Additional resources</span></span>

- [<span data-ttu-id="ea7b7-178">Konfigurace elektronických faktur v RCS</span><span class="sxs-lookup"><span data-stu-id="ea7b7-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="ea7b7-179">Vystavení elektronických faktur v aplikacích Finance a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ea7b7-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

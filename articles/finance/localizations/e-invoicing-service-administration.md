---
title: Komponenty pro správu doplňku elektronického fakturování
description: Toto téma poskytuje informace o komponentách, které souvisejí se správou doplňku elektronické fakturace.
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
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592567"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="9fe50-103">Komponenty pro správu doplňku elektronického fakturování</span><span class="sxs-lookup"><span data-stu-id="9fe50-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="9fe50-104">Toto téma poskytuje informace o komponentách, které souvisejí se správou doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="9fe50-105">Poskytuje také informace, jak konfigurovat službu doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="9fe50-106">Azure</span><span class="sxs-lookup"><span data-stu-id="9fe50-106">Azure</span></span>

<span data-ttu-id="9fe50-107">Použijte Microsoft Azure k vytvoření tajných klíčů pro trezor klíčů a účet úložiště.</span><span class="sxs-lookup"><span data-stu-id="9fe50-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="9fe50-108">Potom použijte tajné klíče v konfiguraci doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="9fe50-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="9fe50-109">Lifecycle Services</span></span>

<span data-ttu-id="9fe50-110">Pomocí Microsoft Dynamics Lifecycle Services (LCS) povolte doplněk pro mikroslužby pro váš projekt nasazení LCS.</span><span class="sxs-lookup"><span data-stu-id="9fe50-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="9fe50-111">Instalace doplňku mikroslužeb v LCS vyžaduje alespoň virtuální počítač úrovně 2.</span><span class="sxs-lookup"><span data-stu-id="9fe50-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="9fe50-112">Další informace o plánování prostředí naleznete v části [Plánování prostředí](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="9fe50-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="9fe50-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="9fe50-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="9fe50-114">Dynamics 365 Regulatory Configuration Services (RCS) je rozhraní, které se používá ke konfiguraci doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="9fe50-115">Prostředky typu prostředí nebo funkce elektronické fakturace jsou vytvářeny, udržovány a hostovány v RCS.</span><span class="sxs-lookup"><span data-stu-id="9fe50-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="9fe50-116">Když jsou prostředky připraveny, jsou publikovány ve službě doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="9fe50-117">Registrace RCS viz [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="9fe50-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="9fe50-118">Pro více informací o RCS viz [Regulatory Configuration Services (RCS) – funkce globalizace](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="9fe50-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="9fe50-119">Integrace s doplňkem elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="9fe50-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="9fe50-120">Než budete pomocí RCS moci konfigurovat elektronické faktury, musíte nakonfigurovat RCS tak, aby umožňovalo komunikaci s doplňkem elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="9fe50-121">Tuto konfiguraci provedete na kartě **Doplněk elektronické fakturace** na stránce **Parametry elektronického vykazování**.</span><span class="sxs-lookup"><span data-stu-id="9fe50-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="9fe50-122">Koncový bod služby</span><span class="sxs-lookup"><span data-stu-id="9fe50-122">Service endpoint</span></span>

<span data-ttu-id="9fe50-123">Doplněk elektronické fakturace je k dispozici v několika geografických oblastech datového centra Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe50-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="9fe50-124">Následující tabulka uvádí dostupnost podle oblastí.</span><span class="sxs-lookup"><span data-stu-id="9fe50-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="9fe50-125">Geografie datového centra Azure</span><span class="sxs-lookup"><span data-stu-id="9fe50-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="9fe50-126">Východní USA</span><span class="sxs-lookup"><span data-stu-id="9fe50-126">East US</span></span>                    |
| <span data-ttu-id="9fe50-127">USA – západ</span><span class="sxs-lookup"><span data-stu-id="9fe50-127">West US</span></span>                    |
| <span data-ttu-id="9fe50-128">Sever EU</span><span class="sxs-lookup"><span data-stu-id="9fe50-128">North EU</span></span>                   |
| <span data-ttu-id="9fe50-129">Západ EU</span><span class="sxs-lookup"><span data-stu-id="9fe50-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="9fe50-130">Prostředí služby</span><span class="sxs-lookup"><span data-stu-id="9fe50-130">Service environments</span></span>

<span data-ttu-id="9fe50-131">Prostředí služeb jsou logické oddíly, které jsou vytvořeny na podporu provádění funkcí elektronické fakturace v doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="9fe50-132">Tajné klíče zabezpečení a digitální certifikáty a správa (tj. přístupová oprávnění) musí být nakonfigurovány na úrovni prostředí služby.</span><span class="sxs-lookup"><span data-stu-id="9fe50-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="9fe50-133">Zákazníci mohou vytvořit tolik prostředí služeb, kolik chtějí.</span><span class="sxs-lookup"><span data-stu-id="9fe50-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="9fe50-134">Všechna prostředí služeb, která zákazník vytvoří, jsou na sobě navzájem nezávislá.</span><span class="sxs-lookup"><span data-stu-id="9fe50-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="9fe50-135">Prostředí služeb musí být vytvořena a udržována v RCS.</span><span class="sxs-lookup"><span data-stu-id="9fe50-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="9fe50-136">Když jsou prostředí služeb připraveny, musí být publikovány v doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="9fe50-137">Stav prostředí služeb</span><span class="sxs-lookup"><span data-stu-id="9fe50-137">Service environment status</span></span>

<span data-ttu-id="9fe50-138">Prostředí služeb lze spravovat prostřednictvím stavu.</span><span class="sxs-lookup"><span data-stu-id="9fe50-138">Service environments can be managed through status.</span></span> <span data-ttu-id="9fe50-139">K dispozici jsou tyto možnosti:</span><span class="sxs-lookup"><span data-stu-id="9fe50-139">The possible options are:</span></span>

- <span data-ttu-id="9fe50-140">**Nepublikováno** – Prostředí bylo vytvořeno, ale dosud nebylo publikováno.</span><span class="sxs-lookup"><span data-stu-id="9fe50-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="9fe50-141">**Publikováno** – Prostředí bylo publikováno v doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="9fe50-142">**Změněno** – Atributy publikovaného prostředí byly změněny, ale změny ještě nebyly publikovány.</span><span class="sxs-lookup"><span data-stu-id="9fe50-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="9fe50-143">Tajné klíče zákazníků</span><span class="sxs-lookup"><span data-stu-id="9fe50-143">Customer secrets</span></span>

<span data-ttu-id="9fe50-144">Doplňková služba elektronické fakturace je zodpovědná za ukládání všech vašich obchodních údajů v prostředcích Azure, které vlastní vaše společnost.</span><span class="sxs-lookup"><span data-stu-id="9fe50-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="9fe50-145">Abyste zajistili, že služba funguje správně a že ke všem obchodním datům, která jsou potřebná a generovaná doplňkem elektronické fakturace, přistupuje pouze doplněk, musíte vytvořit dva hlavní prostředky Azure:</span><span class="sxs-lookup"><span data-stu-id="9fe50-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="9fe50-146">Účet úložiště Azure (úložiště Blob), které bude uchovávat elektronické faktury</span><span class="sxs-lookup"><span data-stu-id="9fe50-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="9fe50-147">Trezor klíčů Azure, který bude uchovávat certifikáty a identifikátor URI (Uniform Resource Identifier) účtu úložiště</span><span class="sxs-lookup"><span data-stu-id="9fe50-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="9fe50-148">Vyhrazený trezor klíčů a účet úložiště odběratele musí být výslovně přiděleny pro použití s doplňkem elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="9fe50-149">Další informace viz [Vytvoření účtu úložiště a trezoru klíčů Azure](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="9fe50-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="9fe50-150">Uživatelé</span><span class="sxs-lookup"><span data-stu-id="9fe50-150">Users</span></span>

<span data-ttu-id="9fe50-151">Každé prostředí služeb musí obsahovat seznam uživatelů, kteří se mohou připojit z aplikací Dynamics 365 Finance a Dynamics 365 Supply Chain Management v doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="9fe50-152">Publikování</span><span class="sxs-lookup"><span data-stu-id="9fe50-152">Publication</span></span>

<span data-ttu-id="9fe50-153">Prostředí služeb musí být publikovány v doplňku elektronické fakturace, než je možné je použít.</span><span class="sxs-lookup"><span data-stu-id="9fe50-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="9fe50-154">Aplikace Finance a Supply Chain Management mají přístup pouze k publikovaným prostředím.</span><span class="sxs-lookup"><span data-stu-id="9fe50-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="9fe50-155">Kromě toho musí být prostředí služeb publikováno, než se jakékoli aktualizace jeho atributů projeví ve službě elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="9fe50-156">Připojené aplikace</span><span class="sxs-lookup"><span data-stu-id="9fe50-156">Connected applications</span></span>

<span data-ttu-id="9fe50-157">Připojené aplikace jsou instance aplikací Finance a Supply Chain Management, ke kterým byste se mohli chtít připojit prostřednictvím RCS.</span><span class="sxs-lookup"><span data-stu-id="9fe50-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="9fe50-158">Kromě adresy URL aplikace a jejího klienta obsahuje připojená aplikace pověření, která umožňují RCS připojit se k prostředí.</span><span class="sxs-lookup"><span data-stu-id="9fe50-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="9fe50-159">Prostřednictvím připojených aplikací můžete nakonfigurovat část funkce elektronické fakturace v aplikacích Finance a Supply Chain Management, aby byla funkční celá funkce elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="9fe50-160">Finance a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9fe50-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="9fe50-161">Integrace s doplňkem elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="9fe50-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="9fe50-162">Než budete moci použít aplikace Finance a Supply Chain Management k vystavování elektronických faktur pomocí doplňku elektronické fakturace, musí být doplněk nakonfigurován tak, aby umožňoval komunikaci se službou.</span><span class="sxs-lookup"><span data-stu-id="9fe50-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="9fe50-163">Funkce integrace doplňku elektronické fakturace</span><span class="sxs-lookup"><span data-stu-id="9fe50-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="9fe50-164">Aby bylo možné povolit komunikaci mezi aplikacemi Finance a Supply Chain Management a doplňkem elektronické fakturace, musíte zapnout funkci **Integrace doplňku elektronické fakturace** v pracovním prostoru **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="9fe50-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="9fe50-165">Koncový bod služby</span><span class="sxs-lookup"><span data-stu-id="9fe50-165">Service endpoint</span></span>

<span data-ttu-id="9fe50-166">Koncovým bodem služby je adresa URL, kde se nachází doplněk elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="9fe50-167">Než budete moci vystavovat elektronické faktury, v aplikacích Finance a Supply Chain Management musí být nakonfigurován koncový bod služby, aby byla možná komunikace se službou.</span><span class="sxs-lookup"><span data-stu-id="9fe50-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="9fe50-168">Chcete-li nakonfigurovat koncový bod služby, přejděte na **Správa organizace \> Nastavení \> Parametr elektronického dokumentu** a poté na kartě **Služby odesílání** v poli **Adresa URL doplňku elektronické fakturace** zadejte adresu URL, jak je popsáno v tabulce v části **Koncový bod služby**.</span><span class="sxs-lookup"><span data-stu-id="9fe50-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="9fe50-169">Prostředí</span><span class="sxs-lookup"><span data-stu-id="9fe50-169">Environments</span></span>

<span data-ttu-id="9fe50-170">Název prostředí zadaný v aplikacích Finance and Supply Chain Management odkazuje na název prostředí vytvořeného v RCS a publikovaného v doplňku elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="9fe50-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="9fe50-171">Prostředí musí být nakonfigurováno na kartě **Služby odesílání** na stránce **Parametr elektronického dokumentu**, aby každý požadavek na vystavení elektronické faktury obsahoval prostředí, podle kterého může doplněk elektronické fakturace určit, která funkce elektronické fakturace má požadavek zpracovat.</span><span class="sxs-lookup"><span data-stu-id="9fe50-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9fe50-172">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="9fe50-172">Additional resources</span></span>

- [<span data-ttu-id="9fe50-173">Konfigurace elektronických faktur v RCS</span><span class="sxs-lookup"><span data-stu-id="9fe50-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="9fe50-174">Vystavení elektronických faktur v aplikacích Finance a Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9fe50-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

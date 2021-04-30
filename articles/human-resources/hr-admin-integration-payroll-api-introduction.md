---
title: Úvod do rozhraní API integrace mezd
description: Toto téma popisuje rozhraní API Dynamics 365 Human Resources pro integraci mezd.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61b90c566325bb8d83b09fceebc721cfb14d3fc8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891119"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="33cf6-103">Úvod do rozhraní API integrace mezd</span><span class="sxs-lookup"><span data-stu-id="33cf6-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="33cf6-104">Tento dokument popisuje rozhraní API Dynamics 365 Human Resources pro integraci mezd.</span><span class="sxs-lookup"><span data-stu-id="33cf6-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="33cf6-105">API umožňuje efektivní přímou integraci mezi systémy Human Resources a mzdovými systémy partnerů.</span><span class="sxs-lookup"><span data-stu-id="33cf6-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="33cf6-106">Integrované prostředí začíná v Human Resources profilem zaměstnanců, platem a srážkami a informacemi o příspěvcích.</span><span class="sxs-lookup"><span data-stu-id="33cf6-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="33cf6-107">Když si najmete zaměstnance a zadáte požadovaný profil a informace o platu do Human Resources, mzdový systém tyto informace použije při zpracování mezd.</span><span class="sxs-lookup"><span data-stu-id="33cf6-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="33cf6-108">Veškeré aktualizace provedené v informacích o zaměstnancích nebo výplatách jsou také staženy pro použití v pozdějších výplatách.</span><span class="sxs-lookup"><span data-stu-id="33cf6-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Tok integrace mezd](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="33cf6-110">Aby bylo možné integraci povolit, v modulu Human Resources jsou přidány tyto komponenty:</span><span class="sxs-lookup"><span data-stu-id="33cf6-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="33cf6-111">Funkce pro označení zaměstnance jako připraveného k výplatě</span><span class="sxs-lookup"><span data-stu-id="33cf6-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="33cf6-112">Rozhraní API pro integraci, které otevírá nové funkce pro integraci aplikací</span><span class="sxs-lookup"><span data-stu-id="33cf6-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="33cf6-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="33cf6-113">Microsoft Dataverse</span></span>

<span data-ttu-id="33cf6-114">Toto rozhraní API je postaveno na Microsoft Dataverse (dříve Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="33cf6-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="33cf6-115">Veškerá interakce RESTful s tímto API probíhá prostřednictvím webového rozhraní Microsoft Dataverse Web API, které používá OData.</span><span class="sxs-lookup"><span data-stu-id="33cf6-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="33cf6-116">Toto rozhraní API je podmnožinou webového rozhraní Dataverse Web API.</span><span class="sxs-lookup"><span data-stu-id="33cf6-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="33cf6-117">Dataverse Web API definuje charakteristiky, jako je ověřování, smlouvy SLA, dávka, řízení souběžnosti a zpracování chyb.</span><span class="sxs-lookup"><span data-stu-id="33cf6-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="33cf6-118">Další obecné informace o webovém rozhraní Microsoft Dataverse Web API viz:</span><span class="sxs-lookup"><span data-stu-id="33cf6-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="33cf6-119">Co je Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="33cf6-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="33cf6-120">Použití webového rozhraní Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="33cf6-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="33cf6-121">Průvodce vývojáře Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="33cf6-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="33cf6-122">Tato dokumentace obsahuje podrobnosti a pokyny pro vývojáře k používání webového rozhraní Dataverse, včetně následujících témat:</span><span class="sxs-lookup"><span data-stu-id="33cf6-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="33cf6-123">Ověření pro Microsoft Dataverse s webovým API</span><span class="sxs-lookup"><span data-stu-id="33cf6-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="33cf6-124">Provádění operací pomocí webového rozhraní API</span><span class="sxs-lookup"><span data-stu-id="33cf6-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="33cf6-125">Použití Postmana s webovým rozhraní API</span><span class="sxs-lookup"><span data-stu-id="33cf6-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="33cf6-126">Pomocí sledování změn můžete synchronizovat data s externími systémy</span><span class="sxs-lookup"><span data-stu-id="33cf6-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="33cf6-127">Virtuální tabulky pro Human Resources v Dataverse</span><span class="sxs-lookup"><span data-stu-id="33cf6-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="33cf6-128">Koncové body rozhraní API pro integraci mezd využívají možnosti platformy virtuálních tabulek Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="33cf6-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="33cf6-129">Ve výchozím nastavení nejsou virtuální tabulky a jejich přidružené koncové body rozhraní API nasazeny pro prostředí Human Resources, což organizacím umožňuje určit, které koncové body OData budou pro dané prostředí k dispozici.</span><span class="sxs-lookup"><span data-stu-id="33cf6-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="33cf6-130">Chcete-li použít rozhraní API, musí být pro prostředí vygenerovány virtuální tabulky pro entity Human Resources.</span><span class="sxs-lookup"><span data-stu-id="33cf6-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="33cf6-131">Informace o generování virtuálních tabulek pro rozhraní API najdete v části [Konfigurace virtuálních tabulek Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="33cf6-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="33cf6-132">Datový model</span><span class="sxs-lookup"><span data-stu-id="33cf6-132">Data model</span></span>

<span data-ttu-id="33cf6-133">Následující diagramy ukazují vztahy v rámci rozhraní API.</span><span class="sxs-lookup"><span data-stu-id="33cf6-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="33cf6-134">Několik typů má cizí klíče k jiným, již existujícím entitám v modulu Human Resources, které zde nejsou znázorněny.</span><span class="sxs-lookup"><span data-stu-id="33cf6-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="33cf6-135">Tento dokument poskytuje informace o entitách, které jsou specifické pro scénáře integrace mezd.</span><span class="sxs-lookup"><span data-stu-id="33cf6-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="33cf6-136">Existuje však mnoho dalších entit ve webovém rozhraní API Dataverse pro Human Resources, které mohou být pro integraci rovněž relevantní.</span><span class="sxs-lookup"><span data-stu-id="33cf6-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="33cf6-137">Na některé z těchto entit se odkazuje ve vztazích cizích klíčů nebo ve vlastnostech navigace.</span><span class="sxs-lookup"><span data-stu-id="33cf6-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Datový model rozhraní API pro integraci mezd](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="33cf6-139">Zaměstnanec na výplatní listině a související entity</span><span class="sxs-lookup"><span data-stu-id="33cf6-139">Payroll employee and related entities</span></span>

<span data-ttu-id="33cf6-140">Entity:</span><span class="sxs-lookup"><span data-stu-id="33cf6-140">Entities:</span></span>

- [<span data-ttu-id="33cf6-141">Zaměstnanec na výplatní listině</span><span class="sxs-lookup"><span data-stu-id="33cf6-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="33cf6-142">Adresa pracovníka na výplatní listině</span><span class="sxs-lookup"><span data-stu-id="33cf6-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="33cf6-143">Mzdový plán fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="33cf6-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="33cf6-144">Práce pozice mzdy</span><span class="sxs-lookup"><span data-stu-id="33cf6-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="33cf6-145">Pozice mzdy</span><span class="sxs-lookup"><span data-stu-id="33cf6-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="33cf6-146">Viz také</span><span class="sxs-lookup"><span data-stu-id="33cf6-146">See also</span></span>

[<span data-ttu-id="33cf6-147">Generování a kontrola entit mzdy</span><span class="sxs-lookup"><span data-stu-id="33cf6-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="33cf6-148">Konfigurace parametrů Human Resources</span><span class="sxs-lookup"><span data-stu-id="33cf6-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="33cf6-149">Konfigurace sdílených parametrů Human Resources</span><span class="sxs-lookup"><span data-stu-id="33cf6-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="33cf6-150">Co je Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="33cf6-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="33cf6-151">Použití webového rozhraní Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="33cf6-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
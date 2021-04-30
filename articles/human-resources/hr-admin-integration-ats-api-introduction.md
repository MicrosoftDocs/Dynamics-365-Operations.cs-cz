---
title: Úvod do rozhraní API pro integraci systému sledování žadatelů
description: Toto téma popisuje rozhraní API pro integraci systému sledování žadatelů (ATS) v Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f70e377d6844b5c4f9201f0a561ad9cfcab2eda1
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890118"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="1da79-103">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="1da79-103">Applicant Tracking System integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1da79-104">Toto téma popisuje rozhraní API pro integraci systému sledování žadatelů (ATS) v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1da79-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="1da79-105">Účelem rozhraní API je umožnit efektivní integraci mezi Dynamics 365 Human Resources a partnerskými systémy ATS.</span><span class="sxs-lookup"><span data-stu-id="1da79-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![Tok integrace ATS](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="1da79-107">Integrované prostředí začíná v modulu Human Resources, když náborový manažer vytvoří požadavek na nábor.</span><span class="sxs-lookup"><span data-stu-id="1da79-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="1da79-108">Když je požadavek aktivován, ATS vytáhne podrobnosti o požadavku k vytvoření náborového projektu.</span><span class="sxs-lookup"><span data-stu-id="1da79-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="1da79-109">Poté dle náborového kanálu vybere a přijme kandidáta na dané pozice.</span><span class="sxs-lookup"><span data-stu-id="1da79-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="1da79-110">Nakonec ATS dokončí integraci opakovanou cestou zasláním záznamu vybraného kandidáta do modulu Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1da79-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="1da79-111">Záznam kandidáta pak může projít více ověřeními a pracovními postupy náboru, než je vytvořen záznam zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="1da79-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="1da79-112">Aby bylo možné integraci povolit, v modulu Human Resources jsou přidány tyto komponenty:</span><span class="sxs-lookup"><span data-stu-id="1da79-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="1da79-113">Funkce pro vytvoření žádosti o nábor.</span><span class="sxs-lookup"><span data-stu-id="1da79-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="1da79-114">Rozšířený profil kandidáta a související pracovní postupy.</span><span class="sxs-lookup"><span data-stu-id="1da79-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="1da79-115">Rozhraní API pro integraci, které otevírá nové funkce pro integraci aplikací.</span><span class="sxs-lookup"><span data-stu-id="1da79-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="1da79-116">Další informace o nastavení a používání funkce žádosti o nábor a práci s kandidáty najdete v tématu [Nábor uchazečů o práci](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="1da79-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="1da79-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="1da79-117">Microsoft Dataverse</span></span>

<span data-ttu-id="1da79-118">Toto rozhraní API je postaveno na Microsoft Dataverse (dříve Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="1da79-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="1da79-119">Veškerá interakce RESTful s tímto API probíhá prostřednictvím webového rozhraní Microsoft Dataverse Web API, které používá OData.</span><span class="sxs-lookup"><span data-stu-id="1da79-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="1da79-120">Toto rozhraní API je podmnožinou webového rozhraní Dataverse Web API.</span><span class="sxs-lookup"><span data-stu-id="1da79-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="1da79-121">Dataverse Web API definuje charakteristiky, jako je ověřování, smlouvy SLA, dávka, řízení souběžnosti a zpracování chyb.</span><span class="sxs-lookup"><span data-stu-id="1da79-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="1da79-122">Další obecné informace o webovém rozhraní Microsoft Dataverse Web API viz:</span><span class="sxs-lookup"><span data-stu-id="1da79-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="1da79-123">Co je Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="1da79-123">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="1da79-124">Použití webového rozhraní Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="1da79-124">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="1da79-125">Průvodce vývojáře Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="1da79-125">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="1da79-126">Výše uvedená dokumentace obsahuje podrobnosti a pokyny pro vývojáře ohledně použití webového rozhraní Dataverse Web API, jako je [správa ověřování](/powerapps/developer/data-platform/webapi/authenticate-web-api), [provádění operací](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [použití platformy Postman s tímto rozhraním API](/powerapps/developer/data-platform/webapi/use-postman-web-api) a [použití sledování změn nebo delta tokenů](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) s daným rozhraním API.</span><span class="sxs-lookup"><span data-stu-id="1da79-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="1da79-127">Sada možností</span><span class="sxs-lookup"><span data-stu-id="1da79-127">Option sets</span></span>

<span data-ttu-id="1da79-128">Datový model rozhraní API pro integraci ATS popsaný v tomto dokumentu obsahuje sady možností, které poskytují výčtové hodnoty přidružené k vlastnostem entity.</span><span class="sxs-lookup"><span data-stu-id="1da79-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="1da79-129">Podrobnosti o práci se sadami možností v Dataverse Web API viz [Vytváření a aktualizace sad možností pomocí webového rozhraní API](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="1da79-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="1da79-130">Sady možností jsou definovány pro každé prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1da79-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="1da79-131">Virtuální tabulky pro Human Resources v Dataverse</span><span class="sxs-lookup"><span data-stu-id="1da79-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="1da79-132">Koncové body rozhraní API pro integraci ATS využívají možnosti platformy virtuálních tabulek Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1da79-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="1da79-133">Ve výchozím nastavení nejsou virtuální tabulky a jejich přidružené koncové body rozhraní API nasazeny pro prostředí Human Resources, což organizacím umožňuje určit, které koncové body OData budou pro dané prostředí k dispozici.</span><span class="sxs-lookup"><span data-stu-id="1da79-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="1da79-134">Chcete-li použít rozhraní API, musí být pro prostředí vygenerovány virtuální tabulky pro entity Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1da79-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="1da79-135">Informace o generování virtuálních tabulek pro rozhraní API najdete v části [Konfigurace virtuálních tabulek Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="1da79-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="1da79-136">Datový model</span><span class="sxs-lookup"><span data-stu-id="1da79-136">Data model</span></span>

<span data-ttu-id="1da79-137">Datový model je soustředěn kolem dvou hlavních entit:</span><span class="sxs-lookup"><span data-stu-id="1da79-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="1da79-138">**RecruitingRequest** představuje žádost na ATS o nábor jedné či více otevřených pozic. Ukázkový dotaz viz [Příklad dotazu pro entitu Žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="1da79-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="1da79-139">**CandidateToHire** představuje podrobnosti o uchazeči, který přijal nabídku na pozici.</span><span class="sxs-lookup"><span data-stu-id="1da79-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="1da79-140">**Person** představuje osobu, která je kandidátem.</span><span class="sxs-lookup"><span data-stu-id="1da79-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="1da79-141">Osoba může mít ve společnosti více rolí, jako je kandidát, pracovník, zaměstnanec nebo dodavatel.</span><span class="sxs-lookup"><span data-stu-id="1da79-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="1da79-142">Příklad dotazu viz [Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="1da79-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="1da79-143">Následující diagramy ukazují vztahy v rámci rozhraní API.</span><span class="sxs-lookup"><span data-stu-id="1da79-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="1da79-144">Několik typů má cizí klíče k jiným, již existujícím entitám v modulu Human Resources, které zde nejsou znázorněny.</span><span class="sxs-lookup"><span data-stu-id="1da79-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="1da79-145">Tento dokument poskytuje informace o entitách, které jsou specifické pro scénáře integrace náboru.</span><span class="sxs-lookup"><span data-stu-id="1da79-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="1da79-146">Existuje však mnoho dalších entit v Dataverse Web API pro Dynamics 365 Human Resources, které mohou být pro integraci rovněž relevantní.</span><span class="sxs-lookup"><span data-stu-id="1da79-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="1da79-147">Můžete například potřebovat také podrobnosti o pracovnících, pracích, pozicích nebo jiných entitách, které zde nejsou definovány.</span><span class="sxs-lookup"><span data-stu-id="1da79-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="1da79-148">Na mnoho z těchto entit se odkazuje ve vztazích cizích klíčů nebo ve vlastnostech navigace.</span><span class="sxs-lookup"><span data-stu-id="1da79-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Datový model rozhraní API pro integraci ATS](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="1da79-150">Žádost o nábor a související entity a sady možností</span><span class="sxs-lookup"><span data-stu-id="1da79-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="1da79-151">Ukázkový dotaz:</span><span class="sxs-lookup"><span data-stu-id="1da79-151">Example query:</span></span> 

- [<span data-ttu-id="1da79-152">Příklad dotazu na žádost o nábor</span><span class="sxs-lookup"><span data-stu-id="1da79-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="1da79-153">Entity:</span><span class="sxs-lookup"><span data-stu-id="1da79-153">Entities:</span></span>

- [<span data-ttu-id="1da79-154">Požadavek na nábor</span><span class="sxs-lookup"><span data-stu-id="1da79-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="1da79-155">Pozice požadavků na nábor</span><span class="sxs-lookup"><span data-stu-id="1da79-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="1da79-156">Požadavky na zkušenosti pro nábor</span><span class="sxs-lookup"><span data-stu-id="1da79-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="1da79-157">Požadavek na vzdělání při náboru</span><span class="sxs-lookup"><span data-stu-id="1da79-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="1da79-158">Místo požadavku na nábor</span><span class="sxs-lookup"><span data-stu-id="1da79-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="1da79-159">Sada možností:</span><span class="sxs-lookup"><span data-stu-id="1da79-159">Option sets:</span></span>

- [<span data-ttu-id="1da79-160">Stav práce z hlediska přesčasů</span><span class="sxs-lookup"><span data-stu-id="1da79-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="1da79-161">Stav pozice v žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="1da79-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="1da79-162">Stav žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="1da79-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="1da79-163">Regulační kategorie pracovních míst</span><span class="sxs-lookup"><span data-stu-id="1da79-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="1da79-164">Kandidát k přijetí a související entity a sady možností</span><span class="sxs-lookup"><span data-stu-id="1da79-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="1da79-165">Ukázkový dotaz:</span><span class="sxs-lookup"><span data-stu-id="1da79-165">Example query:</span></span>

- [<span data-ttu-id="1da79-166">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="1da79-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="1da79-167">Entity:</span><span class="sxs-lookup"><span data-stu-id="1da79-167">Entities:</span></span>

- [<span data-ttu-id="1da79-168">Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="1da79-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="1da79-169">Osoba</span><span class="sxs-lookup"><span data-stu-id="1da79-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="1da79-170">Vzdělání osoby</span><span class="sxs-lookup"><span data-stu-id="1da79-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="1da79-171">Profesionální zkušenosti osoby</span><span class="sxs-lookup"><span data-stu-id="1da79-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="1da79-172">Adresa osoby</span><span class="sxs-lookup"><span data-stu-id="1da79-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="1da79-173">Kontakt strany</span><span class="sxs-lookup"><span data-stu-id="1da79-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="1da79-174">Dovednost osoby</span><span class="sxs-lookup"><span data-stu-id="1da79-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="1da79-175">Úroveň hodnocení</span><span class="sxs-lookup"><span data-stu-id="1da79-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="1da79-176">Certifikát osoby</span><span class="sxs-lookup"><span data-stu-id="1da79-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="1da79-177">Typ certifikátu</span><span class="sxs-lookup"><span data-stu-id="1da79-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="1da79-178">Prověřování osoby</span><span class="sxs-lookup"><span data-stu-id="1da79-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="1da79-179">Typy prověřování</span><span class="sxs-lookup"><span data-stu-id="1da79-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="1da79-180">Osobní identifikační číslo</span><span class="sxs-lookup"><span data-stu-id="1da79-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="1da79-181">Sady možností:</span><span class="sxs-lookup"><span data-stu-id="1da79-181">Option sets:</span></span>

- [<span data-ttu-id="1da79-182">Výsledek integrace uchazeče</span><span class="sxs-lookup"><span data-stu-id="1da79-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="1da79-183">Prázdné Ano Ne</span><span class="sxs-lookup"><span data-stu-id="1da79-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="1da79-184">Stav dokončení</span><span class="sxs-lookup"><span data-stu-id="1da79-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="1da79-185">Typ kontaktu</span><span class="sxs-lookup"><span data-stu-id="1da79-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="1da79-186">Základ kreditu vzdělání</span><span class="sxs-lookup"><span data-stu-id="1da79-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="1da79-187">Rod</span><span class="sxs-lookup"><span data-stu-id="1da79-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="1da79-188">Rodinný stav</span><span class="sxs-lookup"><span data-stu-id="1da79-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="1da79-189">Měsíce roku</span><span class="sxs-lookup"><span data-stu-id="1da79-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="1da79-190">Ne Ano</span><span class="sxs-lookup"><span data-stu-id="1da79-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="1da79-191">Jednotka období</span><span class="sxs-lookup"><span data-stu-id="1da79-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="1da79-192">Frekvence prověřování</span><span class="sxs-lookup"><span data-stu-id="1da79-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="1da79-193">Generovat frekvenci prověřování z</span><span class="sxs-lookup"><span data-stu-id="1da79-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="1da79-194">Typ úrovně dovedností</span><span class="sxs-lookup"><span data-stu-id="1da79-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="1da79-195">Viz také</span><span class="sxs-lookup"><span data-stu-id="1da79-195">See also</span></span>

[<span data-ttu-id="1da79-196">Nábor uchazečů o práci</span><span class="sxs-lookup"><span data-stu-id="1da79-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="1da79-197">Co je Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="1da79-197">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="1da79-198">Použití webového rozhraní Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="1da79-198">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="1da79-199">Vytváření a aktualizace sad možností pomocí webového rozhraní API</span><span class="sxs-lookup"><span data-stu-id="1da79-199">Create and update option sets using the Web API</span></span>](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
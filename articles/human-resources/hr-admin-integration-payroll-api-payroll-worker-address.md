---
title: Adresa pracovníka na výplatní listině
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu adresy pracovníka na výplatní listině v Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881942"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="d946e-103">Adresa pracovníka na výplatní listině</span><span class="sxs-lookup"><span data-stu-id="d946e-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d946e-104">Toto téma poskytuje informace a ukázkový dotaz pro entitu adresy pracovníka na výplatní listině v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d946e-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="d946e-105">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="d946e-105">Properties</span></span>

| <span data-ttu-id="d946e-106">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="d946e-106">Property</span></span><br><span data-ttu-id="d946e-107">**Fyzický název**</span><span class="sxs-lookup"><span data-stu-id="d946e-107">**Physical name**</span></span><br><span data-ttu-id="d946e-108">**_Typ_**</span><span class="sxs-lookup"><span data-stu-id="d946e-108">**_Type_**</span></span> | <span data-ttu-id="d946e-109">Použít</span><span class="sxs-lookup"><span data-stu-id="d946e-109">Use</span></span> | <span data-ttu-id="d946e-110">popis</span><span class="sxs-lookup"><span data-stu-id="d946e-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d946e-111">**Město**</span><span class="sxs-lookup"><span data-stu-id="d946e-111">**City**</span></span><br><span data-ttu-id="d946e-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="d946e-112">mshr_city</span></span><br><span data-ttu-id="d946e-113">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d946e-113">*String*</span></span> | <span data-ttu-id="d946e-114">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-114">Read-only</span></span><br><span data-ttu-id="d946e-115">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-115">Required</span></span> | <span data-ttu-id="d946e-116">Město definované pro adresu.</span><span class="sxs-lookup"><span data-stu-id="d946e-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="d946e-117">**Číslo pracovníka**</span><span class="sxs-lookup"><span data-stu-id="d946e-117">**Personnel number**</span></span><br><span data-ttu-id="d946e-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="d946e-118">mshr_personnelnumber</span></span><br><span data-ttu-id="d946e-119">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d946e-119">*String*</span></span> | <span data-ttu-id="d946e-120">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-120">Read-only</span></span><br><span data-ttu-id="d946e-121">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-121">Required</span></span> | <span data-ttu-id="d946e-122">Jedinečné osobní číslo zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d946e-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="d946e-123">**Oblast země**</span><span class="sxs-lookup"><span data-stu-id="d946e-123">**Country region**</span></span><br><span data-ttu-id="d946e-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="d946e-124">mshr_countryregionid</span></span><br><span data-ttu-id="d946e-125">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d946e-125">*String*</span></span> | <span data-ttu-id="d946e-126">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-126">Read-only</span></span><br><span data-ttu-id="d946e-127">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-127">Required</span></span> | <span data-ttu-id="d946e-128">Oblast země definovaná pro adresu</span><span class="sxs-lookup"><span data-stu-id="d946e-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="d946e-129">**Platné od**</span><span class="sxs-lookup"><span data-stu-id="d946e-129">**Valid from**</span></span><br><span data-ttu-id="d946e-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="d946e-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="d946e-131">*Posun data a času*</span><span class="sxs-lookup"><span data-stu-id="d946e-131">*Date Time Offset*</span></span> | <span data-ttu-id="d946e-132">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-132">Read-only</span></span> <br><span data-ttu-id="d946e-133">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-133">Required</span></span> | <span data-ttu-id="d946e-134">Datum, odkdy je adresa platná.</span><span class="sxs-lookup"><span data-stu-id="d946e-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="d946e-135">**Pracoval(a) na adrese**</span><span class="sxs-lookup"><span data-stu-id="d946e-135">**Worked in address**</span></span><br><span data-ttu-id="d946e-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="d946e-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="d946e-137">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-137">Read-only</span></span><br><span data-ttu-id="d946e-138">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-138">Required</span></span> | <span data-ttu-id="d946e-139">Označuje, zda je adresa tam, kde zaměstnanec pracuje.</span><span class="sxs-lookup"><span data-stu-id="d946e-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="d946e-140">**Okres**</span><span class="sxs-lookup"><span data-stu-id="d946e-140">**County**</span></span><br><span data-ttu-id="d946e-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="d946e-141">mshr_county</span></span><br><span data-ttu-id="d946e-142">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d946e-142">*String*</span></span> | <span data-ttu-id="d946e-143">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-143">Read-only</span></span><br><span data-ttu-id="d946e-144">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-144">Required</span></span> | <span data-ttu-id="d946e-145">Kraj definovaný pro adresu.</span><span class="sxs-lookup"><span data-stu-id="d946e-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="d946e-146">**ID adresy pracovníka na výplatní listině**</span><span class="sxs-lookup"><span data-stu-id="d946e-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="d946e-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="d946e-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="d946e-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="d946e-148">*GUID*</span></span> | <span data-ttu-id="d946e-149">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-149">Required</span></span><br><span data-ttu-id="d946e-150">Generováno systémem</span><span class="sxs-lookup"><span data-stu-id="d946e-150">System generated</span></span> | <span data-ttu-id="d946e-151">Systémem generovaná hodnota GUID pro jedinečnou identifikaci adresy.</span><span class="sxs-lookup"><span data-stu-id="d946e-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="d946e-152">**Primární pole**</span><span class="sxs-lookup"><span data-stu-id="d946e-152">**Primary field**</span></span><br><span data-ttu-id="d946e-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="d946e-153">mshr_primaryfield</span></span><br><span data-ttu-id="d946e-154">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d946e-154">*String*</span></span> | <span data-ttu-id="d946e-155">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-155">Read-only</span></span><br><span data-ttu-id="d946e-156">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-156">Required</span></span> |  |
| <span data-ttu-id="d946e-157">**Ulice**</span><span class="sxs-lookup"><span data-stu-id="d946e-157">**Street**</span></span><br><span data-ttu-id="d946e-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="d946e-158">mshr_street</span></span><br><span data-ttu-id="d946e-159">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d946e-159">*String*</span></span> | <span data-ttu-id="d946e-160">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-160">Read-only</span></span><br><span data-ttu-id="d946e-161">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-161">Required</span></span> | <span data-ttu-id="d946e-162">Ulice definovaná pro adresu.</span><span class="sxs-lookup"><span data-stu-id="d946e-162">The street defined for the address.</span></span> |
| <span data-ttu-id="d946e-163">**Platné do**</span><span class="sxs-lookup"><span data-stu-id="d946e-163">**Valid to**</span></span><br><span data-ttu-id="d946e-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="d946e-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="d946e-165">*Posun data a času*</span><span class="sxs-lookup"><span data-stu-id="d946e-165">*Date Time Offset*</span></span> | <span data-ttu-id="d946e-166">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-166">Read-only</span></span> <br><span data-ttu-id="d946e-167">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-167">Required</span></span> | <span data-ttu-id="d946e-168">Datum, dokdy je adresa platná.</span><span class="sxs-lookup"><span data-stu-id="d946e-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="d946e-169">**ID umístění**</span><span class="sxs-lookup"><span data-stu-id="d946e-169">**Location ID**</span></span><br><span data-ttu-id="d946e-170">mshr_locationidbr>*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d946e-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="d946e-171">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-171">Read-only</span></span> <br><span data-ttu-id="d946e-172">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-172">Required</span></span> | <span data-ttu-id="d946e-173">ID adresy.</span><span class="sxs-lookup"><span data-stu-id="d946e-173">The ID for the address.</span></span>  |
| <span data-ttu-id="d946e-174">**PSČ**</span><span class="sxs-lookup"><span data-stu-id="d946e-174">**Postal code**</span></span><br><span data-ttu-id="d946e-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="d946e-175">mshr_zipcode</span></span><br><span data-ttu-id="d946e-176">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d946e-176">*String*</span></span> | <span data-ttu-id="d946e-177">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-177">Read-only</span></span> <br><span data-ttu-id="d946e-178">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-178">Required</span></span> |<span data-ttu-id="d946e-179">Identifikační číslo definované pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d946e-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="d946e-180">**Bydlel(a) na adrese**</span><span class="sxs-lookup"><span data-stu-id="d946e-180">**Lived in address**</span></span><br><span data-ttu-id="d946e-181">mshr_islivedinaddressbr>*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d946e-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="d946e-182">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-182">Read-only</span></span><br><span data-ttu-id="d946e-183">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-183">Required</span></span> | <span data-ttu-id="d946e-184">Označuje, zda je adresa tam, kde zaměstnanec bydlí.</span><span class="sxs-lookup"><span data-stu-id="d946e-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="d946e-185">**Kraj**</span><span class="sxs-lookup"><span data-stu-id="d946e-185">**State**</span></span><br><span data-ttu-id="d946e-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="d946e-186">mshr_state</span></span><br><span data-ttu-id="d946e-187">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d946e-187">*String*</span></span> | <span data-ttu-id="d946e-188">Jen pro čtení</span><span class="sxs-lookup"><span data-stu-id="d946e-188">Read-only</span></span><br><span data-ttu-id="d946e-189">Povinná</span><span class="sxs-lookup"><span data-stu-id="d946e-189">Required</span></span> | <span data-ttu-id="d946e-190">Stát definovaná pro adresu.</span><span class="sxs-lookup"><span data-stu-id="d946e-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="d946e-191">Ukázkový dotaz</span><span class="sxs-lookup"><span data-stu-id="d946e-191">Example query</span></span>

<span data-ttu-id="d946e-192">**Žádost**</span><span class="sxs-lookup"><span data-stu-id="d946e-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="d946e-193">**Odezva**</span><span class="sxs-lookup"><span data-stu-id="d946e-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

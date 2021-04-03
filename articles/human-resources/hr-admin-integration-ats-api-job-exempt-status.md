---
title: Stav práce z hlediska přesčasů
description: Toto téma popisuje sadu možností pro stav práce z hlediska přesčasů v Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464445"
---
# <a name="job-exempt-status"></a><span data-ttu-id="61abf-103">Stav práce z hlediska přesčasů</span><span class="sxs-lookup"><span data-stu-id="61abf-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="61abf-104">Toto téma popisuje sadu možností pro stav práce z hlediska přesčasů v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="61abf-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="61abf-105">Fyzický název: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="61abf-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="61abf-106">Tento výčet specifikuje sadu možností pro hodnoty stavu práce z hlediska přesčasů podle zákona FLSA.</span><span class="sxs-lookup"><span data-stu-id="61abf-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="61abf-107">To je k dispozici v existující sadě možností cdm_jobexemptstatus.</span><span class="sxs-lookup"><span data-stu-id="61abf-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="61abf-108">Hodnota</span><span class="sxs-lookup"><span data-stu-id="61abf-108">Value</span></span> | <span data-ttu-id="61abf-109">Štítek</span><span class="sxs-lookup"><span data-stu-id="61abf-109">Label</span></span> | <span data-ttu-id="61abf-110">popis</span><span class="sxs-lookup"><span data-stu-id="61abf-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="61abf-111">200000000</span><span class="sxs-lookup"><span data-stu-id="61abf-111">200000000</span></span> | <span data-ttu-id="61abf-112">Osvobození</span><span class="sxs-lookup"><span data-stu-id="61abf-112">Exempt</span></span> | <span data-ttu-id="61abf-113">Práce je vyjmuta z přesčasů podle pokynů FLSA.</span><span class="sxs-lookup"><span data-stu-id="61abf-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="61abf-114">200000001</span><span class="sxs-lookup"><span data-stu-id="61abf-114">200000001</span></span> | <span data-ttu-id="61abf-115">Neosvobozené</span><span class="sxs-lookup"><span data-stu-id="61abf-115">NonExempt</span></span> | <span data-ttu-id="61abf-116">Práce není vyjmuta z přesčasů podle pokynů FLSA.</span><span class="sxs-lookup"><span data-stu-id="61abf-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="61abf-117">200000002</span><span class="sxs-lookup"><span data-stu-id="61abf-117">200000002</span></span> | <span data-ttu-id="61abf-118">Nevztahuje se</span><span class="sxs-lookup"><span data-stu-id="61abf-118">Does Not Apply</span></span> | <span data-ttu-id="61abf-119">Pokyny ohledně stavu FLSA se na práci nevztahují.</span><span class="sxs-lookup"><span data-stu-id="61abf-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="61abf-120">Viz také</span><span class="sxs-lookup"><span data-stu-id="61abf-120">See also</span></span>

[<span data-ttu-id="61abf-121">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="61abf-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="61abf-122">Příklad dotazu na žádost o nábor</span><span class="sxs-lookup"><span data-stu-id="61abf-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
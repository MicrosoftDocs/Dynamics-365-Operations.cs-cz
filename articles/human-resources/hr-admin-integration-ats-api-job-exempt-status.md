---
title: Stav práce z hlediska přesčasů
description: Toto téma popisuje sadu možností pro stav práce z hlediska přesčasů v Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053844"
---
# <a name="job-exempt-status"></a><span data-ttu-id="a31b5-103">Stav práce z hlediska přesčasů</span><span class="sxs-lookup"><span data-stu-id="a31b5-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a31b5-104">Toto téma popisuje sadu možností pro stav práce z hlediska přesčasů v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a31b5-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="a31b5-105">Fyzický název: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="a31b5-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="a31b5-106">Tento výčet specifikuje sadu možností pro hodnoty stavu práce z hlediska přesčasů podle zákona FLSA.</span><span class="sxs-lookup"><span data-stu-id="a31b5-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="a31b5-107">To je k dispozici v existující sadě možností cdm_jobexemptstatus.</span><span class="sxs-lookup"><span data-stu-id="a31b5-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="a31b5-108">Hodnota</span><span class="sxs-lookup"><span data-stu-id="a31b5-108">Value</span></span> | <span data-ttu-id="a31b5-109">Štítek</span><span class="sxs-lookup"><span data-stu-id="a31b5-109">Label</span></span> | <span data-ttu-id="a31b5-110">popis</span><span class="sxs-lookup"><span data-stu-id="a31b5-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a31b5-111">200000000</span><span class="sxs-lookup"><span data-stu-id="a31b5-111">200000000</span></span> | <span data-ttu-id="a31b5-112">Osvobození</span><span class="sxs-lookup"><span data-stu-id="a31b5-112">Exempt</span></span> | <span data-ttu-id="a31b5-113">Práce je vyjmuta z přesčasů podle pokynů FLSA.</span><span class="sxs-lookup"><span data-stu-id="a31b5-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="a31b5-114">200000001</span><span class="sxs-lookup"><span data-stu-id="a31b5-114">200000001</span></span> | <span data-ttu-id="a31b5-115">Neosvobozené</span><span class="sxs-lookup"><span data-stu-id="a31b5-115">NonExempt</span></span> | <span data-ttu-id="a31b5-116">Práce není vyjmuta z přesčasů podle pokynů FLSA.</span><span class="sxs-lookup"><span data-stu-id="a31b5-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="a31b5-117">200000002</span><span class="sxs-lookup"><span data-stu-id="a31b5-117">200000002</span></span> | <span data-ttu-id="a31b5-118">Nevztahuje se</span><span class="sxs-lookup"><span data-stu-id="a31b5-118">Does Not Apply</span></span> | <span data-ttu-id="a31b5-119">Pokyny ohledně stavu FLSA se na práci nevztahují.</span><span class="sxs-lookup"><span data-stu-id="a31b5-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a31b5-120">Viz také</span><span class="sxs-lookup"><span data-stu-id="a31b5-120">See also</span></span>

[<span data-ttu-id="a31b5-121">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="a31b5-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="a31b5-122">Příklad dotazu na žádost o nábor</span><span class="sxs-lookup"><span data-stu-id="a31b5-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
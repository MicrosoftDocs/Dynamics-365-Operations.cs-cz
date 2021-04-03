---
title: Frekvence prověřování
description: Toto téma popisuje stav nastavený pro frekvenci prověřování Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4ad81fba659a5bb22ab5131519036e156a43a486
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464543"
---
# <a name="screening-frequency"></a><span data-ttu-id="10e78-103">Frekvence prověřování</span><span class="sxs-lookup"><span data-stu-id="10e78-103">Screening frequency</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="10e78-104">Toto téma popisuje stav nastavený pro frekvenci prověřování Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="10e78-104">This topic describes the Screening frequency option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="10e78-105">Fyzický název: mshr_hcmfrequencyunit</span><span class="sxs-lookup"><span data-stu-id="10e78-105">Physical name: mshr_hcmfrequencyunit</span></span>

<span data-ttu-id="10e78-106">Tento výčet poskytuje sadu možností pro hodnoty frekvence prověřování.</span><span class="sxs-lookup"><span data-stu-id="10e78-106">This enumeration provides the option set of values for the screening frequency.</span></span> 

| <span data-ttu-id="10e78-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="10e78-107">Value</span></span> | <span data-ttu-id="10e78-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="10e78-108">Label</span></span> | <span data-ttu-id="10e78-109">popis</span><span class="sxs-lookup"><span data-stu-id="10e78-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="10e78-110">200000000 Pouze jednorázově</span><span class="sxs-lookup"><span data-stu-id="10e78-110">200000000 One-time only</span></span> | <span data-ttu-id="10e78-111">Screening je vyžadován pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="10e78-111">The screening is required only once.</span></span> |
| <span data-ttu-id="10e78-112">200000001 denně</span><span class="sxs-lookup"><span data-stu-id="10e78-112">200000001 Daily</span></span> | <span data-ttu-id="10e78-113">Četnost prověřování se počítá ve dnech.</span><span class="sxs-lookup"><span data-stu-id="10e78-113">The screening frequency is calculated in days.</span></span> |
| <span data-ttu-id="10e78-114">200000002 týdně</span><span class="sxs-lookup"><span data-stu-id="10e78-114">200000002 Weekly</span></span> | <span data-ttu-id="10e78-115">Četnost prověřování se počítá v týdnech.</span><span class="sxs-lookup"><span data-stu-id="10e78-115">The screening frequency is calculated in weeks.</span></span> |
| <span data-ttu-id="10e78-116">200000003 měsíčně</span><span class="sxs-lookup"><span data-stu-id="10e78-116">200000003 Monthly</span></span> | <span data-ttu-id="10e78-117">Četnost prověřování se počítá v měsících.</span><span class="sxs-lookup"><span data-stu-id="10e78-117">The screening frequency is calculated in months.</span></span> |
| <span data-ttu-id="10e78-118">200000004 ročně</span><span class="sxs-lookup"><span data-stu-id="10e78-118">200000004 Yearly</span></span> | <span data-ttu-id="10e78-119">Četnost prověřování se počítá v letech.</span><span class="sxs-lookup"><span data-stu-id="10e78-119">The screening frequency is calculated in years.</span></span> |

## <a name="see-also"></a><span data-ttu-id="10e78-120">Viz také</span><span class="sxs-lookup"><span data-stu-id="10e78-120">See also</span></span>

[<span data-ttu-id="10e78-121">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="10e78-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="10e78-122">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="10e78-122">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
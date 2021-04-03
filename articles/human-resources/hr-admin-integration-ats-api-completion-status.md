---
title: Stav dokončení
description: Toto téma popisuje sadu možností stavu dokončení pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468196"
---
# <a name="completion-status"></a><span data-ttu-id="34a5e-103">Stav dokončení</span><span class="sxs-lookup"><span data-stu-id="34a5e-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="34a5e-104">Toto téma popisuje sadu možností stavu dokončení pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="34a5e-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="34a5e-105">Fyzický název: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="34a5e-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="34a5e-106">Tento výčet poskytuje sadu možností pro hodnoty stavu prověřování kandidátů.</span><span class="sxs-lookup"><span data-stu-id="34a5e-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="34a5e-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="34a5e-107">Value</span></span> | <span data-ttu-id="34a5e-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="34a5e-108">Label</span></span> | <span data-ttu-id="34a5e-109">popis</span><span class="sxs-lookup"><span data-stu-id="34a5e-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="34a5e-110">200000000</span><span class="sxs-lookup"><span data-stu-id="34a5e-110">200000000</span></span> | <span data-ttu-id="34a5e-111">Nedokončeno</span><span class="sxs-lookup"><span data-stu-id="34a5e-111">Not Complete</span></span> | <span data-ttu-id="34a5e-112">Kandidát dosud neabsolvoval prověřování.</span><span class="sxs-lookup"><span data-stu-id="34a5e-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="34a5e-113">200000001</span><span class="sxs-lookup"><span data-stu-id="34a5e-113">200000001</span></span> | <span data-ttu-id="34a5e-114">Úspěšný</span><span class="sxs-lookup"><span data-stu-id="34a5e-114">Pass</span></span> | <span data-ttu-id="34a5e-115">Kandidát úspěšně prošel prověřováním.</span><span class="sxs-lookup"><span data-stu-id="34a5e-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="34a5e-116">200000002</span><span class="sxs-lookup"><span data-stu-id="34a5e-116">200000002</span></span> | <span data-ttu-id="34a5e-117">Chyba</span><span class="sxs-lookup"><span data-stu-id="34a5e-117">Fail</span></span> | <span data-ttu-id="34a5e-118">Kandidát selhal při prověřování.</span><span class="sxs-lookup"><span data-stu-id="34a5e-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="34a5e-119">Viz také</span><span class="sxs-lookup"><span data-stu-id="34a5e-119">See also</span></span>

[<span data-ttu-id="34a5e-120">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="34a5e-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="34a5e-121">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="34a5e-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
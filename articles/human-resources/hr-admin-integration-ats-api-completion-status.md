---
title: Stav dokončení
description: Toto téma popisuje sadu možností stavu dokončení pro Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1b0c61ac9d9dc611d2a4700a1a004e3d15b4445
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798362"
---
# <a name="completion-status"></a><span data-ttu-id="53173-103">Stav dokončení</span><span class="sxs-lookup"><span data-stu-id="53173-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="53173-104">Toto téma popisuje sadu možností stavu dokončení pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="53173-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="53173-105">Fyzický název: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="53173-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="53173-106">Tento výčet poskytuje sadu možností pro hodnoty stavu prověřování kandidátů.</span><span class="sxs-lookup"><span data-stu-id="53173-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="53173-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="53173-107">Value</span></span> | <span data-ttu-id="53173-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="53173-108">Label</span></span> | <span data-ttu-id="53173-109">popis</span><span class="sxs-lookup"><span data-stu-id="53173-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="53173-110">200000000</span><span class="sxs-lookup"><span data-stu-id="53173-110">200000000</span></span> | <span data-ttu-id="53173-111">Nedokončeno</span><span class="sxs-lookup"><span data-stu-id="53173-111">Not Complete</span></span> | <span data-ttu-id="53173-112">Kandidát dosud neabsolvoval prověřování.</span><span class="sxs-lookup"><span data-stu-id="53173-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="53173-113">200000001</span><span class="sxs-lookup"><span data-stu-id="53173-113">200000001</span></span> | <span data-ttu-id="53173-114">Úspěšný</span><span class="sxs-lookup"><span data-stu-id="53173-114">Pass</span></span> | <span data-ttu-id="53173-115">Kandidát úspěšně prošel prověřováním.</span><span class="sxs-lookup"><span data-stu-id="53173-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="53173-116">200000002</span><span class="sxs-lookup"><span data-stu-id="53173-116">200000002</span></span> | <span data-ttu-id="53173-117">Chyba</span><span class="sxs-lookup"><span data-stu-id="53173-117">Fail</span></span> | <span data-ttu-id="53173-118">Kandidát selhal při prověřování.</span><span class="sxs-lookup"><span data-stu-id="53173-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="53173-119">Viz také</span><span class="sxs-lookup"><span data-stu-id="53173-119">See also</span></span>

[<span data-ttu-id="53173-120">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="53173-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="53173-121">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="53173-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
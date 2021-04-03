---
title: Výsledek integrace uchazeče
description: Toto téma popisuje sadu možností výsledku integrace uchazeče pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467546"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="ef540-103">Výsledek integrace uchazeče</span><span class="sxs-lookup"><span data-stu-id="ef540-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ef540-104">Toto téma popisuje sadu možností výsledku integrace uchazeče pro Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ef540-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ef540-105">Fyzický název: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="ef540-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="ef540-106">Tento výčet poskytuje stav záznamu kandidáta.</span><span class="sxs-lookup"><span data-stu-id="ef540-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="ef540-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="ef540-107">Value</span></span> | <span data-ttu-id="ef540-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="ef540-108">Label</span></span> | <span data-ttu-id="ef540-109">popis</span><span class="sxs-lookup"><span data-stu-id="ef540-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ef540-110">200000000</span><span class="sxs-lookup"><span data-stu-id="ef540-110">200000000</span></span> | <span data-ttu-id="ef540-111">Nezpracováno</span><span class="sxs-lookup"><span data-stu-id="ef540-111">Not processed</span></span> | <span data-ttu-id="ef540-112">Kandidát stále přichází v úvahu.</span><span class="sxs-lookup"><span data-stu-id="ef540-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="ef540-113">200000001</span><span class="sxs-lookup"><span data-stu-id="ef540-113">200000001</span></span> | <span data-ttu-id="ef540-114">Zařazeno</span><span class="sxs-lookup"><span data-stu-id="ef540-114">Hired</span></span> | <span data-ttu-id="ef540-115">Kandidát byl přijat.</span><span class="sxs-lookup"><span data-stu-id="ef540-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="ef540-116">200000002</span><span class="sxs-lookup"><span data-stu-id="ef540-116">200000002</span></span> | <span data-ttu-id="ef540-117">Nepřijat/a</span><span class="sxs-lookup"><span data-stu-id="ef540-117">Not hired</span></span> | <span data-ttu-id="ef540-118">Bylo rozhodnuto nezaměstnat kandidáta.</span><span class="sxs-lookup"><span data-stu-id="ef540-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="ef540-119">200000003</span><span class="sxs-lookup"><span data-stu-id="ef540-119">200000003</span></span> | <span data-ttu-id="ef540-120">Zamítnuto</span><span class="sxs-lookup"><span data-stu-id="ef540-120">Dismissed</span></span> | <span data-ttu-id="ef540-121">Kandidát byl vyloučen z úvahy.</span><span class="sxs-lookup"><span data-stu-id="ef540-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ef540-122">Viz také</span><span class="sxs-lookup"><span data-stu-id="ef540-122">See also</span></span>

[<span data-ttu-id="ef540-123">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="ef540-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ef540-124">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="ef540-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
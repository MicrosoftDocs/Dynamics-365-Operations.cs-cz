---
title: Stav pozice v žádosti o nábor
description: Toto téma popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126043"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="7a4e2-103">Stav pozice v žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="7a4e2-103">Recruiting request position status</span></span>

<span data-ttu-id="7a4e2-104">Toto téma popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7a4e2-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7a4e2-105">Fyzický název: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="7a4e2-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="7a4e2-106">Tento výčet poskytuje sadu možností pro stavové hodnoty každé pozice a požadavek na nábor v entitě RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="7a4e2-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="7a4e2-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="7a4e2-107">Value</span></span> | <span data-ttu-id="7a4e2-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="7a4e2-108">Label</span></span> | <span data-ttu-id="7a4e2-109">popis</span><span class="sxs-lookup"><span data-stu-id="7a4e2-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7a4e2-110">200000000</span><span class="sxs-lookup"><span data-stu-id="7a4e2-110">200000000</span></span> | <span data-ttu-id="7a4e2-111">Otevřená</span><span class="sxs-lookup"><span data-stu-id="7a4e2-111">Open</span></span> | <span data-ttu-id="7a4e2-112">Pozice v požadavku na nábor je pro nábor otevřená.</span><span class="sxs-lookup"><span data-stu-id="7a4e2-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="7a4e2-113">To neznamená, že pro pozici není aktuálně aktivní přiřazení pozice.</span><span class="sxs-lookup"><span data-stu-id="7a4e2-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="7a4e2-114">V době náboru může být na pozici zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="7a4e2-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="7a4e2-115">Označuje pouze to, že pozice je k dispozici pro nábor v kontextu požadavku na nábor.</span><span class="sxs-lookup"><span data-stu-id="7a4e2-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="7a4e2-116">200000001</span><span class="sxs-lookup"><span data-stu-id="7a4e2-116">200000001</span></span> | <span data-ttu-id="7a4e2-117">Obsazená</span><span class="sxs-lookup"><span data-stu-id="7a4e2-117">Filled</span></span> | <span data-ttu-id="7a4e2-118">Pro zařazení na pozici byl vybrán pracovník.</span><span class="sxs-lookup"><span data-stu-id="7a4e2-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="7a4e2-119">200000002</span><span class="sxs-lookup"><span data-stu-id="7a4e2-119">200000002</span></span> | <span data-ttu-id="7a4e2-120">Zrušená</span><span class="sxs-lookup"><span data-stu-id="7a4e2-120">Canceled</span></span> | <span data-ttu-id="7a4e2-121">Žádost o nábor na tuto pozici byla zrušena.</span><span class="sxs-lookup"><span data-stu-id="7a4e2-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7a4e2-122">Viz také</span><span class="sxs-lookup"><span data-stu-id="7a4e2-122">See also</span></span>

[<span data-ttu-id="7a4e2-123">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="7a4e2-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7a4e2-124">Příklad dotazu na žádost o nábor</span><span class="sxs-lookup"><span data-stu-id="7a4e2-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

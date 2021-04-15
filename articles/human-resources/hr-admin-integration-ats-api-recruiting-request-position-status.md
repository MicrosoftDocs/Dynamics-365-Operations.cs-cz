---
title: Stav pozice v žádosti o nábor
description: Toto téma popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789724"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="f497f-103">Stav pozice v žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="f497f-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f497f-104">Toto téma popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f497f-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f497f-105">Fyzický název: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="f497f-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="f497f-106">Tento výčet poskytuje sadu možností pro stavové hodnoty každé pozice a požadavek na nábor v entitě RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="f497f-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="f497f-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f497f-107">Value</span></span> | <span data-ttu-id="f497f-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="f497f-108">Label</span></span> | <span data-ttu-id="f497f-109">popis</span><span class="sxs-lookup"><span data-stu-id="f497f-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f497f-110">200000000</span><span class="sxs-lookup"><span data-stu-id="f497f-110">200000000</span></span> | <span data-ttu-id="f497f-111">Otevřená</span><span class="sxs-lookup"><span data-stu-id="f497f-111">Open</span></span> | <span data-ttu-id="f497f-112">Pozice v požadavku na nábor je pro nábor otevřená.</span><span class="sxs-lookup"><span data-stu-id="f497f-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="f497f-113">To neznamená, že pro pozici není aktuálně aktivní přiřazení pozice.</span><span class="sxs-lookup"><span data-stu-id="f497f-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="f497f-114">V době náboru může být na pozici zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="f497f-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="f497f-115">Označuje pouze to, že pozice je k dispozici pro nábor v kontextu požadavku na nábor.</span><span class="sxs-lookup"><span data-stu-id="f497f-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="f497f-116">200000001</span><span class="sxs-lookup"><span data-stu-id="f497f-116">200000001</span></span> | <span data-ttu-id="f497f-117">Obsazená</span><span class="sxs-lookup"><span data-stu-id="f497f-117">Filled</span></span> | <span data-ttu-id="f497f-118">Pro zařazení na pozici byl vybrán pracovník.</span><span class="sxs-lookup"><span data-stu-id="f497f-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="f497f-119">200000002</span><span class="sxs-lookup"><span data-stu-id="f497f-119">200000002</span></span> | <span data-ttu-id="f497f-120">Zrušená</span><span class="sxs-lookup"><span data-stu-id="f497f-120">Canceled</span></span> | <span data-ttu-id="f497f-121">Žádost o nábor na tuto pozici byla zrušena.</span><span class="sxs-lookup"><span data-stu-id="f497f-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f497f-122">Viz také</span><span class="sxs-lookup"><span data-stu-id="f497f-122">See also</span></span>

[<span data-ttu-id="f497f-123">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="f497f-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f497f-124">Příklad dotazu na žádost o nábor</span><span class="sxs-lookup"><span data-stu-id="f497f-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
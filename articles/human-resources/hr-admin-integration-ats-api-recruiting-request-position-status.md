---
title: Stav pozice v žádosti o nábor
description: Toto téma popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.
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
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051874"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="60fad-103">Stav pozice v žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="60fad-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="60fad-104">Toto téma popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="60fad-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="60fad-105">Fyzický název: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="60fad-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="60fad-106">Tento výčet poskytuje sadu možností pro stavové hodnoty každé pozice a požadavek na nábor v entitě RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="60fad-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="60fad-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="60fad-107">Value</span></span> | <span data-ttu-id="60fad-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="60fad-108">Label</span></span> | <span data-ttu-id="60fad-109">popis</span><span class="sxs-lookup"><span data-stu-id="60fad-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="60fad-110">200000000</span><span class="sxs-lookup"><span data-stu-id="60fad-110">200000000</span></span> | <span data-ttu-id="60fad-111">Otevřená</span><span class="sxs-lookup"><span data-stu-id="60fad-111">Open</span></span> | <span data-ttu-id="60fad-112">Pozice v požadavku na nábor je pro nábor otevřená.</span><span class="sxs-lookup"><span data-stu-id="60fad-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="60fad-113">To neznamená, že pro pozici není aktuálně aktivní přiřazení pozice.</span><span class="sxs-lookup"><span data-stu-id="60fad-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="60fad-114">V době náboru může být na pozici zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="60fad-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="60fad-115">Označuje pouze to, že pozice je k dispozici pro nábor v kontextu požadavku na nábor.</span><span class="sxs-lookup"><span data-stu-id="60fad-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="60fad-116">200000001</span><span class="sxs-lookup"><span data-stu-id="60fad-116">200000001</span></span> | <span data-ttu-id="60fad-117">Obsazená</span><span class="sxs-lookup"><span data-stu-id="60fad-117">Filled</span></span> | <span data-ttu-id="60fad-118">Pro zařazení na pozici byl vybrán pracovník.</span><span class="sxs-lookup"><span data-stu-id="60fad-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="60fad-119">200000002</span><span class="sxs-lookup"><span data-stu-id="60fad-119">200000002</span></span> | <span data-ttu-id="60fad-120">Zrušená</span><span class="sxs-lookup"><span data-stu-id="60fad-120">Canceled</span></span> | <span data-ttu-id="60fad-121">Žádost o nábor na tuto pozici byla zrušena.</span><span class="sxs-lookup"><span data-stu-id="60fad-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="60fad-122">Viz také</span><span class="sxs-lookup"><span data-stu-id="60fad-122">See also</span></span>

[<span data-ttu-id="60fad-123">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="60fad-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="60fad-124">Příklad dotazu na žádost o nábor</span><span class="sxs-lookup"><span data-stu-id="60fad-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
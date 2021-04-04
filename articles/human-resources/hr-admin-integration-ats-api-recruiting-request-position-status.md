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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464711"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="ebde9-103">Stav pozice v žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="ebde9-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ebde9-104">Toto téma popisuje stav nastavená pro pozici žádosti o nábor Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ebde9-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ebde9-105">Fyzický název: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="ebde9-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="ebde9-106">Tento výčet poskytuje sadu možností pro stavové hodnoty každé pozice a požadavek na nábor v entitě RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="ebde9-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="ebde9-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="ebde9-107">Value</span></span> | <span data-ttu-id="ebde9-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="ebde9-108">Label</span></span> | <span data-ttu-id="ebde9-109">popis</span><span class="sxs-lookup"><span data-stu-id="ebde9-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ebde9-110">200000000</span><span class="sxs-lookup"><span data-stu-id="ebde9-110">200000000</span></span> | <span data-ttu-id="ebde9-111">Otevřená</span><span class="sxs-lookup"><span data-stu-id="ebde9-111">Open</span></span> | <span data-ttu-id="ebde9-112">Pozice v požadavku na nábor je pro nábor otevřená.</span><span class="sxs-lookup"><span data-stu-id="ebde9-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="ebde9-113">To neznamená, že pro pozici není aktuálně aktivní přiřazení pozice.</span><span class="sxs-lookup"><span data-stu-id="ebde9-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="ebde9-114">V době náboru může být na pozici zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="ebde9-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="ebde9-115">Označuje pouze to, že pozice je k dispozici pro nábor v kontextu požadavku na nábor.</span><span class="sxs-lookup"><span data-stu-id="ebde9-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="ebde9-116">200000001</span><span class="sxs-lookup"><span data-stu-id="ebde9-116">200000001</span></span> | <span data-ttu-id="ebde9-117">Obsazená</span><span class="sxs-lookup"><span data-stu-id="ebde9-117">Filled</span></span> | <span data-ttu-id="ebde9-118">Pro zařazení na pozici byl vybrán pracovník.</span><span class="sxs-lookup"><span data-stu-id="ebde9-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="ebde9-119">200000002</span><span class="sxs-lookup"><span data-stu-id="ebde9-119">200000002</span></span> | <span data-ttu-id="ebde9-120">Zrušená</span><span class="sxs-lookup"><span data-stu-id="ebde9-120">Canceled</span></span> | <span data-ttu-id="ebde9-121">Žádost o nábor na tuto pozici byla zrušena.</span><span class="sxs-lookup"><span data-stu-id="ebde9-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ebde9-122">Viz také</span><span class="sxs-lookup"><span data-stu-id="ebde9-122">See also</span></span>

[<span data-ttu-id="ebde9-123">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="ebde9-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ebde9-124">Příklad dotazu na žádost o nábor</span><span class="sxs-lookup"><span data-stu-id="ebde9-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
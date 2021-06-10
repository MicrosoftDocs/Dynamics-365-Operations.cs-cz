---
title: Stav žádosti o nábor
description: Toto téma popisuje stav nastavená pro stav žádosti o nábor Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059177"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="c2051-103">Stav žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="c2051-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c2051-104">Toto téma popisuje stav nastavená pro stav žádosti o nábor Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c2051-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c2051-105">Fyzický název: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="c2051-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="c2051-106">Tento výčet poskytuje sadu možností pro stavové hodnoty RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="c2051-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="c2051-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="c2051-107">Value</span></span> | <span data-ttu-id="c2051-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="c2051-108">Label</span></span> | <span data-ttu-id="c2051-109">popis</span><span class="sxs-lookup"><span data-stu-id="c2051-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c2051-110">200000000</span><span class="sxs-lookup"><span data-stu-id="c2051-110">200000000</span></span> | <span data-ttu-id="c2051-111">Koncept</span><span class="sxs-lookup"><span data-stu-id="c2051-111">Draft</span></span> | <span data-ttu-id="c2051-112">Žádost je ve stavu konceptu a není připravena na aktivní nábor.</span><span class="sxs-lookup"><span data-stu-id="c2051-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="c2051-113">200000001</span><span class="sxs-lookup"><span data-stu-id="c2051-113">200000001</span></span> | <span data-ttu-id="c2051-114">Probíhá kontrola</span><span class="sxs-lookup"><span data-stu-id="c2051-114">In Review</span></span> | <span data-ttu-id="c2051-115">Žádost byla odeslána a je směrována ke schválení pomocí pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="c2051-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="c2051-116">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="c2051-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c2051-117">200000002</span><span class="sxs-lookup"><span data-stu-id="c2051-117">200000002</span></span> | <span data-ttu-id="c2051-118">Čeká na zpracování</span><span class="sxs-lookup"><span data-stu-id="c2051-118">Pending</span></span> | <span data-ttu-id="c2051-119">Požadavek čeká na provedení pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="c2051-119">The request is pending workflow action.</span></span> <span data-ttu-id="c2051-120">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="c2051-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c2051-121">200000003</span><span class="sxs-lookup"><span data-stu-id="c2051-121">200000003</span></span> | <span data-ttu-id="c2051-122">Zrušená</span><span class="sxs-lookup"><span data-stu-id="c2051-122">Canceled</span></span> | <span data-ttu-id="c2051-123">Požadavek byl zrušen.</span><span class="sxs-lookup"><span data-stu-id="c2051-123">The request has been canceled.</span></span> <span data-ttu-id="c2051-124">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="c2051-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c2051-125">200000004</span><span class="sxs-lookup"><span data-stu-id="c2051-125">200000004</span></span> | <span data-ttu-id="c2051-126">Zamítnutý</span><span class="sxs-lookup"><span data-stu-id="c2051-126">Denied</span></span> | <span data-ttu-id="c2051-127">Žádost byla zamítnuta.</span><span class="sxs-lookup"><span data-stu-id="c2051-127">The request has been denied.</span></span> <span data-ttu-id="c2051-128">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="c2051-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c2051-129">200000005</span><span class="sxs-lookup"><span data-stu-id="c2051-129">200000005</span></span> | <span data-ttu-id="c2051-130">Aktivní</span><span class="sxs-lookup"><span data-stu-id="c2051-130">Active</span></span> | <span data-ttu-id="c2051-131">Jakýkoli pracovní postup je dokončen a schválen a požadavek je připraven k aktivnímu náboru.</span><span class="sxs-lookup"><span data-stu-id="c2051-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="c2051-132">200000006</span><span class="sxs-lookup"><span data-stu-id="c2051-132">200000006</span></span> | <span data-ttu-id="c2051-133">Uzavřený</span><span class="sxs-lookup"><span data-stu-id="c2051-133">Closed</span></span> | <span data-ttu-id="c2051-134">Žádost o nábor je uzavřena.</span><span class="sxs-lookup"><span data-stu-id="c2051-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c2051-135">Viz také</span><span class="sxs-lookup"><span data-stu-id="c2051-135">See also</span></span>

[<span data-ttu-id="c2051-136">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="c2051-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="c2051-137">Příklad dotazu na žádost o nábor</span><span class="sxs-lookup"><span data-stu-id="c2051-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
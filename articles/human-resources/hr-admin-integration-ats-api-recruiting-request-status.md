---
title: Stav žádosti o nábor
description: Toto téma popisuje stav nastavená pro stav žádosti o nábor Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464639"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="f47a2-103">Stav žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="f47a2-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f47a2-104">Toto téma popisuje stav nastavená pro stav žádosti o nábor Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f47a2-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f47a2-105">Fyzický název: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="f47a2-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="f47a2-106">Tento výčet poskytuje sadu možností pro stavové hodnoty RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="f47a2-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="f47a2-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="f47a2-107">Value</span></span> | <span data-ttu-id="f47a2-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="f47a2-108">Label</span></span> | <span data-ttu-id="f47a2-109">popis</span><span class="sxs-lookup"><span data-stu-id="f47a2-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f47a2-110">200000000</span><span class="sxs-lookup"><span data-stu-id="f47a2-110">200000000</span></span> | <span data-ttu-id="f47a2-111">Koncept</span><span class="sxs-lookup"><span data-stu-id="f47a2-111">Draft</span></span> | <span data-ttu-id="f47a2-112">Žádost je ve stavu konceptu a není připravena na aktivní nábor.</span><span class="sxs-lookup"><span data-stu-id="f47a2-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="f47a2-113">200000001</span><span class="sxs-lookup"><span data-stu-id="f47a2-113">200000001</span></span> | <span data-ttu-id="f47a2-114">Probíhá kontrola</span><span class="sxs-lookup"><span data-stu-id="f47a2-114">In Review</span></span> | <span data-ttu-id="f47a2-115">Žádost byla odeslána a je směrována ke schválení pomocí pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="f47a2-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="f47a2-116">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="f47a2-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="f47a2-117">200000002</span><span class="sxs-lookup"><span data-stu-id="f47a2-117">200000002</span></span> | <span data-ttu-id="f47a2-118">Čeká na zpracování</span><span class="sxs-lookup"><span data-stu-id="f47a2-118">Pending</span></span> | <span data-ttu-id="f47a2-119">Požadavek čeká na provedení pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="f47a2-119">The request is pending workflow action.</span></span> <span data-ttu-id="f47a2-120">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="f47a2-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="f47a2-121">200000003</span><span class="sxs-lookup"><span data-stu-id="f47a2-121">200000003</span></span> | <span data-ttu-id="f47a2-122">Zrušená</span><span class="sxs-lookup"><span data-stu-id="f47a2-122">Canceled</span></span> | <span data-ttu-id="f47a2-123">Požadavek byl zrušen.</span><span class="sxs-lookup"><span data-stu-id="f47a2-123">The request has been canceled.</span></span> <span data-ttu-id="f47a2-124">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="f47a2-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="f47a2-125">200000004</span><span class="sxs-lookup"><span data-stu-id="f47a2-125">200000004</span></span> | <span data-ttu-id="f47a2-126">Zamítnutý</span><span class="sxs-lookup"><span data-stu-id="f47a2-126">Denied</span></span> | <span data-ttu-id="f47a2-127">Žádost byla zamítnuta.</span><span class="sxs-lookup"><span data-stu-id="f47a2-127">The request has been denied.</span></span> <span data-ttu-id="f47a2-128">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="f47a2-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="f47a2-129">200000005</span><span class="sxs-lookup"><span data-stu-id="f47a2-129">200000005</span></span> | <span data-ttu-id="f47a2-130">Aktivní</span><span class="sxs-lookup"><span data-stu-id="f47a2-130">Active</span></span> | <span data-ttu-id="f47a2-131">Jakýkoli pracovní postup je dokončen a schválen a požadavek je připraven k aktivnímu náboru.</span><span class="sxs-lookup"><span data-stu-id="f47a2-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="f47a2-132">200000006</span><span class="sxs-lookup"><span data-stu-id="f47a2-132">200000006</span></span> | <span data-ttu-id="f47a2-133">Uzavřený</span><span class="sxs-lookup"><span data-stu-id="f47a2-133">Closed</span></span> | <span data-ttu-id="f47a2-134">Žádost o nábor je uzavřena.</span><span class="sxs-lookup"><span data-stu-id="f47a2-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f47a2-135">Viz také</span><span class="sxs-lookup"><span data-stu-id="f47a2-135">See also</span></span>

[<span data-ttu-id="f47a2-136">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="f47a2-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f47a2-137">Příklad dotazu na žádost o nábor</span><span class="sxs-lookup"><span data-stu-id="f47a2-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
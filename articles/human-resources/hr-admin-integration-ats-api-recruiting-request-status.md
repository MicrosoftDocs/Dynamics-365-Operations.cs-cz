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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125947"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="86b0a-103">Stav žádosti o nábor</span><span class="sxs-lookup"><span data-stu-id="86b0a-103">Recruiting request status</span></span>

<span data-ttu-id="86b0a-104">Toto téma popisuje stav nastavená pro stav žádosti o nábor Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="86b0a-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="86b0a-105">Fyzický název: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="86b0a-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="86b0a-106">Tento výčet poskytuje sadu možností pro stavové hodnoty RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="86b0a-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="86b0a-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="86b0a-107">Value</span></span> | <span data-ttu-id="86b0a-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="86b0a-108">Label</span></span> | <span data-ttu-id="86b0a-109">popis</span><span class="sxs-lookup"><span data-stu-id="86b0a-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="86b0a-110">200000000</span><span class="sxs-lookup"><span data-stu-id="86b0a-110">200000000</span></span> | <span data-ttu-id="86b0a-111">Koncept</span><span class="sxs-lookup"><span data-stu-id="86b0a-111">Draft</span></span> | <span data-ttu-id="86b0a-112">Žádost je ve stavu konceptu a není připravena na aktivní nábor.</span><span class="sxs-lookup"><span data-stu-id="86b0a-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="86b0a-113">200000001</span><span class="sxs-lookup"><span data-stu-id="86b0a-113">200000001</span></span> | <span data-ttu-id="86b0a-114">Probíhá kontrola</span><span class="sxs-lookup"><span data-stu-id="86b0a-114">In Review</span></span> | <span data-ttu-id="86b0a-115">Žádost byla odeslána a je směrována ke schválení pomocí pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="86b0a-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="86b0a-116">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="86b0a-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="86b0a-117">200000002</span><span class="sxs-lookup"><span data-stu-id="86b0a-117">200000002</span></span> | <span data-ttu-id="86b0a-118">Čeká na zpracování</span><span class="sxs-lookup"><span data-stu-id="86b0a-118">Pending</span></span> | <span data-ttu-id="86b0a-119">Požadavek čeká na provedení pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="86b0a-119">The request is pending workflow action.</span></span> <span data-ttu-id="86b0a-120">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="86b0a-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="86b0a-121">200000003</span><span class="sxs-lookup"><span data-stu-id="86b0a-121">200000003</span></span> | <span data-ttu-id="86b0a-122">Zrušená</span><span class="sxs-lookup"><span data-stu-id="86b0a-122">Canceled</span></span> | <span data-ttu-id="86b0a-123">Požadavek byl zrušen.</span><span class="sxs-lookup"><span data-stu-id="86b0a-123">The request has been canceled.</span></span> <span data-ttu-id="86b0a-124">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="86b0a-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="86b0a-125">200000004</span><span class="sxs-lookup"><span data-stu-id="86b0a-125">200000004</span></span> | <span data-ttu-id="86b0a-126">Zamítnutý</span><span class="sxs-lookup"><span data-stu-id="86b0a-126">Denied</span></span> | <span data-ttu-id="86b0a-127">Žádost byla zamítnuta.</span><span class="sxs-lookup"><span data-stu-id="86b0a-127">The request has been denied.</span></span> <span data-ttu-id="86b0a-128">K dispozici je pouze v případě, že je povolen pracovní postup.</span><span class="sxs-lookup"><span data-stu-id="86b0a-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="86b0a-129">200000005</span><span class="sxs-lookup"><span data-stu-id="86b0a-129">200000005</span></span> | <span data-ttu-id="86b0a-130">Aktivní</span><span class="sxs-lookup"><span data-stu-id="86b0a-130">Active</span></span> | <span data-ttu-id="86b0a-131">Jakýkoli pracovní postup je dokončen a schválen a požadavek je připraven k aktivnímu náboru.</span><span class="sxs-lookup"><span data-stu-id="86b0a-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="86b0a-132">200000006</span><span class="sxs-lookup"><span data-stu-id="86b0a-132">200000006</span></span> | <span data-ttu-id="86b0a-133">Uzavřený</span><span class="sxs-lookup"><span data-stu-id="86b0a-133">Closed</span></span> | <span data-ttu-id="86b0a-134">Žádost o nábor je uzavřena.</span><span class="sxs-lookup"><span data-stu-id="86b0a-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="86b0a-135">Viz také</span><span class="sxs-lookup"><span data-stu-id="86b0a-135">See also</span></span>

[<span data-ttu-id="86b0a-136">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="86b0a-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="86b0a-137">Příklad dotazu na žádost o nábor</span><span class="sxs-lookup"><span data-stu-id="86b0a-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

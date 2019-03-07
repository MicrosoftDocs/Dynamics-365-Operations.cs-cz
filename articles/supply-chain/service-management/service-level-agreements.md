---
title: Smlouvy úrovně služeb
description: Ve smlouvě SLA odběratel souhlasí s minimálním časem odezvy od okamžiku, kdy servisní společnost zaznamená problém, do okamžiku vyřešení potíží.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cffe3a7766502dd5d888a7a99a32150967911301
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "364573"
---
# <a name="service-level-agreements"></a><span data-ttu-id="09e48-103">Smlouvy úrovně služeb</span><span class="sxs-lookup"><span data-stu-id="09e48-103">Service level agreements</span></span>        

[!include [banner](../includes/banner.md)]


<span data-ttu-id="09e48-104">Smlouva o úrovni služeb (SLA) představuje dohodu mezi servisní společností a odběratelem služeb.</span><span class="sxs-lookup"><span data-stu-id="09e48-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="09e48-105">Ve smlouvě SLA odběratel souhlasí s minimálním časem odezvy od okamžiku, kdy servisní společnost zaznamená problém, do okamžiku vyřešení potíží.</span><span class="sxs-lookup"><span data-stu-id="09e48-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="09e48-106">Smlouva SLA zaručuje standardní úroveň služeb, které jsou nabízeny zákazníkům, a také pro servisní společnost jasně definuje čas, za který musí být servisní zákrok dokončený.</span><span class="sxs-lookup"><span data-stu-id="09e48-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="09e48-107">Odběratelům služeb lze nabídnout různé úrovně služeb, pro které lze vytvořit různé smlouvy SLA.</span><span class="sxs-lookup"><span data-stu-id="09e48-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="09e48-108">Vytvoření smlouvy o úrovni služeb (SLA)</span><span class="sxs-lookup"><span data-stu-id="09e48-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="09e48-109">Klikněte na **Správa servisu** \> **Nastavení** \> **Servisní smlouvy** \> **Smlouva o úrovni služeb**.</span><span class="sxs-lookup"><span data-stu-id="09e48-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="09e48-110">Zadejte název smlouvy o úrovni služeb do pole **Smlouva o úrovni služeb**.</span><span class="sxs-lookup"><span data-stu-id="09e48-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="09e48-111">Zadejte čas, který chcete povolit pro dokončení servisních volání, která jsou připojena ke smlouvě o úrovni služeb.</span><span class="sxs-lookup"><span data-stu-id="09e48-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="09e48-112">Poté vyberte kalendář, pokud chcete založit smlouvu o úrovni služeb na konkrétním kalendáři.</span><span class="sxs-lookup"><span data-stu-id="09e48-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="09e48-113">Použití smlouvy o úrovni služeb (SLA)</span><span class="sxs-lookup"><span data-stu-id="09e48-113">Apply a service level agreement</span></span>

<span data-ttu-id="09e48-114">Smlouva SLA se použije přímo na servisní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="09e48-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="09e48-115">Servisní zakázky, které vytvoříte ručně a připojíte k servisní smlouvě se smlouvou SLA, jsou kontrolovány proti této smlouvě SLA.</span><span class="sxs-lookup"><span data-stu-id="09e48-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="09e48-116">Servisní zakázky, které jsou vytvořeny automaticky, nejsou připojeny ke smlouvě SLA.</span><span class="sxs-lookup"><span data-stu-id="09e48-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="09e48-117">Použití smlouvy o úrovni služeb na servisní smlouvu</span><span class="sxs-lookup"><span data-stu-id="09e48-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="09e48-118">Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="09e48-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="09e48-119">Vyberte servisní smlouvu, pro kterou chcete použít SLA, a klepněte na tlačítko **upravit** v **podokně akcí**.</span><span class="sxs-lookup"><span data-stu-id="09e48-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="09e48-120">V poli **smlouva o úrovni služeb** vyberte smlouvy o úrovni služeb, které chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="09e48-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="09e48-121">Použití smlouvy o úrovni služeb na skupinu servisních smluv</span><span class="sxs-lookup"><span data-stu-id="09e48-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="09e48-122">Klikněte na **Správa servisu** \> **Nastavení** \> **Servisní smlouvy** \> **Skupiny servisních smluv**.</span><span class="sxs-lookup"><span data-stu-id="09e48-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="09e48-123">V poli **smlouva o úrovni služeb** vyberte smlouvy o úrovni služeb, které chcete přiřadit.</span><span class="sxs-lookup"><span data-stu-id="09e48-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="09e48-124">Sledování času v servisní smlouvě v porovnání se smlouvou SLA</span><span class="sxs-lookup"><span data-stu-id="09e48-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="09e48-125">Při vytváření nové servisní zakázky pro servisní smlouvy, které je přiřazena SLA, může být aktivován časový interval pro dodání služby a systém začne sledovat čas dodání.</span><span class="sxs-lookup"><span data-stu-id="09e48-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="09e48-126">Navíc můžete nastavit následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="09e48-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="09e48-127">Sledování času pro servisní zakázky lze spouštět a zastavovat a sledovat celkový čas strávených na servisních zakázkách.</span><span class="sxs-lookup"><span data-stu-id="09e48-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="09e48-128">Můžete kontrolovat dodržování dohodnutého časového intervalu odezvy, který je určený ve smlouvě o úrovni služeb.</span><span class="sxs-lookup"><span data-stu-id="09e48-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="09e48-129">Můžete definovat kódy rozhodnutí, které je nutné nastavit při překročení časového intervalu určeného smlouvou SLA.</span><span class="sxs-lookup"><span data-stu-id="09e48-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="09e48-130">Viz také</span><span class="sxs-lookup"><span data-stu-id="09e48-130">See also</span></span>

[<span data-ttu-id="09e48-131">Zobrazení shody se smlouvou na úrovni služeb</span><span class="sxs-lookup"><span data-stu-id="09e48-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  



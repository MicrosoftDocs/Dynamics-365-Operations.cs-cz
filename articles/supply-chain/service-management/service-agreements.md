---
title: "Servisní smlouvy"
description: "Servisní smlouvy vám umožňují definovat zdroje používané při typické servisní návštěvě a způsob, jakým jsou tyto zdroje fakturovány odběrateli."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bf9df2a31c758ba6b63ac7952e00065df04552dc
ms.openlocfilehash: aaff0c1d71fcf2656d5d6e76a2bf4b7b3a699281
ms.contentlocale: cs-cz
ms.lasthandoff: 02/19/2018

---

# <a name="service-agreements"></a><span data-ttu-id="e088d-103">Servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="e088d-103">Service agreements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e088d-104">Servisní smlouvy vám umožňují definovat zdroje používané při typické servisní návštěvě a způsob, jakým jsou tyto zdroje fakturovány odběrateli.</span><span class="sxs-lookup"><span data-stu-id="e088d-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="e088d-105">Každá servisní smlouva je připojena k projektu, jehož prostřednictvím jsou transakce zaúčtovány a fakturovány.</span><span class="sxs-lookup"><span data-stu-id="e088d-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="e088d-106">Transakce servisních zakázek lze však fakturovat také přímo prostřednictvím projektu bez nutnosti připojení servisní zakázky k servisní smlouvě.</span><span class="sxs-lookup"><span data-stu-id="e088d-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="e088d-107">Učinit tak můžete v případě, že je servisní zakázka určena pro jednorázovou servisní návštěvu a nutnost zpracování transakcí servisu rychle převáží nutnost udržovat podrobné informace servisní smlouvy o odběrateli po určitou dobu.</span><span class="sxs-lookup"><span data-stu-id="e088d-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="e088d-108">Servisní smlouva</span><span class="sxs-lookup"><span data-stu-id="e088d-108">Service agreement</span></span>

<span data-ttu-id="e088d-109">V každé servisní smlouvě je nutné zadat projekt, ID servisní smlouvy a skupinu servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="e088d-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="e088d-110">Skupinu servisní smlouvy lze použít k řazení a organizování servisních smluv.</span><span class="sxs-lookup"><span data-stu-id="e088d-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="e088d-111">Záhlaví servisní smlouvy obsahuje nastavení, která se vztahují na všechny přiřazené řádky smlouvy:</span><span class="sxs-lookup"><span data-stu-id="e088d-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="e088d-112">Jedná se o nastavení, které určuje, zda je servisní smlouva pozastavena.</span><span class="sxs-lookup"><span data-stu-id="e088d-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="e088d-113">Je-li servisní smlouva pozastavena, nelze ze servisní smlouvy generovat servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e088d-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="e088d-114">Jedná se o nastavení trvání servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="e088d-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="e088d-115">Jedná se o nastavení způsobu slučování řádků servisní zakázky do servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="e088d-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="e088d-116">Jedná se o nastavení, které určuje, zda je servisní smlouva šablonou.</span><span class="sxs-lookup"><span data-stu-id="e088d-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="e088d-117">V záhlaví servisní smlouvy lze dále nastavit všechny předměty servisu a servisní úlohy, které lze použít spolu se servisní smlouvou pomocí zadání konkrétních servisních úloh nebo předmětů servisu, které mají být připojeny k různým řádkům smlouvy.</span><span class="sxs-lookup"><span data-stu-id="e088d-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="e088d-118">Ze záhlaví servisní smlouvy lze dále kopírovat řádky servisní smlouvy nebo řádky servisní šablony do aktuální servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="e088d-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="e088d-119">Je možné pozastavit platnost servisních smluv a zastavit jednotlivé řádky servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="e088d-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="e088d-120">Jestliže v servisní smlouvě zaškrtnete políčko **Pozastavený**, nebude možné provádět následující akce:</span><span class="sxs-lookup"><span data-stu-id="e088d-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="e088d-121">Vytvořit servisní zakázky automaticky nebo ručně ze servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="e088d-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="e088d-122">Jestliže na řádku servisní smlouvy zaškrtnete políčko **Zastaveno**, nebude možné provádět následující akce:</span><span class="sxs-lookup"><span data-stu-id="e088d-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="e088d-123">Vytvořit servisní zakázky automaticky nebo ručně z řádku servisní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="e088d-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="e088d-124">Kopírovat řádek servisní smlouvy do jiné servisní smlouvy nebo zakázky.</span><span class="sxs-lookup"><span data-stu-id="e088d-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="e088d-125">Pokud je platnost servisní smlouvy pozastavena, všechny připojené řádky budou zastaveny bez ohledu na stav.</span><span class="sxs-lookup"><span data-stu-id="e088d-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="e088d-126">Řádky servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="e088d-126">Service-agreement lines</span></span>

<span data-ttu-id="e088d-127">Každý řádek servisní smlouvy podrobně popisuje obsah navrhované servisní práce.</span><span class="sxs-lookup"><span data-stu-id="e088d-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="e088d-128">Tyto řádky obsahují následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="e088d-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="e088d-129">Typ transakce a popis typu transakce</span><span class="sxs-lookup"><span data-stu-id="e088d-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="e088d-130">Zaměstnanec, který provádí servisní práci</span><span class="sxs-lookup"><span data-stu-id="e088d-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="e088d-131">Předměty, na kterých musí být prováděna pro danou servisní smlouvu</span><span class="sxs-lookup"><span data-stu-id="e088d-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="e088d-132">Frekvence, s jakou je prováděna daná práce a registrovány přiřazené transakce položek, výdajové transakce a transakce poplatků</span><span class="sxs-lookup"><span data-stu-id="e088d-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="e088d-133">Časové okno, ve kterém lze seskupit řádky servisní zakázky do servisní zakázky</span><span class="sxs-lookup"><span data-stu-id="e088d-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="e088d-134">Servisní úlohy používané k seskupení sad řádků smlouvy do pracovních úkolů a k souhrnu pro servisní techniky a odběratele o tom, jaká servisní úloha bude poskytnuta.</span><span class="sxs-lookup"><span data-stu-id="e088d-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="e088d-135">Jedná se o nastavení, které určuje, zda je řádek ukončen.</span><span class="sxs-lookup"><span data-stu-id="e088d-135">Whether a line is stopped.</span></span> <span data-ttu-id="e088d-136">Je-li řádek ukončen, nelze pro něj vytvářet servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e088d-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="e088d-137">Nastavení projektu, jako je například kategorie a vlastnost řádku</span><span class="sxs-lookup"><span data-stu-id="e088d-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e088d-138">Související témata</span><span class="sxs-lookup"><span data-stu-id="e088d-138">Related topics</span></span>

[<span data-ttu-id="e088d-139">Vytváření servisních smluv</span><span class="sxs-lookup"><span data-stu-id="e088d-139">Create service agreements</span></span>](create-service-agreements.md)


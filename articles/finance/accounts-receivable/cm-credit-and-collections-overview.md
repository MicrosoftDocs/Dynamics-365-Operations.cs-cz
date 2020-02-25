---
title: Přehled kreditu a inkas
description: V tomto tématu je uveden přehled funkcí pro kredit a inkaso.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2fdfe05483d577819d64bdf7a4ebfe5d37cd414c
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015137"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="01348-103">Přehled kreditu a inkas</span><span class="sxs-lookup"><span data-stu-id="01348-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="01348-104">Můžete spravovat úvěrový limit pro vaše zákazníky a provádět Inkasní aktivity, když se stanou nezbytnými.</span><span class="sxs-lookup"><span data-stu-id="01348-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="01348-105">Správa úvěrů</span><span class="sxs-lookup"><span data-stu-id="01348-105">Credit management</span></span>

<span data-ttu-id="01348-106">Správa úvěru odběratele vám umožňuje spravovat limity úvěru a řídit tok prodejních objednávek prostřednictvím procesu zaúčtování na základě pravidel úvěru, která vytvoříte.</span><span class="sxs-lookup"><span data-stu-id="01348-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="01348-107">Proces správy úvěru může zahrnovat libovolné z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="01348-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="01348-108">Aktualizaci atributů úvěru pro odběratele, které poskytují dodatečné informace o jejich úvěrové způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="01348-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="01348-109">Vytvoření limitů úvěru pro odběratele pomocí úprav limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="01348-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="01348-110">Vytvoření dočasných limitů úvěru pro odběratele pomocí úprav limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="01348-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="01348-111">Tímto způsobem můžete dočasně zvýšit nebo snížit úvěrové limity odběratelů na základě obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="01348-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="01348-112">Přidání dalších informací, které mohou ovlivnit limit úvěru, jako jsou informace o pojištění a zárukách.</span><span class="sxs-lookup"><span data-stu-id="01348-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="01348-113">Vytvoření skupin úvěrů odběratelů, které propojují odběratele, takže mohou sdílet jeden limit úvěru.</span><span class="sxs-lookup"><span data-stu-id="01348-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="01348-114">Přiřazení hodnocení rizik k odběratelům a následné použití těchto hodnocení k automatickému generování limitů úvěrů pro odběratele pomocí úprav limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="01348-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="01348-115">Vytvoření pravidel blokování, která blokují objednávku v jednom nebo více procesech zaúčtování na základě faktorů, jako jsou například rizika, platební podmínky, limity úvěrů, částky po splatnosti a použitá procentní hodnota limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="01348-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="01348-116">Správu seznamu prodejních objednávek, které jsou blokovány, kontolu důvodů blokování a zmírňování problémů.</span><span class="sxs-lookup"><span data-stu-id="01348-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="01348-117">Uvolnění prodejních objednávek, aby mohly pokračovat v procesu zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="01348-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="01348-118">Nastavení workflow pro správu schválení změn limitu úvěru a uvolnění prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="01348-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="01348-119">Správa inkasa</span><span class="sxs-lookup"><span data-stu-id="01348-119">Collections management</span></span>

<span data-ttu-id="01348-120">Stránka **Inkasa** poskytuje jedno ústřední zobrazení, kde jsou spravovány informace o inkasech pohledávek.</span><span class="sxs-lookup"><span data-stu-id="01348-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="01348-121">Vedoucí inkasa mohou používat toto centrálizované zobrazení ke správě inkas.</span><span class="sxs-lookup"><span data-stu-id="01348-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="01348-122">Inkasní agenti mohou zahájit proces kolekce ze seznamů odběratelů, které jsou generovány pomocí použitím předem definované kolekce kritérií nebo stránky **Odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="01348-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="01348-123">Dříve než začnete s nastavením nebo práci s inkasem, měli byste se seznámit s následujícími koncepty:</span><span class="sxs-lookup"><span data-stu-id="01348-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="01348-124">Snímky pro sledování splatnosti odběratele obsahují informace o splatném zůstatku v určitém okamžiku.</span><span class="sxs-lookup"><span data-stu-id="01348-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="01348-125">Fondy zákazníků kolekce pomáhají v uspořádání vaší práce.</span><span class="sxs-lookup"><span data-stu-id="01348-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="01348-126">Inkasní agenti mohou mít své vlastní fondy zákazníků.</span><span class="sxs-lookup"><span data-stu-id="01348-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="01348-127">Stránky seznamů umožňují uspořádat odběratele inkasa, aktivity a případy.</span><span class="sxs-lookup"><span data-stu-id="01348-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="01348-128">Všechny informace o inkasu odběratele jsou na jedné stránku, která umožňuje provádět další akce.</span><span class="sxs-lookup"><span data-stu-id="01348-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="01348-129">Odpuštění, obnovení nebo stornování úroků a poplatků je možné provést v jednom kroku.</span><span class="sxs-lookup"><span data-stu-id="01348-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="01348-130">Vytvoření transakcí odpisů je možné provést v jednom kroku.</span><span class="sxs-lookup"><span data-stu-id="01348-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="01348-131">Zpracování plateb s nedostatečnými finančními prostředky je možné provést v jednom kroku.</span><span class="sxs-lookup"><span data-stu-id="01348-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="01348-132">Popis těchto pojmů naleznete v tématu [Koncepty správy inkasa](./cm-collections-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="01348-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01348-133">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="01348-133">Additional resources</span></span>

[<span data-ttu-id="01348-134">Nastavení parametrů správy úvěru odběratelů</span><span class="sxs-lookup"><span data-stu-id="01348-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="01348-135">Informace o nastavení správy kreditu odběratelů</span><span class="sxs-lookup"><span data-stu-id="01348-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="01348-136">Přidání informací o správě kreditu pro zákazníka</span><span class="sxs-lookup"><span data-stu-id="01348-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="01348-137">Úvěrové skupiny zákazníka</span><span class="sxs-lookup"><span data-stu-id="01348-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="01348-138">Úpravy úvěrového limitu odběratele</span><span class="sxs-lookup"><span data-stu-id="01348-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="01348-139">Blokování úvěru pro prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="01348-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="01348-140">Periodické úkoly správy úvěru odběratelů</span><span class="sxs-lookup"><span data-stu-id="01348-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)

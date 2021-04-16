---
title: Přehled kreditu a inkas
description: V tomto tématu je uveden přehled funkcí pro kredit a inkaso.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7929150cd9f6c28620f4c4d4cb7b57b02d27a104
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835405"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="09b71-103">Přehled kreditu a inkas</span><span class="sxs-lookup"><span data-stu-id="09b71-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09b71-104">Můžete spravovat úvěrový limit pro vaše zákazníky a provádět Inkasní aktivity, když se stanou nezbytnými.</span><span class="sxs-lookup"><span data-stu-id="09b71-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="09b71-105">Správa úvěrů</span><span class="sxs-lookup"><span data-stu-id="09b71-105">Credit management</span></span>

<span data-ttu-id="09b71-106">Správa úvěru odběratele vám umožňuje spravovat limity úvěru a řídit tok prodejních objednávek prostřednictvím procesu zaúčtování na základě pravidel úvěru, která vytvoříte.</span><span class="sxs-lookup"><span data-stu-id="09b71-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="09b71-107">Proces správy úvěru může zahrnovat libovolné z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="09b71-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="09b71-108">Aktualizaci atributů úvěru pro odběratele, které poskytují dodatečné informace o jejich úvěrové způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="09b71-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="09b71-109">Vytvoření limitů úvěru pro odběratele pomocí úprav limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="09b71-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="09b71-110">Vytvoření dočasných limitů úvěru pro odběratele pomocí úprav limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="09b71-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="09b71-111">Tímto způsobem můžete dočasně zvýšit nebo snížit úvěrové limity odběratelů na základě obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="09b71-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="09b71-112">Přidání dalších informací, které mohou ovlivnit limit úvěru, jako jsou informace o pojištění a zárukách.</span><span class="sxs-lookup"><span data-stu-id="09b71-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="09b71-113">Vytvoření skupin úvěrů odběratelů, které propojují odběratele, takže mohou sdílet jeden limit úvěru.</span><span class="sxs-lookup"><span data-stu-id="09b71-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="09b71-114">Přiřazení hodnocení rizik k odběratelům a následné použití těchto hodnocení k automatickému generování limitů úvěrů pro odběratele pomocí úprav limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="09b71-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="09b71-115">Vytvoření pravidel blokování, která blokují objednávku v jednom nebo více procesech zaúčtování na základě faktorů, jako jsou například rizika, platební podmínky, limity úvěrů, částky po splatnosti a použitá procentní hodnota limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="09b71-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="09b71-116">Správu seznamu prodejních objednávek, které jsou blokovány, kontolu důvodů blokování a zmírňování problémů.</span><span class="sxs-lookup"><span data-stu-id="09b71-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="09b71-117">Uvolnění prodejních objednávek, aby mohly pokračovat v procesu zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="09b71-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="09b71-118">Nastavení workflow pro správu schválení změn limitu úvěru a uvolnění prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="09b71-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="09b71-119">Správa inkasa</span><span class="sxs-lookup"><span data-stu-id="09b71-119">Collections management</span></span>

<span data-ttu-id="09b71-120">Stránka **Inkasa** poskytuje jedno ústřední zobrazení, kde jsou spravovány informace o inkasech pohledávek.</span><span class="sxs-lookup"><span data-stu-id="09b71-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="09b71-121">Vedoucí inkasa mohou používat toto centrálizované zobrazení ke správě inkas.</span><span class="sxs-lookup"><span data-stu-id="09b71-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="09b71-122">Inkasní agenti mohou zahájit proces kolekce ze seznamů odběratelů, které jsou generovány pomocí použitím předem definované kolekce kritérií nebo stránky **Odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="09b71-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="09b71-123">Dříve než začnete s nastavením nebo práci s inkasem, měli byste se seznámit s následujícími koncepty:</span><span class="sxs-lookup"><span data-stu-id="09b71-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="09b71-124">Snímky pro sledování splatnosti odběratele obsahují informace o splatném zůstatku v určitém okamžiku.</span><span class="sxs-lookup"><span data-stu-id="09b71-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="09b71-125">Fondy zákazníků kolekce pomáhají v uspořádání vaší práce.</span><span class="sxs-lookup"><span data-stu-id="09b71-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="09b71-126">Inkasní agenti mohou mít své vlastní fondy zákazníků.</span><span class="sxs-lookup"><span data-stu-id="09b71-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="09b71-127">Stránky seznamů umožňují uspořádat odběratele inkasa, aktivity a případy.</span><span class="sxs-lookup"><span data-stu-id="09b71-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="09b71-128">Všechny informace o inkasu odběratele jsou na jedné stránku, která umožňuje provádět další akce.</span><span class="sxs-lookup"><span data-stu-id="09b71-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="09b71-129">Odpuštění, obnovení nebo stornování úroků a poplatků je možné provést v jednom kroku.</span><span class="sxs-lookup"><span data-stu-id="09b71-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="09b71-130">Vytvoření transakcí odpisů je možné provést v jednom kroku.</span><span class="sxs-lookup"><span data-stu-id="09b71-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="09b71-131">Zpracování plateb s nedostatečnými finančními prostředky je možné provést v jednom kroku.</span><span class="sxs-lookup"><span data-stu-id="09b71-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="09b71-132">Popis těchto pojmů naleznete v tématu [Koncepty správy inkasa](./cm-collections-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="09b71-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09b71-133">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="09b71-133">Additional resources</span></span>

[<span data-ttu-id="09b71-134">Nastavení parametrů správy úvěru odběratelů</span><span class="sxs-lookup"><span data-stu-id="09b71-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="09b71-135">Informace o nastavení správy kreditu odběratelů</span><span class="sxs-lookup"><span data-stu-id="09b71-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="09b71-136">Přidání informací o správě kreditu pro zákazníka</span><span class="sxs-lookup"><span data-stu-id="09b71-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="09b71-137">Úvěrové skupiny odběratele</span><span class="sxs-lookup"><span data-stu-id="09b71-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="09b71-138">Úpravy úvěrového limitu odběratele</span><span class="sxs-lookup"><span data-stu-id="09b71-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="09b71-139">Blokování úvěru pro prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="09b71-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="09b71-140">Periodické úkoly správy úvěru odběratelů</span><span class="sxs-lookup"><span data-stu-id="09b71-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
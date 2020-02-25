---
title: Správa úvěru odběratele
description: ''
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
ms.openlocfilehash: 11da8b7fb59bc8f3e2568ada27db753cc815b9c2
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015143"
---
# <a name="customer-credit-management-overview"></a><span data-ttu-id="3cdc7-102">Přehled správy úvěru odběratele</span><span class="sxs-lookup"><span data-stu-id="3cdc7-102">Customer credit management overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3cdc7-103">Správa úvěru odběratele vám umožňuje spravovat limity úvěru a řídit tok prodejních objednávek prostřednictvím procesu zaúčtování na základě pravidel úvěru, která vytvoříte.</span><span class="sxs-lookup"><span data-stu-id="3cdc7-103">Customer credit management allows you to manage credit limits and control the flow of sales orders through the posting process based on credit rules that you create.</span></span> 

<span data-ttu-id="3cdc7-104">Proces pro použití správy úvěru může zahrnovat některé z následujících kroků nebo všechny tyto kroky:</span><span class="sxs-lookup"><span data-stu-id="3cdc7-104">The process for using credit management can include some or all of the following steps:</span></span>
- <span data-ttu-id="3cdc7-105">Aktualizaci odběratelů pomocí atributů úvěru, které poskytují dodatečné informace o jejich úvěrové způsobilosti</span><span class="sxs-lookup"><span data-stu-id="3cdc7-105">Update customers with credit attributes that provide additional information about their credit worthiness</span></span> 
- <span data-ttu-id="3cdc7-106">Vytvoření limitů úvěru pro odběratele pomocí úprav limitu úvěru</span><span class="sxs-lookup"><span data-stu-id="3cdc7-106">Create credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="3cdc7-107">Vytvoření dočasných limitů úvěru pro odběratele pomocí úprav limitu úvěru, chcete-li dočasně zvýšit nebo snížit jejich limit úvěru na základě potřeb podniku</span><span class="sxs-lookup"><span data-stu-id="3cdc7-107">Create temporary credit limits for customers using credit limit adjustments when you want to increase or decrease their credit limit temporarily based on business needs</span></span>
- <span data-ttu-id="3cdc7-108">Přidání dalších informací, které mohou ovlivnit limit úvěru, jako je například pojištění a záruky</span><span class="sxs-lookup"><span data-stu-id="3cdc7-108">Add additional information that can affect the credit limit such as insurance and guarantees</span></span>
- <span data-ttu-id="3cdc7-109">Vytvoření skupin odběratelů podle limitu úvěru, které propojují odběratele, takže mohou sdílet jeden limit úvěru</span><span class="sxs-lookup"><span data-stu-id="3cdc7-109">Create customer credit groups that link customers together so they can share a single credit limit</span></span>
- <span data-ttu-id="3cdc7-110">Přiřazení hodnocení rizik k odběratelům a následné použití těchto hodnocení k automatickému generování limitů úvěrů pro odběratele pomocí úprav limitu úvěru</span><span class="sxs-lookup"><span data-stu-id="3cdc7-110">Assign risk scores to customers and then use those scores to automatically generate credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="3cdc7-111">Vytvoření pravidel blokování, která budou blokovat objednávku v jednom nebo více procesech zaúčtování na základě faktorů, jako jsou například rizika, platební podmínky, limity úvěrů, částky po splatnosti a použitá procentní hodnota limitu úvěru</span><span class="sxs-lookup"><span data-stu-id="3cdc7-111">Create blocking rules that will place an order on hold during one or more posting processes based on factors such as risk, payment terms, credit limits, overdue amounts, and percentage of credit limit used</span></span>
- <span data-ttu-id="3cdc7-112">Správu seznamu prodejních objednávek, které jsou blokovány, kontolu důvodů blokování a zmírňování problémů</span><span class="sxs-lookup"><span data-stu-id="3cdc7-112">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate the issues</span></span>
- <span data-ttu-id="3cdc7-113">Uvolnění prodejních objednávek a umožnění jejich pokračování v procesu zaúčtování</span><span class="sxs-lookup"><span data-stu-id="3cdc7-113">Release sales orders and allow it to continue through the posting process</span></span>
- <span data-ttu-id="3cdc7-114">Nastavení workflow pro správu schválení změn limitu úvěru a uvolnění prodejních objednávek</span><span class="sxs-lookup"><span data-stu-id="3cdc7-114">Set up workflow to manage the approval of credit limit changes and sales order releases</span></span>


<a name="additional-resources"></a><span data-ttu-id="3cdc7-115">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3cdc7-115">Additional resources</span></span>
--------
[<span data-ttu-id="3cdc7-116">Nastavení parametrů správy úvěru odběratelů</span><span class="sxs-lookup"><span data-stu-id="3cdc7-116">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="3cdc7-117">Informace o nastavení správy kreditu odběratelů</span><span class="sxs-lookup"><span data-stu-id="3cdc7-117">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="3cdc7-118">Přidání informací o správě kreditu pro zákazníka</span><span class="sxs-lookup"><span data-stu-id="3cdc7-118">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="3cdc7-119">Úvěrové skupiny odběratele</span><span class="sxs-lookup"><span data-stu-id="3cdc7-119">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="3cdc7-120">Úpravy úvěrového limitu odběratele</span><span class="sxs-lookup"><span data-stu-id="3cdc7-120">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="3cdc7-121">Blokování úvěru pro prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="3cdc7-121">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="3cdc7-122">Periodické úkoly správy úvěru odběratelů</span><span class="sxs-lookup"><span data-stu-id="3cdc7-122">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)



---
title: Přehled workflowu odběru
description: Toto téma poskytuje přehled workflowu předplatného.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f023ddd8d6f9350702f687763b53b057baa9aed8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423765"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="3908f-103">Přehled workflowu odběru</span><span class="sxs-lookup"><span data-stu-id="3908f-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3908f-104">Pracujete jako správce předplatného pro společnost pronajímající osvětlovací techniku a že vaše společnost nabízí předplatné pro údržbu osvětlovacích techniky.</span><span class="sxs-lookup"><span data-stu-id="3908f-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="3908f-105">Zákazník kontaktuje vaši společnost s cílem zakoupit roční předplatné zahrnující údržbu systému osvětlení.</span><span class="sxs-lookup"><span data-stu-id="3908f-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="3908f-106">Nastavení předplatného</span><span class="sxs-lookup"><span data-stu-id="3908f-106">Setting up subscriptions</span></span>

<span data-ttu-id="3908f-107">Při nastavení předplatného musíte nejprve vytvořit skupinu předplatného pro novou servisní smlouvu nebo ověření existence skupiny předplatného.</span><span class="sxs-lookup"><span data-stu-id="3908f-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="3908f-108">Pokud skupina ověření předplatného existuje, musí pro ni být nastavena frekvence ročního fakturování odběratele a musí umožňovat časové rozlišení prodejního zisku pro každý měsíc v roce.</span><span class="sxs-lookup"><span data-stu-id="3908f-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="3908f-109">Další informace o postupu při nastavení předplatných získáte v tématu [Nastavení skupin předplatného](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="3908f-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="3908f-110">Po vytvoření skupiny předplatného můžete vytvořit předplatné.</span><span class="sxs-lookup"><span data-stu-id="3908f-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="3908f-111">Další informace o vytvoření předplatného servisu naleznete v tématu [Vytvoření předplatného servisu ze skupiny předplatného ](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="3908f-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="3908f-112">Vytvoření a úprava transakcí předplatného</span><span class="sxs-lookup"><span data-stu-id="3908f-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="3908f-113">Po nastavení předplatného vytvoříte transakci poplatku předplatného pro první fakturační období, což je jeden rok.</span><span class="sxs-lookup"><span data-stu-id="3908f-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="3908f-114">Transakce jsou typu **Běžné**.</span><span class="sxs-lookup"><span data-stu-id="3908f-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="3908f-115">To znamená, že lze vytvořit pouze transakce předplatného, u nichž hodnoty Od data a Do data odpovídají existujícím obdobím vytvořeným ve formuláři **Typy období**.</span><span class="sxs-lookup"><span data-stu-id="3908f-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="3908f-116">Další informace o transakcích poplatků naleznete v tématu [Vytvoření transakcí poplatků předplatného](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="3908f-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="3908f-117">Po nastavení předplatného pro určitého odběratele si vzpomenete, že tento odběratel si s vámi dojednal slevu ve výši 10 procent na všechny ceny z ceníku nabízených služeb.</span><span class="sxs-lookup"><span data-stu-id="3908f-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="3908f-118">Z tohoto důvodu budete muset snížit vytvořenou cenu poplatku transakce.</span><span class="sxs-lookup"><span data-stu-id="3908f-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="3908f-119">Později ve stejný den se s vámi telefonicky spojí kontaktní osoba zákazníka a sdělí vám, že nadále požadují servisní smlouvu pro systém osvětlení, avšak že později v průběhu roku plánují instalaci nového systému osvětlení.</span><span class="sxs-lookup"><span data-stu-id="3908f-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="3908f-120">Z tohoto důvodu je požadován rozsah smlouvy jen do října 2013.</span><span class="sxs-lookup"><span data-stu-id="3908f-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="3908f-121">S cílem snížení počtu měsíců pro předplatné zákazníka vytvoříte novou transakci poplatku předplatného typu **Dny omezení**.</span><span class="sxs-lookup"><span data-stu-id="3908f-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="3908f-122">Další informace o tom, jak snížit počet dní, lze najít v tématu [snížení počtu dnů u poplatků za odběr](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="3908f-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="3908f-123">Fakturace a časové rozlišení pro transakce předplatného</span><span class="sxs-lookup"><span data-stu-id="3908f-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="3908f-124">Nyní jste dokončili nastavení předplatného a jste připraveni na fakturaci předplatného pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="3908f-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="3908f-125">Další informace o postupu při fakturaci předplatných získáte v tématu [Fakturace skupin předplatného](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="3908f-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="3908f-126">O dva dny později se s vámi odběratel spojí telefonicky a požaduje, aby předplatné bylo fakturováno v amerických dolarech, a nikoli v eurech.</span><span class="sxs-lookup"><span data-stu-id="3908f-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="3908f-127">Proto vytvoříte dobropis a poté vytvoříte novou transakci předplatného ve správné měně.</span><span class="sxs-lookup"><span data-stu-id="3908f-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="3908f-128">Další informace o postupu při úvěrování předplatných transakcí získáte v tématu [Fakturace skupin předplatného](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="3908f-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="3908f-129">Na konci každého měsíce připíšete časově rozlišené výnosy z předplatného odběratele na účet zisků a ztrát a na účty WIP.</span><span class="sxs-lookup"><span data-stu-id="3908f-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="3908f-130">Další informace o postupu při časovém rozlišení pro předplatné získáte v části [časově rozlišené výnosy předplatného](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="3908f-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  



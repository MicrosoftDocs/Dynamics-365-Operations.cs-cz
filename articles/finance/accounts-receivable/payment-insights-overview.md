---
title: Přehledy plateb odběratele (Preview)
description: Toto téma popisuje funkci přehledů plateb, která pomáhá lépe porozumět typickým platebním praktikám jednotlivých zákazníků. Tato funkce vám pomůže identifikovat okolnosti, které ospravedlňují zahájení procesu inkasa dříve, než byste to udělali v ostatních případech.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f151942555ac503338f0fd44aa8779e3c2970fb1
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644626"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="f2015-104">Přehledy plateb odběratele (Preview)</span><span class="sxs-lookup"><span data-stu-id="f2015-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f2015-105">Toto téma popisuje funkci přehledů plateb, která pomáhá lépe porozumět typickým platebním praktikám jednotlivých zákazníků.</span><span class="sxs-lookup"><span data-stu-id="f2015-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="f2015-106">Tato funkce vám pomůže identifikovat okolnosti, které ospravedlňují zahájení procesu inkasa dříve, než byste to udělali v ostatních případech.</span><span class="sxs-lookup"><span data-stu-id="f2015-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="f2015-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="f2015-107">Overview</span></span>

<span data-ttu-id="f2015-108">Předvídat, kdy zákazník zaplatí faktury, může být náročné.</span><span class="sxs-lookup"><span data-stu-id="f2015-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="f2015-109">Tento nedostatek přehledu vede k méně přesným prognózám toku hotovosti, procesům inkasa, které začínají příliš pozdě, a objednávek, které jsou vydány odběratelům, kteří mohou mít pro platbu výchozí nastavení.</span><span class="sxs-lookup"><span data-stu-id="f2015-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="f2015-110">Přehledy plateb zákazníka (preview) pomáhá organizacím předpovědět, kdy dojde k zaplacení faktury zákazníkem.</span><span class="sxs-lookup"><span data-stu-id="f2015-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="f2015-111">Tyto informace mohou organizacím pomoci vytvořit strategie inkasa, které zvyšují pravděpodobnost včasného zaplacení.</span><span class="sxs-lookup"><span data-stu-id="f2015-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="f2015-112">Předpovědi</span><span class="sxs-lookup"><span data-stu-id="f2015-112">Predictions</span></span>

<span data-ttu-id="f2015-113">Předpovědi plateb umožní organizacím zlepšovat své obchodní procesy tím, že jim usnadní snadnou identifikaci faktur, které by mohly být placeny pozdě, a přijme vhodná opatření, která zlepšují jejich šanci zaplacení včas.</span><span class="sxs-lookup"><span data-stu-id="f2015-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="f2015-114">Pomocí modelu strojového učení, který vyplní historické faktury, platby a data odběratele, aplikace Přehledy plateb odběratelů (Preview) přesnější předpovídá, kdy odběratel zaplatí nevyřízenou fakturu.</span><span class="sxs-lookup"><span data-stu-id="f2015-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="f2015-115">Pro každou otevřenou fakturu mohou Přehledy plateb zákazníka (Preview) předpovědět tři pravděpodobnosti platby:</span><span class="sxs-lookup"><span data-stu-id="f2015-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="f2015-116">Pravděpodobnost platby včas</span><span class="sxs-lookup"><span data-stu-id="f2015-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="f2015-117">Pravděpodobnost platby se zpožděním</span><span class="sxs-lookup"><span data-stu-id="f2015-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="f2015-118">Pravděpodobnost platby s velkým zpožděním</span><span class="sxs-lookup"><span data-stu-id="f2015-118">Probability of payment being made very late</span></span>

<span data-ttu-id="f2015-119">Aplikace Přehledy plateb odběratelů (Preview) také poskytuje agregované zobrazení očekávaných plateb, což může pomoci organizacím pochopit celkovou částku platby, kterou mohou očekávat od zákazníka v jednom ze tří intervalů, včas, se zpožděním a s velkým zpožděním.</span><span class="sxs-lookup"><span data-stu-id="f2015-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="f2015-120">[![Agregované zobrazení předpovědí platby](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="f2015-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="f2015-121">Každá faktura má také přiřazenou pravděpodobnost platby včas.</span><span class="sxs-lookup"><span data-stu-id="f2015-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="f2015-122">Je-li pravděpodobnost platby v čase nižší než 50 %, budou faktury označeny červeným kroužkem, což znamená, že tyto faktury mohou vyžadovat pozornost inkasa.</span><span class="sxs-lookup"><span data-stu-id="f2015-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="f2015-123">[![Seznam pravděpodobností platby](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="f2015-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="f2015-124">Aplikace Customer Payment Insights (Preview) také poskytuje kontextové informace vysvětlující předpověď, jako jsou například nejvyšší faktory ovlivňující předpovědi, aktuální stav obchodu se zákazníkem a podrobnosti historickém chování platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="f2015-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="f2015-125">V mnoha společnostech byl proces inkasa reaktivní aktivitou; což znamená, že nebyl zahájen, dokud nebyly faktury splatné.</span><span class="sxs-lookup"><span data-stu-id="f2015-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="f2015-126">S nástupem aplikace Přehledy plateb zákazníka (Preview) mohou být organizace aktivnější v oblasti inkas.</span><span class="sxs-lookup"><span data-stu-id="f2015-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="f2015-127">Již nemusí čekat na to, aby transakce byly splatné, aby mohl být zahájen proces inkasa.</span><span class="sxs-lookup"><span data-stu-id="f2015-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="f2015-128">Namísto toho mohou pomocí možnosti předpovědi plateb určit, zda provedená aktivní inkasa zvýší pravděpodobnost platby včas.</span><span class="sxs-lookup"><span data-stu-id="f2015-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="f2015-129">Předpověď platby také poskytuje podnikům informace potřebné k tomu, aby byl proces inkasa zahájen včas.</span><span class="sxs-lookup"><span data-stu-id="f2015-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="f2015-130">Metodologie</span><span class="sxs-lookup"><span data-stu-id="f2015-130">Methodology</span></span>

<span data-ttu-id="f2015-131">Vývoj a nasazení řešení AI je tvrdý.</span><span class="sxs-lookup"><span data-stu-id="f2015-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="f2015-132">Vyžaduje tým datových vědců, odborníků na dané záležitosti a techniků, kteří pracují dlouhou dobu na formulování, vývoji, nasazení a udržování použitelného řešení AI.</span><span class="sxs-lookup"><span data-stu-id="f2015-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="f2015-133">Usnadňujeme nasazení a používání řešení AI v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="f2015-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="f2015-134">V modulu Finance připravujeme řešení vybudovaná na aplikaci Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="f2015-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="f2015-135">Koncový uživatel jediným kliknutím na tlačítko může nasadit řešení AI a začít využívat výhod inteligentních předpovědi.</span><span class="sxs-lookup"><span data-stu-id="f2015-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="f2015-136">Není-li organizace spokojená s přesností předpovědi, může uživatel power user znovu jedním kliknutím spustit prostředí rozšíření aplikace AI builder a poté vybrat nebo zrušit výběr polí používaných k vygenerování předpovědi.</span><span class="sxs-lookup"><span data-stu-id="f2015-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="f2015-137">Jakmile je to možné, mohou tyto změny vyzkoušet a publikovat a nově osvojený model bude automaticky vybrán pro předpovědi v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="f2015-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="f2015-138">Jak získat Přehledy plateb zákazníka (Preview)</span><span class="sxs-lookup"><span data-stu-id="f2015-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="f2015-139">Pokud chcete vyzkoušet Přehledy plateb zákazníka (Preview), pošlete e-mail týmu [Přehledy plateb zákazníka (Preview)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="f2015-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="f2015-140">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="f2015-140">Privacy Notice</span></span>

<span data-ttu-id="f2015-141">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="f2015-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>



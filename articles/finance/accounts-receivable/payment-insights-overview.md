---
title: Přehledy plateb odběratele (Preview)
description: V tomto tématu je popsána funkce platebních přehledů, která pomáhá zlepšit pochopení typických způsobů plateb jednotlivých odběratelů a může identifikovat okolnosti, které opravňují ke spouštění procesů inkasa dříve, než jste provedli jiné operace.
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
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773914"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="e9ecc-103">Přehledy plateb odběratele (Preview)</span><span class="sxs-lookup"><span data-stu-id="e9ecc-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e9ecc-104">V tomto tématu je popsána funkce platebních přehledů, která pomáhá zlepšit pochopení typických způsobů plateb jednotlivých odběratelů a může identifikovat okolnosti, které opravňují ke spouštění procesů inkasa dříve, než je možné provést jiné operace.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="e9ecc-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="e9ecc-105">Overview</span></span>

<span data-ttu-id="e9ecc-106">Organizace často považují za náročné předvídat, kdy zákazník zaplatí faktury.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="e9ecc-107">Tento nedostatek přehledu vede k méně přesným prognózám toku hotovosti, procesům inkasa, které začínají příliš pozdě, a objednávek, které jsou vydány odběratelům, kteří mohou mít pro platbu výchozí nastavení.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="e9ecc-108">Toto téma popisuje, jak přehledy plateb (Preview) pomáhají organizacím předpovídat, kdy bude faktura zákazníka zaplacena, což pomáhá organizacím vytvořit strategie optimalizace, které zlepší pravděpodobnost včasného zaplacení.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="e9ecc-109">Předpovědi</span><span class="sxs-lookup"><span data-stu-id="e9ecc-109">Predictions</span></span>

<span data-ttu-id="e9ecc-110">Předpovědi plateb umožní organizacím zlepšovat své obchodní procesy tím, že jim usnadní snadnou identifikaci faktur, které by mohly být placeny pozdě, a přijme vhodná opatření, která zlepšují jejich šanci zaplacení včas.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="e9ecc-111">Pomocí modelu strojového učení, který vyplní historické faktury, platby a data odběratele, aplikace Přehledy plateb odběratelů (Preview) přesnější předpovídá, kdy odběratel zaplatí nevyřízenou fakturu.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="e9ecc-112">Pro každou otevřenou fakturu předpovídají Přehledy plateb zákazníka (Preview) tři pravděpodobnosti platby:</span><span class="sxs-lookup"><span data-stu-id="e9ecc-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="e9ecc-113">Pravděpodobnost platby včas</span><span class="sxs-lookup"><span data-stu-id="e9ecc-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="e9ecc-114">Pravděpodobnost platby se zpožděním</span><span class="sxs-lookup"><span data-stu-id="e9ecc-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="e9ecc-115">Pravděpodobnost platby s velkým zpožděním</span><span class="sxs-lookup"><span data-stu-id="e9ecc-115">Probability of payment being made very late</span></span>

<span data-ttu-id="e9ecc-116">Chcete-li pomoci organizacím pochopit celkovou částku platby, kterou mohou očekávat od zákazníka v jednom ze tří intervalů, včas, se zpožděním a s velkým zpožděním, poskytuje aplikace Přehledy plateb odběratelů (Preview) také agregované zobrazení očekávaných plateb.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="e9ecc-117">[![Agregované zobrazení předpovědí platby](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="e9ecc-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="e9ecc-118">Každá faktura má také přiřazenou pravděpodobnost platby včas.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="e9ecc-119">Je-li pravděpodobnost platby v čase nižší než 50 %, budou faktury označeny červeným kroužkem, což znamená, že tyto faktury mohou vyžadovat pozornost inkasa.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="e9ecc-120">[![Seznam pravděpodobností platby](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="e9ecc-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="e9ecc-121">Aplikace Customer Payment Insights (Preview) také poskytuje kontextové informace vysvětlující předpověď, jako jsou například nejvyšší faktory ovlivňující předpovědi, aktuální stav obchodu se zákazníkem a podrobnosti historickém chování platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="e9ecc-122">V mnoha společnostech byl proces inkasa reaktivní aktivitou; což znamená, že nebyl zahájen, dokud nebyly faktury splatné.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="e9ecc-123">S nástupem aplikace Přehledy plateb zákazníka (Preview) mohou být organizace aktivnější v oblasti inkas.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="e9ecc-124">Již nemusí čekat na to, aby transakce byly splatné, aby mohl být zahájen proces inkasa.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="e9ecc-125">Namísto toho mohou pomocí možnosti předpovědi plateb určit, zda provedená aktivní inkasa zvýší pravděpodobnost platby včas.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="e9ecc-126">Předpověď platby také poskytuje podnikům informace potřebné k tomu, aby byl proces inkasa zahájen včas.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="e9ecc-127">Metodologie</span><span class="sxs-lookup"><span data-stu-id="e9ecc-127">Methodology</span></span>

<span data-ttu-id="e9ecc-128">Vývoj a nasazení řešení AI je tvrdý.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="e9ecc-129">Vyžaduje tým datových vědců, odborníků na dané záležitosti a techniků, kteří pracují dlouhou dobu na formulování, vývoji, nasazení a udržování použitelného řešení AI.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="e9ecc-130">Usnadňujeme nasazení a používání řešení AI v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="e9ecc-131">V modulu Finance připravujeme řešení vybudovaná na aplikaci Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="e9ecc-132">Koncový uživatel jediným kliknutím na tlačítko může nasadit řešení AI a začít využívat výhod inteligentních předpovědi.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="e9ecc-133">Není-li organizace spokojená s přesností předpovědi, může uživatel power user znovu jedním kliknutím spustit prostředí rozšíření aplikace AI builder a poté vybrat nebo zrušit výběr polí používaných k vygenerování předpovědi.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="e9ecc-134">Jakmile je to možné, mohou tyto změny vyzkoušet a publikovat a nově osvojený model bude automaticky vybrán pro předpovědi v modulu Finance.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="e9ecc-135">Jak získat Přehledy plateb zákazníka (Preview)</span><span class="sxs-lookup"><span data-stu-id="e9ecc-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="e9ecc-136">Pokud chcete vyzkoušet Přehledy plateb zákazníka (Preview), pošlete e-mail týmu [Přehledy plateb zákazníka (Preview)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e9ecc-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="e9ecc-137">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="e9ecc-137">Privacy Notice</span></span>

<span data-ttu-id="e9ecc-138">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="e9ecc-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>



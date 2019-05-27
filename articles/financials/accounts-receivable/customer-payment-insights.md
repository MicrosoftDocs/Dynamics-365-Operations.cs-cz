---
title: Přehledy plateb zákazníka (preview)
description: Toto téma popisuje, jak přehledy plateb zákazníka mohou pomoci předpovídat, kdy bude faktura zaplacena, a rovněž pomoci organizacím vytvořit strategie optimalizace, které zlepší pravděpodobnost včasného zaplacení.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566229"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="bbaf7-103">Přehledy plateb zákazníka (preview)</span><span class="sxs-lookup"><span data-stu-id="bbaf7-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="bbaf7-104">Tato funkce je součástí cíleného vydání a je k dispozici pouze pro uživatele, kteří se rozhodli pro soukromé verze Preview.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="bbaf7-105">Tato funkce bude zahrnuta v nadcházejícím vydání všeobecné dostupnosti.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="bbaf7-106">Přehled</span><span class="sxs-lookup"><span data-stu-id="bbaf7-106">Overview</span></span>

<span data-ttu-id="bbaf7-107">Organizace často považují za náročné předvídat, kdy zákazník zaplatí faktury.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="bbaf7-108">Tento nedostatek přehledu může vést k nepřesným prognózám cashflow, neefektivním procesům výběru a možnosti uvolnění objednávek zákazníkům, kteří mohou představovat úvěrové riziko.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="bbaf7-109">Přehledy plateb zákazníka (preview) používají strojové učení pro předpovídání zaplacení faktury.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="bbaf7-110">Poskytuje také optimalizační strategie, které mohou být přizpůsobeny tak, aby maximalizovaly pravděpodobnost, že zákazníci budou platit včas.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="bbaf7-111">Předpovědi</span><span class="sxs-lookup"><span data-stu-id="bbaf7-111">Predictions</span></span>

<span data-ttu-id="bbaf7-112">Předpovědi plateb umožňují organizacím zlepšit své obchodní procesy tím, že pomáhají:</span><span class="sxs-lookup"><span data-stu-id="bbaf7-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="bbaf7-113">Snadno identifikovat faktury, u kterých se dá očekávat opožděné zaplacení.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="bbaf7-114">Provést příslušná opatření ke zlepšení šancí získat platbu včas.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="bbaf7-115">Přehledy plateb zákazníka (preview) používají strojové učení pro předpovídání zaplacení faktury.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="bbaf7-116">Využívá historických faktur, plateb a údajů o zákaznících k vytvoření modelu strojového učení, který slouží k předvídání, kdy bude zaplacena faktura.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="bbaf7-117">Pro každou otevřenou fakturu předpovídají Přehledy plateb zákazníka (preview) tři pravděpodobnosti platby:</span><span class="sxs-lookup"><span data-stu-id="bbaf7-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="bbaf7-118">Pravděpodobnost včasné platby (v rámci data splatnosti faktury).</span><span class="sxs-lookup"><span data-stu-id="bbaf7-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="bbaf7-119">Pravděpodobnost platby do 30 dnů v rámci data splatnosti faktury.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="bbaf7-120">Pravděpodobnost platby po 30 dnech po datu splatnosti faktury.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="bbaf7-121">Pravděpodobnost platby můžete zobrazit v oddílu předpovědi.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="bbaf7-122">[![Předpovědi platby](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="bbaf7-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="bbaf7-123">Každé faktuře je rovněž přiřazena vítězná pravděpodobnost platby pomocí jednoho ze tří scénářů pravděpodobností plateb definovaných výše.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="bbaf7-124">Scénář s nejvyšší pravděpodobnost platby je vítězný scénář.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="bbaf7-125">Předpokládejme například, že předpověď pro fakturu ukazuje 71% pravděpodobnost, že faktura bude zaplacena včas, 13% pravděpodobnost, že faktura bude zaplacena do 30 dnů od data splatnosti a 16% pravděpodobnost, že faktura bude zaplacena po 30 dnech splatnosti.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="bbaf7-126">Nejvyšší pravděpodobnost ukazuje, že faktura bude ve včasném scénáři, takže faktura bude označena pravděpodobností, že bude zaplacena včas</span><span class="sxs-lookup"><span data-stu-id="bbaf7-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="bbaf7-127">[![Předpovědi platby](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="bbaf7-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="bbaf7-128">Strategie optimalizace</span><span class="sxs-lookup"><span data-stu-id="bbaf7-128">Optimization strategies</span></span>

<span data-ttu-id="bbaf7-129">Kromě předpovědí plateb mohou Přehledy plateb zákazníka (preview) využívat optimalizační strategie ke zlepšení šancí na včasné zaplacení.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="bbaf7-130">To umožňuje organizacím provádět analýzu „Co když“ tím, že umožňuje uživatelům přizpůsobit fakturu a parametry zákazníků, a pak porovnat odpovídající vliv na pravděpodobnost, že bude platba faktur přijata včas.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="bbaf7-131">Například organizace může chtít vyhodnotit účinek aktualizace hotovostní slevy na faktury na pravděpodobnost, že bude platba přijata včas.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="bbaf7-132">Když jsou faktury optimalizovány pro použití nové slevy, uživatelé mohou posoudit účinek uplatnění slevy na pravděpodobnost, že budou tyto faktury zaplaceny včas.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="bbaf7-133">Pokud jsou náklady na uplatnění slevy minimální ve srovnání s výhodou včasného získání platby, organizace se může rozhodnout použít vybranou slevu na všechny budoucí otevřené objednávky.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="bbaf7-134">V současné době je k dispozici pouze sleva jako optimalizační strategie pro Přehledy plateb zákazníka (preview).</span><span class="sxs-lookup"><span data-stu-id="bbaf7-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="bbaf7-135">[![Optimalizované předpovědi](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="bbaf7-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="bbaf7-136">Jak získat Přehledy plateb zákazníka (preview)</span><span class="sxs-lookup"><span data-stu-id="bbaf7-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="bbaf7-137">Pokud chcete vyzkoušet Přehledy plateb zákazníka (preview), pošlete e-mail týmu [Finanční přehledy - Preview](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="bbaf7-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="bbaf7-138">Prohlášení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="bbaf7-138">Privacy Statement</span></span>

<span data-ttu-id="bbaf7-139">Verze Preview ukládají údaje o zákaznících ve Spojených státech.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="bbaf7-140">Kromě toho verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 for Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="bbaf7-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>

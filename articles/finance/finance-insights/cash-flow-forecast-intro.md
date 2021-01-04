---
title: Prognóza cashflow (Preview)
description: Toto téma popisuje funkci prognózování cashflow.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
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
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f97b8fc0896f0f7b95bf5609f94367b3a8230ca7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645241"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="61586-103">Prognóza cashflow (Preview)</span><span class="sxs-lookup"><span data-stu-id="61586-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="61586-104">Cashflow je pro každé podnikání zásadní.</span><span class="sxs-lookup"><span data-stu-id="61586-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="61586-105">Dokonce i ziskové společnosti mohou čelit platební neschopnosti, pokud neudržují cashflow, aby uspokojily okamžité potřeby.</span><span class="sxs-lookup"><span data-stu-id="61586-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="61586-106">Funkce prognózování cashflow v přehledech Finance může společnostem pomoci efektivně sledovat a spravovat své hotovostní zůstatky.</span><span class="sxs-lookup"><span data-stu-id="61586-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="61586-107">Tato funkce využívá strojové učení, aby pomohla podnikům předpovídat cashflow přesněji než dříve.</span><span class="sxs-lookup"><span data-stu-id="61586-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="61586-108">Může také pomoci manažerům činit rozhodnutí, která optimalizují příležitosti v kontextu jejich aktuální pozice hotovosti.</span><span class="sxs-lookup"><span data-stu-id="61586-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="61586-109">Pro většinu společností je správa cashflow a jejich prognózování zdlouhavým, opakujícím se a ručním procesem.</span><span class="sxs-lookup"><span data-stu-id="61586-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="61586-110">Většina společností se spoléhá na řešení Microsoft Excel, která mají různé stupně složitosti.</span><span class="sxs-lookup"><span data-stu-id="61586-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="61586-111">Mezi výzvy týkající se přesné předpovědi cashflow patří následující:</span><span class="sxs-lookup"><span data-stu-id="61586-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="61586-112">Data nejsou k dispozici osobám s rozhodovací pravomocí, protože jsou rozptýlena na více místech, včetně:</span><span class="sxs-lookup"><span data-stu-id="61586-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="61586-113">Účetní systém nebo systém plánování podnikových zdrojů</span><span class="sxs-lookup"><span data-stu-id="61586-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="61586-114">Software pro finanční plánování</span><span class="sxs-lookup"><span data-stu-id="61586-114">Financial planning software</span></span>
  - <span data-ttu-id="61586-115">Aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="61586-115">Excel</span></span>
  - <span data-ttu-id="61586-116">Další softwarové aplikace</span><span class="sxs-lookup"><span data-stu-id="61586-116">Additional software applications</span></span> 
- <span data-ttu-id="61586-117">Prognózy jsou založeny na interních znalostních bázích, které se nacházejí v „silech“ v každé doméně nebo oddělení.</span><span class="sxs-lookup"><span data-stu-id="61586-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="61586-118">Měření přesnosti prognózování cashflow po uplatnění financí je nejisté a obtížné.</span><span class="sxs-lookup"><span data-stu-id="61586-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="61586-119">Podrobnosti o funkci prognózování cashflow</span><span class="sxs-lookup"><span data-stu-id="61586-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="61586-120">Funkce prognózování cashflow zahrnuje následující funkce.</span><span class="sxs-lookup"><span data-stu-id="61586-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="61586-121">Usnadňuje integraci dat cashflow z externích systémů do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="61586-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="61586-122">Prognózy cashflow mohou také využívat rámec importu a exportu dat.</span><span class="sxs-lookup"><span data-stu-id="61586-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="61586-123">Tento rámec usnadňuje integraci s Excel OData.</span><span class="sxs-lookup"><span data-stu-id="61586-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="61586-124">Můžete také kombinovat data z více zdrojů a vytvořit komplexní řešení cashflow.</span><span class="sxs-lookup"><span data-stu-id="61586-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="61586-125">Představuje inteligentní pozici hotovosti.</span><span class="sxs-lookup"><span data-stu-id="61586-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="61586-126">Pozice hotovosti se vytváří na základě chování platby zákazníka, aby bylo možné predikovat, kdy může společnost očekávat, že na její účty dorazí hotovost.</span><span class="sxs-lookup"><span data-stu-id="61586-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="61586-127">Analyzuje také historické vzorce platících dodavatelů, aby predikoval, kdy je pravděpodobné, že budou uhrazeny budoucí faktury a objednávky.</span><span class="sxs-lookup"><span data-stu-id="61586-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="61586-128">Představuje inteligentní prognózování cashflow pro dlouhodobé prognózování pomocí časových řad prostřednictvím automatizované integrace s AI Builder.</span><span class="sxs-lookup"><span data-stu-id="61586-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="61586-129">Poskytuje možnost ukládat konkrétní pozice cashflow nebo prognózy, upravovat je a poté snadno porovnávat a měřit výkon prognózy se skutečnými finančními údaji.</span><span class="sxs-lookup"><span data-stu-id="61586-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="61586-130">Umožňuje pravděpodobnostní analýzu prostřednictvím porovnání snímků.</span><span class="sxs-lookup"><span data-stu-id="61586-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="61586-131">Můžete například vytvořit několik snímků, které představují optimistické, pesimistické a nejrealističtější zobrazení cashflow a poté porovnat a zobrazit rozdíly.</span><span class="sxs-lookup"><span data-stu-id="61586-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="61586-132">Poskytuje možnost zobrazit prognózu cashflow ve více měnách, napříč právnickými osobami a filtrovat a zobrazit cashflow související s bankovním účtem.</span><span class="sxs-lookup"><span data-stu-id="61586-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="61586-133">Umožňuje filtrovat a zobrazit bankovní účty, které souvisejí s finančními dimenzemi.</span><span class="sxs-lookup"><span data-stu-id="61586-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="61586-134">Funkce prognózování cashflow v Dynamics 365 Finance umožní vaší organizaci transformovat zdlouhavé, složité a přitom opakující se projekce cashflow na jednoduchý automatizovaný proces.</span><span class="sxs-lookup"><span data-stu-id="61586-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="61586-135">Automatizace nejzdlouhavějších aspektů prognózování cashflow vám umožní soustředit se na kritické rozhodování a dosáhnout požadovaných obchodních výsledků.</span><span class="sxs-lookup"><span data-stu-id="61586-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="61586-136">Nastavení dimenzí pro prognózu cashflow</span><span class="sxs-lookup"><span data-stu-id="61586-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="61586-137">Nová karta na stránce **Nastavení prognózy cashflow** umožňuje řídit, jaké finanční dimenze se mají použít pro filtrování v pracovním prostoru **Prognóza cashflow**.</span><span class="sxs-lookup"><span data-stu-id="61586-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="61586-138">Tato karta se zobrazí, pouze pokud je povolena funkce prognózy cashflow.</span><span class="sxs-lookup"><span data-stu-id="61586-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="61586-139">Na kartě **Dimenze** vyberte ze seznamu dimenze, které se mají použít pro filtrování, a pomocí kláves se šipkami je přesuňte do pravého sloupce.</span><span class="sxs-lookup"><span data-stu-id="61586-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="61586-140">Pro filtrování dat prognózy cashflow lze vybrat pouze dvě dimenze.</span><span class="sxs-lookup"><span data-stu-id="61586-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="61586-141">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="61586-141">Privacy notice</span></span>
<span data-ttu-id="61586-142">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="61586-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>

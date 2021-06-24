---
title: Prognóza cashflow (Preview)
description: Toto téma popisuje funkci prognózování cashflow.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 64935db3b50e7598f2076ecbec72aba020d4f908
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186533"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="94202-103">Prognóza cashflow (Preview)</span><span class="sxs-lookup"><span data-stu-id="94202-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="94202-104">Cashflow je pro každé podnikání zásadní.</span><span class="sxs-lookup"><span data-stu-id="94202-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="94202-105">Dokonce i ziskové společnosti mohou čelit platební neschopnosti, pokud neudržují cashflow, aby uspokojily okamžité potřeby.</span><span class="sxs-lookup"><span data-stu-id="94202-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="94202-106">Funkce prognózování cashflow v přehledech Finance může společnostem pomoci efektivně sledovat a spravovat své hotovostní zůstatky.</span><span class="sxs-lookup"><span data-stu-id="94202-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="94202-107">Tato funkce využívá strojové učení, aby pomohla podnikům předpovídat cashflow přesněji než dříve.</span><span class="sxs-lookup"><span data-stu-id="94202-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="94202-108">Může také pomoci manažerům činit rozhodnutí, která optimalizují příležitosti v kontextu jejich aktuální pozice hotovosti.</span><span class="sxs-lookup"><span data-stu-id="94202-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="94202-109">Pro většinu společností je správa cashflow a jejich prognózování zdlouhavým, opakujícím se a ručním procesem.</span><span class="sxs-lookup"><span data-stu-id="94202-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="94202-110">Většina společností se spoléhá na řešení Microsoft Excel, která mají různé stupně složitosti.</span><span class="sxs-lookup"><span data-stu-id="94202-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="94202-111">Mezi výzvy týkající se přesné předpovědi cashflow patří následující:</span><span class="sxs-lookup"><span data-stu-id="94202-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="94202-112">Data nejsou k dispozici osobám s rozhodovací pravomocí, protože jsou rozptýlena na více místech, včetně:</span><span class="sxs-lookup"><span data-stu-id="94202-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="94202-113">Účetní systém nebo systém plánování podnikových zdrojů</span><span class="sxs-lookup"><span data-stu-id="94202-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="94202-114">Software pro finanční plánování</span><span class="sxs-lookup"><span data-stu-id="94202-114">Financial planning software</span></span>
  - <span data-ttu-id="94202-115">Aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="94202-115">Excel</span></span>
  - <span data-ttu-id="94202-116">Další softwarové aplikace</span><span class="sxs-lookup"><span data-stu-id="94202-116">Additional software applications</span></span> 
- <span data-ttu-id="94202-117">Prognózy jsou založeny na interních znalostních bázích, které se nacházejí v „silech“ v každé doméně nebo oddělení.</span><span class="sxs-lookup"><span data-stu-id="94202-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="94202-118">Měření přesnosti prognózování cashflow po uplatnění financí je nejisté a obtížné.</span><span class="sxs-lookup"><span data-stu-id="94202-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="94202-119">Podrobnosti o funkci prognózování cashflow</span><span class="sxs-lookup"><span data-stu-id="94202-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="94202-120">Funkce prognózování cashflow zahrnuje následující funkce.</span><span class="sxs-lookup"><span data-stu-id="94202-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="94202-121">Usnadňuje integraci dat cashflow z externích systémů do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="94202-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="94202-122">Prognózy cashflow mohou také využívat rámec importu a exportu dat.</span><span class="sxs-lookup"><span data-stu-id="94202-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="94202-123">Tento rámec usnadňuje integraci s Excel OData.</span><span class="sxs-lookup"><span data-stu-id="94202-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="94202-124">Můžete také kombinovat data z více zdrojů a vytvořit komplexní řešení cashflow.</span><span class="sxs-lookup"><span data-stu-id="94202-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="94202-125">Představuje inteligentní pozici hotovosti.</span><span class="sxs-lookup"><span data-stu-id="94202-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="94202-126">Pozice hotovosti se vytváří na základě chování platby zákazníka, aby bylo možné predikovat, kdy může společnost očekávat, že na její účty dorazí hotovost.</span><span class="sxs-lookup"><span data-stu-id="94202-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="94202-127">Analyzuje také historické vzorce platících dodavatelů, aby predikoval, kdy je pravděpodobné, že budou uhrazeny budoucí faktury a objednávky.</span><span class="sxs-lookup"><span data-stu-id="94202-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="94202-128">Představuje inteligentní prognózování cashflow pro dlouhodobé prognózování pomocí časových řad prostřednictvím automatizované integrace s AI Builder.</span><span class="sxs-lookup"><span data-stu-id="94202-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="94202-129">Poskytuje možnost ukládat konkrétní pozice cashflow nebo prognózy, upravovat je a poté snadno porovnávat a měřit výkon prognózy se skutečnými finančními údaji.</span><span class="sxs-lookup"><span data-stu-id="94202-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="94202-130">Umožňuje pravděpodobnostní analýzu prostřednictvím porovnání snímků.</span><span class="sxs-lookup"><span data-stu-id="94202-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="94202-131">Můžete například vytvořit několik snímků, které představují optimistické, pesimistické a nejrealističtější zobrazení cashflow a poté porovnat a zobrazit rozdíly.</span><span class="sxs-lookup"><span data-stu-id="94202-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="94202-132">Poskytuje možnost zobrazit prognózu cashflow ve více měnách, napříč právnickými osobami a filtrovat a zobrazit cashflow související s bankovním účtem.</span><span class="sxs-lookup"><span data-stu-id="94202-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="94202-133">Umožňuje filtrovat a zobrazit bankovní účty, které souvisejí s finančními dimenzemi.</span><span class="sxs-lookup"><span data-stu-id="94202-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="94202-134">Funkce prognózování cashflow v Dynamics 365 Finance umožní vaší organizaci transformovat zdlouhavé, složité a přitom opakující se projekce cashflow na jednoduchý automatizovaný proces.</span><span class="sxs-lookup"><span data-stu-id="94202-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="94202-135">Automatizace nejzdlouhavějších aspektů prognózování cashflow vám umožní soustředit se na kritické rozhodování a dosáhnout požadovaných obchodních výsledků.</span><span class="sxs-lookup"><span data-stu-id="94202-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="94202-136">Nastavení dimenzí pro prognózu cashflow</span><span class="sxs-lookup"><span data-stu-id="94202-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="94202-137">Nová karta na stránce **Nastavení prognózy cashflow** umožňuje řídit, jaké finanční dimenze se mají použít pro filtrování v pracovním prostoru **Prognóza cashflow**.</span><span class="sxs-lookup"><span data-stu-id="94202-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="94202-138">Tato karta se zobrazí, pouze pokud je povolena funkce prognózy cashflow.</span><span class="sxs-lookup"><span data-stu-id="94202-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="94202-139">Na kartě **Dimenze** vyberte ze seznamu dimenze, které se mají použít pro filtrování, a pomocí kláves se šipkami je přesuňte do pravého sloupce.</span><span class="sxs-lookup"><span data-stu-id="94202-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="94202-140">Pro filtrování dat prognózy cashflow lze vybrat pouze dvě dimenze.</span><span class="sxs-lookup"><span data-stu-id="94202-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

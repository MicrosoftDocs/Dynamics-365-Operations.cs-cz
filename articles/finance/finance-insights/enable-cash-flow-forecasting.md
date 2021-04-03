---
title: Povolení prognózy cashflow (Preview)
description: Toto téma vysvětluje, jak zapnout funkci prognózy cashflow ve finančních přehledech.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2de75962f5b8a71c8f7138289078b5c669ae1daa
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250571"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="208d6-103">Povolení prognózy cashflow (Preview)</span><span class="sxs-lookup"><span data-stu-id="208d6-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="208d6-104">Toto téma vysvětluje, jak zapnout funkci prognózy cashflow ve finančních přehledech.</span><span class="sxs-lookup"><span data-stu-id="208d6-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="208d6-105">Chcete-li použít předpovědi plateb v cashflow, musíte nastavit funkci předpovědí plateb zákazníků, jak je popsáno v části [Povolení předpovědí plateb zákazníka](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="208d6-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="208d6-106">Použijte informace ze stránky prostředí v Microsoft Dynamics Lifecycle Services (LCS) pro připojení k primární instanci Azure SQL pro dané prostředí.</span><span class="sxs-lookup"><span data-stu-id="208d6-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="208d6-107">Spuštěním následujícího příkazu Transact-SQL (T-SQL) zapněte testování pro prostředí sandboxu.</span><span class="sxs-lookup"><span data-stu-id="208d6-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="208d6-108">(Možná budete muset zapnout přístup ke své IP adrese v LCS, než se budete moci vzdáleně připojit k aplikačnímu objektovému serveru \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="208d6-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="208d6-109">Pokud vaše nasazení Microsoft Dynamics 365 Finance je nasazení Service Fabric, můžete tento krok přeskočit.</span><span class="sxs-lookup"><span data-stu-id="208d6-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="208d6-110">Tým finančních přehledů už měl testování zapnout za vás.</span><span class="sxs-lookup"><span data-stu-id="208d6-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="208d6-111">Pokud nevidíte funkci v pracovním prostoru **Správa funkcí** nebo pokud při pokusu o zapnutí dojde k potížím, kontaktujte <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="208d6-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="208d6-112">Otevřete pracovní prostor **Správa funkcí** a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="208d6-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="208d6-113">Vyberte možnost **Zkontrolovat aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="208d6-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="208d6-114">Zapněte následující funkce:</span><span class="sxs-lookup"><span data-stu-id="208d6-114">Turn on the following features:</span></span>

        - <span data-ttu-id="208d6-115">Nový ovládací prvek mřížky</span><span class="sxs-lookup"><span data-stu-id="208d6-115">New grid control</span></span>
        - <span data-ttu-id="208d6-116">Seskupování do mřížek (Preview)</span><span class="sxs-lookup"><span data-stu-id="208d6-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="208d6-117">Předpovědi plateb odběratelů (Preview)</span><span class="sxs-lookup"><span data-stu-id="208d6-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="208d6-118">Prognózy cashflow (Preview)</span><span class="sxs-lookup"><span data-stu-id="208d6-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="208d6-119">Přejděte na **Pokladna a banka \> Nastavení prognózy cashflow** a přidejte účty likvidity, které by měly být zahrnuty do prognóz.</span><span class="sxs-lookup"><span data-stu-id="208d6-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="208d6-120">Pokud nejsou zřízeny účty likvidity, nelze generovat cashflow.</span><span class="sxs-lookup"><span data-stu-id="208d6-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="208d6-121">Jděte na **Pokladna a banka \> Nastavení \> Finanční přehledy (Preview) \> Prognózy cashflow (Preview)** a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="208d6-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="208d6-122">Na kartě **Prognózy cashflow** vyberte **Povolit funkci**.</span><span class="sxs-lookup"><span data-stu-id="208d6-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="208d6-123">Vyberte **Vytvořit predikční model**.</span><span class="sxs-lookup"><span data-stu-id="208d6-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="208d6-124">Další informace o funkci prognózy cashflow naleznete v tématu [Prognóza cashflow](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="208d6-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="208d6-125">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="208d6-125">Privacy notice</span></span>

<span data-ttu-id="208d6-126">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="208d6-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Povolení prognózy cashflow (Preview)
description: Toto téma vysvětluje, jak zapnout funkci prognózy cashflow ve finančních přehledech.
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
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222551"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="61674-103">Povolení prognózy cashflow (Preview)</span><span class="sxs-lookup"><span data-stu-id="61674-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="61674-104">Toto téma vysvětluje, jak zapnout funkci prognózy cashflow ve finančních přehledech.</span><span class="sxs-lookup"><span data-stu-id="61674-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="61674-105">Chcete-li použít předpovědi plateb v cashflow, musíte nastavit funkci předpovědí plateb zákazníků, jak je popsáno v části [Povolení předpovědí plateb zákazníka](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="61674-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="61674-106">Použijte informace ze stránky prostředí v Microsoft Dynamics Lifecycle Services (LCS) pro připojení k primární instanci Azure SQL pro dané prostředí.</span><span class="sxs-lookup"><span data-stu-id="61674-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="61674-107">Spuštěním následujícího příkazu Transact-SQL (T-SQL) zapněte testování pro prostředí sandboxu.</span><span class="sxs-lookup"><span data-stu-id="61674-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="61674-108">(Možná budete muset zapnout přístup ke své IP adrese v LCS, než se budete moci vzdáleně připojit k aplikačnímu objektovému serveru \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="61674-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="61674-109">Tento krok přeskočte, pokud používáte verzi 10.0.20 nebo novější nebo pokud používáte nasazení Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="61674-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="61674-110">Tým finančních přehledů už měl testování zapnout za vás.</span><span class="sxs-lookup"><span data-stu-id="61674-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="61674-111">Pokud nevidíte funkci v pracovním prostoru **Správa funkcí** nebo pokud při pokusu o zapnutí dojde k potížím, kontaktujte <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="61674-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="61674-112">Otevřete pracovní prostor **Správa funkcí** a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="61674-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="61674-113">Vyberte možnost **Zkontrolovat aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="61674-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="61674-114">Zapněte následující funkce:</span><span class="sxs-lookup"><span data-stu-id="61674-114">Turn on the following features:</span></span>

        - <span data-ttu-id="61674-115">Nový ovládací prvek mřížky</span><span class="sxs-lookup"><span data-stu-id="61674-115">New grid control</span></span>
        - <span data-ttu-id="61674-116">Seskupování do mřížek (Preview)</span><span class="sxs-lookup"><span data-stu-id="61674-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="61674-117">Předpovědi plateb odběratelů (Preview)</span><span class="sxs-lookup"><span data-stu-id="61674-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="61674-118">Prognózy cashflow (Preview)</span><span class="sxs-lookup"><span data-stu-id="61674-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="61674-119">Přejděte na **Pokladna a banka \> Nastavení prognózy cashflow** a přidejte účty likvidity, které by měly být zahrnuty do prognóz.</span><span class="sxs-lookup"><span data-stu-id="61674-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="61674-120">Pokud nejsou zřízeny účty likvidity, nelze generovat cashflow.</span><span class="sxs-lookup"><span data-stu-id="61674-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="61674-121">Jděte na **Pokladna a banka \> Nastavení \> Finanční přehledy (Preview) \> Prognózy cashflow (Preview)** a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="61674-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="61674-122">Na kartě **Prognózy cashflow** vyberte **Povolit funkci**.</span><span class="sxs-lookup"><span data-stu-id="61674-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="61674-123">Vyberte **Vytvořit predikční model**.</span><span class="sxs-lookup"><span data-stu-id="61674-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="61674-124">Další informace o funkci prognózy cashflow naleznete v tématu [Prognóza cashflow](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="61674-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

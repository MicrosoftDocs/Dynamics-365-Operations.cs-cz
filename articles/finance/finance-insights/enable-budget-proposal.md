---
title: Povolení návrhů rozpočtu (Preview)
description: Toto téma vysvětluje, jak zapnout funkci návrhu rozpočtu ve finančních přehledech.
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
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d8443c4e3e6f3d3a90acedc7c05b2846d6b68369
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646198"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="219ab-103">Povolení návrhů rozpočtu (Preview)</span><span class="sxs-lookup"><span data-stu-id="219ab-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="219ab-104">Toto téma vysvětluje, jak zapnout funkci návrhu rozpočtu ve finančních přehledech.</span><span class="sxs-lookup"><span data-stu-id="219ab-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="219ab-105">Použijte informace ze stránky prostředí v Microsoft Dynamics Lifecycle Services (LCS) pro připojení k primární instanci Azure SQL pro dané prostředí.</span><span class="sxs-lookup"><span data-stu-id="219ab-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="219ab-106">Spuštěním následujícího příkazu Transact-SQL (T-SQL) zapněte testování pro prostředí sandboxu.</span><span class="sxs-lookup"><span data-stu-id="219ab-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="219ab-107">(Možná budete muset zapnout přístup ke své IP adrese v LCS, než se budete moci vzdáleně připojit k aplikačnímu objektovému serveru \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="219ab-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="219ab-108">Pokud vaše nasazení Microsoft Dynamics 365 Finance je nasazení Service Fabric, můžete tento krok přeskočit.</span><span class="sxs-lookup"><span data-stu-id="219ab-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="219ab-109">Tým finančních přehledů už měl testování zapnout za vás.</span><span class="sxs-lookup"><span data-stu-id="219ab-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="219ab-110">Pokud nevidíte funkci v pracovním prostoru **Správa funkcí** nebo pokud se při pokusu o zapnutí setkáte s problémy, pošlete e-mail na adresu [Tým pro aplikaci Finanční přehledy (Preview)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="219ab-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="219ab-111">Otevřete pracovní prostor **Správa funkcí** a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="219ab-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="219ab-112">Vyberte možnost **Zkontrolovat aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="219ab-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="219ab-113">Vyhledejte **Návrh rozpočtu** a zapněte tuto funkci.</span><span class="sxs-lookup"><span data-stu-id="219ab-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="219ab-114">Jděte na **Rozpočtování \> Nastavení \> Základní rozpočtování \> Návrh rozpočtu (Preview)** a vyberte **Povolit funkci**.</span><span class="sxs-lookup"><span data-stu-id="219ab-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="219ab-115">Oznámení o ochraně osobních údajů</span><span class="sxs-lookup"><span data-stu-id="219ab-115">Privacy notice</span></span>
<span data-ttu-id="219ab-116">Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.</span><span class="sxs-lookup"><span data-stu-id="219ab-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
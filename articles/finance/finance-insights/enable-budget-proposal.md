---
title: Povolení návrhů rozpočtu (Preview)
description: Toto téma vysvětluje, jak zapnout funkci návrhu rozpočtu ve finančních přehledech.
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222527"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="9fc52-103">Povolení návrhů rozpočtu (Preview)</span><span class="sxs-lookup"><span data-stu-id="9fc52-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="9fc52-104">Toto téma vysvětluje, jak zapnout funkci návrhu rozpočtu ve finančních přehledech.</span><span class="sxs-lookup"><span data-stu-id="9fc52-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="9fc52-105">Použijte informace ze stránky prostředí v Microsoft Dynamics Lifecycle Services (LCS) pro připojení k primární instanci Azure SQL pro dané prostředí.</span><span class="sxs-lookup"><span data-stu-id="9fc52-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="9fc52-106">Spuštěním následujícího příkazu Transact-SQL (T-SQL) zapněte testování pro prostředí sandboxu.</span><span class="sxs-lookup"><span data-stu-id="9fc52-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="9fc52-107">(Možná budete muset zapnout přístup ke své IP adrese v LCS, než se budete moci vzdáleně připojit k aplikačnímu objektovému serveru \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="9fc52-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="9fc52-108">Tento krok přeskočte, pokud používáte verzi 10.0.20 nebo novější nebo pokud používáte nasazení Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="9fc52-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="9fc52-109">Tým finančních přehledů už měl testování zapnout za vás.</span><span class="sxs-lookup"><span data-stu-id="9fc52-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="9fc52-110">Pokud nevidíte funkci v pracovním prostoru **Správa funkcí** nebo pokud při pokusu o zapnutí dojde k potížím, kontaktujte <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="9fc52-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="9fc52-111">Otevřete pracovní prostor **Správa funkcí** a postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="9fc52-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="9fc52-112">Vyberte možnost **Zkontrolovat aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="9fc52-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="9fc52-113">Vyhledejte **Návrh rozpočtu** a zapněte tuto funkci.</span><span class="sxs-lookup"><span data-stu-id="9fc52-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="9fc52-114">Jděte na **Rozpočtování \> Nastavení \> Základní rozpočtování \> Návrh rozpočtu (Preview)** a vyberte **Povolit funkci**.</span><span class="sxs-lookup"><span data-stu-id="9fc52-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Konfigurace parametrů, které ovlivňují výkazy maloobchodu
description: Toto téma ukazuje konfigurace pro parametry velkoobchodu, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7892a216d836ebcc297a5b7eb87bc996dd9b91bf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140824"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="1aa91-103">Konfigurace parametrů, které ovlivňují výkazy maloobchodu</span><span class="sxs-lookup"><span data-stu-id="1aa91-103">Configure parameters that affect retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1aa91-104">Toto téma ukazuje konfigurace pro parametry velkoobchodu, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="1aa91-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="1aa91-105">Tato procedura používá ukázkovou společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="1aa91-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="1aa91-106">V navigačním podokně přejděte na **Moduly > Maloobchodní a velkoobchodní prodej > Nastavení centrály > Parametry > Parametry velkoobchodu**.</span><span class="sxs-lookup"><span data-stu-id="1aa91-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="1aa91-107">Vyberte kartu **Účtování**.</span><span class="sxs-lookup"><span data-stu-id="1aa91-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="1aa91-108">Pokud chcete zaúčtovat konkrétně částky časové slevy, vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="1aa91-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="1aa91-109">Pokud chcete použít výchozí účet, vyberte **Standardní** nebo vyberte **Periodický**, pokud chcete definovat účet, který má být použit pro jednotlivé časové slevy.</span><span class="sxs-lookup"><span data-stu-id="1aa91-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="1aa91-110">Vyberte **Souhrn** v případě, že řádky zásob mají být agregovány vždy, když je to možné.</span><span class="sxs-lookup"><span data-stu-id="1aa91-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="1aa91-111">Vyberte **Ano**, pokud faktury a platby mají být automaticky vyrovnány v rámci procesu zaúčtování výkazu.</span><span class="sxs-lookup"><span data-stu-id="1aa91-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="1aa91-112">Vyberte **Ano**, pokud je nutné agregovat transakce odvodu do trezoru.</span><span class="sxs-lookup"><span data-stu-id="1aa91-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="1aa91-113">Vyberte **Ano**, pokud je nutné agregovat transakce odvodu do banky.</span><span class="sxs-lookup"><span data-stu-id="1aa91-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="1aa91-114">Výběrem možnosti **Ano** aktivujete agregace pro zaúčtování výkazu.</span><span class="sxs-lookup"><span data-stu-id="1aa91-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="1aa91-115">Výběrem možnosti **Ano** můžete vytvořit a zpracovat objednávky současně při zaúčtování výkazů.</span><span class="sxs-lookup"><span data-stu-id="1aa91-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="1aa91-116">Zadejte maximální počet objednávek, které mají být zpracovány v jednotlivých dávkových úlohách.</span><span class="sxs-lookup"><span data-stu-id="1aa91-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="1aa91-117">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1aa91-117">Select **Save**.</span></span>


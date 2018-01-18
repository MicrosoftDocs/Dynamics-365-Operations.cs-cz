--- 
title: " Konfigurace parametrů pro maloobchodní výkazy"
description: "Tato procedura ukazuje konfigurace pro Parametry maloobchodu, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 61540297a2ebbbc76657734140b8add009db67ca
ms.contentlocale: cs-cz
ms.lasthandoff: 01/17/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="0af41-103"> Konfigurace parametrů pro maloobchodní výkazy</span><span class="sxs-lookup"><span data-stu-id="0af41-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0af41-104">Tato procedura ukazuje konfigurace pro Parametry maloobchodu, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="0af41-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="0af41-105">Tato procedura používá ukázkovou společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="0af41-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="0af41-106">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Nastavení centrály > Parametry > Parametry maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="0af41-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="0af41-107">Klikněte na kartu Zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="0af41-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="0af41-108">Pokud chcete zaúčtovat konkrétně částky časové slevy, vyberte "Ano".</span><span class="sxs-lookup"><span data-stu-id="0af41-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="0af41-109">Pokud chcete použít výchozí účet, vyberte „Standardní“ nebo vyberte „Periodický“, pokud chcete definovat účet, který má být použit pro jednotlivé časové slevy.</span><span class="sxs-lookup"><span data-stu-id="0af41-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="0af41-110">Vyberte „Souhrn“ v případě, že řádky zásob mají být agregovány vždy, když je to možné.</span><span class="sxs-lookup"><span data-stu-id="0af41-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="0af41-111">Vyberte „Ano“, pokud faktury a platby mají být automaticky vyrovnány v rámci procesu zaúčtování výkazu.</span><span class="sxs-lookup"><span data-stu-id="0af41-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="0af41-112">Vyberte „Ano“, pokud je nutné agregovat transakce odvodu do trezoru.</span><span class="sxs-lookup"><span data-stu-id="0af41-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="0af41-113">Vyberte „Ano“, pokud je nutné agregovat transakce odvodu do banky.</span><span class="sxs-lookup"><span data-stu-id="0af41-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="0af41-114">Výběrem možnosti „Ano“ aktivujete agregace pro zaúčtování výkazu.</span><span class="sxs-lookup"><span data-stu-id="0af41-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="0af41-115">Výběrem možnosti „Ano“ můžete vytvořit a zpracovat objednávky současně při zaúčtování výkazů.</span><span class="sxs-lookup"><span data-stu-id="0af41-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="0af41-116">Zadejte maximální počet objednávek, které mají být zpracovány v jednotlivých dávkových úlohách.</span><span class="sxs-lookup"><span data-stu-id="0af41-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="0af41-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0af41-117">Click Save.</span></span>



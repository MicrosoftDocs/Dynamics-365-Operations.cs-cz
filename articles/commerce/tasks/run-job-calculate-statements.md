---
title: Konfigurace a spuštění úlohy pro výpočet výkazů
description: Tento postup vás provede konfigurací a spuštěním opakovaných dávkových úloh pro tvorbu a výpočet výkazů pro vybraný obchod nebo skupinu obchodů.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 973236acca0cb8c0d57171e4bb9d4daaa7faaf38
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410816"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="0f54a-103">Konfigurace a spuštění úlohy pro výpočet výkazů</span><span class="sxs-lookup"><span data-stu-id="0f54a-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f54a-104">Tento postup vás provede konfigurací a spuštěním opakovaných dávkových úloh pro tvorbu a výpočet výkazů pro vybraný obchod nebo skupinu obchodů.</span><span class="sxs-lookup"><span data-stu-id="0f54a-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="0f54a-105">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="0f54a-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="0f54a-106">Přejděte na Všechny pracovní prostory > Uložit finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="0f54a-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="0f54a-107">Klikněte na Vypočítat výkazy.</span><span class="sxs-lookup"><span data-stu-id="0f54a-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="0f54a-108">Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte určitý obchod nebo uzel.</span><span class="sxs-lookup"><span data-stu-id="0f54a-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="0f54a-109">Kliknutím na šipku přidejte výběr.</span><span class="sxs-lookup"><span data-stu-id="0f54a-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="0f54a-110">Klikněte na kartu Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="0f54a-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="0f54a-111">Vyberte možnost „Ano“ v části Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="0f54a-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="0f54a-112">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="0f54a-112">Click Recurrence.</span></span>
6. <span data-ttu-id="0f54a-113">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="0f54a-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="0f54a-114">Zadejte čas do pole Počáteční čas.</span><span class="sxs-lookup"><span data-stu-id="0f54a-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="0f54a-115">Vyberte možnost Bez koncového data.</span><span class="sxs-lookup"><span data-stu-id="0f54a-115">Select the No end date option.</span></span>
9. <span data-ttu-id="0f54a-116">V poli PatternUnit zadejte „Dny“.</span><span class="sxs-lookup"><span data-stu-id="0f54a-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="0f54a-117">Do pole Za zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0f54a-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="0f54a-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0f54a-118">Click OK.</span></span>
12. <span data-ttu-id="0f54a-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0f54a-119">Click OK.</span></span>


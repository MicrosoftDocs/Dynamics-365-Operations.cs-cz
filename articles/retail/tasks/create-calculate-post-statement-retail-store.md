--- 
title: " Vytvoření, výpočet a zaúčtování výkazu pro maloobchod"
description: "Tento postup vás provede manuálním postupem pro vytvoření, výpočet a zaúčtování výpisu pro obchod."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9f9888d04f4e2419de9d4a6857a81ae40f6f21a
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="9e513-103"> Vytvoření, výpočet a zaúčtování výkazu pro maloobchod</span><span class="sxs-lookup"><span data-stu-id="9e513-103">Create, calculate, and post a statement for a retail store</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9e513-104">Tento postup vás provede manuálním postupem pro vytvoření, výpočet a zaúčtování výpisu pro obchod.</span><span class="sxs-lookup"><span data-stu-id="9e513-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="9e513-105">Existují také dávkové úlohy, které lze konfigurovat pro stejné úkoly.</span><span class="sxs-lookup"><span data-stu-id="9e513-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="9e513-106">Postup pro konfiguraci a spuštění dávkových úlohy můžete najít v jiných tématech.</span><span class="sxs-lookup"><span data-stu-id="9e513-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="9e513-107">Chcete-li provést tento postup, musíte mít transakce, které byly dokončeny v POS a potom převedeny do aplikace Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="9e513-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="9e513-108">Tento záznam používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="9e513-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="9e513-109">Tento postup může odkazovat na Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="9e513-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="9e513-110">Všimněte si, Dynamics AX se nyní nazývá Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="9e513-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="9e513-111">Přejděte na Všechny pracovní prostory > ..</span><span class="sxs-lookup"><span data-stu-id="9e513-111">Go to All workspaces > ..</span></span> <span data-ttu-id="9e513-112">> Finance maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="9e513-112">> Retail store financials.</span></span>
2. <span data-ttu-id="9e513-113">Klikněte na Nový výkaz.</span><span class="sxs-lookup"><span data-stu-id="9e513-113">Click New statement.</span></span>
3. <span data-ttu-id="9e513-114">V poli Číslo obchodu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9e513-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9e513-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9e513-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9e513-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9e513-116">Click OK.</span></span>
    * <span data-ttu-id="9e513-117">Nastavení skupiny obsahuje nastavení, která řídí, které transakce budou zahrnuty do výkazu a způsob jejich seskupení do řádků výkazu.</span><span class="sxs-lookup"><span data-stu-id="9e513-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="9e513-118">Můžete otevřít nastavení skupiny a tato nastavení změnit, nebo můžete použít výchozí hodnoty.</span><span class="sxs-lookup"><span data-stu-id="9e513-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="9e513-119">Pole Metoda výkazu definuje způsob, jak budou seskupeny řádky výkazu.</span><span class="sxs-lookup"><span data-stu-id="9e513-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="9e513-120">Pokud chcete vypočítat výkaz pouze pro konkrétního zaměstnance nebo registr, vyberte zaměstnance nebo registrační pokladnu.</span><span class="sxs-lookup"><span data-stu-id="9e513-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="9e513-121">Vyberte možnost v poli Metoda uzávěrky.</span><span class="sxs-lookup"><span data-stu-id="9e513-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="9e513-122">Klikněte na Vypočítat výkaz.</span><span class="sxs-lookup"><span data-stu-id="9e513-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="9e513-123">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="9e513-123">Click Yes.</span></span>
    * <span data-ttu-id="9e513-124">Po výpočtu výkazu, by měly být vytvořený řádky s celkovými částkami pro každý použitý způsob platby a metodu výkazu.</span><span class="sxs-lookup"><span data-stu-id="9e513-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="9e513-125">Zadejte do každého řádku spočtenou částka, pokud je nutné ji zadávat nebo aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="9e513-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="9e513-126">Vypočtená pole budou vyplněna částkami z výkazů úhrad provedených v POS.</span><span class="sxs-lookup"><span data-stu-id="9e513-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="9e513-127">Klikněte na Zaúčtovat výkaz.</span><span class="sxs-lookup"><span data-stu-id="9e513-127">Click Post statement.</span></span>
10. <span data-ttu-id="9e513-128">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="9e513-128">Click Close.</span></span>
11. <span data-ttu-id="9e513-129">Přejděte na Maloobchodní a velkoobchodní prodej > Kanály > Finance maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="9e513-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="9e513-130">Klepněte na kartu Zaúčtované výpisy.</span><span class="sxs-lookup"><span data-stu-id="9e513-130">Click the Posted statements tab.</span></span>



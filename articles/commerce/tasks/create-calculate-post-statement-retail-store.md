---
title: Vytvoření, výpočet a zaúčtování výkazů pro maloobchod
description: Toto téma popisuje ruční postup pro vytvoření, výpočet a zaúčtování výpisu pro obchod.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58900ca4d3f6893689822a8cc5657d8c91772f65
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798530"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="332cc-103">Vytvoření, výpočet a zaúčtování výkazů pro maloobchod</span><span class="sxs-lookup"><span data-stu-id="332cc-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="332cc-104">Toto téma popisuje ruční postup pro vytvoření, výpočet a zaúčtování výpisu pro obchod.</span><span class="sxs-lookup"><span data-stu-id="332cc-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="332cc-105">Existují také dávkové úlohy, které lze konfigurovat pro stejné úkoly.</span><span class="sxs-lookup"><span data-stu-id="332cc-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="332cc-106">Postup pro konfiguraci a spuštění dávkových úlohy můžete najít v jiných tématech.</span><span class="sxs-lookup"><span data-stu-id="332cc-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="332cc-107">Pokud chcete tento postup dokončit, musíte mít transakce, které byly dokončeny v POS a pak odeslány do aplikace Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="332cc-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="332cc-108">Tento záznam používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="332cc-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="332cc-109">Na domovské stránce vyberte **Finance obchodu**.</span><span class="sxs-lookup"><span data-stu-id="332cc-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="332cc-110">Vyberte **Nový výpis**.</span><span class="sxs-lookup"><span data-stu-id="332cc-110">Select **New statement**.</span></span>
3. <span data-ttu-id="332cc-111">V poli **Uložit číslo** vyberte z rozevíracího seznamu požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="332cc-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="332cc-112">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="332cc-112">Select **OK**.</span></span>
5. <span data-ttu-id="332cc-113">Skupina **Nastavení** obsahuje nastavení, která řídí, které transakce budou zahrnuty do výkazu a způsob jejich seskupení do řádků výkazu.</span><span class="sxs-lookup"><span data-stu-id="332cc-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="332cc-114">Můžete otevřít skupinu **Nastavení** a tato nastavení změnit, nebo můžete použít výchozí hodnoty.</span><span class="sxs-lookup"><span data-stu-id="332cc-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="332cc-115">Pole **Metoda výkazu** definuje způsob, jak budou seskupeny řádky výkazu.</span><span class="sxs-lookup"><span data-stu-id="332cc-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="332cc-116">Pokud chcete vypočítat výkaz pouze pro konkrétního zaměstnance nebo registr, v poli **zaměstnanec/registr** vyberte zaměstnance nebo registrační pokladnu.</span><span class="sxs-lookup"><span data-stu-id="332cc-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="332cc-117">Vyberte možnost v poli **Metoda uzávěrky**.</span><span class="sxs-lookup"><span data-stu-id="332cc-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="332cc-118">V podokně akcí vyberte **Vypočítat výkaz**.</span><span class="sxs-lookup"><span data-stu-id="332cc-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="332cc-119">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="332cc-119">Select **Yes**.</span></span>
    - <span data-ttu-id="332cc-120">Po výpočtu výkazu, by měly být vytvořený řádky s celkovými částkami pro každý použitý způsob platby a metodu výkazu.</span><span class="sxs-lookup"><span data-stu-id="332cc-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="332cc-121">Zadejte do každého řádku spočtenou částka, pokud je nutné ji zadávat nebo aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="332cc-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="332cc-122">Vypočtená pole budou vyplněna částkami z výkazů úhrad provedených v POS.</span><span class="sxs-lookup"><span data-stu-id="332cc-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="332cc-123">V podokně akcí vyberte **Publikovat výkaz**.</span><span class="sxs-lookup"><span data-stu-id="332cc-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="332cc-124">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="332cc-124">Select **Close**.</span></span>
11. <span data-ttu-id="332cc-125">Zavřete podokno.</span><span class="sxs-lookup"><span data-stu-id="332cc-125">Close the pane.</span></span>
12. <span data-ttu-id="332cc-126">Na domovské stránce vyberte **Finance obchodu**.</span><span class="sxs-lookup"><span data-stu-id="332cc-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="332cc-127">Vyberte kartu **Publikované výkazy**.</span><span class="sxs-lookup"><span data-stu-id="332cc-127">Select the **Posted statements** tab.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
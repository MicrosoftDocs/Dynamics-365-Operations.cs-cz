--- 
title: "Nabídka pořízení dlouhodobého majetku"
description: "Tento postup popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku."
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 34638f9dc88eb3850f659e4b9741d02418213112
ms.contentlocale: cs-cz
ms.lasthandoff: 09/11/2018

---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="4f5cf-103">Nabídka pořízení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="4f5cf-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f5cf-104">Tento postup popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="4f5cf-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="4f5cf-106">Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="4f5cf-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-107">Click New.</span></span>
3. <span data-ttu-id="4f5cf-108">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="4f5cf-109">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-109">Click Lines.</span></span>
5. <span data-ttu-id="4f5cf-110">Klepněte na tlačítko Návrhy.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-110">Click Proposals.</span></span>
6. <span data-ttu-id="4f5cf-111">Klikněte na Návrh pořizovací ceny.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="4f5cf-112">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-112">Click Filter.</span></span>
8. <span data-ttu-id="4f5cf-113">Kliknutím na tlačítko Vynulovat vymažte předchozí hodnoty.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="4f5cf-114">Vyberte řádek Číslo dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="4f5cf-115">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="4f5cf-116">Nastavte zbývající kritéria pro dlouhodobý majetek, který chcete získat s tímto návrhem.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="4f5cf-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-117">Click OK.</span></span>
12. <span data-ttu-id="4f5cf-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-118">Click OK.</span></span>
    * <span data-ttu-id="4f5cf-119">Ověřte, že byly vytvořeny řádky transakce.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="4f5cf-120">V návrhu pořízení bude zahrnut pouze dlouhodobý majetek s datem pořízení a pořizovací cenou nastavenou v knize.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="4f5cf-121">Klikněte na kartu Knihy.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-121">Click the Books tab.</span></span>
14. <span data-ttu-id="4f5cf-122">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="4f5cf-122">Click Post.</span></span>



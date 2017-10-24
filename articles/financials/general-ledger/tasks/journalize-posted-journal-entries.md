--- 
title: "Zapsání zaúčtovaných položek deníku do deníku"
description: "Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 490e9a4beda43f6e32b87792b11153c3e8e322d6
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="5d2f8-103">Zapsání zaúčtovaných položek deníku do deníku</span><span class="sxs-lookup"><span data-stu-id="5d2f8-103">Journalize posted journal entries</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d2f8-104">Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="5d2f8-105">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="5d2f8-106">Ověřte nastavení pro deník hlavní knihy v části Hlavní kniha > Nastavení hlavní knihy > Parametry hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="5d2f8-107">Pole Rozšířený deník hlavní knihy lze nastavit na Ano nebo Ne.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="5d2f8-108">Pokud ano, bude výstup sestavy jiný.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="5d2f8-109">Vyberte, zda období lze uzavřít, pokud nebyl spuštěn proces zařazení do deníku.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="5d2f8-110">Pokud je tato možnost nastavena na hodnotu Ano, období nelze zavřít, dokud neskončí proces zapisování do deníku pro toto období.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="5d2f8-111">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-111">Close the page.</span></span>
5. <span data-ttu-id="5d2f8-112">Přejděte do hlavní knihy > Periodické úkoly > Zapisování do deníku.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="5d2f8-113">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-113">Click Filter.</span></span>
7. <span data-ttu-id="5d2f8-114">Vyberte řádek obsahující kritéria filtru, která chcete definovat.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="5d2f8-115">V poli Kritéria zadejte nebo vyberte kritéria filtrování.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="5d2f8-116">Kliknutím na tlačítko OK stránku filtru zavřete.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="5d2f8-117">Kliknutím na tlačítko OK spusťte proces zařazení do deníku.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="5d2f8-118">Po dokončení procesu se vygeneruje sestava.</span><span class="sxs-lookup"><span data-stu-id="5d2f8-118">A report will be generated after the process is complete.</span></span>  



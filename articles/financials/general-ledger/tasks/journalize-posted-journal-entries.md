---
title: Zapsání zaúčtovaných položek deníku do deníku
description: Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b50809cf9eb59475856f91d9f1ddfe28ecfd8de6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547903"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="8b1d3-103">Zapsání zaúčtovaných položek deníku do deníku</span><span class="sxs-lookup"><span data-stu-id="8b1d3-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b1d3-104">Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="8b1d3-105">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="8b1d3-106">Ověřte nastavení pro deník hlavní knihy v části Hlavní kniha > Nastavení hlavní knihy > Parametry hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="8b1d3-107">Pole Rozšířený deník hlavní knihy lze nastavit na Ano nebo Ne.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="8b1d3-108">Pokud ano, bude výstup sestavy jiný.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="8b1d3-109">Vyberte, zda období lze uzavřít, pokud nebyl spuštěn proces zařazení do deníku.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="8b1d3-110">Pokud je tato možnost nastavena na hodnotu Ano, období nelze zavřít, dokud neskončí proces zapisování do deníku pro toto období.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="8b1d3-111">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-111">Close the page.</span></span>
5. <span data-ttu-id="8b1d3-112">Přejděte do hlavní knihy > Periodické úkoly > Zapisování do deníku.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="8b1d3-113">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-113">Click Filter.</span></span>
7. <span data-ttu-id="8b1d3-114">Vyberte řádek obsahující kritéria filtru, která chcete definovat.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="8b1d3-115">V poli Kritéria zadejte nebo vyberte kritéria filtrování.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="8b1d3-116">Kliknutím na tlačítko OK stránku filtru zavřete.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="8b1d3-117">Kliknutím na tlačítko OK spusťte proces zařazení do deníku.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="8b1d3-118">Po dokončení procesu se vygeneruje sestava.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-118">A report will be generated after the process is complete.</span></span>  


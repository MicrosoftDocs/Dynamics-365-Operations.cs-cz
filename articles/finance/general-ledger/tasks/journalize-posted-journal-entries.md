---
title: Zapsání zaúčtovaných položek deníku do deníku
description: Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f50ee568df492bcd811d2fefb1784bb55b50384b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441086"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="ed9db-103">Zapsání zaúčtovaných položek deníku do deníku</span><span class="sxs-lookup"><span data-stu-id="ed9db-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed9db-104">Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku.</span><span class="sxs-lookup"><span data-stu-id="ed9db-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="ed9db-105">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ed9db-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="ed9db-106">V **navigačním podokně** přejděte na **Moduly > Hlavní kniha > Nastavení hlavní knihy > Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="ed9db-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="ed9db-107">Pole **Rozšířený deník hlavní knihy** lze nastavit na Ano nebo Ne.</span><span class="sxs-lookup"><span data-stu-id="ed9db-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="ed9db-108">Pokud ano, bude výstup sestavy jiný.</span><span class="sxs-lookup"><span data-stu-id="ed9db-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="ed9db-109">Vyberte, zda období lze uzavřít, pokud nebyl spuštěn proces zařazení do deníku.</span><span class="sxs-lookup"><span data-stu-id="ed9db-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="ed9db-110">Pokud je tato možnost nastavena na hodnotu Ano, období nelze zavřít, dokud neskončí proces zapisování do deníku pro toto období.</span><span class="sxs-lookup"><span data-stu-id="ed9db-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="ed9db-111">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ed9db-111">Close the page.</span></span>
5. <span data-ttu-id="ed9db-112">V **navigačním podokně** přejděte na **Moduly > Hlavní kniha > Periodické úlohy > Zapisování do deníku**.</span><span class="sxs-lookup"><span data-stu-id="ed9db-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="ed9db-113">Klikněte na tlačítko **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="ed9db-113">Click **Filter**.</span></span>
7. <span data-ttu-id="ed9db-114">Vyberte řádek obsahující kritéria filtru, která chcete definovat.</span><span class="sxs-lookup"><span data-stu-id="ed9db-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="ed9db-115">V poli **Kritéria** zadejte nebo vyberte kritéria filtrování.</span><span class="sxs-lookup"><span data-stu-id="ed9db-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="ed9db-116">Kliknutím na tlačítko **OK** stránku filtru zavřete.</span><span class="sxs-lookup"><span data-stu-id="ed9db-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="ed9db-117">Kliknutím na tlačítko **OK** spusťte proces zařazení do deníku.</span><span class="sxs-lookup"><span data-stu-id="ed9db-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="ed9db-118">Po dokončení procesu se vygeneruje sestava.</span><span class="sxs-lookup"><span data-stu-id="ed9db-118">A report will be generated after the process is complete.</span></span>  


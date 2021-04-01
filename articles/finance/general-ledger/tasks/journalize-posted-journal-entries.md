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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca1aed3a77da66ef336942b2c178abdd425d3c25
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240659"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="2be83-103">Zapsání zaúčtovaných položek deníku do deníku</span><span class="sxs-lookup"><span data-stu-id="2be83-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2be83-104">Tento postup ukazuje zapisováním do deníku zaúčtovaných položek deníku.</span><span class="sxs-lookup"><span data-stu-id="2be83-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="2be83-105">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="2be83-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="2be83-106">V **navigačním podokně** přejděte na **Moduly > Hlavní kniha > Nastavení hlavní knihy > Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="2be83-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="2be83-107">Pole **Rozšířený deník hlavní knihy** lze nastavit na Ano nebo Ne.</span><span class="sxs-lookup"><span data-stu-id="2be83-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="2be83-108">Pokud ano, bude výstup sestavy jiný.</span><span class="sxs-lookup"><span data-stu-id="2be83-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="2be83-109">Vyberte, zda období lze uzavřít, pokud nebyl spuštěn proces zařazení do deníku.</span><span class="sxs-lookup"><span data-stu-id="2be83-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="2be83-110">Pokud je tato možnost nastavena na hodnotu Ano, období nelze zavřít, dokud neskončí proces zapisování do deníku pro toto období.</span><span class="sxs-lookup"><span data-stu-id="2be83-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="2be83-111">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2be83-111">Close the page.</span></span>
5. <span data-ttu-id="2be83-112">V **navigačním podokně** přejděte na **Moduly > Hlavní kniha > Periodické úlohy > Zapisování do deníku**.</span><span class="sxs-lookup"><span data-stu-id="2be83-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="2be83-113">Klikněte na tlačítko **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="2be83-113">Click **Filter**.</span></span>
7. <span data-ttu-id="2be83-114">Vyberte řádek obsahující kritéria filtru, která chcete definovat.</span><span class="sxs-lookup"><span data-stu-id="2be83-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="2be83-115">V poli **Kritéria** zadejte nebo vyberte kritéria filtrování.</span><span class="sxs-lookup"><span data-stu-id="2be83-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="2be83-116">Kliknutím na tlačítko **OK** stránku filtru zavřete.</span><span class="sxs-lookup"><span data-stu-id="2be83-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="2be83-117">Kliknutím na tlačítko **OK** spusťte proces zařazení do deníku.</span><span class="sxs-lookup"><span data-stu-id="2be83-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="2be83-118">Po dokončení procesu se vygeneruje sestava.</span><span class="sxs-lookup"><span data-stu-id="2be83-118">A report will be generated after the process is complete.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
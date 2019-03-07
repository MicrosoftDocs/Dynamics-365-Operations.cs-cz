---
title: Nastavení číselných řad pomocí průvodce
description: Číselné řady slouží ke generování čitelných, jedinečných identifikátorů pro záznamy hlavních dat a záznamy transakcí, které je požadují.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1808ab9240ab291f9d203893a634bd390f16e2e7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "328233"
---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="0e497-103">Nastavení číselných řad pomocí průvodce</span><span class="sxs-lookup"><span data-stu-id="0e497-103">Set up number sequences by using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e497-104">Číselné řady slouží ke generování čitelných, jedinečných identifikátorů pro záznamy hlavních dat a záznamy transakcí, které je požadují.</span><span class="sxs-lookup"><span data-stu-id="0e497-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="0e497-105">Hlavní záznam dat nebo transakce, která vyžaduje identifikátor, je označován jako odkaz.</span><span class="sxs-lookup"><span data-stu-id="0e497-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="0e497-106">Než bude možné vytvořit nové záznamy pro odkaz, musíte nastavit číselné řady a spojit je s odkazem.</span><span class="sxs-lookup"><span data-stu-id="0e497-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="0e497-107">Tento postup popisuje, jak nastavit všechny požadované číselné řady současně pomocí průvodce.</span><span class="sxs-lookup"><span data-stu-id="0e497-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="0e497-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="0e497-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="0e497-109">Přejděte na Správa organizace > Číselné řady > Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="0e497-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="0e497-110">Klepněte na tlačítko Generovat.</span><span class="sxs-lookup"><span data-stu-id="0e497-110">Click Generate.</span></span>
3. <span data-ttu-id="0e497-111">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="0e497-111">Click Next.</span></span>
    * <span data-ttu-id="0e497-112">Na této stránce můžete upravit identifikační kód, nejnižší hodnotu a nejvyšší hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0e497-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="0e497-113">Kromě toho můžete určit, zda musí být číselné řady souvislé.</span><span class="sxs-lookup"><span data-stu-id="0e497-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="0e497-114">Nevybírejte možnost Souvislá, pokud musíte předem přidělit čísla pro číselnou řadu.</span><span class="sxs-lookup"><span data-stu-id="0e497-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="0e497-115">Chcete-li přidat rozsah segmentu do formátu číselné řady, vyberte formát v seznamu a potom klikněte na možnost Zahrnout obor do formátu.</span><span class="sxs-lookup"><span data-stu-id="0e497-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="0e497-116">Chcete-li odebrat rozsah segmentu z formátu číselné řady, vyberte formát v seznamu a potom klikněte na možnost Odebrat obor z formátu.</span><span class="sxs-lookup"><span data-stu-id="0e497-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="0e497-117">Chcete-li vyloučit číselnou řadu z automatického generování, vyberte číselnou řadu v seznamu a potom klikněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="0e497-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="0e497-118">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="0e497-118">Click Next.</span></span>
5. <span data-ttu-id="0e497-119">Klepněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="0e497-119">Click Finish.</span></span>


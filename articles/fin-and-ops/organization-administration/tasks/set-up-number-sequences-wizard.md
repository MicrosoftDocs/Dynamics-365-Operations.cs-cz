--- 
title: "Nastavení číselných řad pomocí průvodce"
description: "Číselné řady slouží ke generování čitelných, jedinečných identifikátorů pro záznamy hlavních dat a záznamy transakcí, které je požadují."
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e8f3227f231ffc287bd6ea6204ed50f8b684e5fb
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="1dc08-103">Nastavení číselných řad pomocí průvodce</span><span class="sxs-lookup"><span data-stu-id="1dc08-103">Set up number sequences by using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1dc08-104">Číselné řady slouží ke generování čitelných, jedinečných identifikátorů pro záznamy hlavních dat a záznamy transakcí, které je požadují.</span><span class="sxs-lookup"><span data-stu-id="1dc08-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="1dc08-105">Hlavní záznam dat nebo transakce, která vyžaduje identifikátor, je označován jako odkaz.</span><span class="sxs-lookup"><span data-stu-id="1dc08-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="1dc08-106">Než bude možné vytvořit nové záznamy pro odkaz, musíte nastavit číselné řady a spojit je s odkazem.</span><span class="sxs-lookup"><span data-stu-id="1dc08-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="1dc08-107">Tento postup popisuje, jak nastavit všechny požadované číselné řady současně pomocí průvodce.</span><span class="sxs-lookup"><span data-stu-id="1dc08-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="1dc08-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="1dc08-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="1dc08-109">Přejděte na Správa organizace > Číselné řady > Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="1dc08-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="1dc08-110">Klepněte na tlačítko Generovat.</span><span class="sxs-lookup"><span data-stu-id="1dc08-110">Click Generate.</span></span>
3. <span data-ttu-id="1dc08-111">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="1dc08-111">Click Next.</span></span>
    * <span data-ttu-id="1dc08-112">Na této stránce můžete upravit identifikační kód, nejnižší hodnotu a nejvyšší hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1dc08-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="1dc08-113">Kromě toho můžete určit, zda musí být číselné řady souvislé.</span><span class="sxs-lookup"><span data-stu-id="1dc08-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="1dc08-114">Nevybírejte možnost Souvislá, pokud musíte předem přidělit čísla pro číselnou řadu.</span><span class="sxs-lookup"><span data-stu-id="1dc08-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="1dc08-115">Chcete-li přidat rozsah segmentu do formátu číselné řady, vyberte formát v seznamu a potom klikněte na možnost Zahrnout obor do formátu.</span><span class="sxs-lookup"><span data-stu-id="1dc08-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="1dc08-116">Chcete-li odebrat rozsah segmentu z formátu číselné řady, vyberte formát v seznamu a potom klikněte na možnost Odebrat obor z formátu.</span><span class="sxs-lookup"><span data-stu-id="1dc08-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="1dc08-117">Chcete-li vyloučit číselnou řadu z automatického generování, vyberte číselnou řadu v seznamu a potom klikněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="1dc08-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="1dc08-118">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="1dc08-118">Click Next.</span></span>
5. <span data-ttu-id="1dc08-119">Klepněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="1dc08-119">Click Finish.</span></span>



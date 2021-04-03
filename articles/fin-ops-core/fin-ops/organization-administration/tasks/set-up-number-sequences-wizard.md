---
title: Nastavení číselných řad pomocí průvodce
description: Toto téma popisuje, jak nastavit všechny požadované číselné řady současně pomocí průvodce.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b79924e2c8d94b5e5e160a123e9b0cde0971fd96
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560476"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="b0735-103">Nastavení číselných řad pomocí průvodce</span><span class="sxs-lookup"><span data-stu-id="b0735-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0735-104">Číselné řady slouží ke generování čitelných, jedinečných identifikátorů pro záznamy hlavních dat a záznamy transakcí, které je požadují.</span><span class="sxs-lookup"><span data-stu-id="b0735-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="b0735-105">Hlavní záznam dat nebo transakce, která vyžaduje identifikátor, je označován jako odkaz.</span><span class="sxs-lookup"><span data-stu-id="b0735-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="b0735-106">Než bude možné vytvořit nové záznamy pro odkaz, musíte nastavit číselné řady a spojit je s odkazem.</span><span class="sxs-lookup"><span data-stu-id="b0735-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="b0735-107">Toto téma popisuje, jak nastavit všechny požadované číselné řady současně pomocí průvodce.</span><span class="sxs-lookup"><span data-stu-id="b0735-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="b0735-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="b0735-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b0735-109">Přejděte na **Navigace > Moduly > Správa organizace > Číselné řady > Číselné řady**.</span><span class="sxs-lookup"><span data-stu-id="b0735-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="b0735-110">Vyberte **Generovat**.</span><span class="sxs-lookup"><span data-stu-id="b0735-110">Select **Generate**.</span></span>
3. <span data-ttu-id="b0735-111">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="b0735-111">Select **Next**.</span></span>

   - <span data-ttu-id="b0735-112">Na této stránce můžete upravit identifikační kód, nejnižší hodnotu a nejvyšší hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0735-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="b0735-113">Kromě toho můžete určit, zda musí být číselné řady souvislé.</span><span class="sxs-lookup"><span data-stu-id="b0735-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="b0735-114">Nevybírejte možnost **Souvislá**, pokud musíte předem přidělit čísla pro číselnou řadu.</span><span class="sxs-lookup"><span data-stu-id="b0735-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="b0735-115">Chcete-li přidat rozsah segmentu do formátu číselné řady, vyberte formát v seznamu a potom klikněte na možnost **Zahrnout obor do formátu**.</span><span class="sxs-lookup"><span data-stu-id="b0735-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="b0735-116">Chcete-li odebrat rozsah segmentu z formátu číselné řady, vyberte formát v seznamu a potom vyberte možnost **Odebrat obor z formátu**.</span><span class="sxs-lookup"><span data-stu-id="b0735-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="b0735-117">Chcete-li vyloučit číselnou řadu z automatického generování, vyberte číselnou řadu v seznamu a potom vyberte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="b0735-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="b0735-118">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="b0735-118">Select **Next**.</span></span>
5. <span data-ttu-id="b0735-119">Vyberte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="b0735-119">Select **Finish**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
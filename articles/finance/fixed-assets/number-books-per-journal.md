---
title: Počet knih na deník
description: Toto téma popisuje vztah mezi deníky a knihami majetku, když vytvoříte návrh na pořízení nebo odpis dlouhodobého majetku prostřednictvím dávkové úlohy. Můžete definovat maximální počet knih, které jsou zahrnuty pro každou akvizici a pro odpisy.
author: moaamer
manager: Ann Beebe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d4ba98cefdc0b555eedfaa56b6a3ca4870b5de93
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650650"
---
# <a name="number-of-books-per-journal"></a><span data-ttu-id="fb4de-104">Počet knih na deník</span><span class="sxs-lookup"><span data-stu-id="fb4de-104">Number of books per journal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb4de-105">Toto téma popisuje vztah mezi deníky a knihami majetku, když vytvoříte návrh na pořízení nebo odpis dlouhodobého majetku prostřednictvím dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="fb4de-105">This topic describes the relationship between journals and asset books when you create a fixed asset acquisition or depreciation proposal through a batch job.</span></span> <span data-ttu-id="fb4de-106">Můžete definovat maximální počet knih, které jsou zahrnuty pro každou akvizici a pro odpisy pomocí polí v části **Počet knih na deník** na kartě **Obecné** na stránce **Parametry dlouhodobého majetku** (**Dlouhodobý majetek \> Nastavení \> Parametry dlouhodobého majetku**).</span><span class="sxs-lookup"><span data-stu-id="fb4de-106">You can define the maximum number of books that are included for each acquisition and for depreciation by using the fields in the **Number of books per journal** section on the **General** tab of the **Fixed assets parameters** page (**Fixed assets \> Setup \> Fixed assets parameters**).</span></span> <span data-ttu-id="fb4de-107">Tato pole vám umožňují rozdělit počet knih majetku do deníku pořízení a deníku odpisů.</span><span class="sxs-lookup"><span data-stu-id="fb4de-107">These fields let you distribute the number of asset books per acquisition journal and depreciation journal.</span></span>

<span data-ttu-id="fb4de-108">U akvizičního návrhu je výchozí hodnota alespoň 10 000 knih.</span><span class="sxs-lookup"><span data-stu-id="fb4de-108">For an acquisition proposal, the default value is at least 10,000 books.</span></span> <span data-ttu-id="fb4de-109">U návrhu odpisů je výchozí hodnota alespoň 2 000 knih.</span><span class="sxs-lookup"><span data-stu-id="fb4de-109">For a depreciation proposal, the default value is at least 2,000 books.</span></span>

<span data-ttu-id="fb4de-110">Například pokud existuje 4 000 položek dlouhodobého majetku a ke každému majetku jsou přidruženy dvě knihy, jedna kniha bude zaúčtována do aktuální vrstvy a druhá kniha bude zaúčtována do daňové vrstvy.</span><span class="sxs-lookup"><span data-stu-id="fb4de-110">For example, if there are 4,000 fixed assets, and two books are associated with each asset, one book will be posted to the current layer, and the other book will be posted to the tax layer.</span></span> <span data-ttu-id="fb4de-111">Pokud získáte 4 000 položek dlouhodobého majetku prostřednictvím dávkového zpracování, bude dávková úloha, která vytvoří jeden deník pořízení dlouhodobého majetku, obsahovat 4 000 knih majetku.</span><span class="sxs-lookup"><span data-stu-id="fb4de-111">If you acquire 4,000 fixed assets through batch processing, the batch job that creates one fixed asset acquisition journal will contain 4,000 asset books.</span></span>

> [!NOTE]
> <span data-ttu-id="fb4de-112">Vytvořený deník se bude používat až do dokončení dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="fb4de-112">The journal that is created will continue to be used until the batch job is completed.</span></span>
>
> <span data-ttu-id="fb4de-113">Odvozené knihy nejsou zahrnuty do maximálního počtu knih v deníku.</span><span class="sxs-lookup"><span data-stu-id="fb4de-113">The derived books aren't included in the maximum number of books per journal.</span></span>

<span data-ttu-id="fb4de-114">Dávkové zpracování můžete použít ke spuštění odpisů pro stejnou sadu pořízeného majetku.</span><span class="sxs-lookup"><span data-stu-id="fb4de-114">You can use  batch processing to run depreciation for the same set of acquired assets.</span></span> <span data-ttu-id="fb4de-115">Například dávková úloha vytvoří dva odpisové deníky, z nichž každý obsahuje 2 000 knih majetku.</span><span class="sxs-lookup"><span data-stu-id="fb4de-115">For example, a batch job creates two depreciation journals, each of which consists of 2,000 asset books.</span></span> <span data-ttu-id="fb4de-116">První deník bude obsahovat knihy spojené s dlouhodobým majetkem, které jsou očíslovány od 1 do 2 000.</span><span class="sxs-lookup"><span data-stu-id="fb4de-116">The first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,000.</span></span> <span data-ttu-id="fb4de-117">Druhý deník bude pak obsahovat knihy spojené s dlouhodobým majetkem, které jsou očíslovány od 2 001 do 4 000.</span><span class="sxs-lookup"><span data-stu-id="fb4de-117">The second journal will then contain books that are associated with the fixed assets that are numbered 2,001 through 4,000.</span></span>

<span data-ttu-id="fb4de-118">Úloha dávkového zpracování vylučuje uzavřené knihy.</span><span class="sxs-lookup"><span data-stu-id="fb4de-118">The batch processing job excludes closed books.</span></span> <span data-ttu-id="fb4de-119">Například v dávkové úloze pro odpisy je uzavřeno 10 z prvních 2 000 knih.</span><span class="sxs-lookup"><span data-stu-id="fb4de-119">For example, in a batch job for depreciation, 10 of the first 2,000 books are closed.</span></span> <span data-ttu-id="fb4de-120">V tomto případě bude první deník obsahovat knihy spojené s dlouhodobým majetkem, které jsou očíslovány od 1 do 2 011.</span><span class="sxs-lookup"><span data-stu-id="fb4de-120">In this case, the first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,011.</span></span> <span data-ttu-id="fb4de-121">Druhý deník bude pak obsahovat knihy spojené s dlouhodobým majetkem, které jsou očíslovány od 2 012 do 4 000.</span><span class="sxs-lookup"><span data-stu-id="fb4de-121">The second journal will then contain books that are associated with the fixed assets that are numbered 2,012 through 4,000.</span></span>

<span data-ttu-id="fb4de-122">Omezení počtu knih se použije, pokud ve stejném deníku neexistují duplicitní ID majetku.</span><span class="sxs-lookup"><span data-stu-id="fb4de-122">The limit on the number of books is applied if duplicate asset IDs don't exist in the same journal.</span></span> <span data-ttu-id="fb4de-123">Pokud je však ID majetku stejné jako ID knihy, lze počet knih v deníku překročit, aby bylo ID majetku ve stejném deníku.</span><span class="sxs-lookup"><span data-stu-id="fb4de-123">However, if the asset ID is the same as the book ID, the number of books per journal can be exceeded to keep the asset ID in the same journal.</span></span>

<span data-ttu-id="fb4de-124">Například existuje 5 001 ID dlouhodobého majetku, ke každému ID dlouhodobého majetku jsou přidruženy tři knihy a každá kniha majetku je zaúčtována do stejné účtovací vrstvy.</span><span class="sxs-lookup"><span data-stu-id="fb4de-124">For example, there are 5,001 fixed asset IDs, three books are associated with each fixed asset ID, and each asset book is posted to the same posting layer.</span></span> <span data-ttu-id="fb4de-125">Spustíte odpisy po tři po sobě jdoucí měsíce bez shrnutí.</span><span class="sxs-lookup"><span data-stu-id="fb4de-125">You run depreciation for three consecutive months, without summarization.</span></span> <span data-ttu-id="fb4de-126">Odpisový deník bude vytvořen pomocí dávkové úlohy a systém vytvoří sedm deníků, které mají 667 ID dlouhodobého majetku a tři knihy pro každé ID dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="fb4de-126">The depreciation journal will be created through a batch job, and the system will create seven journals that have 667 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="fb4de-127">Výsledkem bude 2 001 knih.</span><span class="sxs-lookup"><span data-stu-id="fb4de-127">The result will be 2,001 books.</span></span> <span data-ttu-id="fb4de-128">Proto za tři měsíce bude existovat 6 003 řádků deníku, které udržují stejná ID majetku ve stejném deníku.</span><span class="sxs-lookup"><span data-stu-id="fb4de-128">Therefore, in three months, there will be 6,003 journal lines to maintain the same asset IDs in the same journal.</span></span> <span data-ttu-id="fb4de-129">Systém také vytvoří jeden deník, který má 332 ID dlouhodobého majetku a tři knihy pro každé ID dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="fb4de-129">The system will also create one journal that has 332 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="fb4de-130">Za tři měsíce to bude 2 988 řádků.</span><span class="sxs-lookup"><span data-stu-id="fb4de-130">In three months, there will be 2,988 lines.</span></span>
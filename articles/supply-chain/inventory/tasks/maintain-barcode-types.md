---
title: "Udržování typů čárových kódů"
description: "Tento postup popisuje, jak nastavit novou definici čárového kódu, který lze použít v rámci sestavy seznamu výdejek."
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45323206550d1b0ed66d89f4be7b995c60af63fc
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-bar-code-types"></a><span data-ttu-id="22410-103">Udržování typů čárových kódů</span><span class="sxs-lookup"><span data-stu-id="22410-103">Maintain bar code types</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22410-104">Tento postup popisuje, jak nastavit novou definici čárového kódu, který lze použít v rámci sestavy seznamu výdejek.</span><span class="sxs-lookup"><span data-stu-id="22410-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="22410-105">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="22410-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="22410-106">Pokud používáte USMF, můžete použít ukázkové hodnoty, které jsou zobrazeny.</span><span class="sxs-lookup"><span data-stu-id="22410-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="22410-107">Tyto úkoly obvykle provádějí vedoucí skladu.</span><span class="sxs-lookup"><span data-stu-id="22410-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="22410-108">Přejděte k čárovým kódům.</span><span class="sxs-lookup"><span data-stu-id="22410-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="22410-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="22410-109">Click New.</span></span>
3. <span data-ttu-id="22410-110">Zadejte hodnotu do pole Nastavení čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="22410-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="22410-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="22410-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="22410-112">Vyberte možnost v poli Typ čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="22410-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="22410-113">Pokud používáte data USMF, můžete vybrat „Kód 39“.</span><span class="sxs-lookup"><span data-stu-id="22410-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="22410-114">Do pole Velikost zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="22410-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="22410-115">Zadejte číslo do pole Maximální délka.</span><span class="sxs-lookup"><span data-stu-id="22410-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="22410-116">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="22410-116">Click Save.</span></span>
9. <span data-ttu-id="22410-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="22410-117">Close the page.</span></span>
10. <span data-ttu-id="22410-118">Přejděte do parametrů modulu Řízení zásob a skladu</span><span class="sxs-lookup"><span data-stu-id="22410-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="22410-119">V poli Nastavení čárového kódu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="22410-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="22410-120">Vyberte nastavení čárového kódu, který jste předtím vytvořili, nezapomeňte však, že formát čárového kódu musí odpovídat formátu jedinečného identifikátoru pro typ záznamu používaného v procesu.</span><span class="sxs-lookup"><span data-stu-id="22410-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="22410-121">Například pro postupy výdeje by formát čárového kódu měl odpovídat formátu odkazu postupu výdeje, což je obvykle číselná řada.</span><span class="sxs-lookup"><span data-stu-id="22410-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="22410-122">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="22410-122">Click Save.</span></span>
13. <span data-ttu-id="22410-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="22410-123">Close the page.</span></span>


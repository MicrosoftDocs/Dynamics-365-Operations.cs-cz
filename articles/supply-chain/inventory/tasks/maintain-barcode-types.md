---
title: Údržba typů čárového kódu
description: Tento postup popisuje, jak nastavit novou definici čárového kódu, který lze použít v rámci sestavy seznamu výdejek.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0d7092228f078f528ec1cb9ac56d7034c44bccf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "349692"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="86398-103">Údržba typů čárového kódu</span><span class="sxs-lookup"><span data-stu-id="86398-103">Maintain barcode types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="86398-104">Tento postup popisuje, jak nastavit novou definici čárového kódu, který lze použít v rámci sestavy seznamu výdejek.</span><span class="sxs-lookup"><span data-stu-id="86398-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="86398-105">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="86398-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="86398-106">Pokud používáte USMF, můžete použít ukázkové hodnoty, které jsou zobrazeny.</span><span class="sxs-lookup"><span data-stu-id="86398-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="86398-107">Tyto úkoly obvykle provádějí vedoucí skladu.</span><span class="sxs-lookup"><span data-stu-id="86398-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="86398-108">Přejděte k čárovým kódům.</span><span class="sxs-lookup"><span data-stu-id="86398-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="86398-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="86398-109">Click New.</span></span>
3. <span data-ttu-id="86398-110">Zadejte hodnotu do pole Nastavení čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="86398-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="86398-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="86398-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="86398-112">Vyberte možnost v poli Typ čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="86398-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="86398-113">Pokud používáte data USMF, můžete vybrat „Kód 39“.</span><span class="sxs-lookup"><span data-stu-id="86398-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="86398-114">Do pole Velikost zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="86398-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="86398-115">Zadejte číslo do pole Maximální délka.</span><span class="sxs-lookup"><span data-stu-id="86398-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="86398-116">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="86398-116">Click Save.</span></span>
9. <span data-ttu-id="86398-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="86398-117">Close the page.</span></span>
10. <span data-ttu-id="86398-118">Přejděte do parametrů modulu Řízení zásob a skladu</span><span class="sxs-lookup"><span data-stu-id="86398-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="86398-119">V poli Nastavení čárového kódu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="86398-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="86398-120">Vyberte nastavení čárového kódu, který jste předtím vytvořili, nezapomeňte však, že formát čárového kódu musí odpovídat formátu jedinečného identifikátoru pro typ záznamu používaného v procesu.</span><span class="sxs-lookup"><span data-stu-id="86398-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="86398-121">Například pro postupy výdeje by formát čárového kódu měl odpovídat formátu odkazu postupu výdeje, což je obvykle číselná řada.</span><span class="sxs-lookup"><span data-stu-id="86398-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="86398-122">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="86398-122">Click Save.</span></span>
13. <span data-ttu-id="86398-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="86398-123">Close the page.</span></span>


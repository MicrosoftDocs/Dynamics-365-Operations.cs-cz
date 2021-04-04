---
title: Řešení potíží s optimalizací plánování
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete při práci s optimalizací plánování setkat.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 39583c244f09f54551d560e8b1dd9f1a5a1590cc
ms.sourcegitcommit: 72f70c81176e86cda714a4712525f73514c895b7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/16/2021
ms.locfileid: "5457322"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="1fa69-103">Řešení potíží s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="1fa69-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1fa69-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete při práci s optimalizací plánování setkat.</span><span class="sxs-lookup"><span data-stu-id="1fa69-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="1fa69-105">Instalace doplňku Optimalizace plánování se nedokončuje</span><span class="sxs-lookup"><span data-stu-id="1fa69-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="1fa69-106">Optimalizace plánování vyžaduje povolenou službu Lifecycle Services (LCS), prostředí s vysokou dostupností, vrstvy 2 nebo vyšší (ne prostředí OneBox) s Dynamics 365 Supply Chain Management verze 10.0.7 a novější.</span><span class="sxs-lookup"><span data-stu-id="1fa69-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="1fa69-107">Pokud se pokusíte nainstalovat doplněk v prostředí OneBox, instalace nebude dokončena.</span><span class="sxs-lookup"><span data-stu-id="1fa69-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="1fa69-108">**Oprava**: Zrušte instalaci a použijte prostředí s vysokou dostupností, stupeň 2 nebo vyšší (nikoli prostředí OneBox).</span><span class="sxs-lookup"><span data-stu-id="1fa69-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="1fa69-109">Když je povolena optimalizace plánování, plánování dávkových úloh se nezdaří</span><span class="sxs-lookup"><span data-stu-id="1fa69-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="1fa69-110">Pokud povolíte optimalizaci plánování, vestavěný modul hlavního plánování se automaticky deaktivuje.</span><span class="sxs-lookup"><span data-stu-id="1fa69-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="1fa69-111">Dávkové úlohy hlavního plánování, které byly vytvořeny pro vestavěný plánovací modul Supply Chain Management, selžou, pokud jsou spuštěny při povolené optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="1fa69-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="1fa69-112">Může se zobrazit chybová zpráva, například *Tato operace spustila hlavní plánování, které není podporováno, když je povolena optimalizace plánování*.</span><span class="sxs-lookup"><span data-stu-id="1fa69-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="1fa69-113">**Oprava**: Zrušte všechny dávkové úlohy hlavního plánování, které byly vytvořeny pro vestavěný plánovací modul Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1fa69-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="1fa69-114">Výsledky optimalizace plánování se liší od předchozích výsledků</span><span class="sxs-lookup"><span data-stu-id="1fa69-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="1fa69-115">Optimalizace plánování se v některých oblastech liší od vestavěného hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="1fa69-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="1fa69-116">To může být také způsobeno chystanými funkcemi.</span><span class="sxs-lookup"><span data-stu-id="1fa69-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="1fa69-117">**Oprava**: Spusťte analýzu přizpůsobení optimalizace plánování a poté analyzujte výsledky a porozumění dopadu s odkazem na související dokumentaci.</span><span class="sxs-lookup"><span data-stu-id="1fa69-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="1fa69-118">Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="1fa69-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="1fa69-119">Nelze povolit optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="1fa69-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="1fa69-120">**Stav připojení** musí být **Připojeno** před nastavením možnosti **Použít optimalizaci plánování** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="1fa69-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="1fa69-121">Další informace naleznete v tématu [Začínáme s optimalizací plánování](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="1fa69-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="1fa69-122">**Oprava**: Zkontrolujte, zda byl doplněk optimalizace plánování úspěšně nainstalován.</span><span class="sxs-lookup"><span data-stu-id="1fa69-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="1fa69-123">Během CTP se zobrazí chybová zpráva</span><span class="sxs-lookup"><span data-stu-id="1fa69-123">Error message is shown during CTP</span></span>

<span data-ttu-id="1fa69-124">Pokud se pokusíte spustit příslib na základě ověření dostupné kapacity (CTP) z prodejní objednávky, když je aktivována optimalizace plánování, zobrazí se následující chybová zpráva: *Tato operace spustila hlavní plánování, které není podporováno, když je aktivována optimalizace plánování*.</span><span class="sxs-lookup"><span data-stu-id="1fa69-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="1fa69-125">Souvisí to s čekající funkcí, která je plánována jako součást podpory výrobních zakázek.</span><span class="sxs-lookup"><span data-stu-id="1fa69-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="1fa69-126">**Oprava:** Pokud je aktivována optimalizace plánování, vyhněte se výpočtům CTP, dokud nebude dostupná podpora CTP.</span><span class="sxs-lookup"><span data-stu-id="1fa69-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1fa69-127">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="1fa69-127">Additional resources</span></span>

[<span data-ttu-id="1fa69-128">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="1fa69-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="1fa69-129">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="1fa69-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
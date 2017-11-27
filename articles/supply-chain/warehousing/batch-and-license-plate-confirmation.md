---
title: "Potvrzení dávky a poznávací značky"
description: "Toto téma popisuje, jak nastavit a použít potvrzení dávky a registrační značky z mobilního zařízení."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0444caa0f1cc176153c322b8619db65bd377ddd0
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="ddeb6-103">Potvrzení dávky a poznávací značky</span><span class="sxs-lookup"><span data-stu-id="ddeb6-103">Batch and license plate confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ddeb6-104">Potvrzení dávky vám umožňuje potvrdit z mobilního zařízení, že byla vydána správná dávka.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="ddeb6-105">Při počátečním vyskladnění práce pro dávku pouze nad položkami, kde dávka nad označuje rozsah dávek vyšší než umístění v hierarchii vyhledávání, musíte ověřit, že vyskladněná dávka se shoduje dávkou na řádku práce.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="ddeb6-106">Potvrzení registrační značky vám umožňuje potvrdit z mobilního zařízení, že byla vydána správná registrační značka.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="ddeb6-107">Při vyskladnění práce ze skladového místa fáze musíte ověřit, že vyskladněná registrační značka odpovídá registrační značce, která je přidružena k práci.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="ddeb6-108">Pokud práce začala naskenováním poznávací značky, tento krok potvrzení bude přeskočen.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="ddeb6-109">Kdy se to používá</span><span class="sxs-lookup"><span data-stu-id="ddeb6-109">Where it applies</span></span>
<span data-ttu-id="ddeb6-110">Potvrzení platí v následujících situacích:</span><span class="sxs-lookup"><span data-stu-id="ddeb6-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="ddeb6-111">Potvrzení dávky se týká počátečního vyskladnění práce pro dávku nad položky.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="ddeb6-112">Potvrzení poznávací značky platí pro vyskladnění ze skladových míst fáze.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="ddeb6-113">Nastavení potvrzení dávky a poznávací značky</span><span class="sxs-lookup"><span data-stu-id="ddeb6-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="ddeb6-114">Můžete nakonfigurovat potvrzení dávky a poznávací značky z položek nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="ddeb6-115">Z položek nabídky mobilního zařízení vstupte do nastavení potvrzení práce.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="ddeb6-116">Vyberte možnost pro potvrzení dávky nebo registrační značky.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="ddeb6-117">Obě možnosti jsou k dispozici pro vyskladnění typu práce, které nemají povolené automatické potvrzení.</span><span class="sxs-lookup"><span data-stu-id="ddeb6-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  


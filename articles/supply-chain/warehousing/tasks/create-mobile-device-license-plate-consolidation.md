--- 
title: "Vytvoření položky nabídky na mobilním zařízení pro konsolidaci registračních značek"
description: "Tato procedura ukazuje, jak vytvořit položku nabídky mobilního zařízení pro práci s konsolidací registračních značek."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7b8d20561ff092bd64c17c5d9335e9f54a1d191b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="bc67c-103">Vytvoření položky nabídky na mobilním zařízení pro konsolidaci registračních značek</span><span class="sxs-lookup"><span data-stu-id="bc67c-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc67c-104">Tato procedura ukazuje, jak vytvořit položku nabídky mobilního zařízení pro práci s konsolidací registračních značek.</span><span class="sxs-lookup"><span data-stu-id="bc67c-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="bc67c-105">To umožňuje pracovníkům skladu konsolidovat položky na jednom licenčním štítku s položkami na jiném licenčním štítku ve stejném umístění.</span><span class="sxs-lookup"><span data-stu-id="bc67c-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="bc67c-106">Mohou je použít například v případě, že následující pracovní kroky byly stejné u obou pracovních příkazů, takže je práci potřeba provést jednou pro sloučené položky.</span><span class="sxs-lookup"><span data-stu-id="bc67c-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="bc67c-107">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="bc67c-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="bc67c-108">Tento úkol obvykle provádí vedoucí skladu.</span><span class="sxs-lookup"><span data-stu-id="bc67c-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="bc67c-109">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="bc67c-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="bc67c-110">Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="bc67c-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="bc67c-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bc67c-111">Click New.</span></span>
3. <span data-ttu-id="bc67c-112">Do pole Položky nabídky mobilního zařízení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bc67c-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="bc67c-113">Zadejte hodnotu do pole Titul.</span><span class="sxs-lookup"><span data-stu-id="bc67c-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="bc67c-114">V poli Režim vyberte „Nepřímý“.</span><span class="sxs-lookup"><span data-stu-id="bc67c-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="bc67c-115">V poli Kód aktivity vyberte "Konsolidovat registrační značky".</span><span class="sxs-lookup"><span data-stu-id="bc67c-115">In the Activity code field, select 'Consolidate license plates'.</span></span>



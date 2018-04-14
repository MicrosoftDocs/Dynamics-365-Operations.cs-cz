--- 
title: "Přidání výpočtu do modelu konfigurace produktu"
description: "Tento postup popisuje, jak přidat nový výpočet pro model konfigurace produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 01434e8dbd1e66ae04d0b7910ef2be582297ac84
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="32439-103">Přidání výpočtu do modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="32439-103">Add a calculation to a product configuration model</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32439-104">Tento postup popisuje, jak přidat nový výpočet pro model konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="32439-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="32439-105">Zobrazuje vytvoření logického výrazu za použití operátoru „Jestliže“ k nastavení výšky reproduktoru až 10 pro bílé reproduktory a 15 pro jiné povrchové úpravy skříně.</span><span class="sxs-lookup"><span data-stu-id="32439-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="32439-106">Postup používá komponentu špičkového reproduktoru v ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="32439-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="32439-107">Přidání výpočtu</span><span class="sxs-lookup"><span data-stu-id="32439-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="32439-108">Vytvoření vzorce výpočtu</span><span class="sxs-lookup"><span data-stu-id="32439-108">Create calculation expression</span></span>
1. <span data-ttu-id="32439-109">Klepněte na Upravit výraz.</span><span class="sxs-lookup"><span data-stu-id="32439-109">Click Edit expression.</span></span>
2. <span data-ttu-id="32439-110">Do pole Základ omezení zadejte „Jestliže [Povrchová úprava skříně == „bílá“, 10, 15]“.</span><span class="sxs-lookup"><span data-stu-id="32439-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="32439-111">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="32439-111">Click Validate.</span></span>
4. <span data-ttu-id="32439-112">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="32439-112">Click Close.</span></span>
5. <span data-ttu-id="32439-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="32439-113">Click OK.</span></span>



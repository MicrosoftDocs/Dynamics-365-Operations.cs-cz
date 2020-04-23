---
title: Přidání výpočtu do modelu konfigurace produktu
description: Tento postup popisuje, jak přidat nový výpočet pro model konfigurace produktu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32bc2ac5815c2739147664f1e1df2528178db51e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213393"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="169d1-103">Přidání výpočtu do modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="169d1-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="169d1-104">Tento postup popisuje, jak přidat nový výpočet pro model konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="169d1-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="169d1-105">Zobrazuje vytvoření logického výrazu za použití operátoru „Jestliže“ k nastavení výšky reproduktoru až 10 pro bílé reproduktory a 15 pro jiné povrchové úpravy skříně.</span><span class="sxs-lookup"><span data-stu-id="169d1-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="169d1-106">Postup používá komponentu špičkového reproduktoru v ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="169d1-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="169d1-107">Přidání výpočtu</span><span class="sxs-lookup"><span data-stu-id="169d1-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="169d1-108">Vytvoření vzorce výpočtu</span><span class="sxs-lookup"><span data-stu-id="169d1-108">Create calculation expression</span></span>
1. <span data-ttu-id="169d1-109">Klepněte na Upravit výraz.</span><span class="sxs-lookup"><span data-stu-id="169d1-109">Click Edit expression.</span></span>
2. <span data-ttu-id="169d1-110">Do pole Základ omezení zadejte „Jestliže [Povrchová úprava skříně == „bílá“, 10, 15]“.</span><span class="sxs-lookup"><span data-stu-id="169d1-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="169d1-111">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="169d1-111">Click Validate.</span></span>
4. <span data-ttu-id="169d1-112">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="169d1-112">Click Close.</span></span>
5. <span data-ttu-id="169d1-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="169d1-113">Click OK.</span></span>


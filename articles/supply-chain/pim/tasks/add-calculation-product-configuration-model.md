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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d09a3544631960e3f6b292dbdd8927dd499f07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987047"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="43fff-103">Přidání výpočtu do modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="43fff-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="43fff-104">Tento postup popisuje, jak přidat nový výpočet pro model konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="43fff-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="43fff-105">Zobrazuje vytvoření logického výrazu za použití operátoru „Jestliže“ k nastavení výšky reproduktoru až 10 pro bílé reproduktory a 15 pro jiné povrchové úpravy skříně.</span><span class="sxs-lookup"><span data-stu-id="43fff-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="43fff-106">Postup používá komponentu špičkového reproduktoru v ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="43fff-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="43fff-107">Přidání výpočtu</span><span class="sxs-lookup"><span data-stu-id="43fff-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="43fff-108">Vytvoření vzorce výpočtu</span><span class="sxs-lookup"><span data-stu-id="43fff-108">Create calculation expression</span></span>
1. <span data-ttu-id="43fff-109">Klepněte na Upravit výraz.</span><span class="sxs-lookup"><span data-stu-id="43fff-109">Click Edit expression.</span></span>
2. <span data-ttu-id="43fff-110">Do pole Základ omezení zadejte „Jestliže [Povrchová úprava skříně == „bílá“, 10, 15]“.</span><span class="sxs-lookup"><span data-stu-id="43fff-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="43fff-111">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="43fff-111">Click Validate.</span></span>
4. <span data-ttu-id="43fff-112">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="43fff-112">Click Close.</span></span>
5. <span data-ttu-id="43fff-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="43fff-113">Click OK.</span></span>


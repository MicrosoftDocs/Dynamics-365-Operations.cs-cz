---
title: Přidání omezení výrazu do modelu konfigurace produktu
description: Tento postup popisuje, jak můžete přidat nový výraz omezení pro model konfigurace produktu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81026d8622d3f03b3b87747800f4845cda823569
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256152"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="86dd7-103">Přidání omezení výrazu do modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="86dd7-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86dd7-104">Tento postup popisuje, jak můžete přidat nový výraz omezení pro model konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="86dd7-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="86dd7-105">Ukazuje, jak se můžete vyhlásit, že ochrana rohu musí být uplatněna na reproduktor, pokud uživatel vybral přední mřížkou kovovou.</span><span class="sxs-lookup"><span data-stu-id="86dd7-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="86dd7-106">Postup používá komponentu špičkového reproduktoru v ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="86dd7-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="86dd7-107">Vytvoření omezení výrazu</span><span class="sxs-lookup"><span data-stu-id="86dd7-107">Create an expression constraint</span></span>
1. <span data-ttu-id="86dd7-108">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="86dd7-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="86dd7-109">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="86dd7-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="86dd7-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="86dd7-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="86dd7-111">Tento příklad používá model Špičkového reproduktoru.</span><span class="sxs-lookup"><span data-stu-id="86dd7-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="86dd7-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="86dd7-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="86dd7-113">Rozbalte sekci Omezení.</span><span class="sxs-lookup"><span data-stu-id="86dd7-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="86dd7-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="86dd7-114">Click Add.</span></span>
7. <span data-ttu-id="86dd7-115">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="86dd7-115">Click Create.</span></span>
8. <span data-ttu-id="86dd7-116">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="86dd7-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="86dd7-117">Zadat výraz</span><span class="sxs-lookup"><span data-stu-id="86dd7-117">Enter expression</span></span>
1. <span data-ttu-id="86dd7-118">Klepněte na Upravit výraz.</span><span class="sxs-lookup"><span data-stu-id="86dd7-118">Click Edit expression.</span></span>
    * <span data-ttu-id="86dd7-119">Pokud odemknete uživatelské rozhraní v záznamu úkolů v této fázi, můžete používat IntelliSense a seznam symbolů k vytváření omezení výrazu.</span><span class="sxs-lookup"><span data-stu-id="86dd7-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="86dd7-120">V poli Základ omezení zadejte hodnotu „Implikuje [Přední mřížka == "Kov", Ochrana rohu]“.</span><span class="sxs-lookup"><span data-stu-id="86dd7-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="86dd7-121">Tento logický výraz uvádí: Pokud přední mřížka je kovová, je nutné vybrat možnost ochrany rohu.</span><span class="sxs-lookup"><span data-stu-id="86dd7-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="86dd7-122">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="86dd7-122">Click Validate.</span></span>
    * <span data-ttu-id="86dd7-123">Ověřovací funkce je spuštěna prostřednictvím omezení výrazu a kontroluje chyby syntaxe.</span><span class="sxs-lookup"><span data-stu-id="86dd7-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="86dd7-124">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="86dd7-124">Click Close.</span></span>
5. <span data-ttu-id="86dd7-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="86dd7-125">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
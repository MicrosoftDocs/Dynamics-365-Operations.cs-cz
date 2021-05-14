---
title: Přidání omezení výrazu do modelu konfigurace produktu
description: Tento postup popisuje, jak můžete přidat nový výraz omezení pro model konfigurace produktu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920874"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="d65f3-103">Přidání omezení výrazu do modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="d65f3-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d65f3-104">Tento postup popisuje, jak můžete přidat nový výraz omezení pro model konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="d65f3-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="d65f3-105">Ukazuje, jak se můžete vyhlásit, že ochrana rohu musí být uplatněna na reproduktor, pokud uživatel vybral přední mřížkou kovovou.</span><span class="sxs-lookup"><span data-stu-id="d65f3-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="d65f3-106">Postup používá komponentu špičkového reproduktoru v ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="d65f3-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="d65f3-107">Vytvoření omezení výrazu</span><span class="sxs-lookup"><span data-stu-id="d65f3-107">Create an expression constraint</span></span>

1. <span data-ttu-id="d65f3-108">Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="d65f3-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="d65f3-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d65f3-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d65f3-110">Tento příklad používá model Špičkového reproduktoru.</span><span class="sxs-lookup"><span data-stu-id="d65f3-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="d65f3-111">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d65f3-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="d65f3-112">Rozbalte sekci **Omezení**.</span><span class="sxs-lookup"><span data-stu-id="d65f3-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="d65f3-113">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d65f3-113">Select **Add**.</span></span>
7. <span data-ttu-id="d65f3-114">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="d65f3-114">Select **Create**.</span></span>
8. <span data-ttu-id="d65f3-115">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="d65f3-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="d65f3-116">Zadat výraz</span><span class="sxs-lookup"><span data-stu-id="d65f3-116">Enter expression</span></span>

1. <span data-ttu-id="d65f3-117">Vyberte **Upravit výraz**.</span><span class="sxs-lookup"><span data-stu-id="d65f3-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="d65f3-118">Pokud odemknete uživatelské rozhraní v záznamu úkolů v této fázi, můžete používat IntelliSense a seznam symbolů k vytváření omezení výrazu.</span><span class="sxs-lookup"><span data-stu-id="d65f3-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="d65f3-119">V poli **Základ omezení** zadejte hodnotu „Implies[FrontGrill=="Metal", CornerProtection]“.</span><span class="sxs-lookup"><span data-stu-id="d65f3-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="d65f3-120">Tento logický výraz uvádí: Pokud přední mřížka je kovová, je nutné vybrat možnost ochrany rohu.</span><span class="sxs-lookup"><span data-stu-id="d65f3-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="d65f3-121">Vyberte **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="d65f3-121">Select **Validate**.</span></span>
    * <span data-ttu-id="d65f3-122">Ověřovací funkce je spuštěna prostřednictvím omezení výrazu a kontroluje chyby syntaxe.</span><span class="sxs-lookup"><span data-stu-id="d65f3-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="d65f3-123">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="d65f3-123">Select **Close**.</span></span>
5. <span data-ttu-id="d65f3-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d65f3-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
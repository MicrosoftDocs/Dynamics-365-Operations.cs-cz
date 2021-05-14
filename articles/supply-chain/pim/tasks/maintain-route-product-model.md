---
title: Údržba postupu pro model produktu
description: Spuštění této procedury vyžaduje, aby model konfigurace produktu existoval.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921258"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="941fc-103">Údržba postupu pro model produktu</span><span class="sxs-lookup"><span data-stu-id="941fc-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="941fc-104">Spuštění této procedury vyžaduje, aby model konfigurace produktu existoval.</span><span class="sxs-lookup"><span data-stu-id="941fc-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="941fc-105">Při provádění celým procesem tento postup používá model špičkový model reproduktoru v ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="941fc-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="941fc-106">Přidání postupu operace</span><span class="sxs-lookup"><span data-stu-id="941fc-106">Add a route operation</span></span>

1. <span data-ttu-id="941fc-107">Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="941fc-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="941fc-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="941fc-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="941fc-109">Pro toto cvičení vyberte model špičkového reproduktoru.</span><span class="sxs-lookup"><span data-stu-id="941fc-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="941fc-110">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="941fc-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="941fc-111">Rozbalte sekci **Operace postupu**.</span><span class="sxs-lookup"><span data-stu-id="941fc-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="941fc-112">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="941fc-112">Select **Add**.</span></span>
1. <span data-ttu-id="941fc-113">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="941fc-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="941fc-114">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="941fc-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="941fc-115">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="941fc-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="941fc-116">Zadání podrobností operace postupu</span><span class="sxs-lookup"><span data-stu-id="941fc-116">Enter route operation details</span></span>

1. <span data-ttu-id="941fc-117">Vyberte **Podrobnosti operace trasy**.</span><span class="sxs-lookup"><span data-stu-id="941fc-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="941fc-118">V poli **Operace** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="941fc-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="941fc-119">V poli **Operace č.**</span><span class="sxs-lookup"><span data-stu-id="941fc-119">In the **Oper. No.**</span></span> <span data-ttu-id="941fc-120">zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="941fc-120">field, enter a number.</span></span>
    * <span data-ttu-id="941fc-121">Čísla operace určující pořadí v postupu.</span><span class="sxs-lookup"><span data-stu-id="941fc-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="941fc-122">Každá vlastnost při operaci postupu může získat statickou hodnotu nebo namapování na atribut.</span><span class="sxs-lookup"><span data-stu-id="941fc-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="941fc-123">Mapování na atribut způsobí, že hodnota bude nastavena v rámci konfigurace.</span><span class="sxs-lookup"><span data-stu-id="941fc-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="941fc-124">V poli **Skupina postupů** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="941fc-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="941fc-125">Skupina postupů určuje základní chování pro náklady, spotřebu a nastavení.</span><span class="sxs-lookup"><span data-stu-id="941fc-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="941fc-126">Vyberte kartu **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="941fc-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="941fc-127">Vyberte kartu **Časy**.</span><span class="sxs-lookup"><span data-stu-id="941fc-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="941fc-128">Do pole **Množství procesu** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="941fc-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="941fc-129">Určuje, kolik se zpracuje při jedné operaci.</span><span class="sxs-lookup"><span data-stu-id="941fc-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="941fc-130">Do pole **Hodiny/čas** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="941fc-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="941fc-131">Zadejte časový úsek.</span><span class="sxs-lookup"><span data-stu-id="941fc-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="941fc-132">Zaškrtněte políčko položky **Nastavit**.</span><span class="sxs-lookup"><span data-stu-id="941fc-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="941fc-133">Do pole **Operační čas** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="941fc-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="941fc-134">Určete čas zpracování pro množství, které jste zadali.</span><span class="sxs-lookup"><span data-stu-id="941fc-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="941fc-135">Zvolte kartu **Požadavky na zdroj**.</span><span class="sxs-lookup"><span data-stu-id="941fc-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="941fc-136">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="941fc-136">Select **Add**.</span></span>
1. <span data-ttu-id="941fc-137">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="941fc-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="941fc-138">V poli **Typ požadavku** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="941fc-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="941fc-139">Rozhodněte, zda chcete zadat určité zdroje nebo možností, které musí mít.</span><span class="sxs-lookup"><span data-stu-id="941fc-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="941fc-140">V poli **Požadavek** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="941fc-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="941fc-141">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="941fc-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Udržování kusovníku pro model konfigurace produktu
description: Spuštění této procedury vyžaduje stávající model konfigurace produktu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921310"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="daad5-103">Udržování kusovníku pro model konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="daad5-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="daad5-104">Spuštění této procedury vyžaduje stávající model konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="daad5-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="daad5-105">Model špičkového reproduktoru v ukázkové společnosti USMF slouží k vytváření tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="daad5-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="daad5-106">Přidání řádku kusovníku</span><span class="sxs-lookup"><span data-stu-id="daad5-106">Add a BOM line</span></span>

1. <span data-ttu-id="daad5-107">Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="daad5-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="daad5-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="daad5-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="daad5-109">Pro tuto proceduru vyberte špičkový reproduktor.</span><span class="sxs-lookup"><span data-stu-id="daad5-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="daad5-110">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="daad5-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="daad5-111">Rozbalte sekci **Řádky kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="daad5-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="daad5-112">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="daad5-112">Select **Add**.</span></span>
1. <span data-ttu-id="daad5-113">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="daad5-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="daad5-114">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="daad5-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="daad5-115">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="daad5-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="daad5-116">Přidání podrobností řádku kusovníku</span><span class="sxs-lookup"><span data-stu-id="daad5-116">Add BOM line details</span></span>

1. <span data-ttu-id="daad5-117">Vyberte **Podrobnosti řádku kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="daad5-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="daad5-118">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="daad5-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="daad5-119">Můžete vybrat zboží M0055.</span><span class="sxs-lookup"><span data-stu-id="daad5-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="daad5-120">Pro každou vlastnost řádku kusovníku můžete vybrat, zda to je pevná hodnota, nebo je mapována k atributu.</span><span class="sxs-lookup"><span data-stu-id="daad5-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="daad5-121">Zaškrtněte políčko položky **Nastavit**.</span><span class="sxs-lookup"><span data-stu-id="daad5-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="daad5-122">Vyberte možnost *Ano* v poli **Výpočet**.</span><span class="sxs-lookup"><span data-stu-id="daad5-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="daad5-123">Nastavení vlastností **Výpočet** na hodnotu *Ano* zajišťuje, že řádek kusovníku bude součástí výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="daad5-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="daad5-124">Vyberte kartu **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="daad5-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="daad5-125">Zaškrtněte políčko položky **Nastavit**.</span><span class="sxs-lookup"><span data-stu-id="daad5-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="daad5-126">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="daad5-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="daad5-127">Pole množství určuje množství zboží, které bude zahrnuto v kusovníku.</span><span class="sxs-lookup"><span data-stu-id="daad5-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="daad5-128">Může se jednat o zřejmého uchazeče pro mapování atributů.</span><span class="sxs-lookup"><span data-stu-id="daad5-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="daad5-129">Vyberte karu **Dimenze**.</span><span class="sxs-lookup"><span data-stu-id="daad5-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="daad5-130">Ověřte, zda některá z dimenzí produktu je aktivní, a proto se hodnota nebo atribut musí přiřadit.</span><span class="sxs-lookup"><span data-stu-id="daad5-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="daad5-131">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="daad5-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Udržování kusovníku pro model konfigurace produktu
description: Spuštění této procedury vyžaduje stávající model konfigurace produktu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457aa5720919d8455a3099b200980bb36f60577f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "342378"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="de59a-103">Udržování kusovníku pro model konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="de59a-103">Maintain BOM for a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="de59a-104">Spuštění této procedury vyžaduje stávající model konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="de59a-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="de59a-105">Model špičkového reproduktoru v ukázkové společnosti USMF slouží k vytváření tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="de59a-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="de59a-106">Přidání řádku kusovníku</span><span class="sxs-lookup"><span data-stu-id="de59a-106">Add a BOM line</span></span>
1. <span data-ttu-id="de59a-107">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="de59a-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="de59a-108">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="de59a-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="de59a-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="de59a-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="de59a-110">Pro tuto proceduru vyberte špičkový reproduktor.</span><span class="sxs-lookup"><span data-stu-id="de59a-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="de59a-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="de59a-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="de59a-112">Rozbalte sekci Řádky kusovníku.</span><span class="sxs-lookup"><span data-stu-id="de59a-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="de59a-113">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="de59a-113">Click Add.</span></span>
7. <span data-ttu-id="de59a-114">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="de59a-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="de59a-115">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="de59a-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="de59a-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="de59a-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="de59a-117">Přidání podrobností řádku kusovníku</span><span class="sxs-lookup"><span data-stu-id="de59a-117">Add BOM line details</span></span>
1. <span data-ttu-id="de59a-118">Klepněte na podrobnosti řádku kusovníku.</span><span class="sxs-lookup"><span data-stu-id="de59a-118">Click BOM line details.</span></span>
2. <span data-ttu-id="de59a-119">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="de59a-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="de59a-120">Můžete vybrat zboží M0055.</span><span class="sxs-lookup"><span data-stu-id="de59a-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="de59a-121">Pro každou vlastnost řádku kusovníku můžete vybrat, zda to je pevná hodnota, nebo je mapována k atributu.</span><span class="sxs-lookup"><span data-stu-id="de59a-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="de59a-122">Zaškrtněte políčko položky Nastavit.</span><span class="sxs-lookup"><span data-stu-id="de59a-122">Select the Set check box.</span></span>
4. <span data-ttu-id="de59a-123">Vyberte možnost Ano v poli Výpočet.</span><span class="sxs-lookup"><span data-stu-id="de59a-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="de59a-124">Nastavení vlastností výpočtu na hodnotu Ano zajišťuje, že řádek kusovníku bude součástí výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="de59a-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="de59a-125">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="de59a-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="de59a-126">Zaškrtněte políčko položky Nastavit.</span><span class="sxs-lookup"><span data-stu-id="de59a-126">Select the Set check box.</span></span>
7. <span data-ttu-id="de59a-127">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="de59a-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="de59a-128">Pole množství určuje množství zboží, které bude zahrnuto v kusovníku.</span><span class="sxs-lookup"><span data-stu-id="de59a-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="de59a-129">Může se jednat o zřejmého uchazeče pro mapování atributů.</span><span class="sxs-lookup"><span data-stu-id="de59a-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="de59a-130">Klepněte na kartu Dimenze.</span><span class="sxs-lookup"><span data-stu-id="de59a-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="de59a-131">Ověřte, zda některá z dimenzí produktu je aktivní, a proto se hodnota nebo atribut musí přiřadit.</span><span class="sxs-lookup"><span data-stu-id="de59a-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="de59a-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="de59a-132">Click OK.</span></span>


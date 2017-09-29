--- 
title: "Udržování kusovníku pro model konfigurace produktu"
description: "Spuštění této procedury vyžaduje stávající model konfigurace produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: c017d7719ac6af43b0c8a162080bb753587df030
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="2654b-103">Udržování kusovníku pro model konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="2654b-103">Maintain BOM for a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2654b-104">Spuštění této procedury vyžaduje stávající model konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="2654b-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="2654b-105">Model špičkového reproduktoru v ukázkové společnosti USMF slouží k vytváření tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="2654b-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="2654b-106">Přidání řádku kusovníku</span><span class="sxs-lookup"><span data-stu-id="2654b-106">Add a BOM line</span></span>
1. <span data-ttu-id="2654b-107">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="2654b-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="2654b-108">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="2654b-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="2654b-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2654b-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2654b-110">Pro tuto proceduru vyberte špičkový reproduktor.</span><span class="sxs-lookup"><span data-stu-id="2654b-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="2654b-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2654b-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2654b-112">Rozbalte sekci Řádky kusovníku.</span><span class="sxs-lookup"><span data-stu-id="2654b-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="2654b-113">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="2654b-113">Click Add.</span></span>
7. <span data-ttu-id="2654b-114">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="2654b-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="2654b-115">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="2654b-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="2654b-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2654b-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="2654b-117">Přidání podrobností řádku kusovníku</span><span class="sxs-lookup"><span data-stu-id="2654b-117">Add BOM line details</span></span>
1. <span data-ttu-id="2654b-118">Klepněte na podrobnosti řádku kusovníku.</span><span class="sxs-lookup"><span data-stu-id="2654b-118">Click BOM line details.</span></span>
2. <span data-ttu-id="2654b-119">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2654b-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2654b-120">Můžete vybrat zboží M0055.</span><span class="sxs-lookup"><span data-stu-id="2654b-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="2654b-121">Pro každou vlastnost řádku kusovníku můžete vybrat, zda to je pevná hodnota, nebo je mapována k atributu.</span><span class="sxs-lookup"><span data-stu-id="2654b-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="2654b-122">Zaškrtněte políčko položky Nastavit.</span><span class="sxs-lookup"><span data-stu-id="2654b-122">Select the Set check box.</span></span>
4. <span data-ttu-id="2654b-123">Vyberte možnost Ano v poli Výpočet.</span><span class="sxs-lookup"><span data-stu-id="2654b-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="2654b-124">Nastavení vlastností výpočtu na hodnotu Ano zajišťuje, že řádek kusovníku bude součástí výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="2654b-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="2654b-125">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="2654b-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="2654b-126">Zaškrtněte políčko položky Nastavit.</span><span class="sxs-lookup"><span data-stu-id="2654b-126">Select the Set check box.</span></span>
7. <span data-ttu-id="2654b-127">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="2654b-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2654b-128">Pole množství určuje množství zboží, které bude zahrnuto v kusovníku.</span><span class="sxs-lookup"><span data-stu-id="2654b-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="2654b-129">Může se jednat o zřejmého uchazeče pro mapování atributů.</span><span class="sxs-lookup"><span data-stu-id="2654b-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="2654b-130">Klepněte na kartu Dimenze.</span><span class="sxs-lookup"><span data-stu-id="2654b-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="2654b-131">Ověřte, zda některá z dimenzí produktu je aktivní, a proto se hodnota nebo atribut musí přiřadit.</span><span class="sxs-lookup"><span data-stu-id="2654b-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="2654b-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="2654b-132">Click OK.</span></span>



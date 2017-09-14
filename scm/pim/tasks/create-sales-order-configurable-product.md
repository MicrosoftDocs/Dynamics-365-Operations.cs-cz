--- 
title: "Vytvoření prodejní objednávky pro konfigurovatelný produkt"
description: "Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
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
ms.openlocfilehash: 646606237f593d24792a0ae072948f2e12782283
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="0f628-103">Vytvoření prodejní objednávky pro konfigurovatelný produkt</span><span class="sxs-lookup"><span data-stu-id="0f628-103">Create a sales order for a configurable product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f628-104">Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="0f628-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="0f628-105">Tento příklad využívá model reproduktoru D0006 v ukázkové datové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="0f628-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="0f628-106">Zpracovatel prodejních objednávek obvykle používá tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="0f628-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="0f628-107">Vytvořit prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="0f628-107">Create a sales order</span></span>
1. <span data-ttu-id="0f628-108">Klikněte na Zpracování a dotaz na prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="0f628-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="0f628-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0f628-109">Click New.</span></span>
3. <span data-ttu-id="0f628-110">Klikněte na Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="0f628-110">Click Sales order.</span></span>
4. <span data-ttu-id="0f628-111">V poli Účet odběratele vyberte US-001.</span><span class="sxs-lookup"><span data-stu-id="0f628-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="0f628-112">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0f628-112">Click OK.</span></span>
6. <span data-ttu-id="0f628-113">Do pole Číslo položky vyberte „D0006“.</span><span class="sxs-lookup"><span data-stu-id="0f628-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="0f628-114">Pro tento úkol je nutné vybrat konfigurovatelný produkt.</span><span class="sxs-lookup"><span data-stu-id="0f628-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="0f628-115">Klikněte na Produkt a dodávka.</span><span class="sxs-lookup"><span data-stu-id="0f628-115">Click Product and supply.</span></span>
8. <span data-ttu-id="0f628-116">Klikněte na Řádek konfigurace.</span><span class="sxs-lookup"><span data-stu-id="0f628-116">Click Configure line.</span></span>
    * <span data-ttu-id="0f628-117">Všimněte si, že se změnila cena, na základě konfigurace, která byla vybrána, a že pole Zahrnout kabel je nyní nastaveno na hodnotu True.</span><span class="sxs-lookup"><span data-stu-id="0f628-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="0f628-118">Všimněte si výchozí ceny a nastavení, která jsou vybrána pro kabel.</span><span class="sxs-lookup"><span data-stu-id="0f628-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="0f628-119">Klikněte na Šablona nákladu.</span><span class="sxs-lookup"><span data-stu-id="0f628-119">Click Load template.</span></span>
    * <span data-ttu-id="0f628-120">Tento příklad ukazuje, jak lze použít šablonu pro výběr předdefinované konfigurace.</span><span class="sxs-lookup"><span data-stu-id="0f628-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="0f628-121">Pokud používáte tuto proceduru jako průvodce záznamem úloh a chcete zjistit další dostupné hodnoty atributů, musíte klepnout na tlačítko Odemknout.</span><span class="sxs-lookup"><span data-stu-id="0f628-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="0f628-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0f628-122">Click OK.</span></span>
11. <span data-ttu-id="0f628-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0f628-123">Click OK.</span></span>
12. <span data-ttu-id="0f628-124">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="0f628-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="0f628-125">Klepněte na kartu Produkt.</span><span class="sxs-lookup"><span data-stu-id="0f628-125">Click the Product tab.</span></span>
    * <span data-ttu-id="0f628-126">Konfigurace položky je nyní uvedena pod dimenzemi produktu.</span><span class="sxs-lookup"><span data-stu-id="0f628-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="0f628-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0f628-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="0f628-128">Vyberte konfiguraci produktu.</span><span class="sxs-lookup"><span data-stu-id="0f628-128">Select the product configuration</span></span>



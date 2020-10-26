---
title: Vytvoření prodejní objednávky pro konfigurovatelný produkt
description: Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 988d87757019d20dcaf675af925166ed376685f5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985478"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="409c4-103">Vytvoření prodejní objednávky pro konfigurovatelný produkt</span><span class="sxs-lookup"><span data-stu-id="409c4-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="409c4-104">Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="409c4-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="409c4-105">Tento příklad využívá model reproduktoru D0006 v ukázkové datové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="409c4-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="409c4-106">Zpracovatel prodejních objednávek obvykle používá tuto proceduru.</span><span class="sxs-lookup"><span data-stu-id="409c4-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="409c4-107">Vytvořit prodejní objednávku</span><span class="sxs-lookup"><span data-stu-id="409c4-107">Create a sales order</span></span>
1. <span data-ttu-id="409c4-108">Klikněte na Zpracování a dotaz na prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="409c4-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="409c4-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="409c4-109">Click New.</span></span>
3. <span data-ttu-id="409c4-110">Klikněte na Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="409c4-110">Click Sales order.</span></span>
4. <span data-ttu-id="409c4-111">V poli Účet odběratele vyberte US-001.</span><span class="sxs-lookup"><span data-stu-id="409c4-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="409c4-112">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="409c4-112">Click OK.</span></span>
6. <span data-ttu-id="409c4-113">Do pole Číslo položky vyberte „D0006“.</span><span class="sxs-lookup"><span data-stu-id="409c4-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="409c4-114">Pro tento úkol je nutné vybrat konfigurovatelný produkt.</span><span class="sxs-lookup"><span data-stu-id="409c4-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="409c4-115">Klikněte na Produkt a dodávka.</span><span class="sxs-lookup"><span data-stu-id="409c4-115">Click Product and supply.</span></span>
8. <span data-ttu-id="409c4-116">Klikněte na Řádek konfigurace.</span><span class="sxs-lookup"><span data-stu-id="409c4-116">Click Configure line.</span></span>
    * <span data-ttu-id="409c4-117">Všimněte si, že se změnila cena, na základě konfigurace, která byla vybrána, a že pole Zahrnout kabel je nyní nastaveno na hodnotu True.</span><span class="sxs-lookup"><span data-stu-id="409c4-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="409c4-118">Všimněte si výchozí ceny a nastavení, která jsou vybrána pro kabel.</span><span class="sxs-lookup"><span data-stu-id="409c4-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="409c4-119">Klikněte na Šablona nákladu.</span><span class="sxs-lookup"><span data-stu-id="409c4-119">Click Load template.</span></span>
    * <span data-ttu-id="409c4-120">Tento příklad ukazuje, jak lze použít šablonu pro výběr předdefinované konfigurace.</span><span class="sxs-lookup"><span data-stu-id="409c4-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="409c4-121">Pokud používáte tuto proceduru jako průvodce záznamem úloh a chcete zjistit další dostupné hodnoty atributů, musíte klepnout na tlačítko Odemknout.</span><span class="sxs-lookup"><span data-stu-id="409c4-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="409c4-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="409c4-122">Click OK.</span></span>
11. <span data-ttu-id="409c4-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="409c4-123">Click OK.</span></span>
12. <span data-ttu-id="409c4-124">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="409c4-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="409c4-125">Klepněte na kartu Produkt.</span><span class="sxs-lookup"><span data-stu-id="409c4-125">Click the Product tab.</span></span>
    * <span data-ttu-id="409c4-126">Konfigurace položky je nyní uvedena pod dimenzemi produktu.</span><span class="sxs-lookup"><span data-stu-id="409c4-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="409c4-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="409c4-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="409c4-128">Vyberte konfiguraci produktu.</span><span class="sxs-lookup"><span data-stu-id="409c4-128">Select the product configuration</span></span>


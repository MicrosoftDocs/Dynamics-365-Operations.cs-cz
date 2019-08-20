---
title: Vytvoření nového produktu
description: Toto téma popisuje, jak vytvořit nový sdílený produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 722414eee1e738e1438bbb40dbd9b8ca606f9245
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844794"
---
# <a name="create-a-new-product"></a><span data-ttu-id="499a5-103">Vytvoření nového produktu</span><span class="sxs-lookup"><span data-stu-id="499a5-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="499a5-104">Toto téma popisuje, jak vytvořit nový sdílený produkt.</span><span class="sxs-lookup"><span data-stu-id="499a5-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="499a5-105">Obvykle jej má na starost návrhář produktu.</span><span class="sxs-lookup"><span data-stu-id="499a5-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="499a5-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="499a5-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="499a5-107">Vytvoření produktu</span><span class="sxs-lookup"><span data-stu-id="499a5-107">Create a product</span></span>
1. <span data-ttu-id="499a5-108">V navigačním podokně přejděte na **Moduly > Řízení informací o produktech > Produkty > Produkty**.</span><span class="sxs-lookup"><span data-stu-id="499a5-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="499a5-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="499a5-109">Select **New**.</span></span>
3. <span data-ttu-id="499a5-110">Zadejte hodnotu do pole **Číslo produktu**.</span><span class="sxs-lookup"><span data-stu-id="499a5-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="499a5-111">Pokud nebyla číselná řada nastavena pro číslo produktu, musí být zadána ručně.</span><span class="sxs-lookup"><span data-stu-id="499a5-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="499a5-112">Do pole **Název produktu** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="499a5-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="499a5-113">Vyhledávací název je výchozí hodnota pro název produktu.</span><span class="sxs-lookup"><span data-stu-id="499a5-113">The product name defaults to the search name.</span></span> <span data-ttu-id="499a5-114">Tento údaj lze v případě potřeby změnit.</span><span class="sxs-lookup"><span data-stu-id="499a5-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="499a5-115">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="499a5-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="499a5-116">Nastavení skupin dimenzí</span><span class="sxs-lookup"><span data-stu-id="499a5-116">Set up dimension groups</span></span>
1. <span data-ttu-id="499a5-117">Kliknutím na možnost **Skupiny dimenzí** otevřete dialog Zanechat.</span><span class="sxs-lookup"><span data-stu-id="499a5-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="499a5-118">V poli **Skupina dimenze úložiště** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="499a5-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="499a5-119">Skupina dimenze úložiště určuje, které dimenze uskladnění je nutné zadat pro jednotlivé transakce produktu, a jakým způsobem budou sledovány ve skladu.</span><span class="sxs-lookup"><span data-stu-id="499a5-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="499a5-120">V poli **Skupina sledovací dimenze** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="499a5-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="499a5-121">Skupina sledovací dimenze určuje, které sledovací dimenze je nutné zadat pro jednotlivé transakce produktu, a jakým způsobem budou zpracovány ve skladu.</span><span class="sxs-lookup"><span data-stu-id="499a5-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="499a5-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="499a5-122">Select **OK**.</span></span>


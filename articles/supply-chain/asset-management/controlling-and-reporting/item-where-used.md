---
title: Kde byla položka použita
description: Tohle téma popisuje, jak získat přehled o tom, kde se používá položka v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: aa1f00ba6b8259221aa2b1ee460be43ee9a311b2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205457"
---
# <a name="item-where-used"></a><span data-ttu-id="e1a45-103">Kde byla položka použita</span><span class="sxs-lookup"><span data-stu-id="e1a45-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e1a45-104">Můžete provést výpočet pro určitou položku, abyste získali přehled o tom, kde je použita položka v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="e1a45-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="e1a45-105">Ve výsledcích se zobrazuje kontext, ve kterém byla položka použita během její životnosti.</span><span class="sxs-lookup"><span data-stu-id="e1a45-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="e1a45-106">Stránku **Kde byla položka použita** lze otevřít z hlavní nabídky modulu Správa majetku a lze ji také otevřít z následujících stránek:</span><span class="sxs-lookup"><span data-stu-id="e1a45-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="e1a45-107">Kusovníky majetku</span><span class="sxs-lookup"><span data-stu-id="e1a45-107">Asset BOMs</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="e1a45-108">Náhradní díly ve výchozích nastaveních typu majetku</span><span class="sxs-lookup"><span data-stu-id="e1a45-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [<span data-ttu-id="e1a45-109">Kategorie typů práce údržby, typy práce údržby , varianty typů práce údržby, obory práce údržby a kontrolní seznamy údržby</span><span class="sxs-lookup"><span data-stu-id="e1a45-109">Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="e1a45-110">Prognóza údržby</span><span class="sxs-lookup"><span data-stu-id="e1a45-110">Maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="e1a45-111">Zásobování</span><span class="sxs-lookup"><span data-stu-id="e1a45-111">Procurement</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="e1a45-112">Nákup pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="e1a45-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="e1a45-113">Provedení výpočtu místa použití položky</span><span class="sxs-lookup"><span data-stu-id="e1a45-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="e1a45-114">Klikněte na možnosti **Správa majetku** > **Dotazy** > **Kde byla položka použita** nebo vyberte tlačítko **Kde byla položka použita** na jedné z výše uvedených stránek.</span><span class="sxs-lookup"><span data-stu-id="e1a45-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="e1a45-115">V dialogovém okně **Kde byla položka použita** vyberte položku, pro kterou chcete provést výpočet v poli **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="e1a45-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="e1a45-116">V poli **Úroveň** určete, jak detailní mají být řádky položky v případě funkčních míst.</span><span class="sxs-lookup"><span data-stu-id="e1a45-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="e1a45-117">Pokud například do pole zadáte číslo „1“ a struktura funkčního místa má více úrovní, všechny řádky položek pro funkční místo budou zobrazeny na nejvyšší úrovni.</span><span class="sxs-lookup"><span data-stu-id="e1a45-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="e1a45-118">Proto mohou být vztah/množství na řádku přidány z funkčních míst na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="e1a45-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="e1a45-119">Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky položky na všech úrovních funkčních míst, ke kterým se vztahují.</span><span class="sxs-lookup"><span data-stu-id="e1a45-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="e1a45-120">V oddílu **Zahrnout** vyberte možnost „Ano“ u přepínacích tlačítek, která chcete zahrnout do výpočtu.</span><span class="sxs-lookup"><span data-stu-id="e1a45-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="e1a45-121">Výpočet zahájíte klepnutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1a45-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="e1a45-122">Na kartě **Kde byla položka použita** zvolte tlačítka **> Seskupit podle** pro zobrazení požadované úrovně podrobností výpočtu.</span><span class="sxs-lookup"><span data-stu-id="e1a45-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="e1a45-123">Vybraná tlačítka **Seskupit podle** jsou zvýrazněna.</span><span class="sxs-lookup"><span data-stu-id="e1a45-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="e1a45-124">Kliknutím na tlačítko jej aktivujte nebo deaktivujte.</span><span class="sxs-lookup"><span data-stu-id="e1a45-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="e1a45-125">Chcete-li zobrazit dimenze související s danou položkou, klikněte na možnost **Zobrazit dimenze** a vyberte dimenze, které mají být zobrazeny.</span><span class="sxs-lookup"><span data-stu-id="e1a45-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="e1a45-126">Příklad</span><span class="sxs-lookup"><span data-stu-id="e1a45-126">Example</span></span>

<span data-ttu-id="e1a45-127">Na níže uvedeném snímku obrazovky je zobrazen příklad výpočtu použitého pro položku s číslem položky „1000“.</span><span class="sxs-lookup"><span data-stu-id="e1a45-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Příklad výpočtu místa použití položky](media/12-controlling-and-reporting.png)


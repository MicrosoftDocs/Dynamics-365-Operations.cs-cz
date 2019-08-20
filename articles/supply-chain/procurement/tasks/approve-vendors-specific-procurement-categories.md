---
title: Schválení dodavatelů pro konkrétní kategorie zásobování
description: Při vytvoření nákupního požadavku může být existovat požadavek vybrat schválené nebo upřednostňované dodavatele v závislosti na tom, jak jsou zásady nákupu nastaveny.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eec50e2e8f08fabb64f89c17159b97ba770026f8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836329"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="e25a4-103">Schválení dodavatelů pro konkrétní kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="e25a4-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e25a4-104">Při vytvoření nákupního požadavku může být existovat požadavek vybrat schválené nebo upřednostňované dodavatele v závislosti na tom, jak jsou zásady nákupu nastaveny.</span><span class="sxs-lookup"><span data-stu-id="e25a4-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="e25a4-105">Tento postup popisuje, jak určit, že je dodavatel schválený nebo upřednostňovaný pro specifickou kategorii zásobování.</span><span class="sxs-lookup"><span data-stu-id="e25a4-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="e25a4-106">Tento úkol by obvykle prováděl zásobovací pracovník.</span><span class="sxs-lookup"><span data-stu-id="e25a4-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="e25a4-107">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e25a4-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="e25a4-108">Přejděte na Zásobování a zdroje > Dodavatelé > Všichni dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="e25a4-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="e25a4-109">Vyberte dodavatele, kterého chcete nastavit jako schváleného nebo upřednostňovaného dodavatele pro kategorii.</span><span class="sxs-lookup"><span data-stu-id="e25a4-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="e25a4-110">V podokně akcí klikněte na položku Obecné.</span><span class="sxs-lookup"><span data-stu-id="e25a4-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="e25a4-111">Klikněte na Kategorie.</span><span class="sxs-lookup"><span data-stu-id="e25a4-111">Click Categories.</span></span>
5. <span data-ttu-id="e25a4-112">Klikněte na Přidat kategorii.</span><span class="sxs-lookup"><span data-stu-id="e25a4-112">Click Add category.</span></span>
6. <span data-ttu-id="e25a4-113">V poli Kategorie zaškrtněte KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ.</span><span class="sxs-lookup"><span data-stu-id="e25a4-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="e25a4-114">V poli Stav kategorie dodavatele vyberte „Upřednostňované“.</span><span class="sxs-lookup"><span data-stu-id="e25a4-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="e25a4-115">Je možné zadat více než jednoho upřednostněného dodavatele pro kategorii.</span><span class="sxs-lookup"><span data-stu-id="e25a4-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="e25a4-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e25a4-116">Click Save.</span></span>
9. <span data-ttu-id="e25a4-117">Přejděte do nabídky Zásobování a zdroje > Kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="e25a4-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="e25a4-118">Ve stromovém zobrazení vyberte “KATEGORIE ZÁSOBOVÁNÍ SPOLEČNOSTI\KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ“.</span><span class="sxs-lookup"><span data-stu-id="e25a4-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="e25a4-119">Rozbalte sekci Dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="e25a4-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="e25a4-120">Zkontrolujte, zda se vámi vybraný dodavatel zobrazí jako upřednostněný dodavatel pro kategorii Kancelářské a stolní příslušenství.</span><span class="sxs-lookup"><span data-stu-id="e25a4-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="e25a4-121">Pokud tento postup používáte jako průvodce úkolem, může být nutné kliknutím na tlačítko Odemknout umožnit procházení seznamem dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="e25a4-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="e25a4-122">Také je možné přidat upřednostňované a schválené dodavatele na této stránce.</span><span class="sxs-lookup"><span data-stu-id="e25a4-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="e25a4-123">Ve stromu rozbalte KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ.</span><span class="sxs-lookup"><span data-stu-id="e25a4-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="e25a4-124">Ve stromu vyberte Nůžky.</span><span class="sxs-lookup"><span data-stu-id="e25a4-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="e25a4-125">Vyberte Ne v poli Zdědit dodavatele z nadřazené kategorie:.</span><span class="sxs-lookup"><span data-stu-id="e25a4-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="e25a4-126">Vyberte Ano v poli Zdědit dodavatele z nadřazené kategorie:.</span><span class="sxs-lookup"><span data-stu-id="e25a4-126">Select Yes in the Inherit vendors from parent category: field.</span></span>


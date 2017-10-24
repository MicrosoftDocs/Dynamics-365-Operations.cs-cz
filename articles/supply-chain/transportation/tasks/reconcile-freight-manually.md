--- 
title: "Ruční odsouhlasení dopravného"
description: "Tato procedura ukazuje, jak ručně odsouhlasit dopravné."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="b11a0-103">Ruční odsouhlasení dopravného</span><span class="sxs-lookup"><span data-stu-id="b11a0-103">Reconcile freight manually</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b11a0-104">Tato procedura ukazuje, jak ručně odsouhlasit dopravné.</span><span class="sxs-lookup"><span data-stu-id="b11a0-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="b11a0-105">To obvykle provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="b11a0-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="b11a0-106">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="b11a0-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="b11a0-107">Výběr nákladu k odsouhlasení</span><span class="sxs-lookup"><span data-stu-id="b11a0-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="b11a0-108">Přejděte do nabídky Správa přepravy > Plánování > Pracovní plocha plánování vytížení.</span><span class="sxs-lookup"><span data-stu-id="b11a0-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="b11a0-109">Zrušte zaškrtnutí políčka Skrýt expedované a přijaté.</span><span class="sxs-lookup"><span data-stu-id="b11a0-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="b11a0-110">V seznamu vyberte náklad s ID 00006.</span><span class="sxs-lookup"><span data-stu-id="b11a0-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="b11a0-111">Vytvoření faktury dopravce</span><span class="sxs-lookup"><span data-stu-id="b11a0-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="b11a0-112">Pokud ručně odsouhlasíte dopravné a neobdrželi jste automaticky faktury dopravce, můžete vytvořit fakturu založenou na účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="b11a0-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="b11a0-113">Klepněte na položku Související informace.</span><span class="sxs-lookup"><span data-stu-id="b11a0-113">Click Related information.</span></span>
2. <span data-ttu-id="b11a0-114">Klikněte na Zobrazit podrobnosti účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="b11a0-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="b11a0-115">Klikněte na Generovat fakturu za dopravné.</span><span class="sxs-lookup"><span data-stu-id="b11a0-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="b11a0-116">Zadejte hodnotu do pole Faktura.</span><span class="sxs-lookup"><span data-stu-id="b11a0-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="b11a0-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b11a0-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="b11a0-118">Odsouhlasení faktury</span><span class="sxs-lookup"><span data-stu-id="b11a0-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="b11a0-119">Odsouhlasení faktury dopravce a účtu dopravného provádíte řádek po řádku.</span><span class="sxs-lookup"><span data-stu-id="b11a0-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="b11a0-120">Klikněte na Spárovat účty dopravného a faktury.</span><span class="sxs-lookup"><span data-stu-id="b11a0-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="b11a0-121">Rozbalte část Podrobnosti faktury.</span><span class="sxs-lookup"><span data-stu-id="b11a0-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="b11a0-122">Rozbalte oddíl Podrobnosti nespárovaného účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="b11a0-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="b11a0-123">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b11a0-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="b11a0-124">Klepněte na tlačítko Spárovat.</span><span class="sxs-lookup"><span data-stu-id="b11a0-124">Click Match.</span></span>
6. <span data-ttu-id="b11a0-125">Rozbalte oddíl Podrobnosti spárovaného účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="b11a0-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="b11a0-126">Odeslat fakturu ke schválení</span><span class="sxs-lookup"><span data-stu-id="b11a0-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="b11a0-127">Klikněte na Odeslat ke schválení.</span><span class="sxs-lookup"><span data-stu-id="b11a0-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="b11a0-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b11a0-128">Close the page.</span></span>
3. <span data-ttu-id="b11a0-129">Zrušte zaškrtnutí políčka Skrytí schváleno.</span><span class="sxs-lookup"><span data-stu-id="b11a0-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="b11a0-130">Klikněte na Deníky faktur dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b11a0-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="b11a0-131">Klepnutím přejdete na odkaz v poli Číslo referenčního deníku.</span><span class="sxs-lookup"><span data-stu-id="b11a0-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="b11a0-132">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="b11a0-132">Click Lines.</span></span>



---
title: Ruční odsouhlasení dopravného
description: Tato procedura ukazuje, jak ručně odsouhlasit dopravné.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8679a729dc17e3ee85468b459da3956a92160ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974053"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="01a3b-103">Ruční odsouhlasení dopravného</span><span class="sxs-lookup"><span data-stu-id="01a3b-103">Reconcile freight manually</span></span>

<span data-ttu-id="01a3b-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="01a3b-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="01a3b-105">Tato procedura ukazuje, jak ručně odsouhlasit dopravné.</span><span class="sxs-lookup"><span data-stu-id="01a3b-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="01a3b-106">To obvykle provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="01a3b-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="01a3b-107">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="01a3b-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="01a3b-108">Výběr nákladu k odsouhlasení</span><span class="sxs-lookup"><span data-stu-id="01a3b-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="01a3b-109">Přejděte do nabídky Správa přepravy > Plánování > Pracovní plocha plánování vytížení.</span><span class="sxs-lookup"><span data-stu-id="01a3b-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="01a3b-110">Zrušte zaškrtnutí políčka Skrýt expedované a přijaté.</span><span class="sxs-lookup"><span data-stu-id="01a3b-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="01a3b-111">V seznamu vyberte náklad s ID 00006.</span><span class="sxs-lookup"><span data-stu-id="01a3b-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="01a3b-112">Vytvoření faktury dopravce</span><span class="sxs-lookup"><span data-stu-id="01a3b-112">Create a carrier invoice</span></span>
<span data-ttu-id="01a3b-113">Pokud ručně odsouhlasíte dopravné a neobdrželi jste automaticky faktury dopravce, můžete vytvořit fakturu založenou na účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="01a3b-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="01a3b-114">Klepněte na položku Související informace.</span><span class="sxs-lookup"><span data-stu-id="01a3b-114">Click Related information.</span></span>
2. <span data-ttu-id="01a3b-115">Klikněte na Zobrazit podrobnosti účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="01a3b-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="01a3b-116">Klikněte na Generovat fakturu za dopravné.</span><span class="sxs-lookup"><span data-stu-id="01a3b-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="01a3b-117">Zadejte hodnotu do pole Faktura.</span><span class="sxs-lookup"><span data-stu-id="01a3b-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="01a3b-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="01a3b-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="01a3b-119">Odsouhlasení faktury</span><span class="sxs-lookup"><span data-stu-id="01a3b-119">Reconcile the invoice</span></span>
<span data-ttu-id="01a3b-120">Odsouhlasení faktury dopravce a účtu dopravného provádíte řádek po řádku.</span><span class="sxs-lookup"><span data-stu-id="01a3b-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="01a3b-121">Klikněte na Spárovat účty dopravného a faktury.</span><span class="sxs-lookup"><span data-stu-id="01a3b-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="01a3b-122">Rozbalte část Podrobnosti faktury.</span><span class="sxs-lookup"><span data-stu-id="01a3b-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="01a3b-123">Rozbalte oddíl Podrobnosti nespárovaného účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="01a3b-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="01a3b-124">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="01a3b-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="01a3b-125">Klepněte na tlačítko Spárovat.</span><span class="sxs-lookup"><span data-stu-id="01a3b-125">Click Match.</span></span>
6. <span data-ttu-id="01a3b-126">Rozbalte oddíl Podrobnosti spárovaného účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="01a3b-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="01a3b-127">Odeslat fakturu ke schválení</span><span class="sxs-lookup"><span data-stu-id="01a3b-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="01a3b-128">Klikněte na Odeslat ke schválení.</span><span class="sxs-lookup"><span data-stu-id="01a3b-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="01a3b-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01a3b-129">Close the page.</span></span>
3. <span data-ttu-id="01a3b-130">Zrušte zaškrtnutí políčka Skrytí schváleno.</span><span class="sxs-lookup"><span data-stu-id="01a3b-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="01a3b-131">Klikněte na Deníky faktur dodavatele.</span><span class="sxs-lookup"><span data-stu-id="01a3b-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="01a3b-132">Klepnutím přejdete na odkaz v poli Číslo referenčního deníku.</span><span class="sxs-lookup"><span data-stu-id="01a3b-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="01a3b-133">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="01a3b-133">Click Lines.</span></span>


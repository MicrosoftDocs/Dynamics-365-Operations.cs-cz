---
title: Ruční odsouhlasení dopravného
description: Tato procedura ukazuje, jak ručně odsouhlasit dopravné.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a0a5450697a09e5e54e74b35b2576eb6bbd4cdf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838507"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="07c92-103">Ruční odsouhlasení dopravného</span><span class="sxs-lookup"><span data-stu-id="07c92-103">Reconcile freight manually</span></span>

<span data-ttu-id="07c92-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="07c92-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="07c92-105">Tato procedura ukazuje, jak ručně odsouhlasit dopravné.</span><span class="sxs-lookup"><span data-stu-id="07c92-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="07c92-106">To obvykle provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="07c92-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="07c92-107">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="07c92-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="07c92-108">Výběr nákladu k odsouhlasení</span><span class="sxs-lookup"><span data-stu-id="07c92-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="07c92-109">Přejděte do nabídky Správa přepravy > Plánování > Pracovní plocha plánování vytížení.</span><span class="sxs-lookup"><span data-stu-id="07c92-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="07c92-110">Zrušte zaškrtnutí políčka Skrýt expedované a přijaté.</span><span class="sxs-lookup"><span data-stu-id="07c92-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="07c92-111">V seznamu vyberte náklad s ID 00006.</span><span class="sxs-lookup"><span data-stu-id="07c92-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="07c92-112">Vytvoření faktury dopravce</span><span class="sxs-lookup"><span data-stu-id="07c92-112">Create a carrier invoice</span></span>
<span data-ttu-id="07c92-113">Pokud ručně odsouhlasíte dopravné a neobdrželi jste automaticky faktury dopravce, můžete vytvořit fakturu založenou na účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="07c92-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="07c92-114">Klepněte na položku Související informace.</span><span class="sxs-lookup"><span data-stu-id="07c92-114">Click Related information.</span></span>
2. <span data-ttu-id="07c92-115">Klikněte na Zobrazit podrobnosti účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="07c92-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="07c92-116">Klikněte na Generovat fakturu za dopravné.</span><span class="sxs-lookup"><span data-stu-id="07c92-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="07c92-117">Zadejte hodnotu do pole Faktura.</span><span class="sxs-lookup"><span data-stu-id="07c92-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="07c92-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="07c92-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="07c92-119">Odsouhlasení faktury</span><span class="sxs-lookup"><span data-stu-id="07c92-119">Reconcile the invoice</span></span>
<span data-ttu-id="07c92-120">Odsouhlasení faktury dopravce a účtu dopravného provádíte řádek po řádku.</span><span class="sxs-lookup"><span data-stu-id="07c92-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="07c92-121">Klikněte na Spárovat účty dopravného a faktury.</span><span class="sxs-lookup"><span data-stu-id="07c92-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="07c92-122">Rozbalte část Podrobnosti faktury.</span><span class="sxs-lookup"><span data-stu-id="07c92-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="07c92-123">Rozbalte oddíl Podrobnosti nespárovaného účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="07c92-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="07c92-124">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="07c92-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="07c92-125">Klepněte na tlačítko Spárovat.</span><span class="sxs-lookup"><span data-stu-id="07c92-125">Click Match.</span></span>
6. <span data-ttu-id="07c92-126">Rozbalte oddíl Podrobnosti spárovaného účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="07c92-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="07c92-127">Odeslat fakturu ke schválení</span><span class="sxs-lookup"><span data-stu-id="07c92-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="07c92-128">Klikněte na Odeslat ke schválení.</span><span class="sxs-lookup"><span data-stu-id="07c92-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="07c92-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="07c92-129">Close the page.</span></span>
3. <span data-ttu-id="07c92-130">Zrušte zaškrtnutí políčka Skrytí schváleno.</span><span class="sxs-lookup"><span data-stu-id="07c92-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="07c92-131">Klikněte na Deníky faktur dodavatele.</span><span class="sxs-lookup"><span data-stu-id="07c92-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="07c92-132">Klepnutím přejdete na odkaz v poli Číslo referenčního deníku.</span><span class="sxs-lookup"><span data-stu-id="07c92-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="07c92-133">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="07c92-133">Click Lines.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
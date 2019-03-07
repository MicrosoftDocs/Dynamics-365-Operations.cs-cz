---
title: Zaznamenání faktury dodavatele do deníku faktur
description: Tento průvodce úkolem ukazuje, jak vytvořit záznam faktur dodavatele, které nejsou spojeny s nákupními objednávkami.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "348933"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="43a3a-103">Zaznamenání faktury dodavatele do deníku faktur</span><span class="sxs-lookup"><span data-stu-id="43a3a-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43a3a-104">Tento průvodce úkolem ukazuje, jak vytvořit záznam faktur dodavatele, které nejsou spojeny s nákupními objednávkami.</span><span class="sxs-lookup"><span data-stu-id="43a3a-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="43a3a-105">Mezi příklady tohoto typu faktury patří výdaje pro dodávky nebo služby.</span><span class="sxs-lookup"><span data-stu-id="43a3a-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="43a3a-106">Tento záznam používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="43a3a-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="43a3a-107">Přejděte na Závazky > Pracovní prostory > Záznam faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="43a3a-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="43a3a-108">Klikněte na Nový deník faktur.</span><span class="sxs-lookup"><span data-stu-id="43a3a-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="43a3a-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="43a3a-109">Click New.</span></span>
4. <span data-ttu-id="43a3a-110">V poli Název zadejte název deníku nebo kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="43a3a-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="43a3a-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="43a3a-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="43a3a-112">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="43a3a-112">Click Lines.</span></span>
    * <span data-ttu-id="43a3a-113">V poli Datum zadejte datum zaúčtování, které provede aktualizaci hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="43a3a-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="43a3a-114">V poli Účet vyberte účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="43a3a-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="43a3a-115">Do pole Faktura zadejte číslo faktury.</span><span class="sxs-lookup"><span data-stu-id="43a3a-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="43a3a-116">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="43a3a-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="43a3a-117">V poli Dobropis zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="43a3a-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="43a3a-118">V poli Protiúčet zadejte číslo účtu nebo kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání</span><span class="sxs-lookup"><span data-stu-id="43a3a-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="43a3a-119">Skupina prodejní daně bude používat výchozí údaje z účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="43a3a-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="43a3a-120">Skupina DPH položky bude používat výchozí údaje z hlavního účtu určeného v poli Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="43a3a-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="43a3a-121">Datum splatnosti bude vypočteno na základě platebních podmínek.</span><span class="sxs-lookup"><span data-stu-id="43a3a-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="43a3a-122">Platební sleva bude používat výchozí údaje z účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="43a3a-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="43a3a-123">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="43a3a-123">Click Post.</span></span>
13. <span data-ttu-id="43a3a-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="43a3a-124">Close the page.</span></span>


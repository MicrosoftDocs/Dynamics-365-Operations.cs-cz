---
title: Zaznamenání faktury dodavatele do deníku faktur
description: Tento průvodce úkolem ukazuje, jak vytvořit záznam faktur dodavatele, které nejsou spojeny s nákupními objednávkami.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9f2cbe0c9d1609aa3713776f81bafa396fff301
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645274"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="01180-103">Zaznamenání faktury dodavatele do deníku faktur</span><span class="sxs-lookup"><span data-stu-id="01180-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01180-104">Tento průvodce úkolem ukazuje, jak vytvořit záznam faktur dodavatele, které nejsou spojeny s nákupními objednávkami.</span><span class="sxs-lookup"><span data-stu-id="01180-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="01180-105">Mezi příklady tohoto typu faktury patří výdaje pro dodávky nebo služby.</span><span class="sxs-lookup"><span data-stu-id="01180-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="01180-106">Tento záznam používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="01180-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="01180-107">Přejděte na **Navigační podokno > Moduly > Závazky > Pracovní prostory > Záznam faktury dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="01180-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="01180-108">V **Podokně akcí** klikněte na možnost **Nový deník faktur**.</span><span class="sxs-lookup"><span data-stu-id="01180-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="01180-109">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="01180-109">Click **New**.</span></span>
4. <span data-ttu-id="01180-110">V poli **Název** zadejte název deníku nebo kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="01180-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="01180-111">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="01180-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="01180-112">V **Podokně akcí** klikněte na **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="01180-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="01180-113">V poli **Datum** zadejte datum zaúčtování, které provede aktualizaci hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="01180-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="01180-114">V poli **Účet** vyberte **Účet dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="01180-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="01180-115">Do pole **Faktura** zadejte číslo faktury.</span><span class="sxs-lookup"><span data-stu-id="01180-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="01180-116">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="01180-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="01180-117">V poli **Dobropis** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="01180-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="01180-118">V poli **Protiúčet** zadejte číslo účtu nebo kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání</span><span class="sxs-lookup"><span data-stu-id="01180-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="01180-119">**Skupina prodejní daně** bude používat výchozí údaje z účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="01180-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="01180-120">**Skupina DPH položky** bude používat výchozí údaje z hlavního účtu určeného v poli **Protiúčet**.</span><span class="sxs-lookup"><span data-stu-id="01180-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="01180-121">**Datum splatnosti** bude vypočteno na základě platebních podmínek.</span><span class="sxs-lookup"><span data-stu-id="01180-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="01180-122">**Platební sleva** bude používat výchozí údaje z účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="01180-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="01180-123">Pokud jste povolili workflow deníku faktur dodavatele, klikněte na **Pracovní postup> Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="01180-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="01180-124">Po schválení vašeho odeslání bude datum posunuto na první den následujícího otevřeného období, pokud datum zaúčtování transakce spadá do období, které je pozdrženo nebo uzavřeno pro zaúčtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="01180-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="01180-125">Klikněte na možnost **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="01180-125">Click **Post**.</span></span>
13. <span data-ttu-id="01180-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01180-126">Close the page.</span></span>


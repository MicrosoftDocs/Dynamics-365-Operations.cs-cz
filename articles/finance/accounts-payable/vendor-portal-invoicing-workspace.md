---
title: Pracovní prostor fakturace dodavatelské spolupráce
description: Toto téma vysvětluje, jak můžete zobrazit faktury dodavatele a přijmout faktury z pracovního prostoru spolupráce dodavatele.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a3f4729a8a788f4f5b2b2e9923f515b86590b946
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188801"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="e0e16-103">Pracovní prostor fakturace dodavatelské spolupráce</span><span class="sxs-lookup"><span data-stu-id="e0e16-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0e16-104">Toto téma vysvětluje, jak můžete zobrazit faktury dodavatele a přijmout faktury z pracovního prostoru spolupráce dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e0e16-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="e0e16-105">Pracovní prostor **fakturace dodavatelské spolupráce** lze použít pro zobrazení informace o faktuře dodavatele a odeslání faktur do systému pomocí možností workflowu.</span><span class="sxs-lookup"><span data-stu-id="e0e16-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


## <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="e0e16-106">Pracovní prostor fakturace dodavatelské spolupráce</span><span class="sxs-lookup"><span data-stu-id="e0e16-106">Vendor collaboration invoicing workspace</span></span>

### <a name="summary-tiles"></a><span data-ttu-id="e0e16-107">Dlaždice souhrnu</span><span class="sxs-lookup"><span data-stu-id="e0e16-107">Summary tiles</span></span>

<span data-ttu-id="e0e16-108">Dlaždice **Souhrnu** poskytují přehled o fakturách pro vybraného dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e0e16-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="e0e16-109">Faktury můžete zobrazovat podle jejich stavu.</span><span class="sxs-lookup"><span data-stu-id="e0e16-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="e0e16-110">Návrhy faktur nebyly odeslány do workflowu.</span><span class="sxs-lookup"><span data-stu-id="e0e16-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="e0e16-111">Odeslané ale neschválené faktury jsou ty faktury, které dodavatel odeslal, ale nebyly zaúčtovány v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="e0e16-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="e0e16-112">Schválené ale nezaplacené faktury jsou ty faktury, které byly zaznamenány v aplikaci, ale ještě nebyly zcela zaplaceny.</span><span class="sxs-lookup"><span data-stu-id="e0e16-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="e0e16-113">Zaplacené faktury jsou ty, které byly v aplikaci plně uhrazeny.</span><span class="sxs-lookup"><span data-stu-id="e0e16-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="e0e16-114">Klepnutím na dlaždici otevřete filtrované zobrazení stránky **seznamu faktur**.</span><span class="sxs-lookup"><span data-stu-id="e0e16-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="e0e16-115">Tabulkový seznam</span><span class="sxs-lookup"><span data-stu-id="e0e16-115">Tabular lists</span></span>

<span data-ttu-id="e0e16-116">V oddíle **Tabulkové seznamy** se stav fakturace rozděluje podobným způsobem jako dlaždice souhrnu: návrhy a odeslané ale neschválené seznamy.</span><span class="sxs-lookup"><span data-stu-id="e0e16-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="e0e16-117">Ve stavu návrhu lze fakturu přijmout do workflowu nebo odstranit.</span><span class="sxs-lookup"><span data-stu-id="e0e16-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="e0e16-118">Poslední tabulkový seznam je možnost pro vyhledání faktur.</span><span class="sxs-lookup"><span data-stu-id="e0e16-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="e0e16-119">Při hledání můžete filtrovat, což umožňuje rychlejší vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0e16-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="e0e16-120">Stránka seznamu všech faktur dodavatelů</span><span class="sxs-lookup"><span data-stu-id="e0e16-120">All vendor invoices list page</span></span>

<span data-ttu-id="e0e16-121">Můžete zobrazit všechny zaúčtované a nezaúčtované faktury dodavatele na stránce seznamu **Faktury dodavatelské spolupráce**.</span><span class="sxs-lookup"><span data-stu-id="e0e16-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="e0e16-122">Tuto stránku se seznamem můžete použít, chcete-li zobrazit stav platby faktur.</span><span class="sxs-lookup"><span data-stu-id="e0e16-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="e0e16-123">Stavy plateb zahrnují nezaúčtované, nezaplacené, částečně zaplacené a plně zaplacené.</span><span class="sxs-lookup"><span data-stu-id="e0e16-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="e0e16-124">Vytvořit novou fakturu z nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="e0e16-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="e0e16-125">Novou fakturu dodavatele můžete vytvořit, pokud vyberete akci **Nová** v pracovním prostoru **fakturace dodavatelské spolupráce**.</span><span class="sxs-lookup"><span data-stu-id="e0e16-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="e0e16-126">Číslo nákupní objednávky a číslo faktury musí zadat dodavatel.</span><span class="sxs-lookup"><span data-stu-id="e0e16-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="e0e16-127">Ve výchozím nastavení se všechny řádky z nákupní objednávky dodavatele zobrazí na nové faktuře.</span><span class="sxs-lookup"><span data-stu-id="e0e16-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="e0e16-128">Před odesláním dodavatelské faktury do workflowu lze upravovat informace o množství a nákladech.</span><span class="sxs-lookup"><span data-stu-id="e0e16-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="e0e16-129">Před odesláním můžete k faktuře také připojit soubory, poznámky, obrázky a adresy URL.</span><span class="sxs-lookup"><span data-stu-id="e0e16-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="e0e16-130">Další informace naleznete v tématu [Dodavatelská spolupráce s externími dodavateli](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="e0e16-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Výpočet a úprava DPH na faktuře dodavatele
description: Pokud původní zdrojový dokument zobrazí různé částky daně tak, jak se vypočítají, můžete je upravit před zaúčtováním.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "308913"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="b79bf-103">Výpočet a úprava DPH na faktuře dodavatele</span><span class="sxs-lookup"><span data-stu-id="b79bf-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b79bf-104">Pokud původní zdrojový dokument zobrazí různé částky daně tak, jak se vypočítají, můžete je upravit před zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="b79bf-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="b79bf-105">Tento úkol používá ukázkovou společnost DEMF.</span><span class="sxs-lookup"><span data-stu-id="b79bf-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="b79bf-106">Přejděte na Závazky > Faktury > Deník faktur.</span><span class="sxs-lookup"><span data-stu-id="b79bf-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="b79bf-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b79bf-107">Click New.</span></span>
3. <span data-ttu-id="b79bf-108">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b79bf-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b79bf-109">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b79bf-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b79bf-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b79bf-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b79bf-111">Klikněte na možnost Řádky.</span><span class="sxs-lookup"><span data-stu-id="b79bf-111">Click Lines.</span></span>
7. <span data-ttu-id="b79bf-112">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b79bf-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b79bf-113">Zadejte požadované hodnoty do pole Účet.</span><span class="sxs-lookup"><span data-stu-id="b79bf-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="b79bf-114">Zadejte hodnotu do pole Faktura.</span><span class="sxs-lookup"><span data-stu-id="b79bf-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="b79bf-115">V poli Dobropis zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="b79bf-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="b79bf-116">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="b79bf-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="b79bf-117">Klikněte na DPH.</span><span class="sxs-lookup"><span data-stu-id="b79bf-117">Click Sales tax.</span></span>
13. <span data-ttu-id="b79bf-118">V poli Celková částka skutečné DPH zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="b79bf-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="b79bf-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b79bf-119">Click OK.</span></span>
15. <span data-ttu-id="b79bf-120">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="b79bf-120">Click Save.</span></span>
16. <span data-ttu-id="b79bf-121">Klikněte na DPH.</span><span class="sxs-lookup"><span data-stu-id="b79bf-121">Click Sales tax.</span></span>
17. <span data-ttu-id="b79bf-122">Na kartě Úprava lze upravit částky DPH podle kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="b79bf-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="b79bf-123">Klikněte na Resetovat skutečné částky z vypočítaných částek.</span><span class="sxs-lookup"><span data-stu-id="b79bf-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="b79bf-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b79bf-124">Click OK.</span></span>
20. <span data-ttu-id="b79bf-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b79bf-125">Click Save.</span></span>


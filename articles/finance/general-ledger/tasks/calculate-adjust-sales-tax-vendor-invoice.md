---
title: Výpočet a úprava DPH na faktuře dodavatele
description: V tomto tématu je vysvětleno, jak upravit DPH u faktury dodavatele v aplikaci Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2536e87953267eae13cf3b42c2bd5476fc647c22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994708"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="92dc0-103">Výpočet a úprava DPH na faktuře dodavatele</span><span class="sxs-lookup"><span data-stu-id="92dc0-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92dc0-104">V tomto tématu je vysvětleno, jak upravit DPH u faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="92dc0-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="92dc0-105">Pokud původní zdrojový dokument zobrazí různé částky daně tak, jak se vypočítají, můžete je upravit před zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="92dc0-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="92dc0-106">Tento úkol používá ukázkovou společnost DEMF.</span><span class="sxs-lookup"><span data-stu-id="92dc0-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="92dc0-107">V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Deník faktury**.</span><span class="sxs-lookup"><span data-stu-id="92dc0-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="92dc0-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="92dc0-108">Select **New**.</span></span>
3. <span data-ttu-id="92dc0-109">V poli **Název** nového řádku vyberte některou z možností v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="92dc0-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="92dc0-110">V podokně akcí zvolte **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="92dc0-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="92dc0-111">Zadejte požadované hodnoty do pole **Účet**.</span><span class="sxs-lookup"><span data-stu-id="92dc0-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="92dc0-112">Zadejte hodnotu do pole **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="92dc0-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="92dc0-113">V poli **Dobropis** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="92dc0-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="92dc0-114">Zadejte požadované hodnoty do pole **Protiúčet**.</span><span class="sxs-lookup"><span data-stu-id="92dc0-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="92dc0-115">Vyberte **DPH**.</span><span class="sxs-lookup"><span data-stu-id="92dc0-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="92dc0-116">V poli **Celková částka skutečné DPH** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="92dc0-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="92dc0-117">Na kartě **Úprava** lze upravit částky DPH podle kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="92dc0-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="92dc0-118">Vyberte **Resetovat skutečné částky z vypočítaných částek**.</span><span class="sxs-lookup"><span data-stu-id="92dc0-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="92dc0-119">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="92dc0-119">Select **OK**.</span></span>
14. <span data-ttu-id="92dc0-120">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="92dc0-120">Select **Save**.</span></span>


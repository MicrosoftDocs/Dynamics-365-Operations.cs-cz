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
ms.openlocfilehash: f4d01fe7587e01c04af28be934a235d955455216
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204730"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="ceaaa-103">Výpočet a úprava DPH na faktuře dodavatele</span><span class="sxs-lookup"><span data-stu-id="ceaaa-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ceaaa-104">V tomto tématu je vysvětleno, jak upravit DPH u faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="ceaaa-105">Pokud původní zdrojový dokument zobrazí různé částky daně tak, jak se vypočítají, můžete je upravit před zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="ceaaa-106">Tento úkol používá ukázkovou společnost DEMF.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="ceaaa-107">V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Deník faktury**.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="ceaaa-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-108">Select **New**.</span></span>
3. <span data-ttu-id="ceaaa-109">V poli **Název** nového řádku vyberte některou z možností v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="ceaaa-110">V podokně akcí zvolte **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="ceaaa-111">Zadejte požadované hodnoty do pole **Účet**.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="ceaaa-112">Zadejte hodnotu do pole **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="ceaaa-113">V poli **Dobropis** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="ceaaa-114">Zadejte požadované hodnoty do pole **Protiúčet**.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="ceaaa-115">Vyberte **DPH**.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="ceaaa-116">V poli **Celková částka skutečné DPH** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="ceaaa-117">Na kartě **Úprava** lze upravit částky DPH podle kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="ceaaa-118">Vyberte **Resetovat skutečné částky z vypočítaných částek**.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="ceaaa-119">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-119">Select **OK**.</span></span>
14. <span data-ttu-id="ceaaa-120">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ceaaa-120">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Registrace prodejních provizí
description: V tomto tématu je vysvětleno, jak se počítají a registrují prodejní provize.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c6dbccc3e2c33c8dfec2373bd21c7bd217a889b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203220"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="c8653-103">Registrace prodejních provizí</span><span class="sxs-lookup"><span data-stu-id="c8653-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8653-104">V tomto tématu je vysvětleno, jak se počítají a registrují prodejní provize.</span><span class="sxs-lookup"><span data-stu-id="c8653-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="c8653-105">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="c8653-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c8653-106">Před spuštěním této příručky, spusťte průvodce s názvem „Nastavení pravidel prodejní provize“ abyste měli všechna nezbytná nastavení výpočtu provize.</span><span class="sxs-lookup"><span data-stu-id="c8653-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="c8653-107">Poznamenejte si čísla odběratele a zboží, které jste zvolili pro proces provize a použijte je, když budete v této příručce vyzváni k vytvoření prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="c8653-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="c8653-108">Faktura prodejní objednávky, která opravňuje prodejce získat provizi</span><span class="sxs-lookup"><span data-stu-id="c8653-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="c8653-109">V navigačním podokně přejděte na **Moduly > Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="c8653-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="c8653-110">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="c8653-110">Select **New**.</span></span>
3. <span data-ttu-id="c8653-111">V poli **Účet odběratele** vyberte požadovaný záznam v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="c8653-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="c8653-112">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8653-112">Select **OK**.</span></span>
5. <span data-ttu-id="c8653-113">V podokně akcí vyberte **Možnosti**.</span><span class="sxs-lookup"><span data-stu-id="c8653-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="c8653-114">Vyberte **Změnit zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="c8653-114">Select **Change view**.</span></span>
7. <span data-ttu-id="c8653-115">Vyberte **Zobrazení záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="c8653-115">Select **Header view**.</span></span>
8. <span data-ttu-id="c8653-116">Rozbalte sekci **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="c8653-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="c8653-117">Hodnota v poli **Prodejní skupina** představuje skupinu s jedním nebo více přiřazenými prodejními zástupci.</span><span class="sxs-lookup"><span data-stu-id="c8653-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="c8653-118">Uživatelé ve skupině jsou ti, kteří po vyfakturování objednávky podle předdefinované sazby a distribuce obdrží provizi.</span><span class="sxs-lookup"><span data-stu-id="c8653-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="c8653-119">Hodnota se zkopíruje z karty zákazníka, ale pokud chcete, lze ji změnit.</span><span class="sxs-lookup"><span data-stu-id="c8653-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="c8653-120">Skupina prodeje se zkopíruje také do řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="c8653-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="c8653-121">Můžete ji změnit tak, že se může lišit od skupiny uvedené v záhlaví a/nebo mezi řádky.</span><span class="sxs-lookup"><span data-stu-id="c8653-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="c8653-122">Hodnota v poli **Skupina provize** představuje skupinu, kterou jste vytvořili pro jednoho nebo více odběratelů za účelem sledování provizí.</span><span class="sxs-lookup"><span data-stu-id="c8653-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="c8653-123">Hodnota se zkopíruje z karty zákazníka, ale pokud chcete, lze ji změnit.</span><span class="sxs-lookup"><span data-stu-id="c8653-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="c8653-124">V podokně akcí vyberte **Možnosti**.</span><span class="sxs-lookup"><span data-stu-id="c8653-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="c8653-125">Vyberte **Změnit zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="c8653-125">Select **Change view**.</span></span>
11. <span data-ttu-id="c8653-126">Vyberte **Zobrazení řádku**.</span><span class="sxs-lookup"><span data-stu-id="c8653-126">Select **Line view**.</span></span>
12. <span data-ttu-id="c8653-127">V rozevírací nabídce pole **Číslo položky** vyberte položku, kterou jste nastavili pro provize.</span><span class="sxs-lookup"><span data-stu-id="c8653-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="c8653-128">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="c8653-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="c8653-129">Udělejte si poznámku o řádku Čistá částka.</span><span class="sxs-lookup"><span data-stu-id="c8653-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="c8653-130">Ta představuje výnosy z prodeje, které v tomto příkladu jsou základem pro výpočet provize.</span><span class="sxs-lookup"><span data-stu-id="c8653-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="c8653-131">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="c8653-131">Select **Save**.</span></span>
15. <span data-ttu-id="c8653-132">V podokně akcí vyberte možnost **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="c8653-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="c8653-133">Vyberte možnost **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="c8653-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="c8653-134">Rozbalte sekci **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="c8653-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="c8653-135">V poli **Množství** vyberte možnost **Vše**.</span><span class="sxs-lookup"><span data-stu-id="c8653-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="c8653-136">Vyberte možnost **Ano** v poli **Účtování**.</span><span class="sxs-lookup"><span data-stu-id="c8653-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="c8653-137">Vyberte **OK** a poté vyberte **OK** v dalším podokně.</span><span class="sxs-lookup"><span data-stu-id="c8653-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="c8653-138">Zaúčtování transakce může trvat kolem minuty.</span><span class="sxs-lookup"><span data-stu-id="c8653-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="c8653-139">K dokončení povolte zpracování a nezavírejte stránku.</span><span class="sxs-lookup"><span data-stu-id="c8653-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="c8653-140">Zobrazení registrovaných provizí z prodeje</span><span class="sxs-lookup"><span data-stu-id="c8653-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="c8653-141">V podokně akcí zvolte **Faktura** a poté opět vyberte **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="c8653-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="c8653-142">V podokně akcí zvolte **Faktura** a poté vyberte **Transakce provizí**.</span><span class="sxs-lookup"><span data-stu-id="c8653-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="c8653-143">Na kartě **Přehled** jsou zobrazeny řádky představující částky provize vyplacené prodejním zástupcům, kteří jsou přiřazeni k vyfakturované prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="c8653-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="c8653-144">Zkontrolujme si podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="c8653-144">Let's review the details.</span></span>  
    - <span data-ttu-id="c8653-145">Pokud jste použili průvodce „Nastavení pravidel prodejní provize“ k nastavení skupiny **Prodejní provize**, existují dva prodejci, kteří obdrží provizi, a provize bude mezi nimi rozdělena stejnoměrně.</span><span class="sxs-lookup"><span data-stu-id="c8653-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="c8653-146">V tomto příkladu se vypočítává celková částka provize jako procento výnosu z prodeje (čistá částka řádku objednávky).</span><span class="sxs-lookup"><span data-stu-id="c8653-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="c8653-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c8653-147">Close the page.</span></span>
4. <span data-ttu-id="c8653-148">Vyberte **Doklad**.</span><span class="sxs-lookup"><span data-stu-id="c8653-148">Select **Voucher**.</span></span> <span data-ttu-id="c8653-149">Transakce dokladu můžete zkontrolovat pro částky provize, které byly zaúčtované do předdefinovaných výdajů a účtů vyplacené provize.</span><span class="sxs-lookup"><span data-stu-id="c8653-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


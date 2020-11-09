---
title: Řešení problémů s cenami, slevami, smlouvami a rabaty
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s cenami, slevami, smlouvami a rabaty.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b4349eeba285492202b5df8481b277a06708a4c8
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018206"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="dbd6a-103">Řešení problémů s cenami, slevami, smlouvami a rabaty</span><span class="sxs-lookup"><span data-stu-id="dbd6a-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="dbd6a-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s cenami, slevami, smlouvami a rabaty.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="dbd6a-105">Po vytvoření nákupní objednávky nemohu propojit nákupní smlouvu s řádkem nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="dbd6a-106">Po vytvoření nákupní objednávky musí být k nákupní objednávce přiřazena nákupní smlouva.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="dbd6a-107">Jinak nelze řádky nákupní objednávky přidružit k řádkům kupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="dbd6a-108">Jaká kontrola spustí zprávu „Aktualizovat ceny a slevy zadané ručně nebo externí dokument“?</span><span class="sxs-lookup"><span data-stu-id="dbd6a-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="dbd6a-109">Když změníte datum odeslání, může se zobrazit zpráva „Aktualizovat ceny a slevy zadané ručně nebo externí dokument.“</span><span class="sxs-lookup"><span data-stu-id="dbd6a-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="dbd6a-110">Tuto zprávu obdržíte proto, že když se změní datum odeslání, může být spuštěna jiná obchodní nebo prodejní smlouva a způsobit změnu ceny.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="dbd6a-111">Změna data odeslání může také ovlivnit plány skladu a další související informace.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="dbd6a-112">Zpráva se spustí vždy, když dojde ke změně některého z dat nebo některých dalších parametrů.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="dbd6a-113">Účelem zprávy je ujistit se, že jste si vědomi cenových změn, které mohou na základě těchto změn nastat.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="dbd6a-114">Zpráva je výzvou k vyhodnocení obchodní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="dbd6a-115">Celý popis najdete v tématu [Zásady hodnocení obchodní smlouvy](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="dbd6a-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="dbd6a-116">Příjemka nákupní objednávky nezahrnuje všechny poplatky.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="dbd6a-117">Reprodukování problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-117">Reproduce the issue</span></span>

<span data-ttu-id="dbd6a-118">Následující postup ukazuje jeden způsob, jak reprodukovat problém.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="dbd6a-119">Na stránce **Parametry modulu Zásobování a zdroje** na kartě **Dodávka** se ujistěte, že možnost **Generovat náklady na příjemce produktu** je nastavena na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="dbd6a-120">Vytvořte nákupní objednávku, která obsahuje náklady.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="dbd6a-121">Potvrďte nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="dbd6a-122">Přijměte nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="dbd6a-123">Podívejte se na celkový příjem a porovnejte jej s očekávaným součtem.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="dbd6a-124">Všimněte si, že ne všechny poplatky jsou zahrnuty v příjemce nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dbd6a-125">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-125">Issue resolution</span></span>

<span data-ttu-id="dbd6a-126">Řešení závisí na způsobu, jakým byly nastaveny vedlejší náklady.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="dbd6a-127">Informace o tom, jak nastavit vedlejší náklady podle vašich požadavků, najdete v následujícím příspěvku na blogu: [Zaúčtování vedlejších nákladů v době příjemky produktu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="dbd6a-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="dbd6a-128">Ceny a slevy z obchodních smluv se neuplatňují na řádcích prodejních nebo nákupních objednávek, které se importují prostřednictvím správy dat.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dbd6a-129">Popis problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-129">Issue description</span></span>

<span data-ttu-id="dbd6a-130">Obchodní smlouvy, které se vztahují na řádky prodejních nebo nákupních objednávek, se neuplatňují na řádky, které se importují prostřednictvím správy dat.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="dbd6a-131">Stejné obchodní smlouvy se však používají na řádcích prodejních nebo nákupních objednávek, které se vytvářejí ručně.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="dbd6a-132">Důvod problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-132">Reason for the issue</span></span>

<span data-ttu-id="dbd6a-133">Pokud řádky nákupní objednávky, které jsou importovány prostřednictvím správy dat, již obsahují informace o ceně, obchodní smlouva nebude u těchto řádků přehodnocena.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="dbd6a-134">Například pokud **Procento slevy řádku** nebo některá z cenových a slevových hodnot je pro řádek nastaveno , pak nebudou obchodní smlouvy pro daný řádek vyhledávány.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="dbd6a-135">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-135">Issue workaround</span></span>

<span data-ttu-id="dbd6a-136">Toto chování se očekává a je podobné pro prodejní i nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="dbd6a-137">Řešením je importovat řádky nákupní objednávky bez nastavení jakýchkoli informací o ceně.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="dbd6a-138">Poté budou použity obchodní smlouvy a řádky nákupní objednávky budou aktualizovány na základě definovaných obchodních smluv.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="dbd6a-139">Rabat dodavatele se nesčítá na základě faktur.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dbd6a-140">Popis problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-140">Issue description</span></span>

<span data-ttu-id="dbd6a-141">Pokud zaúčtované faktury mají různá data splatnosti, tyto faktury se neprojeví v rabatech dodavatelů, které se z nich generují.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dbd6a-142">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-142">Issue resolution</span></span>

<span data-ttu-id="dbd6a-143">Datum splatnosti se při výpočtu rabatu dodavatele úmyslně nezohledňuje.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="dbd6a-144">Zvažte přizpůsobení systému tak, aby datum splatnosti a vztah k faktuře byly zjevnější s ohledem na skutečný rabat dodavatele.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="dbd6a-145">Jednotkové ceny u nákupních objednávek se nevypočítávají na základě převodu jednotek.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dbd6a-146">Popis problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-146">Issue description</span></span>

<span data-ttu-id="dbd6a-147">Když se na nákupní objednávce změní jednotka, ceny obchodních smluv se nepřepočítají podle definic převodu jednotek.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dbd6a-148">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-148">Issue resolution</span></span>

<span data-ttu-id="dbd6a-149">Ceny se vždy získávají z obchodních smluv (nebo jiného nastavení cen v systému, jako jsou prodejní smlouvy nebo ceny zboží), a jsou stanoveny pro jednotku.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="dbd6a-150">Pokud je jednotka změněna na řádku objednávky, systém vyhledá cenu pro novou jednotku a použije tuto cenu.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="dbd6a-151">Pokud pro jednotku není nalezena žádná cena, systém cenu nepoužije.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="dbd6a-152">Převod jednotky nelze použít k přepočtu ceny na jinou jednotku.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="dbd6a-153">Teoreticky se cena za jednu krabici z deseti nemusí rovnat desetinásobku ceny jedné krabice.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="dbd6a-154">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-154">Issue workaround</span></span>

<span data-ttu-id="dbd6a-155">Jedním ze způsobů, jak tento problém vyřešit, je zajistit, aby existovaly obchodní smlouvy pro jednotky, u kterých očekáváte, že budou použity na řádcích objednávek pro položku.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="dbd6a-156">U obchodních smluv dochází k problémům s převodem měn.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="dbd6a-157">Ceny obchodních smluv se nepřepočítají podle měny, když se měna liší od nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="dbd6a-158">Funkce *Obecná měna* umožňuje definovat ceny a slevy pouze v jedné měně.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="dbd6a-159">Poté můžete převádět na jiné měny podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="dbd6a-160">Po dokončení převodu může funkce navíc automaticky použít inteligentní zaokrouhlování.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="dbd6a-161">Když otevřu stránku Nákupní smlouva v režimu zobrazení řádku, nemohu stránku přizpůsobit přidáním pole Cena jednotky v přehledu řádku.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="dbd6a-162">Některá sdílená pole v rámci smlouvy nelze zahrnout do přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="dbd6a-163">K tomuto omezení dochází z důvodu implementovaného datového modelu.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="dbd6a-164">Proto nemůžete přizpůsobit pole **Jednotka ceny**.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="dbd6a-165">Maximální limit z nákupní smlouvy není účinný u nákupní žádanky.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="dbd6a-166">Popis problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-166">Issue description</span></span>

<span data-ttu-id="dbd6a-167">Pokud je nákupní žádanka propojena s nákupní smlouvou, maximální limit z nákupní smlouvy neplatí na nákupní žádance.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="dbd6a-168">Informace o výchozí ceně jsou správně zadány, ale v nákupní žádance lze objednat více, než je maximální limit z kupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="dbd6a-169">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="dbd6a-169">Issue resolution</span></span>

<span data-ttu-id="dbd6a-170">Toto chování se očekává.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-170">This behavior is expected.</span></span> <span data-ttu-id="dbd6a-171">Protože žádanky nejsou vždy schváleny, nemělo by být v nákupní smlouvě vyhrazeno množství nebo částka.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="dbd6a-172">Proto nesplníte maximální limit z nákupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="dbd6a-173">Obchodní smlouvy lze uzavřít z odmítnutých požadavků na cenovou nabídku.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="dbd6a-174">Systém tedy nebrání vytváření deníků obchodních smluv, pokud nebyl přijat řádek RFQ.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="dbd6a-175">Můžete vytvořit obchodní smlouvy pro jakékoli odpovědi na požadavky na nabídku (RFQ), bez ohledu na to, zda byly přijaty nebo odmítnuty.</span><span class="sxs-lookup"><span data-stu-id="dbd6a-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="dbd6a-176">Další informace naleznete v tématu [Přehled požadavků na nabídku](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="dbd6a-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>


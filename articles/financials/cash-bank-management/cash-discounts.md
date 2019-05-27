---
title: Platební slevy
description: Platební slevy jsou nastaveny a sdílené pro závazky a pohledávky.  Dostupná platební sleva může být definovaná na faktuře odběratele nebo dodavatele a proběhne, jestliže bude faktura zaplacena v rámci data platební slevy.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd15a021244e55ea988a95184a758a321ebeafb3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561608"
---
# <a name="cash-discounts"></a><span data-ttu-id="c2ea1-104">Platební slevy</span><span class="sxs-lookup"><span data-stu-id="c2ea1-104">Cash discounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2ea1-105">Platební slevy jsou nastaveny a sdílené pro závazky a pohledávky.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="c2ea1-106">Dostupná platební sleva může být definovaná na faktuře odběratele nebo dodavatele a proběhne, jestliže bude faktura zaplacena v rámci data platební slevy.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

## <a name="cash-discounts"></a><span data-ttu-id="c2ea1-107">Platební slevy</span><span class="sxs-lookup"><span data-stu-id="c2ea1-107">Cash discounts</span></span>

<span data-ttu-id="c2ea1-108">Na stránce Platební slevy lze vytvořit platební slevy pro odběratele nebo dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="c2ea1-109">Pomocí pole Další kód slevy lze definovat také řadu platebních slev, které budou postupně následovat vždy, když vyprší platnost předchozí platební slevy.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="c2ea1-110">Další informace naleznete v části „Příklad: Řada platebních slev“ dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="c2ea1-111">Pokud jsou faktura, transakce akreditivu (platba nebo dobropis) nebo obě tyto možnosti zadány v jiné měně než v zúčtovací měně právnické osoby, platební sleva se vypočítá pomocí směnného kurzu na základě data platby nebo dobropisu.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="c2ea1-112">Pokud jsou faktura a platební doklad zadány v jiných právnických osobách a zúčtovací měny se pro právnické osoby liší, směnný kurz je převzat z právnické osoby faktury k datu dokumentu akreditivu.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="c2ea1-113">Další informace naleznete v části „Příklad: Směnné kurzy pro platební slevy“ dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>

## <a name="defaulting-order-of-cash-discount-main-account"></a><span data-ttu-id="c2ea1-114">Výchozí objednávka hlavního účtu platební slevy</span><span class="sxs-lookup"><span data-stu-id="c2ea1-114">Defaulting order of cash discount main account</span></span>

<span data-ttu-id="c2ea1-115">Pokud je faktura uhrazena v termínu opravňujícím k platební slevě, zaúčtuje se platební sleva automaticky na hlavní účet platebních slev podle následující výchozí priority:</span><span class="sxs-lookup"><span data-stu-id="c2ea1-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="c2ea1-116">Hlavní účet určený v poli Alternativní účet pro slevu na odběratelově stránce Vyrovnat otevřené transakce a dodavatelově stránce Vyrovnat otevřené transakce.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="c2ea1-117">Hlavní účet určený v poli Platební sleva odběratele nebo Platební sleva dodavatele účetní skupiny hlavní knihy, která je přiřazena ke kódu DPH na faktuře.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="c2ea1-118">Na stránce Skupiny zaúčtování hlavní knihy nastavte účetní skupiny hlavní knihy a na stránce Kódy DPH je přiřaďte ke kódům DPH.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="c2ea1-119">Hlavní účtovací účet na stránce Platební slevy buď v poli Hlavní účet slev odběratele, nebo v poli Hlavní účet slev dodavatele pro kód platební slevy, který je na uhrazené faktuře.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="c2ea1-120">Hlavní účet pro platební slevy, který je definován na stránce Účty pro automatické transakce.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="c2ea1-121"> Příklad: Řada platebních slev</span><span class="sxs-lookup"><span data-stu-id="c2ea1-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="c2ea1-122">vytvořte tři kódy platební slevy následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c2ea1-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="c2ea1-123">Kód 5D10% – platební sleva 10 % při uhrazení částky do 5 dní.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="c2ea1-124">Kód 10D5% – platební sleva 5 % při uhrazení částky do 10 dní.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="c2ea1-125">Kód 14D2% – platební sleva 2 % při uhrazení částky do 14 dní.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="c2ea1-126">V poli Další kód slevy:</span><span class="sxs-lookup"><span data-stu-id="c2ea1-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="c2ea1-127">Pro kód 5D10%, vyberte 10D5%.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="c2ea1-128">Pro kód 10D5%, vyberte 14D2%.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="c2ea1-129">Pro kód 14D2% ponechte pole Další kód slevy prázdné.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="c2ea1-130">Tři platební slevy následují po sobě tak, jak datum platby postupně překračuje datum dřívější platební slevy na faktuře.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="c2ea1-131">Při uhrazení faktury je poskytnuta pouze jedna platební sleva podle toho, jaké datum platební slevy bylo v řadě platebních slev splněno.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="c2ea1-132"> Příklad: Směnné kurzy pro platební slevy</span><span class="sxs-lookup"><span data-stu-id="c2ea1-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="c2ea1-133">Zúčtovací měna vaší právnické osoby je EUR a pro USD jsou zadány následující směnné kurty:</span><span class="sxs-lookup"><span data-stu-id="c2ea1-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="c2ea1-134">1. únor = 110</span><span class="sxs-lookup"><span data-stu-id="c2ea1-134">February 1 = 110</span></span>
-   <span data-ttu-id="c2ea1-135">1. březen = 80</span><span class="sxs-lookup"><span data-stu-id="c2ea1-135">March 1 = 80</span></span>

<span data-ttu-id="c2ea1-136">Faktura na 1000 USD s podmínkou platební slevy 20D2% je zaúčtována 15. února.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="c2ea1-137">Částka v zúčtovací měně faktury činí 1100 EUR.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="c2ea1-138">Platba za 980 USD je vyrovnána s fakturou 1. března.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="c2ea1-139">Částka platební slevy je 20 USD.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="c2ea1-140">Částka v zúčtovací měně u dané platby činí 784 EUR.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="c2ea1-141">Částka v zúčtovací měně u platební slevy je vypočítána pomocí směnného kurzu ke dni 1. března: 20 \* 80 / 100 = 16 EUR.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

> [!NOTE]
> <span data-ttu-id="c2ea1-142">Je-li na stránce Parametry pohledávek nebo na stránce Parametry závazků zvolena možnost Vypočítat platební slevy pro částečné platby, použije se směnný kurz platný k datu jednotlivých částečných plateb.</span><span class="sxs-lookup"><span data-stu-id="c2ea1-142">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> 


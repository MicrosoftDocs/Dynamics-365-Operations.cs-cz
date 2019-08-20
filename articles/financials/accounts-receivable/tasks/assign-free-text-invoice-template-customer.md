---
title: Přiřazení šablony volné faktury k odběrateli
description: Tato úloha demonstruje způsob, jak přiřadit šablonu volné faktury pro odběratele.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53bff33083a78c0bb1c7d243fe9965fb264d209e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843042"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="b9f50-103">Přiřazení šablony volné faktury k odběrateli</span><span class="sxs-lookup"><span data-stu-id="b9f50-103">Assign free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9f50-104">Tato úloha demonstruje způsob, jak přiřadit šablonu volné faktury pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="b9f50-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="b9f50-105">Tento úkol využívá ukázkovou společnost USMF a je určen pro uživatele, který je odpovědný za správu a zpracování faktur pohledávek.</span><span class="sxs-lookup"><span data-stu-id="b9f50-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="b9f50-106">Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="b9f50-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="b9f50-107">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b9f50-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b9f50-108">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="b9f50-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="b9f50-109">Klikněte na Opakované faktury.</span><span class="sxs-lookup"><span data-stu-id="b9f50-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="b9f50-110">Na této stránce můžete přiřadit šablony volných faktur k odběratelům a určit, jak často faktury budou odesílány odběrateli.</span><span class="sxs-lookup"><span data-stu-id="b9f50-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="b9f50-111">Klikněte na možnost Nový a přiřaďte tak novou šablonu k odběrateli.</span><span class="sxs-lookup"><span data-stu-id="b9f50-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="b9f50-112">Vybrat šablonu volné faktury, kterou chcete přiřadit odběrateli.</span><span class="sxs-lookup"><span data-stu-id="b9f50-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="b9f50-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b9f50-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="b9f50-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b9f50-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b9f50-115">Zadejte datum, kdy bude vygenerována první faktura.</span><span class="sxs-lookup"><span data-stu-id="b9f50-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="b9f50-116">Zadejte koncové datum opakování.</span><span class="sxs-lookup"><span data-stu-id="b9f50-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="b9f50-117">Vyberte jednu z následujících možností: Bez koncového data – faktury budou generovány neomezeně dlouho, dokud šablony nebude odebrána z účtu odběratele.</span><span class="sxs-lookup"><span data-stu-id="b9f50-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="b9f50-118">Koncové datum fakturace – Vyberte tuto možnost a zadejte poslední datum, kdy lze fakturu generovat.</span><span class="sxs-lookup"><span data-stu-id="b9f50-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="b9f50-119">Maximální kumulativní částka, po které se zastaví generování faktury.</span><span class="sxs-lookup"><span data-stu-id="b9f50-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="b9f50-120">Zadejte maximální kumulativní částku, které lze dosáhnout pomocí vybrané šablony.</span><span class="sxs-lookup"><span data-stu-id="b9f50-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="b9f50-121">Například zadáte-li 1 000,00 a necháte vygenerovat měsíční faktury vždy pro 100,00, faktury zastaví generování po vygenerování desáté faktury.</span><span class="sxs-lookup"><span data-stu-id="b9f50-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="b9f50-122">Vygenerujte opakované faktury pomocí výchozích hodnot ze šablony volné faktury nebo účtu odběratele.</span><span class="sxs-lookup"><span data-stu-id="b9f50-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="b9f50-123">Vyberte, zda chcete při vytvoření faktury k určení výchozích hodnot pro jazyk, účetní profil, skupinu DPH, skupinu DPH položky, kód seznamu, zemi/oblast pro dodávku, měnu, platební podmínky, způsob platby, specifikaci plateb, platební kalendář, platební slevu, finanční dimenze a převodní poukázku žira využít šablonu volné faktury nebo účet odběratele.</span><span class="sxs-lookup"><span data-stu-id="b9f50-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="b9f50-124">Vyberte způsob opakování.</span><span class="sxs-lookup"><span data-stu-id="b9f50-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="b9f50-125">Denně – Vyberte tuto možnost a zadejte počet dní do pole Za.</span><span class="sxs-lookup"><span data-stu-id="b9f50-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="b9f50-126">Například pokud zadáte 15, faktura bude pro tohoto odběratele vygenerována každých 15 dnů.</span><span class="sxs-lookup"><span data-stu-id="b9f50-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="b9f50-127">Týdně – Vyberte tuto možnost a zadejte počet týdnů do pole Za.</span><span class="sxs-lookup"><span data-stu-id="b9f50-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="b9f50-128">Například pokud zadáte 2, faktura bude pro tohoto odběratele vygenerována každé dva týdny.</span><span class="sxs-lookup"><span data-stu-id="b9f50-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="b9f50-129">Měsíčně – Vyberte tuto možnost a zadejte počet měsíců do pole Za.</span><span class="sxs-lookup"><span data-stu-id="b9f50-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="b9f50-130">Například pokud zadáte 6, faktura bude pro tohoto odběratele vygenerována každých šest měsíců.</span><span class="sxs-lookup"><span data-stu-id="b9f50-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="b9f50-131">Ročně – Vyberte tuto možnost a zadejte počet roků do pole Za.</span><span class="sxs-lookup"><span data-stu-id="b9f50-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="b9f50-132">Například pokud zadáte 2, faktura bude pro tohoto odběratele vygenerována každé dva roky.</span><span class="sxs-lookup"><span data-stu-id="b9f50-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="b9f50-133">Do pole Za zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="b9f50-133">In the Per field, enter a number.</span></span>


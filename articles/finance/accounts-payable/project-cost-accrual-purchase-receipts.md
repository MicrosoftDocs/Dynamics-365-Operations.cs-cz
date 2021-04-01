---
title: Časové rozlišení projektu na nákupních příjemkách
description: Toto téma popisuje, jak lze sledovat časově rozlišené náklady na projekt z nákupních příjemek v aplikaci Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c2b92f1f5caf34bf798b86380b73c2dcc7de17b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231633"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="fb646-103">Časové rozlišení projektu na nákupních příjemkách</span><span class="sxs-lookup"><span data-stu-id="fb646-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb646-104">Toto téma popisuje, jak lze sledovat časově rozlišené náklady na projekt z nákupních příjemek v aplikaci Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="fb646-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="fb646-105">Faktury pro projekt často přicházejí později než zboží a služby, což může mít významný dopad na projekt klíčové ukazatele výkonu (KPI).</span><span class="sxs-lookup"><span data-stu-id="fb646-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="fb646-106">Je důležité, aby bylo možné sledovat tyto transakce ve finančních i projektových sestavách.</span><span class="sxs-lookup"><span data-stu-id="fb646-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="fb646-107">Ilustruje to následující vzorový scénář.</span><span class="sxs-lookup"><span data-stu-id="fb646-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="fb646-108">Společnost Contoso Consulting zahájila nový projekt nasazení do cloudu.</span><span class="sxs-lookup"><span data-stu-id="fb646-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="fb646-109">Je vytvořena nákupní objednávka pro nákup počítače pro projekt.</span><span class="sxs-lookup"><span data-stu-id="fb646-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="fb646-110">Počítač bude stát 1 500 USD a instalační služba 150 USD.</span><span class="sxs-lookup"><span data-stu-id="fb646-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="fb646-111">Dodavatel má dodat a nainstalovat počítač, ale fakturu ještě nedošla do společnosti Contoso Consulting.</span><span class="sxs-lookup"><span data-stu-id="fb646-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="fb646-112">Vedoucí projektu by chtěl vidět poměrné rozložení nákladů na 1650 USD před dodáním faktury.</span><span class="sxs-lookup"><span data-stu-id="fb646-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="fb646-113">Tyto náklady by se projevily také ve finančních výkazech společnosti ke konci měsíce.</span><span class="sxs-lookup"><span data-stu-id="fb646-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="fb646-114">Časově rozlišené náklady musí být zaznamenány na finanční úrovni i na úrovni projektu pro účely vykazování.</span><span class="sxs-lookup"><span data-stu-id="fb646-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="fb646-115">V aplikaci Finance and Operations lze sledovat finanční aktualizaci příjemky produktu pro kategorie zboží a zakázek.</span><span class="sxs-lookup"><span data-stu-id="fb646-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="fb646-116">U zboží na stránce **Parametry závazků** vyberte možnost **Zaúčtování příjemky produktu do knihy**.</span><span class="sxs-lookup"><span data-stu-id="fb646-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="fb646-117">[![Stránka Parametry závazků](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="fb646-117">[![Accounts payable parameters page](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="fb646-118">Pro kategorie zásobování na stránce **Pravidlo zásad kategorie** vyberte zásady **Zásobování** a potom vyberte **Časově rozlišený nákupní výdaj na příjemce** pro každou kategorii zásobování.</span><span class="sxs-lookup"><span data-stu-id="fb646-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="fb646-119">[![Stránka Pravidlo zásad kategorie](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="fb646-119">[![Category policy rule page](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="fb646-120">Účty **Nákupní výdaj nefakturovaný** a **Časově rozlišený nákup** v **nastavení účtování** budou použity k zaúčtování dokladů, které jsou spojené s touto příjemkou produktu</span><span class="sxs-lookup"><span data-stu-id="fb646-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>

<span data-ttu-id="fb646-121">Pomocí stejného scénáře se podíváme na to, jaký vliv bude mít zaúčtování příjemky produktu na hlavní knihu a informace o projektu.</span><span class="sxs-lookup"><span data-stu-id="fb646-121">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="fb646-122">**Krok 1:** Vytvořte a potvrďte novou nákupní objednávku pro projekt k zaznamenání nákupu počítače za 1500 USD a instalační služby za 150 USD.</span><span class="sxs-lookup"><span data-stu-id="fb646-122">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="fb646-123">[![Vytvoření nové nákupní objednávky](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="fb646-123">[![Create new purchase order](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="fb646-124">Při potvrzení nákupní objednávky jsou pro projekt vytvořeny transakce pro potvrzené náklady.</span><span class="sxs-lookup"><span data-stu-id="fb646-124">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="fb646-125">[![Vytvořené transakce](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="fb646-125">[![Transactions created](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="fb646-126">Transakce pro potvrzené náklady bude mít v poli **Původ transakce** nastavenou hodnotu **Nákupní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="fb646-126">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="fb646-127">Vytvoření a potvrzení nákupní objednávky nevytváří transakce pro projekt.</span><span class="sxs-lookup"><span data-stu-id="fb646-127">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="fb646-128">**Krok 2:** Doručení zboží a služeb proběhne a je registrována příjemka produktu.</span><span class="sxs-lookup"><span data-stu-id="fb646-128">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="fb646-129">Zaúčtování příjemky produktu bude generovat a zaúčtuje doklad do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="fb646-129">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="fb646-130">Doklad bude připsán na stranu nákupních výdajů, nefakturovaného účtu a poměrně rozloženého účtu nákupního kreditu.</span><span class="sxs-lookup"><span data-stu-id="fb646-130">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="fb646-131">[![Transakce dokladu](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="fb646-131">[![Voucher transactions](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="fb646-132">Zaúčtování příjemky produktu bude používat nastavení účtování pro kategorie zásobování a produkty a nikoli nastavení účtování pro kategorie projektu.</span><span class="sxs-lookup"><span data-stu-id="fb646-132">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="fb646-133">Aby se správně projevil finanční dopad na časově rozlišený nákup, je nutné toto nastavení vyrovnat.</span><span class="sxs-lookup"><span data-stu-id="fb646-133">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="fb646-134">Je možné mapovat kategorie zásobování na kategorie projektu na stránce **Kategorie zásobování**.</span><span class="sxs-lookup"><span data-stu-id="fb646-134">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="fb646-135">[![Stránka Kategorie zásobování](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="fb646-135">[![Procurement category page](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="fb646-136">**Krok 3:** Vytvořte standardní fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="fb646-136">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="fb646-137">Zaúčtování příjemky produktu nemá vliv na informace o projektu.</span><span class="sxs-lookup"><span data-stu-id="fb646-137">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="fb646-138">Tento problém odstraníte vygenerováním návrhu faktury dodavatele přímo po zaúčtování nákupní příjemky.</span><span class="sxs-lookup"><span data-stu-id="fb646-138">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="fb646-139">Přejděte na stránku **Nákupní objednávka** &gt; **karta Faktura** &gt; **Generovat** &gt; **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="fb646-139">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="fb646-140">Tím se vytvoří dokument čekající faktury, který aktualizuje informace o projektu.</span><span class="sxs-lookup"><span data-stu-id="fb646-140">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="fb646-141">Vytvoření návrhu faktury dodavatele bude generovat čekající transakce projektu.</span><span class="sxs-lookup"><span data-stu-id="fb646-141">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="fb646-142">[![Čekající transakce projektu](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="fb646-142">[![Pending project transactions](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="fb646-143">Na stránce **Potvrzené náklady** se záznamy vytvořené v kroku 1 uzavřou a nové záznamy budou vytvořeny tak, aby odrážely náklady závazků pocházející z nevyřízené faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="fb646-143">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="fb646-144">Pole **Původ transakce** pro potvrzené náklady bude nastaveno na hodnotu **faktura dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="fb646-144">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="fb646-145">[![Stránka Potvrzené náklady](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="fb646-145">[![Commited costs page](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="fb646-146">Faktura dodavatele zůstane v nevyřízeném stavu, dokud nepřijde skutečná dodavatelská faktura.</span><span class="sxs-lookup"><span data-stu-id="fb646-146">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
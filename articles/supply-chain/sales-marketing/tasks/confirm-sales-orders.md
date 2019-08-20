---
title: Potvrzení prodejních objednávek
description: Tento postup ukazuje postup potvrzení prodejních objednávek.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c01c5e070954b3791df3cb67ba7c4f4ec79e3003
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833971"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="4e88f-103">Potvrzení prodejních objednávek</span><span class="sxs-lookup"><span data-stu-id="4e88f-103">Confirm sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e88f-104">Tento postup ukazuje postup potvrzení prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="4e88f-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="4e88f-105">Bude vám předvedeno, jak potvrdit jednu objednávku a více objednávek najednou.</span><span class="sxs-lookup"><span data-stu-id="4e88f-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="4e88f-106">Tyto úkoly obvykle provádějí zpracovatelé prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="4e88f-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="4e88f-107">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="4e88f-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4e88f-108">Dříve než začnete, ověřte, že pro stejného odběratele existuje několik otevřených prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="4e88f-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="4e88f-109">V případě, že používáte data USMF, můžete použít odběratele US-027.</span><span class="sxs-lookup"><span data-stu-id="4e88f-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="4e88f-110">Potvrzení jedné prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="4e88f-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="4e88f-111">Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="4e88f-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="4e88f-112">V seznamu najděte a vyberte objednávku, kterou chcete potvrdit.</span><span class="sxs-lookup"><span data-stu-id="4e88f-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="4e88f-113">Kliknutím na odkaz na čísle prodejní objednávky otevřete vybranou objednávku.</span><span class="sxs-lookup"><span data-stu-id="4e88f-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="4e88f-114">V podokně akcí klikněte na možnost Prodej.</span><span class="sxs-lookup"><span data-stu-id="4e88f-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="4e88f-115">Klikněte na možnost Potvrdit prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="4e88f-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="4e88f-116">Rozbalte nebo sbalte oddíl Parametry.</span><span class="sxs-lookup"><span data-stu-id="4e88f-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="4e88f-117">Ujistěte se, že je pole Zaúčtování – Ano aktivní.</span><span class="sxs-lookup"><span data-stu-id="4e88f-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="4e88f-118">Nastavte možnost Tisk potvrzení na Ano.</span><span class="sxs-lookup"><span data-stu-id="4e88f-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="4e88f-119">Pole Zkontrolovat limit úvěru určuje metodu, která se používá k výpočtu zbývajícího úvěru zákazníka.</span><span class="sxs-lookup"><span data-stu-id="4e88f-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="4e88f-120">Ve výchozím nastavení se zkopíruje ze stránky Parametry pohledávek.</span><span class="sxs-lookup"><span data-stu-id="4e88f-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="4e88f-121">Pokud chcete kontrolu limitu úvěru přeskočit při potvrzení určité prodejní objednávky, nastavte možnost Zkontrolovat limitu úvěru na hodnotu Neomezeno.</span><span class="sxs-lookup"><span data-stu-id="4e88f-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="4e88f-122">Je třeba si však uvědomit, že i když je toto pole je nastaveno na hodnotu Neomezeno, kontrola limitu úvěru bude i přesto provedena, pokud je v hlavních datech odběratele vybrána možnost Povinný limit úvěru.</span><span class="sxs-lookup"><span data-stu-id="4e88f-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="4e88f-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4e88f-123">Click OK.</span></span>
9. <span data-ttu-id="4e88f-124">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="4e88f-124">Click Yes.</span></span>
10. <span data-ttu-id="4e88f-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4e88f-125">Close the page.</span></span>
11. <span data-ttu-id="4e88f-126">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="4e88f-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="4e88f-127">Klikněte na tlačítko Změnit zobrazení.</span><span class="sxs-lookup"><span data-stu-id="4e88f-127">Click Change view.</span></span>
13. <span data-ttu-id="4e88f-128">Klikněte na možnost Zobrazení záhlaví.</span><span class="sxs-lookup"><span data-stu-id="4e88f-128">Click Header view.</span></span>
    * <span data-ttu-id="4e88f-129">Při potvrzení objednávky je nastaven stav dokumentu na hodnotu Potvrzení.</span><span class="sxs-lookup"><span data-stu-id="4e88f-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="4e88f-130">V podokně akcí klikněte na možnost Prodej.</span><span class="sxs-lookup"><span data-stu-id="4e88f-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="4e88f-131">Klikněte na možnost Prodejní objednávka – potvrzení.</span><span class="sxs-lookup"><span data-stu-id="4e88f-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="4e88f-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4e88f-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="4e88f-133">Potvrzení více prodejních objednávek najednou</span><span class="sxs-lookup"><span data-stu-id="4e88f-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="4e88f-134">Přejděte do nabídky Prodej a marketing > Prodejní objednávky > Potvrzení objednávky > Potvrdit prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="4e88f-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="4e88f-135">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="4e88f-135">Click Select.</span></span>
3. <span data-ttu-id="4e88f-136">V seznamu na kartě Rozsah vyhledejte a vyberte záznam, který odkazuje na pole Účet odběratele.</span><span class="sxs-lookup"><span data-stu-id="4e88f-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="4e88f-137">V poli Kritéria kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="4e88f-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4e88f-138">V seznamu najděte a vyberte účet odběratele, který má více objednávek, které chcete hromadně potvrdit.</span><span class="sxs-lookup"><span data-stu-id="4e88f-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="4e88f-139">Pokud používáte data USMF, můžete vybrat účet US-027.</span><span class="sxs-lookup"><span data-stu-id="4e88f-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="4e88f-140">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4e88f-140">Click OK.</span></span>
    * <span data-ttu-id="4e88f-141">Karta Přehled zobrazuje seznam objednávek, které splňují kritéria dotazu.</span><span class="sxs-lookup"><span data-stu-id="4e88f-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="4e88f-142">Tyto položky budou zahrnuty do potvrzení.</span><span class="sxs-lookup"><span data-stu-id="4e88f-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="4e88f-143">Pole Souhrnná aktualizace pro určuje parametr, pomocí kterého se více objednávek shrne do jednoho potvrzovacího dokumentu.</span><span class="sxs-lookup"><span data-stu-id="4e88f-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="4e88f-144">Ve výchozím nastavení je tato možnost zkopírována z nastavení Výchozí hodnoty souhrnné aktualizace na stránce Parametry pohledávek.</span><span class="sxs-lookup"><span data-stu-id="4e88f-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="4e88f-145">V poli Souhrnná aktualizace pro vyberte možnost Objednávka.</span><span class="sxs-lookup"><span data-stu-id="4e88f-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="4e88f-146">Minimální parametry požadované k vytvoření souhrnných aktualizací jsou Účet faktury a Měna.</span><span class="sxs-lookup"><span data-stu-id="4e88f-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="4e88f-147">To znamená, že souhrnné aktualizace, které mají jiné účty faktur a jiné měny, nejsou povoleny.</span><span class="sxs-lookup"><span data-stu-id="4e88f-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="4e88f-148">Na stránce Parametry souhrnné aktualizace, která je přístupná prostřednictvím stránky Parametry pohledávek, lze nastavit další parametry.</span><span class="sxs-lookup"><span data-stu-id="4e88f-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="4e88f-149">V poli Prodejní objednávka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="4e88f-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4e88f-150">V seznamu vyberte číslo prodejní objednávky, která má být souhrnnou objednávkou.</span><span class="sxs-lookup"><span data-stu-id="4e88f-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="4e88f-151">Klikněte na možnost Uspořádat.</span><span class="sxs-lookup"><span data-stu-id="4e88f-151">Click Arrange.</span></span>
11. <span data-ttu-id="4e88f-152">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4e88f-152">Click OK.</span></span>
12. <span data-ttu-id="4e88f-153">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4e88f-153">Click OK.</span></span>


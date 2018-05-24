---
title: "Podrobení vrácených položek kontrole"
description: "Podrobení vrácených položek kontrole"
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: df209cfdbdef591e9f24161b3651316c43d69ee0
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---


# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="6f916-103">Podrobení vrácených položek kontrole</span><span class="sxs-lookup"><span data-stu-id="6f916-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="6f916-104">Klikněte na **Řízení zásob** \> **Periodicky** \> **Správa kvality** \> **Karanténní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="6f916-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="6f916-105">Vyhledejte řádek objednávky, který odpovídá kontrolované vrácené položce.</span><span class="sxs-lookup"><span data-stu-id="6f916-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="6f916-106">Karanténní příkaz lze přidružit pouze jednomu číslu zboží.</span><span class="sxs-lookup"><span data-stu-id="6f916-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="6f916-107">Při vrácení 10 položek s různými čísly zboží v rámci jedné dodávky a při jejich odeslání do karantény dojde k vytvoření 10 samostatných karanténních příkazů.</span><span class="sxs-lookup"><span data-stu-id="6f916-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="6f916-108">Po prověření položky určete pomocí výběru v poli **Dispoziční kód** akci, která má být pro danou položku provedena, a způsob zpracování souvisejících finančních transakcí.</span><span class="sxs-lookup"><span data-stu-id="6f916-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="6f916-109">Mezi příklady patří vrácení položky na sklad a refundace odběratele, vyřazení položky a odeslání náhradní položky odběrateli nebo vrácení položky odběrateli bez náhrady.</span><span class="sxs-lookup"><span data-stu-id="6f916-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="6f916-110">V případě, že více položkám vráceným v rámci jedné dávky čísel položek nelze přiřadit stejný dispoziční kód, je nutné rozdělit karanténní příkaz (<STRONG>Funkce</STRONG> &gt; <STRONG>Rozdělit</STRONG>), aby bylo možné přiřadit jednotlivým dílčím dávkám různé dispoziční kódy.</span><span class="sxs-lookup"><span data-stu-id="6f916-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="6f916-111">Po dokončení kontroly můžete klepnutím na položku **Vykázat jako dokončené** vydat vrácené položky a vytvořit záznam deníku doručení položky.</span><span class="sxs-lookup"><span data-stu-id="6f916-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="6f916-112">Osoba nebo oddělení, které zboží obdržely, poté deník zpracují, aby došlo k vrácení daného zboží do skladových zásob.</span><span class="sxs-lookup"><span data-stu-id="6f916-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="6f916-113">- nebo -</span><span class="sxs-lookup"><span data-stu-id="6f916-113">–or–</span></span>
    
    <span data-ttu-id="6f916-114">Ukončete karanténní příkaz a přesuňte položky zpět přímo na sklad pomocí jedné z funkcí tlačítka **Zásoby**.</span><span class="sxs-lookup"><span data-stu-id="6f916-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="6f916-115">Uložte změny zavřením formuláře.</span><span class="sxs-lookup"><span data-stu-id="6f916-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f916-116">Viz také</span><span class="sxs-lookup"><span data-stu-id="6f916-116">See also</span></span>

[<span data-ttu-id="6f916-117">Určení způsobu nakládání s vrácenými položkami</span><span class="sxs-lookup"><span data-stu-id="6f916-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  




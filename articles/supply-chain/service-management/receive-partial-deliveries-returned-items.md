---
title: "Příjem částečných dodávek vrácených položek"
description: "Částečné dodávky jsou definovány v souvislosti se řádky vratek, nikoli s odesláním vratky."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
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
ms.openlocfilehash: f9f596d31f2438a353b02bf939786b284937db86
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="e23cb-103">Příjem částečných dodávek vrácených položek</span><span class="sxs-lookup"><span data-stu-id="e23cb-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e23cb-104">Částečné dodávky jsou definovány v souvislosti se řádky vratek, nikoli s odesláním vratky.</span><span class="sxs-lookup"><span data-stu-id="e23cb-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="e23cb-105">To znamená, že když obdržíte úplné množství určené na jednom řádku vratky, ale nic z jiných řádků vratky, tato dodávka není částečnou dodávkou.</span><span class="sxs-lookup"><span data-stu-id="e23cb-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="e23cb-106">Pokud však řádek vratky vyžaduje vrácení například 10 jednotek konkrétní položky, ale obdržíte pouze čtyři, o částečnou dodávku se jedná.</span><span class="sxs-lookup"><span data-stu-id="e23cb-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="e23cb-107">Pokud vrácená dodávka obsahuje menší než úplné množství na řádku vratky, můžete dodávku odložit a vyčkat doručení zbylého množství nebo můžete zaznamenat a zaúčtovat částečné množství.</span><span class="sxs-lookup"><span data-stu-id="e23cb-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="e23cb-108">Zaznamenání a zaúčtování částečného množství</span><span class="sxs-lookup"><span data-stu-id="e23cb-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="e23cb-109">Po výběru objednávky vrácení pro příjezd na kartě **Přehled příjezdu – sklad: %1, Dok: %2, název deníku: %3** formulář, klikněte na **Počáteční příjezd** k vytvoření deníku příjezdu a pak kliknutím na **Deníky** \> **Zobrazit příjezdy z příjmů** otevřete formulář **Deník místa**.</span><span class="sxs-lookup"><span data-stu-id="e23cb-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="e23cb-110">Vyberte řádek deníku, se kterým chcete pracovat, a poté klepnutím na položku **Řádky** otevřete formulář **Řádky deníku, místa**.</span><span class="sxs-lookup"><span data-stu-id="e23cb-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="e23cb-111">Vyberte řádek čísla položky, pro který bylo doručeno pouze částečné množství, a poté klepnutím na položky **Funkce** \> **Rozdělit** otevřete formulář **Rozdělit**.</span><span class="sxs-lookup"><span data-stu-id="e23cb-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="e23cb-112">Do pole **Rozdělit množství** zadejte množství pro celkový počet přijatých položek a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e23cb-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="e23cb-113">Ve formuláři **Řádky deníku, skl. místa** vyberte řádek pro množství položek, které jste obdrželi, a poté klepněte na položku **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="e23cb-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="e23cb-114">Po převzetí položek můžete zaúčtovat řádek pro další množství.</span><span class="sxs-lookup"><span data-stu-id="e23cb-114">You can post the line for the additional quantity after the items have arrived.</span></span>






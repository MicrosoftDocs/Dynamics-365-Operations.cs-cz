---
title: Registrace příjmu vrácených položek
description: Příjem vráceného zboží můžete zaregistrovat pomocí formuláře Přehled doručení nebo Registrace.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08a40d7e95ffb17a096f759b332e77aeaf96ffd6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742237"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="06e93-103">Registrace příjmu vrácených položek</span><span class="sxs-lookup"><span data-stu-id="06e93-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="06e93-104">K dispozici jsou dva způsoby záznamu příjmu vrácených položek.</span><span class="sxs-lookup"><span data-stu-id="06e93-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="06e93-105">Prvním způsobem je proces příjmu do skladu, který používá formulář **Přehled doručení**.</span><span class="sxs-lookup"><span data-stu-id="06e93-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="06e93-106">Druhý používá formulář **Registrace**.</span><span class="sxs-lookup"><span data-stu-id="06e93-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="06e93-107">Zaznamenat příjem vrácených položek ve formuláři Přehled doručení</span><span class="sxs-lookup"><span data-stu-id="06e93-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="06e93-108">Lze použít formulář **Přehled doručení** k identifikaci vrácené dodávky podle čísla autorizace vrácení materiálu (RMA).</span><span class="sxs-lookup"><span data-stu-id="06e93-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="06e93-109">Pokud je definován název deníku na kartě **Nastavení** a řádky deníku, které odpovídají příslušným řádkům ve formuláři **Přehled doručení** existují, je vytvořeno nové záhlaví deníku po kliknutí na **Zahájit doručení**.</span><span class="sxs-lookup"><span data-stu-id="06e93-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="06e93-110">Klikněte na **Řízení skladů** \> **Pravidelné** \> **Přehled příjezdů**.</span><span class="sxs-lookup"><span data-stu-id="06e93-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="06e93-111">V poli **Název nastavení** vyberte **Vratka** a klikněte na **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="06e93-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="06e93-112">Výsledky hledání můžete omezit použitím polí <STRONG>Rozsah</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="06e93-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="06e93-113">Přesné výsledky dosáhnete zadáním nebo výběrem čísla RMA v poli <STRONG>číslo RMA</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="06e93-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="06e93-114">Pokud chcete definovat a uložit sadu filtrů, které budou omezovat, která příchozí doručení se zobrazí, klikněte na kartu <STRONG>nastavení</STRONG>. Dostupné filtry zahrnují typy skladů a překladiště.</span><span class="sxs-lookup"><span data-stu-id="06e93-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="06e93-115">Vrácené objednávky nelze směšovat s jinými typy doručení ve formuláři <STRONG>Přehled doručení</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="06e93-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="06e93-116">Proto bude odkaz vždy na prodejní objednávku, ale žádné ID prodejní objednávky nebude uvedeno v záhlaví deníku.</span><span class="sxs-lookup"><span data-stu-id="06e93-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="06e93-117">V mřížce **Příjmy** vyhledejte řádek, který odpovídá vracené položce a pak zaškrtněte políčko ve sloupci **Vybrat pro doručení**.</span><span class="sxs-lookup"><span data-stu-id="06e93-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="06e93-118">Pokud chcete z vratky vyloučit určité řádky, například položky z původní objednávky, které nebyly obsaženy ve vratce, zrušte zaškrtnutí políček **Vybrat pro doručení** v tabulce **Řádky** v dolní části formuláře.</span><span class="sxs-lookup"><span data-stu-id="06e93-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="06e93-119">Klikněte na tlačítko **Spustit doručení** a vytvořte deník doručení.</span><span class="sxs-lookup"><span data-stu-id="06e93-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="06e93-120">Můžete vybrat několik vratek a zahrnout je do jednoho procesu doručení.</span><span class="sxs-lookup"><span data-stu-id="06e93-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="06e93-121">Všechny řádky vratky budou zkopírovány do odpovídajícího řádku deníku pro doručení položek.</span><span class="sxs-lookup"><span data-stu-id="06e93-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="06e93-122">Deník doručení můžete vytvořit také ručně pomocí formuláře <STRONG>Doručení zboží</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="06e93-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="06e93-123">Klikněte na **Řízení zásob** \> **Deníky** \> **Doručení položky** \> **Doručení položky**.</span><span class="sxs-lookup"><span data-stu-id="06e93-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="06e93-124">Vyberte deník doručení, který jste právě vytvořili, a potom kliknutím na **Řádky** otevřete formulář **Řádky deníku, umístění**.</span><span class="sxs-lookup"><span data-stu-id="06e93-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="06e93-125">Na kartě **Obecné** nastavte požadovanou hodnotu v poli **Množství**, pokud je to požadováno, a pak přiřaďte kód dispozice v poli **Kód dispozice**.</span><span class="sxs-lookup"><span data-stu-id="06e93-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="06e93-126">Alternativně můžete vybrat políčko **Správa karantény**, chcete-li vrácené zboží odesílat prostřednictvím procesu kontroly v souvislosti s karanténním příkazem.</span><span class="sxs-lookup"><span data-stu-id="06e93-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="06e93-127">Při odeslání vráceného zboží přes karanténu nelze zadat kód dispozice.</span><span class="sxs-lookup"><span data-stu-id="06e93-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="06e93-128">Klikněte na tlačítko **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="06e93-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="06e93-129">Pokud proces ověření proběhne bezchybně, klepněte na položku **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="06e93-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="06e93-130">Zaznamenat příjem vrácených položek ve formuláři Registrace</span><span class="sxs-lookup"><span data-stu-id="06e93-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="06e93-131">Jako alternativu k použití formuláře **Přehled doručení** můžete použít formulář **Registrace** pro registraci doručení vráceného zboží.</span><span class="sxs-lookup"><span data-stu-id="06e93-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="06e93-132">Klikněte na **Prodej a marketing** \> **Společné** \> **Objednávky vratky** \> **Všechny objednávky vratky**.</span><span class="sxs-lookup"><span data-stu-id="06e93-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="06e93-133">Vytvořte novou objednávku vratky nebo otevřete objednávku vratky ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="06e93-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="06e93-134">Na pevné záložce **Řádky** vyberte řádek vratky.</span><span class="sxs-lookup"><span data-stu-id="06e93-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="06e93-135">Klikněte na **Aktualizovat řádek** a potom na **Registrace**.</span><span class="sxs-lookup"><span data-stu-id="06e93-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="06e93-136">Přiřaďte kód dispozice v poli **Kód dispozice** a potom klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="06e93-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="06e93-137">Není možné odeslat položku ke kontrole jako karanténní objednávku pomocí formuláře <STRONG>Registrace</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="06e93-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="06e93-138">V mřížce **Transakce** vyberte transakci, která má být zaregistrována.</span><span class="sxs-lookup"><span data-stu-id="06e93-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="06e93-139">V mřížce **registrovat** klepněte na tlačítko **přidat**.</span><span class="sxs-lookup"><span data-stu-id="06e93-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="06e93-140">Opakujte předchozí dva kroky, dokud se všechny vrácené položky nezobrazí v mřížce **Registrovat**.</span><span class="sxs-lookup"><span data-stu-id="06e93-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="06e93-141">Klikněte na **Zaúčtovat vše**.</span><span class="sxs-lookup"><span data-stu-id="06e93-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="06e93-142">Viz také</span><span class="sxs-lookup"><span data-stu-id="06e93-142">See also</span></span>

<span data-ttu-id="06e93-143">[Přehled doručení (formulář)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="06e93-143">[Arrival overview (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span></span>

  



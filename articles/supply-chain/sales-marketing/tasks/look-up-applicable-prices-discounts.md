--- 
title: "Vyhledání platných cen a slev"
description: "Tento postup popisuje vyhledání ceny a/nebo slevy produktu, které jsou aktuálně platné pro určitého odběratele, aniž by byla vytvořena prodejní objednávka."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f372db3d2e358cde6a5e65b01f4dc499c69fe022
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="186c3-103">Vyhledání platných cen a slev</span><span class="sxs-lookup"><span data-stu-id="186c3-103">Look up applicable prices and discounts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="186c3-104">Tento postup popisuje vyhledání ceny a/nebo slevy produktu, které jsou aktuálně platné pro určitého odběratele, aniž by byla vytvořena prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="186c3-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="186c3-105">Postup vás provede konkrétním příkladem a aby bylo možné vybrat potřebné hodnoty, je nutné v příkladu použít ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="186c3-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="186c3-106">Vyhledání platné ceny</span><span class="sxs-lookup"><span data-stu-id="186c3-106">Find the applicable price</span></span>
1. <span data-ttu-id="186c3-107">Přejděte do nabídky Prodej a marketing > Ceny a slevy > Vyhledat ceny.</span><span class="sxs-lookup"><span data-stu-id="186c3-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="186c3-108">V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="186c3-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="186c3-109">V seznamu vyhledejte a vyberte odběratele US-001.</span><span class="sxs-lookup"><span data-stu-id="186c3-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="186c3-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="186c3-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="186c3-111">Do pole Číslo položky zadejte T0004.</span><span class="sxs-lookup"><span data-stu-id="186c3-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="186c3-112">Ve výchozím nastavení je pole Množství nastaveno na hodnotu 1.</span><span class="sxs-lookup"><span data-stu-id="186c3-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="186c3-113">Pokud však znáte velikost objednávky, kterou chce odběratel podat pro daný produkt, zadejte tuto hodnotu.</span><span class="sxs-lookup"><span data-stu-id="186c3-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="186c3-114">Tyto informace jsou relevantní, pokud mají obchodní smlouvy s odběratelem množstevní kategorie, takže v případě, že cena závisí na minimálním nakoupeném množství.</span><span class="sxs-lookup"><span data-stu-id="186c3-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="186c3-115">V poli Datum zadejte datum, kdy má odběratel podat objednávku.</span><span class="sxs-lookup"><span data-stu-id="186c3-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="186c3-116">Datem může být aktuální den nebo jakékoli budoucí datum.</span><span class="sxs-lookup"><span data-stu-id="186c3-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="186c3-117">Systém nyní vrátí cenu, která platí pro vybraný produkt při nákupu vybraným odběratelem ve vybrané datum a se zadaným množstvím.</span><span class="sxs-lookup"><span data-stu-id="186c3-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="186c3-118">Pokud by v tomto příkladu odběratel US-001 koupil dnes 1 jednotku produktu T0004, bylo by mu účtováno 350 CAD za jednotku.</span><span class="sxs-lookup"><span data-stu-id="186c3-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="186c3-119">Tato cena je převzata z existující a aktivní obchodní smlouvy s odběratelem.</span><span class="sxs-lookup"><span data-stu-id="186c3-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="186c3-120">Ostatní pole na stránce poskytují podrobnosti o ceně produktu a nákladech produktu (pokud to je nastaveno v základním produktu) a vypočtené ziskovosti.</span><span class="sxs-lookup"><span data-stu-id="186c3-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="186c3-121">Je-li vybrána možnost Zobrazit související varianty produktu, znamená to, že existují další obchodní smlouvy pro varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="186c3-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="186c3-122">Klikněte na políčko Zobrazit související varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="186c3-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="186c3-123">Zobrazí se seznam variant produktu a také informace o jejich dimenzích.</span><span class="sxs-lookup"><span data-stu-id="186c3-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="186c3-124">V seznamu označte řádek představující bílou barvu.</span><span class="sxs-lookup"><span data-stu-id="186c3-124">In the list, mark the line representing colour White.</span></span>
    * <span data-ttu-id="186c3-125">Všimněte si, že cena produktu je nyní jiná než cena zobrazená dříve, když nebyla zadána pro dimenzi.</span><span class="sxs-lookup"><span data-stu-id="186c3-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="186c3-126">Klikněte na možnost Zobrazit prodejní ceny.</span><span class="sxs-lookup"><span data-stu-id="186c3-126">Click View sales prices.</span></span>
    * <span data-ttu-id="186c3-127">Stránka Cena (prodej) zobrazí všechny obchodní smlouvy vztahující se k produktu, včetně jeho variant.</span><span class="sxs-lookup"><span data-stu-id="186c3-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="186c3-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="186c3-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="186c3-129">Vyhledání platné slevy</span><span class="sxs-lookup"><span data-stu-id="186c3-129">Find the applicable discount</span></span>
    * <span data-ttu-id="186c3-130">Ověřte, že pole Účet odběratele obsahuje číslo odběratele US-001.</span><span class="sxs-lookup"><span data-stu-id="186c3-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="186c3-131">Do pole Číslo položky zadejte T0012.</span><span class="sxs-lookup"><span data-stu-id="186c3-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="186c3-132">Ujistěte se, že je v poli Množství nastavena hodnota 1.</span><span class="sxs-lookup"><span data-stu-id="186c3-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="186c3-133">Následující podrobnosti o ceně zobrazené pro produkt T0012 pocházejí z jedné nebo více obchodních smluv: Jednotková cena je 1 000 CAD a procento slevy je 5.</span><span class="sxs-lookup"><span data-stu-id="186c3-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="186c3-134">Nastavte množství na hodnotu 20.</span><span class="sxs-lookup"><span data-stu-id="186c3-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="186c3-135">Vyšší objednané množství způsobí, že se řádková sleva, která bude nabídnuta odběrateli, změní z 5 na 7 procent.</span><span class="sxs-lookup"><span data-stu-id="186c3-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="186c3-136">Čistá částka se vypočítá na základě jednotkové ceny, slevy a celkového množství.</span><span class="sxs-lookup"><span data-stu-id="186c3-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="186c3-137">Klikněte na možnost Zobrazit řádkovou slevu.</span><span class="sxs-lookup"><span data-stu-id="186c3-137">Click View line discount.</span></span>
    * <span data-ttu-id="186c3-138">Jsou zde dvě smlouvy řádkových slev pro produkt T0012, kde je zadána sleva 5 procent pro množství na řádku objednávky od 1 do 10 a 7% sleva na množství objednávky vyšší než 10.</span><span class="sxs-lookup"><span data-stu-id="186c3-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="186c3-139">Všimněte si, že slevy platí pro skupinu produktů, v tomto příkladu to je kód skupiny 01, do které produkt T0012 patří.</span><span class="sxs-lookup"><span data-stu-id="186c3-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="186c3-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="186c3-140">Close the page.</span></span>



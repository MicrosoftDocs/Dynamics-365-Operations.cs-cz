--- 
title: "Zadávání prodejních smluv"
description: "Tato procedura popisuje, jak vytvořit prodejní smlouvu, která zavazuje jednoho ze zákazníků ke koupi produktu za smluvenou částku během času výměnou za zvláštní slevy."
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
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 943ae430b148670d248716c9ece21850bf7d2dfd
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="cd0a5-103">Zadávání prodejních smluv</span><span class="sxs-lookup"><span data-stu-id="cd0a5-103">Enter sales agreements</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd0a5-104">Tato procedura popisuje, jak vytvořit prodejní smlouvu, která zavazuje jednoho ze zákazníků ke koupi produktu za</span><span class="sxs-lookup"><span data-stu-id="cd0a5-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an</span></span>

<span data-ttu-id="cd0a5-105">smluvenou částku během času výměnou za zvláštní slevy.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-105">agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="cd0a5-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="cd0a5-107">Nastavení záhlaví prodejní smlouvy</span><span class="sxs-lookup"><span data-stu-id="cd0a5-107">Set up sales agreement header</span></span>
1. <span data-ttu-id="cd0a5-108">Přejděte na Prodej a marketing > Prodejní smlouvy > Prodejní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-108">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="cd0a5-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-109">Click New.</span></span>
3. <span data-ttu-id="cd0a5-110">V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cd0a5-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cd0a5-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cd0a5-113">V poli Klasifikace prodejní smlouvy kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-113">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cd0a5-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cd0a5-115">Rozbalte sekci Obecné.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-115">Expand the General section.</span></span>
9. <span data-ttu-id="cd0a5-116">V poli Výchozí závazek vyberte možnost „Závazek – hodnota produktu“.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-116">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="cd0a5-117">Typ závazku je povinné kritérium, které je nutné přiřadit ke smlouvě k definování způsobu plnění smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-117">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="cd0a5-118">Čtyři přednastavené typy umožňují nastavit cíl závazku odběratele vyjádřený jako množství nebo hodnota.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-118">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="cd0a5-119">Typ závazku množství lze použít pouze k určitému produktu, ale oba typy hodnot se vztahují na prodej určeného a neurčeného zboží.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-119">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="cd0a5-120">Do pole Datum vypršení platnosti nastavte datum na budoucí datum, kdy má vypršet platnost smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-120">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="cd0a5-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-121">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="cd0a5-122">Nastavení řádku závazku pro hodnotu produktu</span><span class="sxs-lookup"><span data-stu-id="cd0a5-122">Set up product value commitment lines</span></span>
1. <span data-ttu-id="cd0a5-123">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-123">Click Add line.</span></span>
2. <span data-ttu-id="cd0a5-124">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cd0a5-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cd0a5-126">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cd0a5-127">Typ závazku, který jste vybrali pro smlouvu, ovlivňuje druh informací, které lze zadat na řádky smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-127">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="cd0a5-128">Například u smlouvy založené na hodnotě je třeba určit celkovou čistou částku (v dohodnuté měně) za kterou se odběratel zavazuje koupit zboží od vás.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-128">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="cd0a5-129">V tomto příkladu nejsou pole Množství a Jednotky na řádku k dispozici vzhledem k tomu, že vytvoříte smlouvu pro zákazníka ke koupi produktu s konkrétní hodnotou.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-129">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="cd0a5-130">Do pole Částka čisté zadejte peněžní částku, za kterou se zákazník zavázal nakoupit.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-130">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="cd0a5-131">Do pole Procento slevy zadejte procentuální hodnotu, která bude použita pro řádky prodejní objednávky odběratele, které jsou propojeny s touto smlouvou.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-131">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="cd0a5-132">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-132">Expand the Line details section.</span></span>
8. <span data-ttu-id="cd0a5-133">Vyberte možnost Ano v poli Max je vynuceno.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-133">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="cd0a5-134">Výběr možnosti Max je vynuceno znamená, že celková částka všech řádků prodejní objednávky používající zvláštní ceny závazku, slevy nebo platební podmínky, nesmí překročit částku zadanou v závazku.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-134">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="cd0a5-135">Minimální a maximální částky určují rozsah hodnot, za které musí být realizován prodej u jednotlivých prodejních objednávek používajících vybranou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-135">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="cd0a5-136">Rozbalte část Záhlaví prodejní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-136">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="cd0a5-137">Pokud je stav smlouvy nastaven na Platné, prodejní objednávky nesmí být přidruženy ke smlouvě a proto nemohou přispívat k plnění dohody.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-137">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="cd0a5-138">V této fázi lze stav změnit ručně.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-138">You can change the status manually at this stage.</span></span> <span data-ttu-id="cd0a5-139">Stav by však normálně byl změněn při potvrzení smlouvy pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-139">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="cd0a5-140">V podokně akcí klepněte na možnost Prodejní smlouva.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-140">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="cd0a5-141">Klikněte na možnost Potvrzení.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-141">Click Confirmation.</span></span>
    * <span data-ttu-id="cd0a5-142">Ověřte, že možnost Označit smlouvu jako platnou je nastavena na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-142">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="cd0a5-143">Vyberte možnost Ano v poli Tisk sestavy.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-143">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="cd0a5-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-144">Click OK.</span></span>
14. <span data-ttu-id="cd0a5-145">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-145">Close the page.</span></span>
    * <span data-ttu-id="cd0a5-146">Smlouva je nyní platná a můžete zahájit propojení smlouvy s nákupními objednávkami odběratele protiúčtem vůči potvrzenému cíli.</span><span class="sxs-lookup"><span data-stu-id="cd0a5-146">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  



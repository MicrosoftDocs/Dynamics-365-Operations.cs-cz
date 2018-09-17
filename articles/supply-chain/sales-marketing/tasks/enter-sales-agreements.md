--- 
title: "Zadávání prodejních smluv"
description: "Tato procedura popisuje, jak vytvořit prodejní smlouvu, která zavazuje jednoho ze zákazníků ke koupi produktu za smluvenou částku během času výměnou za zvláštní slevy."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 025c9fe2f769f37b63bd79c6c3afedc31a955310
ms.contentlocale: cs-cz
ms.lasthandoff: 09/17/2018

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="519c1-103">Zadávání prodejních smluv</span><span class="sxs-lookup"><span data-stu-id="519c1-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="519c1-104">Tato procedura popisuje, jak vytvořit prodejní smlouvu, která zavazuje jednoho ze zákazníků ke koupi produktu za smluvenou částku během času výměnou za zvláštní slevy.</span><span class="sxs-lookup"><span data-stu-id="519c1-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="519c1-105">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="519c1-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="519c1-106">Nastavení záhlaví prodejní smlouvy</span><span class="sxs-lookup"><span data-stu-id="519c1-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="519c1-107">Přejděte na Prodej a marketing > Prodejní smlouvy > Prodejní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="519c1-107">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="519c1-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="519c1-108">Click New.</span></span>
3. <span data-ttu-id="519c1-109">V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="519c1-109">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="519c1-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="519c1-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="519c1-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="519c1-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="519c1-112">V poli Klasifikace prodejní smlouvy kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="519c1-112">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="519c1-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="519c1-113">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="519c1-114">Rozbalte sekci Obecné.</span><span class="sxs-lookup"><span data-stu-id="519c1-114">Expand the General section.</span></span>
9. <span data-ttu-id="519c1-115">V poli Výchozí závazek vyberte možnost „Závazek – hodnota produktu“.</span><span class="sxs-lookup"><span data-stu-id="519c1-115">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="519c1-116">Typ závazku je povinné kritérium, které je nutné přiřadit ke smlouvě k definování způsobu plnění smlouvy.</span><span class="sxs-lookup"><span data-stu-id="519c1-116">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="519c1-117">Čtyři přednastavené typy umožňují nastavit cíl závazku odběratele vyjádřený jako množství nebo hodnota.</span><span class="sxs-lookup"><span data-stu-id="519c1-117">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="519c1-118">Typ závazku množství lze použít pouze k určitému produktu, ale oba typy hodnot se vztahují na prodej určeného a neurčeného zboží.</span><span class="sxs-lookup"><span data-stu-id="519c1-118">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="519c1-119">Do pole Datum vypršení platnosti nastavte datum na budoucí datum, kdy má vypršet platnost smlouvy.</span><span class="sxs-lookup"><span data-stu-id="519c1-119">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="519c1-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="519c1-120">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="519c1-121">Nastavení řádku závazku pro hodnotu produktu</span><span class="sxs-lookup"><span data-stu-id="519c1-121">Set up product value commitment lines</span></span>
1. <span data-ttu-id="519c1-122">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="519c1-122">Click Add line.</span></span>
2. <span data-ttu-id="519c1-123">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="519c1-123">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="519c1-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="519c1-124">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="519c1-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="519c1-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="519c1-126">Typ závazku, který jste vybrali pro smlouvu, ovlivňuje druh informací, které lze zadat na řádky smlouvy.</span><span class="sxs-lookup"><span data-stu-id="519c1-126">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="519c1-127">Například u smlouvy založené na hodnotě je třeba určit celkovou čistou částku (v dohodnuté měně) za kterou se odběratel zavazuje koupit zboží od vás.</span><span class="sxs-lookup"><span data-stu-id="519c1-127">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="519c1-128">V tomto příkladu nejsou pole Množství a Jednotky na řádku k dispozici vzhledem k tomu, že vytvoříte smlouvu pro zákazníka ke koupi produktu s konkrétní hodnotou.</span><span class="sxs-lookup"><span data-stu-id="519c1-128">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="519c1-129">Do pole Částka čisté zadejte peněžní částku, za kterou se zákazník zavázal nakoupit.</span><span class="sxs-lookup"><span data-stu-id="519c1-129">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="519c1-130">Do pole Procento slevy zadejte procentuální hodnotu, která bude použita pro řádky prodejní objednávky odběratele, které jsou propojeny s touto smlouvou.</span><span class="sxs-lookup"><span data-stu-id="519c1-130">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="519c1-131">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="519c1-131">Expand the Line details section.</span></span>
8. <span data-ttu-id="519c1-132">Vyberte možnost Ano v poli Max je vynuceno.</span><span class="sxs-lookup"><span data-stu-id="519c1-132">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="519c1-133">Výběr možnosti Max je vynuceno znamená, že celková částka všech řádků prodejní objednávky používající zvláštní ceny závazku, slevy nebo platební podmínky, nesmí překročit částku zadanou v závazku.</span><span class="sxs-lookup"><span data-stu-id="519c1-133">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="519c1-134">Minimální a maximální částky určují rozsah hodnot, za které musí být realizován prodej u jednotlivých prodejních objednávek používajících vybranou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="519c1-134">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="519c1-135">Rozbalte část Záhlaví prodejní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="519c1-135">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="519c1-136">Pokud je stav smlouvy nastaven na Platné, prodejní objednávky nesmí být přidruženy ke smlouvě a proto nemohou přispívat k plnění dohody.</span><span class="sxs-lookup"><span data-stu-id="519c1-136">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="519c1-137">V této fázi lze stav změnit ručně.</span><span class="sxs-lookup"><span data-stu-id="519c1-137">You can change the status manually at this stage.</span></span> <span data-ttu-id="519c1-138">Stav by však normálně byl změněn při potvrzení smlouvy pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="519c1-138">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="519c1-139">V podokně akcí klepněte na možnost Prodejní smlouva.</span><span class="sxs-lookup"><span data-stu-id="519c1-139">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="519c1-140">Klikněte na možnost Potvrzení.</span><span class="sxs-lookup"><span data-stu-id="519c1-140">Click Confirmation.</span></span>
    * <span data-ttu-id="519c1-141">Ověřte, že možnost Označit smlouvu jako platnou je nastavena na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="519c1-141">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="519c1-142">Vyberte možnost Ano v poli Tisk sestavy.</span><span class="sxs-lookup"><span data-stu-id="519c1-142">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="519c1-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="519c1-143">Click OK.</span></span>
14. <span data-ttu-id="519c1-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="519c1-144">Close the page.</span></span>
    * <span data-ttu-id="519c1-145">Smlouva je nyní platná a můžete zahájit propojení smlouvy s nákupními objednávkami odběratele protiúčtem vůči potvrzenému cíli.</span><span class="sxs-lookup"><span data-stu-id="519c1-145">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  



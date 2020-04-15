---
title: Zadávání prodejních smluv
description: Toto téma vysvětluje, jak vytvořit prodejní smlouvu, která zavazuje jednoho ze zákazníků ke koupi produktu za smluvenou částku během času výměnou za zvláštní slevy.
author: omulvad
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06d251992c7facca471ac893e5a0fee333e0cbed
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148646"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="1e5a5-103">Zadávání prodejních smluv</span><span class="sxs-lookup"><span data-stu-id="1e5a5-103">Enter sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1e5a5-104">Toto téma vysvětluje, jak vytvořit prodejní smlouvu, která zavazuje jednoho ze zákazníků ke koupi produktu za smluvenou částku během času výměnou za zvláštní slevy.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-104">This topic explains how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="1e5a5-105">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="1e5a5-106">Nastavení záhlaví prodejní smlouvy</span><span class="sxs-lookup"><span data-stu-id="1e5a5-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="1e5a5-107">V navigačním podokně přejděte na **Moduly > Prodej a marketing > Prodejní smlouvy > Prodejní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-107">In the navigation pane, go to **Modules > Sales and marketing > Sales agreements > Sales agreements**.</span></span>
2. <span data-ttu-id="1e5a5-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-108">Select **New**.</span></span>
3. <span data-ttu-id="1e5a5-109">V poli **Účet odběratele** vyberte požadovaný záznam v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-109">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="1e5a5-110">V poli **Klasifikace prodejní smlouvy** vyberte požadovaný záznam v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-110">In the **Sales agreement classification** field, select the desired record from the drop-down menu.</span></span>
5. <span data-ttu-id="1e5a5-111">Rozbalte sekci **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-111">Expand the **General** section.</span></span>
6. <span data-ttu-id="1e5a5-112">V poli **Výchozí závazek** vyberte možnost **Závazek – hodnota produktu**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-112">In the **Default commitment** field, select **Product value commitment**.</span></span> <span data-ttu-id="1e5a5-113">Typ závazku je povinné kritérium, které je nutné přiřadit ke smlouvě k definování způsobu plnění smlouvy.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-113">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="1e5a5-114">Čtyři přednastavené typy umožňují nastavit cíl závazku odběratele vyjádřený jako množství nebo hodnota.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-114">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="1e5a5-115">Typ závazku množství lze použít pouze k určitému produktu, ale oba typy hodnot se vztahují na prodej určeného a neurčeného zboží.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-115">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
7. <span data-ttu-id="1e5a5-116">Do pole **Datum vypršení platnosti** nastavte datum na budoucí datum, kdy má vypršet platnost smlouvy.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-116">In the **Expiration date** field, set the date to a future date when you want the agreement to expire.</span></span>
8. <span data-ttu-id="1e5a5-117">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-117">Select **OK**.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="1e5a5-118">Nastavení řádku závazku pro hodnotu produktu</span><span class="sxs-lookup"><span data-stu-id="1e5a5-118">Set up product value commitment lines</span></span>
1. <span data-ttu-id="1e5a5-119">Vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-119">Select **Add line**.</span></span>
2. <span data-ttu-id="1e5a5-120">V poli **Číslo položky** vyberte z rozevírací nabídky požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-120">In the **Item number** field, select the desired record from the drop-down menu.</span></span> <span data-ttu-id="1e5a5-121">Typ závazku, který jste vybrali pro smlouvu, ovlivňuje druh informací, které lze zadat na řádky smlouvy.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-121">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="1e5a5-122">Například u smlouvy založené na hodnotě je třeba určit celkovou čistou částku (v dohodnuté měně) za kterou se odběratel zavazuje koupit zboží od vás.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-122">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="1e5a5-123">V tomto příkladu nejsou pole **Množství** a **Jednotka** na řádku k dispozici vzhledem k tomu, že vytvoříte smlouvu pro zákazníka ke koupi produktu s konkrétní hodnotou.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-123">In this example the **Quantity** and **Unit** fields on the line are unavailable because you're creating an agreement for the customer to buy a specific value of a product.</span></span>   
3. <span data-ttu-id="1e5a5-124">Do pole **Čistá částka** zadejte peněžní částku, za kterou se zákazník zavázal nakoupit.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-124">In the **Net amount** field, enter the monetary amount that the customer has committed to buying.</span></span>
4. <span data-ttu-id="1e5a5-125">Do pole **Procento slevy** zadejte procentuální hodnotu, která bude použita pro řádky prodejní objednávky odběratele, které jsou propojeny s touto smlouvou.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-125">In the **Discount percent** field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
5. <span data-ttu-id="1e5a5-126">Rozbalte sekci **Podrobnosti řádku**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-126">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="1e5a5-127">Vyberte možnost **Ano** v poli **Max** je vynuceno.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-127">Select **Yes** in the **Max is enforced** field.</span></span>
    - <span data-ttu-id="1e5a5-128">Výběr možnosti **Max je vynuceno** znamená, že celková částka všech řádků prodejní objednávky používající zvláštní ceny závazku, slevy nebo platební podmínky, nesmí překročit částku zadanou v závazku.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-128">Selecting **Max is enforced** means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    - <span data-ttu-id="1e5a5-129">Minimální a maximální částky určují rozsah hodnot, za které musí být realizován prodej u jednotlivých prodejních objednávek používajících vybranou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-129">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
7. <span data-ttu-id="1e5a5-130">Rozbalte část **Záhlaví prodejní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-130">Expand the **Sales agreement header** section.</span></span> <span data-ttu-id="1e5a5-131">Pokud je stav smlouvy nastaven na **Platná**, prodejní objednávky nesmí být přidruženy ke smlouvě a proto nemohou přispívat k plnění dohody.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-131">Unless the status of the agreement is set to **Effective**, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="1e5a5-132">V této fázi lze stav změnit ručně.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-132">You can change the status manually at this stage.</span></span> <span data-ttu-id="1e5a5-133">Stav by však normálně byl změněn při potvrzení smlouvy pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-133">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
8. <span data-ttu-id="1e5a5-134">V podokně akcí zvolte možnost **Prodejní smlouva**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-134">On the Action Pane, select **Sales agreement**.</span></span>
9. <span data-ttu-id="1e5a5-135">Vyberte **Potvrzení**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-135">Select **Confirmation**.</span></span> <span data-ttu-id="1e5a5-136">Ověřte, že možnost **Označit smlouvu jako platnou** je nastavena na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-136">Make sure that the **Mark agreement as effective** option is set to **Yes**.</span></span>  
10. <span data-ttu-id="1e5a5-137">Vyberte možnost **Ano** v poli **Tisk sestavy**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-137">Select **Yes** in the **Print report** field.</span></span>
11. <span data-ttu-id="1e5a5-138">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-138">Select **OK**.</span></span>
12. <span data-ttu-id="1e5a5-139">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-139">Close the page.</span></span> <span data-ttu-id="1e5a5-140">Smlouva je nyní platná.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-140">The agreement is now effective.</span></span> <span data-ttu-id="1e5a5-141">Můžete zahájit propojení smlouvy s objednávkami odběratele protiúčtem vůči potvrzenému cíli.</span><span class="sxs-lookup"><span data-stu-id="1e5a5-141">You can start linking the customer's orders to the agreement to offset against the committed target.</span></span>  


---
title: Sledování položky nebo suroviny
description: Tento postup uvádí použití sledování položky k určení, kde bylo zboží nebo suroviny použity nebo jsou používány.
author: pjacobse
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a3b2ab752089b2c60c5c5e02cb2c558c17dcf8b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829805"
---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="2ef19-103">Sledování položky nebo suroviny</span><span class="sxs-lookup"><span data-stu-id="2ef19-103">Trace an item or raw material</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ef19-104">Tento postup uvádí použití sledování položky k určení, kde bylo zboží nebo suroviny použity nebo jsou používány.</span><span class="sxs-lookup"><span data-stu-id="2ef19-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="2ef19-105">Pomocí tohoto postupu lze identifikovat zboží, vysledovat ho zpět ke zdroji, a potom jej sledovat dopředu přes výrobu a prodeji hotového výrobku.</span><span class="sxs-lookup"><span data-stu-id="2ef19-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="2ef19-106">Tento proces použít k analýze ovlivněných odběratelů, dotyčných prodejních objednávek a další.</span><span class="sxs-lookup"><span data-stu-id="2ef19-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="2ef19-107">Tato procedura používá data ukázkové společnosti USP2.</span><span class="sxs-lookup"><span data-stu-id="2ef19-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="2ef19-108">Sledujte položky zpětně za použití známého čísla dávky</span><span class="sxs-lookup"><span data-stu-id="2ef19-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="2ef19-109">V **Navigačním podokně** přejděte na **Moduly > Řízení zásob > Dotazy a sestavy > Sledovací dimenze > Sledování zboží**.</span><span class="sxs-lookup"><span data-stu-id="2ef19-109">In the **Navigation pane**, go to **Modules > Inventory management > Inquiries and reports > Tracking dimensions > Item tracing**.</span></span>
2. <span data-ttu-id="2ef19-110">V poli **Číslo položky** vyberte „P9100“.</span><span class="sxs-lookup"><span data-stu-id="2ef19-110">In the **Item number** field, select 'P9100'.</span></span>
3. <span data-ttu-id="2ef19-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2ef19-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2ef19-112">V poli **Dopředu nebo dozadu** vyberte „Dozadu“.</span><span class="sxs-lookup"><span data-stu-id="2ef19-112">In the **Forward or backward** field, select 'Backward'.</span></span>
5. <span data-ttu-id="2ef19-113">V poli **Číslo dávky** vyberte „as-12-344-01“.</span><span class="sxs-lookup"><span data-stu-id="2ef19-113">In the **Batch number** field, select 'as-12-344-01'.</span></span>
6. <span data-ttu-id="2ef19-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2ef19-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2ef19-115">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ef19-115">Click **OK**.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="2ef19-116">Identifikujte zboží, sledujte ho dopředu a proveďte analýzu</span><span class="sxs-lookup"><span data-stu-id="2ef19-116">Identify an item, trace it forward, and make an analysis</span></span>

<span data-ttu-id="2ef19-117">Nejvyšší uzel stromové struktury představuje množství vybraných položek na skladě a dávky.</span><span class="sxs-lookup"><span data-stu-id="2ef19-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="2ef19-118">Je nutné rozbalit uzly ve stromu a vyhledat tak položku, u které má být provedeno dopředné sledování.</span><span class="sxs-lookup"><span data-stu-id="2ef19-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="2ef19-119">Ve stromovém zobrazení rozbalte níže popsané uzly a pak vyberte poslední uzel.</span><span class="sxs-lookup"><span data-stu-id="2ef19-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    
    <span data-ttu-id="2ef19-120">Rozbalení „P9100 / 1 / 10 / as-12-344-01 ● 2 sudy ● 7,00 galonů \P9100 ● Vyskladněno ● Prodejní objednávka 000072 ● 22. 12. 2015 ● -1 sud ● -4,00 galony ● Pracoviště = 1, sklad = 10, číslo dávky = as-12-344-01 \P9100 ● Výroba B-000050 ● 9. 12. 2015 ● 7 sudů ● 27,00 galonů ● Pracoviště = 1, sklad = 10, číslo dávky = as-12-344-01 ● Vedlejší produkty: P9101“ a pak vyberte uzel.</span><span class="sxs-lookup"><span data-stu-id="2ef19-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="2ef19-121">Ve stromovém zobrazení rozbalte níže popsaný uzel a pak jej vyberte.</span><span class="sxs-lookup"><span data-stu-id="2ef19-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    
    <span data-ttu-id="2ef19-122">Od uzlu, který jste právě vybrali, rozbalte „M9103 ● Řádek výroby B-000050 ● 9. 12. 2015 ● -160,00 liber ● velikost = 70, barva = OK, pracoviště = 1, sklad = 10, číslo dávky = App01“ a pak vyberte daný uzel.</span><span class="sxs-lookup"><span data-stu-id="2ef19-122">Starting from the node that you've just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="2ef19-123">Klepněte na **Sledovat z uzlu**.</span><span class="sxs-lookup"><span data-stu-id="2ef19-123">Click **Trace from node**.</span></span>
4. <span data-ttu-id="2ef19-124">Klikněte na **Vpřed**.</span><span class="sxs-lookup"><span data-stu-id="2ef19-124">Click **Forward**.</span></span>
5. <span data-ttu-id="2ef19-125">V **Podokně akcí** klepněte na možnost **Sledování**.</span><span class="sxs-lookup"><span data-stu-id="2ef19-125">On the **Action Pane**, click **Tracing**.</span></span>
    
    <span data-ttu-id="2ef19-126">Existuje několik možností sledování, které poskytují informace o odběratelích, a které jsou ovlivněny vámi sledovaným zbožím a prodejními objednávkami souvisejícími s položkou, která byla nebo nebyla zatím expedována.</span><span class="sxs-lookup"><span data-stu-id="2ef19-126">There are several tracing options which provide information about the customers impacted by the item that you're tracing, and the sales orders related to the item which have and haven't been shipped.</span></span>   
6. <span data-ttu-id="2ef19-127">Klikněte na **Zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="2ef19-127">Click **Customers**.</span></span>
7. <span data-ttu-id="2ef19-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2ef19-128">Close the page.</span></span>
8. <span data-ttu-id="2ef19-129">V **Podokně akcí** klepněte na možnost **Sledování**.</span><span class="sxs-lookup"><span data-stu-id="2ef19-129">On the **Action Pane**, click **Tracing**.</span></span>
9. <span data-ttu-id="2ef19-130">Klikněte na **Prodejní objednávky za expedované zboží**.</span><span class="sxs-lookup"><span data-stu-id="2ef19-130">Click **Shipped sales orders**.</span></span>
10. <span data-ttu-id="2ef19-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2ef19-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
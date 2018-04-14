---
title: "Sledování zásob dodávky s použitím dodavatelské spolupráce"
description: "Tato procedura ukazuje, jak použít spolupráci dodavatele k zobrazení informací o úrovni zásob produktu, který jste umístili v zásilce pro zákazníka."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f071b9c2358e6720bd9c69e4ed7be6e059521113
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="24901-103">Sledování zásob dodávky s použitím dodavatelské spolupráce</span><span class="sxs-lookup"><span data-stu-id="24901-103">Monitor consignment inventory using vendor collaboration</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="24901-104">Tato procedura ukazuje, jak použít spolupráci dodavatele k zobrazení informací o úrovni zásob produktu, který jste umístili v zásilce pro zákazníka.</span><span class="sxs-lookup"><span data-stu-id="24901-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="24901-105">Můžete také sledovat spotřebu zásob, když zákazník převezme vlastnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="24901-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="24901-106">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="24901-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="24901-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="24901-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="24901-108">Zobrazení spotřebovaných zásob</span><span class="sxs-lookup"><span data-stu-id="24901-108">View consumed inventory</span></span>
1. <span data-ttu-id="24901-109">Přejděte do nabídky Spolupráce dodavatele > Zásoby dodávky > Produkty přijaté ze zásob dodávky.</span><span class="sxs-lookup"><span data-stu-id="24901-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="24901-110">V seznamu jsou uvedeny řádky příjemky, které byly vytvořeny při změně vlastnictví šarže zásob dodávky z dodavatele na odběratele.</span><span class="sxs-lookup"><span data-stu-id="24901-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="24901-111">Bude pravděpodobně nutné přejít doprava, chcete-li zobrazit množství a další informace.</span><span class="sxs-lookup"><span data-stu-id="24901-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="24901-112">Informace v tomto seznamu slouží ke generování faktur pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="24901-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="24901-113">Můžete také exportovat data do aplikace Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="24901-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="24901-114">Klikněte na možnost Zobrazit nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="24901-114">Click View purchase order.</span></span>
3. <span data-ttu-id="24901-115">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="24901-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="24901-116">Řádek je označen jako Zásilka a oddílu v záhlaví ukazuje, že má nákupní objednávka stav Přijato.</span><span class="sxs-lookup"><span data-stu-id="24901-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="24901-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="24901-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="24901-118">Zobrazení zásob na skladě</span><span class="sxs-lookup"><span data-stu-id="24901-118">View on-hand inventory</span></span>
1. <span data-ttu-id="24901-119">Přejděte do nabídky Spolupráce dodavatele > Zásoby dodávky > Zásoby dodávky na skladě.</span><span class="sxs-lookup"><span data-stu-id="24901-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="24901-120">Stránka Zásoby dodávky na skladě ukazuje zásobu, kterou vlastníte ve skladu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="24901-120">The On-hand consignment inventory page shows the stock that you own at the customer’s warehouse.</span></span> <span data-ttu-id="24901-121">Další dimenze, například pracoviště a sklad, můžete zobrazit klepnutím na kartu Zobrazit dimenze.</span><span class="sxs-lookup"><span data-stu-id="24901-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   


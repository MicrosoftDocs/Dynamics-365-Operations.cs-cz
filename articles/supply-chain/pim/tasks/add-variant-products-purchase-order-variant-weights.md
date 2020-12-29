---
title: Přidávání variant produktů do nákupních objednávek s použitím různých hmotností
description: Tato procedura vás provede kroky použití hmotností variant pro automatické vyplnění řádků nákupní objednávky pro každou variantu produktu.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27ff3784074a36d073930ba68c8dec8b1121356e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424217"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="ff2db-103">Přidávání variant produktů do nákupních objednávek s použitím různých hmotností</span><span class="sxs-lookup"><span data-stu-id="ff2db-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff2db-104">Tato procedura vás provede kroky použití hmotností variant pro automatické vyplnění řádků nákupní objednávky pro každou variantu produktu.</span><span class="sxs-lookup"><span data-stu-id="ff2db-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="ff2db-105">Když vyberete množství produktu, které chcete nakoupit, budou vytvořeny řádky nákupní objednávky pro všechny varianty produktu s navrženým množstvím podle hmotnosti nakonfigurované pro varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="ff2db-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="ff2db-106">Tento postup neobsahuje postup konfigurace hodnot hmotnosti dimenzí produktů a variant produktu.</span><span class="sxs-lookup"><span data-stu-id="ff2db-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="ff2db-107">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="ff2db-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ff2db-108">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ff2db-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="ff2db-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ff2db-109">Click New.</span></span>
3. <span data-ttu-id="ff2db-110">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="ff2db-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ff2db-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ff2db-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ff2db-112">Přepněte rozšíření oddílu Obecné.</span><span class="sxs-lookup"><span data-stu-id="ff2db-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="ff2db-113">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="ff2db-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ff2db-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ff2db-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ff2db-115">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="ff2db-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ff2db-116">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ff2db-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ff2db-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ff2db-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ff2db-118">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ff2db-118">Click OK.</span></span>
12. <span data-ttu-id="ff2db-119">Přepněte rozšíření oddílu Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="ff2db-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="ff2db-120">Klikněte na kartu Varianty.</span><span class="sxs-lookup"><span data-stu-id="ff2db-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="ff2db-121">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="ff2db-121">Click Add line.</span></span>
15. <span data-ttu-id="ff2db-122">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ff2db-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="ff2db-123">Do pole Číslo zboží zadejte „0140“.</span><span class="sxs-lookup"><span data-stu-id="ff2db-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="ff2db-124">Nastavte množství na hodnotu 1000.</span><span class="sxs-lookup"><span data-stu-id="ff2db-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="ff2db-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ff2db-125">Click Save.</span></span>


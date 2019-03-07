---
title: Vytvoření a správa blokování zásob
description: Tento postup popisuje, jak zabránit u fyzických zásob na skladě rezervace jinými odchozími zdrojovými dokumenty pomocí blokování zásob.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09789dc0b89f8bd36cca9b3e5be366bf17246243
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "322253"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="4706f-103">Vytvoření a správa blokování zásob</span><span class="sxs-lookup"><span data-stu-id="4706f-103">Create and maintain an inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4706f-104">Tento postup popisuje, jak zabránit u fyzických zásob na skladě rezervace jinými odchozími zdrojovými dokumenty pomocí blokování zásob.</span><span class="sxs-lookup"><span data-stu-id="4706f-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="4706f-105">Postup můžete spustit s ukázkovými daty společnosti USMF s ukázkovými hodnotami, které jsou zobrazeny.</span><span class="sxs-lookup"><span data-stu-id="4706f-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="4706f-106">Před zahájením tohoto postupu je třeba mít k dispozici položku s dostupnými fyzickými zásobami na skladě.</span><span class="sxs-lookup"><span data-stu-id="4706f-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="4706f-107">Vytvoření blokování zásob</span><span class="sxs-lookup"><span data-stu-id="4706f-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="4706f-108">Přejděte do možnosti Řízení zásob > Periodické úkoly > Blokování zásob.</span><span class="sxs-lookup"><span data-stu-id="4706f-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="4706f-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4706f-109">Click New.</span></span>
3. <span data-ttu-id="4706f-110">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="4706f-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4706f-111">Ze seznamu vyberte položku, kterou chcete vybrat.</span><span class="sxs-lookup"><span data-stu-id="4706f-111">In the list, select the item you want to choose.</span></span> 
    * <span data-ttu-id="4706f-112">Vyberte číslo položky v rámci fyzických zásob na skladě, kterou chcete blokovat.</span><span class="sxs-lookup"><span data-stu-id="4706f-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="4706f-113">Pokud používáte USMF, můžete vybrat položku M9201.</span><span class="sxs-lookup"><span data-stu-id="4706f-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="4706f-114">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="4706f-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="4706f-115">Používáte-li položku M9201, musíte vybrat číslo menší než 200.</span><span class="sxs-lookup"><span data-stu-id="4706f-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="4706f-116">Rozbalte oddíl Dimenze zásob.</span><span class="sxs-lookup"><span data-stu-id="4706f-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="4706f-117">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="4706f-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="4706f-118">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="4706f-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4706f-119">Pokud používáte položku M9201, můžete vybrat sklad 51.</span><span class="sxs-lookup"><span data-stu-id="4706f-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="4706f-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4706f-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="4706f-121">Aktualizace podmínek pro blokování zásob</span><span class="sxs-lookup"><span data-stu-id="4706f-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="4706f-122">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="4706f-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="4706f-123">Aktualizujte pole s množstvím zásob podle blokovaného množství.</span><span class="sxs-lookup"><span data-stu-id="4706f-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="4706f-124">V poli Očekávané datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="4706f-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="4706f-125">Můžete určit, zda se u blokovaných zásob očekává uvolnění pro rezervaci přiřazením předpokládaného data.</span><span class="sxs-lookup"><span data-stu-id="4706f-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="4706f-126">Pokud vyberete možnost Očekávané příjmy pro blokování zásob, zobrazí se toto datum na očekávané transakci, protože se jedná o výchozí údaj při ručním vytváření blokování.</span><span class="sxs-lookup"><span data-stu-id="4706f-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="4706f-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4706f-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="4706f-128">Odebrání blokování zásob</span><span class="sxs-lookup"><span data-stu-id="4706f-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="4706f-129">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="4706f-129">Click Delete.</span></span>
2. <span data-ttu-id="4706f-130">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="4706f-130">Click Yes.</span></span>
3. <span data-ttu-id="4706f-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4706f-131">Close the page.</span></span>


---
title: Vytvoření a správa blokování zásob
description: Toto téma popisuje, jak použít blokování zásob k zabránění u fyzických zásob na skladě rezervaci jinými odchozími zdrojovými dokumenty.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956151"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="934d1-103">Vytvoření a správa blokování zásob</span><span class="sxs-lookup"><span data-stu-id="934d1-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="934d1-104">Toto téma popisuje, jak použít blokování zásob k zabránění u fyzických zásob na skladě rezervaci jinými odchozími zdrojovými dokumenty.</span><span class="sxs-lookup"><span data-stu-id="934d1-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="934d1-105">Před zahájením tohoto postupu je třeba mít k dispozici položku s dostupnými fyzickými zásobami na skladě.</span><span class="sxs-lookup"><span data-stu-id="934d1-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="934d1-106">Blokovat zásoby</span><span class="sxs-lookup"><span data-stu-id="934d1-106">Block inventory</span></span>

<span data-ttu-id="934d1-107">Chcete-li vytvořit záznam blokování zásob tak, aby byly blokované zásoby, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="934d1-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="934d1-108">Přejděte do možnosti **Řízení zásob \> Periodické úkoly \> Blokování zásob**.</span><span class="sxs-lookup"><span data-stu-id="934d1-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="934d1-109">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="934d1-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="934d1-110">V záhlaví nového blokujícího záznamu nastavte pole **Číslo položky** na položku, kterou chcete blokovat, a zadejte popis.</span><span class="sxs-lookup"><span data-stu-id="934d1-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="934d1-111">Na pevné záložce **Obecné** v poli **Množství** zadejte počet položek, které mají být zablokovány.</span><span class="sxs-lookup"><span data-stu-id="934d1-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="934d1-112">Na rychlé záložce **Dimenze zásob** určete místo a sklad, kde se aktuálně nacházejí položky, které chcete blokovat.</span><span class="sxs-lookup"><span data-stu-id="934d1-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="934d1-113">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="934d1-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="934d1-114">Aktualizace podmínek pro blokování zásob</span><span class="sxs-lookup"><span data-stu-id="934d1-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="934d1-115">Chcete-li aktualizovat záznam blokování inventáře, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="934d1-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="934d1-116">Přejděte do možnosti **Řízení zásob \> Periodické úkoly \> Blokování zásob**.</span><span class="sxs-lookup"><span data-stu-id="934d1-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="934d1-117">V podokně seznamu vyberte příslušný záznam blokování.</span><span class="sxs-lookup"><span data-stu-id="934d1-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="934d1-118">Podle potřeby záznam upravte.</span><span class="sxs-lookup"><span data-stu-id="934d1-118">Edit the record as required.</span></span> <span data-ttu-id="934d1-119">Například můžete chtít změnit hodnotu **Očekávané datum** k určení, že se blokovaných zásob očekává uvolnění pro rezervaci.</span><span class="sxs-lookup"><span data-stu-id="934d1-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="934d1-120">Pokud je vybrána **Očekávané příjmy**, datum se zobrazí u očekávané transakce.</span><span class="sxs-lookup"><span data-stu-id="934d1-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="934d1-121">(Možnost **Očekávané příjmy** je při ručním vytvoření blokujícího záznamu vybrána ve výchozím nastavení.)</span><span class="sxs-lookup"><span data-stu-id="934d1-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="934d1-122">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="934d1-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="934d1-123">Odblokování zásob</span><span class="sxs-lookup"><span data-stu-id="934d1-123">Unblock inventory</span></span>

<span data-ttu-id="934d1-124">Chcete-li odstranit záznam blokování zásob tak, aby byly zásoby odblokovány, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="934d1-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="934d1-125">Přejděte do možnosti **Řízení zásob \> Periodické úkoly \> Blokování zásob**.</span><span class="sxs-lookup"><span data-stu-id="934d1-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="934d1-126">V podokně seznamu vyberte příslušný záznam blokování.</span><span class="sxs-lookup"><span data-stu-id="934d1-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="934d1-127">V podokně Akce zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="934d1-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="934d1-128">Budete vyzvání k potvrzení operace.</span><span class="sxs-lookup"><span data-stu-id="934d1-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="934d1-129">Pokračujte výběrem tlačítka **Ano**.</span><span class="sxs-lookup"><span data-stu-id="934d1-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="934d1-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="934d1-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

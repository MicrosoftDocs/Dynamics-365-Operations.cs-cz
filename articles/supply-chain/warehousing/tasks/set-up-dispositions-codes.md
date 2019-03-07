---
title: Nastavení dispozičních kódů
description: Tento postup se zaměřuje na nastavení dispozičního kódu, který lze použít v mobilním zařízení pro proces příjmu vratky.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85402e05d55367da5fe89b242ad8eafc727b441e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "324116"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="baf15-103">Nastavení dispozičních kódů</span><span class="sxs-lookup"><span data-stu-id="baf15-103">Set up dispositions codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="baf15-104">Tento postup se zaměřuje na nastavení dispozičního kódu, který lze použít v mobilním zařízení pro proces příjmu vratky.</span><span class="sxs-lookup"><span data-stu-id="baf15-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="baf15-105">Dispoziční kódy je sada pravidel, které lze použít při příjmu položek.</span><span class="sxs-lookup"><span data-stu-id="baf15-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="baf15-106">Například když uživatel při práci používá mobilní zařízení k příjmu položek, které byly poškozené, uživatel musí naskenovat dispoziční kód pro poškozené položky.</span><span class="sxs-lookup"><span data-stu-id="baf15-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="baf15-107">Podle naskenovaného dispozičního kódu lze určit stav zásob přijatého zboží, šablonu práce a směrnici umístění.</span><span class="sxs-lookup"><span data-stu-id="baf15-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="baf15-108">Pro proces Příjem nákupní objednávky a Vykázat výrobní zakázku jako dokončenou lze dispoziční kód použít volitelně.</span><span class="sxs-lookup"><span data-stu-id="baf15-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="baf15-109">Pokud v případě procesu příjmu prodejní vratky jsou položky registrovány pomocí mobilního zařízení, použití dispozičního kódu je povinné.</span><span class="sxs-lookup"><span data-stu-id="baf15-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="baf15-110">Tento průvodce byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="baf15-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="baf15-111">Tento postup je určen pro vedoucího skladu.</span><span class="sxs-lookup"><span data-stu-id="baf15-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="baf15-112">Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Dispoziční kódy.</span><span class="sxs-lookup"><span data-stu-id="baf15-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="baf15-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="baf15-113">Click New.</span></span>
    * <span data-ttu-id="baf15-114">Vytvořte nový dispoziční kód pro použití u vrácených položek odběratele.</span><span class="sxs-lookup"><span data-stu-id="baf15-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="baf15-115">Zadejte hodnotu do pole Dispoziční kód.</span><span class="sxs-lookup"><span data-stu-id="baf15-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="baf15-116">V poli Stav zásob vyberte stav zásob v případě, že existuje blokování zásob.</span><span class="sxs-lookup"><span data-stu-id="baf15-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="baf15-117">V případě, že používáte USMF, vyberte „Blokování“.</span><span class="sxs-lookup"><span data-stu-id="baf15-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="baf15-118">K dispozičnímu kódu můžete přidat stav zásob, a tak přepsat výchozí stav na řádcích objednávky.</span><span class="sxs-lookup"><span data-stu-id="baf15-118">You can add an inventory status to the disposition code to override the default status that’s on the order lines.</span></span>  
5. <span data-ttu-id="baf15-119">Zadejte hodnotu do pole Šablona práce.</span><span class="sxs-lookup"><span data-stu-id="baf15-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="baf15-120">Volitelné: Vyberte kód šablony práce přidružený k vratce.</span><span class="sxs-lookup"><span data-stu-id="baf15-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="baf15-121">Jestliže není zadána žádná hodnota, bude šablona práce přeložena pomocí standardních pravidel nastavených v systému.</span><span class="sxs-lookup"><span data-stu-id="baf15-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="baf15-122">Výběr šablony práce omezí procesy, se kterými lze tento dispoziční kód použít.</span><span class="sxs-lookup"><span data-stu-id="baf15-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="baf15-123">Například pokud má dispoziční kód šablonu práce s pracovním příkazem typu nákupní objednávky, nelze jej použít k registraci položek vrácených odběratelem.</span><span class="sxs-lookup"><span data-stu-id="baf15-123">For example, if a disposition code has a work template with a work order of type purchase order, it can’t be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="baf15-124">Zadejte hodnotu do pole Vrátit dispoziční kód.</span><span class="sxs-lookup"><span data-stu-id="baf15-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="baf15-125">Dispoziční kód vrácení určuje zbývající proces vratky pro registrované položky.</span><span class="sxs-lookup"><span data-stu-id="baf15-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="baf15-126">V tomto příkladu by měl odběratel obdržet dobropis.</span><span class="sxs-lookup"><span data-stu-id="baf15-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="baf15-127">Přidejte dispoziční kód vrácení obsahující akci Dal.</span><span class="sxs-lookup"><span data-stu-id="baf15-127">Add a returns disposition code that contains an action Credit.</span></span>  


---
title: Změna vlastnictví zásob dodávky na základě výrobní poptávky
description: Tato procedura ukazuje, jak změnit vlastníka zásob dodávky od dodavatele vaší právnické osobě, když existuje poptávka po zásobách ve výrobě.
author: perlynne
manager: AnnBe
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8200e0235fa78cbef4fdadd1d1c124446b89e72a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145865"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="04319-103">Změna vlastnictví zásob dodávky na základě výrobní poptávky</span><span class="sxs-lookup"><span data-stu-id="04319-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04319-104">Tato procedura ukazuje, jak změnit vlastníka zásob dodávky od dodavatele vaší právnické osobě, když existuje poptávka po zásobách ve výrobě.</span><span class="sxs-lookup"><span data-stu-id="04319-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="04319-105">Tato změna vlastnictví se provádí vytvořením a zaúčtováním deníků změn vlastnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="04319-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="04319-106">Řádky deníku změny vlastnictví lze vytvořit ručně nebo, jak je znázorněno v tomto záznamu, na základě existující výrobní poptávky.</span><span class="sxs-lookup"><span data-stu-id="04319-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="04319-107">Tento úkol obvykle provádí vedoucí dílny.</span><span class="sxs-lookup"><span data-stu-id="04319-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="04319-108">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="04319-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="04319-109">Používáte-li vlastní data, musí být splněny následující předpoklady: název skladového deníku, který byl nastaven pro změnu vlastnictví zásob, fyzicky zaznamenané zboží na skladě vlastněné dodavatelem a jeden nebo více řádků výrobních zakázek pro materiál.</span><span class="sxs-lookup"><span data-stu-id="04319-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="04319-110">Tento postup je určen pro funkci, která byla přidána do Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="04319-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="04319-111">Procesy odchozích zásilek nejsou podporovány ve výchozím nastavení a automatické zpracování deníku vlastnictví není podporováno.</span><span class="sxs-lookup"><span data-stu-id="04319-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="04319-112">Vytvoření deníku vlastnictví zásob</span><span class="sxs-lookup"><span data-stu-id="04319-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="04319-113">Přejděte do nabídky Řízení zásob > Položky deníku > Položky > Změna vlastnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="04319-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="04319-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="04319-114">Click New.</span></span>
    * <span data-ttu-id="04319-115">Deník změn vlastnictví zásob se používá ke změně vlastníka zásob od dodavatele na stávající právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="04319-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="04319-116">Tato změna vlastnictví se provádí uvolněním zásob na skladě, které jsou ve vlastnictví dodavatele, a následným přijetím těchto zásob v aktuální právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="04319-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="04319-117">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04319-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="04319-118">Můžete vybrat pouze názvy skladového deníku, které mají typ deníku Změna vlastnictví.</span><span class="sxs-lookup"><span data-stu-id="04319-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="04319-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="04319-119">Click OK.</span></span>
5. <span data-ttu-id="04319-120">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="04319-120">Click Functions.</span></span>
6. <span data-ttu-id="04319-121">Klikněte na Vytvořit řádky deníku z výrobních zakázek.</span><span class="sxs-lookup"><span data-stu-id="04319-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="04319-122">Proces změny vlastnictví proces lze spustit pomocí dotazu na všechny výrobní linky, které mají požadavek na spotřebu surovin.</span><span class="sxs-lookup"><span data-stu-id="04319-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="04319-123">V poli Stavy skladového výdeje k zahrnutí vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="04319-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="04319-124">Tato možnost umožňuje filtrovat podle stavu problému skladových transakcí.</span><span class="sxs-lookup"><span data-stu-id="04319-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="04319-125">Můžete například vytvořit řádky deníku pro zásoby, které mají fyzické stavy Vydané a Rezervované.</span><span class="sxs-lookup"><span data-stu-id="04319-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="04319-126">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="04319-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="04319-127">Tato část umožňuje aplikovat další filtrování.</span><span class="sxs-lookup"><span data-stu-id="04319-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="04319-128">Můžete například vybrat konkrétní datum surovin.</span><span class="sxs-lookup"><span data-stu-id="04319-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="04319-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="04319-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="04319-130">Zaúčtování deníku změn vlastnictví zásob</span><span class="sxs-lookup"><span data-stu-id="04319-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="04319-131">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="04319-131">Click Post.</span></span>
    * <span data-ttu-id="04319-132">Při zaúčtování deníku jsou vydány zásoby vlastněné dodavatelem pomocí reference Změna vlastnictví.</span><span class="sxs-lookup"><span data-stu-id="04319-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="04319-133">Zásoby jsou pak přijaty jako zásoby na skladě pomocí skladové transakce, která je aktualizována příjemkou produktu na nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="04319-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="04319-134">Všimněte si, že jsou vytvořeny pouze transakce, které se vztahují k zaúčtovanému deníku.</span><span class="sxs-lookup"><span data-stu-id="04319-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="04319-135">Nejsou vytvořeny žádné očekávané skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="04319-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="04319-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="04319-136">Click OK.</span></span>
3. <span data-ttu-id="04319-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="04319-137">Close the page.</span></span>


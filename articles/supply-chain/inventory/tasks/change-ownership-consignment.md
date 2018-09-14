--- 
title: "Změna vlastnictví zásob dodávky na základě výrobní poptávky"
description: "Tato procedura ukazuje, jak změnit vlastníka zásob dodávky od dodavatele vaší právnické osobě, když existuje poptávka po zásobách ve výrobě."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d1324da6996230eb383e2f37d3a133ec35cb0f41
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="b303c-103">Změna vlastnictví zásob dodávky na základě výrobní poptávky</span><span class="sxs-lookup"><span data-stu-id="b303c-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b303c-104">Tato procedura ukazuje, jak změnit vlastníka zásob dodávky od dodavatele vaší právnické osobě, když existuje poptávka po zásobách ve výrobě.</span><span class="sxs-lookup"><span data-stu-id="b303c-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="b303c-105">Tato změna vlastnictví se provádí vytvořením a zaúčtováním deníků změn vlastnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="b303c-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="b303c-106">Řádky deníku změny vlastnictví lze vytvořit ručně nebo, jak je znázorněno v tomto záznamu, na základě existující výrobní poptávky.</span><span class="sxs-lookup"><span data-stu-id="b303c-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="b303c-107">Tento úkol obvykle provádí vedoucí dílny.</span><span class="sxs-lookup"><span data-stu-id="b303c-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="b303c-108">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="b303c-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="b303c-109">Používáte-li vlastní data, musí být splněny následující předpoklady: název skladového deníku, který byl nastaven pro změnu vlastnictví zásob, fyzicky zaznamenané zboží na skladě vlastněné dodavatelem a jeden nebo více řádků výrobních zakázek pro materiál.</span><span class="sxs-lookup"><span data-stu-id="b303c-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="b303c-110">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations, verze 1611.</span><span class="sxs-lookup"><span data-stu-id="b303c-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="b303c-111">Vytvoření deníku vlastnictví zásob</span><span class="sxs-lookup"><span data-stu-id="b303c-111">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="b303c-112">Přejděte do nabídky Řízení zásob > Položky deníku > Položky > Změna vlastnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="b303c-112">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="b303c-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b303c-113">Click New.</span></span>
    * <span data-ttu-id="b303c-114">Deník změn vlastnictví zásob se používá ke změně vlastníka zásob od dodavatele na stávající právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="b303c-114">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="b303c-115">Tato změna vlastnictví se provádí uvolněním zásob na skladě, které jsou ve vlastnictví dodavatele, a následným přijetím těchto zásob v aktuální právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="b303c-115">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="b303c-116">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b303c-116">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="b303c-117">Můžete vybrat pouze názvy skladového deníku, které mají typ deníku Změna vlastnictví.</span><span class="sxs-lookup"><span data-stu-id="b303c-117">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="b303c-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b303c-118">Click OK.</span></span>
5. <span data-ttu-id="b303c-119">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="b303c-119">Click Functions.</span></span>
6. <span data-ttu-id="b303c-120">Klikněte na Vytvořit řádky deníku z výrobních zakázek.</span><span class="sxs-lookup"><span data-stu-id="b303c-120">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="b303c-121">Proces změny vlastnictví proces lze spustit pomocí dotazu na všechny výrobní linky, které mají požadavek na spotřebu surovin.</span><span class="sxs-lookup"><span data-stu-id="b303c-121">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="b303c-122">V poli Stavy skladového výdeje k zahrnutí vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="b303c-122">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="b303c-123">Tato možnost umožňuje filtrovat podle stavu problému skladových transakcí.</span><span class="sxs-lookup"><span data-stu-id="b303c-123">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="b303c-124">Můžete například vytvořit řádky deníku pro zásoby, které mají fyzické stavy Vydané a Rezervované.</span><span class="sxs-lookup"><span data-stu-id="b303c-124">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="b303c-125">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="b303c-125">Expand the Records to include section.</span></span>
    * <span data-ttu-id="b303c-126">Tato část umožňuje aplikovat další filtrování.</span><span class="sxs-lookup"><span data-stu-id="b303c-126">This section lets you apply additional filtering.</span></span> <span data-ttu-id="b303c-127">Můžete například vybrat konkrétní datum surovin.</span><span class="sxs-lookup"><span data-stu-id="b303c-127">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="b303c-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b303c-128">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="b303c-129">Zaúčtování deníku změn vlastnictví zásob</span><span class="sxs-lookup"><span data-stu-id="b303c-129">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="b303c-130">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="b303c-130">Click Post.</span></span>
    * <span data-ttu-id="b303c-131">Při zaúčtování deníku jsou vydány zásoby vlastněné dodavatelem pomocí reference Změna vlastnictví.</span><span class="sxs-lookup"><span data-stu-id="b303c-131">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="b303c-132">Zásoby jsou pak přijaty jako zásoby na skladě pomocí skladové transakce, která je aktualizována příjemkou produktu na nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="b303c-132">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="b303c-133">Všimněte si, že jsou vytvořeny pouze transakce, které se vztahují k zaúčtovanému deníku.</span><span class="sxs-lookup"><span data-stu-id="b303c-133">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="b303c-134">Nejsou vytvořeny žádné očekávané skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="b303c-134">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="b303c-135">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b303c-135">Click OK.</span></span>
3. <span data-ttu-id="b303c-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b303c-136">Close the page.</span></span>



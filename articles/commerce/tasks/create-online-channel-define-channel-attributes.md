---
title: Vytvoření online sítě a definování atributů kanálu
description: Tato procedura vás provede vytvářením nového online kanálu a jeho přidáním do organizační hierarchie.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f15b035c01801041d637a2d315d8a3ddcc9d6540
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410836"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="9f4ae-103">Vytvoření online sítě a definování atributů kanálu</span><span class="sxs-lookup"><span data-stu-id="9f4ae-103">Create online channel and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f4ae-104">Tato procedura vás provede vytvářením nového online kanálu a jeho přidáním do organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="9f4ae-105">Než budete moci vytvořit nový online kanál, je nutné vytvořit organizační hierarchii.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="9f4ae-106">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="9f4ae-107">Vytvoření nového online kanálu</span><span class="sxs-lookup"><span data-stu-id="9f4ae-107">Create a new online channel</span></span>
1. <span data-ttu-id="9f4ae-108">Přejděte na Retail and Commerce > Kanály > Online obchody.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="9f4ae-109">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-109">Click New.</span></span>
3. <span data-ttu-id="9f4ae-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9f4ae-111">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="9f4ae-112">V poli Časové pásmo obchodu vyberte požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="9f4ae-113">V poli Výchozí odběratel zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="9f4ae-114">V poli Adresář odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="9f4ae-115">V poli Platební podmínky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="9f4ae-116">V poli Metody platby zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="9f4ae-117">V poli Profil oznámení e-mailem zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="9f4ae-118">Rozbalte část Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="9f4ae-119">V poli BusinessUnit zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="9f4ae-120">Podobně nastavte hodnotu pro všechny ostatní výchozí dimenze.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="9f4ae-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="9f4ae-122">Přidat online kanál do organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="9f4ae-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="9f4ae-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-123">Close the page.</span></span>
2. <span data-ttu-id="9f4ae-124">Přejděte do nabídky Správa organizace > Organizace > Organization hierarchies.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="9f4ae-125">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="9f4ae-126">Klikněte na možnost Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-126">Click View.</span></span>
5. <span data-ttu-id="9f4ae-127">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-127">Click Edit.</span></span>
    * <span data-ttu-id="9f4ae-128">Můžete vybrat libovolný uzel hierarchie, pod který chcete vložit nový kanál.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="9f4ae-129">Klepněte na tlačítko Vložit.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-129">Click Insert.</span></span>
7. <span data-ttu-id="9f4ae-130">Klikněte na Kanál Commerce.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="9f4ae-131">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-131">Click OK.</span></span>
9. <span data-ttu-id="9f4ae-132">Kliknutím na možnost Publikovat otevřete dialog Zanechat.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="9f4ae-133">Do pole Datum platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="9f4ae-134">Klikněte na tlačítko Publikovat.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="9f4ae-135">Konfigurace objednávek pro blízké oznámení v reálném čase</span><span class="sxs-lookup"><span data-stu-id="9f4ae-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="9f4ae-136">Přejděte na možnost Retail a Commerce > Nastavení centrály > Parametry > Parametry Commerce.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="9f4ae-137">Nastavte možnost Použít službu Realtime Service pro vytvoření obejdnávky eCommerce na Ano.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="9f4ae-138">Spusťte plán distribuce 1070 k synchronizování změn do databáze kanálů.</span><span class="sxs-lookup"><span data-stu-id="9f4ae-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 



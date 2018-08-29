--- 
title: "Zadání produktů z distribučních center do obchodů pomocí metody buyer's push"
description: "Tato procedura vás provede postupem, jak vytvořit a zpracovat buyer's push k distribuci produktů z jednoho skladové místa do jednoho nebo více obchodů."
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ed47b4f052dab99dec058910e4b8558481b34e59
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="push-products-from-distribution-centers-to-stores-via-buyers-push"></a><span data-ttu-id="aeda0-103">Zadání produktů z distribučních center do obchodů pomocí metody buyer's push</span><span class="sxs-lookup"><span data-stu-id="aeda0-103">Push products from distribution centers to stores via buyer's push</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="aeda0-104">Tato procedura vás provede postupem, jak vytvořit a zpracovat buyer's push k distribuci produktů z jednoho skladové místa do jednoho nebo více obchodů.</span><span class="sxs-lookup"><span data-stu-id="aeda0-104">This procedure walks through the steps to create and process a Buyer's push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="aeda0-105">Můžete definovat více konfigurací a nechat systém navrhovat, jak budou produkty distribuovány, nebo ručně zadat, kam budou produkty distribuovány a kolik jich bude distribuováno do jednotlivých obchodů.</span><span class="sxs-lookup"><span data-stu-id="aeda0-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="aeda0-106">Tato procedura neobsahuje nastavení dat, která lze použít pro buyer's push, jako jsou například pravidla doplnění, organizační hierarchie a skladovací hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="aeda0-106">This procedure doesn't include setup of data that can be used in the Buyer's push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="aeda0-107">Tato procedura používá ukázkovou společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="aeda0-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="aeda0-108">Přejděte na možnost Buyer's push.</span><span class="sxs-lookup"><span data-stu-id="aeda0-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="aeda0-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="aeda0-109">Click New.</span></span>
3. <span data-ttu-id="aeda0-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="aeda0-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="aeda0-111">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="aeda0-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="aeda0-112">V poli Sklad zadejte nebo vyberte sklad, který obsahuje produkty s hodnotami množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="aeda0-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="aeda0-113">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="aeda0-113">Click Add.</span></span>
7. <span data-ttu-id="aeda0-114">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="aeda0-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="aeda0-115">V poli Číslo zboží zadejte nebo vyberte produkt.</span><span class="sxs-lookup"><span data-stu-id="aeda0-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="aeda0-116">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="aeda0-116">Click Add.</span></span>
10. <span data-ttu-id="aeda0-117">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="aeda0-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="aeda0-118">V poli Číslo zboží zadejte nebo vyberte variantu produktu.</span><span class="sxs-lookup"><span data-stu-id="aeda0-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="aeda0-119">Při zadávání varianty produktu budou vytvořeny řádky pro každou variantu.</span><span class="sxs-lookup"><span data-stu-id="aeda0-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="aeda0-120">Označte řádek na seznamu.</span><span class="sxs-lookup"><span data-stu-id="aeda0-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="aeda0-121">V poli Zadané množství zadejte počet vybraných produktů, které chcete distribuovat.</span><span class="sxs-lookup"><span data-stu-id="aeda0-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="aeda0-122">Do pole Další množství k zadání zadejte množství produktů, které mají dostupné množství pro distribuci.</span><span class="sxs-lookup"><span data-stu-id="aeda0-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="aeda0-123">V poli Distribuce zadejte „Váha místa“.</span><span class="sxs-lookup"><span data-stu-id="aeda0-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="aeda0-124">Můžete vybrat ostatní typy pro používání jiných pravidel pro distribuci.</span><span class="sxs-lookup"><span data-stu-id="aeda0-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="aeda0-125">V poli Hierarchie doplnění zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="aeda0-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="aeda0-126">Vyberte možnost Ano v poli Uznat sortimenty.</span><span class="sxs-lookup"><span data-stu-id="aeda0-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="aeda0-127">Klikněte na Vypočítat množství a zkontrolujte množství, která jsou přidána k řádkům v oddílu Sklad.</span><span class="sxs-lookup"><span data-stu-id="aeda0-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="aeda0-128">Klepněte na Vytvořit objednávku.</span><span class="sxs-lookup"><span data-stu-id="aeda0-128">Click Create order.</span></span>
20. <span data-ttu-id="aeda0-129">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="aeda0-129">Click Yes.</span></span>



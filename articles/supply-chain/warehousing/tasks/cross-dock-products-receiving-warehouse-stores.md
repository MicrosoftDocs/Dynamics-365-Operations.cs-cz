---
title: Používání cross dockingu pro distribuci produktů z přijímacího skladu do obchodů
description: Tato procedura vás provede postupem, jak vytvořit a zpracovat cross docking k distribuci produktů ze skladové místa příjmů nákupní objednávky do jednoho nebo více obchodů.
author: ShylaThompson
manager: tfehr
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bf53ba136c446df61893f4703e5951e42ae605d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217073"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="85e8b-103">Používání cross dockingu pro distribuci produktů z přijímacího skladu do obchodů</span><span class="sxs-lookup"><span data-stu-id="85e8b-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85e8b-104">Tato procedura vás provede postupem, jak vytvořit a zpracovat cross docking k distribuci produktů ze skladové místa příjmů nákupní objednávky do jednoho nebo více obchodů.</span><span class="sxs-lookup"><span data-stu-id="85e8b-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="85e8b-105">Můžete definovat více konfigurací a nechat systém navrhovat, jak budou produkty distribuovány, nebo ručně zadat, kam budou produkty distribuovány a kolik jich bude distribuováno do jednotlivých obchodů.</span><span class="sxs-lookup"><span data-stu-id="85e8b-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="85e8b-106">Procedura neobsahuje nastavení dat, která lze použít pro cross docking, jako jsou například pravidla doplnění, organizační hierarchie a skladovací hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="85e8b-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="85e8b-107">Procedura používá ukázkovou společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="85e8b-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="85e8b-108">Přejděte na Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="85e8b-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="85e8b-109">Vyberte nákupní objednávku ze seznamu a kliknutím na odkaz ji otevřete.</span><span class="sxs-lookup"><span data-stu-id="85e8b-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="85e8b-110">V podokně akcí klikněte na Retail and Commerce.</span><span class="sxs-lookup"><span data-stu-id="85e8b-110">On the Action Pane, click Retail and Commerce.</span></span>
4. <span data-ttu-id="85e8b-111">Klikněte na Cross docking.</span><span class="sxs-lookup"><span data-stu-id="85e8b-111">Click Cross docking.</span></span>
5. <span data-ttu-id="85e8b-112">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="85e8b-112">Click Edit.</span></span>
    * <span data-ttu-id="85e8b-113">Kategorie lze použít k filtrování položek v části Řádky.</span><span class="sxs-lookup"><span data-stu-id="85e8b-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="85e8b-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="85e8b-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="85e8b-115">V poli Množství pro cross docking zadejte hodnotu, která určuje, jaká část zakoupeného množství vybraného produktu by měla být distribuována.</span><span class="sxs-lookup"><span data-stu-id="85e8b-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="85e8b-116">Do pole Další množství pro cross docking zadejte hodnotu, která určuje množství pro distribuci dostupných produktů, které jsou kupovány.</span><span class="sxs-lookup"><span data-stu-id="85e8b-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="85e8b-117">V poli Distribuce zadejte „Váha místa“.</span><span class="sxs-lookup"><span data-stu-id="85e8b-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="85e8b-118">Můžete vybrat ostatní typy pro používání různých pravidel pro distribuci.</span><span class="sxs-lookup"><span data-stu-id="85e8b-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="85e8b-119">V poli Hierarchie doplnění zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="85e8b-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="85e8b-120">Vyberte možnost Ano v poli Uznat sortimenty.</span><span class="sxs-lookup"><span data-stu-id="85e8b-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="85e8b-121">Klikněte na Výpočet množství.</span><span class="sxs-lookup"><span data-stu-id="85e8b-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="85e8b-122">Klepněte na Vytvořit objednávku.</span><span class="sxs-lookup"><span data-stu-id="85e8b-122">Click Create order.</span></span>
14. <span data-ttu-id="85e8b-123">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="85e8b-123">Click Yes.</span></span>
15. <span data-ttu-id="85e8b-124">Vyhledejte a vyberte na seznamu sklad, který obdržel produkty.</span><span class="sxs-lookup"><span data-stu-id="85e8b-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="85e8b-125">Klikněte na objednávku, abyste zobrazili objednávky, které byly vytvořeny pro vybraný sklad.</span><span class="sxs-lookup"><span data-stu-id="85e8b-125">Click Order to view the orders that got created for the selected warehouse</span></span>


---
title: Přehled uznání výnosů
description: Toto téma obsahuje informace o funkci uznání výnosů. Tato funkce poskytuje flexibilní rámec, který vám umožňuje definovat pravidla specifická pro společnost pro uznání jak výnosové ceny, tak plán výnosů pro objednávky s více prvky.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 92af567499c1a8a23cd4d51e5bab48eaab2d8422
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2020
ms.locfileid: "4458641"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="d2205-104">Přehled uznání výnosů</span><span class="sxs-lookup"><span data-stu-id="d2205-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="d2205-105">Funkci uznání výnosů nelze zapnout pomocí správy funkcí.</span><span class="sxs-lookup"><span data-stu-id="d2205-105">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="d2205-106">Pro její zapnutí musíte momentálně použít konfigurační klíče.</span><span class="sxs-lookup"><span data-stu-id="d2205-106">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="d2205-107">Společnosti v průmyslových odvětvích, které prodávají více prvků, jako jsou produkty, služby, předplatné atd., musí být schopny rozdělit objednávky s více prvky, aby mohly být výnosy přiznány na základě souboru pokynů pro jednotlivé společnosti a pro jednotlivá odvětví.</span><span class="sxs-lookup"><span data-stu-id="d2205-107">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

<span data-ttu-id="d2205-108">Obecně lze proces přiznání výnosů použít k provedení těchto úloh:</span><span class="sxs-lookup"><span data-stu-id="d2205-108">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="d2205-109">Přiřazení výnosů, abyste mohli zaručit, že příslušná výnosová cena bude uznána na základě hodnoty komponent na objednávkách s více prvky.</span><span class="sxs-lookup"><span data-stu-id="d2205-109">Allocate revenue, to help guarantee that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="d2205-110">Odložení výnosů na základě plánu výnosů, který představuje smluvní časový rámec a procenta pro uznání výnosů v čase.</span><span class="sxs-lookup"><span data-stu-id="d2205-110">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="d2205-111">Video [Způsob použití uznání výnosů v Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (zobrazené výše) je zahrnuto do [playlistu Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) dostupného na YouTube.</span><span class="sxs-lookup"><span data-stu-id="d2205-111">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="d2205-112">Funkce uznání výnosů poskytuje flexibilní rámec, který vám umožňuje definovat pravidla specifická pro společnost pro uznání jak výnosové ceny, tak plán výnosů.</span><span class="sxs-lookup"><span data-stu-id="d2205-112">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="d2205-113">Uvolněné produkty se používají pro podporu uznání výnosů v dokumentech prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="d2205-113">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="d2205-114">Uvolněné produkty obsahují nastavení, které je vyžadováno pro určení výnosové ceny a plánu výnosů.</span><span class="sxs-lookup"><span data-stu-id="d2205-114">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="d2205-115">Prodejní objednávka může pocházet z projektu určeného časem a materiálem.</span><span class="sxs-lookup"><span data-stu-id="d2205-115">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="d2205-116">Společnosti mohou používat funkcionalitu plánu výnosů bez použití funkcionality výnosové ceny.</span><span class="sxs-lookup"><span data-stu-id="d2205-116">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="d2205-117">Proto se cena na řádcích prodejní objednávky použije buď jako výnos nebo jako odložený výnos.</span><span class="sxs-lookup"><span data-stu-id="d2205-117">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="d2205-118">Pokud na řádku prodejní objednávky existuje plán výnosů, cena na řádku prodejní objednávky se odloží.</span><span class="sxs-lookup"><span data-stu-id="d2205-118">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="d2205-119">Pokud na řádku prodejní objednávky neexistuje plán výnosů, cena na řádku prodejní objednávky bude zaúčtována na účet výnosů v okamžik, kdy je fakturována.</span><span class="sxs-lookup"><span data-stu-id="d2205-119">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="d2205-120">Výnosová cena se vypočítá buď při potvrzení prodejní objednávky nebo při zaúčtování faktury.</span><span class="sxs-lookup"><span data-stu-id="d2205-120">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="d2205-121">Chcete-li zobrazit náhled výnosové ceny před zaúčtováním faktury, musíte potvrdit prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="d2205-121">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="d2205-122">Když je prodejní objednávka potvrzena, vytvoří se též plán očekávaných výnosů, pokud některý z řádků prodejní objednávky má plán výnosů.</span><span class="sxs-lookup"><span data-stu-id="d2205-122">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="d2205-123">Když je prodejní objednávka vyfakturována, plán očekávaných výnosů je odstraněn a je nahrazen za plán uznání skutečných výnosů.</span><span class="sxs-lookup"><span data-stu-id="d2205-123">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="d2205-124">Podrobnosti plánu uznání výnosů se udržují pro každý řádek prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d2205-124">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="d2205-125">Proto může manažer uznání výnosů zobrazit podrobnosti a uvolnit řádky do výnosů, když byl dokončen smluvní závazek.</span><span class="sxs-lookup"><span data-stu-id="d2205-125">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="d2205-126">Na konci každého období může manažer uznání výnosů vytvořit deník výnosů, aby uvolnil všechny řádky plánu, které jsou splatné v den nebo před dnem, který určí.</span><span class="sxs-lookup"><span data-stu-id="d2205-126">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="d2205-127">Tento deník výnosů není zaúčtován okamžitě.</span><span class="sxs-lookup"><span data-stu-id="d2205-127">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="d2205-128">Proto může manažer uznání výnosů ověřit, že jsou z odložených výnosů do skutečných výnosů uvolňovány správné částky.</span><span class="sxs-lookup"><span data-stu-id="d2205-128">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="d2205-129">Pokud smluvní změna způsobí přidání nového řádku prodejní objednávky buď do existující prodejní objednávky nebo nové prodejní objednávky, lze spustit proces přidělení, aby se opravila výnosová cena napříč všemi řádky v prodejních objednávkách.</span><span class="sxs-lookup"><span data-stu-id="d2205-129">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>

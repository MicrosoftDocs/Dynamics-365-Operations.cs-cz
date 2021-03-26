---
title: Přehled uznání výnosů
description: Toto téma obsahuje informace o funkci uznání výnosů. Tato funkce poskytuje flexibilní rámec, který vaší společnosti umožňuje definovat vlastní pravidla uznání výnosové ceny a plánu výnosů pro objednávky s více složkami.
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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: b21cf04674d01df31dc3304886e7cda035bdcce2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238249"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="94cd4-104">Přehled uznání výnosů</span><span class="sxs-lookup"><span data-stu-id="94cd4-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94cd4-105">Společnosti podnikající v oborech, kde se obchoduje s více složkami, jako jsou produkty, služby nebo předplatná, musí umět rozlišovat jednotlivé složky na objednávkách, takže jejich výnosy mohou být uznány na základě souboru pokynů pro jednotlivé společnosti a odvětví.</span><span class="sxs-lookup"><span data-stu-id="94cd4-105">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

> [!NOTE]
> <span data-ttu-id="94cd4-106">Funkci uznání výnosů nelze zapnout prostřednictvím správy funkcí.</span><span class="sxs-lookup"><span data-stu-id="94cd4-106">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="94cd4-107">V současné době ji aktivujete pomocí konfiguračních klíčů.</span><span class="sxs-lookup"><span data-stu-id="94cd4-107">Currently, you must use configuration keys to turn it on.</span></span>

> <span data-ttu-id="94cd4-108">Uznání výnosů (včetně funkce sady) nelze použít v kanálech Commerce (elektronické obchodování, POS, kontaktní středisko).</span><span class="sxs-lookup"><span data-stu-id="94cd4-108">Revenue recognition, including bundle functionality, isn't supported for use in Commerce channels (e-commerce, POS, call center).</span></span> <span data-ttu-id="94cd4-109">Položky konfigurované s uznáním výnosů nesmí být přidány na objednávky nebo do transakcí vytvořených v kanálech Commerce.</span><span class="sxs-lookup"><span data-stu-id="94cd4-109">Items configured with revenue recognition should not be added to orders or transactions created in Commerce channels.</span></span>

<span data-ttu-id="94cd4-110">Obecně lze uznání výnosů použít k následujícím účelům:</span><span class="sxs-lookup"><span data-stu-id="94cd4-110">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="94cd4-111">Přidělení výnosů, které pomáhá zaručit, že příslušná výnosová cena bude uznána na základě hodnoty komponent na objednávkách s více složkami.</span><span class="sxs-lookup"><span data-stu-id="94cd4-111">Allocate revenue, to help ensure that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="94cd4-112">Odložení výnosů na základě plánu výnosů, který představuje smluvní časový rámec a procenta pro uznání výnosů v čase.</span><span class="sxs-lookup"><span data-stu-id="94cd4-112">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="94cd4-113">Video [Způsob použití uznání výnosů v Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (zobrazené výše) je zahrnuto do [playlistu Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) dostupného na YouTube.</span><span class="sxs-lookup"><span data-stu-id="94cd4-113">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="94cd4-114">Funkce uznání výnosů poskytuje flexibilní rámec, který vám umožňuje definovat pravidla specifická pro společnost pro uznání jak výnosové ceny, tak plán výnosů.</span><span class="sxs-lookup"><span data-stu-id="94cd4-114">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="94cd4-115">Uvolněné produkty se používají pro podporu uznání výnosů v dokumentech prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="94cd4-115">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="94cd4-116">Uvolněné produkty obsahují nastavení, které je vyžadováno pro určení výnosové ceny a plánu výnosů.</span><span class="sxs-lookup"><span data-stu-id="94cd4-116">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="94cd4-117">Prodejní objednávka může pocházet z projektu určeného časem a materiálem.</span><span class="sxs-lookup"><span data-stu-id="94cd4-117">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="94cd4-118">Společnosti mohou používat funkcionalitu plánu výnosů bez použití funkcionality výnosové ceny.</span><span class="sxs-lookup"><span data-stu-id="94cd4-118">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="94cd4-119">Proto se cena na řádcích prodejní objednávky použije buď jako výnos nebo jako odložený výnos.</span><span class="sxs-lookup"><span data-stu-id="94cd4-119">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="94cd4-120">Pokud na řádku prodejní objednávky existuje plán výnosů, cena na řádku prodejní objednávky se odloží.</span><span class="sxs-lookup"><span data-stu-id="94cd4-120">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="94cd4-121">Pokud na řádku prodejní objednávky neexistuje plán výnosů, cena na řádku prodejní objednávky bude zaúčtována na účet výnosů v okamžik, kdy je fakturována.</span><span class="sxs-lookup"><span data-stu-id="94cd4-121">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="94cd4-122">Výnosová cena se vypočítá buď při potvrzení prodejní objednávky nebo při zaúčtování faktury.</span><span class="sxs-lookup"><span data-stu-id="94cd4-122">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="94cd4-123">Chcete-li zobrazit náhled výnosové ceny před zaúčtováním faktury, musíte potvrdit prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="94cd4-123">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="94cd4-124">Když je prodejní objednávka potvrzena, vytvoří se též plán očekávaných výnosů, pokud některý z řádků prodejní objednávky má plán výnosů.</span><span class="sxs-lookup"><span data-stu-id="94cd4-124">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="94cd4-125">Když je prodejní objednávka vyfakturována, plán očekávaných výnosů je odstraněn a je nahrazen za plán uznání skutečných výnosů.</span><span class="sxs-lookup"><span data-stu-id="94cd4-125">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="94cd4-126">Podrobnosti plánu uznání výnosů se udržují pro každý řádek prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="94cd4-126">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="94cd4-127">Proto může manažer uznání výnosů zobrazit podrobnosti a uvolnit řádky do výnosů, když byl dokončen smluvní závazek.</span><span class="sxs-lookup"><span data-stu-id="94cd4-127">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="94cd4-128">Na konci každého období může manažer uznání výnosů vytvořit deník výnosů, aby uvolnil všechny řádky plánu, které jsou splatné v den nebo před dnem, který určí.</span><span class="sxs-lookup"><span data-stu-id="94cd4-128">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="94cd4-129">Tento deník výnosů není zaúčtován okamžitě.</span><span class="sxs-lookup"><span data-stu-id="94cd4-129">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="94cd4-130">Proto může manažer uznání výnosů ověřit, že jsou z odložených výnosů do skutečných výnosů uvolňovány správné částky.</span><span class="sxs-lookup"><span data-stu-id="94cd4-130">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="94cd4-131">Pokud smluvní změna způsobí přidání nového řádku prodejní objednávky buď do existující prodejní objednávky nebo nové prodejní objednávky, lze spustit proces přidělení, aby se opravila výnosová cena napříč všemi řádky v prodejních objednávkách.</span><span class="sxs-lookup"><span data-stu-id="94cd4-131">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Uvolnění výrobních zakázek
description: Uvolněná výrobní zakázka je objednávka, která byla schválena k výrobě. Výraz Uvolněná popisuje stav v životním cyklu výrobní zakázky, kde je výrobní zakázka k dispozici ke spuštění v rámci dílenské výroby a skladových procesů.
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 118b0d6300647135b22e42cc84a79f07e48d7ef4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811695"
---
# <a name="release-production-orders"></a><span data-ttu-id="9d020-104">Uvolnění výrobních zakázek</span><span class="sxs-lookup"><span data-stu-id="9d020-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d020-105">Uvolněná výrobní zakázka je objednávka, která byla schválena k výrobě.</span><span class="sxs-lookup"><span data-stu-id="9d020-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="9d020-106">Výraz Uvolněná popisuje stav v životním cyklu výrobní zakázky, kde je výrobní zakázka k dispozici ke spuštění v rámci dílenské výroby a skladových procesů.</span><span class="sxs-lookup"><span data-stu-id="9d020-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span>

## <a name="characteristics-of-the-released-state"></a><span data-ttu-id="9d020-107">Charakteristika stavu Uvolněno</span><span class="sxs-lookup"><span data-stu-id="9d020-107">Characteristics of the Released state</span></span>

<span data-ttu-id="9d020-108">Stav **Uvolněno** je jeden ze stavů životního cyklu výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="9d020-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="9d020-109">Výrobní zakázky, které jsou ve stavu **Uvolněno**, jsou k dispozici pro spuštění v dílenské výrobě a pro procesy skladu.</span><span class="sxs-lookup"><span data-stu-id="9d020-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="9d020-110">Stav **Uvolněno** má následující charakteristiky:</span><span class="sxs-lookup"><span data-stu-id="9d020-110">The **Released** state has the following characteristics:</span></span>

- <span data-ttu-id="9d020-111">Výrobní zakázku lze změnit na stav **Uvolněno** ve výrobní zakázce nebo pomocí dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="9d020-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="9d020-112">Výrobní zakázky lze rovněž automaticky aktualizovat s použitím potvrzení plánovaných výrobních zakázek pomocí pole **Ochranná doba potvrzení** na stránce **Hlavní plán**.</span><span class="sxs-lookup"><span data-stu-id="9d020-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
- <span data-ttu-id="9d020-113">Stav **Uvolněno** je signál pro dílenskou obsluhu (operátory) pro spouštění výrobních úloh v dílně.</span><span class="sxs-lookup"><span data-stu-id="9d020-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
- <span data-ttu-id="9d020-114">Výrobní doklady, jako například karty technického postupu, postupy úlohy a pracovní karty poskytují informace o výrobních úlohách, a lze je vydat.</span><span class="sxs-lookup"><span data-stu-id="9d020-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
- <span data-ttu-id="9d020-115">Pro materiály, které jsou fyzicky rezervovány, se vytvoří skladová práce pro výdej materiálu pro výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="9d020-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="9d020-116">Uvolnění úloh do výroby</span><span class="sxs-lookup"><span data-stu-id="9d020-116">Releasing jobs to the shop floor</span></span>

<span data-ttu-id="9d020-117">Po uvolnění výrobní zakázky jsou výrobní úlohy, které se vztahují k objednávce, viditelné a připravené pro registraci.</span><span class="sxs-lookup"><span data-stu-id="9d020-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="9d020-118">Operátoři mohou provádět registrace úloh, jako je začátek, konec a dokončení, na stránce **Terminál úkolových lístků** nebo **Zařízení úkolového lístku**.</span><span class="sxs-lookup"><span data-stu-id="9d020-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="9d020-119">Zaregistrovaná doba a množství jsou automaticky převedeny ze stránek registrace na výrobní deníky, aby byl sledován spotřebovaný čas a množství.</span><span class="sxs-lookup"><span data-stu-id="9d020-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="9d020-120">Karty technologického postupu</span><span class="sxs-lookup"><span data-stu-id="9d020-120">Route cards</span></span>

<span data-ttu-id="9d020-121">Karta technologického postupu poskytuje souhrn informací pocházejících z nastavení operací a technologických postupů a z metod plánování úloh.</span><span class="sxs-lookup"><span data-stu-id="9d020-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="9d020-122">Operace tech. postupu</span><span class="sxs-lookup"><span data-stu-id="9d020-122">Route jobs</span></span>

<span data-ttu-id="9d020-123">Operace technologického postupu obsahuje podrobný seznam všech úloh určité operace a zahrnuje časové údaje pro dobu nastavení, zpracování, čekání a přepravy.</span><span class="sxs-lookup"><span data-stu-id="9d020-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="9d020-124">Operace lakování bude například vyžadovat údaje pro jednotlivé úlohy, jako je doba nastavení, doba zpracování (pro proces lakování) a doba čekání (pro zasychání).</span><span class="sxs-lookup"><span data-stu-id="9d020-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="9d020-125">Úkolové lístky</span><span class="sxs-lookup"><span data-stu-id="9d020-125">Job cards</span></span>

<span data-ttu-id="9d020-126">Na úkolových lístcích jsou uvedena čísla jednotlivých úloh pro určitou operaci.</span><span class="sxs-lookup"><span data-stu-id="9d020-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="9d020-127">(Vždy jedna úloha na stránku.)</span><span class="sxs-lookup"><span data-stu-id="9d020-127">One job appears on each page.</span></span> <span data-ttu-id="9d020-128">Úlohy uvedené na úkolovém lístku a jejich odhadované doby pocházejí z konfiguračních údajů na kartách technologického postupu a z údajů pro operace technologického postupu.</span><span class="sxs-lookup"><span data-stu-id="9d020-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="9d020-129">Z úkolového lístku můžete otevřít stránku **Řádky výr. deníku**, **úkolový lístek**.</span><span class="sxs-lookup"><span data-stu-id="9d020-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="9d020-130">Zpětnou vazbu ohledně výrobního procesu mohou poskytnout osoby používající provozní prostředky.</span><span class="sxs-lookup"><span data-stu-id="9d020-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="9d020-131">K dispozici jsou pole, do nichž můžete zadat statistické údaje o spotřebě a informace, jako jsou například chyby v množství.</span><span class="sxs-lookup"><span data-stu-id="9d020-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="9d020-132">Skladová práce pro výdej surovin</span><span class="sxs-lookup"><span data-stu-id="9d020-132">Warehouse work for raw material picking</span></span>

<span data-ttu-id="9d020-133">Práce pro výdej surovin je vytvořena v průběhu uvolnění.</span><span class="sxs-lookup"><span data-stu-id="9d020-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="9d020-134">Práce je generována pouze pro množství materiálů, které byly fyzicky rezervovány pro výrobní zakázku před vydáním objednávky.</span><span class="sxs-lookup"><span data-stu-id="9d020-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="9d020-135">Následující nastavení je vyžadováno ke generování práce skladu pro výdej surovin:</span><span class="sxs-lookup"><span data-stu-id="9d020-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

- <span data-ttu-id="9d020-136">Směrnice skladového místa pro výdej surovin, které určují, ve kterém umístění skladu chcete vydat materiál</span><span class="sxs-lookup"><span data-stu-id="9d020-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
- <span data-ttu-id="9d020-137">Šablona vlny pro suroviny, kde jsou konfigurovány zásady provedení skladové práce</span><span class="sxs-lookup"><span data-stu-id="9d020-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
- <span data-ttu-id="9d020-138">Vstupní místo výroby, která určuje, kam jsou materiály umístěny</span><span class="sxs-lookup"><span data-stu-id="9d020-138">A production input location that determines where materials are put</span></span>

<span data-ttu-id="9d020-139">Pokud používáte umístění řízená registrační značkou, můžete si vybrat, zda má být během zpracování vychystávání surovin vybráno objednané množství nebo celkové množství dostupné pro položku.</span><span class="sxs-lookup"><span data-stu-id="9d020-139">When using license plate controlled locations, you can choose whether the ordered quantity or the full quantity available for the item should be picked while processing the raw material picking work.</span></span> <span data-ttu-id="9d020-140">Nastavení této možnosti:</span><span class="sxs-lookup"><span data-stu-id="9d020-140">To set this option:</span></span>

1. <span data-ttu-id="9d020-141">přejděte na **Správa informací o produktu \> Produkty \> Vydané produkty** a otevřete příslušnou položku.</span><span class="sxs-lookup"><span data-stu-id="9d020-141">Go to **Product information management \> Products \> Released products** and open the relevant item.</span></span>
1. <span data-ttu-id="9d020-142">Rozbalte záložku s náhledem **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="9d020-142">Expand the **Warehouse** FastTab.</span></span>
1. <span data-ttu-id="9d020-143">Vyberte jednu z následujících možností pro pole **Vychystávání materiálu na pozicích SPZ**:</span><span class="sxs-lookup"><span data-stu-id="9d020-143">Select one of the following options for the  **Material picking in license plate locations** field:</span></span>
    - <span data-ttu-id="9d020-144">*Výdej objednávky*: Pouze pokud chcete určit, že vydávat se budou pouze objednaná množství.</span><span class="sxs-lookup"><span data-stu-id="9d020-144">*Order picking*: Only the ordered quantity should be picked.</span></span>
    - <span data-ttu-id="9d020-145">*Fázování*: Kdykoli je to možné, měla by být vydána pouze celá množství z registrační značky.</span><span class="sxs-lookup"><span data-stu-id="9d020-145">*Staging*: Whenever possible, the full quantity available at the license plate should be picked.</span></span> <span data-ttu-id="9d020-146">Aby pracovník mohl vybrat celé množství registrační značky, nesmí značka obsahovat smíšené položky a nesmí mít smíšené rozměry.</span><span class="sxs-lookup"><span data-stu-id="9d020-146">For a worker to be able to pick the full license plate quantity, the license plate must not contain mixed items and must not have mixed dimensions.</span></span> <span data-ttu-id="9d020-147">Pokud registrační značka obsahuje smíšené rozměry nebo položky, bude výběr probíhat, jako by byl nastaven na *Vyzvednutí objednávky*.</span><span class="sxs-lookup"><span data-stu-id="9d020-147">If the license plate contains mixed dimensions or items, the pick will proceed as if it were set to *Order picking*.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
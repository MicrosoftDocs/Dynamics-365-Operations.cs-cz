---
title: Sledování příchozích cest a cest přepravních kontejnerů
description: Toto téma vysvětluje, jak můžete pomocí stránky Sledování vstupu monitorovat průběh cest a cest přepravních kontejnerů.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 678f2b6cda0592e0393bb15f372cb4be84778932
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501239"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a><span data-ttu-id="2e8ea-103">Sledování příchozích cest a cest přepravních kontejnerů</span><span class="sxs-lookup"><span data-stu-id="2e8ea-103">Track inbound voyages and shipping container journeys</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2e8ea-104">Stránka **Sledování vstupu** umožňuje monitorovat průběh cest a cest přepravních kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-104">The **Inbound tracking** page lets you track the progress of your voyages and shipping container journeys.</span></span> <span data-ttu-id="2e8ea-105">Každá cesta a cesta kontejneru je rozdělena na části podle *aktivit*, z nichž každá má na stránce svůj vlastní řádek.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-105">Each voyage and journey is broken down by *activities*, each of which has its own row on the page.</span></span> <span data-ttu-id="2e8ea-106">Na této stránce můžete zobrazit a zadat odhadovaná a skutečná kalendářní data podle aktivity.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-106">You can use the page to view and enter estimated dates and actual dates by activity.</span></span>

<span data-ttu-id="2e8ea-107">Obvykle, v závislosti na nastavení zadaném v [řídicím centru sledování](delivery-information-setup.md#tracking-control-center), tyto aktivity automaticky zobrazují odhadované datum dojetí do konečného cíle.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-107">Typically, depending on the setup in the [Tracking control center](delivery-information-setup.md#tracking-control-center), these activities automatically show the estimated landing date at the final destination.</span></span> <span data-ttu-id="2e8ea-108">V závislosti na nastavení také konečné datum obvykle aktualizuje datum dodání nebo potvrzené datum na řádcích nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-108">Also depending on the setup, the final date usually updates the delivery date or confirmed date on purchase order lines.</span></span> <span data-ttu-id="2e8ea-109">U řádků převodního příkazu můžete nastavit systém tak, aby aktualizoval datum přijetí.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-109">For transfer order lines, you can set up the system to update the receipt date.</span></span>

<span data-ttu-id="2e8ea-110">Chcete-li otevřít stránku **Sledování vstupu** přejděte na uzel **Náklady za doručení \> Sledování \> Sledování vstupu**.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-110">To open the **Inbound tracking** page, go to **Landed cost \> Tracking \> Inbound tracking**.</span></span>

## <a name="filter-the-activities-list"></a><span data-ttu-id="2e8ea-111">Filtrování seznamu aktivit</span><span class="sxs-lookup"><span data-stu-id="2e8ea-111">Filter the activities list</span></span>

<span data-ttu-id="2e8ea-112">Pole **Cesta** a **Přepravní kontejner** v horní části stránky **Sledování vstupu** můžete použít k filtrování stránky tak, aby zobrazovala pouze aktivity, které jsou přidruženy k vybrané cestě anebo přepravnímu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-112">You can use the **Voyage** and **Shipping container** fields at the top of the **Inbound tracking** page to filter the page so that it shows only activities that are associated with the selected voyage and/or shipping container.</span></span>

## <a name="update-tracking-information"></a><span data-ttu-id="2e8ea-113">Aktualizace informace o sledování</span><span class="sxs-lookup"><span data-stu-id="2e8ea-113">Update tracking information</span></span>

<span data-ttu-id="2e8ea-114">Chcete-li aktualizovat plán cesty nebo cesty kontejneru, zadejte datum zahájení první aktivity.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-114">To update the schedule for a voyage or journey, enter the start date for the first activity.</span></span> <span data-ttu-id="2e8ea-115">Odhadované datum ukončení poslední aktivity se poté aktualizuje.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-115">The estimated end date of the last activity is then updated.</span></span> <span data-ttu-id="2e8ea-116">Nastavení pro každý úsek a šablonu cesty v [řídicím centru sledování](delivery-information-setup.md#tracking-control-center) určuje odhadované doby realizace.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-116">The setup for each leg and journey template in the [Tracking control center](delivery-information-setup.md#tracking-control-center) determines the estimated lead times.</span></span> <span data-ttu-id="2e8ea-117">Odhadovaná data ukončení využívají dobu realizace od data zahájení aktivity.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-117">The estimated end dates use the lead time from the start date of the activity.</span></span> <span data-ttu-id="2e8ea-118">Poté, když je zaznamenáno skutečné datum ukončení, je datum zahájení další aktivity aktualizováno na stejné datum jako skutečné datum ukončení předchozí aktivity.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-118">Then, when the actual end date is recorded, the start date of the next activity is updated to the same date as the previous activity's actual end date.</span></span> <span data-ttu-id="2e8ea-119">Skutečná doba realizace se aktualizuje, aby bylo možné provést srovnání a analýzu.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-119">The actual lead time is updated so that comparison and analysis can be done.</span></span> <span data-ttu-id="2e8ea-120">Další poznámky lze zadat do pole **Poznámka**.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-120">Additional notes can be entered in the **Note** field.</span></span>

<span data-ttu-id="2e8ea-121">Pořadí aktivit v mřížce je určeno pořadím úseků v příslušné šabloně cesty.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-121">The order of the activities in the grid is determined by the order of the legs in the relevant journey template.</span></span> <span data-ttu-id="2e8ea-122">Pokud se změní pořadí úseků v připojené cestě, změní se také řízení sledování.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-122">If order of the legs in the attached journey changes, the tracking control also changes.</span></span>

<span data-ttu-id="2e8ea-123">Data všech kontejnerů můžete aktualizovat výběrem příkazu **Aktualizovat datum zahájení** nebo **Aktualizovat skutečné datum ukončení** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-123">You can update the dates for all containers by selecting **Update start date** or **Update actual end date** on the Action Pane.</span></span> <span data-ttu-id="2e8ea-124">Alternativně můžete zadat kalendářní data pro každý kontejner v zásilce.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-124">Alternatively, you can enter the dates per container on the shipment.</span></span> <span data-ttu-id="2e8ea-125">Tento přístup umožňuje větší flexibilitu, protože kontejnery lze v prostředí s více cestami rozdělit.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-125">This approach allows for greater flexibility, because containers can be split in a multi-journey environment.</span></span>

## <a name="buttons-on-the-action-pane"></a><span data-ttu-id="2e8ea-126">Tlačítka v podokně akcí</span><span class="sxs-lookup"><span data-stu-id="2e8ea-126">Buttons on the Action Pane</span></span>

<span data-ttu-id="2e8ea-127">Tlačítka v podokně akcí na stránce **Sledování vstupu** můžete použít pro práci s příchozími cestami.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-127">You can use the buttons on the Action Pane of the **Inbound tracking** page to work with inbound voyages and journeys.</span></span> <span data-ttu-id="2e8ea-128">V následující tabulce jsou popsána dostupná tlačítka.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-128">The following table describes the buttons that are available.</span></span>

| <span data-ttu-id="2e8ea-129">Tlačítko</span><span class="sxs-lookup"><span data-stu-id="2e8ea-129">Button</span></span> | <span data-ttu-id="2e8ea-130">popis</span><span class="sxs-lookup"><span data-stu-id="2e8ea-130">Description</span></span> |
|---|---|
| <span data-ttu-id="2e8ea-131">Úpravy</span><span class="sxs-lookup"><span data-stu-id="2e8ea-131">Edit</span></span> | <span data-ttu-id="2e8ea-132">Upravte cestu nebo cestu přepravního kontejneru.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-132">Edit a voyage or shipping container journey.</span></span> |
| <span data-ttu-id="2e8ea-133">Nová</span><span class="sxs-lookup"><span data-stu-id="2e8ea-133">New</span></span> | <span data-ttu-id="2e8ea-134">Vytvořte novou cestu nebo cestu přepravního kontejneru.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-134">Create a new voyage or shipping container journey.</span></span> |
| <span data-ttu-id="2e8ea-135">Odstranit</span><span class="sxs-lookup"><span data-stu-id="2e8ea-135">Delete</span></span> | <span data-ttu-id="2e8ea-136">Odstraňte vybranou cestu nebo cestu přepravního kontejneru.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-136">Delete a selected voyage or shipping container journey.</span></span> |
| <span data-ttu-id="2e8ea-137">Počáteční datum aktualizace</span><span class="sxs-lookup"><span data-stu-id="2e8ea-137">Update start date</span></span> | <span data-ttu-id="2e8ea-138">Aktualizujte datum zahájení aktivity pro všechny kontejnery v cestě.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-138">Update the start date of an activity for all containers in a voyage.</span></span> <span data-ttu-id="2e8ea-139">Když se aktualizuje datum zahájení konkrétní aktivity nebo úsek cesty, aktualizují se následující odhadovaná data zahájení na základě zadané doby realizace.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-139">When the start date of a specific activity or leg of a journey is updated, the subsequent estimated start dates are updated based on the specified lead time.</span></span> |
| <span data-ttu-id="2e8ea-140">Aktualizovat skutečné koncové datum</span><span class="sxs-lookup"><span data-stu-id="2e8ea-140">Update actual end date</span></span> | <span data-ttu-id="2e8ea-141">Aktualizujte datum ukončení aktivity pro všechny kontejnery v cestě.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-141">Update the end date of an activity for all containers in a voyage.</span></span> <span data-ttu-id="2e8ea-142">Když se aktualizuje datum ukončení konkrétní aktivity nebo úsek cesty, aktualizují se následující aktivity na základě zadané doby realizace.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-142">When the end date of a specific activity is updated, the subsequent activities are updated based on the specified lead time.</span></span> |
| <span data-ttu-id="2e8ea-143">Přidat aktivity</span><span class="sxs-lookup"><span data-stu-id="2e8ea-143">Add activities</span></span> | <span data-ttu-id="2e8ea-144">Přidejte aktivitu do cesty ručně.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-144">Manually add an activity to a voyage.</span></span> <span data-ttu-id="2e8ea-145">Můžete například přidat aktivitu dezinfekce.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-145">For example, you might add a fumigation activity.</span></span> <span data-ttu-id="2e8ea-146">Přidání může způsobit změnu potvrzeného data dodání zboží na lodi nebo cestě.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-146">The addition might cause the confirmed delivery date of the goods in the vessel or voyage to change.</span></span> <span data-ttu-id="2e8ea-147">Když je do cesty přidána aktivita, odhadované dny se nezadají, dokud se neaktualizuje datum zahájení úseku cesty.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-147">When an activity is added to the journey, the estimated days aren't entered until the start date of a journey leg is updated.</span></span> |

## <a name="information-and-settings-on-the-overview-tab"></a><span data-ttu-id="2e8ea-148">Informace a nastavení na kartě Přehled</span><span class="sxs-lookup"><span data-stu-id="2e8ea-148">Information and settings on the Overview tab</span></span>

<span data-ttu-id="2e8ea-149">Karta **Přehled** zobrazuje seznam všech aktivit, které patří do cesty anebo přepravního kontejneru, který je vybrán v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-149">The **Overview** tab shows a list of all the activities that belong to the voyage and/or shipping container that is selected at the top of the page.</span></span> <span data-ttu-id="2e8ea-150">V následující tabulce jsou popsána pole, která jsou k dispozici pro každou aktivitu.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-150">The following table describes the fields that are available for each activity.</span></span>

| <span data-ttu-id="2e8ea-151">Pole</span><span class="sxs-lookup"><span data-stu-id="2e8ea-151">Field</span></span> | <span data-ttu-id="2e8ea-152">popis</span><span class="sxs-lookup"><span data-stu-id="2e8ea-152">Description</span></span> |
|---|---|
| <span data-ttu-id="2e8ea-153">Úsek</span><span class="sxs-lookup"><span data-stu-id="2e8ea-153">Leg</span></span> | <span data-ttu-id="2e8ea-154">ID úseku pro aktivitu, jak je definován v šabloně cesty.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-154">The leg ID for the activity, as defined by the journey template.</span></span> |
| <span data-ttu-id="2e8ea-155">Způsob dodání</span><span class="sxs-lookup"><span data-stu-id="2e8ea-155">Mode of delivery</span></span> | <span data-ttu-id="2e8ea-156">Předpokládaná metoda doručení pro aktivitu.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-156">The expected delivery method for the activity.</span></span> |
| <span data-ttu-id="2e8ea-157">Aktivita</span><span class="sxs-lookup"><span data-stu-id="2e8ea-157">Activity</span></span> | <span data-ttu-id="2e8ea-158">Toto pole obvykle identifikuje úlohu nebo úkol, který je spojen s aktivitou.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-158">This field usually identifies the job or task that is associated with the activity.</span></span> <span data-ttu-id="2e8ea-159">Mezi typické příklady patří *Plavba lodí* a *Odbavení*.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-159">Typical examples include *Sailing* and *Clearance*.</span></span> |
| <span data-ttu-id="2e8ea-160">popis</span><span class="sxs-lookup"><span data-stu-id="2e8ea-160">Description</span></span> | <span data-ttu-id="2e8ea-161">Delší popis aktivity.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-161">A longer description of the activity.</span></span> |
| <span data-ttu-id="2e8ea-162">Počáteční datum</span><span class="sxs-lookup"><span data-stu-id="2e8ea-162">Start date</span></span> | <span data-ttu-id="2e8ea-163">Toto pole zpočátku zobrazuje odhadované datum zahájení aktivity.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-163">This field initially shows the estimated start date of the activity.</span></span> <span data-ttu-id="2e8ea-164">Po zadání skutečného data ukončení předchozí aktivity se však zobrazí skutečné datum zahájení.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-164">However, after the previous activity's actual end date has been entered, it shows the actual start date.</span></span> <span data-ttu-id="2e8ea-165">Toto pole se používá k určení odhadovaného data ukončení na základě doby realizace.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-165">This field is used to determine the estimated end date, based on the lead time.</span></span> |
| <span data-ttu-id="2e8ea-166">Odhadované datum ukončení</span><span class="sxs-lookup"><span data-stu-id="2e8ea-166">Estimated end date</span></span> | <span data-ttu-id="2e8ea-167">Hodnota tohoto pole se počítá na základě data zahájení a doby realizace.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-167">The value of this field is calculated based on the start date and lead time.</span></span> <span data-ttu-id="2e8ea-168">Obvykle nebudete hodnotu upravovat přímo.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-168">You won't usually edit the value directly.</span></span> |
| <span data-ttu-id="2e8ea-169">Skutečné datum dokončení</span><span class="sxs-lookup"><span data-stu-id="2e8ea-169">Actual end date</span></span> | <span data-ttu-id="2e8ea-170">Uživatel by měl toto pole aktualizovat co nejdříve po výskytu aktivity.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-170">A user should update this field as soon as possible after the activity has occurred.</span></span> <span data-ttu-id="2e8ea-171">Skutečná doba realizace se poté aktualizuje.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-171">The actual lead time is then updated.</span></span> |
| <span data-ttu-id="2e8ea-172">Odhadované dny</span><span class="sxs-lookup"><span data-stu-id="2e8ea-172">Estimated days</span></span> | <span data-ttu-id="2e8ea-173">Odhadovaná doba (ve dnech) potřebná k dokončení aktivity.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-173">The estimated time (in days) that is required to complete the activity.</span></span> |
| <span data-ttu-id="2e8ea-174">Skutečné dny</span><span class="sxs-lookup"><span data-stu-id="2e8ea-174">Actual days</span></span> | <span data-ttu-id="2e8ea-175">Skutečná doba (ve dnech) potřebná k dokončení aktivity.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-175">The actual time (in days) that is required to complete the activity.</span></span> |
| <span data-ttu-id="2e8ea-176">Poznámka</span><span class="sxs-lookup"><span data-stu-id="2e8ea-176">Note</span></span> | <span data-ttu-id="2e8ea-177">Toto pole použijte k přidání různých poznámek a podrobností o aktivitě.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-177">Use this field to add miscellaneous notes and details about the activity.</span></span> |

## <a name="information-and-settings-on-the-general-tab"></a><span data-ttu-id="2e8ea-178">Informace a nastavení na kartě Obecné</span><span class="sxs-lookup"><span data-stu-id="2e8ea-178">Information and settings on the General tab</span></span>

<span data-ttu-id="2e8ea-179">Karta **Obecné** zobrazuje informace o úseku, který je vybrán na kartě **Přehled**. Ačkoli se tu opakují některé informace uvedené na kartě **Přehled**, obsahuje také další informace o vybraném úseku.</span><span class="sxs-lookup"><span data-stu-id="2e8ea-179">The **General** tab shows information about the leg that is selected on the **Overview** tab. Although it repeats some of the information that appears on the **Overview** tab, it also includes additional information about the selected leg.</span></span>
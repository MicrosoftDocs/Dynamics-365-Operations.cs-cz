---
title: Pojistné doby
description: Toto téma popisuje, jak lze použít pojistné doby s doplňkem optimalizace plánování pro Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4a15b1c3df5de1dc5a55cfaa08686ee85ed50ba3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236020"
---
# <a name="safety-margins"></a><span data-ttu-id="6184a-103">Pojistné doby</span><span class="sxs-lookup"><span data-stu-id="6184a-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6184a-104">Toto téma popisuje, jak lze použít pojistné doby s doplňkem optimalizace plánování pro Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6184a-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="6184a-105">Přehled pojistných dob</span><span class="sxs-lookup"><span data-stu-id="6184a-105">Safety margins overview</span></span>

<span data-ttu-id="6184a-106">Účelem pojistných dob je povolit nastavení, které poskytuje určitou časovou rezervu nad rámec běžné doby realizace.</span><span class="sxs-lookup"><span data-stu-id="6184a-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="6184a-107">Například když materiál musí být vybalen nebo zkontrolován poté, co dorazí od dodavatele, nemůžete jen tak přidat čas navíc k době realizace nákupu, protože tento přístup poskytne dodavateli další časovou rezervu.</span><span class="sxs-lookup"><span data-stu-id="6184a-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="6184a-108">V tomto příkladu použijeme rezervu příjmu k zajištění, že dodavatel provede dodávku dříve.</span><span class="sxs-lookup"><span data-stu-id="6184a-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="6184a-109">Tento přístup poskytuje časovou rezervu, aby bylo možné se zbožím manipulovat interně.</span><span class="sxs-lookup"><span data-stu-id="6184a-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="6184a-110">Existují tři typy pojistných dob:</span><span class="sxs-lookup"><span data-stu-id="6184a-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="6184a-111">**Rezerva** – Časová rezerva pro zadání objednávky dodávky</span><span class="sxs-lookup"><span data-stu-id="6184a-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="6184a-112">**Rezerva příjmu** – Časová rezerva pro zpracování příchozí dodávky</span><span class="sxs-lookup"><span data-stu-id="6184a-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="6184a-113">**Rezerva výdeje** – Časová rezerva pro manipulaci se zásilkami</span><span class="sxs-lookup"><span data-stu-id="6184a-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="6184a-114">Následující obrázek ukazuje, jak tyto pojistné doby platí v průběhu času.</span><span class="sxs-lookup"><span data-stu-id="6184a-114">The following illustration shows how these safety margins apply over time.</span></span>

![Pojistné doby](media/safety-margins-1.png)

<span data-ttu-id="6184a-116">Všechny pojistné doby jsou definovány ve dnech.</span><span class="sxs-lookup"><span data-stu-id="6184a-116">All margins are defined in days.</span></span> <span data-ttu-id="6184a-117">Výchozí hodnota *0* (nula) označuje, že není použita žádná pojistná doba.</span><span class="sxs-lookup"><span data-stu-id="6184a-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="6184a-118">Pokud nastavíte více pojistných dob, přidají se všechny k celkovému času od *data objednávky* dodávky po *datum požadavku* poptávky.</span><span class="sxs-lookup"><span data-stu-id="6184a-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="6184a-119">Například nastavení nemá žádnou dobu realizace a všechny tři typy pojistných dob jsou nastaveny na jeden den.</span><span class="sxs-lookup"><span data-stu-id="6184a-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="6184a-120">V takovém případě budou mezi datem objednávky dodávky a datem požadavku poptávky tři dny, takže pokud je datum objednávky 1. července, datem požadavku bude 4. července.</span><span class="sxs-lookup"><span data-stu-id="6184a-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="6184a-121">Rezerva příjmu</span><span class="sxs-lookup"><span data-stu-id="6184a-121">Receipt margin</span></span>

<span data-ttu-id="6184a-122">Rezerva příjmu je pravděpodobně nejpoužívanější ze tří pojistných dob.</span><span class="sxs-lookup"><span data-stu-id="6184a-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="6184a-123">Používá se na *datum doručení* a zpět z *data požadavku*.</span><span class="sxs-lookup"><span data-stu-id="6184a-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="6184a-124">Jinými slovy, produkty by měly být obdrženy stanovený počet dnů rezervy příjmu před tím, než jsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="6184a-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="6184a-125">Následující obrázek znázorňuje rezervu příjmu.</span><span class="sxs-lookup"><span data-stu-id="6184a-125">The following illustration highlights the receipt margin.</span></span>

![Rezerva příjmu](media/safety-margins-2.png)

<span data-ttu-id="6184a-127">Rezerva příjmu se obvykle používá jako časová rezerva, aby se zajistil čas pro registraci skladu nebo jiné časově náročné procesy, které nejsou zachyceny jako součást obecné doby realizace v systému.</span><span class="sxs-lookup"><span data-stu-id="6184a-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="6184a-128">Jednou z výhod pro nákupy je, že *datum doručení* nákupní objednávky se odpovídajícím způsobem posune dopředu.</span><span class="sxs-lookup"><span data-stu-id="6184a-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="6184a-129">Pokud místo použití rezervy příjmu zvýšíte dobu realizace, bude dodavatel i nadále vyzván k dodání na poslední chvíli.</span><span class="sxs-lookup"><span data-stu-id="6184a-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="6184a-130">Všimněte si, že rezerva příjmu nemění *datum požadavku* dodávky.</span><span class="sxs-lookup"><span data-stu-id="6184a-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="6184a-131">Proto není rezerva příjmu přímo viditelná, když se porovnávají data požadavků na poptávku a nabídku (například na stránce **Čisté požadavky**).</span><span class="sxs-lookup"><span data-stu-id="6184a-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="6184a-132">Pokud je například rezerva příjmu nastavena na čtyři dny a řádek nákupní objednávky je naplánován pro příjem k patnáctému v měsíci, vypočítá hlavní plánování upravené datum příjmu na devatenáctého v měsíci.</span><span class="sxs-lookup"><span data-stu-id="6184a-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="6184a-133">Všimněte si, že rezerva příjmu se nepoužije, když se jako dodávka použijí zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="6184a-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="6184a-134">Předpokládá se, že veškeré zásoby na skladě jsou k dispozici okamžitě bez ohledu na to, kdy byly skutečně přijaty.</span><span class="sxs-lookup"><span data-stu-id="6184a-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="6184a-135">Rezerva</span><span class="sxs-lookup"><span data-stu-id="6184a-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="6184a-136">**Již brzy:** Tato funkce zatím není optimalizací plánování podporována.</span><span class="sxs-lookup"><span data-stu-id="6184a-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="6184a-137">Dokud není podporována, všechny hodnoty, které jsou zadány v poli **Rezerva přidaná k době realizace položky** budou považovány za *0* (nula).</span><span class="sxs-lookup"><span data-stu-id="6184a-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="6184a-138">Následující obrázek znázorňuje rezervu.</span><span class="sxs-lookup"><span data-stu-id="6184a-138">The following illustration highlights the reorder margin.</span></span>

![Rezerva](media/safety-margins-3.png)

<span data-ttu-id="6184a-140">Rezerva je přidána před dobu realizace položky pro všechny plánované objednávky během hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="6184a-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="6184a-141">Proto zajišťuje dodatečný čas pro vystavení objednávky dodávky.</span><span class="sxs-lookup"><span data-stu-id="6184a-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="6184a-142">Tato pojistná doba se obvykle používá jako časová rezerva k zajištění času pro schvalovací procesy nebo jiné interní procesy, které jsou vyžadovány během vytváření objednávek dodávky.</span><span class="sxs-lookup"><span data-stu-id="6184a-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="6184a-143">Rezerva se vloží mezi *datum objednávky* nabídky a *počáteční datum*.</span><span class="sxs-lookup"><span data-stu-id="6184a-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="6184a-144">Rezerva výdeje</span><span class="sxs-lookup"><span data-stu-id="6184a-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="6184a-145">**Již brzy:** Tato funkce zatím není optimalizací plánování podporována.</span><span class="sxs-lookup"><span data-stu-id="6184a-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="6184a-146">Dokud není podporována, všechny hodnoty, které jsou zadány v poli **Rezerva výdeje odečtená od požadovaného data** budou považovány za *0* (nula).</span><span class="sxs-lookup"><span data-stu-id="6184a-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="6184a-147">Následující obrázek znázorňuje rezervu výdeje.</span><span class="sxs-lookup"><span data-stu-id="6184a-147">The following illustration highlights the issue margin.</span></span>

![Rezerva výdeje](media/safety-margins-4.png)

<span data-ttu-id="6184a-149">Rezerva výdeje se odečte od data požadavku poptávky během hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="6184a-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="6184a-150">Pomáhá zajistit, abyste měli čas reagovat a odeslat příchozí objednávky nabídky.</span><span class="sxs-lookup"><span data-stu-id="6184a-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="6184a-151">Tato pojistná doba se obvykle používá jako časová rezerva k zajištění času pro expedici a související odchozí procesy skladu.</span><span class="sxs-lookup"><span data-stu-id="6184a-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="6184a-152">Všimněte si, že když se použije rezerva výdeje, neodpovídají související data požadavků nabídky a poptávky.</span><span class="sxs-lookup"><span data-stu-id="6184a-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="6184a-153">Místo toho se liší o rezervu výdeje, protože rezerva výdeje je přidána mezi *datum požadavku* dodávky a *datum požadavku* poptávky.</span><span class="sxs-lookup"><span data-stu-id="6184a-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="6184a-154">Nastavení pojistných dob</span><span class="sxs-lookup"><span data-stu-id="6184a-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="6184a-155">Zapnutí pojistných dob ve správě funkcí</span><span class="sxs-lookup"><span data-stu-id="6184a-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="6184a-156">Než můžete použít tuto funkci s optimalizací plánování, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="6184a-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="6184a-157">Správci mohou pomocí pracovního prostoru [Správa funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="6184a-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6184a-158">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="6184a-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6184a-159">**Modul:** _Hlavní plánování_</span><span class="sxs-lookup"><span data-stu-id="6184a-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="6184a-160">**Název funkce:** _Pojistné doby pro optimalizaci plánování_</span><span class="sxs-lookup"><span data-stu-id="6184a-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="6184a-161">Definování pojistných dob</span><span class="sxs-lookup"><span data-stu-id="6184a-161">Define safety margins</span></span>

<span data-ttu-id="6184a-162">Pojistné doby mají flexibilní nastavení.</span><span class="sxs-lookup"><span data-stu-id="6184a-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="6184a-163">Lze je nastavit jak na *skupinu disponsibility*, tak na *hlavní plán*.</span><span class="sxs-lookup"><span data-stu-id="6184a-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="6184a-164">Je důležité, abyste pochopili, že pojistné doby jsou přidávány přes sebe.</span><span class="sxs-lookup"><span data-stu-id="6184a-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="6184a-165">Například rezerva příjmu dvou dnů ve skupině disponsibility a tří dnů v hlavním plánu vytvoří faktickou rezervu příjmu pět dní.</span><span class="sxs-lookup"><span data-stu-id="6184a-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="6184a-166">Možnost nastavit pojistnou dobu hlavního plánu může být užitečná, když chcete simulovat delší dobu realizace nebo nejistotu pro konkrétní plán, ale bez ovlivnění denního plánování.</span><span class="sxs-lookup"><span data-stu-id="6184a-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="6184a-167">Pojistné doby skupiny disponibility</span><span class="sxs-lookup"><span data-stu-id="6184a-167">Coverage group safety margins</span></span>

<span data-ttu-id="6184a-168">Chcete-li použít pojistnou dobu na skupinu disponisibility, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="6184a-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="6184a-169">Přejděte na **Hlavní plánování \> Nastavení \> Skupiny disponibility**.</span><span class="sxs-lookup"><span data-stu-id="6184a-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="6184a-170">V podokně seznamu vyberte požadovanou skupinu disponsibility.</span><span class="sxs-lookup"><span data-stu-id="6184a-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="6184a-171">Na záložce s náhledem **Ostatní** v sekci **Pojistné doby ve dnech** použijte následující pole k nastavení požadovaných pojistných dob (ve dnech):</span><span class="sxs-lookup"><span data-stu-id="6184a-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="6184a-172">Rezerva příjmu přičtená k požadovanému datu</span><span class="sxs-lookup"><span data-stu-id="6184a-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="6184a-173">Rezerva výdeje odečtená od požadovaného data</span><span class="sxs-lookup"><span data-stu-id="6184a-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="6184a-174">Rezerva přidaná k době realizace položky</span><span class="sxs-lookup"><span data-stu-id="6184a-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="6184a-175">Pojistné doby hlavního plánu</span><span class="sxs-lookup"><span data-stu-id="6184a-175">Master plan safety margins</span></span>

<span data-ttu-id="6184a-176">Chcete-li použít pojistnou dobu na hlavní plán, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="6184a-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="6184a-177">Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.</span><span class="sxs-lookup"><span data-stu-id="6184a-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="6184a-178">V podokně seznamu vyberte požadovaný hlavní plán.</span><span class="sxs-lookup"><span data-stu-id="6184a-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="6184a-179">Na záložce s náhledem **Pojistné doby ve dnech** použijte následující pole k nastavení požadovaných pojistných dob (ve dnech):</span><span class="sxs-lookup"><span data-stu-id="6184a-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="6184a-180">Rezerva příjmu přičtená k požadovanému datu</span><span class="sxs-lookup"><span data-stu-id="6184a-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="6184a-181">Rezerva výdeje odečtená od požadovaného data</span><span class="sxs-lookup"><span data-stu-id="6184a-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="6184a-182">Rezerva přidaná k době realizace položky</span><span class="sxs-lookup"><span data-stu-id="6184a-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="6184a-183">Definování, zda jsou výpočty založeny na kalendářních nebo pracovních dnech</span><span class="sxs-lookup"><span data-stu-id="6184a-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="6184a-184">Můžete nastavit všechny pojistné doby tak, aby se počítaly na základě kalendářních nebo pracovních dnů.</span><span class="sxs-lookup"><span data-stu-id="6184a-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="6184a-185">Přejděte na **Hlavní plánování \> Nastavení \> Parametry hlavního plánování**.</span><span class="sxs-lookup"><span data-stu-id="6184a-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="6184a-186">Na kartě **Obecné** v sekci **Pojistné doby ve dnech** nastavte možnost **Pracovní dny** na *Ano* pro vypočítání pojistných dob na základě pracovních dnů.</span><span class="sxs-lookup"><span data-stu-id="6184a-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="6184a-187">Nastavte možnost na *Ne* pro výpočet pojistných dob na základě kalendářních dnů.</span><span class="sxs-lookup"><span data-stu-id="6184a-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="6184a-188">Například kalendář je otevřen od pondělí do pátku a uzavřen od soboty do neděle.</span><span class="sxs-lookup"><span data-stu-id="6184a-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="6184a-189">Pokud existuje pojistná doba v délce jednoho dne, datum požadavku v pondělí vytvoří datum doručení na předchozí pátek, protože sobota a neděle nejsou pracovní dny.</span><span class="sxs-lookup"><span data-stu-id="6184a-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="6184a-190">Kalendář, který slouží k určení pracovních dnů, závisí na nastavení a typu dodávky.</span><span class="sxs-lookup"><span data-stu-id="6184a-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="6184a-191">Lze jej určit pomocí kalendářů skupiny disponsibility, skladu a dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6184a-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="6184a-192">Pokud *sklad* není součástí dimenze disponsibility (jinými slovy, plánování je založeno pouze na *pracovišti*), kalendář skladu se nepoužívá.</span><span class="sxs-lookup"><span data-stu-id="6184a-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="6184a-193">Systém dokáže zpracovat nastavení, kde je definován jeden nebo více kalendářů.</span><span class="sxs-lookup"><span data-stu-id="6184a-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="6184a-194">Následující podsekce popisují možné kombinace, které lze použít k dosažení požadovaného výsledku.</span><span class="sxs-lookup"><span data-stu-id="6184a-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="6184a-195">Kalendář, který se používá po celou dobu trvání</span><span class="sxs-lookup"><span data-stu-id="6184a-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="6184a-196">Definované kalendáře určují skutečnou celkovou dobu realizace v kalendářních dnech, od data objednávky dodávky do data požadavku poptávky.</span><span class="sxs-lookup"><span data-stu-id="6184a-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="6184a-197">Používá se následující stanovení priorit kalendáře:</span><span class="sxs-lookup"><span data-stu-id="6184a-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="6184a-198">**Doba realizace nákupu** – Zohledňuje se pouze kalendář skupiny disponisibility.</span><span class="sxs-lookup"><span data-stu-id="6184a-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="6184a-199">**Rezerva příjmu** – Používá se kalendář skupiny disponisibility, pokud je definován.</span><span class="sxs-lookup"><span data-stu-id="6184a-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="6184a-200">V ostatních případech se používá kalendář skladu.</span><span class="sxs-lookup"><span data-stu-id="6184a-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="6184a-201">**Rezerva výdeje** – Používá se kalendář skupiny disponisibility, pokud je definován.</span><span class="sxs-lookup"><span data-stu-id="6184a-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="6184a-202">V ostatních případech se používá kalendář skladu.</span><span class="sxs-lookup"><span data-stu-id="6184a-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="6184a-203">**Rezerva** – Zohledňuje se pouze kalendář skupiny disponisibility.</span><span class="sxs-lookup"><span data-stu-id="6184a-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="6184a-204">Kalendář, který se používá pro konečné datum</span><span class="sxs-lookup"><span data-stu-id="6184a-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="6184a-205">Následující pravidla se používají k určení, zda plánovací modul může použít zadané datum pro zadaný typ data:</span><span class="sxs-lookup"><span data-stu-id="6184a-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="6184a-206">**Datum příjmu nákupu** – Použije se kalendář dodavatele, pokud je definován.</span><span class="sxs-lookup"><span data-stu-id="6184a-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="6184a-207">Jinak se použije kalendář skupiny disponisibility, pokud je definován.</span><span class="sxs-lookup"><span data-stu-id="6184a-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="6184a-208">Pokud není definován žádný z těchto kalendářů, použije se kalendář skladu.</span><span class="sxs-lookup"><span data-stu-id="6184a-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="6184a-209">**Datum příjmu převodu** – Používá se kalendář skupiny disponisibility, pokud je definován.</span><span class="sxs-lookup"><span data-stu-id="6184a-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="6184a-210">V ostatních případech se používá kalendář skladu.</span><span class="sxs-lookup"><span data-stu-id="6184a-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="6184a-211">**Datum příjmu výroby** – Používá se kalendář skupiny disponisibility, pokud je definován.</span><span class="sxs-lookup"><span data-stu-id="6184a-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="6184a-212">V ostatních případech se používá kalendář skladu.</span><span class="sxs-lookup"><span data-stu-id="6184a-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="6184a-213">**Otevřený den problému výdeje** – Používá se kalendář skladu, pokud je definován.</span><span class="sxs-lookup"><span data-stu-id="6184a-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="6184a-214">Jinak se použije kalendář skupiny disponisibility.</span><span class="sxs-lookup"><span data-stu-id="6184a-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="6184a-215">**Otevřený den objednávky** – Používá se kombinace (průsečík) kalendáře skupiny disponsibility a kalendáře dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6184a-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="6184a-216">Chcete-li použít dané datum, musí být oba kalendáře otevřené.</span><span class="sxs-lookup"><span data-stu-id="6184a-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="6184a-217">Pokud je definován pouze jeden z těchto kalendářů, použije se pouze tento kalendář.</span><span class="sxs-lookup"><span data-stu-id="6184a-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="6184a-218">Matice přehledu nastavení kalendáře</span><span class="sxs-lookup"><span data-stu-id="6184a-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="6184a-219">Následující obrázek představuje matici, která shrnuje, které kalendáře se použijí při výpočtu pojistných dob.</span><span class="sxs-lookup"><span data-stu-id="6184a-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="6184a-220">(Vyberte obrázek a otevřete jeho verzi ve vysokém rozlišení.) Následující zkratky a barvy se používají k označení, kde je specifikován každý typ kalendáře:</span><span class="sxs-lookup"><span data-stu-id="6184a-220">(Select the image to open a high-resolution version of it.) The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="6184a-221">**Skupina disponsibility (CG):** Zelená</span><span class="sxs-lookup"><span data-stu-id="6184a-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="6184a-222">**Sklad (WH):** Žlutá</span><span class="sxs-lookup"><span data-stu-id="6184a-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="6184a-223">**Dodavatel (V):** Modrá</span><span class="sxs-lookup"><span data-stu-id="6184a-223">**Vendor (V):** Blue</span></span>

<span data-ttu-id="6184a-224">[![Matice přehledu nastavení kalendáře](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span><span class="sxs-lookup"><span data-stu-id="6184a-224">[![Calendar setup overview matrix](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)</span></span>

## <a name="calculating-delays"></a><span data-ttu-id="6184a-225">Výpočet zpoždění</span><span class="sxs-lookup"><span data-stu-id="6184a-225">Calculating delays</span></span>

<span data-ttu-id="6184a-226">Všechny tři typy pojistných dob jsou zahrnuty, když systém určuje, zda je objednávka zpožděna.</span><span class="sxs-lookup"><span data-stu-id="6184a-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="6184a-227">Například položka má dobu realizace jeden den a rezervu příjmu tři dny.</span><span class="sxs-lookup"><span data-stu-id="6184a-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="6184a-228">Nákupní objednávka pro tuto položku je nastavena tak, že je dnes vyžadována.</span><span class="sxs-lookup"><span data-stu-id="6184a-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="6184a-229">V tomto případě se zpoždění počítá jako *doba realizace* + *rezerva příjmu* = čtyři dny.</span><span class="sxs-lookup"><span data-stu-id="6184a-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="6184a-230">Proto pokud je dnes 14. srpna, čtyři dny zpoždění způsobí doručení 18. srpna.</span><span class="sxs-lookup"><span data-stu-id="6184a-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="6184a-231">Následující obrázek znázorňuje tento příklad.</span><span class="sxs-lookup"><span data-stu-id="6184a-231">The following illustration shows this example.</span></span>

![Příklad výpočtu zpoždění](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="6184a-233">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="6184a-233">Additional resources</span></span>

[<span data-ttu-id="6184a-234">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="6184a-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="6184a-235">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="6184a-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
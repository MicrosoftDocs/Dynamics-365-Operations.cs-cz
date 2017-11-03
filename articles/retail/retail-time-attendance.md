---
title: "Maloobchodní čas a docházka"
description: "Toto téma popisuje scénáře, které jsou podporovány pro správu času a docházky v Microsoft Dynamics 365 for Retail."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d5672579c1e2d51e4b6494a1e86e3606c09a93a2
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="retail-time-and-attendance"></a><span data-ttu-id="f13ce-103">Čas a návštěvnost maloobchodu</span><span class="sxs-lookup"><span data-stu-id="f13ce-103">Retail time and attendance</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="f13ce-104">Toto téma popisuje scénáře, které jsou podporovány pro správu času a docházky v Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="f13ce-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span> 

<a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="f13ce-105">Spravovat nastavení pracovníka a plánování</span><span class="sxs-lookup"><span data-stu-id="f13ce-105">Manage worker setup and scheduling</span></span>
----------------------------------

### <a name="initial-configuration"></a><span data-ttu-id="f13ce-106">Počáteční konfigurace </span><span class="sxs-lookup"><span data-stu-id="f13ce-106">Initial configuration</span></span>

-   <span data-ttu-id="f13ce-107">Spusťte průvodce konfigurací.</span><span class="sxs-lookup"><span data-stu-id="f13ce-107">Run the configuration wizard.</span></span>
-   <span data-ttu-id="f13ce-108">Zaregistrujte pracovníky jako pracovníky s registrací času.</span><span class="sxs-lookup"><span data-stu-id="f13ce-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="f13ce-109">Plánování kalendářů pracovníka</span><span class="sxs-lookup"><span data-stu-id="f13ce-109">Plan worker schedules</span></span>

-   <span data-ttu-id="f13ce-110">Použijte profily pomocí plánovače práce.</span><span class="sxs-lookup"><span data-stu-id="f13ce-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="f13ce-111">Další informace naleznete v tématu <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span><span class="sxs-lookup"><span data-stu-id="f13ce-111">For more information, see <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span></span>

<span data-ttu-id="f13ce-112">Informace o postupu konfigurace naleznete v tématu <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span><span class="sxs-lookup"><span data-stu-id="f13ce-112">For information about the configuration steps, see <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="f13ce-113">Maloobchodní plánovač – Konfigurace</span><span class="sxs-lookup"><span data-stu-id="f13ce-113">Retail-specific configuration</span></span>

-   <span data-ttu-id="f13ce-114">Povolte funkční profil pro čas odchodu pro pracovníky, kterým chcete umožnit časovou registraci.</span><span class="sxs-lookup"><span data-stu-id="f13ce-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="f13ce-115">Klikněte na tlačítko **Funkční profily POS** &gt; **Funkce** &gt; **Registrace času POS** &gt; **Povolit registrace času**.</span><span class="sxs-lookup"><span data-stu-id="f13ce-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
-   <span data-ttu-id="f13ce-116">Konfigurujte skupiny oprávnění pro pokladní místa (POS) a umožněte tak zobrazit oprávnění časových položek.</span><span class="sxs-lookup"><span data-stu-id="f13ce-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="f13ce-117">Toto oprávnění umožňuje uživateli zobrazit časové záznamy jiných zaměstnanců v obchodě (a z jiných přidružených obchodů, ke kterým je uživatel přidružen, prostřednictvím adresáře).</span><span class="sxs-lookup"><span data-stu-id="f13ce-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="f13ce-118">Je vhodné povolit toto oprávnění pro roli správce, ale ne pro roli pokladníka.</span><span class="sxs-lookup"><span data-stu-id="f13ce-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="f13ce-119">Klikněte na tlačítko **Skupiny oprávnění POS** &gt; **Zobrazit záznamy časomíry**.</span><span class="sxs-lookup"><span data-stu-id="f13ce-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="f13ce-120">Čas pokladny</span><span class="sxs-lookup"><span data-stu-id="f13ce-120">Register time</span></span>
### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="f13ce-121">Čas registrace pokladníka / nepokladníka</span><span class="sxs-lookup"><span data-stu-id="f13ce-121">Cashier and non-cashier time registrations</span></span>

-   <span data-ttu-id="f13ce-122">V POS:</span><span class="sxs-lookup"><span data-stu-id="f13ce-122">On POS:</span></span>
    -   <span data-ttu-id="f13ce-123">Operace příchodu:</span><span class="sxs-lookup"><span data-stu-id="f13ce-123">Clock-in operations:</span></span>
        -   <span data-ttu-id="f13ce-124">Přihlaste se pomocí operace bez zásuvky nebo nové směny.</span><span class="sxs-lookup"><span data-stu-id="f13ce-124">Log on with a non-drawer operation or New shift.</span></span>
        -   <span data-ttu-id="f13ce-125">Vyberte hodiny operace.</span><span class="sxs-lookup"><span data-stu-id="f13ce-125">Select a Time Clock operation.</span></span>
        -   <span data-ttu-id="f13ce-126">Vyberte požadovanou operaci:</span><span class="sxs-lookup"><span data-stu-id="f13ce-126">Select a desired operation:</span></span>
            -   <span data-ttu-id="f13ce-127">Označení příchodu</span><span class="sxs-lookup"><span data-stu-id="f13ce-127">Clock-in</span></span>
            -   <span data-ttu-id="f13ce-128">Přestávka v práci</span><span class="sxs-lookup"><span data-stu-id="f13ce-128">Break for Work</span></span>
            -   <span data-ttu-id="f13ce-129">Přestávka na oběd</span><span class="sxs-lookup"><span data-stu-id="f13ce-129">Break for Lunch</span></span>
            -   <span data-ttu-id="f13ce-130">Označení odchodu</span><span class="sxs-lookup"><span data-stu-id="f13ce-130">Clock-out</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="f13ce-131">Aktuální stav</span><span class="sxs-lookup"><span data-stu-id="f13ce-131">Current state</span></span></th>
    <th><span data-ttu-id="f13ce-132">Dostupné operace</span><span class="sxs-lookup"><span data-stu-id="f13ce-132">Available operations</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="f13ce-133">Označení příchodu</span><span class="sxs-lookup"><span data-stu-id="f13ce-133">Clock-in</span></span></td>
    <td><ul>
    <li><span data-ttu-id="f13ce-134">Přestávka v práci</span><span class="sxs-lookup"><span data-stu-id="f13ce-134">Break for Work</span></span></li>
    <li><span data-ttu-id="f13ce-135">Přestávka na oběd</span><span class="sxs-lookup"><span data-stu-id="f13ce-135">Break for Lunch</span></span></li>
    <li><span data-ttu-id="f13ce-136">Označení odchodu</span><span class="sxs-lookup"><span data-stu-id="f13ce-136">Clock-out</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f13ce-137">Přestávka v práci</span><span class="sxs-lookup"><span data-stu-id="f13ce-137">Break for Work</span></span></td>
    <td><span data-ttu-id="f13ce-138">Označení příchodu</span><span class="sxs-lookup"><span data-stu-id="f13ce-138">Clock-in</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="f13ce-139">Přestávka na oběd</span><span class="sxs-lookup"><span data-stu-id="f13ce-139">Break for Lunch</span></span></td>
    <td><span data-ttu-id="f13ce-140">Označení příchodu</span><span class="sxs-lookup"><span data-stu-id="f13ce-140">Clock-in</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="f13ce-141">Označení odchodu</span><span class="sxs-lookup"><span data-stu-id="f13ce-141">Clock-out</span></span></td>
    <td><span data-ttu-id="f13ce-142">Označení příchodu</span><span class="sxs-lookup"><span data-stu-id="f13ce-142">Clock-in</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="f13ce-143">[![StavyČasomíry](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="f13ce-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>
-   <span data-ttu-id="f13ce-144">Prohlédněte si zprávu s ověřením a ověřte správnost času aktuální aktivity.</span><span class="sxs-lookup"><span data-stu-id="f13ce-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
-   <span data-ttu-id="f13ce-145">Protokolový deník:</span><span class="sxs-lookup"><span data-stu-id="f13ce-145">Logbook:</span></span>
    -   <span data-ttu-id="f13ce-146">Klepnutím na tlačítko **Protokolový deník** zobrazíte časové aktivity.</span><span class="sxs-lookup"><span data-stu-id="f13ce-146">Click **Logbook** to view time clock activity.</span></span>
    -   <span data-ttu-id="f13ce-147">Časové filtry slouží k výběru různých časových oken.</span><span class="sxs-lookup"><span data-stu-id="f13ce-147">Use time filters to select different time windows.</span></span>
    -   <span data-ttu-id="f13ce-148">Při práci na více místech obchodu se zobrazí vaše registrace času ze všech obchodů, kde máte zaznamenaný čas.</span><span class="sxs-lookup"><span data-stu-id="f13ce-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="f13ce-149">Filtr obchodu slouží k zobrazení času registrací z vybraného obchodu.</span><span class="sxs-lookup"><span data-stu-id="f13ce-149">You can use the store filter to view time registrations from a selected store.</span></span>

<!-- -->

-   <span data-ttu-id="f13ce-150">Různá časová pásma:</span><span class="sxs-lookup"><span data-stu-id="f13ce-150">Different time zones:</span></span>
    -   <span data-ttu-id="f13ce-151">Při zobrazení času z jiného místa (pro pokladní deníky nebo pomocí **Zobrazit časové záznamy** pro scénáře správce), kdy se toto umístění nachází v jiném časovém pásmu, jsou zobrazené časové záznamy převedeny na místní časové pásmo.</span><span class="sxs-lookup"><span data-stu-id="f13ce-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="f13ce-152">Například jste vedoucím dvou obchodů, jednoho v Arizoně a druhého v Nevadě.</span><span class="sxs-lookup"><span data-stu-id="f13ce-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="f13ce-153">Pokladník zaregistruje příchod v 9:00</span><span class="sxs-lookup"><span data-stu-id="f13ce-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="f13ce-154">v Arizoně.</span><span class="sxs-lookup"><span data-stu-id="f13ce-154">in Arizona.</span></span> <span data-ttu-id="f13ce-155">V daném okamžiku je čas v Nevadě 8:00.</span><span class="sxs-lookup"><span data-stu-id="f13ce-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="f13ce-156">Proto pokud jste v obchodě v Nevadě a podíváte se na záznamy registrace času, registrace času je označena jako 8:00.</span><span class="sxs-lookup"><span data-stu-id="f13ce-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="f13ce-157">Zobrazit registrace pracovní doby pracovníků</span><span class="sxs-lookup"><span data-stu-id="f13ce-157">View worker time registrations</span></span>
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="f13ce-158">Zobrazení registrací času pracovníka a filtrování podle typu obchodu nebo aktivity</span><span class="sxs-lookup"><span data-stu-id="f13ce-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="f13ce-159">V POS:</span><span class="sxs-lookup"><span data-stu-id="f13ce-159">On POS:</span></span>

-   <span data-ttu-id="f13ce-160">Vyberte **Zobrazit časové záznamy**.</span><span class="sxs-lookup"><span data-stu-id="f13ce-160">Select **View timeclock entries**.</span></span>
-   <span data-ttu-id="f13ce-161">Zobrazí se aktivity časové registrace od všech zaměstnanců přiřazených do stejných obchodů, ke kterým jste přiřazeni vy.</span><span class="sxs-lookup"><span data-stu-id="f13ce-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
-   <span data-ttu-id="f13ce-162">Můžete použít typ aktivity a uložit filtry pro filtrování registrace pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="f13ce-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="f13ce-163">Zpracovávat a spravovat registrace pracovní doby</span><span class="sxs-lookup"><span data-stu-id="f13ce-163">Process and manage time registrations</span></span>
<span data-ttu-id="f13ce-164">Uživatel aplikace Dynamics 365 for Retail používá workflow pro výpočet, schvalování a převádění registrací pracovní doby do mzdového systému.</span><span class="sxs-lookup"><span data-stu-id="f13ce-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="f13ce-165">Primární operace</span><span class="sxs-lookup"><span data-stu-id="f13ce-165">Primary operations</span></span>

-   <span data-ttu-id="f13ce-166">Vypočítat</span><span class="sxs-lookup"><span data-stu-id="f13ce-166">Calculate</span></span>
-   <span data-ttu-id="f13ce-167">Schválit</span><span class="sxs-lookup"><span data-stu-id="f13ce-167">Approve</span></span>
-   <span data-ttu-id="f13ce-168">Odeslání pro mzdu</span><span class="sxs-lookup"><span data-stu-id="f13ce-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="f13ce-169">Jiné běžné operace</span><span class="sxs-lookup"><span data-stu-id="f13ce-169">Other common operations</span></span>

-   <span data-ttu-id="f13ce-170">Hromadný odchod</span><span class="sxs-lookup"><span data-stu-id="f13ce-170">Bulk Clock-out</span></span>
-   <span data-ttu-id="f13ce-171">Registrování absence</span><span class="sxs-lookup"><span data-stu-id="f13ce-171">Register Absence</span></span>

<span data-ttu-id="f13ce-172">Další informace o postupu zpracování času a docházky naleznete v tématu <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span><span class="sxs-lookup"><span data-stu-id="f13ce-172">For more information about how to process time and attendance registrations, see <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span></span>





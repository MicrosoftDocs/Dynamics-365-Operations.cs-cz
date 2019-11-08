---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent – Core HR (11. ledna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4bf106507800f53be80af1733667bfec3023b56f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551832"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a><span data-ttu-id="cd1d4-103">Co je nového nebo upraveného v aplikaci Dynamics 365 Talent – Core HR (11. ledna 2019)</span><span class="sxs-lookup"><span data-stu-id="cd1d4-103">What's new or changed in Dynamics 365 Talent - Core HR (January 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd1d4-104">**Sestavení 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="cd1d4-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="cd1d4-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="cd1d4-106">Změny</span><span class="sxs-lookup"><span data-stu-id="cd1d4-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="cd1d4-107">Ověření požadavků na dovolenou prostřednictvím předpovědi dostupného zůstatku</span><span class="sxs-lookup"><span data-stu-id="cd1d4-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="cd1d4-108">Změny provedené v této verzi umožní zaměstnancům vyžádat si budoucí dovolenou bez odečtení od aktuálního zůstatku.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="cd1d4-109">Použijí se standardní workflow pro všechny budoucí žádosti.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="cd1d4-110">Další informace naleznete v tématu [Časové rozlišení volna na základě odpracovaných hodin](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="cd1d4-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="cd1d4-111">Zobrazení předpovídaného zůstatku dovolené v modulu ESS a People</span><span class="sxs-lookup"><span data-stu-id="cd1d4-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="cd1d4-112">Tato funkce umožňuje zobrazení zůstatků za období dovolené budoucími manažery lidských zdrojů, vedoucími a zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="cd1d4-113">Zaměstnanci mohou zobrazit budoucí zůstatky v pracovním prostoru **Samoobsluha zaměstnanců** a personalisté mají přístup ke stejnými informacím pomocí pracovní plochy **Lidé**.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="cd1d4-114">Upozornění na změnu zůstatků dovolené</span><span class="sxs-lookup"><span data-stu-id="cd1d4-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="cd1d4-115">Zůstatky dovolené zobrazí aktuální zůstatek zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="cd1d4-116">Budoucí zůstatky jsou dostupné v pracovních prostorech **Samoobslužný portál zaměstnanců** a **Lidé** po zadání hodnoty "K datu" pro výpočet předpovídaného zůstatku.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="cd1d4-117">Byla přidána navigace k zobrazení předpovídaných zůstatků v následujících oblastech:</span><span class="sxs-lookup"><span data-stu-id="cd1d4-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="cd1d4-118">Karta **Pracovní volno** v pracovním prostoru **samoobslužný servis zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="cd1d4-119">Karta **Dovolená a absence** v pracovním prostoru **Správa samoobslužného prostoru**.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="cd1d4-120">Stránka **Dovolená a absence** v pracovním prostoru **Lidé**.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="cd1d4-121">Povolení desetinných míst pro plány variabilní kompenzace (platební plány)</span><span class="sxs-lookup"><span data-stu-id="cd1d4-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="cd1d4-122">Odměny a plány variabilního odměňování mají další flexibilitu pro částky a přepisy hodnot s desetinnými místy.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="cd1d4-123">Po uložení plánu nelze změnit data registrací variabilního odměňování</span><span class="sxs-lookup"><span data-stu-id="cd1d4-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="cd1d4-124">Tato změna umožňuje aktualizace koncového data plánu (rozšířené nebo s ukončenou platností) po uložení plánu.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="cd1d4-125">Je možné stále aktivovat nebo deaktivovat plány nezávisle na počátečním a koncovém datu.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="cd1d4-126">Mzdové informace, které jsou k dispozici při přiřazení role zabezpečení Správce mezd</span><span class="sxs-lookup"><span data-stu-id="cd1d4-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="cd1d4-127">Role správce mezd byla aktualizována tak, aby měla přístup k informacím o mzdám během procesu žádosti.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="cd1d4-128">Samoobsluha pro zaměstnance | rozbalení hierarchie pozic z dlaždic se nedaří získat nadřazený uzel</span><span class="sxs-lookup"><span data-stu-id="cd1d4-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="cd1d4-129">Byly provedeny změny pro účely odstranění chyby, která nastala při přidávání hierarchie pozice do nového pracovního prostoru a navigaci v rámci organizační struktury.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="cd1d4-130">Používá se nová zpráva o ověření při použití pořadí čísel pracovníků</span><span class="sxs-lookup"><span data-stu-id="cd1d4-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="cd1d4-131">Byla provedena změna k objasnění, jaký je problém při náboru zaměstnanci v případě, že se používá nové číslo personálu.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="cd1d4-132">Samoobslužný pracovní prostor zaměstnance vybraný jako počáteční stránka spuštění</span><span class="sxs-lookup"><span data-stu-id="cd1d4-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="cd1d4-133">Když je jako počáteční stránka pro spuštění uživatele vybrán pracovní prostor **Samoobsluha zaměstnance** a tento uživatel nemá přiřazenou roli zaměstnance, systém se přesměruje na výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="cd1d4-134">Kód důvodu výpovědi aktualizuje záznam o přiřazení pozice</span><span class="sxs-lookup"><span data-stu-id="cd1d4-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="cd1d4-135">Kód důvodu výpovědi bude nyní aktualizovat přiřazení pozice při výpovědi pro zaměstnance a ukončení pozice.</span><span class="sxs-lookup"><span data-stu-id="cd1d4-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 

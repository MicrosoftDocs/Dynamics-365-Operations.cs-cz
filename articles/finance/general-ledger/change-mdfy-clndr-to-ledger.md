---
title: Změna nebo opětovné přiřazení kalendáře hlavní knihy
description: Toto téma vysvětluje, jak změnit kalendář, který je aktuálně přiřazen k hlavní knize, a jak přiřadit k hlavní knize nový kalendář.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039943"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="cfde2-103">Změna nebo opětovné přiřazení kalendáře hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="cfde2-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfde2-104">Toto téma vysvětluje, jak změnit kalendář, který je aktuálně přiřazen k hlavní knize, a jak přiřadit k hlavní knize nový kalendář.</span><span class="sxs-lookup"><span data-stu-id="cfde2-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="cfde2-105">Problém</span><span class="sxs-lookup"><span data-stu-id="cfde2-105">Issue</span></span>

<span data-ttu-id="cfde2-106">Společnosti někdy musí buď změnit existující kalendář, který je přiřazen k hlavní knize, nebo přiřadit nový kalendář.</span><span class="sxs-lookup"><span data-stu-id="cfde2-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="cfde2-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="cfde2-107">Resolution</span></span>

<span data-ttu-id="cfde2-108">Jsou dva scénáře změny nebo opětovného přiřazení kalendáře hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="cfde2-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="cfde2-109">První scénář zahrnuje změnu existujícího kalendáře, který je již k hlavní knize přiřazen.</span><span class="sxs-lookup"><span data-stu-id="cfde2-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="cfde2-110">Druhý scénář zahrnuje vytvoření nového kalendáře a jeho přiřazení k hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="cfde2-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="cfde2-111">Obě změny lze provést kdykoli, a to i po zaúčtování transakcí do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="cfde2-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="cfde2-112">Změna existujícího fiskálního kalendáře</span><span class="sxs-lookup"><span data-stu-id="cfde2-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="cfde2-113">Chcete-li změnit existující kalendář, který je přiřazen k hlavní knize, přejděte k nabídce **Hlavní kniha \> Nastavení hlavní knihy \> Hlavní kniha** a výběrem odkazu na fiskální kalendář otevřete stránku **Kalendáře hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="cfde2-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="cfde2-114">Na změny, které lze v kalendáři provést, se vztahují limity.</span><span class="sxs-lookup"><span data-stu-id="cfde2-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="cfde2-115">Můžete například změnit počáteční a koncové datum *období* v roce, ale nemůžete změnit počáteční a koncové datum *roku* v kalendáři.</span><span class="sxs-lookup"><span data-stu-id="cfde2-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="cfde2-116">Chcete-li změnit období v roce, vyberte příslušný kalendář a rok.</span><span class="sxs-lookup"><span data-stu-id="cfde2-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="cfde2-117">Nejprve použijte tlačítko **Odstranit období**, abyste odstranili některá nebo všechna existující provozní období.</span><span class="sxs-lookup"><span data-stu-id="cfde2-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="cfde2-118">Odstranit lze všechna provozní období kromě prvního.</span><span class="sxs-lookup"><span data-stu-id="cfde2-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="cfde2-119">Poté použijte tlačítko **Rozdělit období**, abyste zadáním příslušného počátečního data dalšího období rozdělili zbývající jedno nebo více období na nová období.</span><span class="sxs-lookup"><span data-stu-id="cfde2-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="cfde2-120">Jakmile změníte období v kalendáři, musíte spustit proces **Přepočítat období hlavní knihy** v každé právnické osobě (společnosti), ke které je kalendář přiřazen.</span><span class="sxs-lookup"><span data-stu-id="cfde2-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="cfde2-121">Přestože žádná varovná zpráva nepřipomíná, abyste tento krok provedli, proces přepočtu je nutný k aktualizaci období, které je přiřazeno každé zaúčtované transakci v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="cfde2-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="cfde2-122">Chcete-li spustit proces přepočtu, vyberte pro každou společnost možnost **Přepočítat období hlavní knihy** na stránce **Nastavení hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="cfde2-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="cfde2-123">Pokud není proces přepočtu spuštěn, transakční zůstatky v předvaze nebo na finančních výkazech mohou být zahrnuty do období nesprávně.</span><span class="sxs-lookup"><span data-stu-id="cfde2-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="cfde2-124">V takovém případě můžete zůstatky kdykoli opravit spuštěním procesu přepočtu.</span><span class="sxs-lookup"><span data-stu-id="cfde2-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="cfde2-125">Přiřazení nového fiskálního kalendáře</span><span class="sxs-lookup"><span data-stu-id="cfde2-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="cfde2-126">Chcete-li přiřadit nový fiskální kalendář, přejděte na **Hlavní kniha \> Nastavení hlavní knihy \> Hlavní kniha** a vyberte **Upravit**, aby stránka **Hlavní kniha** přešla do režimu úprav.</span><span class="sxs-lookup"><span data-stu-id="cfde2-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="cfde2-127">Pak vyberte v poli **Fiskální kalendář** nový fiskální kalendář.</span><span class="sxs-lookup"><span data-stu-id="cfde2-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="cfde2-128">Po změně fiskálního kalendáře hlavní knihy musíte spustit volbu **Přepočítat období hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="cfde2-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="cfde2-129">Když k hlavní knize přiřadíte nový fiskální kalendář, zobrazí se zpráva, která vám pomůže tento krok dokončit.</span><span class="sxs-lookup"><span data-stu-id="cfde2-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="cfde2-130">Přestože zpráva může znít, že je proces přepočtu volitelný, ve skutečnosti není.</span><span class="sxs-lookup"><span data-stu-id="cfde2-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="cfde2-131">Je nutné aktualizovat období, které je přiřazeno ke každé zaúčtované transakci v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="cfde2-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="cfde2-132">Chcete-li spustit proces přepočtu, vyberte možnost **Přepočítat období hlavní knihy** na stránce **Nastavení hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="cfde2-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="cfde2-133">Pokud není proces přepočtu spuštěn, transakční zůstatky v předvaze nebo na finančních výkazech mohou být zahrnuty do období nesprávně.</span><span class="sxs-lookup"><span data-stu-id="cfde2-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="cfde2-134">V takovém případě můžete zůstatky kdykoli opravit spuštěním procesu přepočtu.</span><span class="sxs-lookup"><span data-stu-id="cfde2-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

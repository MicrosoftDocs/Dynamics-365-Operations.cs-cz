---
title: Správa leasingů prostřednictvím rámce importu leasingu
description: Toto téma vysvětluje, jak pomocí rámce importu leasingu upravit více leasingů najednou.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseImportHeader
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 083adf0a4bb74ac65e6f8b5077f65c74eb3fa337
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880903"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="28c50-103">Správa leasingů prostřednictvím rámce importu leasingu</span><span class="sxs-lookup"><span data-stu-id="28c50-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28c50-104">Toto téma vysvětluje, jak pomocí rámce importu leasingu upravit více leasingů v jednom kroku.</span><span class="sxs-lookup"><span data-stu-id="28c50-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="28c50-105">Pomocí této funkce můžete ušetřit čas a můžete také zajistit přesnější úpravy snížením pravděpodobnosti lidské chyby.</span><span class="sxs-lookup"><span data-stu-id="28c50-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="28c50-106">Tato funkce navíc může propojit Microsoft Dynamics 365 Finance s externími datovými entitami pro efektivní odesílání dat.</span><span class="sxs-lookup"><span data-stu-id="28c50-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="28c50-107">K integraci leasingu majektu s externími systémy lze použít následující datové entity:</span><span class="sxs-lookup"><span data-stu-id="28c50-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="28c50-108">Pracovní leasing</span><span class="sxs-lookup"><span data-stu-id="28c50-108">Lease staging</span></span>
- <span data-ttu-id="28c50-109">Pracovní platební smlouva</span><span class="sxs-lookup"><span data-stu-id="28c50-109">Payment contract staging</span></span>
- <span data-ttu-id="28c50-110">Pracovní smlouva o zachraňovacích nákladech</span><span class="sxs-lookup"><span data-stu-id="28c50-110">Executory contract staging</span></span>

<span data-ttu-id="28c50-111">Proces importu můžete použít k úpravě leasingu, aktualizaci nefinančních informací nebo přidání nových leasingů.</span><span class="sxs-lookup"><span data-stu-id="28c50-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="28c50-112">Před importem si můžete data leasingu prohlédnout a upravit.</span><span class="sxs-lookup"><span data-stu-id="28c50-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="28c50-113">Systém může spustit následující tři procesy prostřednictvím sady pro import leasingu.</span><span class="sxs-lookup"><span data-stu-id="28c50-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="28c50-114">Typ procesu</span><span class="sxs-lookup"><span data-stu-id="28c50-114">Process type</span></span>  | <span data-ttu-id="28c50-115">popis</span><span class="sxs-lookup"><span data-stu-id="28c50-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="28c50-116">Přidat záznam</span><span class="sxs-lookup"><span data-stu-id="28c50-116">Add record</span></span>    | <span data-ttu-id="28c50-117">Migrované leasingy, které mají tento typ procesu, vytvoří leasing v systému.</span><span class="sxs-lookup"><span data-stu-id="28c50-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="28c50-118">Časový plán splátek musí být potvrzen ručně a po migraci musí být ručně zaúčtován záznam deníku počátečního uznání.</span><span class="sxs-lookup"><span data-stu-id="28c50-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="28c50-119">Aktualizovat záznam</span><span class="sxs-lookup"><span data-stu-id="28c50-119">Update record</span></span> | <span data-ttu-id="28c50-120">Migrované leasingy, které mají tento typ procesu, aktualizují hodnoty pole pro leasing, který je již v systému.</span><span class="sxs-lookup"><span data-stu-id="28c50-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="28c50-121">Pouze pole, která byla vybrána na stránce **Aktualizovat výběr polí** jsou aktualizována.</span><span class="sxs-lookup"><span data-stu-id="28c50-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="28c50-122">Doporučili jsme vám vybrat nefinanční pole na stránce **Aktualizovat výběr polí**, protože tento typ procesu neupravuje leasing.</span><span class="sxs-lookup"><span data-stu-id="28c50-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="28c50-123">Upravit záznam</span><span class="sxs-lookup"><span data-stu-id="28c50-123">Adjust record</span></span> | <span data-ttu-id="28c50-124">Migrované leasingy, které mají tento typ procesu, upravují leasing.</span><span class="sxs-lookup"><span data-stu-id="28c50-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="28c50-125">Tato úprava způsobí změnu finančního leasingu.</span><span class="sxs-lookup"><span data-stu-id="28c50-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="28c50-126">Po zpracování leasingu systém vytvoří nový plán splátek pomocí nových dat ze sady pro import leasingu.</span><span class="sxs-lookup"><span data-stu-id="28c50-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="28c50-127">Systém nepotvrzuje plán splátek ani nezaúčtuje záznam deníku úprav.</span><span class="sxs-lookup"><span data-stu-id="28c50-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="28c50-128">Po odeslání informací prostřednictvím pracovního prostoru **Správa dat** otevřete stránku **Importovat záhlaví** (**Leasing majetku \> Rámec importu leasingu \> Importovat záhlaví**).</span><span class="sxs-lookup"><span data-stu-id="28c50-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="28c50-129">Tato stránka obsahuje seznam všech importů tří datových entit, které byly uvedeny dříve.</span><span class="sxs-lookup"><span data-stu-id="28c50-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="28c50-130">Chcete-li před spuštěním zpracování zobrazit data fázování leasingu, vyberte **Data fázování**.</span><span class="sxs-lookup"><span data-stu-id="28c50-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="28c50-131">Funkce porovnání umožňuje porovnat záznam, který importujete, s odpovídajícím záznamem, který je již ve vašem systému.</span><span class="sxs-lookup"><span data-stu-id="28c50-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="28c50-132">Chcete-li porovnat jednotlivý záznam leasingu, vyberte leasing a poté vyberte **Porovnat**.</span><span class="sxs-lookup"><span data-stu-id="28c50-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="28c50-133">Tento krok byste měli provést a vygenerovat tak sestavu **Rozdíly** před migrací záznamů o leasingu.</span><span class="sxs-lookup"><span data-stu-id="28c50-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="28c50-134">Funkce Porovnat porovnává hodnoty ve datech fázování s hodnotami pro leasing, která jsou aktuálně v systému.</span><span class="sxs-lookup"><span data-stu-id="28c50-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="28c50-135">Funkce porovnání nefunguje u leasingů, které mají typ zpracování **Přidat záznam**, protože proti tomuto leasingu není co porovnávat.</span><span class="sxs-lookup"><span data-stu-id="28c50-135">The Compare functionality won't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="28c50-136">Chcete-li porovnat více leasingů najednou, přejděte na **Leasing majetku \> Rámec importu leasingu \> Periodické** a vyberte **Porovnat**.</span><span class="sxs-lookup"><span data-stu-id="28c50-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic**, and select **Compare**.</span></span>

<span data-ttu-id="28c50-137">U každé entity si můžete prohlédnout rozdíly mezi tím, co je aktuálně v systému, a tím, co je v tabulkách fázování.</span><span class="sxs-lookup"><span data-stu-id="28c50-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="28c50-138">Pro každou entitu v tabulkách fázování vyberte **Zobrazit rozdíly**.</span><span class="sxs-lookup"><span data-stu-id="28c50-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="28c50-139">Zobrazí se dialogové okno, které zobrazuje aktuální hodnotu a navrhovanou hodnotu fázování.</span><span class="sxs-lookup"><span data-stu-id="28c50-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="28c50-140">Hodnotu fázování můžete také aktualizovat změnou v sloupci **Nová hodnota** a poté vybrat **Aktualizovat fázování**.</span><span class="sxs-lookup"><span data-stu-id="28c50-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="28c50-141">Můžete ověřit leasingy, abyste zajistili, že záznamy lze přenést do systému bez chyb.</span><span class="sxs-lookup"><span data-stu-id="28c50-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="28c50-142">Před migrací záznamu o leasingu systém spustí několik ověření, aby bylo zajištěno, že bude záznam úspěšně importován.</span><span class="sxs-lookup"><span data-stu-id="28c50-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="28c50-143">Chcete-li ověřit individuální leasing, vyberte **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="28c50-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="28c50-144">Chcete-li ověřit více leasingů najednou, přejděte na **Leasing majetku \> Rámec importu leasingu \> Periodické** a vyberte **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="28c50-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic**, and select **Validate**.</span></span>

<span data-ttu-id="28c50-145">Chcete-li zpracovat individuální leasing, vyberte **Migrace záznamů o lesaingu** na stránce **Importovat záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="28c50-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="28c50-146">Při migraci leasingu provede systém akci uvedenou v poli **Typ zpracování**.</span><span class="sxs-lookup"><span data-stu-id="28c50-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="28c50-147">Chcete-li migrovat více leasingů najednou, přejděte na **Leasing majetku \> Rámec importu leasingu \> Periodické** a vyberte **Migrovat**.</span><span class="sxs-lookup"><span data-stu-id="28c50-147">To migrate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic**, and select **Migrate**.</span></span>

<span data-ttu-id="28c50-148">Po porovnání leasingu můžete spustit sestavu a zobrazit rozdíly pro každý leasing, který je zahrnut v ID importu.</span><span class="sxs-lookup"><span data-stu-id="28c50-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="28c50-149">Chcete-li spustit sestavu pro jeden leasing, vyberte tento leasing v datech fázování a poté vyberte **Porovnat a zobrazit sestavu \> Sestava o rozdílech**.</span><span class="sxs-lookup"><span data-stu-id="28c50-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="28c50-150">Chcete-li porovnat více leasingů najednou, přejděte na **Leasing majetku \> Rámec importu leasingu \> Periodické** a vyberte **Porovnat**.</span><span class="sxs-lookup"><span data-stu-id="28c50-150">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic** and select **Compare**.</span></span> 

## <a name="set-up-update-fields"></a><span data-ttu-id="28c50-151">Nastavení polí aktualizací</span><span class="sxs-lookup"><span data-stu-id="28c50-151">Set up update fields</span></span>

<span data-ttu-id="28c50-152">Pokud používáte rámec importu leasingu k aktualizaci leasingu a typ zpracování je **Aktualizovat záznam**, můžete vybrat konkrétní pole k aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="28c50-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="28c50-153">Přejděte na **Leasing majetku \> Rámec importu leasingu \> Nastavení \> Aktualizovat výběr pole**.</span><span class="sxs-lookup"><span data-stu-id="28c50-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="28c50-154">Na stránce, která se zobrazí, vyberte pole, která chcete aktualizovat, a poté je výběrem zelené šipky přesuňte na seznam **Vybraná pole**.</span><span class="sxs-lookup"><span data-stu-id="28c50-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="28c50-155">Pouze pole v seznamu **Vybraná pole** lze aktualizovat pomocí sady pro import leasingu.</span><span class="sxs-lookup"><span data-stu-id="28c50-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

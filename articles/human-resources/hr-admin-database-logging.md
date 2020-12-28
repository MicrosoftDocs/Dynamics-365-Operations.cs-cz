---
title: Konfigurace a správa protokolování databáze
description: Můžete sledovat změny tabulek a polí v Dynamics 365 Human Resources s protokolováním databáze.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417630"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="14cc0-103">Konfigurace a správa protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="14cc0-103">Configure and manage database logging</span></span>

<span data-ttu-id="14cc0-104">Můžete sledovat změny tabulek a polí v Dynamics 365 Human Resources s protokolováním databáze.</span><span class="sxs-lookup"><span data-stu-id="14cc0-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="14cc0-105">Toto téma popisuje následující postupy:</span><span class="sxs-lookup"><span data-stu-id="14cc0-105">This topic describes how to:</span></span>

- <span data-ttu-id="14cc0-106">Správa zabezpečení a výkonu pro protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="14cc0-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="14cc0-107">Nastavit protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="14cc0-107">Set up database logging</span></span>
- <span data-ttu-id="14cc0-108">Vyčištění protokolů databáze</span><span class="sxs-lookup"><span data-stu-id="14cc0-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="14cc0-109">Přehled protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="14cc0-109">Overview of database logging</span></span>

<span data-ttu-id="14cc0-110">Protokolování databáze sleduje konkrétní změny tabulek a polí Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="14cc0-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="14cc0-111">Tyto změny zahrnují vkládání, aktualizaci nebo odstraňování.</span><span class="sxs-lookup"><span data-stu-id="14cc0-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="14cc0-112">Protokolování databáze ukládá záznam změn do tabulek nebo polí v tabulce protokolu databáze.</span><span class="sxs-lookup"><span data-stu-id="14cc0-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="14cc0-113">Obchodní využití protokolování databáze zahrnuje:</span><span class="sxs-lookup"><span data-stu-id="14cc0-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="14cc0-114">Vytvoření záznamu auditu změn konkrétních tabulek, které obsahují citlivé informace.</span><span class="sxs-lookup"><span data-stu-id="14cc0-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="14cc0-115">Sledování jednotlivých transakcí.</span><span class="sxs-lookup"><span data-stu-id="14cc0-115">Tracking single transactions.</span></span> <span data-ttu-id="14cc0-116">Protokolování databáze není určeno ke sledování automatických transakcí, které probíhají v dávkových úlohách.</span><span class="sxs-lookup"><span data-stu-id="14cc0-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="14cc0-117">Zabezpečení pro protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="14cc0-117">Security for database logging</span></span>

<span data-ttu-id="14cc0-118">Protokoly databází mohou obsahovat citlivá data.</span><span class="sxs-lookup"><span data-stu-id="14cc0-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="14cc0-119">Omezte přístup tak, aby zahrnoval pouze role zabezpečení, které vyžadují přístup k datům protokolu.</span><span class="sxs-lookup"><span data-stu-id="14cc0-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="14cc0-120">Protokolování databáze a výkon</span><span class="sxs-lookup"><span data-stu-id="14cc0-120">Database logging and performance</span></span>

<span data-ttu-id="14cc0-121">Ačkoli je to hodnotné z obchodního hlediska, protokolování databáze může být nákladné z hlediska používání a správy zdrojů.</span><span class="sxs-lookup"><span data-stu-id="14cc0-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="14cc0-122">Dopady výkonu protokolování databáze zahrnuje:</span><span class="sxs-lookup"><span data-stu-id="14cc0-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="14cc0-123">Tabulka databázového protokolu se může rychle rozšiřovat a způsobit nárůst velikosti databáze.</span><span class="sxs-lookup"><span data-stu-id="14cc0-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="14cc0-124">Rozrůstání tabulky závisí na množství zaprotokolovaných dat, která se rozhodnete zachovat.</span><span class="sxs-lookup"><span data-stu-id="14cc0-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="14cc0-125">Ve výchozím nastavení tabulka protokolu databáze uchovává data protokolu pouze za 30 dní.</span><span class="sxs-lookup"><span data-stu-id="14cc0-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="14cc0-126">Protokolování databáze může nepříznivě ovlivnit dlouhodobé automatizované procesy, například dlouhodobý import dat.</span><span class="sxs-lookup"><span data-stu-id="14cc0-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="14cc0-127">Doporučené postupy</span><span class="sxs-lookup"><span data-stu-id="14cc0-127">Best practices</span></span>

<span data-ttu-id="14cc0-128">Chcete-li vylepšit výkon, omezte položky protokolu výběrem konkrétních polí k zaprotokolování místo celých tabulek.</span><span class="sxs-lookup"><span data-stu-id="14cc0-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="14cc0-129">Z důvodu udržení celkového výkonu je protokolování databáze omezeno na 20 tabulek.</span><span class="sxs-lookup"><span data-stu-id="14cc0-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="14cc0-130">Pro jednotlivá pole lze protokolovat pouze aktualizace.</span><span class="sxs-lookup"><span data-stu-id="14cc0-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="14cc0-131">Nastavit protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="14cc0-131">Set up database logging</span></span>

<span data-ttu-id="14cc0-132">Můžete použít průvodce **Protokolováním změn databáze** k nastavení protokolování databáze.</span><span class="sxs-lookup"><span data-stu-id="14cc0-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="14cc0-133">Průvodce poskytuje flexibilní způsob nastavení protokolování tabulek nebo polí.</span><span class="sxs-lookup"><span data-stu-id="14cc0-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="14cc0-134">Přejděte na **Správa systému > Odkazy > Databáze > Nastavení protokolu databáze**.</span><span class="sxs-lookup"><span data-stu-id="14cc0-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="14cc0-135">Výběrem tlačítka **Nový** spusťte průvodce **změnami protokolování databáze**.</span><span class="sxs-lookup"><span data-stu-id="14cc0-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="14cc0-136">Průvodce dokončete.</span><span class="sxs-lookup"><span data-stu-id="14cc0-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="14cc0-137">Vyčištění protokolů databáze</span><span class="sxs-lookup"><span data-stu-id="14cc0-137">Clean up database logs</span></span>

<span data-ttu-id="14cc0-138">Můžete odstranit všechny nebo část protokolů databáze pomocí následujících možností:</span><span class="sxs-lookup"><span data-stu-id="14cc0-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="14cc0-139">Vyberte všechny protokoly pro konkrétní tabulku.</span><span class="sxs-lookup"><span data-stu-id="14cc0-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="14cc0-140">Vyberte konkrétní typy protokolu databáze.</span><span class="sxs-lookup"><span data-stu-id="14cc0-140">Select specific types of database log.</span></span>
- <span data-ttu-id="14cc0-141">Vyberte datum a čas vytvoření protokolu.</span><span class="sxs-lookup"><span data-stu-id="14cc0-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="14cc0-142">Chcete-li nastavit čištění protokolu databáze, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="14cc0-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="14cc0-143">Přejděte na **Správa systému > Odkazy > Databáze > Protokol databáze**.</span><span class="sxs-lookup"><span data-stu-id="14cc0-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="14cc0-144">Vyberte **Vyčistit protokol**.</span><span class="sxs-lookup"><span data-stu-id="14cc0-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="14cc0-145">Vyberte metodu výběru protokolů k odstranění zadáním jedné z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="14cc0-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="14cc0-146">ID tabulky</span><span class="sxs-lookup"><span data-stu-id="14cc0-146">Table ID</span></span>
   - <span data-ttu-id="14cc0-147">Typ protokolu</span><span class="sxs-lookup"><span data-stu-id="14cc0-147">Type of log</span></span>
   - <span data-ttu-id="14cc0-148">Datum a čas vytvoření</span><span class="sxs-lookup"><span data-stu-id="14cc0-148">Created date and time</span></span>

3. <span data-ttu-id="14cc0-149">Pomocí karty **Vyčištění protokolu databáze** zjistěte, kdy spustit úlohu vyčištění protokolu.</span><span class="sxs-lookup"><span data-stu-id="14cc0-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="14cc0-150">Ve výchozím nastavení jsou protokoly databáze k dispozici po dobu 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="14cc0-150">By default, database logs are available for 30 days.</span></span>

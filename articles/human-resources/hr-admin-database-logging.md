---
title: Konfigurace a správa protokolování databáze
description: Můžete sledovat změny tabulek a polí v Dynamics 365 Human Resources s protokolováním databáze.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae974436469c00a3df6fd40d9d60521a0883a917
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054805"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="1db93-103">Konfigurace a správa protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="1db93-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1db93-104">Můžete sledovat změny tabulek a polí v Dynamics 365 Human Resources s protokolováním databáze.</span><span class="sxs-lookup"><span data-stu-id="1db93-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="1db93-105">Toto téma popisuje následující postupy:</span><span class="sxs-lookup"><span data-stu-id="1db93-105">This topic describes how to:</span></span>

- <span data-ttu-id="1db93-106">Správa zabezpečení a výkonu pro protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="1db93-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="1db93-107">Nastavit protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="1db93-107">Set up database logging</span></span>
- <span data-ttu-id="1db93-108">Vyčištění protokolů databáze</span><span class="sxs-lookup"><span data-stu-id="1db93-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="1db93-109">Přehled protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="1db93-109">Overview of database logging</span></span>

<span data-ttu-id="1db93-110">Protokolování databáze sleduje konkrétní změny tabulek a polí Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1db93-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="1db93-111">Tyto změny zahrnují vkládání, aktualizaci nebo odstraňování.</span><span class="sxs-lookup"><span data-stu-id="1db93-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="1db93-112">Protokolování databáze ukládá záznam změn do tabulek nebo polí v tabulce protokolu databáze.</span><span class="sxs-lookup"><span data-stu-id="1db93-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="1db93-113">Obchodní využití protokolování databáze zahrnuje:</span><span class="sxs-lookup"><span data-stu-id="1db93-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="1db93-114">Vytvoření záznamu auditu změn konkrétních tabulek, které obsahují citlivé informace.</span><span class="sxs-lookup"><span data-stu-id="1db93-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="1db93-115">Sledování jednotlivých transakcí.</span><span class="sxs-lookup"><span data-stu-id="1db93-115">Tracking single transactions.</span></span> <span data-ttu-id="1db93-116">Protokolování databáze není určeno ke sledování automatických transakcí, které probíhají v dávkových úlohách.</span><span class="sxs-lookup"><span data-stu-id="1db93-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="1db93-117">Zabezpečení pro protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="1db93-117">Security for database logging</span></span>

<span data-ttu-id="1db93-118">Protokoly databází mohou obsahovat citlivá data.</span><span class="sxs-lookup"><span data-stu-id="1db93-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="1db93-119">Omezte přístup tak, aby zahrnoval pouze role zabezpečení, které vyžadují přístup k datům protokolu.</span><span class="sxs-lookup"><span data-stu-id="1db93-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="1db93-120">Protokolování databáze a výkon</span><span class="sxs-lookup"><span data-stu-id="1db93-120">Database logging and performance</span></span>

<span data-ttu-id="1db93-121">Ačkoli je to hodnotné z obchodního hlediska, protokolování databáze může být nákladné z hlediska používání a správy zdrojů.</span><span class="sxs-lookup"><span data-stu-id="1db93-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="1db93-122">Dopady výkonu protokolování databáze zahrnuje:</span><span class="sxs-lookup"><span data-stu-id="1db93-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="1db93-123">Tabulka databázového protokolu se může rychle rozšiřovat a způsobit nárůst velikosti databáze.</span><span class="sxs-lookup"><span data-stu-id="1db93-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="1db93-124">Rozrůstání tabulky závisí na množství zaprotokolovaných dat, která se rozhodnete zachovat.</span><span class="sxs-lookup"><span data-stu-id="1db93-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="1db93-125">Ve výchozím nastavení tabulka protokolu databáze uchovává data protokolu pouze za 30 dní.</span><span class="sxs-lookup"><span data-stu-id="1db93-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="1db93-126">Protokolování databáze může nepříznivě ovlivnit dlouhodobé automatizované procesy, například dlouhodobý import dat.</span><span class="sxs-lookup"><span data-stu-id="1db93-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="1db93-127">Doporučené postupy</span><span class="sxs-lookup"><span data-stu-id="1db93-127">Best practices</span></span>

<span data-ttu-id="1db93-128">Chcete-li vylepšit výkon, omezte položky protokolu výběrem konkrétních polí k zaprotokolování místo celých tabulek.</span><span class="sxs-lookup"><span data-stu-id="1db93-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="1db93-129">Z důvodu udržení celkového výkonu je protokolování databáze omezeno na 20 tabulek.</span><span class="sxs-lookup"><span data-stu-id="1db93-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="1db93-130">Pro jednotlivá pole lze protokolovat pouze aktualizace.</span><span class="sxs-lookup"><span data-stu-id="1db93-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="1db93-131">Nastavit protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="1db93-131">Set up database logging</span></span>

<span data-ttu-id="1db93-132">Můžete použít průvodce **Protokolováním změn databáze** k nastavení protokolování databáze.</span><span class="sxs-lookup"><span data-stu-id="1db93-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="1db93-133">Průvodce poskytuje flexibilní způsob nastavení protokolování tabulek nebo polí.</span><span class="sxs-lookup"><span data-stu-id="1db93-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="1db93-134">Přejděte na **Správa systému > Odkazy > Databáze > Nastavení protokolu databáze**.</span><span class="sxs-lookup"><span data-stu-id="1db93-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="1db93-135">Výběrem tlačítka **Nový** spusťte průvodce **změnami protokolování databáze**.</span><span class="sxs-lookup"><span data-stu-id="1db93-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="1db93-136">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="1db93-136">Select **Next**.</span></span> 
3. <span data-ttu-id="1db93-137">Na stránce **Tabulky a pole** průvodce vyberte tabulky a pole, u kterých chcete povolit protokolování databáze, a vyberte možnost **Další**.</span><span class="sxs-lookup"><span data-stu-id="1db93-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="1db93-138">Protokolování databáze není k dispozici u všech tabulek v databázi aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1db93-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="1db93-139">Výběrem možnosti **Zobrazit všechny tabulky** pod seznamem rozbalíte seznam tabulek a polí, aby se zobrazily všechny databázové tabulky, u kterých je k dispozici protokolování databáze, ale toto bude jen podmnožina úplného seznamu databázových tabulek.</span><span class="sxs-lookup"><span data-stu-id="1db93-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="1db93-140">Na stránce **Typy změn** průvodce vyberte datové operace, u kterých chcete sledovat změny pro každou z tabulek a polí, a vyberte možnost **Další**.</span><span class="sxs-lookup"><span data-stu-id="1db93-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="1db93-141">V následující tabulce najdete popis datových operací, které jsou k dispozici u protokolování.</span><span class="sxs-lookup"><span data-stu-id="1db93-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="1db93-142">Na stránce **Dokončit** zkontrolujte provedené změny a vyberte možnost **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="1db93-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="1db93-143">Operace</span><span class="sxs-lookup"><span data-stu-id="1db93-143">Operation</span></span> | <span data-ttu-id="1db93-144">popis</span><span class="sxs-lookup"><span data-stu-id="1db93-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="1db93-145">Sledovat nové transakce</span><span class="sxs-lookup"><span data-stu-id="1db93-145">Track new transactions</span></span> | <span data-ttu-id="1db93-146">Vytvořte protokol pro nové záznamy, které jsou vytvořeny v tabulce.</span><span class="sxs-lookup"><span data-stu-id="1db93-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="1db93-147">Aktualizace</span><span class="sxs-lookup"><span data-stu-id="1db93-147">Update</span></span> | <span data-ttu-id="1db93-148">Vytvořte protokol pro aktualizace záznamů tabulky nebo aktualizace jednotlivě vybraných polí v tabulce.</span><span class="sxs-lookup"><span data-stu-id="1db93-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="1db93-149">Pokud se rozhodnete protokolovat aktualizace pro tabulku, vytvoří se záznam protokolu pokaždé, když se provede aktualizace jakéhokoli pole libovolného záznamu v tabulce.</span><span class="sxs-lookup"><span data-stu-id="1db93-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="1db93-150">Pokud se rozhodnete protokolovat aktualizace pro konkrétní pole, záznam protokolu se vytvoří, pouze když se provedou aktualizace těchto polí záznamů tabulky.</span><span class="sxs-lookup"><span data-stu-id="1db93-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="1db93-151">Odstranit</span><span class="sxs-lookup"><span data-stu-id="1db93-151">Delete</span></span> | <span data-ttu-id="1db93-152">Vytvořte protokol pro záznamy odstraněné z tabulky.</span><span class="sxs-lookup"><span data-stu-id="1db93-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="1db93-153">Přejmenovat klíč</span><span class="sxs-lookup"><span data-stu-id="1db93-153">Rename key</span></span> | <span data-ttu-id="1db93-154">Vytvořte záznam protokolu při přejmenování klíče tabulky.</span><span class="sxs-lookup"><span data-stu-id="1db93-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="1db93-155">Vyčištění protokolů databáze</span><span class="sxs-lookup"><span data-stu-id="1db93-155">Clean up database logs</span></span>

<span data-ttu-id="1db93-156">Můžete odstranit všechny nebo část protokolů databáze pomocí následujících možností:</span><span class="sxs-lookup"><span data-stu-id="1db93-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="1db93-157">Vyberte všechny protokoly pro konkrétní tabulku.</span><span class="sxs-lookup"><span data-stu-id="1db93-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="1db93-158">Vyberte konkrétní typy protokolu databáze.</span><span class="sxs-lookup"><span data-stu-id="1db93-158">Select specific types of database log.</span></span>
- <span data-ttu-id="1db93-159">Vyberte datum a čas vytvoření protokolu.</span><span class="sxs-lookup"><span data-stu-id="1db93-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="1db93-160">Chcete-li nastavit čištění protokolu databáze, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="1db93-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="1db93-161">Přejděte na **Správa systému > Odkazy > Databáze > Protokol databáze**.</span><span class="sxs-lookup"><span data-stu-id="1db93-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="1db93-162">Vyberte **Vyčistit protokol**.</span><span class="sxs-lookup"><span data-stu-id="1db93-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="1db93-163">Vyberte metodu výběru protokolů k odstranění zadáním jedné z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="1db93-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="1db93-164">ID tabulky</span><span class="sxs-lookup"><span data-stu-id="1db93-164">Table ID</span></span>
   - <span data-ttu-id="1db93-165">Typ protokolu</span><span class="sxs-lookup"><span data-stu-id="1db93-165">Type of log</span></span>
   - <span data-ttu-id="1db93-166">Datum a čas vytvoření</span><span class="sxs-lookup"><span data-stu-id="1db93-166">Created date and time</span></span>

3. <span data-ttu-id="1db93-167">Pomocí karty **Vyčištění protokolu databáze** zjistěte, kdy spustit úlohu vyčištění protokolu.</span><span class="sxs-lookup"><span data-stu-id="1db93-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="1db93-168">Ve výchozím nastavení jsou protokoly databáze k dispozici po dobu 30 dnů.</span><span class="sxs-lookup"><span data-stu-id="1db93-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

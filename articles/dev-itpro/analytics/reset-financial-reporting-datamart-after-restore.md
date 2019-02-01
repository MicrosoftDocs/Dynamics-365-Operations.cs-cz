---
title: "Resetování datového tržiště finančního výkaznictví"
description: "Toto téma popisuje postup resetování datového tržiště finančního výkaznictví."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: cs-cz
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="9fe68-103">Resetování datového tržiště finančního výkaznictví</span><span class="sxs-lookup"><span data-stu-id="9fe68-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9fe68-104">Toto téma vysvětluje resetování datového tržiště finančního výkaznictví pro následující verze:</span><span class="sxs-lookup"><span data-stu-id="9fe68-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="9fe68-105">Aplikace Microsoft Dynamics 365 for Finance and Operations: Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="9fe68-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="9fe68-106">Microsoft Dynamics 365 for Finance and Operations: Finanční výkaznictví, vydání 7.0.10000.4 a vyšší</span><span class="sxs-lookup"><span data-stu-id="9fe68-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="9fe68-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (místní)</span><span class="sxs-lookup"><span data-stu-id="9fe68-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="9fe68-108">Abyste získali Finance and Operations: Finanční výkaznictví, vydání 7.2.6.0, můžete stáhnout článek znalostní báze KB 4052514 z <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span><span class="sxs-lookup"><span data-stu-id="9fe68-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="9fe68-109">Resetování datového tržiště finančního výkaznictví pro Finance and Operations, Finanční výkaznictví, vydání 7.2.6.0 a vyšší</span><span class="sxs-lookup"><span data-stu-id="9fe68-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="9fe68-110">Resetování datového tržiště finančního výkaznictví z Návrháře sestav</span><span class="sxs-lookup"><span data-stu-id="9fe68-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="9fe68-111">Kroky v tomto procesu jsou podporovány pro Finance and Operations, Finanční výkaznictví, vydání 7.2.6.0 a vyšší.</span><span class="sxs-lookup"><span data-stu-id="9fe68-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="9fe68-112">Pokud máte dřívější vydání, obraťte se na tým podpory.</span><span class="sxs-lookup"><span data-stu-id="9fe68-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="9fe68-113">V určitých situacích je nutné resetovat datové tržiště pro Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="9fe68-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="9fe68-114">Tento úkol můžete dokončit v klientovi návrháře sestav.</span><span class="sxs-lookup"><span data-stu-id="9fe68-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="9fe68-115">Zde je několik scénářů, kdy je třeba resetovat datové tržiště:</span><span class="sxs-lookup"><span data-stu-id="9fe68-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="9fe68-116">Databáze aplikace Finance and Operations byla obnovena, ale nebyla obnovena databáze datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="9fe68-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="9fe68-117">Za určité období máte nesprávná data.</span><span class="sxs-lookup"><span data-stu-id="9fe68-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="9fe68-118">Podpora vás může vyzvat k resetování datového tržiště jako součást kroku při řešení potíží.</span><span class="sxs-lookup"><span data-stu-id="9fe68-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="9fe68-119">Resetování datového tržiště má být provedeno pouze během situace, kdy je se na databázi zpracovává malé množství dat.</span><span class="sxs-lookup"><span data-stu-id="9fe68-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="9fe68-120">Finanční výkaznictví není k dispozici během procesu resetování.</span><span class="sxs-lookup"><span data-stu-id="9fe68-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="9fe68-121">Resetování datového tržiště</span><span class="sxs-lookup"><span data-stu-id="9fe68-121">Reset the data mart</span></span>

<span data-ttu-id="9fe68-122">Chcete-li resetovat datového tržiště, v návrháři sestav v nabídce **Nástroje** zvolte **Resetovat datové tržiště**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="9fe68-123">Zobrazené dialogové okno má dvě části: **Statistiky** a **Resetování**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="9fe68-124">[![Dialogové okno resetování datového tržiště](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="9fe68-124">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="9fe68-125">Pokusy o integraci</span><span class="sxs-lookup"><span data-stu-id="9fe68-125">Integration attempts</span></span>

<span data-ttu-id="9fe68-126">Mřížka **Integrace pokusí** ukazuje, kolikrát se systém pokusil integrovat transakce.</span><span class="sxs-lookup"><span data-stu-id="9fe68-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="9fe68-127">Systém pokračuje v pokusu o integraci dat několik dnů, pokud několik prvních pokusů není úspěšných.</span><span class="sxs-lookup"><span data-stu-id="9fe68-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="9fe68-128">Uvidíte, že datové tržiště je třeba resetovat, pokud je počet pokusů 8 a více a pokud existuje mnoho kombinací dimenzí nebo záznamů transakcí.</span><span class="sxs-lookup"><span data-stu-id="9fe68-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="9fe68-129">V tomto případě nebudou data vyreportována.</span><span class="sxs-lookup"><span data-stu-id="9fe68-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="9fe68-130">Stav dat</span><span class="sxs-lookup"><span data-stu-id="9fe68-130">Data status</span></span>

<span data-ttu-id="9fe68-131">Mřížka **Stav dat** poskytuje snímek transakcí, směnných kurzů a hodnoty dimenzí v datovém tržišti.</span><span class="sxs-lookup"><span data-stu-id="9fe68-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="9fe68-132">Velký počet zastaralých záznamů označuje, že došlo k četným aktualizacím záznamům.</span><span class="sxs-lookup"><span data-stu-id="9fe68-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="9fe68-133">Taková situace může způsobit pomalejší čas generování sestav.</span><span class="sxs-lookup"><span data-stu-id="9fe68-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="9fe68-134">Nezarovnané kategorie hlavního účtu</span><span class="sxs-lookup"><span data-stu-id="9fe68-134">Misaligned main account categories</span></span>

<span data-ttu-id="9fe68-135">Používáte-li verzi, která je starší než Microsoft Dynamics 365 for Finance and Operations: Finanční výkaznictví, vydání 7.2.1, může být zapotřebí resetovat datové tržiště, pokud přejmenujete účty nebo přesunete účty mezi kategoriemi účtů.</span><span class="sxs-lookup"><span data-stu-id="9fe68-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="9fe68-136">Tyto akce mohou způsobit, že hlavní kategorie účtů budou nesprávně zarovnány.</span><span class="sxs-lookup"><span data-stu-id="9fe68-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="9fe68-137">Pole **Nezarovnané kategorie hlavního účtu** ukazuje, zda dochází k daného problému.</span><span class="sxs-lookup"><span data-stu-id="9fe68-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="9fe68-138">Resetování datového tržiště Finance and Operations: Finanční výkaznictví, vydání 7.2.6.0</span><span class="sxs-lookup"><span data-stu-id="9fe68-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="9fe68-139">Chcete-li resetovat datové tržiště v aplikaci Finance and Operations: Finanční výkaznictví, vydání 7.2.6.0 a dřívější, v dialogovém okně **Resetovat datové tržiště** zvolte zaškrtávací políčko **Resetovat datové tržiště** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="9fe68-140">Resetování datového tržiště musí být prováděno pouze během plánované odstávky.</span><span class="sxs-lookup"><span data-stu-id="9fe68-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="9fe68-141">[![Zaškrtávací políčko resetování datového tržiště](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="9fe68-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="9fe68-142">Resetování datového tržiště a volba důvodu v aplikaci Microsoft Dynamics 365 for Finance and Operations: Finanční výkaznictví, vydání 7.3.0</span><span class="sxs-lookup"><span data-stu-id="9fe68-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="9fe68-143">Pokud určíte, že je nutné resetovat datové tržiště, zvolte zaškrtávací políčko **Resetovat datové tržiště** a poté vyberte příčinu v poli **Důvod**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="9fe68-144">Existují tyto možnosti:</span><span class="sxs-lookup"><span data-stu-id="9fe68-144">The following options are available:</span></span>

- <span data-ttu-id="9fe68-145">**Chybějící nebo nesprávná data** – Na základě statistik jste určili, že mohou chybět data.</span><span class="sxs-lookup"><span data-stu-id="9fe68-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="9fe68-146">Než budete pokračovat, doporučujeme, abyste kontaktovali podporu a pokusili se určit hlavní příčinu.</span><span class="sxs-lookup"><span data-stu-id="9fe68-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="9fe68-147">**Obnovit databázi** – Databáze aplikace Finance and Operations byla obnovena, ale nebyla obnovena databáze datového tržiště finančního výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="9fe68-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="9fe68-148">**Ostatní** – Resetujete datové tržiště z jiného důvodu.</span><span class="sxs-lookup"><span data-stu-id="9fe68-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="9fe68-149">Pokud se obáváte problému, kontaktujte podporu, která ho identifikuje.</span><span class="sxs-lookup"><span data-stu-id="9fe68-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="9fe68-150">[![Resetovat datové tržiště](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="9fe68-150">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="9fe68-151">Před zahájením resetu ověřte, zda všechny úlohy resetu datového tržiště dokončily počáteční vytížení.</span><span class="sxs-lookup"><span data-stu-id="9fe68-151">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="9fe68-152">To můžete potvrdit vyhledáním hodnoty ve sloupci Čas posledního spuštění výběrem položek **Nástroje** &gt; **Stav integrace**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-152">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="9fe68-153">Vymazat uživatele a společnosti</span><span class="sxs-lookup"><span data-stu-id="9fe68-153">Clear users and companies</span></span>

<span data-ttu-id="9fe68-154">Vyberte zaškrtávací políčko **Vymazat uživatele a společnosti**, pokud jste obnovili databázi, ale poté jste provedli změny uživatelů nebo společností.</span><span class="sxs-lookup"><span data-stu-id="9fe68-154">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="9fe68-155">Toto políčko budete muset zaškrtávat zřídka.</span><span class="sxs-lookup"><span data-stu-id="9fe68-155">You should rarely have to select this check box.</span></span>

<span data-ttu-id="9fe68-156">Jakmile jste připraveni zahájit proces resetování, zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-156">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="9fe68-157">Budete vyzváni k potvrzení, že jste připraveni zahájit proces.</span><span class="sxs-lookup"><span data-stu-id="9fe68-157">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="9fe68-158">Všimněte si, že finanční výkaznictví nebude k dispozici během resetování a během počáteční integrace dat, ke které dochází později.</span><span class="sxs-lookup"><span data-stu-id="9fe68-158">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="9fe68-159">Pokud chcete ověřit stav integrace, vyberte **Nástroje** &gt; **Stav integrace** a zobrazí se poslední čas, kdy byla integrace naposledy spuštěna, a její stav.</span><span class="sxs-lookup"><span data-stu-id="9fe68-159">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="9fe68-160">[![Zobrazení stavu integrace](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="9fe68-160">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="9fe68-161">Reset je dokončen, když všechna mapování zobrazují stav RanToCompletion a okno stavu integrace okno v levém dolním rohu říká Integrace dokončena.</span><span class="sxs-lookup"><span data-stu-id="9fe68-161">The reset is finished when all mappings show the status of RanToCompletion and the Integration Status window says “Integration complete” in the bottom-left corner.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="9fe68-162">Resetování datového tržiště finančního výkaznictví pro Finance and Operations, Finanční výkaznictví, vydání 7.0.10000.4 a vyšší</span><span class="sxs-lookup"><span data-stu-id="9fe68-162">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="9fe68-163">Pokud někdy obnovíte databázi aplikace Finance and Operations ze zálohy nebo zkopírujete databázi z jiného prostředí, musíte postupovat podle kroků v této části, chcete-li zajistit, aby datové tržiště finančního výkaznictví správně používalo obnovenou databázi aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe68-163">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="9fe68-164">Kroky v tomto procesu jsou podporovány aplikací Microsoft Dynamics AX, verze 7.0.1 (květen 2016) (sestavení aplikace 7.0.1265.23014 a sestavení finančního výkaznictví 7.0.10000.4) a vyšší.</span><span class="sxs-lookup"><span data-stu-id="9fe68-164">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="9fe68-165">Pokud máte dřívější verzi aplikace Finance and Operations, obraťte se na náš tým podpory pro pomoc.</span><span class="sxs-lookup"><span data-stu-id="9fe68-165">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="9fe68-166">Export definicí sestav</span><span class="sxs-lookup"><span data-stu-id="9fe68-166">Export report definitions</span></span>

<span data-ttu-id="9fe68-167">Nejdříve postupujte podle těchto kroků pro exportování návrhů sestav z návrháře sestav.</span><span class="sxs-lookup"><span data-stu-id="9fe68-167">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="9fe68-168">V návrháři sestav zvolte **Společnost** &gt; **Skupiny stavebních bloků**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-168">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="9fe68-169">Vyberte skupinu stavebních bloků k exportu a poté zvolte **Export**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-169">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fe68-170">V modulu Finance and Operations je podporována pouze jedna skupina stavebních bloků, **výchozí**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-170">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="9fe68-171">Vyberte definice sestavy k exportu:</span><span class="sxs-lookup"><span data-stu-id="9fe68-171">Select the report definitions to export:</span></span>

    - <span data-ttu-id="9fe68-172">Pokud chcete vyexportovat všechny definice sestav a přidružené stavební bloky, zvolte **Vybrat vše**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-172">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="9fe68-173">Pokud chcete exportovat konkrétní sestavy, řádky, sloupce, stromy či sady dimenzí, zvolte příslušnou kartu a vyberte položky k exportu.</span><span class="sxs-lookup"><span data-stu-id="9fe68-173">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="9fe68-174">Stisknutím a podržením klávesy Ctrl vyberte více položek na kartě. Při výběru sestav, které chcete exportovat, jsou vybrány přidružené řádky, sloupce, stromy a sady dimenzí.</span><span class="sxs-lookup"><span data-stu-id="9fe68-174">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="9fe68-175">Vyberte **Export**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-175">Select **Export**.</span></span>
5. <span data-ttu-id="9fe68-176">Zadejte název souboru a vyberte bezpečné místo, kam chcete uložit exportované definice sestavy.</span><span class="sxs-lookup"><span data-stu-id="9fe68-176">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="9fe68-177">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-177">Select **Save**.</span></span>

<span data-ttu-id="9fe68-178">Můžete kopírovat nebo odeslat tento soubor do bezpečného umístění.</span><span class="sxs-lookup"><span data-stu-id="9fe68-178">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="9fe68-179">Tímto způsobem lze soubor importovat do jiného prostředí později.</span><span class="sxs-lookup"><span data-stu-id="9fe68-179">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="9fe68-180">Informace o použití účtu úložiště Microsoft Azure naleznete v části [Přenos dat pomocí nástroje příkazového řádku AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="9fe68-180">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="9fe68-181">Microsoft neposkytuje úložiště účtu v rámci vaší smlouvy na aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe68-181">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="9fe68-182">Musíte zakoupit účet úložiště nebo použít účet úložiště ze samostatného předplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe68-182">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="9fe68-183">Musíte znát chování jednotky D na virtuálních počítačích Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe68-183">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="9fe68-184">Neukládejte trvale své exportované skupiny stavebních bloků na jednotce D. Více informací o dočasných discích naleznete v části [Princip dočasné jednotky na virtuálních počítačích Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="9fe68-184">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="9fe68-185">Ukončení služeb</span><span class="sxs-lookup"><span data-stu-id="9fe68-185">Stop services</span></span>

<span data-ttu-id="9fe68-186">Následující služby systému Microsoft Windows budou mít otevřená připojení k databázi Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe68-186">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="9fe68-187">Proto musíte použít vzdálenou plochu Microsoft pro připojení ke všem počítačům v prostředí a zastavit tyto služby pomocí services.msc.</span><span class="sxs-lookup"><span data-stu-id="9fe68-187">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="9fe68-188">World wide web publishing service (na všech počítačích AOS)</span><span class="sxs-lookup"><span data-stu-id="9fe68-188">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="9fe68-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (pouze na nesoukromých počítačích AOS)</span><span class="sxs-lookup"><span data-stu-id="9fe68-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="9fe68-190">Management Reporter 2012 Process Service (pouze v počítačích BI)</span><span class="sxs-lookup"><span data-stu-id="9fe68-190">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="9fe68-191">Resetovat</span><span class="sxs-lookup"><span data-stu-id="9fe68-191">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="9fe68-192">Stažení nejnovějšího balíčku MinorVersionDataUpgrade.zip</span><span class="sxs-lookup"><span data-stu-id="9fe68-192">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="9fe68-193">Stáhněte nejnovější balíček MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="9fe68-193">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="9fe68-194">Pokyny k vyhledání a stažení správné verze balíčku upgradu dat lze najít v části [Stažení nejnovějšího nasaditelného balíčku pro upgrade dat](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="9fe68-194">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> 

<span data-ttu-id="9fe68-195">Upgrade ke stažení balíčku MinorVersionDataUpgrade.zip není vyžadován.</span><span class="sxs-lookup"><span data-stu-id="9fe68-195">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="9fe68-196">Proto stačí postupovat podle kroků v části "Stažení nejnovějšího nasaditelného balíčku pro upgrade dat" tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="9fe68-196">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="9fe68-197">Je možné přeskočit všechny ostatní kroky v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="9fe68-197">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="9fe68-198">Spuštění skriptů proti databázi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9fe68-198">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="9fe68-199">Spusťte následující skripty proti databázi Finance and Operations (nikoli proti databázi finančního výkaznictví):</span><span class="sxs-lookup"><span data-stu-id="9fe68-199">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="9fe68-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="9fe68-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="9fe68-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="9fe68-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="9fe68-202">Tyto skripty pomáhají zaručit správnost uživatelů, rolí a nastavení sledování změn.</span><span class="sxs-lookup"><span data-stu-id="9fe68-202">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="9fe68-203">Spuštění příkazu Windows PowerShell pro resetování databáze</span><span class="sxs-lookup"><span data-stu-id="9fe68-203">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="9fe68-204">V počítači AOS spusťte Microsoft Windows PowerShell jako správce a pro resetování integrace mezi aplikací Finance and Operations a finančním výkaznictvím spusťte následující příkazy.</span><span class="sxs-lookup"><span data-stu-id="9fe68-204">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="9fe68-205">Zde uvádíme vysvětlení parametrů v příkazu **Reset-DatamartIntegration**:</span><span class="sxs-lookup"><span data-stu-id="9fe68-205">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="9fe68-206">Platné hodnoty parametru **-Reason** jsou **SERVICING**, **BADDATA** a **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-206">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="9fe68-207">Parametr **-ReasonDetail** je textový.</span><span class="sxs-lookup"><span data-stu-id="9fe68-207">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="9fe68-208">Parametry reason a reason detail budou zaznamenány ve sledování telemetrie/prostředí.</span><span class="sxs-lookup"><span data-stu-id="9fe68-208">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="9fe68-209">Po spuštění příkazů se zobrazí výzva k zadání **Y** pro potvrzení, že chcete resetovat databázi.</span><span class="sxs-lookup"><span data-stu-id="9fe68-209">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="9fe68-210">Restartování služeb</span><span class="sxs-lookup"><span data-stu-id="9fe68-210">Restart services</span></span>

<span data-ttu-id="9fe68-211">Pomocí services.msc restartujte dříve zastavené služby:</span><span class="sxs-lookup"><span data-stu-id="9fe68-211">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="9fe68-212">World wide web publishing service (na všech počítačích AOS)</span><span class="sxs-lookup"><span data-stu-id="9fe68-212">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="9fe68-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (pouze na nesoukromých počítačích AOS)</span><span class="sxs-lookup"><span data-stu-id="9fe68-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="9fe68-214">Management Reporter 2012 Process Service (pouze v počítačích BI)</span><span class="sxs-lookup"><span data-stu-id="9fe68-214">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="9fe68-215">Import definicí sestav</span><span class="sxs-lookup"><span data-stu-id="9fe68-215">Import report definitions</span></span>

<span data-ttu-id="9fe68-216">Importujte návrhy sestavy z Návrháře sestav pomocí souboru vytvořeného během exportu.</span><span class="sxs-lookup"><span data-stu-id="9fe68-216">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="9fe68-217">V návrháři sestav zvolte **Společnost** &gt; **Skupiny stavebních bloků**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-217">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="9fe68-218">Vyberte skupinu stavebních bloků k exportu a poté zvolte **Export**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-218">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fe68-219">V modulu Finance and Operations je podporována pouze jedna skupina stavebních bloků, **výchozí**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-219">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="9fe68-220">Vyberte stavební blok **Výchozí** a zvolte **Import**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-220">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="9fe68-221">Vyberte soubor obsahující definice exportované sestavy a zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-221">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="9fe68-222">V dialogovém okně **Import** vyberte definice sestav, které chcete naimportovat:</span><span class="sxs-lookup"><span data-stu-id="9fe68-222">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="9fe68-223">Pokud chcete importovat všechny definice sestav a přidružené stavební bloky, zvolte **Vybrat vše**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-223">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="9fe68-224">Chcete-li naimportovat konkrétní sestavy, řádky, sloupce, stromy nebo sady dimenzí, vyberte konkrétní sestavy, řádky, sloupce, stromy nebo sady dimenzí, které chcete naimportovat.</span><span class="sxs-lookup"><span data-stu-id="9fe68-224">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="9fe68-225">Vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-225">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="9fe68-226">Resetování datového tržiště finančního výkaznictví pro Finance and Operations (místní)</span><span class="sxs-lookup"><span data-stu-id="9fe68-226">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="9fe68-227">Požádejte všechny uživatele, aby ukončili návrháře sestav a oblast finančního výkaznictví aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe68-227">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="9fe68-228">Spusťte následující skript proti databázi finančního vykazování (MRDB).</span><span class="sxs-lookup"><span data-stu-id="9fe68-228">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="9fe68-229">Zkraťte nebo odstraňte všechny záznamy z tabulky FINANCIALREPORTS v databázi aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe68-229">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="9fe68-230">Zkraťte nebo odstraňte všechny záznamy z tabulky FINANCIALREPORTVERSION, pokud tato databáze v aplikaci Finance and Operations existuje.</span><span class="sxs-lookup"><span data-stu-id="9fe68-230">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="9fe68-231">Pokud tabulka neexistuje v databázi aplikace Finance and Operations, vynechte tento krok.</span><span class="sxs-lookup"><span data-stu-id="9fe68-231">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="9fe68-232">Spusťte skript **ResetDatamart.sql** proti databázi finančního vykazování.</span><span class="sxs-lookup"><span data-stu-id="9fe68-232">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="9fe68-233">Tento skript zakáže integraci datového tržiště, odstraní všechna data datového tržiště potom znovu povolí integraci datového tržiště.</span><span class="sxs-lookup"><span data-stu-id="9fe68-233">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="9fe68-234">Po resetování můžete znovu ověřit ručně načtení dat spuštěním následujícího dotazu proti databázi finančního výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="9fe68-234">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="9fe68-235">Potvrďte, že všechny řádky mají hodnotu **LastRunTime** a že **StateType** je nastaven na **5**.</span><span class="sxs-lookup"><span data-stu-id="9fe68-235">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="9fe68-236">Hodnota **5** pro **StateType** označuje, že data byla úspěšně znovu načtena.</span><span class="sxs-lookup"><span data-stu-id="9fe68-236">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="9fe68-237">Hodnota **7** označuje chybový stav.</span><span class="sxs-lookup"><span data-stu-id="9fe68-237">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="9fe68-238">V některých případech mapa organizační hierarchie má tento stav při prvním spuštění.</span><span class="sxs-lookup"><span data-stu-id="9fe68-238">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="9fe68-239">Chybový stav by však měl být automaticky vyřešen.</span><span class="sxs-lookup"><span data-stu-id="9fe68-239">However, the faulted state but should be automatically resolved.</span></span>

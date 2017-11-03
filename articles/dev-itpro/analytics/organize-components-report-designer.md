---
title: "Uspořádání součástí zprávy v návrháři sestavy"
description: "Poté, co jste navrhli stavební bloky a vygenerovali sestavy, je užitečné uspořádat tyto objekty a usnadnit uživatelům jejich vyhledání. Tento článek popisuje způsob uspořádání existujících sestav, stavebních bloků a objektů v návrháři sestav."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d575e2b0215b0e8c4b6cb1b17c0f1d908b862e9d
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="35cc2-104">Uspořádání součástí zprávy v návrháři sestavy</span><span class="sxs-lookup"><span data-stu-id="35cc2-104">Organize report components in report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="35cc2-105">Poté, co jste navrhli stavební bloky a vygenerovali sestavy, je užitečné uspořádat tyto objekty a usnadnit uživatelům jejich vyhledání.</span><span class="sxs-lookup"><span data-stu-id="35cc2-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="35cc2-106">Tento článek popisuje způsob uspořádání existujících sestav, stavebních bloků a objektů v návrháři sestav.</span><span class="sxs-lookup"><span data-stu-id="35cc2-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="35cc2-107">Můžete přejmenovat složky, sestavy, stavební bloky a jiné objekty v návrháři sestavy k usnadnění uspořádání souborů.</span><span class="sxs-lookup"><span data-stu-id="35cc2-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="35cc2-108">V závislosti na typu objekt, jehož název měníte, může být nutné aktualizovat přidružení tohoto objektu.</span><span class="sxs-lookup"><span data-stu-id="35cc2-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="35cc2-109">Přejmenování složky nebo stavebního bloku v Návrháři sestav</span><span class="sxs-lookup"><span data-stu-id="35cc2-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="35cc2-110">V Návrháři sestav můžete přejmenovat složky, definice sestav, definice řádků, definice sloupců a definice stromu výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="35cc2-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="35cc2-111">**Poznámka:** při přejmenování stavebního bloku je nutné aktualizovat všechny definice sestavy, které používají daný stavební blok.</span><span class="sxs-lookup"><span data-stu-id="35cc2-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="35cc2-112">Jinak nelze vytvořit novou sestavu.</span><span class="sxs-lookup"><span data-stu-id="35cc2-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="35cc2-113">Přejmenování složky nebo stavebního bloku v Návrháři sestav</span><span class="sxs-lookup"><span data-stu-id="35cc2-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="35cc2-114">V Návrháři sestav můžete k vyhledání složky nebo objektu k přejmenování použít navigační podokno.</span><span class="sxs-lookup"><span data-stu-id="35cc2-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="35cc2-115">Klikněte pravým tlačítkem myši na objekt a poté klikněte na možnost **Přejmenovat**.</span><span class="sxs-lookup"><span data-stu-id="35cc2-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="35cc2-116">Pole **Název** v podokně navigace se zpřístupní.</span><span class="sxs-lookup"><span data-stu-id="35cc2-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="35cc2-117">Zadejte nový název a stiskněte klávesu Enter.</span><span class="sxs-lookup"><span data-stu-id="35cc2-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="35cc2-118">Pokud je stavební blok definicí řádku, definicí sloupce nebo definicí stromu výkaznictví, je nutné aktualizovat další stavební bloky, které jsou k němu přidružené.</span><span class="sxs-lookup"><span data-stu-id="35cc2-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="35cc2-119">Klikněte pravým tlačítkem myši na stavební blok, který jste přejmenovali v kroku 3, vyberte položku **Přidružení** a poté vyberte položku v seznamu k aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="35cc2-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="35cc2-120">Opakujte krok 4, dokud nebudou aktualizovány všechny přidružené položky.</span><span class="sxs-lookup"><span data-stu-id="35cc2-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="35cc2-121">Vytvoření a správa skupin sestav</span><span class="sxs-lookup"><span data-stu-id="35cc2-121">Create and manage report groups</span></span>
<span data-ttu-id="35cc2-122">Můžete seskupovat definice sestavy a generovat více sestav současně.</span><span class="sxs-lookup"><span data-stu-id="35cc2-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="35cc2-123">Abyste mohli vytvářet, upravovat, odstraňovat a generovat skupiny sestav, musíte mít roli návrháře nebo správce.</span><span class="sxs-lookup"><span data-stu-id="35cc2-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="35cc2-124">Uživatelé s rolí generátora mohou generovat skupiny sestav a mohou také upravovat nastavení definic sestavy pro skupiny sestav.</span><span class="sxs-lookup"><span data-stu-id="35cc2-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="35cc2-125">Vytvoření skupiny sestav</span><span class="sxs-lookup"><span data-stu-id="35cc2-125">Create a report group</span></span>

1.  <span data-ttu-id="35cc2-126">V Návrháři sestav v navigačním podokně klikněte na tlačítko **Skupiny sestav**.</span><span class="sxs-lookup"><span data-stu-id="35cc2-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="35cc2-127">V nabídce **Soubor** klepněte na **Nový** &gt; **Definice skupiny sestav** a otevřete tak novou skupinu sestav v okně prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="35cc2-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="35cc2-128">Případně klikněte na tlačítko **Skupina sestav** ![Skupina sestav](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Skupina sestav") na panelu nástrojů.</span><span class="sxs-lookup"><span data-stu-id="35cc2-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="35cc2-129">Klikněte na kartu **Skupina sestav**. Abyste přepsali informací v jednotlivých definicích sestavy pro generování této sestavy, zaškrtněte políčko **Přepsat nastavení společnosti, podrobností a data z jednotlivých definic sestavy**.</span><span class="sxs-lookup"><span data-stu-id="35cc2-129">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="35cc2-130">Název společnosti, úroveň podrobností, nastavení předběžných údajů a datum jsou vyplněny automaticky, ale přesto můžete provést aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="35cc2-130">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="35cc2-131">Zaškrtněte políčko **Zahrnout všechny měny vykazování**, pokud chcete vygenerovat více sestav zobrazujících tyto měny.</span><span class="sxs-lookup"><span data-stu-id="35cc2-131">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="35cc2-132">Více zobrazení pak bude k dispozici po kliknutí na tlačítko **Měna** ve Webovém prohlížeči při zobrazení sestavy.</span><span class="sxs-lookup"><span data-stu-id="35cc2-132">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="35cc2-133">V poli **Sestavy ve skupině** kliknutím na tlačítko **Přidat** vyberte sestavy, které chcete zahrnout do skupiny sestav.</span><span class="sxs-lookup"><span data-stu-id="35cc2-133">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="35cc2-134">Chcete-li vybrat více sestav v dialogovém okně **Přidat**, podržte klávesu Ctrl při výběru sestav.</span><span class="sxs-lookup"><span data-stu-id="35cc2-134">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="35cc2-135">Po dokončení výběru sestav klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="35cc2-135">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="35cc2-136">Kliknutím na položky **Soubor** &gt; **Uložit** uložte novou skupinu sestav.</span><span class="sxs-lookup"><span data-stu-id="35cc2-136">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="35cc2-137">Úprava skupiny sestav</span><span class="sxs-lookup"><span data-stu-id="35cc2-137">Modify a report group</span></span>

1.  <span data-ttu-id="35cc2-138">V Návrháři sestav v navigačním podokně klikněte na tlačítko **Skupiny sestav**.</span><span class="sxs-lookup"><span data-stu-id="35cc2-138">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="35cc2-139">Klikněte dvakrát na skupinu zásad, kterou chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="35cc2-139">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="35cc2-140">Klikněte na kartu **Skupina sestav** a proveďte požadované změny.</span><span class="sxs-lookup"><span data-stu-id="35cc2-140">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="35cc2-141">V nabídce **Soubor** klikněte na příkaz **Uložit** pro uložení změněné skupiny sestav. Případně klikněte na tlačítko **Uložit** ![Uložit](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Uložit") na panelu nástrojů.</span><span class="sxs-lookup"><span data-stu-id="35cc2-141">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="35cc2-142">**Poznámka:** Pokud jste naplánovali sestavy tak, aby byly generovány v určitých intervalech, můžete přepsat tato nastavení a vygenerovat sestavu okamžitě.</span><span class="sxs-lookup"><span data-stu-id="35cc2-142">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="35cc2-143">Vygenerování sestavy skupiny sestav</span><span class="sxs-lookup"><span data-stu-id="35cc2-143">Generate a report group report</span></span>

1.  <span data-ttu-id="35cc2-144">V Návrháři sestav v navigačním podokně klikněte na tlačítko **Skupiny sestav**.</span><span class="sxs-lookup"><span data-stu-id="35cc2-144">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="35cc2-145">Otevřete skupinu sestav k vygenerování.</span><span class="sxs-lookup"><span data-stu-id="35cc2-145">Open the report group to generate.</span></span>
3.  <span data-ttu-id="35cc2-146">Klikněte na tlačítko **Generovat sestavu** ![Generovat sestavu](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generovat sestavu") pro generování sestav.</span><span class="sxs-lookup"><span data-stu-id="35cc2-146">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="35cc2-147">Odstranění skupiny sestav</span><span class="sxs-lookup"><span data-stu-id="35cc2-147">Delete a report group</span></span>

1.  <span data-ttu-id="35cc2-148">V Návrháři sestav v navigačním podokně klikněte na tlačítko **Skupiny sestav**.</span><span class="sxs-lookup"><span data-stu-id="35cc2-148">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="35cc2-149">Klikněte pravým tlačítkem myši na skupinu sestav, kterou chcete odstranit, a vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="35cc2-149">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="35cc2-150">Když se zobrazí potvrzující zpráva, klepněte na tlačítko **Ano**.</span><span class="sxs-lookup"><span data-stu-id="35cc2-150">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="35cc2-151">Ovládací prvky karta Skupina sestav</span><span class="sxs-lookup"><span data-stu-id="35cc2-151">Report Group tab controls</span></span>
<span data-ttu-id="35cc2-152">Následující tabulka popisuje ovládací prvky na kartě **Skupina sestav**.</span><span class="sxs-lookup"><span data-stu-id="35cc2-152">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35cc2-153">Ovládací prvek</span><span class="sxs-lookup"><span data-stu-id="35cc2-153">Control</span></span></th>
<th><span data-ttu-id="35cc2-154">Popis</span><span class="sxs-lookup"><span data-stu-id="35cc2-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35cc2-155">Přepsat nastavení společnosti, podrobností a data z jednotlivých definic sestavy</span><span class="sxs-lookup"><span data-stu-id="35cc2-155">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="35cc2-156">Zaškrtnutím tohoto políčka můžete přepsat jednotlivé definice sestav v této skupině sestav pro generování pouze těchto sestav.</span><span class="sxs-lookup"><span data-stu-id="35cc2-156">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35cc2-157">Název společnosti</span><span class="sxs-lookup"><span data-stu-id="35cc2-157">Company name</span></span></td>
<td><span data-ttu-id="35cc2-158">Vyberte společnost, která má být použita pro sestavy.</span><span class="sxs-lookup"><span data-stu-id="35cc2-158">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35cc2-159">Úroveň podrobností</span><span class="sxs-lookup"><span data-stu-id="35cc2-159">Detail level</span></span></td>
<td><span data-ttu-id="35cc2-160">Vyberte úroveň detailu, které mají sestavy obsahovat.</span><span class="sxs-lookup"><span data-stu-id="35cc2-160">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="35cc2-161"><strong>Finanční</strong>− souhrnná sestava se základními údaji.</span><span class="sxs-lookup"><span data-stu-id="35cc2-161"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="35cc2-162">Nelze podrobně zobrazit účty a dimenze, s výjimkou účtů a dimenzí přidaných prostřednictvím stromu výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="35cc2-162">You can't drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="35cc2-163"><strong>Finanční &amp; účetní</strong> − sestava, která obsahuje souhrn na vysoké úrovni a podrobnosti účtu.</span><span class="sxs-lookup"><span data-stu-id="35cc2-163"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="35cc2-164"><strong>Finanční, účetní &amp; transakční</strong> − sestava, která obsahuje souhrn na vysoké úrovni a podrobnosti transakcí.</span><span class="sxs-lookup"><span data-stu-id="35cc2-164"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35cc2-165">Provizorní</span><span class="sxs-lookup"><span data-stu-id="35cc2-165">Provisional</span></span></td>
<td><span data-ttu-id="35cc2-166">Vyberte typy aktivit, které mají sestavy obsahovat.</span><span class="sxs-lookup"><span data-stu-id="35cc2-166">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="35cc2-167"><strong>Pouze zaúčtovaná aktivita</strong> – zahrnuje pouze transakce a zůstatky, které jsou zaúčtovány ve vašich finančních datech.</span><span class="sxs-lookup"><span data-stu-id="35cc2-167"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="35cc2-168"><strong>Zaúčtovaná a nezaúčtovaná aktivita</strong> – zahrnuje všechny transakce a zůstatky, které jsou zadány a zaúčtovány ve vašich finančních datech.</span><span class="sxs-lookup"><span data-stu-id="35cc2-168"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="35cc2-169"><strong>Pouze nezaúčtovaná aktivita</strong> – zahrnuje pouze transakce, které jsou zadány, ale nejsou ještě zaúčtovány ve vašich finančních datech.</span><span class="sxs-lookup"><span data-stu-id="35cc2-169"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35cc2-170">Zahrnout všechny měny vykazování</span><span class="sxs-lookup"><span data-stu-id="35cc2-170">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="35cc2-171">Pokud jsou ve vašem systému Microsoft Dynamics ERP definovány další měny vykazování, budou uvedeny zde.</span><span class="sxs-lookup"><span data-stu-id="35cc2-171">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="35cc2-172">Označením tohoto pole vygenerujete další sestavy ve vybraných měnách.</span><span class="sxs-lookup"><span data-stu-id="35cc2-172">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="35cc2-173">Chcete-li tyto sestavy zobrazit v nástroji Web Viewer, klikněte na tlačítko <strong>Měna</strong> a pak vyberte měnu.</span><span class="sxs-lookup"><span data-stu-id="35cc2-173">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35cc2-174">Informace o datu nejsou uloženy s definicí sestavy</span><span class="sxs-lookup"><span data-stu-id="35cc2-174">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="35cc2-175">Základní období</span><span class="sxs-lookup"><span data-stu-id="35cc2-175">Base period</span></span></li>
<li><span data-ttu-id="35cc2-176">Základní rok</span><span class="sxs-lookup"><span data-stu-id="35cc2-176">Base year</span></span></li>
<li><span data-ttu-id="35cc2-177">Pokryté období</span><span class="sxs-lookup"><span data-stu-id="35cc2-177">Period covered</span></span></li>
</ul>
<span data-ttu-id="35cc2-178">Pouze výchozí nastavení základního období se uloží s definicí sestavy.</span><span class="sxs-lookup"><span data-stu-id="35cc2-178">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35cc2-179">Informace o datu jsou uloženy s definicí sestavy</span><span class="sxs-lookup"><span data-stu-id="35cc2-179">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="35cc2-180">Datum sestavy</span><span class="sxs-lookup"><span data-stu-id="35cc2-180">Report date</span></span></li>
<li><span data-ttu-id="35cc2-181">Výchozí základní období</span><span class="sxs-lookup"><span data-stu-id="35cc2-181">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35cc2-182">Sestavy ve skupině</span><span class="sxs-lookup"><span data-stu-id="35cc2-182">Reports in group</span></span></td>
<td><span data-ttu-id="35cc2-183">Umožňuje přidat, odstranit a změnit pořadí sestav ve skupině sestav.</span><span class="sxs-lookup"><span data-stu-id="35cc2-183">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="35cc2-184">Pokud chcete do skupiny sestav přidat definice sestav, dvojím kliknutím na skupinu sestav ji otevřete a klikněte na tlačítko <strong>Přidat</strong>.</span><span class="sxs-lookup"><span data-stu-id="35cc2-184">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="35cc2-185">Vyberte sestavy, které chcete do této skupiny sestav zahrnout, a klikněte na tlačítko <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="35cc2-185">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="35cc2-186">Chcete-li ze skupiny sestav odebrat sestavu, vyberte ji a klikněte na tlačítko <strong>Odebrat</strong>.</span><span class="sxs-lookup"><span data-stu-id="35cc2-186">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="35cc2-187">Chcete-li změnit pořadí, ve kterém jsou generovány sestavy, vyberte v seznamu sestavu a klikněte na tlačítko <strong>Přesunout nahoru</strong> nebo <strong>Přesunout dolů</strong>.</span><span class="sxs-lookup"><span data-stu-id="35cc2-187">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="35cc2-188">Viz také</span><span class="sxs-lookup"><span data-stu-id="35cc2-188">See also</span></span>
--------

[<span data-ttu-id="35cc2-189">Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="35cc2-189">Financial reporting</span></span>](financial-reporting-intro.md)





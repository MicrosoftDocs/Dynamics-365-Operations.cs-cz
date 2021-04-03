---
title: Poradce při potížích souvisejících s upgrady aplikací Finance and Operations
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s upgrady aplikací Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: ae54ffc9f7a97793dfaddc29f5aae66e5b06c931
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561195"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="067b7-103">Poradce při potížích souvisejících s upgrady aplikací Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="067b7-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="067b7-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="067b7-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="067b7-105">Konkrétně obsahuje informace, které vám pomohou vyřešit problémy s upgrady aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="067b7-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="067b7-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="067b7-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="067b7-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="067b7-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="067b7-108">Chyby synchronizace databáze</span><span class="sxs-lookup"><span data-stu-id="067b7-108">Database synchronization errors</span></span>

<span data-ttu-id="067b7-109">**Požadovaná role pro opravu problému:** správce systému</span><span class="sxs-lookup"><span data-stu-id="067b7-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="067b7-110">Pokud se pokusíte pomocí tabulky **DualWriteProjectConfiguration** aktualizovat aplikaci Finance and Operations na Platform update 30, může se zobrazit chybová zpráva podobná následujícímu příkladu.</span><span class="sxs-lookup"><span data-stu-id="067b7-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="067b7-111">Chcete-li opravit problém, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="067b7-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="067b7-112">Přihlaste se k virtuálnímu počítači pro aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="067b7-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="067b7-113">Spusťte Visual Studio jako správce a otevřete strom aplikačních objektů (AOT).</span><span class="sxs-lookup"><span data-stu-id="067b7-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="067b7-114">Vyhledejte **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="067b7-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="067b7-115">Ve stromu aplikačních objektů klepněte pravým tlačítkem myši na položku **DualWriteProjectConfiguration** a vyberte **Přidat do nového projektu**.</span><span class="sxs-lookup"><span data-stu-id="067b7-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="067b7-116">Chcete-li li vytvořit nový projekt, který bude používat výchozí možnosti, klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="067b7-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="067b7-117">V Průzkumníku řešení klikněte pravým tlačítkem na **Vlastnosti projektu** a lnastavte **Synchronizovat databázi na sestavení** na **True**.</span><span class="sxs-lookup"><span data-stu-id="067b7-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="067b7-118">Sestavte projekt a potvrďte, že je sestavení úspěšné.</span><span class="sxs-lookup"><span data-stu-id="067b7-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="067b7-119">V nabídce **Dynamics 365** vyberte možnost **Synchronizovat databázi**.</span><span class="sxs-lookup"><span data-stu-id="067b7-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="067b7-120">Chcete-li provést úplnou synchronizaci databáze, vyberte možnost **Synchronizovat**.</span><span class="sxs-lookup"><span data-stu-id="067b7-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="067b7-121">Po úspěšné synchronizaci celé databáze spusťte znovu krok synchronizace databáze v Lifecycle Services (LCS) Microsoft Dynamics a podle potřeby použijte skripty ručního upgradu, abyste mohli pokračovat v aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="067b7-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="067b7-122">Problém s chybějícími sloupci tabulky na mapách</span><span class="sxs-lookup"><span data-stu-id="067b7-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="067b7-123">**Požadovaná role pro opravu problému:** správce systému</span><span class="sxs-lookup"><span data-stu-id="067b7-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="067b7-124">Na stránce **Dvojího zápisu** se může zobrazit chybová zpráva podobná následujícímu příkladu:</span><span class="sxs-lookup"><span data-stu-id="067b7-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="067b7-125">*Chybějící zdrojové pole \<field name\> ve schématu.*</span><span class="sxs-lookup"><span data-stu-id="067b7-125">*Missing source field \<field name\> in the schema.*</span></span>

![Příklad chybové zprávy chybějícího zdrojového sloupce](media/error_missing_field.png)

<span data-ttu-id="067b7-127">Chcete-li tento problém vyřešit, zkontrolujte nejprve, že v tabulce jsou sloupce.</span><span class="sxs-lookup"><span data-stu-id="067b7-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="067b7-128">Přihlaste se k modulu VM pro aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="067b7-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="067b7-129">Přejděte na **Pracovní prostory \> Správa dat**, vyberte dlaždici **Parametry architektury** a pak na kartě **Nastavení tabulky** vyberte **Aktualizovat seznam tabulek** pro aktualizaci tabulek.</span><span class="sxs-lookup"><span data-stu-id="067b7-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="067b7-130">Přejděte na **Pracovní prostory \> Správa dat**, vyberte kartu **Datové tabulky** a zkontrolujte, zda je daná tabulka uvedena v seznamu.</span><span class="sxs-lookup"><span data-stu-id="067b7-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="067b7-131">Není-li tabulka v seznamu uvedena, přihlaste se k virtuálnímu počítači pro aplikaci Finance and Operations a ujistěte se, že je daná tabulka dostupná.</span><span class="sxs-lookup"><span data-stu-id="067b7-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="067b7-132">Otevřete stránku **Mapování tabulek** ze stránky **Dvojí zapisování** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="067b7-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="067b7-133">Chcete-li vyplnit sloupce v mapování tabulky, vyberte možnost **Aktualizovat seznam tabulek** .</span><span class="sxs-lookup"><span data-stu-id="067b7-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="067b7-134">Pokud problém stále není opraven, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="067b7-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="067b7-135">Tento postup vás provede procesem odstranění tabulky a jejím opětovným přidáním.</span><span class="sxs-lookup"><span data-stu-id="067b7-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="067b7-136">Chcete-li předejít problémům, postupujte přesně podle kroků.</span><span class="sxs-lookup"><span data-stu-id="067b7-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="067b7-137">V aplikaci Finance and Operations přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Datové tabulky**.</span><span class="sxs-lookup"><span data-stu-id="067b7-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="067b7-138">Vyhledejte tabulku, u které chybí atribut.</span><span class="sxs-lookup"><span data-stu-id="067b7-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="067b7-139">V panelu nástrojů klikněte na možnost **Změnit mapování cíle**.</span><span class="sxs-lookup"><span data-stu-id="067b7-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="067b7-140">V podokně **Mapovat fázování na cíl** klikněte na možnost **Generovat mapování**.</span><span class="sxs-lookup"><span data-stu-id="067b7-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="067b7-141">Otevřete stránku **Mapování tabulek** ze stránky **Dvojí zapisování** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="067b7-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="067b7-142">Není-li atribut automaticky naplněn na mapě, přidejte jej ručně kliknutím na tlačítko **Přidat atribut** a následným kliknutím na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="067b7-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="067b7-143">Vyberte mapování a klikněte na tlačítko **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="067b7-143">Select the map and click **Run**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
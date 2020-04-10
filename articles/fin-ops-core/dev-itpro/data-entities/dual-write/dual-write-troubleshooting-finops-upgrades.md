---
title: Poradce při potížích souvisejících s upgrady aplikací Finance and Operations
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s upgrady aplikací Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172870"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="bb700-103">Poradce při potížích souvisejících s upgrady aplikací Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="bb700-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="bb700-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bb700-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="bb700-105">Konkrétně obsahuje informace, které vám pomohou vyřešit problémy s upgrady aplikací Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bb700-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb700-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="bb700-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="bb700-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="bb700-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="bb700-108">Chyby synchronizace databáze</span><span class="sxs-lookup"><span data-stu-id="bb700-108">Database synchronization errors</span></span>

<span data-ttu-id="bb700-109">**Požadovaná role pro opravu problému:** správce systému</span><span class="sxs-lookup"><span data-stu-id="bb700-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="bb700-110">Pokud se pokusíte pomocí entity **DualWriteProjectConfiguration** aktualizovat aplikaci Finance and Operations na Platform update 30, může se zobrazit chybová zpráva podobná následujícímu příkladu.</span><span class="sxs-lookup"><span data-stu-id="bb700-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="bb700-111">Chcete-li opravit problém, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="bb700-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="bb700-112">Přihlaste se k virtuálnímu počítači pro aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bb700-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="bb700-113">Spusťte Visual Studio jako správce a otevřete strom aplikačních objektů (AOT).</span><span class="sxs-lookup"><span data-stu-id="bb700-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="bb700-114">Vyhledejte **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="bb700-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="bb700-115">Ve stromu aplikačních objektů klepněte pravým tlačítkem myši na položku **DualWriteProjectConfiguration** a vyberte **Přidat do nového projektu**.</span><span class="sxs-lookup"><span data-stu-id="bb700-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="bb700-116">Chcete-li li vytvořit nový projekt, který bude používat výchozí možnosti, klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="bb700-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="bb700-117">V Průzkumníku řešení klikněte pravým tlačítkem na **Vlastnosti projektu** a lnastavte **Synchronizovat databázi na sestavení** na **True**.</span><span class="sxs-lookup"><span data-stu-id="bb700-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="bb700-118">Sestavte projekt a potvrďte, že je sestavení úspěšné.</span><span class="sxs-lookup"><span data-stu-id="bb700-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="bb700-119">V nabídce **Dynamics 365** vyberte možnost **Synchronizovat databázi**.</span><span class="sxs-lookup"><span data-stu-id="bb700-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="bb700-120">Chcete-li provést úplnou synchronizaci databáze, vyberte možnost **Synchronizovat**.</span><span class="sxs-lookup"><span data-stu-id="bb700-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="bb700-121">Po úspěšné synchronizaci celé databáze spusťte znovu krok synchronizace databáze v Lifecycle Services (LCS) Microsoft Dynamics a podle potřeby použijte skripty ručního upgradu, abyste mohli pokračovat v aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="bb700-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="bb700-122">Problém Chybějící pole entity u map</span><span class="sxs-lookup"><span data-stu-id="bb700-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="bb700-123">**Požadovaná role pro opravu problému:** správce systému</span><span class="sxs-lookup"><span data-stu-id="bb700-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="bb700-124">Na stránce **Dvojího zápisu** se může zobrazit chybová zpráva podobná následujícímu příkladu:</span><span class="sxs-lookup"><span data-stu-id="bb700-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="bb700-125">*Chybějící zdrojové pole \<název pole\> ve schématu.*</span><span class="sxs-lookup"><span data-stu-id="bb700-125">*Missing source field \<field name\> in the schema.*</span></span>

![Příklad chybové zprávy chybějícího zdrojového pole](media/error_missing_field.png)

<span data-ttu-id="bb700-127">Chcete-li tento problém vyřešit, zkontrolujte nejprve následující kroky a ujistěte se, že pole jsou v entitě.</span><span class="sxs-lookup"><span data-stu-id="bb700-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="bb700-128">Přihlaste se k modulu VM pro aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bb700-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="bb700-129">Přejděte na **Pracovní prostory \> Správa dat**, vyberte dlaždici **Parametry architektury** a pak na kartě **Nastavení entity** vyberte **Aktualizovat seznam entit** pro aktualizaci entit.</span><span class="sxs-lookup"><span data-stu-id="bb700-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="bb700-130">Přejděte na **Pracovní prostory \> Správa dat**, vyberte kartu **Datové entity** a zkontrolujte, zda je daná entita uvedena v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bb700-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="bb700-131">Není-li entita v seznamu uvedena, přihlaste se k virtuálnímu počítači pro aplikaci Finance and Operations a ujistěte se, že je daná entita dostupná.</span><span class="sxs-lookup"><span data-stu-id="bb700-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="bb700-132">Otevřete stránku **Mapování entit** ze stránky **Dvojí zapisování** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bb700-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="bb700-133">Chcete-li vyplnit pole v mapování entit, vyberte možnost **Aktualizovat seznam entit** .</span><span class="sxs-lookup"><span data-stu-id="bb700-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="bb700-134">Pokud problém stále není opraven, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="bb700-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb700-135">Tento postup vás provede procesem odstranění entity a jejím opětovným přidáním.</span><span class="sxs-lookup"><span data-stu-id="bb700-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="bb700-136">Chcete-li předejít problémům, postupujte přesně podle kroků.</span><span class="sxs-lookup"><span data-stu-id="bb700-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="bb700-137">V aplikaci Finance and Operations přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Datové entity**.</span><span class="sxs-lookup"><span data-stu-id="bb700-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="bb700-138">Vyhledejte entitu, u které chybí pole.</span><span class="sxs-lookup"><span data-stu-id="bb700-138">Find the entity that is missing the field.</span></span> <span data-ttu-id="bb700-139">Vytvořte si poznámku o cílové entitě, pracovní tabulce, názvu entity a dalších hodnotách sloupců.</span><span class="sxs-lookup"><span data-stu-id="bb700-139">Make a note of the target entity, staging table, entity name, and other column values.</span></span>
3. <span data-ttu-id="bb700-140">Pokud některá ze skupin zpracování závisí na této entitě, proveďte před odstraněním entity odpovídající akci pro skupiny zpracování.</span><span class="sxs-lookup"><span data-stu-id="bb700-140">If any of your processing groups depend on this entity, take appropriate action for the processing groups before you delete the entity.</span></span>
4. <span data-ttu-id="bb700-141">Odstraňte entitu, u které chybí pole.</span><span class="sxs-lookup"><span data-stu-id="bb700-141">Delete the entity that is missing the field.</span></span>
5. <span data-ttu-id="bb700-142">Vyberte **Nový** a entitu přidejte zpět.</span><span class="sxs-lookup"><span data-stu-id="bb700-142">Select **New**, and add the entity back.</span></span> <span data-ttu-id="bb700-143">Zadejte hodnoty, které jste si poznamenejte v kroku 2.</span><span class="sxs-lookup"><span data-stu-id="bb700-143">Specify the values that you made a note of in step 2.</span></span>
6. <span data-ttu-id="bb700-144">Otevřete stránku **Mapování entit** ze stránky **Dvojí zapisování** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bb700-144">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
7. <span data-ttu-id="bb700-145">Chcete-li vyplnit pole v mapování entit, vyberte možnost **Aktualizovat seznam entit** .</span><span class="sxs-lookup"><span data-stu-id="bb700-145">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

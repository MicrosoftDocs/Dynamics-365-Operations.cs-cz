---
title: Poradce při potížích se synchronizací v ostrém provozu
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy se synchronizací v ostrém provozu.
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
ms.openlocfilehash: 60839bbd1b3ae642cdd419c7df2388292776a461
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172730"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="20599-103">Poradce při potížích se synchronizací v ostrém provozu</span><span class="sxs-lookup"><span data-stu-id="20599-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="20599-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="20599-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="20599-105">Toto téma obsahuje informace, které vám pomohou vyřešit problémy se synchronizací v ostrém provozu.</span><span class="sxs-lookup"><span data-stu-id="20599-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20599-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="20599-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="20599-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="20599-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="20599-108">Synchronizace v ostrém provozu vyvolá chybu 403 Forbidden při vytváření záznamu v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20599-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="20599-109">Může se zobrazit následující chybová zpráva při vytváření záznamu v aplikaci Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="20599-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="20599-110">*\[{\\"chyba\\":{\\"kód\\":\\"0x80072560\\",\\"zpráva\\":\\"Uživatel není členem organizace.\\"}}\], Vzdálený server vrátil chybu: (403) zakázáno."}}".*</span><span class="sxs-lookup"><span data-stu-id="20599-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="20599-111">Chcete-li tento problém vyřešit, postupujte podle kroků v [Požadavcích na systém a jeho předpoklady](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="20599-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="20599-112">K provedení těchto kroků musí mít uživatelé aplikace se dvojím zápisem, kteří jsou vytvořeni v aplikaci Common Data Service, roli správce systému.</span><span class="sxs-lookup"><span data-stu-id="20599-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="20599-113">Výchozí vlastnící tým musí mít také roli správce systému.</span><span class="sxs-lookup"><span data-stu-id="20599-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="20599-114">Synchronizace v ostrém provozu pro libovolnou entitu neustále vyvolává podobnou chybu při vytváření záznamu v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20599-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="20599-115">**Požadovaná role pro opravu problému:** správce systému</span><span class="sxs-lookup"><span data-stu-id="20599-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="20599-116">Při každém pokusu o uložení dat entity do aplikace Finance and Operations se může zobrazit chybová zpráva podobná následující:</span><span class="sxs-lookup"><span data-stu-id="20599-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="20599-117">*Nelze uložit změny do databáze. Jednotka práce nemůže potvrdit transakci. Nelze zapsat data do entity uoms. Zápisy do UnitOfMeasureEntity se nezdařily. Chybová zpráva Nelze synchronizovat s entitou uoms.*</span><span class="sxs-lookup"><span data-stu-id="20599-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="20599-118">Chcete-li tento problém vyřešit, je nutné zajistit, aby v aplikaci Finance and Operations i Common Data Service existovala potřebná referenční data.</span><span class="sxs-lookup"><span data-stu-id="20599-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="20599-119">Pokud například zákazník, který je součástí aplikace Finance and Operations, patří do určité skupiny odběratelů, ujistěte se, že v Common Data Service existuje daná skupina odběratelů.</span><span class="sxs-lookup"><span data-stu-id="20599-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="20599-120">Pokud existují data na obou stranách a potvrdili jste, že problém není související s daty, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="20599-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="20599-121">Zastavte související entitu.</span><span class="sxs-lookup"><span data-stu-id="20599-121">Stop the related entity.</span></span>
2. <span data-ttu-id="20599-122">Přihlaste se k aplikaci Finance and Operations a ujistěte se, že v tabulkách DualWriteProjectConfiguration a DualWriteProjectFieldConfiguration existují záznamy pro nefunkční entitu.</span><span class="sxs-lookup"><span data-stu-id="20599-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="20599-123">Takto například dotaz vypadá, pokud entita **Zákazníci** selhává.</span><span class="sxs-lookup"><span data-stu-id="20599-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="20599-124">Pokud existují záznamy pro neúspěšnou entitu i po zastavení mapování entit, odstraňte záznamy, které souvisejí s chybnou entitou.</span><span class="sxs-lookup"><span data-stu-id="20599-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="20599-125">Poznamenejte si sloupec **ProjectName** v tabulce DualWriteProjectConfiguration a načtěte záznam v tabulce DualWriteProjectFieldConfiguration použitím názvu projektu k odstranění záznamu.</span><span class="sxs-lookup"><span data-stu-id="20599-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="20599-126">Spusťte mapování entit.</span><span class="sxs-lookup"><span data-stu-id="20599-126">Start the entity mapping.</span></span> <span data-ttu-id="20599-127">Ověřte, zda se data synchronizují bez problémů.</span><span class="sxs-lookup"><span data-stu-id="20599-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="20599-128">Zpracování chyb oprávnění ke čtení nebo zapisování při vytváření dat v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="20599-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="20599-129">Při vytváření dat v aplikaci Finance and Operations se může zobrazit chybová zpráva "špatný požadavek", která se podobá následujícímu příkladu.</span><span class="sxs-lookup"><span data-stu-id="20599-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Příklad chybové zprávy o chybném požadavku](media/error_record_id_source.png)

<span data-ttu-id="20599-131">Chcete-li tento problém vyřešit, je nutné přiřadit správné roli zabezpečení týmu mapované obchodní jednotky Dynamics 365 Sales nebo Dynamics 365 Customer Service, aby bylo možné chybějící oprávnění povolit.</span><span class="sxs-lookup"><span data-stu-id="20599-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="20599-132">V aplikaci Finance and Operations vyhledejte organizační jednotku, která je mapována v sadě Data Integration Connection.</span><span class="sxs-lookup"><span data-stu-id="20599-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Mapování organizace](media/mapped_business_unit.png)

2. <span data-ttu-id="20599-134">Přihlaste se k prostředí v aplikaci řízené podle modelů v Dynamics 365, přejděte k **Nastavení \> Zabezpečení** a najděte tým mapované organizační jednotky.</span><span class="sxs-lookup"><span data-stu-id="20599-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Tým mapované organizační jednotky](media/setting_security_page.png)

3. <span data-ttu-id="20599-136">Otevřete stránku pro tým pro úpravy a poté výběrem možnosti **Spravovat role** otevřete dialogové okno **Spravovat role týmu**.</span><span class="sxs-lookup"><span data-stu-id="20599-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Tlačítko Spravovat role](media/manage_team_roles.png)

4. <span data-ttu-id="20599-138">Přiřaďte roli, která má oprávnění pro čtení a zápis pro příslušné entity, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="20599-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="20599-139">Oprava synchronizačních potíží v prostředí, které má nedávno změněné prostředí Common Data Service</span><span class="sxs-lookup"><span data-stu-id="20599-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="20599-140">**Požadovaná role pro opravu problému:** správce systému</span><span class="sxs-lookup"><span data-stu-id="20599-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="20599-141">Může se zobrazit následující chybová zpráva při vytváření dat v aplikaci Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="20599-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="20599-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Nelze generovat datovou část pro entitu CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Vytvoření zatížení se nezdařilo s chybou Neplatný identifikátor URI: Identifikátor URI je prázdný."}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="20599-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="20599-143">V tomto poli vypadá chyba v aplikaci řízené modelem v produktu Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="20599-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="20599-144">*V kódu ISV došlo k neočekávané chybě. (ErrorType = ClientError) Neočekávaná výjimka z modulu plug-in (Execute): Microsoft.Dynamics.Integrator.CrmPlugins.Plugin: System.Exception: Nepodařilo se zpracovat účet entity. (pokus o připojení se nezdařil, protože připojená strana nereagovala správně po určitém časovém období, nebo navázané připojení se nezdařilo, protože připojený hostitel neodpověděl*</span><span class="sxs-lookup"><span data-stu-id="20599-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.CrmPlugins.Plugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="20599-145">K této chybě dojde, pokud je prostředí Common Data Service nesprávně resetováno v okamžiku, kdy se pokusíte vytvořit data v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="20599-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="20599-146">Chcete-li opravit problém, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="20599-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="20599-147">Přihlaste se k virtuálnímu počítači (VM) Finance and Operations, otevřete SQL Server Management Studio (SSMS) a hledejte záznamy v tabulce DUALWRITEPROJECTCONFIGURATIONENTITY, kde **internalentityname** rovná se **Zákazníci V3** a **externalentityname** rovná se **účty**.</span><span class="sxs-lookup"><span data-stu-id="20599-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="20599-148">V tomto poli je uveden vzhled dotazu.</span><span class="sxs-lookup"><span data-stu-id="20599-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="20599-149">Chcete-li spustit následující dotaz, použijte název projektu z výsledků předchozího dotazu.</span><span class="sxs-lookup"><span data-stu-id="20599-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="20599-150">Zkontrolujte, zda má sloupec **externalenvironmentURL** správnou Common Data Service adresu URL aplikace.</span><span class="sxs-lookup"><span data-stu-id="20599-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="20599-151">Odstraňte všechny duplicitní záznamy, které ukazují na nesprávnou adresu URL Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="20599-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="20599-152">Odstraňte odpovídající záznamy z tabulek DUALWRITEPROJECTFIELDCONFIGURATION a DUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="20599-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="20599-153">Zastavte mapování entit a restartujte jej</span><span class="sxs-lookup"><span data-stu-id="20599-153">Stop the entity mapping, and then restart it</span></span>

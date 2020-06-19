---
title: Poradce při potížích s počáteční synchronizací
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy, které by se mohly vyskytnou během počáteční synchronizace.
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
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410074"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="86054-103">Poradce při potížích s počáteční synchronizací</span><span class="sxs-lookup"><span data-stu-id="86054-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86054-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="86054-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="86054-105">Konkrétně obsahuje informace, které vám pomohou vyřešit problémy, které by se mohly vyskytnou během počáteční synchronizace.</span><span class="sxs-lookup"><span data-stu-id="86054-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86054-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="86054-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="86054-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="86054-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="86054-108">Zkontrolovat chyby počáteční synchronizace v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="86054-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="86054-109">Po povolení šablon mapování by měl být **Spuštěn** stav mapování.</span><span class="sxs-lookup"><span data-stu-id="86054-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="86054-110">Pokud je stav **Nespuštěn**, došlo k chybám při počáteční synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="86054-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="86054-111">Chcete-li zobrazit chyby, vyberte kartu **Podrobnosti o počáteční synchronizaci** na stránce **Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="86054-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Karta počáteční podrobnosti synchronizace](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="86054-113">Počáteční synchronizaci nelze dokončit: 400 Chybný požadavek</span><span class="sxs-lookup"><span data-stu-id="86054-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="86054-114">**Požadovaná role pro opravu problému:** správce systému</span><span class="sxs-lookup"><span data-stu-id="86054-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="86054-115">Při pokusu o spuštění mapování a počáteční synchronizace se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="86054-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="86054-116">*Vzdálený server vrátil chybu: (400) nesprávný požadavek.), při exportu AX byla zjištěna chyba*</span><span class="sxs-lookup"><span data-stu-id="86054-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="86054-117">Následuje příklad úplné chybové zprávy.</span><span class="sxs-lookup"><span data-stu-id="86054-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="86054-118">Pokud k této chybě dojde konzistentně a nelze dokončit počáteční synchronizaci, opravte problém pomocí následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="86054-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="86054-119">Přihlaste se k virtuálnímu počítači pro aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="86054-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="86054-120">Otevřete konzoli MMC.</span><span class="sxs-lookup"><span data-stu-id="86054-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="86054-121">V podokně **Služby** zkontrolujte, zda je spuštěna služba platformy importu a exportu dat Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="86054-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="86054-122">Restartujte ji, pokud byla zastavena, protože ji vyžaduje počáteční synchronizace.</span><span class="sxs-lookup"><span data-stu-id="86054-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="86054-123">Chyba počáteční synchronizace: 403 zakázáno</span><span class="sxs-lookup"><span data-stu-id="86054-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="86054-124">Při počáteční synchronizaci se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="86054-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="86054-125">*(\[zakázáno\], Vzdálený server vrátil chybu: (403) Zakázáno.), při exportu AX byla zjištěna chyba*</span><span class="sxs-lookup"><span data-stu-id="86054-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="86054-126">Chcete-li opravit problém, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="86054-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="86054-127">Přihlášení do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="86054-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="86054-128">Na stránce **aplikací Azure Active Directory** odstraňte klienta **DtAppID** a poté jej znovu přidejte.</span><span class="sxs-lookup"><span data-stu-id="86054-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Seznam aplikací Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="86054-130">Selhání odkazů na sebe sama a cirkulárních odkazů při počáteční synchronizaci</span><span class="sxs-lookup"><span data-stu-id="86054-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="86054-131">Můžou se zobrazit chybové zprávy podobné následujícímu příkladu v případě, že některá z vašich mapování mají odkazy na sebe sama a cirkulární odkazy.</span><span class="sxs-lookup"><span data-stu-id="86054-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="86054-132">Chyby spadají do těchto kategorií:</span><span class="sxs-lookup"><span data-stu-id="86054-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="86054-133">Dodavatelé V2 do mapování entity msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="86054-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="86054-134">Mapování entit zákazníků V3 na účty</span><span class="sxs-lookup"><span data-stu-id="86054-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="86054-135">Vyřešte chybu v Vendors V2 na mapování entit msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="86054-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="86054-136">Mohli byste narazit na následující počáteční chyby synchronizace na mapování **Vendors V2** na **msdyn_vendors**, pokud entity mají existující záznamy s hodnotami v polích **PrimaryContactPersonId** a **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="86054-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="86054-137">To proto, že **InvoiceVendorAccountNumber** je pole s vlastním odkazem a **PrimaryContactPersonId** je kruhový odkaz v mapování dodavatele.</span><span class="sxs-lookup"><span data-stu-id="86054-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="86054-138">*Nelze vyřešit identifikátor GUID pro pole: <field>. Vyhledávání nebylo nalezeno: <value>. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="86054-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="86054-139">Zde je několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="86054-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="86054-140">*Nelze vyřešit GUID pro pole: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Vyhledávání nebylo nalezeno: 000056. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?2$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="86054-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="86054-141">*Nelze vyřešit GUID pro pole: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Vyhledávání nebylo nalezeno: V24-1. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="86054-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="86054-142">Pokud máte záznamy s hodnotami v těchto polích v entitě dodavatele, postupujte podle kroků v části níže a dokončete počáteční synchronizaci úspěšně.</span><span class="sxs-lookup"><span data-stu-id="86054-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="86054-143">V aplikaci Finance and Operations odstraňte pole **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** z mapování a změny uložte.</span><span class="sxs-lookup"><span data-stu-id="86054-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="86054-144">Přejděte na stránku mapování s dvojitým zápisem **Vendors V2 (msdyn_vendors)** a vyberte kartu **Mapování entit**. V levém filtru vyberte **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="86054-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="86054-145">V pravém filtru vyberte **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="86054-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="86054-146">Vyhledejte **primarycontactperson** a najděte zdrojové pole **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="86054-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="86054-147">Klikněte na tlačítko **Akce** a vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="86054-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![vlastní nebo kruhový odkaz 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="86054-149">Opakujte pro odstranění pole **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="86054-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![vlastní nebo kruhový odkaz 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="86054-151">Uložte změny mapování.</span><span class="sxs-lookup"><span data-stu-id="86054-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="86054-152">Zakažte sledování změn pro entitu **Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="86054-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="86054-153">Přejděte na **Správa dat \> Datové entity**.</span><span class="sxs-lookup"><span data-stu-id="86054-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="86054-154">Vyberte entitu **Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="86054-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="86054-155">Klikněte na **Možnosti** z panelu nabídek a poté **Sledování změn**.</span><span class="sxs-lookup"><span data-stu-id="86054-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![vlastní nebo kruhový odkaz 5](media/selfref_options.png)
    
    4. <span data-ttu-id="86054-157">Klikněte na **Zakázat sledování změn**.</span><span class="sxs-lookup"><span data-stu-id="86054-157">Click **Disable Change Tracking**.</span></span>
    
        ![vlastní nebo kruhový odkaz 6](media/selfref_tracking.png)

3. <span data-ttu-id="86054-159">Spusťte počáteční synchronizaci mapování **Vendors V2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="86054-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="86054-160">Počáteční synchronizace by měla úspěšně proběhnout bez chyb.</span><span class="sxs-lookup"><span data-stu-id="86054-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="86054-161">Spusťte počáteční synchronizaci pro mapování **CDS Contacts V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="86054-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="86054-162">Toto mapování musíte synchronizovat, pokud chcete synchronizovat pole primárního kontaktu na entitě dodavatelů, protože záznamy kontaktů je také třeba nejprve synchronizovat.</span><span class="sxs-lookup"><span data-stu-id="86054-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="86054-163">Přidejte pole **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** zpět do mapování **Vendors V2 (msdyn_vendors)** a uložte mapování.</span><span class="sxs-lookup"><span data-stu-id="86054-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="86054-164">Spusťte počáteční znovu pro mapování **Vendors V2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="86054-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="86054-165">Všechny záznamy budou synchronizovány, protože sledování změn je zakázáno.</span><span class="sxs-lookup"><span data-stu-id="86054-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="86054-166">Povolte sledování změn pro entitu **Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="86054-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="86054-167">Vyřešte chybu v mapování entit Customers V3 to Accounts</span><span class="sxs-lookup"><span data-stu-id="86054-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="86054-168">Mohli byste narazit na následující počáteční chyby synchronizace na mapování **VCustomers V3** na **Accounts**, pokud entity mají existující záznamy s hodnotami v polích **ContactPersonID** a **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="86054-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="86054-169">To proto, že **InvoiceAccount** je pole s vlastním odkazem a **ContactPersonID** je kruhový odkaz v mapování dodavatele.</span><span class="sxs-lookup"><span data-stu-id="86054-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="86054-170">*Nelze vyřešit identifikátor GUID pro pole: <field>. Vyhledávání nebylo nalezeno: <value>. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="86054-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="86054-171">*Nelze vyřešit GUID pro pole: primarycontactid.msdyn_contactpersonid. Vyhledávání nebylo nalezeno: 000056. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?2$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="86054-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="86054-172">*Nelze vyřešit GUID pro pole: msdyn_billingaccount.accountnumber. Vyhledávání nebylo nalezeno: 1206-1. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="86054-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="86054-173">Pokud máte záznamy s hodnotami v těchto polích v entitě zákazníka, postupujte podle kroků v části níže a dokončete počáteční synchronizaci úspěšně.</span><span class="sxs-lookup"><span data-stu-id="86054-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="86054-174">Tento přístup můžete použít pro jakékoli dodávané entity, jako jsou účty a kontakty.</span><span class="sxs-lookup"><span data-stu-id="86054-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="86054-175">V aplikaci Finance and Operations odstraňte pole **ContactPersonID** a **InvoiceAccount** z mapování **Customers V3 (accounts)** a mapování uložte.</span><span class="sxs-lookup"><span data-stu-id="86054-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="86054-176">Přejděte na stránku mapování s dvojitým zápisem pro **Customers V3 (accounts)** a vyberte kartu **Mapování entit**. V levém filtru vyberte **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="86054-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="86054-177">V pravém filtru vyberte **Common Data Service.Account**.</span><span class="sxs-lookup"><span data-stu-id="86054-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="86054-178">Vyhledejte **contactperson** a najděte zdrojové pole **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="86054-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="86054-179">Klikněte na tlačítko **Akce** a vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="86054-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![vlastní nebo kruhový odkaz 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="86054-181">Opakujte pro odstranění pole **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="86054-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![vlastní nebo kruhový odkaz](media/cust_selfref4.png)
    
    5. <span data-ttu-id="86054-183">Uložte změny mapování.</span><span class="sxs-lookup"><span data-stu-id="86054-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="86054-184">Zakažte sledování změn pro entitu **Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="86054-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="86054-185">Přejděte na **Správa dat \> Datové entity**.</span><span class="sxs-lookup"><span data-stu-id="86054-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="86054-186">Vyberte entitu **Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="86054-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="86054-187">Klikněte na **Možnosti** z panelu nabídek a poté **Sledování změn**.</span><span class="sxs-lookup"><span data-stu-id="86054-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![vlastní nebo kruhový odkaz 5](media/selfref_options.png)
    
    4. <span data-ttu-id="86054-189">Klikněte na **Zakázat sledování změn**.</span><span class="sxs-lookup"><span data-stu-id="86054-189">Click **Disable Change Tracking**.</span></span>
    
        ![vlastní nebo kruhový odkaz 6](media/selfref_tracking.png)

3. <span data-ttu-id="86054-191">Spusťte počáteční synchronizaci pro mapování **Customers V3 (Accounts)**.</span><span class="sxs-lookup"><span data-stu-id="86054-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="86054-192">Počáteční synchronizace by měla úspěšně proběhnout bez chyb.</span><span class="sxs-lookup"><span data-stu-id="86054-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="86054-193">Spusťte počáteční synchronizaci pro mapování **CDS Contacts V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="86054-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="86054-194">K dispozici jsou 2 mapy se stejným názvem.</span><span class="sxs-lookup"><span data-stu-id="86054-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="86054-195">Vyberte tu s popisem **Šablona s dvojím zápisem pro synchronizaci mezi kontakty dodavatele FO.CDS V2 a CDS.Contacts. Vyžaduje nový balíček \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="86054-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="86054-196">na kartě mapy **Podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="86054-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="86054-197">Přidejte **InvoiceAccount** a **ContactPersonId** zpět do mapování **Customers V3 (Accounts)** a mapování uložte.</span><span class="sxs-lookup"><span data-stu-id="86054-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="86054-198">Nyní pole **InvoiceAccount** i **ContactPersonId** jsou opět součástí živého synchronizačního režimu.</span><span class="sxs-lookup"><span data-stu-id="86054-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="86054-199">V dalším kroku dokončíte počáteční synchronizaci těchto polí.</span><span class="sxs-lookup"><span data-stu-id="86054-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="86054-200">Spusťte opět počáteční synchronizaci pro mapování **Customers V3 (Accounts)**.</span><span class="sxs-lookup"><span data-stu-id="86054-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="86054-201">Protože sledování změn je zakázáno, spuštěním synchronizace budou synchronizována data pro **InvoiceAccount** a **ContactPersonId** z aplikace Finance and Operations do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="86054-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="86054-202">Chcete-li synchronizovat data pro **InvoiceAccount** a **ContactPersonId** z Common Data Service do Finance and Operations, používáte projekt integrace dat.</span><span class="sxs-lookup"><span data-stu-id="86054-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="86054-203">V Power Apps vytvořit projekt integrace dat mezi entitami **Sales.Account** a **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="86054-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="86054-204">Směr dat musí být z Common Data Service do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="86054-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="86054-205">Protože **InvoiceAccount** je nový atribut v dvojitém zápisu, možná budete chtít přeskočit počáteční synchronizaci pro tento atribut.</span><span class="sxs-lookup"><span data-stu-id="86054-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="86054-206">Další informace naleznete v tématu [Integrace dat do Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="86054-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="86054-207">Následující obrázek ukazuje projekt, který aktualizuje **CustomerAccount** a **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="86054-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![vlastní nebo kruhový odkaz](media/cust_selfref6.png)

    2. <span data-ttu-id="86054-209">Přidejte do filtru kritéria společnosti na straně Common Data Service, protože v aplikaci Finance and Operations budou aktualizovány pouze záznamy, které odpovídají kritériím filtru.</span><span class="sxs-lookup"><span data-stu-id="86054-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="86054-210">Chcete-li přidat filtr, klikněte na ikonu filtru.</span><span class="sxs-lookup"><span data-stu-id="86054-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="86054-211">V dialogovém okně **Upravit dotaz** můžete přidat dotaz filtru jako **_msdyn_company_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="86054-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="86054-212">Pokud ikona filtru není k dispozici, vytvořte podpůrný ticket a požádejte tým pro integraci dat o povolení filtrování u klienta.</span><span class="sxs-lookup"><span data-stu-id="86054-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="86054-213">Pokud nezadáte dotaz filtru pro **_msdyn_company_value**, jsou všechny záznamy synchronizovány.</span><span class="sxs-lookup"><span data-stu-id="86054-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![vlastní nebo kruhový odkaz](media/cust_selfref7.png)

        <span data-ttu-id="86054-215">Tím je dokončena počáteční synchronizace záznamů.</span><span class="sxs-lookup"><span data-stu-id="86054-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="86054-216">Povolte sledování změn pro entitu **Customers V3** v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="86054-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>


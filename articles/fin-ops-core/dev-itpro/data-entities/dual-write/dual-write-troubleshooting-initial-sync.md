---
title: Poradce při potížích s počáteční synchronizací
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy, které by se mohly vyskytnou během počáteční synchronizace.
author: RamaKrishnamoorthy
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
ms.openlocfilehash: c716707140c85b06ad2f084c10c4b2d0ecfea82e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754007"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="4bf38-103">Poradce při potížích s počáteční synchronizací</span><span class="sxs-lookup"><span data-stu-id="4bf38-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4bf38-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4bf38-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="4bf38-105">Konkrétně obsahuje informace, které vám pomohou vyřešit problémy, které by se mohly vyskytnou během počáteční synchronizace.</span><span class="sxs-lookup"><span data-stu-id="4bf38-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4bf38-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="4bf38-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="4bf38-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="4bf38-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="4bf38-108">Zkontrolovat chyby počáteční synchronizace v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4bf38-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="4bf38-109">Po povolení šablon mapování by měl být **Spuštěn** stav mapování.</span><span class="sxs-lookup"><span data-stu-id="4bf38-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="4bf38-110">Pokud je stav **Nespuštěn**, došlo k chybám při počáteční synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="4bf38-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="4bf38-111">Chcete-li zobrazit chyby, vyberte kartu **Podrobnosti o počáteční synchronizaci** na stránce **Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Chyba na kartě Počáteční podrobnosti synchronizace](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="4bf38-113">Počáteční synchronizaci nelze dokončit: 400 Chybný požadavek</span><span class="sxs-lookup"><span data-stu-id="4bf38-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="4bf38-114">**Požadovaná role pro opravu problému:** správce systému</span><span class="sxs-lookup"><span data-stu-id="4bf38-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="4bf38-115">Při pokusu o spuštění mapování a počáteční synchronizace se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="4bf38-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="4bf38-116">*(\[Chybný požadavek\] Vzdálený server vrátil chybu: (400) chybný požadavek.), při exportu AX byla zjištěna chyba*</span><span class="sxs-lookup"><span data-stu-id="4bf38-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="4bf38-117">Následuje příklad úplné chybové zprávy.</span><span class="sxs-lookup"><span data-stu-id="4bf38-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="4bf38-118">Pokud k této chybě dojde konzistentně a nelze dokončit počáteční synchronizaci, opravte problém pomocí následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="4bf38-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="4bf38-119">Přihlaste se k virtuálnímu počítači pro aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4bf38-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="4bf38-120">Otevřete konzoli MMC.</span><span class="sxs-lookup"><span data-stu-id="4bf38-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="4bf38-121">V podokně **Služby** zkontrolujte, zda je spuštěna služba platformy importu a exportu dat Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4bf38-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="4bf38-122">Restartujte ji, pokud byla zastavena, protože ji vyžaduje počáteční synchronizace.</span><span class="sxs-lookup"><span data-stu-id="4bf38-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="4bf38-123">Chyba počáteční synchronizace: 403 zakázáno</span><span class="sxs-lookup"><span data-stu-id="4bf38-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="4bf38-124">Při počáteční synchronizaci se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="4bf38-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="4bf38-125">*(\[zakázáno\], Vzdálený server vrátil chybu: (403) Zakázáno.), při exportu AX byla zjištěna chyba*</span><span class="sxs-lookup"><span data-stu-id="4bf38-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="4bf38-126">Chcete-li opravit problém, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="4bf38-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="4bf38-127">Přihlášení do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4bf38-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="4bf38-128">Na stránce **aplikací Azure Active Directory** odstraňte klienta **DtAppID** a poté jej znovu přidejte.</span><span class="sxs-lookup"><span data-stu-id="4bf38-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID klient v seznamu aplikací Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="4bf38-130">Selhání odkazů na sebe sama a cirkulárních odkazů při počáteční synchronizaci</span><span class="sxs-lookup"><span data-stu-id="4bf38-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="4bf38-131">Můžou se zobrazit chybové zprávy podobné následujícímu příkladu v případě, že některá z vašich mapování mají odkazy na sebe sama a cirkulární odkazy.</span><span class="sxs-lookup"><span data-stu-id="4bf38-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="4bf38-132">Chyby spadají do těchto kategorií:</span><span class="sxs-lookup"><span data-stu-id="4bf38-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="4bf38-133">Chyby v mapování tabulek Vendors V2–to–msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="4bf38-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="4bf38-134">Chyby v mapování tabulek Customers V3–to–Accounts</span><span class="sxs-lookup"><span data-stu-id="4bf38-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="4bf38-135">Řešení chyb v mapování tabulek Vendors V2–to–msdyn_vendors</span><span class="sxs-lookup"><span data-stu-id="4bf38-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="4bf38-136">Mohli byste narazit na následující počáteční chyby synchronizace na mapování **Vendors V2** na **msdyn\_vendors**, pokud tabulky mají existující řádky s hodnotami ve sloupcích **PrimaryContactPersonId** a **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns.</span></span> <span data-ttu-id="4bf38-137">Tyto chyby se vyskytují proto, že **InvoiceVendorAccountNumber** je sloupec s vlastním odkazem a **PrimaryContactPersonId** je kruhový odkaz v mapování dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4bf38-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing column, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="4bf38-138">Chybové zprávy, které obdržíte, budou mít následující formulář.</span><span class="sxs-lookup"><span data-stu-id="4bf38-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="4bf38-139">*Nelze vyřešit identifikátor GUID pro pole: \<field\>. Vyhledávání nebylo nalezeno: \<value\>. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="4bf38-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="4bf38-140">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="4bf38-140">Here are some examples:</span></span>

- <span data-ttu-id="4bf38-141">*Nelze vyřešit identifikátor GUID pro pole: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Vyhledávání nebylo nalezeno: 000056. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="4bf38-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="4bf38-142">*Nelze vyřešit identifikátor GUID pro pole: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Vyhledávání nebylo nalezeno: V24-1. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="4bf38-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="4bf38-143">Pokud mají libovolné řádky v tabulce dodavatele hodnoty ve sloupcích **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** , postupujte podle kroků v části níže a dokončete počáteční synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="4bf38-143">If any rows in the vendor table have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="4bf38-144">V aplikaci Finance and Operations odstraňte sloupce **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** z mapování a pak mapování uložte.</span><span class="sxs-lookup"><span data-stu-id="4bf38-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="4bf38-145">Na stránce mapování s dvojitým zápisem **Vendors V2 (msdyn\_vendors)**, na kartě **Mapování tabulek**, v levém filtru vyberte **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="4bf38-146">V pravém filtru vyberte **Sales.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="4bf38-147">Vyhledejte **primarycontactperson** a najděte zdrojový sloupec **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source column.</span></span>
    3. <span data-ttu-id="4bf38-148">Vyberte **Akce** a poté vyberte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-148">Select **Actions**, and then select **Delete**.</span></span>

        ![Odstranění sloupce PrimaryContactPersonId](media/vend_selfref3.png)

    4. <span data-ttu-id="4bf38-150">Opakujte tyto kroky pro odstranění sloupce **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** column.</span></span>

        ![Odstranění sloupce InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. <span data-ttu-id="4bf38-152">Uložte změny do mapování.</span><span class="sxs-lookup"><span data-stu-id="4bf38-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="4bf38-153">Vypněte sledování změn pro tabulku **Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-153">Turn off change tracking for the **Vendors V2** table.</span></span>

    1. <span data-ttu-id="4bf38-154">V pracovním prostoru **Správa dat** vyberte dlaždici **Datové tabulky**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="4bf38-155">Vyberte tabulku **Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-155">Select the **Vendors V2** table.</span></span>
    3. <span data-ttu-id="4bf38-156">V podokně akcí zvolte **Možnosti** a poté vyberte **Sledování změn**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Vyberte možnost Sledování změn](media/selfref_options.png)

    4. <span data-ttu-id="4bf38-158">Vyberte **Zakázat sledování změn**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-158">Select **Disable Change Tracking**.</span></span>

        ![Výběr Zakázat sledování změn.](media/selfref_tracking.png)

3. <span data-ttu-id="4bf38-160">Spusťte počáteční synchronizaci mapování **Vendors V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="4bf38-161">Počáteční synchronizace by měla úspěšně proběhnout bez chyb.</span><span class="sxs-lookup"><span data-stu-id="4bf38-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="4bf38-162">Spusťte počáteční synchronizaci pro mapování **CDS Contacts V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="4bf38-163">Toto mapování musíte synchronizovat, pokud chcete synchronizovat sloupec primárního kontaktu v tabulce dodavatelů, protože řádky kontaktů je také třeba také nejprve synchronizovat.</span><span class="sxs-lookup"><span data-stu-id="4bf38-163">You must sync this mapping if you want to sync the primary contact column on the vendors table, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="4bf38-164">Přidejte sloupce **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** zpět do mapování **Vendors V2 (msdyn\_vendors)** a uložte mapování.</span><span class="sxs-lookup"><span data-stu-id="4bf38-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="4bf38-165">Spusťte opět počáteční synchronizaci mapování **Vendors V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="4bf38-166">Všechny řádky budou synchronizovány, protože sledování změn je vypnuto.</span><span class="sxs-lookup"><span data-stu-id="4bf38-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="4bf38-167">Opět zapněte sledování změn pro tabulku **Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-167">Turn change tracking back on for the **Vendors V2** table.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="4bf38-168">Vyřešte chyby v mapování tabulky Customers V3–to–Accounts</span><span class="sxs-lookup"><span data-stu-id="4bf38-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="4bf38-169">Mohli byste narazit na následující počáteční chyby synchronizace na mapování **Customers V3** na **Accounts**, pokud tabulky mají existující řádky s hodnotami ve sloupcích **ContactPersonID** a **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** columns.</span></span> <span data-ttu-id="4bf38-170">Tyto chyby se vyskytují proto, že **InvoiceAccount** je sloupec s vlastním odkazem a **ContactPersonID** je kruhový odkaz v mapování dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4bf38-170">These errors occur because **InvoiceAccount** is a self-referencing column, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="4bf38-171">Chybové zprávy, které obdržíte, budou mít následující formulář.</span><span class="sxs-lookup"><span data-stu-id="4bf38-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="4bf38-172">*Nelze vyřešit identifikátor GUID pro pole: \<field\>. Vyhledávání nebylo nalezeno: \<value\>. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="4bf38-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="4bf38-173">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="4bf38-173">Here are some examples:</span></span>

- <span data-ttu-id="4bf38-174">*Nelze vyřešit identifikátor GUID pro pole: primarycontactid.msdyn\_contactpersonid. Vyhledávání nebylo nalezeno: 000056. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="4bf38-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="4bf38-175">*Nelze vyřešit identifikátor GUID pro pole: msdyn\_billingaccount.accountnumber. Vyhledávání nebylo nalezeno: 1206-1. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="4bf38-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="4bf38-176">Pokud mají libovolné řádky v tabulce zákazníka hodnoty ve sloupcích **ContactPersonID** a **InvoiceAccount**, postupujte podle kroků v části níže a dokončete počáteční synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="4bf38-176">If any rows in the customer table have values in the **ContactPersonID** and **InvoiceAccount** columns, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="4bf38-177">Tento přístup můžete použít pro jakékoli dodávané tabulky, jako jsou **´´Učty** a **Kontakty**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="4bf38-178">V aplikaci Finance and Operations odstraňte sloupce **ContactPersonID** a **InvoiceAccount** z mapování **Customers V3 (accounts)** a mapování uložte.</span><span class="sxs-lookup"><span data-stu-id="4bf38-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** columns from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="4bf38-179">Na stránce mapování s dvojitým zápisem pro **Customers V3 (accounts)** na kartě **Mapování tabulek** v levém filtru vyberte **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="4bf38-180">V pravém filtru vyberte **Dataverse.Account**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="4bf38-181">Vyhledejte **contactperson** a najděte zdrojový sloupec **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-181">Search for **contactperson** to find the **ContactPersonID** source column.</span></span>
    3. <span data-ttu-id="4bf38-182">Vyberte **Akce** a poté vyberte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-182">Select **Actions**, and then select **Delete**.</span></span>

        ![Odstranění sloupce ContactPersonID](media/cust_selfref3.png)

    4. <span data-ttu-id="4bf38-184">Opakujte tyto kroky pro odstranění sloupce **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-184">Repeat these steps to delete the **InvoiceAccount** column.</span></span>

        ![Odstranění sloupce InvoiceAccount](media/cust_selfref4.png)

    5. <span data-ttu-id="4bf38-186">Uložte změny do mapování.</span><span class="sxs-lookup"><span data-stu-id="4bf38-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="4bf38-187">Vypněte sledování změn pro tabulku **Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-187">Turn off change tracking for the **Customers V3** table.</span></span>

    1. <span data-ttu-id="4bf38-188">V pracovním prostoru **Správa dat** vyberte dlaždici **Datové tabulky**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="4bf38-189">Vyberte tabulku **Zákazníci V3**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-189">Select the **Customers V3** table.</span></span>
    3. <span data-ttu-id="4bf38-190">V podokně akcí zvolte **Možnosti** a poté vyberte **Sledování změn**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Vyberte možnost Sledování změn](media/selfref_options.png)

    4. <span data-ttu-id="4bf38-192">Vyberte **Zakázat sledování změn**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-192">Select **Disable Change Tracking**.</span></span>

        ![Výběr Zakázat sledování změn.](media/selfref_tracking.png)

3. <span data-ttu-id="4bf38-194">Spusťte počáteční synchronizaci pro mapování **Customers V3 (Accounts)**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="4bf38-195">Počáteční synchronizace by měla úspěšně proběhnout bez chyb.</span><span class="sxs-lookup"><span data-stu-id="4bf38-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="4bf38-196">Spusťte počáteční synchronizaci pro mapování **CDS Contacts V2 (contacts)**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4bf38-197">Existují dvě mapy se stejným názvem.</span><span class="sxs-lookup"><span data-stu-id="4bf38-197">There are two maps that have the same name.</span></span> <span data-ttu-id="4bf38-198">Vyberte mapu, která má následující popis na kartě **Podrobnosti**: **Šablona s dvojím zápisem pro synchronizaci mezi kontakty dodavatele FO.CDS V2 a CDS.Contacts. Vyžaduje nový balíček \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="4bf38-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="4bf38-199">Přidejte sloupce **InvoiceAccount** a **ContactPersonId** zpět do mapování **Customers V3 (Accounts)** a mapování uložte.</span><span class="sxs-lookup"><span data-stu-id="4bf38-199">Add the **InvoiceAccount** and **ContactPersonId** columns back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="4bf38-200">Sloupce **InvoiceAccount** i **ContactPersonId** jsou opět součástí živého synchronizačního režimu.</span><span class="sxs-lookup"><span data-stu-id="4bf38-200">Both the **InvoiceAccount** column and the **ContactPersonId** column are now part of live synchronization mode again.</span></span> <span data-ttu-id="4bf38-201">V dalším kroku dokončíte počáteční synchronizaci těchto sloupců.</span><span class="sxs-lookup"><span data-stu-id="4bf38-201">In the next step, you will do the initial synchronization for these columns.</span></span>
6. <span data-ttu-id="4bf38-202">Spusťte opět počáteční synchronizaci pro mapování **Customers V3 (Accounts)**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="4bf38-203">Protože sledování změn je vypnuto, data pro **InvoiceAccount** a **ContactPersonId** budou synchronizována z aplikace Finance and Operations do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="4bf38-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="4bf38-204">Chcete-li synchronizovat data pro **InvoiceAccount** a **ContactPersonId** z Dataverse do aplikace Finance and Operations, musíte použít projekt integrace dat.</span><span class="sxs-lookup"><span data-stu-id="4bf38-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="4bf38-205">V Power Apps vytvořit projekt integrace dat mezi tabulkami **Sales.Account** a **Finance and Operations apps.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="4bf38-206">Směr dat musí být z Dataverse do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4bf38-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="4bf38-207">Protože **InvoiceAccount** je nový atribut v dvojitém zápisu, možná budete chtít přeskočit počáteční synchronizaci pro tento atribut.</span><span class="sxs-lookup"><span data-stu-id="4bf38-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="4bf38-208">Další informace naleznete v tématu [Integrace dat do Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="4bf38-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="4bf38-209">Následující ilustrace ukazuje projekt, který aktualizuje **CustomerAccount** a **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Projekt integrace dat pro aktualizaci CustomerAccount a ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="4bf38-211">Přidejte do filtru kritéria společnosti na straně Dataverse, aby byly v aplikaci Finance and Operations aktualizovány pouze řádky, které odpovídají kritériím filtru.</span><span class="sxs-lookup"><span data-stu-id="4bf38-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="4bf38-212">Chcete-li přidat filtr, vyberte tlačítko filtru.</span><span class="sxs-lookup"><span data-stu-id="4bf38-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="4bf38-213">Potom v dialogovém okně **Upravit dotaz** můžete přidat dotaz filtru jako **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="4bf38-214">[POZNÁMKA] Pokud tlačítko filtru není k dispozici, vytvořte podpůrný ticket a požádejte tým pro integraci dat o povolení filtrování u klienta.</span><span class="sxs-lookup"><span data-stu-id="4bf38-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="4bf38-215">Pokud nezadáte dotaz filtru pro **\_msdyn\_company\_value**, budou všechny řádky synchronizovány.</span><span class="sxs-lookup"><span data-stu-id="4bf38-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Přidání dotazu filtru](media/cust_selfref7.png)

    <span data-ttu-id="4bf38-217">Počáteční synchronizace řádků je nyní dokončena.</span><span class="sxs-lookup"><span data-stu-id="4bf38-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="4bf38-218">V aplikaci Finance and Operations opět zapněte sledování změn pro tabulku **Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="4bf38-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** table.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
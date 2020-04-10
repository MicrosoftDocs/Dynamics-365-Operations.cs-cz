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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172707"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="b017c-103">Poradce při potížích s počáteční synchronizací</span><span class="sxs-lookup"><span data-stu-id="b017c-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="b017c-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b017c-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b017c-105">Konkrétně obsahuje informace, které vám pomohou vyřešit problémy, které by se mohly vyskytnou během počáteční synchronizace.</span><span class="sxs-lookup"><span data-stu-id="b017c-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="b017c-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="b017c-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b017c-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="b017c-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="b017c-108">Zkontrolovat chyby počáteční synchronizace v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b017c-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="b017c-109">Po povolení šablon mapování by měl být **Spuštěn** stav mapování.</span><span class="sxs-lookup"><span data-stu-id="b017c-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="b017c-110">Pokud je stav **Nespuštěn**, došlo k chybám při počáteční synchronizaci.</span><span class="sxs-lookup"><span data-stu-id="b017c-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="b017c-111">Chcete-li zobrazit chyby, vyberte kartu **Podrobnosti o počáteční synchronizaci** na stránce **Dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="b017c-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Karta počáteční podrobnosti synchronizace](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="b017c-113">Počáteční synchronizaci nelze dokončit: 400 Chybný požadavek</span><span class="sxs-lookup"><span data-stu-id="b017c-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="b017c-114">**Požadovaná role pro opravu problému:** správce systému</span><span class="sxs-lookup"><span data-stu-id="b017c-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b017c-115">Při pokusu o spuštění mapování a počáteční synchronizace se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="b017c-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="b017c-116">*Vzdálený server vrátil chybu: (400) nesprávný požadavek.), při exportu AX byla zjištěna chyba*</span><span class="sxs-lookup"><span data-stu-id="b017c-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="b017c-117">Následuje příklad úplné chybové zprávy.</span><span class="sxs-lookup"><span data-stu-id="b017c-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="b017c-118">Pokud k této chybě dojde konzistentně a nelze dokončit počáteční synchronizaci, opravte problém pomocí následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="b017c-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="b017c-119">Přihlaste se k virtuálnímu počítači pro aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b017c-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="b017c-120">Otevřete konzoli MMC.</span><span class="sxs-lookup"><span data-stu-id="b017c-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="b017c-121">V podokně **Služby** zkontrolujte, zda je spuštěna služba platformy importu a exportu dat Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b017c-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="b017c-122">Restartujte ji, pokud byla zastavena, protože ji vyžaduje počáteční synchronizace.</span><span class="sxs-lookup"><span data-stu-id="b017c-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="b017c-123">Chyba počáteční synchronizace: 403 zakázáno</span><span class="sxs-lookup"><span data-stu-id="b017c-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="b017c-124">Při počáteční synchronizaci se může zobrazit následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="b017c-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="b017c-125">*(\[zakázáno\], Vzdálený server vrátil chybu: (403) Zakázáno.), při exportu AX byla zjištěna chyba*</span><span class="sxs-lookup"><span data-stu-id="b017c-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="b017c-126">Chcete-li opravit problém, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="b017c-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="b017c-127">Přihlášení do aplikace Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b017c-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="b017c-128">Na stránce **aplikací Azure Active Directory** odstraňte klienta **DtAppID** a poté jej znovu přidejte.</span><span class="sxs-lookup"><span data-stu-id="b017c-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Seznam aplikací Azure AD](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="b017c-130">Selhání odkazů na sebe sama při počáteční synchronizaci</span><span class="sxs-lookup"><span data-stu-id="b017c-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="b017c-131">Může se zobrazit chybová zpráva podobná následujícímu příkladu v případě, že některá z vašich mapování mají vlastní odkazy:</span><span class="sxs-lookup"><span data-stu-id="b017c-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="b017c-132">*U dodavatelů V2 se jedná o následující chybu: ID záznamu: nový záznam, ErrorMessage: nelze přeložit identifikátor GUID pole: msdyn\_invoicevendoraccountnumber. msdyn\_vendoraccountnumber. Vyhledávací hodnota nebyla nalezena: CN-001. Vyzkoušejte, zda tyto adresy URL neexistují referenční data: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` EQ "CN-001"*</span><span class="sxs-lookup"><span data-stu-id="b017c-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="b017c-133">Tento typ chyby se objevuje při počáteční synchronizaci mapování s vlastními odkazy.</span><span class="sxs-lookup"><span data-stu-id="b017c-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="b017c-134">V předchozím příkladu účet faktury pole odkazuje na entitu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="b017c-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="b017c-135">Chcete-li tento problém vyřešit, bude pravděpodobně nutné před provedením počáteční synchronizace dvakrát spustit mapování.</span><span class="sxs-lookup"><span data-stu-id="b017c-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>


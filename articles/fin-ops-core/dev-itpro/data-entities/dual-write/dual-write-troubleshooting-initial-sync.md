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
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Poradce při potížích s počáteční synchronizací

[!include [banner](../../includes/banner.md)]



Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service. Konkrétně obsahuje informace, které vám pomohou vyřešit problémy, které by se mohly vyskytnou během počáteční synchronizace. 

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Zkontrolovat chyby počáteční synchronizace v aplikaci Finance and Operations

Po povolení šablon mapování by měl být **Spuštěn** stav mapování. Pokud je stav **Nespuštěn**, došlo k chybám při počáteční synchronizaci. Chcete-li zobrazit chyby, vyberte kartu **Podrobnosti o počáteční synchronizaci** na stránce **Dvojí zápis**.

![Karta počáteční podrobnosti synchronizace](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Počáteční synchronizaci nelze dokončit: 400 Chybný požadavek

**Požadovaná role pro opravu problému:** správce systému

Při pokusu o spuštění mapování a počáteční synchronizace se může zobrazit následující chybová zpráva:

*Vzdálený server vrátil chybu: (400) nesprávný požadavek.), při exportu AX byla zjištěna chyba*

Následuje příklad úplné chybové zprávy.

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

Pokud k této chybě dojde konzistentně a nelze dokončit počáteční synchronizaci, opravte problém pomocí následujícího postupu.

1. Přihlaste se k virtuálnímu počítači pro aplikaci Finance and Operations.
2. Otevřete konzoli MMC. 
3. V podokně **Služby** zkontrolujte, zda je spuštěna služba platformy importu a exportu dat Microsoft Dynamics 365. Restartujte ji, pokud byla zastavena, protože ji vyžaduje počáteční synchronizace.

## <a name="initial-synchronization-error-403-forbidden"></a>Chyba počáteční synchronizace: 403 zakázáno

Při počáteční synchronizaci se může zobrazit následující chybová zpráva:

*(\[zakázáno\], Vzdálený server vrátil chybu: (403) Zakázáno.), při exportu AX byla zjištěna chyba*

Chcete-li opravit problém, postupujte následovně.

1. Přihlášení do aplikace Finance and Operations.
2. Na stránce **aplikací Azure Active Directory** odstraňte klienta **DtAppID** a poté jej znovu přidejte.

![Seznam aplikací Azure AD](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a>Selhání odkazů na sebe sama při počáteční synchronizaci

Může se zobrazit chybová zpráva podobná následujícímu příkladu v případě, že některá z vašich mapování mají vlastní odkazy:

*U dodavatelů V2 se jedná o následující chybu: ID záznamu: nový záznam, ErrorMessage: nelze přeložit identifikátor GUID pole: msdyn\_invoicevendoraccountnumber. msdyn\_vendoraccountnumber. Vyhledávací hodnota nebyla nalezena: CN-001. Vyzkoušejte, zda tyto adresy URL neexistují referenční data: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` EQ "CN-001"*

Tento typ chyby se objevuje při počáteční synchronizaci mapování s vlastními odkazy. V předchozím příkladu účet faktury pole odkazuje na entitu dodavatele.

Chcete-li tento problém vyřešit, bude pravděpodobně nutné před provedením počáteční synchronizace dvakrát spustit mapování.


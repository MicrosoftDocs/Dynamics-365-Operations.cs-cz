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
ms.openlocfilehash: 709a3c332bb6d086910b257fee9cdec8d2bc81a2
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941048"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Poradce při potížích s počáteční synchronizací

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse. Konkrétně obsahuje informace, které vám pomohou vyřešit problémy, které by se mohly vyskytnou během počáteční synchronizace.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Zkontrolovat chyby počáteční synchronizace v aplikaci Finance and Operations

Po povolení šablon mapování by měl být **Spuštěn** stav mapování. Pokud je stav **Nespuštěn**, došlo k chybám při počáteční synchronizaci. Chcete-li zobrazit chyby, vyberte kartu **Podrobnosti o počáteční synchronizaci** na stránce **Dvojí zápis**.

![Chyba na kartě Počáteční podrobnosti synchronizace](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Počáteční synchronizaci nelze dokončit: 400 Chybný požadavek

**Požadovaná role pro opravu problému:** správce systému

Při pokusu o spuštění mapování a počáteční synchronizace se může zobrazit následující chybová zpráva:

*(\[Chybný požadavek\] Vzdálený server vrátil chybu: (400) chybný požadavek.), při exportu AX byla zjištěna chyba*

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

![DtAppID klient v seznamu aplikací Azure AD](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Selhání odkazů na sebe sama a cirkulárních odkazů při počáteční synchronizaci

Můžou se zobrazit chybové zprávy podobné následujícímu příkladu v případě, že některá z vašich mapování mají odkazy na sebe sama a cirkulární odkazy. Chyby spadají do těchto kategorií:

- [Chyby v mapování tabulek Vendors V2–to–msdyn_vendors](#error-vendor-map)
- [Chyby v mapování tabulek Customers V3–to–Accounts](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Řešení chyb v mapování tabulek Vendors V2–to–msdyn_vendors

Mohli byste narazit na následující počáteční chyby synchronizace na mapování **Vendors V2** na **msdyn\_vendors**, pokud tabulky mají existující řádky s hodnotami ve sloupcích **PrimaryContactPersonId** a **InvoiceVendorAccountNumber**. Tyto chyby se vyskytují proto, že **InvoiceVendorAccountNumber** je sloupec s vlastním odkazem a **PrimaryContactPersonId** je kruhový odkaz v mapování dodavatele.

Chybové zprávy, které obdržíte, budou mít následující formulář.

*Nelze vyřešit identifikátor GUID pro pole: \<field\>. Vyhledávání nebylo nalezeno: \<value\>. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Několik příkladů:

- *Nelze vyřešit identifikátor GUID pro pole: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Vyhledávání nebylo nalezeno: 000056. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Nelze vyřešit identifikátor GUID pro pole: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Vyhledávání nebylo nalezeno: V24-1. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Pokud mají libovolné řádky v tabulce dodavatele hodnoty ve sloupcích **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** , postupujte podle kroků v části níže a dokončete počáteční synchronizaci.

1. V aplikaci Finance and Operations odstraňte sloupce **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** z mapování a pak mapování uložte.

    1. Na stránce mapování s dvojitým zápisem **Vendors V2 (msdyn\_vendors)**, na kartě **Mapování tabulek**, v levém filtru vyberte **Finance and Operations apps.Vendors V2**. V pravém filtru vyberte **Sales.Vendor**.
    2. Vyhledejte **primarycontactperson** a najděte zdrojový sloupec **PrimaryContactPersonId**.
    3. Vyberte **Akce** a poté vyberte **Odstranit**.

        ![Odstranění sloupce PrimaryContactPersonId](media/vend_selfref3.png)

    4. Opakujte tyto kroky pro odstranění sloupce **InvoiceVendorAccountNumber**.

        ![Odstranění sloupce InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. Uložte změny do mapování.

2. Vypněte sledování změn pro tabulku **Vendors V2**.

    1. V pracovním prostoru **Správa dat** vyberte dlaždici **Datové tabulky**.
    2. Vyberte tabulku **Vendors V2**.
    3. V podokně akcí zvolte **Možnosti** a poté vyberte **Sledování změn**.

        ![Vyberte možnost Sledování změn](media/selfref_options.png)

    4. Vyberte **Zakázat sledování změn**.

        ![Výběr Zakázat sledování změn.](media/selfref_tracking.png)

3. Spusťte počáteční synchronizaci mapování **Vendors V2 (msdyn\_vendors)**. Počáteční synchronizace by měla úspěšně proběhnout bez chyb.
4. Spusťte počáteční synchronizaci pro mapování **CDS Contacts V2 (contacts)**. Toto mapování musíte synchronizovat, pokud chcete synchronizovat sloupec primárního kontaktu v tabulce dodavatelů, protože řádky kontaktů je také třeba také nejprve synchronizovat.
5. Přidejte sloupce **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** zpět do mapování **Vendors V2 (msdyn\_vendors)** a uložte mapování.
6. Spusťte opět počáteční synchronizaci mapování **Vendors V2 (msdyn\_vendors)**. Všechny řádky budou synchronizovány, protože sledování změn je vypnuto.
7. Opět zapněte sledování změn pro tabulku **Vendors V2**.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Vyřešte chyby v mapování tabulky Customers V3–to–Accounts

Mohli byste narazit na následující počáteční chyby synchronizace na mapování **Customers V3** na **Accounts**, pokud tabulky mají existující řádky s hodnotami ve sloupcích **ContactPersonID** a **InvoiceAccount**. Tyto chyby se vyskytují proto, že **InvoiceAccount** je sloupec s vlastním odkazem a **ContactPersonID** je kruhový odkaz v mapování dodavatele.

Chybové zprávy, které obdržíte, budou mít následující formulář.

*Nelze vyřešit identifikátor GUID pro pole: \<field\>. Vyhledávání nebylo nalezeno: \<value\>. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Několik příkladů:

- *Nelze vyřešit identifikátor GUID pro pole: primarycontactid.msdyn\_contactpersonid. Vyhledávání nebylo nalezeno: 000056. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Nelze vyřešit identifikátor GUID pro pole: msdyn\_billingaccount.accountnumber. Vyhledávání nebylo nalezeno: 1206-1. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Pokud mají libovolné řádky v tabulce zákazníka hodnoty ve sloupcích **ContactPersonID** a **InvoiceAccount**, postupujte podle kroků v části níže a dokončete počáteční synchronizaci. Tento přístup můžete použít pro jakékoli dodávané tabulky, jako jsou **´´Učty** a **Kontakty**.

1. V aplikaci Finance and Operations odstraňte sloupce **ContactPersonID** a **InvoiceAccount** z mapování **Customers V3 (accounts)** a mapování uložte.

    1. Na stránce mapování s dvojitým zápisem pro **Customers V3 (accounts)** na kartě **Mapování tabulek** v levém filtru vyberte **Finance and Operations app.Customers V3**. V pravém filtru vyberte **Dataverse.Account**.
    2. Vyhledejte **contactperson** a najděte zdrojový sloupec **ContactPersonID**.
    3. Vyberte **Akce** a poté vyberte **Odstranit**.

        ![Odstranění sloupce ContactPersonID](media/cust_selfref3.png)

    4. Opakujte tyto kroky pro odstranění sloupce **InvoiceAccount**.

        ![Odstranění sloupce InvoiceAccount](media/cust_selfref4.png)

    5. Uložte změny do mapování.

2. Vypněte sledování změn pro tabulku **Customers V3**.

    1. V pracovním prostoru **Správa dat** vyberte dlaždici **Datové tabulky**.
    2. Vyberte tabulku **Zákazníci V3**.
    3. V podokně akcí zvolte **Možnosti** a poté vyberte **Sledování změn**.

        ![Vyberte možnost Sledování změn](media/selfref_options.png)

    4. Vyberte **Zakázat sledování změn**.

        ![Výběr Zakázat sledování změn.](media/selfref_tracking.png)

3. Spusťte počáteční synchronizaci pro mapování **Customers V3 (Accounts)**. Počáteční synchronizace by měla úspěšně proběhnout bez chyb.
4. Spusťte počáteční synchronizaci pro mapování **CDS Contacts V2 (contacts)**.

    > [!NOTE]
    > Existují dvě mapy se stejným názvem. Vyberte mapu, která má následující popis na kartě **Podrobnosti**: **Šablona s dvojím zápisem pro synchronizaci mezi kontakty dodavatele FO.CDS V2 a CDS.Contacts. Vyžaduje nový balíček \[Dynamics365SupplyChainExtended\].**

5. Přidejte sloupce **InvoiceAccount** a **ContactPersonId** zpět do mapování **Customers V3 (Accounts)** a mapování uložte. Sloupce **InvoiceAccount** i **ContactPersonId** jsou opět součástí živého synchronizačního režimu. V dalším kroku dokončíte počáteční synchronizaci těchto sloupců.
6. Spusťte opět počáteční synchronizaci pro mapování **Customers V3 (Accounts)**. Protože sledování změn je vypnuto, data pro **InvoiceAccount** a **ContactPersonId** budou synchronizována z aplikace Finance and Operations do Dataverse.
7. Chcete-li synchronizovat data pro **InvoiceAccount** a **ContactPersonId** z Dataverse do aplikace Finance and Operations, musíte použít projekt integrace dat.

    1. V Power Apps vytvořit projekt integrace dat mezi tabulkami **Sales.Account** a **Finance and Operations apps.Customers V3**. Směr dat musí být z Dataverse do aplikace Finance and Operations. Protože **InvoiceAccount** je nový atribut v dvojitém zápisu, možná budete chtít přeskočit počáteční synchronizaci pro tento atribut. Další informace naleznete v tématu [Integrace dat do Dataverse](/power-platform/admin/data-integrator).

        Následující ilustrace ukazuje projekt, který aktualizuje **CustomerAccount** a **ContactPersonId**.

        ![Projekt integrace dat pro aktualizaci CustomerAccount a ContactPersonId](media/cust_selfref6.png)

    2. Přidejte do filtru kritéria společnosti na straně Dataverse, aby byly v aplikaci Finance and Operations aktualizovány pouze řádky, které odpovídají kritériím filtru. Chcete-li přidat filtr, vyberte tlačítko filtru. Potom v dialogovém okně **Upravit dotaz** můžete přidat dotaz filtru jako **\_msdyn\_company\_value eq '\<guid\>'**. 

        > [POZNÁMKA] Pokud tlačítko filtru není k dispozici, vytvořte podpůrný ticket a požádejte tým pro integraci dat o povolení filtrování u klienta.

        Pokud nezadáte dotaz filtru pro **\_msdyn\_company\_value**, budou všechny řádky synchronizovány.

        ![Přidání dotazu filtru](media/cust_selfref7.png)

    Počáteční synchronizace řádků je nyní dokončena.

8. V aplikaci Finance and Operations opět zapněte sledování změn pro tabulku **Customers V3**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
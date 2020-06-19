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

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Selhání odkazů na sebe sama a cirkulárních odkazů při počáteční synchronizaci

Můžou se zobrazit chybové zprávy podobné následujícímu příkladu v případě, že některá z vašich mapování mají odkazy na sebe sama a cirkulární odkazy. Chyby spadají do těchto kategorií:

- [Dodavatelé V2 do mapování entity msdyn_vendors](#error-vendor-map)
- [Mapování entit zákazníků V3 na účty](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Vyřešte chybu v Vendors V2 na mapování entit msdyn_vendors

Mohli byste narazit na následující počáteční chyby synchronizace na mapování **Vendors V2** na **msdyn_vendors**, pokud entity mají existující záznamy s hodnotami v polích **PrimaryContactPersonId** a **InvoiceVendorAccountNumber**. To proto, že **InvoiceVendorAccountNumber** je pole s vlastním odkazem a **PrimaryContactPersonId** je kruhový odkaz v mapování dodavatele.

*Nelze vyřešit identifikátor GUID pro pole: <field>. Vyhledávání nebylo nalezeno: <value>. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

Zde je několik příkladů:

- *Nelze vyřešit GUID pro pole: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Vyhledávání nebylo nalezeno: 000056. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?2$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Nelze vyřešit GUID pro pole: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Vyhledávání nebylo nalezeno: V24-1. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Pokud máte záznamy s hodnotami v těchto polích v entitě dodavatele, postupujte podle kroků v části níže a dokončete počáteční synchronizaci úspěšně.

1. V aplikaci Finance and Operations odstraňte pole **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** z mapování a změny uložte.

    1. Přejděte na stránku mapování s dvojitým zápisem **Vendors V2 (msdyn_vendors)** a vyberte kartu **Mapování entit**. V levém filtru vyberte **Finance and Operations apps.Vendors V2**. V pravém filtru vyberte **Sales.Vendor**.

    2. Vyhledejte **primarycontactperson** a najděte zdrojové pole **PrimaryContactPersonId**.
    
    3. Klikněte na tlačítko **Akce** a vyberte možnost **Odstranit**.
    
        ![vlastní nebo kruhový odkaz 3](media/vend_selfref3.png)
    
    4. Opakujte pro odstranění pole **InvoiceVendorAccountNumber**.
    
        ![vlastní nebo kruhový odkaz 4](media/vend-selfref4.png)
    
    5. Uložte změny mapování.

2. Zakažte sledování změn pro entitu **Vendors V2**.

    1. Přejděte na **Správa dat \> Datové entity**.
    
    2. Vyberte entitu **Vendors V2**.
    
    3. Klikněte na **Možnosti** z panelu nabídek a poté **Sledování změn**.
    
        ![vlastní nebo kruhový odkaz 5](media/selfref_options.png)
    
    4. Klikněte na **Zakázat sledování změn**.
    
        ![vlastní nebo kruhový odkaz 6](media/selfref_tracking.png)

3. Spusťte počáteční synchronizaci mapování **Vendors V2 (msdyn_vendors)**. Počáteční synchronizace by měla úspěšně proběhnout bez chyb.

4. Spusťte počáteční synchronizaci pro mapování **CDS Contacts V2 (contacts)**. Toto mapování musíte synchronizovat, pokud chcete synchronizovat pole primárního kontaktu na entitě dodavatelů, protože záznamy kontaktů je také třeba nejprve synchronizovat.

5. Přidejte pole **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** zpět do mapování **Vendors V2 (msdyn_vendors)** a uložte mapování.

6. Spusťte počáteční znovu pro mapování **Vendors V2 (msdyn_vendors)**. Všechny záznamy budou synchronizovány, protože sledování změn je zakázáno.

7. Povolte sledování změn pro entitu **Vendors V2**.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Vyřešte chybu v mapování entit Customers V3 to Accounts

Mohli byste narazit na následující počáteční chyby synchronizace na mapování **VCustomers V3** na **Accounts**, pokud entity mají existující záznamy s hodnotami v polích **ContactPersonID** a **InvoiceAccount**. To proto, že **InvoiceAccount** je pole s vlastním odkazem a **ContactPersonID** je kruhový odkaz v mapování dodavatele.

*Nelze vyřešit identifikátor GUID pro pole: <field>. Vyhledávání nebylo nalezeno: <value>. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *Nelze vyřešit GUID pro pole: primarycontactid.msdyn_contactpersonid. Vyhledávání nebylo nalezeno: 000056. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?2$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Nelze vyřešit GUID pro pole: msdyn_billingaccount.accountnumber. Vyhledávání nebylo nalezeno: 1206-1. Vyzkoušejte tyto adresy URL a zkontrolujte, zda existují referenční údaje: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

Pokud máte záznamy s hodnotami v těchto polích v entitě zákazníka, postupujte podle kroků v části níže a dokončete počáteční synchronizaci úspěšně. Tento přístup můžete použít pro jakékoli dodávané entity, jako jsou účty a kontakty.

1. V aplikaci Finance and Operations odstraňte pole **ContactPersonID** a **InvoiceAccount** z mapování **Customers V3 (accounts)** a mapování uložte.

    1. Přejděte na stránku mapování s dvojitým zápisem pro **Customers V3 (accounts)** a vyberte kartu **Mapování entit**. V levém filtru vyberte **Finance and Operations app.Customers V3**. V pravém filtru vyberte **Common Data Service.Account**.

    2. Vyhledejte **contactperson** a najděte zdrojové pole **ContactPersonID**.
    
    3. Klikněte na tlačítko **Akce** a vyberte možnost **Odstranit**.
    
        ![vlastní nebo kruhový odkaz 3](media/cust_selfref3.png)
    
    4. Opakujte pro odstranění pole **InvoiceAccount**.
    
        ![vlastní nebo kruhový odkaz](media/cust_selfref4.png)
    
    5. Uložte změny mapování.

2. Zakažte sledování změn pro entitu **Customers V3**.

    1. Přejděte na **Správa dat \> Datové entity**.
    
    2. Vyberte entitu **Customers V3**.
    
    3. Klikněte na **Možnosti** z panelu nabídek a poté **Sledování změn**.
    
        ![vlastní nebo kruhový odkaz 5](media/selfref_options.png)
    
    4. Klikněte na **Zakázat sledování změn**.
    
        ![vlastní nebo kruhový odkaz 6](media/selfref_tracking.png)

3. Spusťte počáteční synchronizaci pro mapování **Customers V3 (Accounts)**. Počáteční synchronizace by měla úspěšně proběhnout bez chyb.

4. Spusťte počáteční synchronizaci pro mapování **CDS Contacts V2 (contacts)**. K dispozici jsou 2 mapy se stejným názvem. Vyberte tu s popisem **Šablona s dvojím zápisem pro synchronizaci mezi kontakty dodavatele FO.CDS V2 a CDS.Contacts. Vyžaduje nový balíček \[Dynamics365SupplyChainExtended\].** na kartě mapy **Podrobnosti**.

5. Přidejte **InvoiceAccount** a **ContactPersonId** zpět do mapování **Customers V3 (Accounts)** a mapování uložte. Nyní pole **InvoiceAccount** i **ContactPersonId** jsou opět součástí živého synchronizačního režimu. V dalším kroku dokončíte počáteční synchronizaci těchto polí.

6. Spusťte opět počáteční synchronizaci pro mapování **Customers V3 (Accounts)**. Protože sledování změn je zakázáno, spuštěním synchronizace budou synchronizována data pro **InvoiceAccount** a **ContactPersonId** z aplikace Finance and Operations do Common Data Service.

7. Chcete-li synchronizovat data pro **InvoiceAccount** a **ContactPersonId** z Common Data Service do Finance and Operations, používáte projekt integrace dat.

    1. V Power Apps vytvořit projekt integrace dat mezi entitami **Sales.Account** a **Finance and Operations apps.Customers V3**. Směr dat musí být z Common Data Service do aplikace Finance and Operations.  Protože **InvoiceAccount** je nový atribut v dvojitém zápisu, možná budete chtít přeskočit počáteční synchronizaci pro tento atribut. Další informace naleznete v tématu [Integrace dat do Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Následující obrázek ukazuje projekt, který aktualizuje **CustomerAccount** a **ContactPersonId**.

        ![vlastní nebo kruhový odkaz](media/cust_selfref6.png)

    2. Přidejte do filtru kritéria společnosti na straně Common Data Service, protože v aplikaci Finance and Operations budou aktualizovány pouze záznamy, které odpovídají kritériím filtru. Chcete-li přidat filtr, klikněte na ikonu filtru. V dialogovém okně **Upravit dotaz** můžete přidat dotaz filtru jako **_msdyn_company_value eq '\<guid\>'**. Pokud ikona filtru není k dispozici, vytvořte podpůrný ticket a požádejte tým pro integraci dat o povolení filtrování u klienta. Pokud nezadáte dotaz filtru pro **_msdyn_company_value**, jsou všechny záznamy synchronizovány.

        ![vlastní nebo kruhový odkaz](media/cust_selfref7.png)

        Tím je dokončena počáteční synchronizace záznamů.

8. Povolte sledování změn pro entitu **Customers V3** v aplikaci Finance and Operations.


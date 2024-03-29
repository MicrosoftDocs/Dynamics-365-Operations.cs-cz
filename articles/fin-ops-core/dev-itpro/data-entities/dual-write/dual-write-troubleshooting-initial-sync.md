---
title: Poradce při potížích s počáteční synchronizací
description: Tento článek obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy, které by se mohly vyskytnou během počáteční synchronizace.
author: RamaKrishnamoorthy
ms.date: 06/24/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d9d74eea90cc2dfca2d5decf6e5cd1d7f52da2a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289477"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Poradce při potížích s počáteční synchronizací

[!include [banner](../../includes/banner.md)]



Tento článek obsahuje informace o odstraňování potíží pro integrací dvojitého zápisu mezi finančními a provozními aplikacemi a Dataverse. Konkrétně obsahuje informace, které vám pomohou vyřešit problémy, které by se mohly vyskytnou během počáteční synchronizace.

> [!IMPORTANT]
> Některé problémy, které tento článek řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Kontrola úvodní synchronizace ve finanční a provozní aplikaci

Po povolení šablon mapování by měl být **Spuštěn** stav mapování. Pokud je stav **Nespuštěn**, došlo k chybám při počáteční synchronizaci. Chcete-li zobrazit chyby, vyberte kartu **Podrobnosti o počáteční synchronizaci** na stránce **Dvojí zápis**.

![Chyba na kartě Počáteční podrobnosti synchronizace.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Počáteční synchronizaci nelze dokončit: 400 Chybný požadavek

**Požadovaná role pro opravu problému:** správce systému

Při pokusu o spuštění mapování a počáteční synchronizace se může zobrazit následující chybová zpráva:

*(\[Chybný požadavek\] Vzdálený server vrátil chybu: (400) chybný požadavek.), při exportu AX byla zjištěna chyba.*

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

1. Přihlaste se k virtuálnímu počítači pro finanční a provozní aplikaci.
2. Otevřete konzoli MMC.
3. V podokně **Služby** zkontrolujte, zda je spuštěna služba platformy importu a exportu dat Microsoft Dynamics 365. Restartujte ji, pokud byla zastavena, protože ji vyžaduje počáteční synchronizace.

## <a name="initial-synchronization-error-403-forbidden"></a>Chyba počáteční synchronizace: 403 zakázáno

Při počáteční synchronizaci se může zobrazit následující chybová zpráva:

*(\[zakázáno\], Vzdálený server vrátil chybu: (403) Zakázáno.), při exportu AX byla zjištěna chyba*

Chcete-li opravit problém, postupujte následovně.

1. Přihlášení do finanční a provozní aplikace.
2. Na stránce **aplikací Azure Active Directory** odstraňte klienta **DtAppID** a poté jej znovu přidejte.

![DtAppID klient v seznamu aplikací Azure AD.](media/aad_applications.png)

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

1. Ve finanční a provozní aplikaci odstraňte sloupce **PrimaryContactPersonId** a **InvoiceVendorAccountNumber** z mapování a pak mapování uložte.

    1. Na stránce mapování s dvojitým zápisem **Vendors V2 (msdyn\_vendors)**, na kartě **Mapování tabulek**, v levém filtru vyberte aplikace **Finanční a provozní aplikace.Vendors V2**. V pravém filtru vyberte **Sales.Vendor**.
    2. Vyhledejte **primarycontactperson** a najděte zdrojový sloupec **PrimaryContactPersonId**.
    3. Vyberte **Akce** a poté vyberte **Odstranit**.

        ![Odstranění sloupce PrimaryContactPersonId.](media/vend_selfref3.png)

    4. Opakujte tyto kroky pro odstranění sloupce **InvoiceVendorAccountNumber**.

        ![Odstranění sloupce InvoiceVendorAccountNumber.](media/vend-selfref4.png)

    5. Uložte změny do mapování.

2. Vypněte sledování změn pro tabulku **Vendors V2**.

    1. V pracovním prostoru **Správa dat** vyberte dlaždici **Datové tabulky**.
    2. Vyberte tabulku **Vendors V2**.
    3. V podokně akcí zvolte **Možnosti** a poté vyberte **Sledování změn**.

        ![Vyberte možnost Sledování změn.](media/selfref_options.png)

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

1. Ve finanční a provozní aplikaci odstraňte sloupce **ContactPersonID** a **InvoiceAccount** z mapování **Customers V3 (accounts)** a mapování uložte.

    1. Na stránce mapování s dvojitým zápisem pro **Customers V3 (accounts)** na kartě **Mapování tabulek** v levém filtru vyberte **Finanční a provozní aplikace.Customers V3**. V pravém filtru vyberte **Dataverse.Account**.
    2. Vyhledejte **contactperson** a najděte zdrojový sloupec **ContactPersonID**.
    3. Vyberte **Akce** a poté vyberte **Odstranit**.

        ![Odstranění sloupce ContactPersonID.](media/cust_selfref3.png)

    4. Opakujte tyto kroky pro odstranění sloupce **InvoiceAccount**.

        ![Odstranění sloupce InvoiceAccount.](media/cust_selfref4.png)

    5. Uložte změny do mapování.

2. Vypněte sledování změn pro tabulku **Customers V3**.

    1. V pracovním prostoru **Správa dat** vyberte dlaždici **Datové tabulky**.
    2. Vyberte tabulku **Zákazníci V3**.
    3. V podokně akcí zvolte **Možnosti** a poté vyberte **Sledování změn**.

        ![Vyberte možnost Sledování změn.](media/selfref_options.png)

    4. Vyberte **Zakázat sledování změn**.

        ![Výběr Zakázat sledování změn.](media/selfref_tracking.png)

3. Spusťte počáteční synchronizaci pro mapování **Customers V3 (Accounts)**. Počáteční synchronizace by měla úspěšně proběhnout bez chyb.
4. Spusťte počáteční synchronizaci pro mapování **CDS Contacts V2 (contacts)**.

    > [!NOTE]
    > Existují dvě mapy se stejným názvem. Vyberte mapu, která má následující popis na kartě **Podrobnosti**: **Šablona s dvojím zápisem pro synchronizaci mezi kontakty dodavatele FO.CDS V2 a CDS.Contacts. Vyžaduje nový balíček \[Dynamics365SupplyChainExtended\].**

5. Přidejte sloupce **InvoiceAccount** a **ContactPersonId** zpět do mapování **Customers V3 (Accounts)** a mapování uložte. Sloupce **InvoiceAccount** i **ContactPersonId** jsou opět součástí živého synchronizačního režimu. V dalším kroku dokončíte počáteční synchronizaci těchto sloupců.
6. Spusťte opět počáteční synchronizaci pro mapování **Customers V3 (Accounts)**. Protože sledování změn je vypnuto, data pro **InvoiceAccount** a **ContactPersonId** budou synchronizována z finanční a provozní aplikace do Dataverse.
7. Chcete-li synchronizovat data pro **InvoiceAccount** a **ContactPersonId** z Dataverse do finanční a provozní aplikace, musíte použít projekt integrace dat.

    1. V Power Apps vytvořte projekt integrace dat mezi tabulkami **Sales.Account** a **Finanční a provozní aplikace.Customers V3**. Směr dat musí být z Dataverse do finanční a provozní aplikace. Protože **InvoiceAccount** je nový atribut v dvojitém zápisu, možná budete chtít přeskočit počáteční synchronizaci pro tento atribut. Další informace naleznete v tématu [Integrace dat do Dataverse](/power-platform/admin/data-integrator).

        Následující ilustrace ukazuje projekt, který aktualizuje **CustomerAccount** a **ContactPersonId**.

        ![Projekt integrace dat pro aktualizaci CustomerAccount a ContactPersonId.](media/cust_selfref6.png)

    2. Přidejte do filtru kritéria společnosti na straně Dataverse, aby byly ve finanční a provozní aplikaci aktualizovány pouze řádky, které odpovídají kritériím filtru. Chcete-li přidat filtr, vyberte tlačítko filtru. Potom v dialogovém okně **Upravit dotaz** můžete přidat dotaz filtru jako **\_msdyn\_company\_value eq '\<guid\>'**.

        > [POZNÁMKA] Pokud tlačítko filtru není k dispozici, vytvořte podpůrný ticket a požádejte tým pro integraci dat o povolení filtrování u klienta.

        Pokud nezadáte dotaz filtru pro **\_msdyn\_company\_value**, budou všechny řádky synchronizovány.

        ![Přidání dotazu filtru.](media/cust_selfref7.png)

    Počáteční synchronizace řádků je nyní dokončena.

8. Ve finanční a provozní aplikaci opět zapněte sledování změn pro tabulku **Customers V3**.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>Počáteční selhání synchronizace na mapách s více než 10 vyhledávacími poli

Může se zobrazit následující chybová zpráva při pokusu o spuštění počátečních selhání synchronizace v mapování **Zákazníci V3 - Účty**, **Prodejní objednávky** nebo jakékoliv mapě s více než 10 vyhledávacími poli:

*CRMExport: Spuštění balíčku dokončeno. Chyba Popis 5 Pokusy o získání dat z https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=numbern account, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$orderby=accountnumber asc failed.*

Z důvodu omezení vyhledávání v dotazu se počáteční synchronizace nezdaří, pokud mapování entit obsahuje více než 10 vyhledávání. Další informace viz [Načíst související záznamy tabulky pomocí dotazu](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

Chcete-li opravit problém, postupujte následovně:

1. Odeberte volitelná vyhledávací pole z mapy entit se dvěma zápisy, aby byl počet vyhledávání 10 nebo méně.
2. Uložte mapu a proveďte počáteční synchronizaci.
3. Když je počáteční synchronizace pro první krok úspěšná, přidejte zbývající vyhledávací pole a odeberte vyhledávací pole, která jste synchronizovali v prvním kroku. Ujistěte se, že počet vyhledávacích polí je 10 nebo méně. Uložte mapu a spusťte počáteční synchronizaci.
4. Opakujte tyto kroky, dokud nebudou synchronizována všechna vyhledávací pole.
5. Přidejte všechna vyhledávací pole zpět na mapu, mapu uložte a spusťte pomocí **Přeskočit počáteční synchronizaci**.

Tento proces povoluje mapu pro režim živé synchronizace.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>Známý problém při počáteční synchronizaci poštovních adres a elektronických elektronických adres

Při pokusu o spuštění počáteční synchronizace poštovních adres strany a elektronických elektronických adres strany se může zobrazit následující chybová zpráva:

*Číslo strany nebylo nalezeno v Dataverse.*

Je nastaven rozsah **DirPartyCDSEntity** ve finanční a provozní aplikaci, který filtruje strany typu **Osoba** a **Organizace**. V důsledku toho počáteční synchronizace mapování **Strany CDS - msdyn_parties** nesynchronizuje strany jiných typů, včetně **Právnická osoba** a **Provozní jednotka**. Když se spustí počáteční synchronizace pro **Poštovní adresy stran CDS (msdyn_partypostaladdresses)** nebo **Kontakty stran V3 (msdyn_partyelectronicaddresses)**, může se zobrazit chyba.

Pracujeme na opravě, která by odstranila rozsah typů stran na entitě Finance a provoz, aby se strany všech typů mohly synchronizovat na Dataverse úspěšně.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Existují nějaké problémy s výkonem při spuštění počáteční synchronizace pro data zákazníků nebo kontaktů?

Pokud jste spustili počáteční synchronizaci pro data **Odběratel** a máte mapy **Odběratel** spuštěné poté se spustí počáteční synchronizace pro data **Kontakty**, mohou nastat problémy s výkonem při vkládání a aktualizacích tabulek **LogisticsPostalAddress** a **LogisticsElectronicAddress** pro adresy **Kontaktů**. Jsou sledovány stejné globální poštovní adresy a tabulky elektronických adres pro **CustCustomerV3Entity** a **VendVendorV2Entity** a duální zápis se pokouší vytvořit více dotazů pro zápis dat na druhou stranu. Pokud jste již spustili počáteční synchronizaci pro **Odběratele**, zastavte odpovídající mapu při spuštění počáteční synchronizace pro data **Kontakty**. Udělejte to samé pro data **Dodavatelů**. Po dokončení počáteční synchronizace můžete spustit všechny mapy přeskočením počáteční synchronizace.

## <a name="float-data-type-that-has-a-zero-value-cant-be-synchronized"></a>Datový typ plovoucí desetinná čárka, který má nulovou hodnotu, nelze synchronizovat

Počáteční synchronizace může selhat u záznamů, které mají pro pole ceny nulovou hodnotu, jako např. **Pevná částka platby** nebo **Množství** v měně transakce. V takovém případě se zobrazí chybová zpráva podobná následujícímu příkladu:

*Při ověřování vstupních parametrů došlo k chybě: Microsoft.OData.ODataException: Nelze převést literál „000000“ na očekávaný typ „Edm.Decimal“,...*

Problém je s hodnotou **Jazykové prostředí** pod **Formáty zdrojových dat** v modulu **Správa dat**. Změňte hodnotu pole **Jazykové prostředí** na **en-us** a pak to zkuste znovu.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


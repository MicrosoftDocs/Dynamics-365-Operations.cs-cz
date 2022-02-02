---
title: Upgrade na model strany a globálního adresáře
description: Toto téma popisuje, jak upgradovat data duálního zápisu na model strany a globálního adresáře.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: eaafe8d98049cb8838317396f28e9d6ca720a677
ms.sourcegitcommit: 08dcbc85e372d4e4fb3ba64389f6d5051212c212
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/20/2022
ms.locfileid: "8015708"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Upgrade na model strany a globálního adresáře

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Šablony Microsoft Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) vám pomůžoz upgradovat následující stávající data v duálním zápisu na model strany a globálního adresáře: **Účet**, **Kontakt** a **Prodejce**.

K dispozici jsou následující tři šablony Data Factory. Pomáhají odsouhlasit data z aplikací Finance a Operace i aplikací Customer Engagement.

- **[Šablona strany](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (Upgradujte data na schéma s dvojím zápisem Party-GAB/arm_template.json)** – Tato šablona pomáhá upgradovat data **Strana** a **Kontakt**, která jsou spojena s daty **Účet**, **Kontakt** a **Prodejce**.
- **[Šablona poštovní adresy strany](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (Upgradujte data na schéma Party-GAB s duálním zápisem/Upgradujte na poštovní adresu strany – GAB/arm_template.json)** – Tato šablona pomáhá upgradovat poštovní adresy, které jsou přidruženy k datům **Účet**, **Kontakt** a **Prodejce**.
- **[Šablona elektronické adresy strany](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (Upgradujte data na schéma Party-GAB s duálním zápisem/Upgradujte na elektronickou adresu strany – GAB/arm_template.json)** – Tato šablona pomáhá upgradovat elektronické adresy, které jsou přidruženy k datům **Účet**, **Kontakt** a **Prodejce**.

Na konci procesu se vygenerují následující soubory s hodnotami oddělenými čárkami (.csv).

| Název souboru | Účel |
|---|---|
| FONewParty.csv | Tento soubor pomáhá vytvářet nové záznamy **Strana** uvnitř aplikace Finance a Operace. |
| ImportFONewPostalAddressLocation.csv | Tento soubor pomáhá vytvářet nové záznamy **Umístění poštovní adresy** v aplikaci Finance a Operace. |
| ImportFONewPartyPostalAddress.csv | Tento soubor pomáhá vytvářet nové záznamy **Poštovní adresa strany** v aplikaci Finance a Operace. |
| ImportFONewPostalAddress.csv | Tento soubor pomáhá vytvářet nové záznamy **Poštovní adresa** v aplikaci Finance a Operace. |
| ImportFONewElectronicAddress.csv | Tento soubor pomáhá vytvářet nové záznamy **Elektronická adresa** v aplikaci Finance a Operace. |

Toto téma vysvětluje, jak používat šablony Data Factory a upgradovat data. Pokud nemáte žádná přizpůsobení, můžete použít šablony tak, jak jsou. Pokud máte přizpůsobení pro data **Účet**, **Kontakt** a **Prodejce**, pak musíte šablonu upravit pomocí pokynů v tomto tématu.

> [!IMPORTANT]
> Pokud budete používat šablony poštovní adresy a elektronické adresy strany, existují zvláštní pokyny. Nejprve musíte spustit šablonu strany, poté šablonu poštovní adresy strany a poté šablonu elektronické adresy strany. Každá šablona je navržena pro import v samostatné datové továrně.

## <a name="prerequisites"></a>Předpoklady

K upgradu na model Strana a Globální adresář musí být splněny následující předpoklady:

+ Musíte mít [Předplatné Azure](https://portal.azure.com/).
+ Musíte mít přístup k [šablonám](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
+ Musíte být stávajícím zákazníkem se dvěma zápisy.

## <a name="prepare-for-the-upgrade"></a>Příprava na upgrade

Upgrade vyžaduje následující přípravu:

+ **Plná synchronizace:** Jak prostředí Finance and operations, tak prostředí Customer Engagement jsou v plně synchronizovaném stavu pro tabulky **Účet (zákazník)**, **Kontakt** a **Prodejce**.
+ **Integrační klíče**: Tabulky **Účet (zákazník)**, **Kontakt** a **Prodejce** v aplikacích Customer Engagement používají integrační klíče, které byly dodány ihned po vybalení. Pokud jste přizpůsobili integrační klíče, musíte přizpůsobit šablonu.
+ **Číslo strany:** Všechny záznamy **Účet (zákazník)**, **Kontakt** a **Prodejce**, které budou upgradovány, mají číslo strany. Záznamy, které nemají číslo strany, budou ignorovány. Chcete-li tyto záznamy upgradovat, přidejte k nim číslo strany, než zahájíte proces upgradu.
+ **Výpadek systému**: Během procesu upgradu budete muset přepnout prostředí Finance and Operations a Customer Engagement offline.
+ **Snímek**: Pořiďte snímek aplikací Finance a Operace i Customer Engagement. Potom, pokud potřebujete, můžete použít snímky k obnovení předchozího stavu.

## <a name="deployment"></a>Nasazení

1. Stáhněte si šablony z [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema).
2. Přihlaste se do [portálu Azure](https://portal.azure.com/).
3. Vytvořte [skupinu prostředků](/azure/azure-resource-manager/management/manage-resource-groups-portal).
4. Vytvořte [účet úložiště](/azure/storage/common/storage-account-create?tabs=azure-portal) ve skupině prostředků, kterou jste vytvořili.
5. Vytvořte [datovou továrnu](/azure/data-factory/quickstart-create-data-factory-portal) ve skupině prostředků, kterou jste vytvořili.
6. Otevřete datovou továrnu a vyberte dlaždici **Autor a monitor**.
7. Na kartě **Spravovat** vyberte **Šablona ARM**.
8. Vyberte **Importovat šablonu ARM** k importování šablony **Strana**.
9. Importujte šablonu do datové továrny. Zadejte následující hodnoty pro **Detaily projektu** a **Podrobnosti instance**.

    | Pole | Hodnota |
    |---|---|
    | Předplatné | Předplatné Azure |
    | Skupina prostředků | Poskytněte stejný prostředek, pod kterým je vytvořen účet úložiště. |
    | Oblast | Oblast |
    | Název továrny | Název továrny |
    | Klíč objektu zabezpečení Service_service spojený s FO | Klíč aplikace |
    | Řetězec Storage_connection Azure Blob | Připojovací řetězec úložiště Azure Blob |
    | Dynamics Crm propojené Service_password | Heslo uživatelského účtu, který jste zadali jako uživatelské jméno. |
    | Service_properties_type Properties_url propojené s FO | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | Service_properties_type Properties_tenant propojené s FO | Údaje o klientovi (název domény nebo ID klienta), pod kterými se vaše aplikace nachází. |
    | Id prostředku Service_properties_type Properties_aad propojené s FO | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | Id objektu zabezpečení Service_properties_type Properties_service propojené s FO | ID klienta aplikace. |
    | Dynamics Crm spojené Service_properties_type Properties_username | Uživatelské jméno použité pro připojení k Dynamics 365. |

    Další informace naleznete v následujících tématech:

    - [Ručně propagujte šablonu Resource Manageru pro každé prostředí](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [Vlastnosti propojené služby](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [Zkopírujte data pomocí Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Po nasazení ověřte datové sady, tok dat a propojenou službu datové továrny.

    ![Datové sady, tok dat a propojená služba.](media/data-factory-validate.png)

11. Přejděte na **Spravovat**. V části **Připojení** vyberte **Propojená služba**. Pak vyberte **DynamicsCrmLinkedService**. V dialogovém okně **Upravit propojenou službu (Dynamics CRM)** zadejte následující hodnoty.

    | Pole | Hodnota |
    |---|---|
    | Název | DynamicsCrmLinkedService |
    | popis | Propojené služby pro připojení k instanci CRM k načtení dat entit |
    | Připojte se pomocí modulu runtime integrace | AutoResolvelntegrationRuntime |
    | Typ nasazení | Online |
    | Uri služby | `https://<organization-name>.crm[x].dynamics.com` |
    | Typ ověření | Office365 |
    | Uživatelské jméno | |
    | Heslo nebo Azure Key Vault | Heslo |
    | Heslo | |

## <a name="prepare-to-run-the-data-factory-templates"></a>Připravte se na spuštění šablon Data Factory

Tato část popisuje nastavení, které je nutné před spuštěním šablony Data Factory Poštovní adresa strany a Elektronická adresa strany.

### <a name="setup-to-run-the-party-postal-address-template"></a>Nastavení pro spuštění šablony Poštovní adresy strany

1. Přihlaste se do aplikací pro zapojení zákazníků a přejděte na **Nastavení** \> **Nastavení přizpůsobení**. Poté na kartě **Všeobecné** nakonfigurujte nastavení časového pásma pro účet správce systému. Časové pásmo musí být v koordinovaném světovém čase (UTC), aby se aktualizovala data „platí od“ a „platí do“ poštovních adres z aplikací Finance a Operace.

    ![Nastavení časového pásma pro účet správce systému.](media/ADF-1.png)

2. V Data Factory, na kartě **Spravovat** pod **Globálními parametry** vytvořte následující globální parametr.

    | Číslo | Název | Typ | Hodnota |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | řetězec | Tento parametr připojuje sériové číslo k nově vytvořeným poštovním adresám jako předponu. Nezapomeňte zadat řetězec, který není v konfliktu s poštovními adresami v aplikacích Finance a Operace a aplikacích Customer Engagement. Na příklad použijte **ADF-PAD-**. |

    ![Globální parametr PostalAddressIdPrefix vytvořený na kartě Spravovat.](media/ADF-2.png)

3. Po dokončení zvolte **Publikovat vše**.

    ![Tlačítko Publikovat vše.](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>Nastavení pro spuštění šablony Elektronické adresy strany

1. V Data Factory, na kartě **Spravovat** pod **Globálními parametry** vytvořte následující globální parametry.

    | Číslo | Název | Typ | Hodnota |
    |---|---|---|---|
    | 1 | IsFOSource | bool | Tento parametr určuje, které primární systémové adresy budou nahrazeny v případě konfliktů. Pokud je hodnota **true**, primární adresy v aplikacích Finance a Operace nahradí primární adresy v aplikacích Customer Engagement. Pokud je hodnota **false**, primární adresy v aplikacích Customer Engagement nahradí primární adresy v aplikacích Finance a Operace. |
    | 2 | ElectronicAddressIdPrefix | řetězec | Tento parametr připojuje sériové číslo k nově vytvořeným elektronickým adresám jako předponu. Nezapomeňte zadat řetězec, který není v konfliktu s elektronickými adresami v aplikacích Finance a Operace a aplikacích Customer Engagement. Na příklad použijte **ADF-EAD-**. |

    ![Globální parametry IsFOSource a ElectronicAddressIdPrefix vytvořené na kartě Spravovat.](media/ADF-4.png)

2. Po dokončení zvolte **Publikovat vše**.

## <a name="run-the-templates"></a>Spusťte šablony

1. Zastavte následující mapy dvojitého zápisu **Účet**, **Kontakt** a **Prodejce**, které využívají aplikaci Finance a Operace:

    + Zákazníci V3 (accounts)
    + Zákazníci V3(kontakty)
    + Kontakty CDS V2(kontakty)
    + Kontakty CDS V2(kontakty)
    + Dodavatel V2 (msdyn_vendor)

2. Ujistěte se, že jsou mapy odstraněny z tabulky **msdy_dualwriteruntimeconfig** v Dataverse.
3. Nainstalujte [řešení strany a globálního adresáře s duálním zápisem](https://aka.ms/dual-write-gab) z AppSource.
4. V aplikaci Finance a Operace spusťte **Počáteční synchronizaci** pro následující tabulky, pokud obsahují data.

    + Oslovení
    + Typy osobní charakteristiky
    + Zdvořilostní zakončení
    + Tituly kontaktní osoby
    + Role v rozhodovacím procesu
    + Úrovně věrnosti

5. V aplikaci pro zapojení zákazníků deaktivujte následující kroky pluginu:

    + Aktualizace účtu

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualizace účtu
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualizace účtu

    + Aktualizace kontaktu

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualizace kontaktu
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualizace kontaktu

    + Aktualizace msdyn_party

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualizace msdyn_party

    + Aktualizace msdyn_vendor

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualizace msdyn_vendor

    + Customeraddress

        + Vytvořit

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Vytvoření customeraddress

        + Aktualizovat

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: Aktualizace customeraddress

        + Odstranit

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: Odstranění customeraddress

    + msdyn_partypostaladdress

        + Vytvořit

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Vytvoření msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Vytvoření msdyn_partypostaladdress

        + Aktualizovat

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Aktualizace msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Aktualizace msdyn_partypostaladdress

    + msdyn_postaladdress

        + Vytvořit

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Vytvoření msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Vytvoření of msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Vytvoření msdyn_postaladdress

        + Aktualizovat

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Aktualizace msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Aktualizace msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + Vytvořit

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Vytvoření msdyn_partyelectronicaddress

        + Aktualizovat

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Aktualizace msdyn_partyelectronicaddress

        + Odstranit

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Odstranění msdyn_partyelectronicaddress

6. V aplikaci pro zapojení zákazníků deaktivujte následující pracovní postupy:

    + Vytvoření dodavatelů v tabulce Účty
    + Vytvoření dodavatelů v tabulce Účty
    + Vytvoření dodavatelů typu Osoba v tabulce Kontakty
    + Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé
    + Aktualizace dodavatelů v tabulce Účty
    + Aktualizace dodavatelů v tabulce Dodavatelé
    + Aktualizace dodavatelů typu Osoba v tabulce Kontakty
    + Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé

7. V datové továrně spusťte šablonu výběrem **Spustit hned**, jak je znázorněno na následující ilustraci. V závislosti na objemu dat může tento proces trvat několik hodin.

    ![Spuštění šablony.](media/data-factory-trigger.png)

    > [!NOTE]
    > Pokud máte přizpůsobení pro **Účet**, **Kontakt** a **Prodejce**, musíte šablonu upravit.

8. Importujte nové záznamy **Strana** do aplikace Finance a Operace.

    1. Stáhněte si soubor **FONewParty.csv** z úložiště Azure Blob. Cesta je **partybootstrapping/output/FONewParty.csv**.
    2. Převeďte soubor **FONewParty.csv** do souboru Excel a importujte soubor Excel do aplikace Finance a Operace. Případně, pokud vám CSV import vyhovuje, můžete soubor .csv importovat přímo. V závislosti na objemu dat může tento krok trvat několik hodin. Další informace naleznete v tématu [Přehled úloh importu a exportu dat](../data-import-export-job.md).

    ![Import záznamů Strany Dataverse.](media/data-factory-import-party.png)

9. V datové továrně spusťte šablony Poštovní adresy strany a Elektronické adresy strany jednu po druhé.

    + Šablona Poštovní adresy strany vloží všechny záznamy poštovní adresy v aplikaci pro zapojení zákazníků a přiřadí je k odpovídajícím záznamům **Účet**, **Kontakt** a **Prodejce**. Vygeneruje také tři soubory .csv: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv a ImportFONewPostalAddress.csv.
    + Šablona Eletronické adresy strany vloží všechny záznamy elektronických adres v aplikaci pro zapojení zákazníků a přiřadí je k odpovídajícím záznamům **Účet**, **Kontakt** a **Prodejce**. Vygeneruje také jeden soubor .csv: ImportFONewElectronicAddress.csv.

    ![Spouštění šablon Poštovní adresy strany a Elektronické adresy strany.](media/ADF-7.png)

10. Chcete-li aktualizovat aplikace Finance a Operace s těmito daty, musíte převést soubory .csv do sešitu aplikace Excel a [importovat jej do aplikace Finance and Operations](/data-entities/data-import-export-job). Případně, pokud vám CSV import vyhovuje, můžete soubory .csv importovat přímo. V závislosti na objemu může tento krok trvat několik hodin.

    ![Úspěšný import.](media/ADF-8.png)

11. V aplikaci pro zapojení zákazníků aktivujte následující kroky pluginu:

    + Aktualizace účtu

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualizace účtu
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualizace účtu

    + Aktualizace kontaktu

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualizace kontaktu
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualizace kontaktu

    + Aktualizace msdyn_party

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualizace msdyn_party

    + Aktualizace msdyn_vendor

        + Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualizace msdyn_vendor

    + msdyn_partypostaladdress

        + Vytvořit

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Vytvoření msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Vytvoření msdyn_partypostaladdress

        + Aktualizovat

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: Aktualizace msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: Aktualizace msdyn_partypostaladdress

    + msdyn_postaladdress

        + Vytvořit

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: Vytvoření msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: Vytvoření of msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Vytvoření msdyn_postaladdress

        + Aktualizovat

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: Aktualizace msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: Aktualizace msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + Vytvořit

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Vytvoření msdyn_partyelectronicaddress

        + Aktualizovat

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: Aktualizace msdyn_partyelectronicaddress

        + Odstranit

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: Odstranění msdyn_partyelectronicaddress

12. V aplikaci pro zapojení zákazníků aktivujte následující pracovní postupy, pokud jste je předtím deaktivovali:

    + Vytvoření dodavatelů v tabulce Účty
    + Vytvoření dodavatelů v tabulce Účty
    + Vytvoření dodavatelů typu Osoba v tabulce Kontakty
    + Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé
    + Aktualizace dodavatelů v tabulce Účty
    + Aktualizace dodavatelů v tabulce Dodavatelé
    + Aktualizace dodavatelů typu Osoba v tabulce Kontakty
    + Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé

13. Spusťte mapy související se záznamy **Strany** podle pokynů v části [Strana a globální adresář](party-gab.md).

## <a name="explanation-of-the-data-factory-templates"></a>Vysvětlení šablon Data Factory

Tato část vás provede kroky v každé šabloně Data Factory.

### <a name="steps-in-the-party-template"></a>Kroky v šabloně Strany

1. Kroky 1 až 6 identifikují společnosti, které mají povolený dvojí zápis, a vytvoří pro ně klauzuli filtru.
2. Kroky 7-1 až 7-9 načítají data z aplikace Finance a Operace a aplikace Customer Engagement a připraví tato data pro upgrade.
3. Kroky 8 až 9 porovnají číslo strany pro záznamy **Účet**, **Kontakt** a **Prodejce** mezi aplikacemi Finance a Operace a aplikacemi Customer Engagement. Všechny záznamy, které nemají číslo strany, budou přeskočeny.
4. Krok 10 vygeneruje dva soubory .csv pro záznamy strany, které je třeba vytvořit v aplikaci Customer Engagement a v aplikaci Finance a Operace.

    - **FOCDSparty.csv** – Tento soubor obsahuje všechny záznamy stran obou systémů bez ohledu na to, zda má společnost povolen duální zápis.
    - **FONewParty.csv** – Tento soubor obsahuje dílčí sadu záznamů strany, kterých si je Dataverse vědom (například účty typu **Potenciální zákazník**).

5. Krok 11 vytvoří strany v aplikaci Customer Engagement.
6. Krok 12 načte globálně jedinečné identifikátory (GUID) stran z aplikace pro zapojení zákazníků a nastaví je tak, aby je bylo možné spojit se záznamy **Účet**, **Kontakt** a **Prodejce** následných krocích.
7. Krok 13 přidružuje záznamy **Účet**, **Kontakt** a **Prodejce** s GUID strany.
8. Kroky 14-1 až 14-3 aktualizují záznamy **Účet**, **Kontakt** a **Prodejce** v aplikaci pro zapojení zákazníků s GUID strany.
9. Kroky 15-1 až 15-3 připravují záznamy **Kontakt pro stranu** pro záznamy **Účet**, **Kontakt** a **Prodejce**.
10. Kroky 16-1 až 16-7 načítají referenční data, jako jsou pozdravy a typy osobní charakteristiky, a přidružují je k záznamům **Kontakt pro stranu**.
11. Kroky 17 sloučí záznamy **Kontakt pro stranu** pro záznamy **Účet**, **Kontakt** a **Prodejce**.
12. Krok 18 importuje záznamy **Kontakt pro stranu** do aplikace pro zapojení zákazníků.

### <a name="steps-in-the-party-postal-address-template"></a>Kroky v šabloně Poštovní adresa strany

1. Kroky 1-1 až 1-10 načítají data z aplikace Finance a Operace a aplikace Customer Engagement a připraví tato data pro upgrade.
2. Krok 2 denormalizuje data poštovní adresy v aplikaci Finance a Operace spojením poštovní adresy a poštovní adresy strany.
3. Krok 3 odstraní duplicitu a sloučí údaje o adrese účtu, kontaktu a dodavatele z aplikace pro zapojení zákazníků.
4. Krok 4 vytvoří soubory .csv pro aplikaci Finance a Operace k vytvoření nových údajů o adrese založených na adresách účtu, kontaktu a prodejce.
5. Krok 5-1 vytvoří soubory .csv pro aplikaci pro zapojení zákazníků, aby se vytvořila všechna data adres na základě aplikace Finance a Operace a aplikace pro zapojení zákazníků.
6. Krok 5-2 převede soubory .csv na formát importu Finance and Operations pro ruční import.

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. Krok 6 importuje data kolekce poštovních adres do aplikace pro zapojení zákazníků.
8. Krok 7 načte data kolekce poštovních adres z aplikace pro zapojení zákazníků.
9. Krok 8 vytvoří údaje o adrese zákazníka a přiřadí ID kolekce poštovních adres.
10. Kroky 9-1 až 9-2 přidruží ID kolekce strany a poštovních adres k poštovním adresám a poštovním adresám stran.
11. Kroky 10-1 až 10-3 importují adresy zákazníků, poštovní adresy a poštovní adresy stran do aplikace pro zapojení zákazníků.

### <a name="steps-in-the-party-electronic-address-template"></a>Kroky v šabloně Elektronická adresa strany

1. Kroky 1-1 až 1-5 načítají data z aplikace Finance a Operace a aplikace Customer Engagement a připraví tato data pro upgrade.
2. Krok 2 konsoliduje elektronické adresy v aplikaci pro zapojení zákazníků z entit účet, kontakt a dodavatel.
3. Krok 3 sloučí data primární elektronické adresy z aplikace pro zapojení zákazníků a aplikace Finance a Operace.
4. Krok 4 vytvoří soubory .csv.

    - Vytvořte nové údaje elektronické adresy pro aplikaci Finance a Operace na základě adres účet, kontakt a dodavatel.
    - Vytvořte nová data elektronické adresy pro aplikaci pro zapojení zákazníků na základě elektronické adresy, účtu, kontaktních adres a adres prodejců a aplikaci Finance a Operace.

5. Krok 5-1 importuje elektronické adresy do aplikace pro zapojení zákazníků.
6. Krok 5-2 vytvoří soubory .csv pro aktualizaci primárních adres pro účty a kontakty v aplikaci pro zapojení zákazníků.
7. Kroky 6-1 až 6-2 importují účty a primární kontaktní adresy do aplikace pro zapojení zákazníků.

## <a name="troubleshooting"></a>Řešení potíží

1. Pokud proces selže, spusťte znovu datovou továrnu. Začněte aktivitou, která selhala.
2. Některé soubory, které generuje datová továrna, lze použít pro ověření dat.
3. Datová továrna běží na základě souborů .csv. Pokud je tedy v libovolné hodnotě pole uvedena čárka, může to ovlivnit výsledky. Z hodnot polí musíte odstranit všechny čárky.
4. Karta **Monitorování** poskytuje informace o všech krocích a datech, která byla zpracována. Vyberte konkrétní krok k ladění.

    ![Záložka Monitorování.](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Další informace o šabloně

Další informace o šabloně najdete v [Komentářích k readme šablony Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).

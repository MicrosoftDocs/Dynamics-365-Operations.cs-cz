---
title: Upgrade na model strany a globálního adresáře
description: Toto téma popisuje, jak upgradovat data duálního zápisu na model strany a globálního adresáře.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857363"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>Upgrade na model strany a globálního adresáře

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[Šablona Azure Data Factory](https://aka.ms/dual-write-gab-adf) vám pomůže upgradovat stávající data tabulek **Účet**, **Kontakt** a **Prodejce** v duálním zápisu na model strany a globálního adresáře. Šablona odsouhlasí data z aplikací Finance and Operations i aplikací pro zapojení zákazníků. Na konci procesu budou pole **Strana** a **Kontakt** záznamy **Strana** vytvořeny a přidruženy k záznamům **Účet**, **Kontakt** a **Prodejce** v aplikacích pro zapojení zákazníků. Soubor CSV (`FONewParty.csv`) je generován k vytvoření nových záznamů **Strana** uvnitř aplikace Finance and Operations. Toto téma obsahuje pokyny k použití šablony Data Factory a upgradu dat.

Pokud nemáte žádná přizpůsobení, můžete použít šablonu tak, jak je. Pokud máte přizpůsobení pro **Účet**, **Kontakt** a **Prodejce**, pak musíte šablonu upravit pomocí následujících pokynů.

> [!Note]
> Šablona pomáhá upgradovat pouze data **Strana**. V budoucím vydání budou zahrnuty poštovní a elektronické adresy.

## <a name="prerequisites"></a>Předpoklady

Jsou zapotřebí následující předpoklady:

+ [Předplatné Azure](https://portal.azure.com/)
+ [Přístup k šabloně](https://aka.ms/dual-write-gab-adf)
+ Jste stávajícím zákazníkem se dvěma zápisy.

## <a name="prepare-for-the-upgrade"></a>Příprava na upgrade

+ **Plně synchronizované**: Obě prostředí jsou plně synchronizovaná pro **Účet (zákazník)**, **Kontakt** a **Prodejce**.
+ **Integrační klíče**: Tabulky **Účet (zákazník)**, **Kontakt** a **Prodejce** v aplikacích pro zapojení zákazníků používají integrační klíče, které byly dodány ihned po vybalení. Pokud jste přizpůsobili integrační klíče, musíte přizpůsobit šablonu.
+ **Číslo strany**: Všechny záznamy **Účet (zákazník)**, **Kontakt** a **Prodejce**, které budou upgradovány, mají číslo **Strana**. Záznamy bez čísla **Strana** budou ignorovány. Chcete-li tyto záznamy upgradovat, přidejte k nim číslo **Strana**, než zahájíte proces upgradu.
+ **Výpadek systému**: Během procesu upgradu budete muset přepnout prostředí Finance and Operations i prostředí zapojení zákazníků offline.
+ **Snímek** : Pořiďte snímky aplikací Finance and Operations i zapojení zákazníků. Pokud potřebujete, použijte snímky k obnovení předchozího stavu.

## <a name="deployment"></a>Nasazení

1. Stáhněte si šablonu z [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).

2. Přihlásit se k aplikaci [Microsoft Azure](https://portal.azure.com/).

3. Vytvořte [skupinu prostředků](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).

4. Vytvořte [účet úložiště](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) ve skupině prostředků, kterou jste vytvořili.

5. Vytvořte [datovou továrnu](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) ve výše uvedené skupině prostředků, kterou jste vytvořili.

6. Otevřete datovou továrnu a vyberte dlaždici **Autor a monitor**.

7. Na kartě **Spravovat** vyberte **Šablona ARM**.

8. Vyberte **Importovat šablonu ARM** k importování šablony **Strana**.

9. Importujte šablonu do datové továrny. Zadejte následující hodnoty pro **Detaily projektu** a **Podrobnosti instance**.

    Pole | Hodnota
    ---|---
    Předplatné | Předplatné Azure
    Skupina prostředků | Poskytněte stejný prostředek, pod kterým je vytvořen účet úložiště.
    Oblast | Zadejte region.
    Název továrny | Zadejte název továrny.
    Klíč objektu zabezpečení Service_service spojený s FO | Zadejte klíč aplikace.
    Řetězec Storage_connection Azure Blob | Řetězec připojení Azure Blob Storage.
    Dynamics Crm propojené Service_password | Heslo uživatelského účtu, který jste zadali jako uživatelské jméno.
    Service_properties_type Properties_url propojené s FO  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    Service_properties_type Properties_tenant propojené s FO | Zadejte údaje o klientovi (název domény nebo ID tenanta), pod kterými se vaše aplikace nachází.
    Id prostředku Service_properties_type Properties_aad propojené s FO | `https://sampledynamics.sandboxoperationsdynamics.com`
    Id objektu zabezpečení Service_properties_type Properties_service propojené s FO | Zadejte ID klienta aplikace.
    Dynamics Crm spojené Service_properties_type Properties_username | Uživatelské jméno pro připojení k Dynamics.

    Další informace viz [Ruční propagace šablony Resource Manageru pro každé prostředí](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Vlastnosti propojené služby](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties) a [Kopírování dat pomocí Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. Po nasazení ověřte datové sady, tok dat a propojenou službu datové továrny.

   ![Datové sady, tok dat a propojená služba](media/data-factory-validate.png)

11. Přejděte na **Spravovat**. V části **Připojení** vyberte **Propojená služba**. Vyberte **DynamicsCrmLinkedService**. Ve formuláři **Upravit propojenou službu (Dynamics CRM)** zadejte následující hodnoty:

    Pole | Hodnota
    ---|---
    Jméno | DynamicsCrmLinkedService
    popis | Propojené služby pro připojení k instanci CRM k načtení dat entit
    Připojte se pomocí modulu runtime integrace | AutoResolvelntegrationRuntime
    Typ nasazení | Online
    Uri služby | `https://<organization-name>.crm[x].dynamics.com`
    Typ ověření | Office365
    Uživatelské jméno |
    Heslo nebo Azure Key Vault | Heslo
    Heslo |

## <a name="run-the-template"></a>Spusťte šablonu

1. Zastavte následující dvojitý zápis **Účet**, **Kontakt** a **Prodejce** pomocí aplikace Finance and Operations.

    + Zákazníci V3 (accounts)
    + Zákazníci V3(kontakty)
    + Kontakty CDS V2(kontakty)
    + Kontakty CDS V2(kontakty)
    + Dodavatel V2 (msdyn_vendor)

2. Ujistěte se, že jsou mapy odstraněny z tabulky `msdy_dualwriteruntimeconfig` v Dataverse.

3. Nainstalujte [řešení strany a globálního adresáře s duálním zápisem](https://aka.ms/dual-write-gab) z AppSource.

4. V aplikaci Finance and Operations, pokud následující tabulky obsahují data, pak pro ně spusťte **Počáteční synchronizaci**.

    + Oslovení
    + Typy osobní charakteristiky
    + Zdvořilostní zakončení
    + Tituly kontaktní osoby
    + Role v rozhodovacím procesu
    + Úrovně věrnosti

5. V aplikaci pro zapojení zákazníků deaktivujte následující kroky pluginu.

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

6. V aplikaci pro zapojení zákazníků deaktivujte následující pracovní postupy:

    + Vytvoření dodavatelů v tabulce Účty
    + Vytvoření dodavatelů v tabulce Účty
    + Vytvoření dodavatelů typu Osoba v tabulce Kontakty
    + Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé
    + Aktualizace dodavatelů v tabulce Účty
    + Aktualizace dodavatelů v tabulce Dodavatelé
    + Aktualizace dodavatelů typu Osoba v tabulce Kontakty
    + Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé

7. V datové továrně spusťte šablonu výběrem **Spustit hned**, jak je znázorněno na následujícím obrázku. V závislosti na objemu dat může tento proces trvat několik hodin.

    ![Spustit běh](media/data-factory-trigger.png)

    > [!NOTE]
    > Pokud máte přizpůsobení pro **Účet**, **Kontakt** a **Prodejce**, pak musíte šablonu upravit.

8. Importujte nové záznamy **Strana** v aplikaci Finance and Operations.

    + Stáhněte si soubor `FONewParty.csv` z úložiště Azure blob. Cesta je `partybootstrapping/output/FONewParty.csv`.
    + Převeďte soubor `FONewParty.csv` do souboru Excel a importujte soubor Excel do souboru aplikace Finance and Operations.  Pokud vám csv import vyhovuje, můžete soubor csv importovat přímo. Import může trvat několik hodin, v závislosti na objemu dat. Další informace naleznete v tématu [Přehled úloh importu a exportu dat](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).

    ![Importování záznamů strany Datavers](media/data-factory-import-party.png)

9. V aplikaci pro zapojení zákazníků aktivujte následující kroky pluginu:

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

10. V aplikacích pro zapojení zákazníků aktivujte následující pracovní postupy, pokud jste je deaktivovali v předchozích krocích:

    + Vytvoření dodavatelů v tabulce Účty
    + Vytvoření dodavatelů v tabulce Účty
    + Vytvoření dodavatelů typu Osoba v tabulce Kontakty
    + Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé
    + Aktualizace dodavatelů v tabulce Účty
    + Aktualizace dodavatelů v tabulce Dodavatelé
    + Aktualizace dodavatelů typu Osoba v tabulce Kontakty
    + Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé

11. Spusťte mapy související se **stranou** podle pokynů v části [Strana a globální adresář](party-gab.md).

## <a name="troubleshooting"></a>Řešení potíží

1. V procesu selže, spusťte znovu továrnu dat počínaje neúspěšnou aktivitou.
2. Některé soubory generuje datová továrna, kterou můžete použít pro účely ověření dat.
3. Datová továrna běží na základě souborů CSV, které jsou odděleny čárkami. Pokud existuje hodnota pole s čárkou, může to ovlivnit výsledky. Musíte odstranit čárky.
4. Karta **Monitorování** poskytuje informace o všech krocích a zpracovaných datech. Vyberte konkrétní krok k ladění.

    ![Záložka Monitorování](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>Další informace o šabloně

Komentáře k šabloně najdete v souboru [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).
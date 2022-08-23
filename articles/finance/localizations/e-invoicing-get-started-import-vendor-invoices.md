---
title: Použití služby elektronické fakturace k importu faktur dodavatele
description: Tento článek poskytuje informace o tom, jak importovat faktury dodavatele pomocí služby elektronické fakturace.
author: gionoder
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: c98f33345b37a72c4099f01e37c82e27002ac687
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283138"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Použití služby elektronické fakturace k importu faktur dodavatele

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tento článek poskytuje informace, které vám pomohou začít s iportem faktur dodavatele pomocí služby elektronické fakturace. Provede vás kroky konfigurace v Regulatory Configuration Services (RCS), Dynamics 365 Finance a Dynamics 365 Supply Chain Management, které musíte dodržovat, abyste mohli přijímat elektronické faktury od dodavatelů.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Nastavení importu faktur dodavatele v RCS
Chcete -li nastavit import faktury dodavatele v RCS, postupujte takto:

1. Nahlédněte do seznamu [obecně dostupných funkcí elektronické fakturace](e-invoicing-configuration-rcs.md#generally-available-features).
2. Vyberte a importujte funkci elektronické fakturace, kterou jste vytvořili. Další informace naleznete v části [Importujte funkci elektronické fakturace od poskytovatele konfigurace společnosti Microsoft](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider)
3. Vytvořte funkce elektronické fakturace pro svou organizaci. Další informace naleznete v části [Vytvoření funkce elektronické fakturace u poskytovatele organizace](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider)

## <a name="configure-an-email-account-channel"></a>Konfigurace kanálu e-mailového účtu

Pokud vámi vytvořená funkce elektronické fakturace importuje faktury elektronických dodavatelů z připojených souborů, které jsou přijímány e-mailem, nakonfigurujte kanál e-mailového účtu.

1. V RCS vyberte funkci elektronické fakturace, kterou jste vytvořili. Ujistěte se, že jste vybrali verzi se stavem **Koncept**.
2. Na kartě **Nastavení** v mřížce vyberte nastavení funkce a poté vyberte **Upravit**.
3. Na kartě **Datový kanál** ve skupině polí **Parametry** v poli **Datový kanál** zadejte název kanálu. Název kanálu by neměl mít více než deset znaků.
4. Do pole **Adresa serveru** zadejte poskytovatele e-mailového účtu. Například adresa serveru pro **https://outlook.live.com/** je **imap-mail.outlook.com**.
5. V poli **Port serveru** zadejte port používaný poskytovatelem e-mailového účtu. Například port serveru pro **https://outlook.live.com/** je **993**.
6. V poli **Tajný kód jména uživatele** zadejte název tajného kódu trezoru klíčů, který obsahuje ID uživatelského účtu e-mailu. Tento tajný kód musí být vytvořen v trezoru klíčů Azure a nastaven v prostředí vaší služby. 
7. V poli **Tajný kód hesla uživatele** zadejte název tajného kódu trezoru klíčů, který obsahuje heslo uživatelského účtu e-mailu.
8. Volitelné - zadejte hodnoty do pole **Z filtru**, **Filtr předmětu** a **Datový filtr**.
9. Zadejte názvy složek poštovní schránky, kde budou e -maily:

    - Importováno z: **Hlavní složka**
    - Po úspěšném zpracování uloženo: **Složka archivu**
    - Uloženo po neúspěšném zpracování: **Složka s chybou** Tyto složky nemusíte vytvářet v poštovní schránce. Složky se vytvoří automaticky po prvním importu a zpracování elektronické faktury. 
   
10. Ve skupině polí **Filtr příloh** přidejte informace o filtrování souborů. Zpracují se pouze přílohy, které splňují definovaný filtr. Můžete například nastavit „\*.xml"pro přílohy s příponou xml. Název přílohy se používá v Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management během instalace. 
11. Na kartě **Pravidla použitelnosti** v případě potřeby zkontrolujte a aktualizujte kritéria. Pole **Kanál** se musí rovnat **kanálu dat** poskytnutému předtím. Další informace naleznete v tématu [Pravidla použitelnosti](e-invoicing-configuration-rcs.md#applicability-rules).
12. Zvolte **Uložit** a zavřete stránku.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Konfigurace kanálu Microsoft SharePoint

Konfigurujte kanál Microsoft SharePoint, pokud funkce elektronické fakturace importuje elektronické faktury dodavatele ze souborů umístěných ve složkách SharePoint.

1. V RCS vyberte funkci elektronické fakturace, kterou jste vytvořili. Ujistěte se, že jste vybrali **verzi** se stavem **Koncept**.
2. Na kartě **Nastavení** v mřížce vyberte nastavení funkce a poté vyberte **Upravit**.
3. Na kartě **Datový kanál** ve skupině polí **Parametry** vyberte **Adresa SharePoint** a zadejte URL adresu SharePointu.
4. Vyberte **Port serveru** a zadejte port používaný poskytovatelem e-mailového účtu.
5. Vyberte **ID aplikace** a zadejte název tajného kódu trezoru klíčů, který obsahuje ID klienta SharePointu.
6. Vyberte **Tajný kód aplikace** a zadejte název tajného kódu trezoru klíčů, který obsahuje heslo klienta SharePointu.
7. Vyberte **Filtr souboru**. Zkontrolujte a aktualizujte masku a filtrujte soubory, které obsahují elektronickou fakturu dodavatele k importu.
8. Na kartě **Pravidla použitelnosti** v případě potřeby zkontrolujte a aktualizujte kritéria. Další informace naleznete v tématu [Pravidla použitelnosti](e-invoicing-configuration-rcs.md#applicability-rules).
9. Zvolte **Uložit** a zavřete stránku.

### <a name="deploy-an-electronic-invoicing-feature"></a>Nasazení funkce elektronické fakturace

Informace o nasazení funkce elektronické fakturace najdete v části [Nasazení funkce elektronické fakturace do prostředí služby](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-or-supply-chain-management"></a>Nastavení importu faktury dodavatele ve Finance a Supply Chain Management
Dokončete kroky v následujících dvou částech a nastavte různé typy importu faktur dodavatele.

### <a name="import-brazilian-nf-e-from-email"></a>Import brazilského NF-e z e-mailu

1. Přihlaste se k prostředí Finance nebo Supply Chain Management a ověřte si, že jste ve správné právnické osobě.
2. Přejděte na **Správa organizace** > **Nastavení** > **Parametry elektronického dokumentu**.
3. Na kartě **Funkce** se ujistěte, že je vybráno **NF -e Federal - brazilská elektronická faktura**.
4. Na kartě **Externí kanály** ve skupině polí **Kanály** vyberte **Přidat**.
5. V poli **Kanál** zadejte **NFe** (název kanálu je uveden v konfiguraci datového kanálu pro funkci elektronické fakturace v RCS).
6. Zadejte popis do pole **Popis**. V poli **Společnost** zvolte právnickou osobu.
7. V poli **Kontext dokumentu** vyberte **Kontext fiskálního dokumentu - Kontextový model faktury zákazníka**.
8. Ve skupině polí **Importovat zdroje** vyberte **Přidat**.
9. V poli **Název** zadejte **XmlFile** (název **filtru přílohy** je uveden v konfiguraci datového kanálu pro funkci elektronické fakturace v RCS).
10. V poli **Popis** zadejte popis a do pole **Název datové entity** vyberte **Přijaté dokumenty XML NF-e**.
11. V poli **Mapování modelu** vyberte **Import e-mailů NF - import e-mailů NF-e (BR)** a poté vyberte **Uložit**.
12. Na kartě **Elektronický dokument** ve skupině polí **Elektronické výkaznictví** vyberte možnost **Přidat** a v poli **Název tabulky** vyberte **Přijatý dokument XML NF-e**.
13. V poli **Kontext dokumentu** vyberte **Dotaz na kontext fiskálního dokumentu - Kontext faktury zákazníka**.
14. V poli **Mapování modelu elektronického dokumentu** vyberte **Dotaz na mapování - Mapování fiskálních dokumentů**.
15. Vyberte **Typy odpovědí** a poté vyberte **Nový**.
16. V poli **Typ odezvy** zadejte **Odpověď**. V poli **Stav odeslání** zadejte **Plánováno**.
17. V poli **Mapování modelů** vyberte **Mapování modelu ze zprávy odpovědi - Formát importu zprávy odpovědi**.
18. Zvolte **Uložit** a pak zavřete stránku.

### <a name="import-peppol-electronic-vendor-invoices"></a>Import elektronických faktur dodavatele PEPPOL

1. Přejděte do pracovního prostoru **Elektronické výkaznictví** a vyberte **Konfigurace výkaznictví**.
2. Vyberte **Kontextový model zákaznické faktury** a pak vyberte **Vytvořit konfiguraci** > **Odvozeno z názvu: kontextový model faktury zákazníka, Microsoft** k vytvoření odvozené konfigurace.
3. Ve verzi **Koncept** vyberte **Návrhář** a ve stromu **Datový model** vyberte **Mapovat model na zdroj dat**.
4. Ve stromu **Definice** vyberte **DataChannel** a poté vyberte **Návrhář**.
5. Ve stromu **Zdroj dat** rozbalte kontejner **$Context\_Channel**. V poli **Hodnota** vyberte **Upravit** a zadejte název datového kanálu. Jedná se o název kanálu zadaný v konfiguraci datového kanálu pro funkci elektronického výkaznictví v RCS. 
7. Zvolte **Uložit** a zavřete stránku.
8. Zavřete stránku.
9. Vyberte odvozenou konfiguraci, kterou jste právě vytvořili, z pole **Kontextový model zákaznické faktury** a na záložce s náhledem **Verze** vyberte **Změnit stav** > **Dokončeno**.
10. Jděte na **Správa organizace** > **Nastavení** > **Parametry elektronického dokumentu** a na kartě **Funkce** se ujistěte, že je vybrána možnost **Globální elektronické faktury PEPPOL**. 
11. Na kartě **Externí kanály** v poli **Kanály** vyberte **Přidat**.
12. Do pole **Kanál** zadejte název datového kanálu a do pole **Popis** zadejte popis.
13. V poli **Společnost** zvolte právnickou osobu. 
14. V poli **Kontext dokumentu** vyberte novou odvozenou konfiguraci **Kontextový model zákaznické faktury**. Popis mapování by měl být **Kontext datového kanálu**.
15. Ve skupině polí **Importovat zdroje** vyberte **Přidat**.
16. Do pole **název** zadejte pole **Název filtru příloh** a v poli **Název datové entity** vyberte **Záhlaví faktury dodavatele**.
17. V poli **Mapování modelu** vyberte **Tisk faktury dodavatele - Import faktury dodavatele**.
18. Klikněte na tlačítko **Uložit** a pak zavřete stránku.


## <a name="receive-electronic-invoices"></a>Přijetí elektronických faktur

Služba elektronické fakturace provádí během importu faktur z datových kanálů dva kroky:

1. Přistupuje k poštovní schránce a čte e-maily.
2. Zpracovává e -maily. 
    
Chcete -li provést tyto dva kroky, klient by měl službu volat pro každý krok ručně. Doporučujeme však nastavit dávku pro příjem elektronických dokumentů.

Chcete-li přijímat elektronické faktury, postupujte takto:

1. Přejděte na **Správa organizace** > **Periodické** > **Elektronické dokumenty** > **Přijímat elektronické dokumenty**.
2. Zvolte **KO** a pak zavřete stránku.


## <a name="view-receive-logs-for-electronic-invoices"></a>Zobrazení protokolů příjmu elektronických faktur

Chcete-li zobrazit protokoly příjmu elektronických faktur, přejděte na **Správa organizace** > **Periodické** > **Elektronické dokumenty** > **Protokol o přijetí elektronického dokumentu**.
Pokud nevidíte úspěšně zpracované faktury, odeberte filtr tabulky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

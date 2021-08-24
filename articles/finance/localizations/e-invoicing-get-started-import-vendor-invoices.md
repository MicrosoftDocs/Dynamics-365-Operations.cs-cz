---
title: Použití služby elektronické fakturace k importu faktur dodavatele
description: Toto téma poskytuje informace o tom, jak importovat faktury dodavatele pomocí služby elektronické fakturace.
author: gionoder
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751245"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Použití služby elektronické fakturace k importu faktur dodavatele

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Toto téma poskytuje informace, které vám pomohou začít s iportem faktur dodavatele pomocí služby elektronické fakturace. Provede vás kroky konfigurace v Regulatory Configuration Services (RCS), Dynamics 365 Finance a Dynamics 365 Supply Chain Management, které musíte dodržovat, abyste mohli přijímat elektronické faktury od dodavatelů.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Nastavení importu faktur dodavatele v RCS
Chcete -li nastavit import faktury dodavatele v RCS, postupujte takto:

1. Nahlédněte do seznamu [obecně dostupných funkcí elektronické fakturace](e-invoicing-configuration-rcs.md#generally-available-features).
2. Vyberte a importujte funkci elektronické fakturace, kterou jste vytvořili. Další informace naleznete v části [Importujte funkci elektronické fakturace od poskytovatele konfigurace společnosti Microsoft](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider)
3. Vytvořte funkce elektronické fakturace pro svou organizaci. Další informace naleznete v části [Vytvoření funkce elektronické fakturace u poskytovatele organizace](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider)

## <a name="configure-an-email-account-channel"></a>Konfigurace kanálu e-mailového účtu

Pokud vámi vytvořená funkce elektronické fakturace importuje faktury elektronických dodavatelů z připojených souborů, které jsou přijímány e-mailem, nakonfigurujte kanál e-mailového účtu.

1. V RCS vyberte funkci elektronické fakturace, kterou jste vytvořili. Ujistěte se, že jste vybrali verzi se stavem **Koncept**.
2. Na kartě **Nastavení** v mřížce vyberte nastavení funkce a poté vyberte **Upravit**.
3. Na kartě **Datový kanál** ve skupině polí **Parametry** vyberte **Adresa serveru** a zadejte poskytovatele e -mailového účtu.
4. Vyberte **Port serveru** a zadejte port používaný poskytovatelem e-mailového účtu.
5. Vyberte **Tajný klíč jména uživatele** a zadejte název tajného klíče trezoru klíčů, který obsahuje ID uživatelského účtu e-mailu.
6. Vyberte **Tajný klíč hesla uživatele** a zadejte název tajného klíče trezoru klíčů, který obsahuje heslo uživatelského účtu e-mailu.
7. Vyberte **Filtr předmětu**. Zkontrolujte a aktualizujte řetězec, který obsahuje výchozí předmět e -mailu, abyste identifikovali e-mail obsahující elektronickou fakturu dodavatele k importu.
8. Na kartě **Pravidla použitelnosti** v případě potřeby zkontrolujte a aktualizujte kritéria. Další informace naleznete v tématu [Pravidla použitelnosti](e-invoicing-configuration-rcs.md#applicability-rules).
9. Zvolte **Uložit** a zavřete stránku.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Konfigurace kanálu Microsoft SharePoint

Konfigurujte kanál Microsoft SharePoint, pokud funkce elektronické fakturace importuje elektronické faktury dodavatele ze souborů umístěných ve složkách SharePoint.

1. V RCS vyberte funkci elektronické fakturace, kterou jste vytvořili. Ujistěte se, že jste vybrali **verzi** se stavem **Koncept**.
2. Na kartě **Nastavení** v mřížce vyberte nastavení funkce a poté vyberte **Upravit**.
3. Na kartě **Datový kanál** ve skupině polí **Parametry** vyberte **Adresa SharePoint** a zadejte URL adresu SharePointu.
4. Vyberte **Port serveru** a zadejte port používaný poskytovatelem e-mailového účtu.
5. Vyberte **ID aplikace** a zadejte název tajného klíče trezoru klíčů, který obsahuje ID klienta SharePointu.
6. Vyberte **Tajný klíč aplikace** a zadejte název tajného klíče trezoru klíčů, který obsahuje heslo klienta SharePointu.
7. Vyberte **Filtr souboru**. Zkontrolujte a aktualizujte masku a filtrujte soubory, které obsahují elektronickou fakturu dodavatele k importu.
8. Na kartě **Pravidla použitelnosti** v případě potřeby zkontrolujte a aktualizujte kritéria. Další informace naleznete v tématu [Pravidla použitelnosti](e-invoicing-configuration-rcs.md#applicability-rules).
9. Zvolte **Uložit** a zavřete stránku.

### <a name="deploy-an-electronic-invoicing-feature"></a>Nasazení funkce elektronické fakturace

Informace o nasazení funkce elektronické fakturace najdete v části [Nasazení funkce elektronické fakturace do prostředí služby](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>Nastavení importu faktury dodavatele ve Finance a Supply Chain Management
Dokončete kroky v následujících dvou částech a nastavte různé typy importu faktur dodavatele.

### <a name="import-vendor-invoices-from-email"></a>Import faktur dodavatele z e-mailu

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
2. Vyberte **Kontextový model faktury zákazníka** a vytvořte odvozenou konfiguraci.
3. Ve verzi **Koncept** vyberte **Návrhář**.
4. Ve stromu **Datový model** vyberte **Faktura zákazníka** a poté vyberte **Mapovat model na zdroj dat**.
5. Ve stromu **Definice** vyberte **Faktura zákazníka** a poté vyberte **Návrhář**.
6. Ve stromě **Zdroje dat** vyberte **Kontext\_Kanál**. V poli **Hodnota** vyberte **PEPPOL**. Jedná se o název kanálu zadaný v konfiguraci datového kanálu pro funkci elektronického výkaznictví v RCS. 
7. Zvolte **Uložit** a zavřete stránku.
8. Zavřete stránku.
9. Vyberte **Kontextový model faktury zákazníka** a na záložce s náhledem **Verze** vyberte **Změnit stav** > **Dokončeno**.
10. Jděte na **Správa organizace** > **Nastavení** > **Parametry elektronického dokumentu** a na kartě **Funkce** se ujistěte, že je vybrána možnost **Globální elektronické faktury PEPPOL**. 
11. Na kartě **Externí kanály** v poli **Kanály** vyberte **Přidat**.
12. V poli **Kanál** zadejte **PEPPOL**. Zadejte popis do pole **Popis**.
13. V poli **Společnost** zvolte právnickou osobu. V poli **Kontext dokumentu** vyberte **Kontext faktury zákazníka - Kontextový model faktury zákazníka**.
14. Zvolte **Uložit** a pak zavřete stránku.


## <a name="receive-electronic-invoices"></a>Přijetí elektronických faktur
Chcete-li přijímat elektronické faktury, postupujte takto:

1. Přejděte na **Správa organizace** > **Periodické** > **Elektronické dokumenty** > **Přijímat elektronické dokumenty**.
2. Zvolte **KO** a pak zavřete stránku.

## <a name="view-receive-logs-for-electronic-invoices"></a>Zobrazení protokolů příjmu elektronických faktur

Chcete-li zobrazit protokoly příjmu elektronických faktur, přejděte na **Správa organizace** > **Periodické** > **Elektronické dokumenty** > **Protokol o přijetí elektronického dokumentu**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

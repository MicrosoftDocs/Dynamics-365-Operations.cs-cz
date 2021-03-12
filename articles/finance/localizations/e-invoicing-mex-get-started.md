---
title: Začněte s doplňkem elektronické fakturace pro Mexiko
description: Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace pro Mexiko v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d91f377af2514af932ea585adb75a56bdee13871
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988467"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a>Začněte s doplňkem elektronické fakturace pro Mexiko

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Doplněk elektronické fakturace pro Mexiko aktuálně nepodporuje všechny funkce, které jsou k dispozici v dokumentu Comprobante Fiscal Digital por Internet (CFDI) a v související integraci zabudované do Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management.

Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace pro Mexiko. Provede vás konfiguračními kroky, které jsou závislé na zemi v Regulatory Configuration Services (RCS) a Finance. Také vás provede kroky, které musíte ve Finance dodržovat, abyste mohli prostřednictvím služby odesílat faktury CFDI, a vysvětlí, jak zkontrolovat výsledky zpracování a stav faktur CFDI.

## <a name="prerequisites"></a>Předpoklady

Než dokončíte kroky v tomto tématu, musíte provést kroky v [Začněte s doplňkem Elektronická fakturace](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>Nastavení RCS

Během instalace RCS dokončíte tyto úlohy:

1. Importujte funkci elektronické fakturace pro zpracování faktur CFDI.
2. Zkontrolujte konfigurace formátu, které jsou vyžadovány ke generování, odesílání a přijímání odpovědí o fakturách CFDI a k odesílání a přijímání odpovědí o zrušení.
3. Nakonfigurujte události, které podporují scénáře odeslání faktury CFDI.
4. Publikujte funkci elektronické fakturace pro faktury CFDI.

> [!NOTE]
> „Funkce elektronické fakturace“ je obecný název prostředku, který je nakonfigurován a publikován tak, aby využíval server doplňku elektronické fakturace. V tomto případě jsou faktury CFDI (MX) funkcí elektronické fakturace, kterou nastavíte.

## <a name="import-the-e-invoicing-feature"></a>Import funkce elektronické fakturace

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **elektronická fakturace**.
3. Na stránce **Funkce elektronické fakturace** vyberte **Import**, chcete-li importovat funkci **Faktury CFDI (MX)** z globálního úložiště.

    > [!NOTE]
    > Pokud nevidíte funkci v seznamu, vyberte **Synchronizovat** a potom opakujte krok 3.

![Funkce importu faktur CFDI (MX)](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

Při importu funkce **Faktury CFDI (MX)** z globálního úložiště importují se také všechna nastavení funkcí, včetně konfigurací a akcí.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>Vytvořte novou verzi funkce faktur CFDI (MX)

Můžete vytvořit novou verzi, pokud je třeba například aktualizovat adresy URL. Další informace viz [Elektronická fakturace CFDI](tasks/mx-00010-e-invoicing-cfdi.md).

- Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte **Nový**.

![Přidání nové verze funkce elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>Aktualizujte verzi konfigurace

1. Na stránce **Funkce elektronické fakturace** na kartě **Konfigurace** vyberte **Přidat** nebo **Odebrat** ke správě verzí konfigurace (konfigurace formátu souboru ER).

    ![Správa konfigurací funkce elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Když vytvoříte novou verzi, všechny konfigurace se zdědí z poslední publikované verze. Ke zpracování faktur CFDI jsou vyžadovány následující konfigurace:

    - Faktura CFDI (BusinessDocumentService)
    - Import zpráv odpovědi CFDI
    - Import protokolu chyb CFDI
    - Žádost o zrušení CFDI (MX) (BusinessDocumentService)
    - Faktura CFDI (BusinessDocumentService)

2. V seznamu vyberte verzi konfigurace a poté vyberte **Upravit** nebo **Zobrazit**, chcete-li otevřít stránku **Návrhář formátů**, kde můžete upravit nebo zobrazit konfiguraci.

    ![Otevření stránky Návrhář formátu](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. Použijte stránku **Návrhář formátů**, chcete-li upravovat a prohlížet konfigurace souborů ve formátu ER. Další informace získáte v tématu [Vytvoření konfigurací elektronického dokumentu](../../dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Stránka návrháře formátu](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Spravujte nastavení funkce elektronické fakturace

- Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** vyberte **Přidat**, **Odebrat** nebo **Upravit** ke správě nastavení funkcí elektronické fakturace.

![Správa nastavení funkce elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

Chcete-li odeslat faktury CFDI k autorizaci (vygenerovat soubor XML, odeslat soubor XML a zpracovat odpověď), je vyžadováno nastavení funkce **Prodejní faktura**.

Chcete-li odeslat zrušení faktury CFDI, jsou vyžadována nastavení funkcí **Zrušení** a **Zrušit**.

### <a name="configure-the-sales-invoice-feature-setup"></a>Nakonfigurujte nastavení funkce prodejní faktury

1. Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** ve sloupci **Nastavení funkce** vyberte **Prodejní faktura**.
2. Vyberte **Upravit**, chcete-li konfigurovat akce, pravidla použitelnosti a proměnné.

    ![Úprava nastavení funkce elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. Na stránce **Nastavení verze funkce** vyberte kartu **Akce** pro správu seznamu akcí. Akce definují seznam operací, které je nutné spustit v postupném pořadí, aby bylo možné provést úplné provedení události.

    ![Karta Akce](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | ID akce | Akce                   | Název akce                                  | Popis akce                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Převod dokumentu       | Generujte elektronickou fakturu CFDI bez digitální značky | Vygenerujte elektronickou fakturu CFDI.                                |
    | 2         | Podepsat dokument            | Digitální značka                                 | Digitálně podepište e-fakturu k odeslání.                |
    | 3         | Volejte mexickou službu PAC | Odeslat elektronickou fakturu CFDI                        | Klient Windows Communication Foundation (WCF) odešle elektronickou fakturu CFDI. |
    | 4         | Odezva procesu         | Analyzujte odpověď webové služby                 | Analyzujte odezvu webové služby a vraťte protokol chyb. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Nastavte adresu URL pro webové Mexican PAZ 

1. Na stránce **Nastavení verze funkce** na kartě **Akce** na pevné záložce **Akce** vyberte **Volejte mexickou službu PAC**.
2. Na pevné záložce **Parametry** v poli **Adresa URL** zadejte adresu URL webové služby pro odeslání faktury CFDI.

> [!NOTE]
> Stejným způsobem aktualizujte adresu URL pro akci **Volat mexickou službu PAC** pro nastavení funkcí **Zrušit** a **Žádost o zrušení**.

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>Přiřaďte verzi konceptu do prostředí elektronické fakturace

1. Na stránce **Funkce elektronické fakturace** na kartě **Prostředí** vyberte **Povolit**.
2. V poli **Prostředí** vyberte prostředí.
3. V poli **Platí od** vyberte datum, kdy má začít platnost prostředí.
3. Vyberte **Povolit**.

![Povolení prostředí elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>Změna stavu verze na Dokončeno.

1. Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte verzi funkce elektronické fakturace, která má stav **Koncept**.
2. Vyberte **Změnit stav \> Dokončeno**.

## <a name="change-the-version-status-to-published"></a>Změna stavu verze na Publikováno.

- Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte **Změnit stav \> Publikovat**.

## <a name="publish-the-e-invoicing-feature"></a>Publikovat funkci elektronické fakturace

1. Na stránce **Funkce elektronické fakturace** vyberte kartu **Verze**, chcete-li spravovat stav funkce **Faktury CFDI (MX)**.
2. Vyberte **Změnit stav** ke změně stavu funkce.

![Změna stavu funkce elektronické fakturace](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a>Nastavte integraci doplňku elektronické fakturace ve Finance

Chcete-li nastavit doplněk Elektronická fakturace v aplikaci Finance, dokončíte tyto úkoly:

1. Importujte datový model ER, mapování datového modelu ER a formáte požadované pro faktury CFDI.
2. Nakonfigurujte typy odpovědí pro aktualizaci faktur CFDI. Tyto typy odpovědí se používají pro odpověď ze serveru autorizovaného poskytovatele certifikace (PAC).

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>Importujte datový model ER, mapování datového modelu ER a kontextové konfigurace pro e-faktury CFDI.

1. Přihlášení do aplikace Finance.
2. V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft**. Ujistěte se, že je tento poskytovatel konfigurace nastaven na **Aktivní**. Další informace o tom, jak nastavit poskytovatele jako **Aktivní** naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Vyberte **Úložiště**.
4. Vyberte **Globální prostředek \> Otevřít**.
5. Importujte **Model faktury**, **Mapování modelu faktury**, **Formát faktury CFDI (MX)**, **Formát žádosti o zrušení faktury CFDI (MX)** a **Formát zrušení faktury CFDI (MX)**.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>Zapněte funkci pro zpracování faktur CFDI

1. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.
2. Na kartě **Funkce** zaškrtněte políčko **Povolit** v řádcích pro odkaz na funkci **MX-00010** and **MX-00016**.

![Zapnutí funkcí pro zpracování faktur CFDI](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>Importujte konfiguraci ER a nastavte typy odpovědí pro aktualizaci faktur CFDI

#### <a name="import-er-configurations"></a>Import konfigurací ER

1. V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft**.
3. Vyberte **Úložiště**.
4. Vyberte **Globální prostředek \> Otevřít**.
5. Importujte **Model zprávy s odpovědí**, **Import protokolu chyb CFDI (MX)** a **Import zpráv CFDI s odpovědí (MX)**.

#### <a name="set-up-the-response-types"></a>Nastavte typy odpovědí

1. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.
2. Na kartě **Elektronický dokument** vyberte **Přidat**.
3. Zadejte deník faktury zákazníka a poté v poli **Název tabulky** vyberte fakturu projektu.
4. Pro každou tabulku definujte související kontext dokumentu:

    - Pro **Deník faktury zákazníka** zadejte **Kontext faktury zákazníka**.
    - Pro **Faktura projektu** zadejte **Kontext faktury projektu**.

4. Vyberte **Typy odpovědí**, chcete-li konfigurovat typy odpovědí, které lze vrátit z doplňku elektronické fakturace a zahrnout do deníku faktury zákazníka nebo faktury projektu.
5. Vyberte **Nový** a pak v poli **Typ odpovědí** vyberte **Odpověď**.
6. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
7. V poli **Mapování modelů** vyberte **Formát importu zprávy odpovědi - mapování modelu ze zprávy odpovědi**.
8. Zvolte **Uložit**.
9. Vyberte **Nový** a pak v poli **Typ odpovědí** vyberte **ResponseData**.
10. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
11. V poli **Mapování modelů** vyberte **Formát importu dat odpovědí CFDI (podrobnosti) - import dat odpovědí**.
12. Zvolte **Uložit**.

## <a name="process-electronic-invoices-in-finance"></a>Zpracovat elektronické faktury v aplikaci Finance 

Během zpracování CFDI faktur ve Finance prostřednictvím doplňku Elektronická fakturace můžete provádět následující úkoly:

- Odesílat faktury CFDI
- Zobrazit protokoly provádění podání.
- Odesílat zrušení faktury CFDI.

### <a name="submit-cfdi-invoices"></a>Odesílat faktury CFDI

Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** již nelze používat postup pro **Export/import elektronické faktury** pro odesílání faktur CFDI (**Pohledávky \> Faktury \> Elektronické faktury)**. Je nahrazen novým procesem, který je pojmenován **Odesílejte elektronické dokumenty**.

> [!NOTE]
> Před použitím nového procesu **Odeslat elektronické dokumenty** ověřte, že bylo dokončeno nastavení požadované pro mexické e-faktury. Další informace naleznete v tématu [Rozložení CFDI verze 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Odesílejte elektronické dokumenty**.
2. Pro první odeslání jakéhokoli dokumentu vždy nastavte možnost **Znovu odeslat dokumenty** na **Ne**. Pokud musíte znovu odeslat dokument prostřednictvím služby, nastavte tuto možnost na **Ano**.
3. Na pevné záložce **Záznamy, které mají být zahrnuty** vyberte **Filtr** a otevřete dialogové okno **Dotaz**, kde můžete vytvořit dotaz pro výběr dokumentů k odeslání.

![Odeslání dokumentu CFDI](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Během prvního pokusu o odeslání dokumentu prostřednictvím služby budete vyzváni k potvrzení spojení s doplňkem Elektronická fakturace. Vyberte **Klikněte zde pro připojení ke službě elektronického odesílání dokumentů**.

### <a name="view-submission-logs"></a>Zobrazit protokoly odeslání

Můžete si prohlédnout protokoly o odeslání pro všechny odeslané dokumenty nebo pouze pro jeden odeslaný dokument.

#### <a name="view-all-submission-logs"></a>Zobrazit všechny protokoly odeslání

Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** je k dispozici nová stránka, která vám umožní sledovat proces odesílání dokumentů. Můžete tuto stránku použít, chcete-li si prohlédnout protokoly o odeslání pro všechny odeslané dokumenty.

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.
2. V poli **Typ dokumentu** vyberte **Deník faktury zákazníka**, chcete-li filtrovat požadované elektronické dokumenty.

    ![Výběr typu dokumentu pro zobrazení protokolů odeslání](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. V podokně akcí vyberte **Dotazy \> Podrobnosti o odeslání** pro zobrazení podrobností o protokolech provádění odeslání.

    ![Zobrazení podrobností protokolu odeslání.](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

Informace v protokolech podání jsou rozděleny mezi tři pevné záložky:

- **Zpracování akcí** - tato pevná záložka zobrazí protokol provádění akcí, které jsou konfigurovány ve verzi funkce, která byla nastavena v RCS. Sloupec **Stav** ukazuje, zda byla akce úspěšně spuštěna.
- **Soubory akcí** - tato pevná záložka zobrazí přechodné soubory, které byly vygenerovány během provádění akcí. Můžete vybrat **Zobrazit** a stáhnout soubor a zobrazit jej.
- **Zpracování protokolu akcí** - Tato pevná záložka zobrazuje výsledky komunikace mezi doplňkem Elektronická fakturace a cílovou webovou službou. Ukazuje také, co bylo vráceno zpracováním z webové služby. Sloupec **Chybový kód** zobrazí návratový kód, který byl vrácen autorizační webovou službou.

Po autorizaci odeslané faktury CFDI se její stav aktualizuje na **Schválený**.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>Zobrazit protokoly o odeslání z faktur CFDI

Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** můžete také zobrazit protokoly odeslání z faktury CFDI.

1. Přejděte na **Pohledávky \> Dotazy a sestavy \> CFDI (elektronické faktury)**.
2. Vyberte CFDI fakturu, která byla odfeslána po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace**.
3. V podokně akcí na kartě **Historie** vyberte **Elektronický protokol dokumentů**.

![Zobrazit protokoly o odeslání z faktur CFDI](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> U faktur CFDI, které byly odeslány před zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace**, je k dispozici tlačítko **Historie**. U faktur CFDI, které byly odeslány po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace**, tlačítko **Historie** není k dispozici.

### <a name="submit-cancellation-of-cfdi-invoices"></a>Zrušení odeslání faktury CFDI

Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** již nelze používat starý postup pro zrušení faktur CFDI. Je nahrazen novým procesem zrušení, který je vložen do stránky **Elektronický protokol pro odesílání dokumentů**.

1. Přejděte na **Pohledávky \> Dotazy a sestavy \> CFDI (elektronické faktury)**.
2. Pokud má faktura CFDI stav **Schváleno**, vyberte **Funkce \> Zrušit CFDI**.
3. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.
4. Vyberte fakturu CFDI a poté vyberte **Funkce \> Odeslat související příspěvky**.
5. Zadejte popis souvisejícího příspěvku a poté vyberte **OK**.

#### <a name="view-cancellation-submission-logs"></a>Zobrazit protokoly zrušení

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.
2. V poli **Typ dokumentu** vyberte **Deník faktury zákazníka**, chcete-li filtrovat pouze dikumenty deníku zákaznických faktur.
3. Vyberte fakturu CFDI a poté na stránce Akce vyberte **Dotazy \> Související příspěvky**.

    Stránka **Související odeslání** zobrazuje všechna související odeslání a jejich stav odeslání pro danou fakturu CFDI. Na následujícím obrázku představuje první řádek odeslání, které požadovalo schválení faktury CFDI. Druhý řádek představuje odeslání, které zrušilo danou fakturu CFDI.

    ![Zobrazit protokoly odeslání zrušení](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. V podokně akcí vyberte **Dotazy \> Podrobnosti o odeslání** pro zobrazení podrobností o protokolech provádění odeslání.

    ![Zobrazení podrobností protokolu odeslání zrušení](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů
Povolení funkcí MX-00010 a MX-00016 (Faktura CFDI a zrušení CFDI) může vyžadovat zasílání omezených dat, která zahrnují daňové identifikační číslo organizace. To bude předáno agenturám třetích stran oprávněným daňovým úřadem pro účely zasílání elektronických faktur tomuto daňovému úřadu v předdefinovaném formátu požadovaném pro integraci s webovými službami těchto vlád. Správce může povolit a zakázat funkce MX-00010 a MX-00016 (Faktura CFDI a zrušení CFDI) přechodem na **Správa organizace \> Nastavení \> Parametry elektronckého dokumentu**. Vyberte kartu **Funkce**, vyberte řádky obsahující funkce MX-00010 a MX-00016 a poté proveďte příslušný výběr. Data importovaná z těchto externích systémů do této online služby Dynamics 365 podléhají našim [Prohlášením o ochraně osobních informací](https://go.microsoft.com/fwlink/?LinkId=512132). Další informace najdete v oddílech Oznámení o ochraně osobních údajů v dokumentaci funkcí pro jednotlivé země.

## <a name="additional-resources"></a>Další prostředky

- [Přehled doplňku Elektronická fakturace](e-invoicing-service-overview.md)
- [Začněte s doplňkem elektronické fakturace](e-invoicing-get-started.md)
- [Nastavení doplňku Elektronická fakturace](e-invoicing-setup.md)

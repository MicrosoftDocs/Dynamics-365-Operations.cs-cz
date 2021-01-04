---
title: Začněte s doplňkem elektronické fakturace pro Brazílii
description: Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace pro Brazílii v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: fb3ec2d60875d7a0747d64b397aafaa0a3d26348
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/19/2020
ms.locfileid: "4441338"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Začněte s doplňkem elektronické fakturace pro Brazílii 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Doplněk elektronické fakturace pro Brazílii aktuálně nepodporuje všechny funkce, které jsou k dispozici v integraci fiskálních dokumentů zabudovaných do Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management.

Toto téma poskytuje informace, které vám pomohou začít s doplňkem elektronické fakturace pro Brazílii. Provede vás konfiguračními kroky, které jsou závislé na zemi v Regulatory Configuration Services (RCS) a ve Finance a Supply Chain Management. Také vás provede procesem odeslání fiskálního dokumentu NF-e (model elektronického fiskálního dokumentu 55) prostřednictvím služby a vysvětlí, jak zkontrolovat výsledky zpracování a stav fiskálních dokumentů.

## <a name="prerequisites"></a>Předpoklady

Než dokončíte kroky v tomto tématu, musíte provést kroky v [Začněte s doplňkem Elektronická fakturace](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>Nastavení RCS

Během instalace RCS dokončíte tyto úlohy:

1. Importujte funkci elektronické fakturace pro fiskální dokumenty NF-e.
2. Zkontrolujte formáty souborů, které jsou vyžadovány k odeslání fiskálních dokumentů NF-e k autorizaci.
3. Zkontrolujte formáty souborů, které jsou požadovány pro zrušení schválené NF-e.
4. Nakonfigurujte událost, která se vyžaduje k odeslání fiskálních dokumentů NF-e k autorizaci.
5. Nakonfigurujte událost, která se vyžaduje pro zrušení schválené NF-e.
6. Přiřaďte funkci elektronické fakturace do prostředí doplňku elektronické fakturace.
7. Publikování funkce elektronické fakturace.

> [!NOTE]
> „Funkce elektronické fakturace“ je obecný název prostředku, který je nakonfigurován a publikován tak, aby využíval server doplňku elektronické fakturace. Nastavení funkce elektronické fakturace mimo jiné kombinuje použití konfiguračních formátů elektronických zpráv (ER) k vytvoření konfigurovatelných souborů exportu a importu a použití akcí a toků akcí k umožnění vytváření konfigurovatelných pravidel pro odesílání požadavků, import odpovědi a analýzu obsahu odpovědí.

## <a name="import-the-e-invoicing-feature"></a>Import funkce elektronické fakturace

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **elektronická fakturace**.
3. Na stránce **Funkce elektronické fakturace** vyberte **Import**, chcete-li importovat funkci elektronické fakturace fiskálních dokumentů NF-e z globálního úložiště.

    ![Tlačítko Importovat](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Vyberte funkci fiskálního dokumentu NF-e a poté vyberte **Import**.

    ![Import funkce NF-e](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>Vytvořte novou verzi funkce fiskálního dokumentu NF-e

- Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte **Nový**.

![Přidání nové verze funkce elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Aktualizujte verzi konfigurace

1. Na stránce **Funkce elektronické fakturace** na kartě **Konfigurace** vyberte **Přidat** nebo **Odebrat** ke správě verzí konfigurace (konfigurace formátu souboru ER).

    ![Správa konfigurací funkce elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - Když vytvoříte novou verzi funkce fiskálního dokumentu NF-e, všechny konfigurační verze (formáty souborů ER) se zdědí z nejnovější verze.
    - K odeslání fiskálního dokumentu NF-e k autorizaci jsou vyžadovány následující konfigurační verze:

        - formát exportu odeslání NFe
        - Import zpráv odpovědi NFe
        - Import protokolu chyb NFe

    - K odeslání zrušení NF-e je nutná následující konfigurační verze:

        - formát exportu zrušení NFe

2. V seznamu vyberte verzi konfigurace a poté vyberte **Upravit** nebo **Zobrazit**, chcete-li otevřít stránku **Návrhář formátů**, kde můžete upravit nebo zobrazit konfiguraci.

    ![Otevření stránky Návrhář formátu](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Použijte stránku **Návrhář formátů**, chcete-li upravovat nebo prohlížet konfigurace souborů ve formátu ER. Další informace získáte v tématu [Vytvoření konfigurací elektronického dokumentu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Stránka návrháře formátu](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>Spravujte nastavení funkce elektronické fakturace

- Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** vyberte **Přidat** nebo **Odebrat** ke správě nastavení funkcí elektronické fakturace (tj. událostí NF-e).

![Správa nastavení funkce elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Když vytvoříte novou verzi funkce fiskálního dokumentu NF-e, která je odvozena z jiné funkce elektronické fakturace, všechna nastavení funkcí (události NF-e) se zdědí z nejnovější verze.

Chcete-li odeslat fiskální dokumenty NF-e k autorizaci, je vyžadováné nastavení funkce **Odeslat**.

Chcete-li odeslat zrušení NF-e, je vyžadováno nastavení funkce **Zrušení**.

#### <a name="configure-the-submit-feature-setup"></a>Nakonfigurujte nastavení funkce Odeslat

1. Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** ve sloupci **Nastavení funkce** vyberte **Odeslat**.
2. Vyberte možnost **Upravit**.

    ![Upravit nastavení funkce elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. Na stránce **Nastavení verze funkce** vyberte kartu **Akce** pro správu seznamu akcí.

    ![Karta Akce](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Zkontrolujte akce, které jsou vyžadovány k odeslání NF-e k autorizaci.

    | ID akce | Název akce                  | Popis akce                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Převod dokumentu           | Vytvořte soubor NF-e XML pro odeslání.                          |
    | 2         | Podepsat dokument                | Aplikujte digitální certifikát na soubor XML.                    |
    | 3         | Volejte brazilskou službu SEFAZ | Odešlete podepsaný soubor XML do webových služeb k autorizaci. |
    | 4         | Odezva procesu             | Získejte odpověď webové služby.                                     |
    | 5         | Převod dokumentu           | Parsujte obsah souboru, který je přijat jako odpověď.     |
    | 6         | Převod dokumentu           | Vytvořte soubor XML a informujte se o stavu odeslání.    |
    | 7         | Volejte brazilskou službu SEFAZ | Odešlete soubor XML, který požaduje stav odeslání.          |
    | 8         | Odezva procesu             | Získejte odpověď webové služby.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Nastavte adresu URL pro webové služby SEFAZ 

1. Na stránce **Nastavení verze funkce** na kartě **Akce** na pevné záložce **Akce** vyberte **Volejte brazilskou službu SEFAZ** (ID akce **3**).
2. Na pevné záložce **Parametry** v poli **Parametr adresy URL** zadejte adresu URL webové služby SEFAZ pro odeslání NF-e.
3. Na pevné záložce **Akce** vyberte **Volejte brazilskou službu SEFAZ** (ID akce **7**).
4. Na pevné záložce **Parametry** v poli **Parametr adresy URL** zadejte adresu URL webové služby SEFAZ pro odeslání NF-e.

#### <a name="configure-the-cancellation-feature-setup"></a>Nakonfigurujte nastavení funkce Zrušení

1. Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** ve sloupci **Nastavení funkce** vyberte **Zrušení**.
2. Vyberte možnost **Upravit**.
3. Na stránce **Nastavení verze funkce** vyberte kartu **Akce** pro správu seznamu akcí.
4. Zkontrolujte akce, které jsou požadovány pro zrušení schválené NF-e.

    | ID akce | Název akce                  | Popis akce                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Převod dokumentu           | Vytvořte soubor zrušení NF-e XML pro odeslání.            |
    | 2         | Podepsat dokument                | Aplikujte digitální certifikát na soubor XML.                   |
    | 3         | Volejte brazilskou službu SEFAZ | Odešlete podepsaný soubor XML do webových služeb ke zrušení. |
    | 4         | Odezva procesu             | Získejte odpověď webové služby.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Nastavte adresu URL pro webové služby SEFAZ

1. Na stránce **Nastavení verze funkce** na kartě **Akce** na pevné záložce **Akce** vyberte **Volejte brazilskou službu SEFAZ** (ID akce **3**).
2. Na pevné záložce **Parametry** v poli **Parametr adresy URL** zadejte adresu URL webové služby SEFAZ pro zrušení schváleného NF-e.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>Zpřístupněte prostředí elektronické fakturace a přiřaďte verzi Koncept

1. Na stránce **Funkce elektronické fakturace** na kartě **Prostředí** vyberte **Povolit**.
2. V poli **Prostředí** vyberte prostředí.
3. V poli **Platí od** vyberte datum, kdy má začít platnost prostředí.
4. Vyberte **Povolit**.

![Povolení prostředí elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Změna stavu kursu na Dokončeno.

1. Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte verzi funkce elektronické fakturace, která má stav **Koncept**.
2. Vyberte **Změnit stav \> Dokončeno**.

### <a name="change-the-status-to-publish"></a>Změna stavu kursu na Publikovat.

1. Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte verzi funkce elektronické fakturace, která má stav **Dokončeno**.
2. Vyberte **Změnit stav \> Publikovat**.

![Publikování funkce elektronické fakturace](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Nastavte integraci doplňku elektronické fakturace ve Finance nebo Supply Chain Management

Během instalace dokončíte tyto úlohy:

1. Zapněte funkci NF-e Federal pro Brazílii.
2. Importujte konkrétní datový model ER, mapování datového modelu a formáty, které jsou vyžadovány pro fiskální dokumenty NF-e.
3. Importujte konfiguraci ER a nastavte typy odpovědí, které jsou nutné k aktualizaci stavu fiskálního dokumentu po vrácení procesu odeslání.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Zapněte funkci NF-e Federal pro Brazílii

1. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.
2. Na kartě **Funkce** zaškrtněte políčko **Povolit** v řádku pro odkaz na funkci **BR00053**.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>Importujte mapování datového modelu ER vyžadované pro fiskální dokumenty NF-e

1. Přihlášení do aplikace Finance.
2. V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft**. Ujistěte se, že je tento poskytovatel konfigurace nastaven na **Aktivní**. Další informace o tom, jak nastavit poskytovatele jako **Aktivní** naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Vyberte **Úložiště**.
4. Vyberte **Globální prostředek \> Otevřít**.
5. Importujte konfiguraci **Mapování fiskálních dokumentů**.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>Importujte konfiguraci ER a nastavte typy odpovědí pro fiskální dokumenty

1. V pracovním prostoru **Elektronické výkaznictví** v části **Poskytovalé konfigurace** vyberte dlaždici **Microsoft**.
2. Vyberte **Úložiště**.
3. Vyberte **Globální prostředek \> Otevřít**.
4. Importujte **Import protokolu chyb NF-e (BR)**, **Formát importu dat odpovědí NF-e (BR)** a **Import zpráv odpovědi NF-e (BR)**.
5. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.
6. Na kartě **Elektronický dokument** vyberte **Přidat**.
6. V poli **Název tabulky** zadejte **Záhlaví fiskálního dokumentu**.
7. V poli **Kontext dokumentu** vyberte **Kontextový model faktury zákazníka - kontext fiskálního dokumentu**.
8. Vybrat **Typy odpovědí**.
9. Vyberte **Nový** a pak v poli **Typ odpovědí** vyberte **Odpověď**.
10. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
11. V poli **Mapování modelů** vyberte **Formát importu zprávy odpovědi - mapování modelu ze zprávy odpovědi**.
12. Zvolte **Uložit**.
13. Vyberte **Nový** a pak v poli **Typ odpovědí** zadejte **ResponseData**.
14. V poli **Stav odeslání** vyberte **Čeká na zpracování**.
15. V poli **Mapování modelů** vyberte **Formát importu dat odpovědí NFe - import dat odpovědí**.
16. Zvolte **Uložit**.

## <a name="electronic-invoice-processing"></a>Zpracování elektronických faktur

Během zpracování ve Finance dokončíte tyto úlohy:

1. Odešlete fiskální dokument prostřednictvím doplňku Elektronická fakturace.
2. Zobrazte protokoly o provedení odeslání a zkontrolujte výsledky zpracování.
3. Odešlete zrušení fiskálního dokumentu prostřednictvím doplňku Elektronická fakturace.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>Odešlete fiskální dokumenty NF-e k autorizaci SEFAZ 

Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** již neluze používat starý postup pro odesílání fiskálních dokumentů NF-e k autorizaci (**Proces exportu / importu NF-e**). Je nahrazen novým procesem, který je pojmenován **Odesílejte elektronické dokumenty**.

> [!NOTE]
> Než budete pokračovat, ujistěte se, že máte jeden nebo více fiskálních dokumentů zákazníka model 55, které byly vystaveny fiskálním zřízením zákazníka. Směr pro tyto fiskální dokumenty musí být nastaven na **Odchozí** a stav musí být **Vytvořeno**. Další informace viz [Vydat fiskální dokument zákazníka (Brazílie)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Odesílejte elektronické dokumenty**.
2. Pro první odeslání jakéhokoli dokumentu vždy nastavte možnost **Znovu odeslat dokumenty** na **Ne**. Pokud musíte znovu odeslat dokument prostřednictvím služby, nastavte tuto možnost na **Ano**.
3. Na pevné záložce **Záznamy, které mají být zahrnuty** vyberte **Filtr** a otevřete dialogové okno **Dotaz**, kde můžete vytvořit dotaz pro výběr dokumentů k odeslání.
4. Na kartě **Rozsah** vyberte možnost **Přidat**.
5. V poli **Tabulka** vyberte **Záhlaví fiskálního dokumentu**.
6. V poli **Odvozená tabulka** vyberte **Záhlaví fiskálního dokumentu**.
6. V poli **Pole** zvolte **Číslo**.
7. V poli **Kritéria** zadejte číslo fiskálního dokladu, který má být odeslán.
8. Zvolte **OK** a zavřete dialogové okno **Dotaz**.
8. Vyberte **OK** k odeslání vybraných dokumentů.

> [!NOTE]
> Během prvního pokusu o odeslání dokumentu prostřednictvím služby budete vyzváni k potvrzení spojení s doplňkem Elektronická fakturace. Vyberte **Klikněte zde pro připojení ke službě elektronického odesílání dokumentů**.

### <a name="view-all-submission-logs"></a>Zobrazit všechny protokoly odeslání

Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** je k dispozici nová stránka, která vám umožní sledovat proces odesílání dokumentů. Můžete tuto stránku použít, chcete-li si prohlédnout protokoly o odeslání pro všechny odeslané dokumenty.

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.
2. V poli **Typ dokumentu** vyberte **Záhlaví fiskálního dokumentu** pro filtrování pouze fiskálních dokumentů.
3. V podokně akcí vyberte **Dotazy \> Podrobnosti o odeslání** pro zobrazení podrobností o protokolech provádění odeslání.

![Zobrazení podrobností protokolu odeslání.](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> U fiskálních dokumentů NF-e sloupec **Chybový kód** zobrazí návratový kód, který byl vrácen webovými službami SEFAZ.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Prohlédněte si protokoly o odeslání prostřednictvím stránky fiskálních dokumentů

Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** můžete také zobrazit protokoly odeslání prostřednictvím stránky fiskálního dokumentu.

1. Přejděte na **Hlavní kniha \> Dotazy a sestavy \> Fiskální dokumenty \> Všechny fiskální dokumenty**.
2. Vyberte fiskální dokument, který byl dříve odeslán prostřednictvím doplňku elektronické fakturace.
3. V podokně akcí na kartě **NF-e federální** vyberte **Elektronický protokol dokumentů**.

![Prohlížení protokolů o odeslání ze stránky fiskálních dokumentů](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Odešlete schválené fiskální dokumenty NF-e ke zrušení SEFAZ

Po zapnutí funkce **Konfigurovatelná integrace doplňku elektronické fakturace** již nelze používat starý postup pro zrušení fiskálních dokumentů NF-e. Je nahrazen novým procesem zrušení, který je vložen do stránky **Elektronický protokol pro odesílání dokumentů**.

> [!NOTE]
> Ujistěte se, že jste zrušili fiskální dokument zákazníka pro schválený fiskální dokument NF-e. Další informace viz [Zrušit fiskální dokument zákazníka (Brazílie)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.
2. Vyberte fiskální dokument a poté vyberte **Funkce \> Odeslat související příspěvky**.
3. Zadejte popis souvisejícího příspěvku a poté vyberte **OK**.

### <a name="view-cancellation-submission-logs"></a>Zobrazit protokoly zrušení

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.
2. V poli **Typ dokumentu** vyberte **Záhlaví fiskálního dokumentu** pro filtrování pouze fiskálních dokumentů.
3. Vyberte fiskální dokument a poté na stránce Akce vyberte **Dotazy \> Související příspěvky**.

    Související odeslání jsou odeslání související s hlavním podáním, které bylo provedeno jako první. Například odeslání, které autorizuje konkrétní NF-e, je hlavním odeslání. Odeslání, které požaduje zrušení stejného NF-e v SEFAZ, je souvisejícím odesdláním. Existuje pouze proto, že požaduje zrušení úlohy, která byla provedena jiným odesláním.

    Stránka **Související odeslání** zobrazuje všechna související odeslání a jejich stav odeslání pro daný fiskální dokument. Na následujícím obrázku představuje první řádek odeslání, které požadovalo schválení fiskálního dokumentu. Druhý řádek představuje odeslání, které zrušilo daný fiskální dokument.

    ![Zobrazit protokoly odeslání zrušení](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. V podokně akcí vyberte **Dotazy \> Podrobnosti o odeslání** pro zobrazení podrobností o protokolech provádění odeslání.

    ![Zobrazení podrobností protokolu odeslání zrušení](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů
Povolení funkce BR-00053 (NF-e Federal) může vyžadovat odesílání omezených dat, která zahrnují daňové identifikační číslo organizace. To bude předáno agenturám třetích stran oprávněným daňovým úřadem pro účely zasílání elektronických faktur tomuto daňovému úřadu v předdefinovaném formátu požadovaném pro integraci s webovými službami těchto vlád. Správce může povolit a zakázat funkci BR-00053 (NF-e Federal) přechodem na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**. Vyberte kartu **Funkce**, vyberte řádek obsahující funkci BR-00053 a poté proveďte příslušný výběr. Data importovaná z těchto externích systémů do této online služby Dynamics 365 podléhají našim [Prohlášením o ochraně osobních informací](https://go.microsoft.com/fwlink/?LinkId=512132). Další informace najdete v oddílech Oznámení o ochraně osobních údajů v dokumentaci funkcí pro jednotlivé země.


## <a name="additional-resources"></a>Další prostředky

- [Přehled doplňku Elektronická fakturace](e-invoicing-service-overview.md)
- [Začněte s doplňkem elektronické fakturace](e-invoicing-get-started.md)
- [Nastavení doplňku Elektronická fakturace](e-invoicing-setup.md)

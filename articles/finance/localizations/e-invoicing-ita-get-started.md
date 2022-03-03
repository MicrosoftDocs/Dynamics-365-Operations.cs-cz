---
title: Začínáme s Elektronickou fakturací pro Itálii
description: Toto téma poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Itálii.
author: gionoder
ms.date: 09/22/2020
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
ms.openlocfilehash: c0197ff9d93833aa50fef56ec597fa0c904d792d
ms.sourcegitcommit: 8bcb9c13eccb14e61c39ca6578d135b64090fad2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2022
ms.locfileid: "8313636"
---
# <a name="get-started-with-electronic-invoicing-for-italy"></a>Začínáme s Elektronickou fakturací pro Itálii

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Elektronická fakturace pro Itálii nemusí aktuálně podporovat všechny funkce, které jsou k dispozici pro elektronické faktury v Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management. 

Toto téma poskytuje informace, které vám pomohou začít s Elektronickou fakturací pro Itálii. Provede vás konfiguračními kroky, které jsou závislé na zemi v Regulatory Configuration Services (RCS) a Finance. Rovněž vás provede procesem odesílání elektronických faktur, které jsou generovány ve formátu **FatturaPA** specifického pro Itálii prostřednictvím služby a vysvětluje, jak zkontrolovat výsledky zpracování.

## <a name="prerequisites"></a>Předpoklady

Než dokončíte kroky v tomto tématu, musíte provést kroky v [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>Nastavení RCS

Během instalace RCS dokončíte tyto úlohy:

1. Naimportujte funkci elektronické fakturace pro export elektronických faktur zákazníků ve formátu **FatturaPA**.
2. Zkontrolujte konfigurace formátu, které jsou vyžadovány pro generování, odesílání a přijímání odpovědí o elektronických fakturách.
3. Nakonfigurujte události, které podporují scénáře odeslání elektronické faktury.
4. Publikování funkce elektronické fakturace.

> [!NOTE]
> „Funkce elektronické fakturace“ je obecný název prostředku, který je nakonfigurován a publikován tak, aby využíval server Elektronické fakturace. V tomto případě je export elektronických faktur zákazníků funkce elektronické fakturace, kterou nastavíte.

## <a name="import-the-e-invoicing-feature"></a>Import funkce elektronické fakturace

1. Přihlaste se k účtu RCS.
2. V pracovním prostoru **Funkce globalizace** v části **Funkce** vyberte dlaždici **elektronická fakturace**.
3. Na stránce **Funkce elektronické fakturace** vyberte **Import**, chcete-li importovat funkci elektronické fakturace z globálního úložiště.

    > [!NOTE]
    > Pokud nevidíte seznam dostupných funkcí, vyberte **Synchronizovat**. 

4. Vyberte funkci **Export eletronických faktur (IT)** a vyberte **Import**.

![Import funkce exportu elektronických faktur (IT).](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

Při importu funkce **Export elektronických faktur (IT)** z globálního úložiště, importují se také všechna nastavení, která jsou popsána v následujících částech.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>Vytvořte novou verzi funkce Exportu eletronických faktur (IT)

1. Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte **Nový**. 

    ![Přidání nové verze funkce elektronické fakturace.](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Dále nakonfigurujete formáty elektronických zpráv (ER), které jsou spojeny s funkcí elektronické fakturace.

2. Na kartě **Konfigurace** vyberte **Přidat** ke správě verzí konfigurace.

    ![Správa verzí konfigurace funkcí elektronické fakturace.](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    V tomto kroku přidáváte a konfigurujete formáty ER různých souborů, které se používají k exportu italských elektronických faktur. U italských elektronických faktur FatturaPA použijte buď následující standardní konfigurace, nebo skutečné přizpůsobené konfigurace, které používáte pro elektronickou fakturaci:

    - Prodejní faktura (IT)
    - Projektová faktura (IT)

    Když vytvoříte funkci elektronické fakturace, která je odvozena z jiné funkce elektronické fakturace, všechny formáty ER se zdědí z původní funkce.

3. Vyberte konkrétní konfiguraci souboru formátu ER.
4. Vyberte **Upravit** nebo **Zobrazit** a otevřete stránku **Návrhář formátů**.

    ![Otevření stránky Návrhář formátu.](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. Použijte stránku **Návrhář formátů**, chcete-li upravovat a prohlížet konfigurace souborů ve formátu ER.

    ![Stránka návrháře formátu.](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Spravujte nastavení funkce elektronické fakturace

- Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** vyberte **Přidat**, **Odebrat** nebo **Upravit** ke správě nastavení funkcí elektronické fakturace.

![Správa nastavení funkce elektronické fakturace.](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

V tomto kroku nakonfigurujete události, které se vztahují na elektronické faktury, včetně generování výstupních souborů XML ve formátu **FatturaPA** a digitální podepisování (je-li požadováno).

### <a name="configure-the-sales-invoice-feature-setup"></a>Nakonfigurujte nastavení funkce prodejní faktury

1. Na stránce **Funkce elektronické fakturace** na kartě **Nastavení** ve sloupci **Nastavení funkce** vyberte **Prodejní faktura**.
2. Vyberte možnost **Upravit**.
3. Na stránce **Nastavení verze funkce** vyberte kartu **Akce** pro správu seznamu akcí. Akce definují seznam operací, které je nutné spustit v postupném pořadí, aby bylo možné provést úplné provedení události.

    ![Karta Akce.](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | ID akce | Název akce        | Popis akce                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Transformovat dokument | Vytvořte soubor XML e-faktury ve formátu **FatturaPA**. |
    | 2         | Podepsat dokument      | Aplikujte digitální podpis na soubor XML.             |

4. Vyberte kartu **Pravidla použitelnosti** pro zobrazení a udržování pravidel použitelnosti. Pravidla použitelnosti definují kontext, kde bude akce spuštěna.

    ![Karta Pravidla použitelnosti.](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Vyberte kartu **Proměnné** pro zobrazení a údržbu proměnných.

    ![Karta Proměnné.](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. Definujte veřejné proměnné, které jsou nutné ke spuštění akcí.

### <a name="configure-the-project-invoice-feature-setup"></a>Nakonfigurujte nastavení funkce projektové faktury 

Kroky a nastavení, které jsou nutné ke konfiguraci nastavení funkce **Projektová faktura** je velmi podobné krokům a nastavením pro nastavení funkce **Prodejní faktura**. Když pracujete s projektovými fakturami, přečtěte si postupy pro prodejní faktury.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>Přiřaďte funkci elektronické fakturace k prostředí

1. Na stránce **Funkce elektronické fakturace** na kartě **Prostředí** vyberte **Povolit**.
2. V poli **Prostředí** vyberte prostředí.
3. V poli **Platí od** vyberte datum, kdy má začít platnost prostředí.
4. Vyberte **Povolit**. 

![Povolení prostředí elektronické fakturace.](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>Publikování funkce elektronické fakturace

Funkci elektronické fakturace můžete publikovat změnou stavu verze na **Dokončeno** nebo **Publikováno**.

### <a name="change-the-version-status-to-completed"></a>Změna stavu verze na Dokončeno.

1. Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte verzi funkce elektronické fakturace, která má stav **Koncept**.
2. Vyberte **Změnit stav \> Dokončeno**. 

### <a name="change-the-version-status-to-published"></a>Změna stavu verze na Publikováno. 

1. Na stránce **Funkce elektronické fakturace** na kartě **Verze** vyberte verzi funkce elektronické fakturace, která má stav **Dokončeno**.
2. Vyberte **Změnit stav \> Publikovat**.

![Změna stavu funkce elektronické fakturace.](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-integration-in-finance"></a>Nastavení integrace Elektronické fakturace ve Finance

Během instalace Finance dokončíte tyto úlohy:

1. Importujte datový model ER, mapování datového modelu ER a kontextové konfigurace pro e-faktury FatturaPA.
2. Nakonfigurujte certifikát, který je vyžadován k digitálnímu podepisování italských elektronických faktur.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>Importujte datový model ER, mapování datového modelu a formáty

1. V pracovním prostoru **Elektronické výkaznictví**, ověřte, že poskytovatel konfigurace **Služba obchodních dokumentů** je nastaven na **Aktivní**.
2. Vyberte **Úložiště**.
3. Vyberte **Globální prostředek \> Otevřít**.
4. Importujte **Model faktury**, **Mapování modelu faktury** a **Kontextový model faktury zákazníka**.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>Zapněte funkci pro export elektronických faktur zákazníků pro Itálii

1. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.
2. Na kartě **Funkce** zaškrtněte políčko **Povoleno** v řádku pro odkaz na funkci **IT00036**.

![Zapnutí funkce FatturaPA.](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Konfigurace elektronických dokumentů

1. Přejděte na **Správa organizace \> Nastavení \> Parametry elektronického dokumentu**.
2. Na kartě **Elektronický dokument** vyberte **Přidat** a zadejte tabulky, které jsou nutné pro generování italských elektronických faktur:

    - **Název tabulky:** Deník faktury zákazníka
    - **Název tabulky:** Projektová faktura

3. Pro každou tabulku definujte související kontext dokumentu:

    - Pro **Deník faktury zákazníka** vyberte **Kontext faktury zákazníka**.
    - Pro **Faktura projektu** vyberte **Kontext faktury projektu**.

![Nastavení typů odpovědí.](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>Zpracování elektronických faktur

Během zpracování ve Finance dokončíte tyto úlohy:

1. Generování italských e-faktur prostřednictvím Elektronické fakturace
2. Zobrazte protokoly o provedení a zkontrolujte výsledky zpracování.

### <a name="generate-electronic-invoices"></a>Generujte elektronické faktury

Po zapnutí funkce **Konfigurovatelná integrace Elektronické fakturace** a aktivaci funkce **IT00036** již nelze použít starý proces pro generování italských elektronických faktur ve Finance. Je nahrazen novým procesem, který je pojmenován **Odesílejte elektronické dokumenty**.

Dokumenty můžete odeslat ručně na základě vašeho požadavku na dokumenty elektronické faktury.

> [!NOTE]
> Než budete pokračovat, ověřte, že bylo dokončeno nastavení požadované pro italské elektronické faktury. Další informace naleznete v tématu [Zákaznické elektronické faktury](./emea-ita-e-invoices.md). Uvědomte si, že některé kroky nastavení popsané v tomto tématu nemusí být k dispozici z důvodu aktivace Elektronické fakturace.

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Odesílejte elektronické dokumenty**.
2. Pro první odeslání jakéhokoli dokumentu nastavte možnost **Znovu odeslat dokumenty** na **Ne**. Pokud musíte znovu odeslat dokument prostřednictvím služby, nastavte tuto možnost na **Ano**.
3. Na pevné záložce **Záznamy, které mají být zahrnuty** vyberte **Filtr** a otevřete dialogové okno **Dotaz**, kde můžete vytvořit dotaz pro výběr dokumentů k odeslání.

![Dialogové okno Odeslat elektronické dokumenty.](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Dotaz filtru

1. V dialogovém okně **Dotaz** nakonfigurujte podmínky filtrování prodejních faktur i projektových faktur nebo ponechte podmínky prázdné, aby zahrnovaly všechny neodeslané faktury.

    ![Nastavení kritérií filtru odeslání.](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. Zvolte **OK** a zavřete dialogové okno **Dotaz**.
3. Vyberte **OK** k odeslání vybraných dokumentů.

> ![POZNÁMKA] Během prvního pokusu o odeslání dokumentu prostřednictvím služby budete vyzváni k potvrzení spojení s Elektronickou fakturací. Vyberte **Klikněte zde pro připojení ke službě elektronického odesílání dokumentů**.

#### <a name="view-submission-logs"></a>Zobrazit protokoly odeslání

Můžete si prohlédnout protokoly o odeslání pro všechny odeslané dokumenty.

1. Přejděte na **Správa organizace \> Periodické \> Elektronické dokumenty \> Protokol o odeslání elektronických dokumentů**.
2. V poli **Typ dokumentu** vyberte **Deník faktury zákazníka** nebo **Faktura projektu**, chcete-li filtrovat požadované elektronické dokumenty.

    ![Výběr typu dokumentu pro zobrazení protokolů odeslání.](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    Hodnota, která je uvedena ve sloupci **Stav odeslání** představuje stav procesu odesílání. Označuje, zda byl proces spuštěn tak, jak byl nakonfigurován, a zda je vyžadována další akce.

3. V podokně akcí vyberte **Dotazy \> Podrobnosti o odeslání** pro zobrazení podrobností o protokolech provádění odeslání.

    ![Zobrazení podrobností protokolu odeslání.](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. Na pevné záložce **Zpracování akcí** můžete zobrazit protokol provádění akcí, které jsou konfigurovány ve verzi funkce, která byla nastavena v RCS. Sloupec **Stav** ukazuje, zda byla akce úspěšně spuštěna.
5. Na pevné záložce **Soubory akcí** můžete zobrazit přechodné soubory, které byly vygenerovány během provádění akcí. Můžete vybrat **Zobrazit** a stáhnout výstupní soubor XML ve formátu **FatturaPA** a zobrazit jeho obsah.

## <a name="related-topics"></a>Související témata

- [Přehled elektronické fakturace](e-invoicing-service-overview.md)
- [Začínáme s Elektronickou fakturací](e-invoicing-get-started.md)
- [Nastavení Elektronické fakturace](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

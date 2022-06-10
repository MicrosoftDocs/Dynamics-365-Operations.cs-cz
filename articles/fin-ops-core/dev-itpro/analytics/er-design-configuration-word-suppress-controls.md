---
title: Potlačit ovládací prvky obsahu Word v generovaných sestavách
description: Toto téma vysvětluje, jak konfigurovat formát elektronického výkaznictví (ER) pro generování zpráv jako souborů Microsoft Word, kde jsou potlačeny ovládací prvky obsahu.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 2c2d79c9ea36c42cfc0f6ba0d3c81d063d8d9446
ms.sourcegitcommit: 6c1bf233748c4bc70fc5a1a9711758cdfd9e07dc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782169"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Potlačit ovládací prvky obsahu Word v generovaných sestavách

[!include [banner](../includes/banner.md)]

Chcete-li generovat sestavy jako dokumenty Microsoft Word, musíte navrhnout šablonu pro zprávy jako dokument aplikace Word. Tato šablona musí obsahovat ovládací prvky obsahu Word jako zástupné symboly pro data, která budou vyplněna za běhu. Chcete-li použít vytvořený dokument Word jako šablonu pro své sestavy, můžete [nakonfigurovat](er-design-configuration-word.md) nové [řešení](er-quick-start1-new-solution.md) [elektronického výkaznictví (ER)](general-electronic-reporting.md). Řešení musí obsahovat [konfiguraci](general-electronic-reporting.md#Configuration) ER, která obsahuje komponentu formát ER. Tento formát ER musí být nakonfigurován pro použití navržené šablony pro generování sestav.

Ve verzi Dynamics 365 Finance 10.0.6 a novější můžete nakonfigurovat vzorce ve formátu ER tak, aby potlačily některé ovládací prvky obsahu Word v generovaných dokumentech.

Následující kroky vysvětlují, jak může uživatel, který je přiřazen správci systému nebo roli konzultanta funkčních elektronických zpráv, nakonfigurovat formát ER, který generuje sestavy jako soubory aplikace Word a potlačuje některé ovládací prvky obsahu v generovaných sestavách, které byly konfigurovány pomocí šablony Word.

Tyto kroky lze provést v rámci společnosti GBSI.

## <a name="prerequisites"></a>Předpoklady

K provedení těchto kroků je nutné nejprve provést kroky v následujících průvodcích:

- [Návrh konfigurace pro generování sestav ve formátu OPENXML](./tasks/er-design-reports-openxml-2016-11.md)
- [Opětovné použití konfigurací elektronického výkaznictví s šablonami Excel pro generování sestav ve formátu Word](./tasks/er-design-configuration-word-2016-11.md)

Po dokončení kroků v těchto průvodcích úkoly jsou připraveny následující položky:

- Formát ER **Vzorová sestava listu**, která je nakonfigurována pro generování dokumentu ve formátu Word
- Verze [konceptu](general-electronic-reporting.md#component-versioning) formátu ER **Vzorové sestavy listu**, který je označen jako **Spustitelný**
- **Elektronický** způsob platby, který je nakonfigurován pro použití formátu ER **Vzorové sestavy listu** pro zpracování plateb dodavatele

Musíte si také stáhnout a uložit následující šablonu pro vzorovou sestavu:

- [Vázaná šablona 2 sestavy platby (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/1/9/b/19b36e39-861a-414e-9150-9880d9d2487c/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>Kontrola stažené šablony Wordu

1. V desktopové aplikaci Word otevřete soubor šablony **SampleVendPaymDocReportBounded2.docx**, který jste stáhli dříve.
2. Ověřte, zda soubor šablony obsahuje souhrnnou část, která zobrazuje celkové částky plateb pro každý kód měny, který byl zjištěn ve zpracovaných platbách.

    - Souhrnná část je umístěna v samostatné tabulce dokumentu aplikace Word.
    - První řádek této tabulky obsahuje záhlaví sloupců tabulky jako záhlaví sekce.
    - Druhý řádek této tabulky obsahuje ovládací prvek opakujícího se obsahu jako podrobnosti sekce.
    - Tento ovládací prvek obsahu je namapován na pole **Souhrnné řádky** vlastní části XML **sestavy**.
    - Na základě tohoto mapování je ovládací prvek obsahu přidružen k prvku **SummaryLines** upravitelného formátu ER.

    > [!NOTE]
    > Opakující se ovládací prvek obsahu je označen klíčem **SummaryLines**, který odpovídá poli vlastní části XML, na kterou byl namapován.

    ![Rozložení šablony Word.](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Volba existující konfigurace sestavy ER

V následujících krocích znovu použijete stávající konfiguraci ER, kterou jste nakonfigurovali, když jste provedli kroky v dříve zmíněných průvodcích úkoly.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Vyberte **Konfigurace vykazování**.
3. Na stránce **Konfigurace** ve stromu konfigurací rozbalte položku **Model platby** a poté vyberte možnost **Vzorová sestava listu**.
4. Vyberte **Návrhář** k úpravě verze konceptu vybraného formátu ER.

## <a name="replace-the-current-template-with-the-new-template"></a>Výměna aktuální šablony za novou šablonu

V současné době se používá soubor SampleVendPaymDocReportBounded.docx jako šablona pro generování výstupu ve formátu Word. V následujícím postupu tuto šablonu Word nahradíte novým souborem šablony Word SampleVendPaymDocReportBounded2.docx, kterou jste předtím stáhli.

1. Na stránce **Návrhář formátu** zvolte **Přílohy**.
2. Na stránce **Přílohy** vyberte **Odstranit** pro odebrání existující šablony.
3. Vyberte **Ano** pro potvrzení odstranění.
4. Vyberte **Nový** \> **Soubor**.
5. Vyberte **Procházet** a poté přejděte na a vyberte soubor **SampleVendPaymDocReportBounded2.docx**, který jste stáhli dříve.
6. Vyberte **OK**.
7. Zavřete stránku **Přílohy**.
8. Na stránce **Návrhář formátů** do pole **Šablona** zadejte nebo vyberte soubor **SampleVendPaymDocReportBounded2.docx**.

## <a name="run-the-format-to-create-word-output"></a>Spuštění formátu pro vytvoření výstupu ve Wordu

1. Přejděte na **Závazky** \> **Platby** \> **Deník plateb**.
2. Na stránce **Platby dodavatele** na kartě **Seznam** vyberte všechny platby.
3. Vyberte **Stav platby** \> **Žádný**.
4. Vyberte **Generovat platby**.
5. V poli **Způsob platby** vyberte **Elektronický**.
6. V poli **Bankovní účet** vyberte **GBSI OPER**.
7. Vyberte **OK**.
8. V dialogovém okně **Parametry elektronického přiznání** vyberte **OK** a analyzujte vygenerovaný výstup.

    ![Platby za zpracování na stránce Platby dodavatele.](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Výstup je prezentován ve formátu Word a obsahuje souhrnnou část.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Nakonfigurujte upravitelný formát tak, aby potlačil část shrnutí

Pokud chcete potlačit souhrnnou část v generovaném dokumentu na základě požadavku uživatele, který spouští tento formát ER, musíte upravit upravitelný formát ER.

1. Přejděte do **Správa organizace** \> **Pracovní prostory** \> **Elektronické hlášení** a otevřete koncept verzi formátu ER pro úpravy.
2. Vyberte **Konfigurace vykazování**. 
3. Na stránce **Konfigurace** ve stromu konfigurací rozbalte položku **Model platby** \> **Vzorová sestava listu**.
4. Vyberte možnost **Návrhář**.
5. Na stránce **Návrhář formátů** rozbalte **Word** a vyberte **SummaryLines**.
6. Na kartě **Mapování** přidejte nový zdroj dat, abyste se za běhu uživatele zeptali, zda má být souhrnná část potlačena:

    1. Vyberte **Přidat kořen**.
    2. V dialogovém okně **Přidat zdroj dat** vyberte **Obecné\Uživatelský vstupní parametr** a otevřete dialogové okno **Vlastnosti zdroje dat „Uživatelský vstupní parametr“**.
    3. Do pole **Název** zadejte **uipSuppress**.
    4. Do pole **Označení** zadejte **Potlačit část shrnutí**.
    5. V poli **Název provozního datového typu** vyberte nebo zadejte **NoYes**.
    6. Vyberte **OK**.

7. Přidání nového zdroje dat typu výčtu aplikace **NoYes**:

    1. Vyberte **Přidat kořen**.
    2. V dialogovém okně **Přidat zdroj dat** vyberte **Dynamics 365 for Operations\Výčet** k otevření dialogového okna **Vlastnosti zdroje dat „výčet“**.
    3. Do pole **Název** zadejte **enumNoYes**.
    4. Do pole **Označení** zadejte **Potlačit možnosti**.
    5. V poli **Název provozního datového typu** vyberte nebo zadejte **NoYes**.
    6. Vyberte **OK**.

8. Pro vybraný prvek formátu **Souhrnné řádky** nakonfigurujte vzorec tak, aby určoval, kdy má být potlačen ovládací prvek obsahu Word, který je přidružen k vybranému prvku formátu:

    1. Na kartě **Mapování** v části **Odstraněno** vyberte **Upravit** k otevření stránky **[Návrhář vzorců](general-electronic-reporting-formula-designer.md)**.
    2. V poli **Vzorec** zadejte vzorec `uipSuppress = enumNoYes.Yes`.
    3. Vyberte **Uložit** a zavřete stránku **Návrhář vzorců**.

        > [!NOTE]
        > Tento vzorec se použije na vygenerovaný dokument **po spuštění všech ostatních prvků formátu**. Chcete-li použít tento vzorec, ovládací prvek obsahu Word, který je označen jako prvek formátu, pro který je vzorec nakonfigurován (**SummaryLines** v tomto případě) se nachází ve vygenerovaném dokumentu. Tento ovládací prvek obsahu je poté zcela odstraněn společně s řádkem v tabulce Word, který ho obsahuje. Řádek podrobností části souhrnu je odstraněn z vygenerovaného dokumentu.
        >
        > V době návrhu můžete nakonfigurovat vzorec **Odstraněno** pro prvek formátu, přestože žádný ovládací prvek obsahu v šabloně Word, který používáte, nemá značku, která odpovídá názvu prvku formátu, pro který je vlastnost **Odstraněno** nakonfigurována. Když ověříte formát v době návrhu, obdržíte a [varování](er-components-inspections.md#i14) o této nesrovnalosti.
        >
        > Za běhu je vyvolána výjimka, pokud žádný ovládací prvek obsahu v šabloně Word, který používáte, nemá značku, která odpovídá názvu prvku formátu, pro který je **odstraněná** nakonfigurována.

    4. Na kartě **Mapování** v části **Odstraněno** nastavte možnost **S nadřazeným** na **Ano**.

        > [!NOTE]
        > Tuto možnost musíte nastavit na **Ano**, abyste odebrali celou tabulku Word jako nadřazený objekt řádku, který obsahuje podrobnosti souhrnné sekce. Pokud nastavíte tuto možnost na **Ne**, řádek záhlaví sekce zůstane v generovaném dokumentu.

9. Změny upravitelného formátu uložíte výběrem možnosti **Uložit**.

    ![Generovaný výstup ve formátu Word.](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Spuštění upraveného formátu pro vytvoření výstupu ve Wordu

1. Přejděte na **Závazky** \> **Platby** \> **Deník plateb**.
2. Vyberte deník plateb, který jste vytvořili, a poté vyberte **Řádky**.
3. Na stránce **Platby dodavatele** vyberte všechny řádky a poté vyberte **Stav platby** \> **Žádný**.
4. Vyberte **Generovat platby**.
5. V poli **Způsob platby** vyberte **Elektronický**.
6. V poli **Bankovní účet** vyberte **GBSI OPER**.
7. Vyberte **OK**.
8. V dialogovém okně **Parametry elektronického přiznání** v poli **Potlačit část shrnutí** vyberte **Ano**.
9. Vyberte **OK** a analyzujte vygenerovaný výstup.

    ![Generovaný výstup ve formátu Word.](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Všimněte si, že výstup neobsahuje souhrnnou část, protože byla potlačena.

## <a name="additional-resources"></a>Další prostředky

- [Návrh konfigurace pro generování sestav ve formátu OPENXML](./tasks/er-design-reports-openxml-2016-11.md)
- [Návrh nové konfigurace elektronického výkaznictví pro generování sestav ve formátu Word](er-design-configuration-word.md)
- [Opětovné použití konfigurací elektronického výkaznictví s šablonami Excel pro generování sestav ve formátu Word](./tasks/er-design-configuration-word-2016-11.md)
- [Kontrola konfigurované komponenty ER zabraňující problémům za běhu](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

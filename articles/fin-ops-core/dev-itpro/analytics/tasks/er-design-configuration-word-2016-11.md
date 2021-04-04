---
title: Opětovné použití konfigurace ER se šablonami aplikace Excel ke generování zpráv ve formátu Word
description: Toto téma popisuje, jak lze konfigurovat formáty sestav, které byly navrženy ke generování sestav jako sešitů aplikace Excel, aby generovaly sestavy jako dokumenty Word.
author: NickSelin
manager: AnnBe
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 601896bad72b079759b1a07efba8717101e94362
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569304"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>Opětovné použití konfigurace ER se šablonami aplikace Excel ke generování zpráv ve formátu Word

[!include [banner](../../includes/banner.md)]

Pokud chcete generovat sestavy jako dokumenty Microsoft Word, můžete [nakonfigurovat](../er-design-configuration-word.md) nový [formát elektronického výkaznictví (ER)](../general-electronic-reporting.md) [formát](../general-electronic-reporting.md#FormatComponentOutbound). Alternativně můžete znovu použít formát ER, který byl původně navržen pro generování sestav jako sešity aplikace Excel. V takovém případě musíte nahradit šablonu aplikace Excel šablonou aplikace Word.

Následující postupy ukazují, jak může uživatel v roli správce systému nebo v roli vývojáře elektronických sestav konfigurovat formát ER tak, aby generoval sestavy jako soubory Word, a to opětovným použitím formátu ER, který byl navržen pro generování sestav jako souborů Excel.

Tyto postupy lze provést v rámci společnosti GBSI.

## <a name="prerequisites"></a>Předpoklady

Pro dokončení těchto postupů musíte nejprve provést kroky v průvodci záznamem úloh [Návrh konfigurace ke generování sestav ve formátu OPENXML](er-design-reports-openxml-2016-11.md).

Musíte si také stáhnout a místně uložit následující šablony pro vzorovou sestavu:

- [Šablona sestavy platby (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=862266)
- [Vázaná šablona sestavy platby (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=862266)

Tyto postupy jsou pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611 (listopad 2016).

## <a name="select-the-existing-er-report-configuration"></a>Volba existující konfigurace sestavy ER

1. V Dynamics 365 Finance přejděte na **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Ujistěte se, že je poskytovatel konfigurace **Litware, Inc.** vybrán jako **Aktivní**. Pokud tomu tak není, postupujte podle pokynů v průvodci záznamem úloh [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).
3. Vyberte **Konfigurace vykazování**. Znovu použijete existující konfiguraci ER, která byla původně navržena ke generování výstupu sestavy ve formátu OPENXML.
4. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a poté vyberte možnost **Vzorová sestava listu**.

    > [!NOTE]
    > Verzi konceptu vybraného formátu ER lze upravit na kartě s náhledem **Verze**.

5. Vyberte možnost **Návrhář**.
6. Na stránce **Návrhář formátů** si všimněte, že nadpis prvku kořenového formátu označuje, že je aktuálně používána šablona aplikace Excel.

![Výběr existující konfigurace sestavy ER](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>Kontrola stažené šablony Wordu

1. V desktopové aplikaci Word otevřete soubor šablony **SampleVendPaymDocReport.docx**, který jste stáhli dříve.
2. Ověřte, že tato šablona obsahuje pouze rozvržení dokumentu, který chcete generovat jako ER výstup.

![Rozvržení šablony Word v desktopové aplikaci](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Nahrazení šablony aplikace Excel šablonou aplikace Word a přidání vlastní části XML

V současné době se používá dokument Excel jako šablona pro generování výstupu ve formátu OPENXML. Tuto šablonu nahradíte souborem šablony Word SampleVendPaymDocReport.docx Word, kterou jste předtím stáhli. Také provedete rozšíření šablony aplikace Word přidáním vlastní části XML.

1. V modulu Finance na stránce **Návrhář formátu** na kartě **Formát** vyberte **Přílohy**.
2. Na stránce **Přílohy** vyberte **Odstranit** pro odebrání existující šablony Excel. Vyberte **Ano**, chcete-li potvrdit změnu.
3. Vyberte **Nový** \> **Soubor**.

    > [!NOTE]
    > Musíte vybrat typ dokumentu, který je [konfigurován](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) v parametrech ER k uložení šablon formátů ER.

4. Vyberte **Procházet** a poté přejděte na a vyberte soubor **SampleVendPaymDocReport.docx**, který jste stáhli dříve.
5. Vyberte **OK**.
6. Zavřete stránku **Přílohy**.
7. Na stránce **Návrhář formátu** v poli **Šablona** zadejte nebo vyberte soubor **SampleVendPaymDocReport.docx** k použití této šablony Word místo šablony Excel, která byla použita předtím.
8. Zvolte **Uložit**.

    Kromě uložení změn v konfiguraci aktualizuje připojenou šablonu aplikace Word rovněž akce **Uložit**. Hierarchická struktura navrženého formátu je přenesena do připojeného dokumentu aplikace Word jako nová vlastní část XML s názvem **Sestava**. Všimněte si, že připojená šablona aplikace Word obsahuje nejen rozvržení dokumentu, který bude generován jako výstup ER, ale zároveň i strukturu dat, která budou ER předána do této šablony za běhu.

9. Všimněte si, že nadpis prvku kořenového formátu označuje, že je aktuálně používána šablona aplikace Word.

    ![Nahrazení šablony aplikace Excel šablonou aplikace Word a přidání vlastní části XML](../media/er-design-configuration-word-2016-11-image03.gif)

10. Na kartě **Formát** vyberte **Přílohy**.

Nyní můžete namapovat prvky vybrané vlastní části XML **Sestava** a ovládacích prvků obsahu dokumentu aplikace Word.

okud jste obeznámeni s dokumenty Word, které lze navrhovat jako formuláře obsahující [ovládací prvky obsahu](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) namapované na prvky [vlastních částí XML](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), proveďte všechny kroky dalšího dílčího úkolu pro vytvoření takového dokumentu. Další informace naleznete v tématu [Vytvoření formulářů, které uživatelé dokončí nebo vytisknou v aplikaci Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b). Jinak následující postup přeskočte.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Získání dokumentu Word, který má vlastní část XML, a mapování dat

1. Ve Finance na stránce **Přílohy** vyberte **Otevřít** ke stažení vybrané šablony z Finance a jejímu místnímu uložení jako dokumentu Word.
3. V desktopové aplikaci Word otevřete dokument, který jste právě stáhli.
4. Na kartě **Vývojář** vyberte **podokno mapování XML**.

    > [!NOTE]
    > Pokud se karta **Vývojář** nezobrazí na pásu karet, přizpůsobte jej a přidejte ji.

5. V podokně **Mapování XML** v poli **Vlastní část XML** vyberte část Vlastní XML **Sestava**.
6. Namapujte prvky vybrané vlastní části XML **Sestava** a ovládací prvky obsahu dokumentu aplikace Word.
7. Aktualizovaný dokument Word uložte místně jako **SampleVendPaymDocReportBounded.docx**.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Zkontrolujte šablonu Word, kde je vlastní část XML namapována na ovládací prvky obsahu

1. V desktopové aplikaci Word otevřete soubor šablony **SampleVendPaymDocReportBounded.docx**, který jste stáhli dříve.
2. Ověřte, že tato šablona obsahuje rozvržení dokumentu, který chcete generovat jako ER výstup. Ovládací prvky obsahu, které se používají jako zástupné symboly pro data, která ER za běhu zadá do této šablony, jsou založeny na mapování, která jsou konfigurována mezi vlastní částí XML **Sestava** a ovládacími prvky obsahu dokumentu Word.

![Náhled šablony Word v desktopové aplikaci](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Nahrajte šablonu Word, kde je vlastní část XML namapována na ovládací prvky obsahu

1. Ve Finance na stránce **Přílohy** vyberte **Odstranit** k odebrání šablony Word, která nemá mapování mezi prvky vlastní části XML **Sestava** a ovládacími prvky obsahu. Vyberte **Ano**, chcete-li potvrdit změnu.
2. Výběrem možností **Nový** \> **Soubor** přidejte nový soubor šablony, který obsahuje mapování mezi vlastním prvkem XML **Sestava** a ovládacími prvky obsahu.

    > [!NOTE]
    > Musíte vybrat typ dokumentu, který je [konfigurován](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) v parametrech ER k uložení šablon formátů ER.

3. Vyberte **Procházet** a poté přejděte na a vyberte soubor **SampleVendPaymDocReportBounded.docx**, který jste stáhli nebo připravili pomocí dokončení postupu v části [Získání souboru Word, který má vlastní část XML k mapování](#get-word-doc).
4. Vyberte **OK**.
5. Zavřete stránku **Přílohy**.
6. Na stránce **Návrhář formátů** v poli **Šablona** vyberte dokument, který jste právě stáhli.
7. Zvolte **Uložit**.
8. Zavřete stránku **Návrhář formátu**.

## <a name="mark-the-configured-format-as-runnable"></a>Označení nakonfigurovaného formátu jako spustitelného

Chcete-li spustit rámcovou verzi upravitelného formátu, musíte ji nastavit jako [spustitelnou](../er-quick-start2-customize-report.md#MarkFormatRunnable).

1. V aplikaci Finance na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
2. V dialogovém okně **Uživatelské parametry** nastavte u možnosti **Spustit nastavení** hodnotu **Ano** a poté stiskněte **OK**.
3. Je-li třeba vyberte možnost **Upravit**, má-li být aktuální stránka editovatelná.
4. Pro aktuálně vybranou konfiguraci **Ukázková sestava listu** nastavte možnost **Spustit koncept** na **Ano**.
5. Zvolte **Uložit**.

## <a name="run-the-format-to-create-output-in-word-format"></a>Spuštění formátu pro vytvoření výstupu ve formátu Word

1. V modulu Finance přejděte na **Závazky** \> **Platby** \> **Deník plateb**.
2. V deníku plateb, který jste zadali dříve, vyberte **Řádky**.
3. Na stránce **Platby dodavatele** vyberte všechny řádky v mřížce.
4. Vyberte **Stav platby** \> **Žádný**.

    ![Platby za zpracování na stránce Platby dodavatele](../media/er-design-configuration-word-2016-11-image05.png)

5. V podokně akcí vyberte **Generovat platby**.
6. V rozevíracím dialogovém okně proveďte následující kroky:

    1. V poli **Způsob platby** vyberte **Elektronický**.
    2. V poli **Bankovní účet** vyberte **GBSI OPER**.
    3. Vyberte **OK**.

7. V dialogovém okně **Parametry elektronické sestavy** vyberte **OK**.
8. Generovaný výstup je ve formátu aplikace Word a obsahuje podrobnosti o zpracovaných platbách. Analyzujte vygenerovaný výstup.

    ![Generovaný výstup ve formátu Word](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Další prostředky

- [Návrh nové konfigurace ER pro generování sestav ve formátu Word](../er-design-configuration-word.md)
- [Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
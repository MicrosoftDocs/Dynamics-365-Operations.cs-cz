---
title: Ladění zdrojů dat prováděného formátu ER za účelem analýzy toku dat a transformace
description: Toto téma vysvětluje, jak můžete ladit zdroje dat prováděného formátu ER, aby bylo možné lépe porozumět nakonfigurovanému toku dat a transformaci.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 3a486800f37dda7829aeeaa56a30285a92a61b9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680775"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>Ladění zdrojů dat prováděného formátu ER za účelem analýzy toku dat a transformace

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Když [konfigurujete](tasks/er-format-configuration-2016-11.md) řešení elektronického výkaznictví (ER) ke generování odchozích dokumentů, definujete metody, které se používají k získání dat mimo aplikaci a jejich zadání do generovaného výstupu. Aby byla podpora životního cyklu řešení ER efektivnější, mělo by vaše řešení sestávat z [datového modelu](general-electronic-reporting.md#DataModelComponent) a jeho komponent [mapování](general-electronic-reporting.md#ModelMappingComponent) a také z [formátu](general-electronic-reporting.md#FormatComponentOutbound) ER a jeho komponent mapování, tak, aby mapování modelu bylo specifické pro aplikaci, zatímco ostatní komponenty zůstaly pro aplikaci agnostické. Proto může několik komponent ER [ovlivnit](general-electronic-reporting.md#FormatComponentOutbound) proces zadávání dat do generovaného výstupu.

Někdy vypadají data generovaného výstupu odlišně od stejných dat v aplikační databázi. V těchto případech budete chtít určit, která komponenta ER je zodpovědná za transformaci dat. Funkce ladicího programu zdroje dat ER významně snižuje čas a náklady, které jsou zahrnuty v tomto šetření. Můžete přerušit provádění formátu ER a otevřít rozhraní ladicího programu zdroje dat. Zde můžete procházet dostupné zdroje dat a vybrat individuální zdroj dat pro provedení. Toto ruční provedení simuluje spuštění zdroje dat během skutečného spuštění formátu ER. Výsledek je uveden na stránce, kde můžete analyzovat přijatá data.

Chcete-li zapnout funkci ladění zdroje dat, nastavte možnost **Povolit ladění dat při spuštění formátu** na **Ano** v uživatelských parametrech ER. Poté můžete spustit ladění zdroje dat při spuštění formátu ER pro generování odchozích dokumentů. Také můžete pomocí možnosti **Spustit ladění** zahájit ladění zdroje dat pro formát ER, který je nakonfigurován v [Návrháři operací ER](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).

Toto téma poskytuje pokyny k zahájení ladění zdroje dat pro spuštěné formáty ER. Vysvětluje, jak vám tyto informace mohou pomoci pochopit tok dat a jejich transformace. Příklady v tomto tématu používají obchodní proces pro zpracování plateb dodavatele.

## <a name="limitations"></a>Omezení

Ladicí program zdroje dat lze použít pro přístup k datům zdrojů dat, které se používají ve formátech ER, které jsou spouštěny pro generování odchozích dokumentů. Nelze jej použít k ladění zdrojů dat formátů ER, které jsou navrženy k analýze příchozích dokumentů.

Následující nastavení formátů ER aktuálně nejsou k dispozici pro ladění zdroje dat:

- Transformace formátu
- Pravidla ověření formátování a mapování
- Povolení výrazů
- Podrobnosti o sběru dat v paměti

## <a name="prerequisites"></a>Předpoklady

- Abyste mohli dokončit příklady v tomto tématu, musíte mít přístup k některé z následujících [rolí](../sysadmin/tasks/assign-users-security-roles.md):

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

- Společnost musí být nastavena na **DEMF**.

- Podle pokynů v [příloze 1](#appendix1) tohoto tématu si stáhněte součásti řešení Microsoft ER, které jsou potřeba ke zpracování plateb dodavatele.
- Podle pokynů v [příloze 2](#appendix2) tohoto tématu připravte pohledávky na zpracování platby dodavatele pomocí řešení ER, které si stáhnete.

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>Zpracování platby dodavatele pro účely získání souboru platby

1. Platby dodavatele zpracujte podle kroků v [příloze 3](#appendix3) tohoto tématu.

    ![Probíhá zpracování plateb dodavatele](./media/er-data-debugger-process-payment.png)

2. Stáhněte a uložte soubor zip do místního počítače.
3. Extrahujte soubor platby **ISO20022 Credit transfer.xml** ze souboru zip.
4. Otevřete extrahovaný soubor platby pomocí prohlížeče souborů XML.

    V souboru platby nemá kód IBAN (International Bank Account Number) bankovního účtu dodavatele žádné mezery. Proto se liší od hodnoty, která byla [zadána](#enteredIBANcode) na stránce **Bankovní účty**.

    ![IBAN kód bez mezer](./media/er-data-debugger-payment-file.png)

    Pomocí ladicího programu zdroje dat ER zjistíte, která složka řešení ER se používá ke zkrácení mezer v kódu IBAN.

## <a name="turn-on-data-source-debugging"></a>Zapnutí ladění zdroje dat

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. Nastavte možnost **Povolit ladění dat při spuštění formátu** na **Ano**.

    > [!NOTE]
    > Tento parametr je specifický pro uživatele a konkrétní společnost.

    ![Dialogové okno Parametry uživatele](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>Zpracovat platbu dodavatele pro ladění

1. Platby dodavatele zpracujte podle kroků v [příloze 3](#appendix3) tohoto tématu.
2. V okně zprávy vyberte **Ano** pro potvrzení, že chcete přerušit zpracování plateb dodavatele a místo toho spustit ladění zdrojů dat na stránce **Ladit zdroje dat**.

    ![Pole zprávy s potvrzením](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>Ladění zdrojů dat, které se používají při zpracování plateb

### <a name="debug-the-model-mapping"></a>Ladění mapování modelu

1. Na stránce **Ladit zdroje dat** v podokně Akce vyberte **Mapování modelu** pro zahájení ladění z této komponenty ER.
2. V podokně zdroje dat vlevo vyberte zdroj dat **\$notSentTransactions** zdroj dat a poté vyberte možnost **Přečíst všechny záznamy**.

    Můžete vybrat volbu **Přečíst 1 záznam**, **Přečíst 10 záznamů**, **Přečíst 100 záznamů** nebo **Přečíst všechny záznamy** pro vynucení odpovídajícího počtu záznamů, které mají být načteny z vybraného zdroje dat. Tímto způsobem můžete simulovat přístup ke zdroji dat z běžícího formátu ER.

3. V podokně dat vpravo vyberte **Rozbalit vše**.

    Vidíte, že vybraný zdroj dat typu **Seznam záznamů** obsahuje jeden záznam.

4. Rozbalte zdroj dat **\$notSentTransactions** a vyberte vnořenou metodu **vendBankAccountInTransactionCompany ()**.
5. Rozbalte metodu **vendBankAccountInTransactionCompany()** a vyberte vnořené pole **IBAN**.
6. Vyberte **Získat hodnotu**.

    Můžete vybrat **Získat hodnotu** pro vynucení čtení hodnoty vybraného pole vybraného zdroje dat. Tímto způsobem můžete simulovat přístup do tohoto pole z běžícího formátu ER.

7. Vyberte **Rozbalit vše**.

    ![Hodnota pole IBAN v mapování modelu](./media/er-data-debugger-debugging-model-mapping.png)

    Jak vidíte, mapování modelů není zodpovědné za zkrácené mezery, protože kód IBAN, který vrátí pro bankovní účet dodavatele, zahrnuje mezery. Proto musíte pokračovat v ladění zdroje dat.

### <a name="debug-the-format-mapping"></a>Ladění mapování formátu

1. Na stránce **Ladit zdroje dat** v podokně Akce vyberte **Mapování formátu** pro pokračování v ladění z této komponenty ER.
2. Vyberte zdroj dat **\$PaymentByDebtor** a poté vyberte **Přečíst všechny záznamy**.
3. Rozbalte **\$PaymentByDebtor**.
4. Rozbalte **\$PaymentByDebtor.Lines** a poté vyberte **Přečíst všechny záznamy**.
5. Rozbalte **\$PaymentByDebtor.Lines.CreditorAccount**.
6. Rozbalte **\$PaymentByDebtor.Lines.CreditorAccount.Identification** a vyberte **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.
7. Vyberte **Získat hodnotu**.
8. Vyberte **Rozbalit vše**.

    ![Hodnota pole IBAN v mapování formátu](./media/er-data-debugger-debugging-format-mapping.png)

    Jak vidíte, zdroje dat mapování formátu nejsou zodpovědné za zkrácené mezery, protože kód IBAN, který vrací pro bankovní účet dodavatele, zahrnuje mezery. Proto musíte pokračovat v ladění zdroje dat.

### <a name="debug-the-format"></a>Ladění formátu

1. Na stránce **Ladit zdroje dat** v podokně Akce vyberte **Formát** pro pokračování v ladění z této komponenty ER.
2. Rozbalte elementy formátu pro výběr možností **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** a pak vyberte **Přečíst všechny záznamy**.
3. Rozbalte elementy formátu pro výběr možností **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** a pak vyberte **Přečíst všechny záznamy**.
4. Rozbalte elementy formátu pro výběr možností **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** a pak vyberte **Získat hodnotu**.
5. Vyberte **Rozbalit vše**.

    ![Hodnota pole IBAN ve formátu](./media/er-data-debugger-debugging-format.png)

   Jak vidíte, vázání formátu není zodpovědné za zkrácené mezery, protože kód IBAN, který vrátí pro bankovní účet dodavatele, zahrnuje mezery. Proto je element **BankIBAN** nakonfigurován tak, aby používal transformaci formátu, která zkrátí mezery.

6. Zavřete ladicí program zdroje dat.

### <a name="review-the-format-transformations"></a>Zkontrolujte transformace formátu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** vyberte **Platební model** \> **Převod kreditu ISO20022**.
3. Vyberte **Návrhář** a pak rozbalte elementy pro výběr možností **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.

    ![Element BankIBAN na stránce Návrhář formátu](./media/er-data-debugger-referred-transformation.png)

    Jak vidíte, element **BankIBAN** je nakonfigurován na použití transformace **odstranit ne alfanumerické**.

4. Vyberte kartu **Transformace**.

    ![Karta Transformace pro element BankIBAN](./media/er-data-debugger-transformation.png)

    Jak vidíte, transformace **odstranit nealfanumerické** je nakonfigurována tak, aby používala výraz, který zkrátí mezery z poskytovaného textového řetězce.

## <a name="start-to-debug-in-the-operation-designer"></a>Spusťte ladění v návrháři operací

Když konfigurujete pracovní verzi formátu ER, kterou lze spustit přímo z Návrháře operací, můžete získat přístup k ladicímu programu zdroje dat výběrem možnosti **Spustit ladění** v podokně akcí.

![Tlačítko Spustit ladění na stránce Návrhář formátu](./media/er-data-debugger-run-from-designer.png)

Mapování formátu a komponenty formátu ER, který je upravován, jsou k dispozici pro ladění.

## <a name="start-to-debug-in-the-model-mapping-designer"></a>Spusťte ladění v návrháři mapování modelu

Když konfigurujete mapování modelu ER, které lze spustit ze stránky **Mapování modelu** můžete získat přístup k lacicímu programu zdroje dat výběrem možnosti **Spustit ladění** v podokně akcí.

![Tlačítko Spustit ladění na stránce vývojáře Mapování modelu](./media/er-data-debugger-run-from-designer-mapping.png)

Komponenta mapování modelu mapování ER je k dispozici pro ladění.

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>Příloha 1: Získání řešení ER

### <a name="download-an-er-solution"></a>Stažení řešení ER

Pokud chcete použít řešení ER ke generování elektronického platebního souboru pro platbu zpracovanou prodejcem, můžete si [stáhnout](download-electronic-reporting-configuration-lcs.md) formát platby ER **Převod kreditu ISO20022**, který je k dispozici v knihovně Sdílený majetek ve službě Microsoft Dynamics Lifecycle Services (LCS) nebo v globálním úložišti.

![Import platebního formátu ER na stránce úložiště konfigurace](./media/er-data-debugger-import-from-repo.png)

Kromě vybraného formátu ER musí být následující [konfigurace](general-electronic-reporting.md#Configuration) automaticky importovány do instance Microsoft Dynamics 365 Finance jako součást řešení ER **Převod úvěru ISO20022**:

- **Model platby** [Konfigurace datového modelu ER](general-electronic-reporting.md#DataModelComponent)
- **Převod kreditu ISO20022** [Konfigurace formátu ER](general-electronic-reporting.md#FormatComponentOutbound)
- **Mapování modelu platby 1611** [Konfigurace mapování modelu ER](general-electronic-reporting.md#ModelMappingComponent)
- **Mapování modelu platby do cíle ISO20022** Konfigurace mapování modelu ER

Na stránce **Konfigurace** systému ER (**Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**) najdete následující konfigurace.

![Importované konfigurace na stránce konfigurace](./media/er-data-debugger-configurations.png)

Pokud v konfiguračním stromu chybí některá z dříve uvedených konfigurací, musíte je stáhnout ručně z knihovny sdílených položek LCS stejným způsobem, jakým jste stáhli formát platby ER **Převod kreditu ISO20022**.

### <a name="analyze-the-downloaded-er-solution"></a>Analýza staženého řešení ER

#### <a name="review-the-model-mapping"></a>Kontrola mapování modelu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Vyberte **Platební model** \> **Mapování platebního modelu 1611**.
3. Vyberte možnost **Návrhář**.
4. Vyberte záznam mapování **Mapování platebního modelu ISO20022 CT**.
5. Vyberte **Návrhář** a poté zkontrolujte otevřené mapování modelu.

    Všimněte si, že pole datového modelu **Platby** je vázáno na zdroj dat **\$notSentTransactions**, který vrací seznam zpracovávaných řádků platby dodavatele.

    ![Pole Platby na stránce Návrhář mapování modelů](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>Kontrola mapování formátu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Vyberte **Platební model** \> **Převod kreditu ISO20022**.
3. Vyberte možnost **Návrhář**.
4. Na kartě **Mapování** zkontrolujte otevřené mapování formátu.

    Všimněte si, že je element **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** souboru **ISO20022CTReports** \> **XMLHeader** vázán na zdroj dat **\$PaymentByDebtor**, který je konfigurován na seskupení záznamů pole **Platby** datového modelu.

    ![Element PmtInf na stránce Návrhář formátu](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>Kontrola formátu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Vyberte **Platební model** \> **Převod kreditu ISO20022**.
3. Vyberte **Návrhář** a poté zkontrolujte otevřený formát.

    Všimněte si, že element formátu v části **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** je konfigurován na zadání kódu IBAN účtu dodavatele v souboru platby.

    ![Element BankIBAN na stránce Návrhář formátu](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>Příloha 2: Konfigurace pohledávek

### <a name="modify-a-vendor-property"></a>Změna vlastnosti dodavatele

1. Přejděte do části **Pohledávky** \> **Dodavatelé** \> **Všichni dodavatelé**.
2. Vyberte dodavatele **DE-01002** a pak v podokně akcí na kartě **Dodavatel** ve skupině **Nastavení** vyberte **Bankovní účty**.
3. Na pevné záložce **Identifikace** v okně **IBAN** <a name="enteredIBANcode"></a>zadejte **GB33 BUKB 2020 1555 5555 55**.
4. Zvolte **Uložit**.

![Pole IBAN nastavené na stránce Bankovní účty dodavatele](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>Nastavení způsobu platby

1. Přejděte na **Pohledávky** \> **Nastavení platby** \> **Způsoby platby**.
2. Vyberte způsob platby **SEPA CT**.
3. Na pevné záložce **Formáty souboru** v části **Formáty souboru** nastavte možnost **Obecný formát elektronického exportu** na **Ano**.
4. V poli **Exportovat konfiguraci formátu** vyberte formát **Převod kreditu ISO20022** ER.
5. Zvolte **Uložit**.

![Nastavení formátu souboru na stránce Způsoby platby](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>Přidání platby dodavatele

1. Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.
2. Přidejte nový deník plateb.
3. Vyberte **Řádky** a přidejte nový řádek platby.
4. V poli **Účet** vyberte dodavatele **DE-01002**.
5. Zadejte hodnotu do pole **Má dáti**.
6. V poli **Způsob platby** vyberte **SEPA CT**.
7. Zvolte **Uložit**.

![Platba dodavatele přidaná na stránce Platby dodavatele](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>Příloha 3: Zpracování platby dodavatele

1. Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.
2. Na stránce **Deník platby dodavatele** vyberte dříve vytvořený deník platby a pak vyberte **Řádky**.
3. Vyberte řádek platby a poté vyberte **Stav platby** \> **Žádný**.
4. Vyberte **Generovat platby**.
5. V poli **Způsob platby** vyberte **SEPA CT**.
6. V poli **Bankovní účet** vyberte **DEMF OPER**.
7. V dialogovém okně **Generovat platby** vyberte **OK**.
8. V dialogovém okně **Parametry elektronické sestavy** vyberte **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Návrh výrazů elektronického výkaznictví pro volání metod třídy aplikace
description: Tento článek popisuje, jak opakovaně použít existující aplikační logiku v konfiguracích elektronického výkaznictví (ER) voláním požadovaných metod aplikačních tříd.
author: kfend
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21c24cee15e9a0fd11838b5b8fd816e4aaed9a93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267835"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Návrh výrazů elektronického výkaznictví pro volání metod třídy aplikace

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak opakovaně použít existující aplikační logiku v konfiguracích [elektronického výkaznictví (ER)](../general-electronic-reporting.md) voláním požadovaných metod aplikačních tříd ve výrazech ER. Hodnoty argumentů pro volání tříd lze dynamicky definovat za běhu. Hodnoty mohou být například založeny na informacích v dokumentu analýzy, aby byla zajištěna jeho správnost.

Jako příklad v tomto článku navrhnete proces, který analyzuje příchozí bankovní výpisy pro aktualizaci dat aplikace. Příchozí bankovní výpisy obdržíte jako textové soubory (.txt), které obsahují kódy mezinárodních čísel bankovních účtů (IBAN). V rámci procesu importu bankovních výpisů je nutné ověřit správnost těchto kódů IBAN na základě logiky, která je již k dispozici.

## <a name="prerequisites"></a>Předpoklady

Postup v tomto článku je navržen pro uživatele s přiřazenou rolí **správce systému** nebo **vývojáře elektronického vykazování**.

Tyto postupy lze dokončit za použití libovolné datové sady.

Pro jejich dokončení je nutné stáhnout a uložit následující soubor: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

V tomto článku vytvoříte požadované konfigurace ER pro vzorovou společnost Litware, Inc. Před provedením procedury v tomto článku je proto třeba provést následující kroky.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** ověřte, že je dostupný poskytovatel konfigurace ukázkové společnosti **Litware, Inc.** a že je označen jako Aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivní](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-a-new-er-model-configuration"></a>Import nové konfigurace ER modelu

1. Na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurace** vyberte dlaždici poskytovatele konfigurace **Microsoft**.
2. Vyberte **Úložiště**.
3. Na stránce **Lokalizační úložiště** vyberte **Zobrazit filtry**.
4. Chcete-li vybrat záznam globálního úložiště, přidejte pole filtru **Název**.
5. Do pole **Název** zadejte **Globální**. Poté vyberte operátor filtru **contains**.
6. Zvolte **Použít**.
7. Vyberte **[Otevřít](../er-download-configurations-global-repo.md#open-configurations-repository)** a zkontrolujte seznam konfigurací ER ve vybraném úložišti.
8. Na stránce **Úložiště konfigurace** ve stromu konfigurací vyberte **Model platby**.
9. Na záložce s náhledem **Verze**, pokud je k dispozici tlačítko **Import**, vyberte jej a poté zvolte **Ano**.

    Pokud není tlačítko **Import** kdispozici, již jste importovali vybranou verzi konfigurace ER **Platební model**.

10. Zavřete stránku **Úložiště konfigurace** a poté zavřete stránku **Lokalizační úložiště**.

## <a name="add-a-new-er-format-configuration"></a>Přidání nové konfigurace formátu ER

Přidejte nový formát ER pro účely analýzy příchozích bankovních výpisů ve formátu TXT.

1. Na stránce **Konfigurace lokalizace** vyberte dlaždici **Konfigurace výkaznictví**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně vyberte **Model platby**.
3. Vyberte **Vytvořit konfiguraci**. 
4. V rozevíracím dialogovém okně proveďte následující kroky:

    1. V poli **Nový** zadejte **Formát založený na datovém modelu PaymentModel**.
    2. Do pole **Název** zadejte **Formát importu bankovního výpisu (ukázka)**.
    3. Vyberte **Ano** v poli **Podporuje import dat**.
    4. Dokončete vytváření konfigurace zvolením **Vytvořit konfiguraci**.

## <a name="design-the-er-format-configuration--format"></a>Návrh konfigurace formátu ER - formát

Navrhněte formát ER, který představuje očekávanou strukturu externího souboru ve formátu TXT.

1. Pro konfiguraci formátu **Formát importu bankovního výpisu (ukázka)**, kterou jste přidali, vyberte **Návrhář**.
2. Na stránce **Návrhář formátu** ve stromu struktury formátu v levém podokně vyberte **Přidat kořen**.
3. V rozevíracím dialogovém okně proveďte následující kroky:

    1. Ve stromu vyberte **Text\\Pořadí**, chcete-li přidat komponentu formátu **Sekvence**.
    2. Do pole **Název** zadejte řetězec **Kořen**.
    3. V poli **speciální znaky** vyberte **Nový řádek – Windows (CR LF)**. Na základě tohoto nastavení bude každý řádek souboru analýzy považován za samostatný záznam.
    4. Vyberte **OK**.

4. Vyberte **přidat**.
5. V rozevíracím dialogovém okně proveďte následující kroky:

    1. Ve stromovém zobrazení vyberte **Text\\Pořadí**.
    2. Do pole **Název** zadejte **Řádek**.
    3. V poli **Násobnost** vyberte **Jeden-n**. Na základě tohoto nastavení se očekává, že v souboru analýzy bude přítomen alespoň jeden řádek.
    4. Vyberte **OK**.

6. Ve stromu vyberte **Kořen\\Řádky** a poté vyberte **Přidat pořadí**.
7. V rozevíracím dialogovém okně proveďte následující kroky:

    1. Do pole **Název** zadejte **Pole**.
    2. V poli **Násobnost** vyberte **Přesně jeden**.
    3. Vyberte **OK**.

8. Ve stromu vyberte **Kořen\\Řádky\\Pole** a poté vyberte **Přidat**.
9. V rozevíracím dialogovém okně proveďte následující kroky:

    1. Ve stromovém zobrazení vyberte **Text\\String**.
    2. Do pole **Název** zadejte **IBAN**.
    3.. Vyberte **OK**.

10. Zvolte možnost **Uložit**.

Konfigurace je nyní konfigurována tak, že každý řádek v souboru analýzy obsahuje pouze kód IBAN.

![Konfigurace formátu Formát importu bankovního výpisu (ukázka) na stránce návrhaře Formát.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>Návrh konfigurace formátu ER – mapování na datový model

Navrhněte mapování formátu ER, které využívá informace ze souboru analýzy k vyplnění datového modelu.

1. Na stránce **Návrhář formátu** v podokně Akce vyberte možnost **Mapovat formát na model**.
2. Na stránce **Mapování modelu na zdroj dat** v podokně Akce vyberte možnost **Nový**.
3. V poli **Definice** vyberte **BankToCustomerDebitCreditNotificationInitiation**.
4. V poli **Název** zadejte **Mapovat na datový model**.
5. Zvolte možnost **Uložit**.
6. Vyberte možnost **Návrhář**.
7. Na stránce **Návrhář mapování modelu** ve stromu **Typy datových zdrojů** zvolte položku **Dynamics 365 for Operations\\Třída**.
8. V sekci **Zdroje dat** vyberte **Přidat kořen**, chcete-li přidat zdroj dat, který volá existující aplikační logiku pro ověření kódů IBAN.
9. V rozevíracím dialogovém okně proveďte následující kroky:

    1. Do pole **Název** zadejte **Kontrolovat\_kódy**.
    2. V poli **Třída** zadejte nebo vyberte **ISO7064**.
    3. Vyberte **OK**.

10. Ve stromě **Typy zdrojů dat** postupujte takto:

    1. Rozbalte zdroj dat **formát**.
    2. Rozbalte **format\\Root: Sequence(Root)**.
    3. Rozbalte **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)**.
    4. Rozbalte **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)\\Fields: Sequence 1..1 (Fields)**.

11. Ve stromě **Datový model** postupujte takto:

    1. Rozbalte pole **Platby** datového modelu.
    2. Rozbalte **Payments\\Creditor Account(CreditorAccount)**.
    3. Robalte **Payments\\Creditor Account(CreditorAccount)\\Identification**.
    4. Rozbralte **Payments\\Creditor Account(CreditorAccount)\\Identification\\IBAN**.

12. Chcete-li svázat komponenty nakonfigurovaného formátu s poli datového modelu, postupujte takto:

    1. Vyberte **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)**.
    2. Vyberte **Platby**.
    3. Vyberte možnost **vazba**. Na základě tohoto nastavení bude každý řádek souboru analýzy považován za jednu platbu.
    4. Vyberte **format\\Root: Sequence(Root)\\Rows: Sequence 1..\* (Rows)\\Fields: Sequence 1..1 (Fields)\\IBAN: String(IBAN)**.
    5. Vyberte **Payments\\Creditor Account(CreditorAccount)\\Identification\\IBAN**.
    6. Vyberte možnost **vazba**. Na základě tohoto nastavení pole **IBAN** datového modelu bude vyplněno hodnotou ze souboru analýzy.

    ![Vazba komponent formátu na pole datového modelu na stránce Návrhář mapování modelu.](../media/design-expressions-app-class-er-02.png)

13. Na kartě **Validace** podle následujících kroků přidejte pravidlo [validace](../general-electronic-reporting-formula-designer.md#Validation), které zobrazuje chybovou zprávu pro libovolný řádek v souboru analýzy, který obsahuje neplatný kód IBAN:

    1. Vyberte **Nový** a poté vyberte **Upravit podmínku**.
    2. Na stránce **Návrhář vzorce** ve stromu **Zdroj dat** rozbalte **Check\_codes**, který představuje aplikační třídu **ISO7064** pro zobrazení dostupných metod této třídy.
    3. Vyberte **Check\_codes\\verifyMOD1271\_36**.
    4. Vyberte **Přidat zdroj dat**.
    5. V poli **Vzorec** zadejte následující [výraz](../general-electronic-reporting-formula-designer.md#Binding): **Check\_codes.verifyMOD1271\_36(format.Root.Rows.Fields.IBAN)**.
    6. Zvolte **Uložit** a pak zavřete stránku.
    7. Vyberte možnost **Upravit zprávu**.
    8. Na stránce **Návrhář vzorců** do pole **Vzorec** zadejte **CONCATENATE("Byl nalezen neplatný kód IBAN:&nbsp;", format.Root.Rows.Fields.IBAN)**.
    9. Zvolte **Uložit** a pak zavřete stránku.

    Na základě těchto nastavení stav ověření vrátí hodnotu *[FALSE](../er-formula-supported-data-types-primitive.md#boolean)* u každého neplatného kódu IBAN voláním stávající metody **verifyMOD1271\_36** aplikační třídy **ISO7064**. Všimněte si, že hodnota kódu IBAN je definována dynamicky při spuštění jako argumentem metody volání založený na obsahu textového souboru analýzy.

    ![Pravidlo ověření na stránce návrháře mapování modelů.](../media/design-expressions-app-class-er-03.png)

14. Zvolte možnost **Uložit**.
15. Zavřete stránku **Návrhář mapování modelů** a poté zavřete stránku **Mapování modelu na zdroj dat**.

## <a name="run-the-format-mapping"></a>Spuštění mapování formátu

Pro účely testování spusťte mapování formátu pomocí souboru SampleIncomingMessage.txt, který jste stáhli dříve. Generovaný výstup zahrnuje data, která budou importována z vybraného textového souboru a načtena do vlastního datového modelu při reálném importu.

1. Na stránce **Mapování modelu k datovým zdrojům** vyberte **Spustit**.
2. Na stránce **Parametry elektronického výkaznictví** vyberte **Procházet**, přejděte na soubor **SampleIncomingMessage.txt**, který jste stáhli, a vyberte jej.
3. Vyberte **OK**.
4. Všimněte si, že stránka **Mapování modelu na zdroj dat** zobrazuje chybovou zprávu o neplatném kódu IBAN.

    ![Výsledek spuštění mapování modelu na stránce Mapování modelu na zdroj dat.](../media/design-expressions-app-class-er-04.png)

5. Zkontrolujte výstup ve formátu XML, který představuje data importovaná z vybraného souboru a přenesená do datového modelu. Všimněte si, že pouze tři řádky importovaného textového soboru byly zpracovány bez chyb. IBAN kód na řádku 4 není platný a byl přeskočen.

    ![výstup XML.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

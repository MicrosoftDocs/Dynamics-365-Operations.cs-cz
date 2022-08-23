---
title: Úprava formátu elektronického výkaznictví a vytvoření vlastního elektronického dokladu
description: Tento článek vysvětluje, jak upravit formát elektronického výkaznictví (ER) od společnosti Microsoft tak, aby generoval vlastní elektronické doklady.
author: kfend
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314,  ""intro-internal
ms.assetid: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
ms.openlocfilehash: 8b0bcdbd011c4c04e2693a3dcb8033c3cbe2adc7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283551"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>Úprava formátu elektronického výkaznictví a vytvoření vlastního elektronického dokladu

[!include[banner](../includes/banner.md)]

Postupy v tomto článku vysvětlují, jak může uživatel v roli administrátora systému nebo v role funkčního konzultanta elektronického výkaznictví provádět tyto úkoly:

- Konfigurace parametrů pro [rámec elektronického výkaznictví (ER)](general-electronic-reporting.md).
- Import konfigurace ER od společnosti Microsoft, jež se používají ke generování souboru platby, když je zpracovávána [platba dodavateli](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md).
- Vytvoření vlastní verze konfigurace standardního formátu ER od společnosti Microsoft.
- Úprava vlastní konfiguraci formátu ER tak, aby byly generovány soubory plateb, jež splňují požadavky konkrétní banky.
- Převzetí změn provedených ve standardní konfiguraci formátu ER do vlastní konfiguraci formátu ER.

Všechny následující procedury lze provést ve společnosti **GBSI**. Není nutné žádné kódování.

- [Konfigurace architektury ER](#ConfigureFramework)

    - [Konfigurace parametrů ER](#ConfigureParameters)
    - [Aktivace poskytovatele konfigurace ER](#ActivateProvider)

        - [Kontrola seznamu poskytovatelů konfigurace ER](#ReviewProvidersList)
        - [Přidání nového poskytovatele konfigurace ER](#ActivateProvider)
        - [Aktivace poskytovatele konfigurace ER](#ActivateAddedProvider)

- [Import standardních konfigurací formátu ER](#ImportERSolution1)

    - [Import standardních konfigurací ER](#ImportERFormat1)
    - [Kontrola importovaných konfigurací ER](#ReviewImportedERSolution)

- [Příprava platby dodavateli ke zpracování](#PrepareVendorPayment)

    - [Přidejte údajů o bance k účtu dodavatele](#AddBankAccount)
    - [Zadání platby dodavateli](#EnterVendorPayment)

- [Zpracování platby dodavateli pomocí standardního formátu ER](#ProcessVendorPayment1)

    - [Nastavení způsobu elektronické platby](#ConfigureMethodOfPayment1)
    - [Zpracování platby dodavateli](#ProcessPayment1)

- [Přizpůsobení standardního formátu ER](#CustomizeProvidedFormat)

    - [Vytvoření vlastního formátu](#DeriveProvidedFormat)
    - [Úprava vlastního formátu](#ConfigureDerivedFormat)
    - [Označení vlastního formátu jako spustitelného](#MarkFormatRunnable)

- [Zpracování platby dodavateli pomocí vlastního formátu ER](#ProcessVendorPayment2)

    - [Nastavení způsobu elektronické platby](#ConfigureMethodOfPayment2)
    - [Zpracování platby dodavateli](#ProcessPayment2)

- [Import nových verzí standardních konfigurací formátu ER](#ImportERSolution2)

    - [Import nových verzí standardních konfigurací ER](#ImportERFormat2)
    - [Kontrola importovaných konfigurací formátu ER](#ReviewImportedERFormat)

- [Převzetí změn z nové verze importovaného formátu do vlastního formátu](#AdoptNewBaseVersion)

    - [Dokončení aktuální verze konceptu vlastního formátu](#CompleteDerivedFormat)
    - [Převedení vlastního formátu na novou základní verzi](#RebaseDerivedFormat)
    - [Zpracování platby dodavateli pomocí nově podloženého formátu ER](#ProcessPayment3)

- [Další prostředky](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>Konfigurace rámce ER

Jako uživatel v roli funkčního konzultanta elektronického výkaznictví musíte nakonfigurovat minimální sadu parametrů ER, abyste mohli začít používat rámec ER k navrhování vlastních verzí standardního formátu ER.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfigurace parametrů ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** vyberte v části **Související odkazy** možnost **Parametry elektronického výkaznictví**.
3. Na stránce **Parametry elektronického výkaznictví** nastavte na kartě **Obecné** u možnosti **Povolit režim návrhu** hodnotu **Ano**.
4. Na kartě **Přílohy** natavte následující parametry:

    - V poli **Konfigurace** vyberte pro společnost **USMF** typ **Soubor**.
    - V polích **Archiv úloh**, **Dočasné**, **Základ** a **Ostatní** vyberte typ **souboru**.

Další informace o parametrech elektronického výkaznictví najdete v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivace poskytovatele konfigurace elektronického výkaznictví

U každé přidané konfigurace elektronického výkaznictví je vyznačen jako vlastník poskytovatel konfigurace elektronického výkaznictví. Pro tyto účely se používá poskytovatel konfigurace elektronického výkaznictví, který je aktivován v pracovním prostoru **Elektronické výkaznictví**. Než začnete přidávat nebo upravovat konfigurace ER, musíte proto aktivovat poskytovatele konfigurace ER v pracovním prostoru **Elektronické výkaznictví**.

> [!NOTE]
> Pouze vlastník konfigurace ER může konfiguraci upravovat. Konfiguraci ER proto můžete upravovat teprve poté, co je příslušná konfigurace ER aktivována v pracovním prostoru **Elektronické výkaznictví**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Kontrola seznamu poskytovatelů konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.
3. Na stránce **Tabulka poskytovatelů konfigurací** má záznam každého poskytovatele jedinečný název a adresu URL. Zkontrolujte obsah této stránky. Pokud již existuje záznam **Litware, Inc.** ( `https://www.litware.com`), další postup, [přidání nového poskytovatele konfigurace ER](#ActivateProvider), přeskočte.

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Přidání nového poskytovatele konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.
3. Na stránce **Poskytovatelé konfigurace** zvolte **Nový**.
4. Do pole **Název** zadejte **Litware, Inc.**
5. Do pole **Internetová adresa** zadejte `https://www.litware.com`.
6. Zvolte **Uložit**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivace poskytovatele konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** klikněte v části **Poskytovatelé konfigurací** na dlaždici **Litware, Inc.** a poté vyberte možnost **Nastavit jako aktivní**.

Další informace o poskytovatelích konfigurací ER naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Import standardních konfigurací formátu ER

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>Import standardních konfigurací ER

Chcete-li přidat standardní konfigurace ER do aktuální instance Microsoft Dynamics 365 Finance, musíte je importovat z [úložiště](general-electronic-reporting.md#Repository) ER, jež je pro tuto instanci nakonfigurováno.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Chcete-li zobrazit seznam úložišť pro poskytovatele Microsoft, klikněte na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurací** na dlaždici **Microsoft** a poté vyberte možnost **Úložiště**.
3. Na stránce **Úložiště konfigurací** vyberte úložiště typu **Globální** a poté zvolte **Otevřít**. Pokud budete vyzváni k autorizaci pro připojení ke službě Regulatory Configuration Service, postupujte podle pokynů k autorizaci.
4. Na stránce **Úložiště konfigurace** vyberte ve stromu konfigurací v levém podokně konfiguraci formátu **BACS (Velká Británie)**.
5. Na záložce s náhledem **Verze** vyberte jako požadovanou verzi formátu vybrané konfigurace ER **1.1**.
6. Vyberte **Importovat**. Vybraná verze se stáhne z globálního úložiště do aktuální instance aplikace Finance.

![Stránka úložiště konfigurace.](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> Pokud máte potíže s přístupem na [globální úložiště](er-download-configurations-global-repo.md), můžete si místo toho [stáhnout konfigurace](download-electronic-reporting-configuration-lcs.md) ze služby Microsoft Dynamics Lifecycle Services (LCS).

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Kontrola importovaných konfigurací ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte **Model platby**.
4. Všimněte si, že kromě vybraného formátu ER **BACS (Velká Británie)** byly importovány další požadované konfigurace ER. Ujistěte se, že ve stromu konfigurací jsou k dispozici následující konfigurace ER:

    - **Model platby** – Tato konfigurace obsahuje komponentu datového modelu ER, jež představuje datovou strukturu platební podnikové domény.
    - **Mapování modelu platby 1611** – Tato konfigurace obsahuje komponentu ER mapování modelu, jež popisuje, jak se datový model vyplní za chodu daty z aplikace.
    - **BACS (Velká Británie)** – Tato konfigurace obsahuje komponenty ER formátu a mapování formátu. Komponenta formát určuje rozvržení sestavy. Komponenta mapování formátu obsahuje zdroj dat modelu a určuje, jak se vyplněno rozvržení sestavy pomocí tohoto zdroje dat za chodu vyplňuje.

![Ve stromové struktuře je k dispozici stránka s konfiguracemi se specifikovanými konfiguracemi ER.](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>Příprava platby dodavateli ke zpracování

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Přidejte údajů o bance k účtu dodavatele

Musíte zadat bankovní údaje pro účet dodavatele, na který bude později odkazovat registrovaná platba.

1. Přejděte do části **Pohledávky** \> **Dodavatelé** \> **Všichni dodavatelé**.
2. Na **Všichni dodavatelé** vyberte účet dodavatele **GB_SI_000001** a poté v podokně Akce na kartě **Dodavatel** vyberte ve skupině **Nastavení** položku **Bankovní účty**.
3. Na stránce **Bankovní účty dodavatele** vyberte **Nový** a zadejte následující údaje:

    1. Do pole **Bankovní účet** zadejte **GBP OPER**.
    2. V poli **Bankovní skupiny** vyberte možnost **BankGBP**.
    3. Do pole **Číslo bankovního účtu** zadejte **202015**.
    4. Do pole **Kód SWIFT** zadejte hodnotu <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.
    5. Do pole **IBAN** zadejte hodnotu **GB33BUKB20201555555555**.
    6. V poli **Směrový kód banky** ponechte výchozí hodnotu <a id="DefineRoutingNumber"></a>**123456**.

    ![Stránka Bankovní účty dodavatele.](./media/er-quick-start2-bank-account.png)

4. Zvolte možnost **Uložit**.
5. Zavřete stránku.
6. Na stránce **Všichni dodavatelé** otevřete účet dodavatele **GB_SI_000001**.
7. Na stránce podrobností dodavatele vyberte možnost **Upravit**. Díky tomu bude stránka v případě potřeby editovatelná.
8. Na záložce s náhledem **Platba** vyberte v poli **Bankovní účet** možnost **GBP OPER**.

    ![Stránka Podrobnosti dodavatele.](./media/er-quick-start2-bank-account-reference.png)

9. Zvolte možnost **Uložit**.
10. Zavřete stránku.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Zadání platby dodavateli

Novou platbu dodavateli musíte vytvořit pomocí [návrhu platby](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).

1. Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.
2. Na stránce **Platební deník dodavatelů** zvolte **Nová**.
3. Zvolte hodnotu **VendPay** v poli **Název**.
4. Vybrat **řádky**.
5. Vyberte **Návrh platby** \> **Vytvořit návrh platby**.
6. V dialogovém okně **Návrh platby dodavateli** nakonfigurujte filtrování tak, aby se zobrazovaly pouze záznamy pro účet dodavatele **GB_SI_000001**, poté klikněte na **OK**.
7. Vyberte řádek pro fakturu **00000007_Inv** a klikněte na **Vytvořit platbu**.

    ![Dialogové okno Návrh platby dodavateli.](./media/er-quick-start2-payment-proposal.png)

8. Ověřte, že zadávaná platba je nakonfigurována k použití **Elektronického** způsobu platby.

    ![Stránka Platby dodavatelů.](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Zpracování platby dodavateli pomocí standardního formátu ER

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>Nastavení způsobu elektronické platby

Musíte nakonfigurovat elektronický způsob platby tak, aby využíval importovanou konfiguraci formátu ER.

1. Přejděte na **Pohledávky** \> **Nastavení platby** \> **Způsoby platby**.
2. Na stránce **Způsoby platby – dodavatelé** vyberte v levém podokně **Elektronický** způsob platby.
3. Vyberte možnost **Upravit**.
4. Na záložce s náhledem **Formáty souborů** nastavte u možnosti **Obecný formát elektronického exportu** hodnotu **Ano**.
5. V poli **Exportovat konfiguraci formátu** vyberte konfiguraci formátu **BACS (Velká Británie)**.

    ![Způsoby platby – stránka prodejců pro nastavení elektronické platební metody pro zpracování plateb dodavatele ve standardním formátu.](./media/er-quick-start2-method-of-payment1.png)

6. Zvolte možnost **Uložit**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Zpracování platby dodavateli

1. Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.
2. Na stránce **Deník platby dodavateli** vyberte dříve přidaný deník platby a pak vyberte **Řádky**.
3. Na stránce **Platby dodavateli** vyberte možnost **Generovat platby**.
4. V dialogovém okně **Generovat platby** zadejte následující údaje:

    - V poli **Způsob platby** vyberte **Elektronický**.
    - V poli **Bankovní účet** vyberte **GBSI OPER**.

5. Vyberte **OK**.
6. V dialogovém okně **Parametry elektronického výkaznictví** nastavte u možnosti **Vytisknout kontrolní sestavu** hodnotu **Ano** a poté stiskněte **OK**.

    ![Stránka Parametry elektronického výkaznictví.](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > Kromě platebního souboru můžete nyní vygenerovat kontrolní sestavu.

7. Stáhněte soubor zip a z něj extrahujte následující soubory:

    - Kontrolní sestava ve formátu Excel
    - Platební soubor ve formátu TXT

        Všimněte si, že v souladu se [strukturou](#PositionRoutingNumber) poskytovaného formátu ER začíná řádek platby ve vygenerovaném souboru směrovým kódem, který byl [definován](#DefineRoutingNumber) pro konfigurovaný bankovní účet.

        ![Platební soubor ve formátu TXT.](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Přizpůsobení standardního formátu ER

V příkladu, který je uveden v této části, chcete použít konfigurace ER poskytnuté společností Microsoft pro účely generování platebních souborů pro platby dodavatelům ve formátu BACS, musíte však přidat přizpůsobení, aby byly podporovány požadavky konkrétní banky. Chcete také mít možnost vlastní formát upgradovat, když budou k dispozici nové verze konfigurací ER. Upgrade však chcete provést s nejnižšími náklady.

V tomto případě musíte jako zástupce společnosti Litware, Inc. vytvořit (odvodit) novou konfiguraci formátu ER s tím, že jako základ použijete konfiguraci **BACS (Velká Británie)** od společnosti Microsoft.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Vytvoření vlastního formátu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a poté vyberte možnost **BACS (Velká Británie)**. Společnost Litware, Inc. použije verzi 1.1 této konfigurace formátu ER jako základ pro vlastní verzi.
3. Výběrem možnosti **Vytvořit konfiguraci** otevřete rozbalovací dialogovou nabídku. Tuto dialogovou nabídku můžete použít k vytvoření nové konfigurace pro vlastní formát platby.
4. Ve skupině polí **Nový** vyberte možnost **Odvodit z názvu: BACS (Velká Británie), Microsoft**.
5. Do pole **Název** zadejte **BACS (Velká Británie – vlastní)**.

    ![Dialogové okno Vytvořit konfiguraci – rozevírací seznam.](./media/er-quick-start2-add-derived-format.png)

6. Vyberte **Vytvořit konfiguraci**.

Vytvoří se verze 1.1.1 **BACS (Velká Británie – vlastní)** konfigurace formátu ER. Tato verze je ve stavu **Koncept** a je editovatelná. Aktuální obsah vašeho vlastního formátu ER odpovídá obsahu formátu poskytnutého společností Microsoft.

![Stránka konfigurace s verzi 1.1.1 BACS (Spojené království – vlastní) konfigurace formátu ER.](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Úprava vlastního formátu

Vlastní formát musíte nakonfigurovat, aby splňoval konkrétní požadavky banky. Banka může například vyžadovat, aby generované platební soubory obsahovaly kód SWIFT (Society for Worldwide Interbank Financial Telecommunication) banky, jíž je přiřazena role zprostředkovatele při zpracování platby dodavateli. Kódy SWIFT jsou mezinárodní bankovní kódy a identifikují konkrétní banky na celém světě. Někdy se též označují jako kódy BIC (Bank Identifier Code). Kód SWIFT sestává z 11 znaků a musí být zadán na začátku každého platebního řádku ve vygenerovaném souboru platby.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a poté vyberte možnost **BACS (Velká Británie – vlastní)**.
3. Na záložce s náhledem **Verze** vyberte jako požadovanou verzi vybrané konfigurace **1.1.1**.
4. Vyberte možnost **Návrhář**.
5. Na stránce **Návrhář formátu** vyberte možnost **Zobrazit podrobnosti**. Zobrazí se další informace o prvcích formátu.
6. Rozbalte a zkontrolujte následující prvky:

    - Prvek **BACSReportsFolder** typu **Složka**. Tento prvek se používá ke generování výstupu ve formátu ZIP.
    - Prvek **soubor** typu **Soubor**. Tento prvek se používá ke generování souboru plateb ve formátu TXT.
    - Prvek **transakce** typu **Sekvence**. Tento prvek se používá ke generování jednoho řádku platby v souboru plateb.
    - Prvek **transakce** typu **Sekvence**. Tento prvek se používá ke generování jednotlivých polí jednoho řádku platby.

7. Vyberte prvek **transakce**.

    ![Prvek transakce v návrháři operací ER.](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Poskytnutá sestava je nakonfigurována tak, aby <a id="PositionRoutingNumber"></a>každý řádek platby začínal směrovým kódem banky. Pro tento účel se používá formátovací prvek **vendBankRouteNum**. 

8. Vyberte **Přidat** a poté vyberte typ formátu prvku, který přidáváte, jako **Text\\String**:

    1. Do pole **Název** zadejte **vendBankSWIFT**.
    2. Do pole **Minimální délka** zadejte hodnotu **11**.
    3. Do pole **Maximální délka** zadejte hodnotu **11**.
    4. Vyberte **OK**.

    > [!NOTE]
    > Prvek **vendBankSWIFT** se použije k zadání kódu SWIFT banky dodavatele do vygenerovaných souborů.

9. Ve stromu struktury formátu vyberte **vendBankSWIFT**.
10. Chcete-li vybraný prvek formátu posunout o jednu úroveň výše, klikněte na **Přesunout nahoru**. Tento krok opakujte, kolikrát je třeba, aby prvek **vendBankSWIFT** byl <a id="PositionSWIFTCode"></a>prvním prvkem pod nadřazeným prvkem **transakce**.

    ![VendBankSWIFT jako první prvek pod prvkem transakce v návrháři operací ER.](./media/er-quick-start2-derived-format1.png)

11. Dokud máte ve stromové struktuře formátu vybraný prvek **vendBankSWIFT**, klikněte na kartu **Mapování** a poté rozbalte zdroj dat **Model**.
12. Rozbalte **model.Payment** \> **model.Payment.CreditorAgent** a vyberte pole zdroje dat **model.Payment.CreditorAgent.BICFI**. Toto pole zdroje dat obsahuje kód SWIFT banky dodavatele, jíž je při zpracování platby dodavateli přiřazena role zprostředkovatele.
13. Vyberte možnost **vazba**. Prvek formátu **vendBankSWIFT** je nyní propojen s polem zdroje dat **model.Payment.CreditorAgent.BICFI**, a proto budou kódy SWIFT vkládány do vygenerovaných platebních souborů.

    ![Prvek formátu vendBankSWIFT svázaný s polem zdroje dat model.Payment.CreditorAgent.BICFI v návrháři operací ER.](./media/er-quick-start2-derived-format2.png)

14. Zvolte možnost **Uložit**.
15. Zavřete stránku návrháře.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Označení vlastního formátu jako spustitelného

Nyní, když máte vytvořenou první verzi vlastního formátu a ten je ve stavu **Koncept**, můžete jej pro testovací účely spustit. Chcete-li sestavu spustit, musíte zpracovat platbu dodavateli pomocí způsobu platby, která odkazuje na váš vlastní formát ER. Ve výchozím nastavení jsou při volání formátu ER z aplikace zvažovány pouze verze se stavem **Dokončeno** nebo **Sdíleno**. Toto chování pomáhá zabránit použití formátů ER s nedokončenými návrhy. Pro zkušební účely však můžete aplikaci přinutit, aby použila verzi formátu ER ve stavu **Koncept**. Pokud při testu zjistíte, že je třeba provést nějaké změny, můžete následně aktuální verzi formátu upravit. Další informace naleznete v tématu [Použitelnost](electronic-reporting-destinations.md#applicability).

Chcete-li použít koncept formátu ER, musíte příslušný formát ER explicitně označit.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. V dialogovém okně **Uživatelské parametry** nastavte u možnosti **Spustit nastavení** hodnotu **Ano** a poté stiskněte **OK**.
4. Je-li třeba vyberte možnost **Upravit**, má-li být aktuální stránka editovatelná.
5. Ve stromu konfigurace v levém podokně vyberte možnost **BACS (Velká Británie – vlastní)**.
6. U možnosti **Spustit koncept** nastavte hodnotu **Ano**.

    ![Možnost Spustit koncept na stránce Konfigurace.](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Zpracování platby dodavateli pomocí vlastního formátu ER

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>Nastavení způsobu elektronické platby

Elektronický způsob platby musíte nakonfigurovat tak, aby byl při zpracování plateb dodavateli použit váš vlastní formát ER.

1. Přejděte na **Pohledávky** \> **Nastavení platby** \> **Způsoby platby**.
2. Na stránce **Způsoby platby – dodavatelé** vyberte v levém podokně **Elektronický** způsob platby.
3. Vyberte možnost **Upravit**.
4. Na záložce s náhledem **Formát souboru** nastavte u možnosti **Obecný formát elektronického exportu** hodnotu **Ano**.
5. V poli **Exportovat konfiguraci formátu** vyberte konfiguraci formátu **BACS (Velká Británie – vlastní)**.

    ![Způsoby platby – stránka prodejců pro nastavení elektronické platební metody pro zpracování plateb dodavatele ve vlastním formátu.](./media/er-quick-start2-method-of-payment2.png)

6. Zvolte možnost **Uložit**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Zpracování platby dodavateli

1. Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.
2. Na stránce **Deník platby dodavateli** vyberte dříve vytvořený deník platby.
3. Vybrat **řádky**.
4. Na stránce **Platby dodavateli** vyberte nad mřížkou **Stav platby** \> **Žádný**.
5. Vyberte **Generovat platbu**.
6. V dialogovém okně **Generovat platby** zadejte následující údaje:

    - V poli **Způsob platby** vyberte **Elektronický**.
    - V poli **Bankovní účet** vyberte **GBSI OPER**.

7. Vyberte **OK**.
8. V dialogovém okně **Parametry elektronického výkaznictví** nastavte u možnosti **Vytisknout kontrolní sestavu** hodnotu **Ano** a poté stiskněte **OK**.

    > [!NOTE]
    > Kromě platebního souboru můžete vygenerovat pouze kontrolní sestavu.

9. Stáhněte soubor zip a z něj extrahujte následující soubory:

    - Kontrolní sestava ve formátu Excel
    - Platební soubor ve formátu TXT

        Všimněte si, že v souladu se strukturou vlastního formátu ER platební řádek ve vygenerovaném souboru nyní [začíná](#PositionSWIFTCode) kódem SWIFT, který byl [zadán](#DefineSWIFTCode) pro bankovní účet dodavatele, jehož platba se zpracovává.

        ![Platební soubor ve formátu TXT používaný ke zpracování platby dodavatele.](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Import nových verzí standardních konfigurací formátu ER

V rámci příkladu uvedeného v této části se zobrazí upozornění na článek ze znalostní báze [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046). Toto oznámení vás informuje o nové verzi formátu ER **BACS (Velká Británie)**, který publikovala společnost Microsoft. Kromě kontrolní sestavy umožňuje tato nová verze uživatelům generovat při zpracování plateb dodavatelům sestavu platebních avíz a sestavu průvodek. Chcete začít používat tuto funkci.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Import nových verzí standardních konfigurací ER

Chcete-li přidat nové verze konfigurace ER do aktuální instance systému Finance, musíte je importovat z nakonfigurovaného [úložiště](general-electronic-reporting.md#Repository) ER.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Chcete-li zobrazit seznam úložišť pro poskytovatele Microsoft, klikněte na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurací** na dlaždici **Microsoft** a poté vyberte možnost **Úložiště**.
3. Na stránce **Úložiště konfigurací** vyberte úložiště typu **Globální** a poté zvolte **Otevřít**. Pokud budete vyzváni k autorizaci pro připojení ke službě Regulatory Configuration Service, postupujte podle pokynů k autorizaci.
4. Na stránce **Úložiště konfigurace** vyberte ve stromu konfigurací v levém podokně konfiguraci formátu **BACS (Velká Británie)**.
5. Na záložce s náhledem **Verze** vyberte jako požadovanou verzi formátu vybrané konfigurace ER **3.3**.
6. Vyberte **Importovat**. Vybraná verze se stáhne z globálního úložiště do aktuální instance aplikace Finance.

![Stránka úložiště konfigurace, záložka Verze, tlačítko Importovat.](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> Pokud máte potíže s přístupem na [globální úložiště](er-download-configurations-global-repo.md), můžete si místo toho [stáhnout konfigurace](download-electronic-reporting-configuration-lcs.md) ze služby Lifecycle Services (LCS).

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>Kontrola importovaných konfigurací formátu ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a poté vyberte možnost **BACS (Velká Británie)**.
4. Na záložce s náhledem **Verze** vyberte verzi **3.3**.
5. Vyberte možnost **Návrhář**.
6. Na stránce **Návrhář formátů** rozbalte prvek formátu **BACSReportsFolder**.
7.  Všimněte si, že verze 3.3 obsahuje prvek formátu **PaymentAdviceReport**, který se používá ke generování sestavy platebních avíz, když je zpracována platba dodavateli.

    ![Prvek formátu PaymentAdviceReport v návrháři operací ER.](./media/er-quick-start2-imported-solution2.png)

8. Zavřete stránku návrháře.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>Převzetí změn z nové verze importovaného formátu do vlastního formátu

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>Dokončení aktuální verze konceptu vlastního formátu

Pokud si přejete zachovat aktuální stav vlastního formátu, dokončíte koncept ve verzi 1.1.1 tak, že změníte jeho stav z **Koncept** na **Dokončeno**.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby**, rozbalte položku **BACS (Velká Británie)** a poté vyberte možnost **BACS (Velká Británie – vlastní)**.
4. Na záložce s náhledem **Verze** vyberte možnost **Změnit stav** \> **Dokončeno** a poté klikněte na **OK**.

Stav verze 1.1.1 se změní z **Koncept** na **Dokončeno** a verze se změní tak, že bude pouze pro čtení. Byla přidána nová editovatelná verze 1.1.2, která je nyní ve stavu **Koncept**. Tuto verzi můžete použít k provedení dalších změn ve vlastním formátu ER.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Převedení vlastního formátu na novou základní verzi

Chcete-li začít používat novou funkčnost verze 3.3 formátu **BACS (Velká Británie)** v rámci přizpůsobování, musíte změnit základní verzi konfigurace na vlastní konfiguraci **BACS (Velká Británie – vlastní)**. Pro tento proces je používáno označení [přeskladnění](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase). Místo verze 1.1 **BACS (Velká Británie)** použijte novou verzi 3.3.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a poté vyberte možnost **BACS (Velká Británie – vlastní)**.
3. Na záložce s náhledem **Verze** vyberte verzi **1.1.2** a poté vyberte **Přeskládat**.
4. V dialogovém okně **Přeskládat** vyberte v poli **Cílová verze** verzi **3.3** základní konfigurace. Tím se tato použije jako nová základní konfigurace a též k aktualizaci konfigurace.

    ![Dialogové okno Přeskládat.](./media/er-quick-start2-rebase1.png)

5. Vyberte **OK**.
6. Všimněte si, že číslo konceptové verze se změnilo z **1.1.2** na **3.3.2**, což umožňuje reflektovat změnu základní verze.

    Když dojde ke spojení vlastní verze a nové základní verze, mohou se objevit konflikty vyplývající ze změn formátu, které nelze sloučit automaticky.

    ![Přestavěná konfigurace s konflikty na stránce Konfigurace.](./media/er-quick-start2-rebase2.png)

    Pokud jsou zjištěny konflikty, je nutné je vyřešit ručně v návrháři formátů.

7. Na záložce s náhledem **Verze** vyberte verzi **3.3.2**.
8. Vyberte možnost **Návrhář**.
9. Na stránce **Návrhář formátů** vyberte na záložce s náhledem **Podrobnosti** záznam konfliktu z přestavby a poté vyberte možnost **Použít základní hodnotu**.

    ![Záznam konfliktu z přestavby v návrháři operací ER.](./media/er-quick-start2-rebase3.png)

10. Zvolte možnost **Uložit**.

    Záznam konfliktu z přestavby by se již neměl na záložce s náhledem **Podrobnosti** objevovat.

    ![Vyřešený konflikt v návrháři operací ER.](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > Konflikt jste vyřešili potvrzením, že je třeba v tomto formátu ER použít verzi 3 základního modelu.

11. Rozbalte **BACSReportsFolder** \> **soubor** \> **transakce** \> **transakce**.
12. Na kartě **Mapování** si všimněte, že verze 3.3.2 vlastního formátu ER obsahuje vaše přizpůsobení (**vendBankSWIFT** a jeho vazby) a novou funkčnost verze 3.3 základního formátu ER od společnosti Microsoft (prvek formátu **PaymentAdviceReport** spolu s vnořenými prvky a nakonfigurovanými vazbami). Pouhými několika kliknutími myši jste přijali změny nové základní verze sloučením s vlastním přizpůsobením.

    ![Sloučený formát v návrháři operací ER.](./media/er-quick-start2-rebase5.png)

13. Zavřete stránku návrháře.

> [!NOTE]
> Akce přestavby je vratná. Chcete-li tuto přestavbu zrušit, vyberte verzi **1.1.1** formátu **BACS (Velká Británie – vlastní)** na záložce s náhledem **Verze** a poté vyberte možnost **Získat tuto verzi**. Verze 3.3.2 se poté přečísluje na 1.1.2 a obsah konceptové verze 1.1.2 bude odpovídat obsahu verze 1.1.1.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Zpracování platby dodavateli pomocí nově podloženého formátu ER

1. Přejděte na **Pohledávky** \> **Platby** \> **Deník plateb dodavatele**.
2. Na stránce **Deník platby dodavateli** vyberte dříve vytvořený deník platby.
3. Vybrat **řádky**.
4. Na stránce **Platby dodavateli** vyberte nad mřížkou **Stav platby** \> **Žádný**.
5. Vyberte **Generovat platbu**.
6. V dialogovém okně **Generovat platby** zadejte následující údaje:

    - V poli **Způsob platby** vyberte **Elektronický**.
    - V poli **Bankovní účet** vyberte **GBSI OPER**.

7. Vyberte **OK**.
8. V dialogovém okně **Parametry elektronického výkaznictví** zadejte následující údaje:

    - Nastavte možnost **Vytisknout kontrolní sestavu** na **Ano**.
    - Nastavte u položky **Tisknout platební avízo** hodnotu **Ano**.

    ![Dialogové okno parametrů elektronického výkaznictví.](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > Kromě platebního souboru můžete nyní vygenerovat kontrolní sestavu a sestavu platebních avíz.

9. Vyberte **OK**.
10. Stáhněte soubor zip a z něj extrahujte následující soubory:

    - Kontrolní sestava ve formátu Excel
    - Sestava platebních avíz ve formátu Excel

        ![Sestava platebních avíz ve formátu Excel.](./media/er-quick-start2-payment-advice-report.png)

    - Platební soubor ve formátu TXT

        Všimněte si, že platební řádek ve vygenerovaném souboru začíná kódem SWIFT, který byl zadán pro bankovní účet dodavatele, jehož platba se zpracovává.

        ![Platební soubor ve formátu TXT používaný ke zpracování platby dodavatele pomocí nově vytvořeného formátu ER.](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Stažení konfigurací ER z Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [Stažení konfigurací ER z Globálního úložiště konfigurační služby](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

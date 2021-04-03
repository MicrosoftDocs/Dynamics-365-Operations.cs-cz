---
title: Přizpůsobte konfigurace elektronického výkaznictví tak, aby generovaly elektronický dokument
description: Toto téma vysvětluje, jak přizpůsobit konfigurace elektronického výkaznictví (ER) od společnosti Microsoft, které generují vlastní elektronické doklady.
author: NickSelin
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a0cc308e2e3c7f42295a6170c4f709a835c5c84
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566119"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Přizpůsobte konfigurace elektronického výkaznictví tak, aby generovaly elektronický dokument

[!include[banner](../includes/banner.md)]

[Rámec elektronického výkaznictví (ER)](general-electronic-reporting.md) vám umožní nahrát ER [konfigurace](general-electronic-reporting.md#Configuration), které Microsoft poskytuje vaší instanci Microsoft Dynamics 365 Finance. Tímto způsobem mohou konfigurace poskytované společností Microsoft sloužit jako ER řešení, které se používá ke generování elektronických faktur zákazníka (e-faktury). Toto řešení ER můžete použít ke konfiguraci vlastního řešení ER pro přístup k vašim vlastním databázovým polím a generování elektronických faktur, které jsou v souladu s vašimi konkrétními požadavky, aniž byste museli upravovat zdrojový kód.

## <a name="overview"></a>Přehled

V příkladu v tomto tématu je třeba zadat federální daňový identifikační kód jako nový vlastní atribut každého zákazníka, který elektronicky fakturujete. Proto musíte přizpůsobit strukturu faktury, která se aktuálně používá, přidáním nové položky, která musí být vyplněna daňovým kódem v každé generované e-faktuře.

Postupy v tomto tématu vysvětlují, jak může uživatel v roli administrátora systému, vývojáře elektronických výkazů nebo funkčního konzultanta elektronického výkaznictví provádět následující úkoly ve vaší instanci Finance:

- [Nakonfigurujte minimální sadu parametrů ER, která je vyžadována k zahájení používání rámce ER](#ConfigureER).
- [Importujte počáteční verze standardních konfigurací ER, které jsou k dispozici pro generování elektronických faktur](#ImportERConfigurations1).
- [Nakonfigurujte parametry pohledávek, abyste mohli začít používat standardní konfigurace ER](#ConfigureAR1).
- [Nakonfigurujte parametry právnické osoby na fakturaci zákazníkům](#ConfigureLE).
- [Připravte záznam zákazníka pro elektronickou fakturaci](#ConfigureCustomer1).
- [Přidejte, zaúčtujte a odešlete fakturu zákazníka pomocí standardních konfigurací ER](#ProcessInvoice1).
- [Přidejte vlastní databázové pole pro správu federálního daňového identifikačního kódu pro zákazníky](#AddCustomField).
- [Aktualizujte metadata ER, abyste povolili změny databáze pro návrháře mapování modelu ER](#RefreshERMetadata).
- [Navrhněte vlastní konfigurace ER pro generování elektronických faktur, které obsahují nový daňový kód](#DesignCustomERConfigurations).
- [Nakonfigurujte parametry pohledávek, abyste mohli začít používat vlastní konfigurace ER](#ConfigureAR2).
- [Aktualizujte záznam zákazníka pro elektronickou fakturaci](#ConfigureCustomer2).
- [Přidejte, zaúčtujte a odešlete fakturu zákazníka pomocí vlastních konfigurací ER](#ProcessInvoice2).
- [Importujte nové verze standardních konfigurací ER, které jsou k dispozici pro generování elektronických faktur](#ImportERConfigurations2).
- [Přijměte změny nových verzí standardních konfigurací ER ve svých vlastních konfiguracích ER](#RebaseCustomERConfigurations).
- [Přidejte, zaúčtujte a odešlete fakturu zákazníka pomocí nových verzí vlastních konfigurací ER](#ProcessInvoice3).

Všechny tyto postupy lze provést v rámci společnosti **DEMF**.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>Konfigurace rámce ER

Jako uživatel v roli funkčního konzultanta elektronického výkaznictví nebo návrháře elektronického výkaznictví musíte nakonfigurovat minimální sadu parametrů ER. Poté můžete začít používat rámec ER k navrhování vlastních verzí standardních konfigurací řešení ER, které se používají ke generování elektronických faktur.

### <a name="configure-er-parameters"></a>Konfigurace parametrů ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** vyberte v části **Související odkazy** možnost **Parametry elektronického výkaznictví**.
3. Na stránce **Parametry elektronického výkaznictví** nastavte na kartě **Obecné** u možnosti **Povolit režim návrhu** hodnotu **Ano**.
4. Na kartě **Přílohy** v poli **Konfigurace** vyberte **Soubor**.
5. V polích **Archiv úloh**, **Dočasné**, **Základ** a **Ostatní** vyberte typ **souboru**.

Další informace o parametrech elektronického výkaznictví najdete v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>Aktivace poskytovatele konfigurace elektronického výkaznictví

U každé přidané konfigurace elektronického výkaznictví je vyznačen jako vlastník poskytovatel konfigurace elektronického výkaznictví. Pro tyto účely se používá poskytovatel konfigurace elektronického výkaznictví, který je aktivován v pracovním prostoru **Elektronické výkaznictví**. Než začnete přidávat nebo upravovat konfigurace ER, musíte proto aktivovat poskytovatele konfigurace ER v pracovním prostoru **Elektronické výkaznictví**.

> [!NOTE]
> Pouze vlastník konfigurace ER může konfiguraci upravovat. Konfiguraci ER proto můžete upravovat teprve poté, co je příslušná konfigurace ER aktivována v pracovním prostoru **Elektronické výkaznictví**.

#### <a name="review-the-list-of-er-configuration-providers"></a>Kontrola seznamu poskytovatelů konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.
3. Na stránce **Tabulka poskytovatelů konfigurací** má záznam každého poskytovatele jedinečný název a adresu URL. Zkontrolujte obsah této stránky. Pokud již existuje záznam **Litware, Inc.** ( `https://www.litware.com`), další postup, [přidání nového poskytovatele konfigurace ER](#AddProvider), přeskočte.

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Přidání nového poskytovatele konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.
3. Na stránce **Poskytovatelé konfigurace** zvolte **Nový**.
4. Do pole **Název** zadejte **Litware, Inc.**
5. Do pole **Internetová adresa** zadejte `https://www.litware.com`.
6. Zvolte **Uložit**.

#### <a name="activate-an-er-configuration-provider"></a>Aktivace poskytovatele konfigurace elektronického výkaznictví

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** klikněte v části **Poskytovatelé konfigurací** na dlaždici **Litware, Inc.** a poté vyberte možnost **Nastavit jako aktivní**.

Další informace o poskytovatelích konfigurací elektronického výkaznictví naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>Importujte počáteční verze standardních konfigurací ER

Chcete-li přidat standardní konfigurace ER do aktuální instance Finance, musíte je importovat z [úložiště](general-electronic-reporting.md#Repository) ER, jež je pro tuto instanci nakonfigurováno.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Chcete-li zobrazit seznam úložišť pro poskytovatele Microsoft, klikněte na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurací** na dlaždici **Microsoft** a poté vyberte možnost **Úložiště**.
3. Na stránce **Úložiště konfigurací** vyberte úložiště typu **Globální** a poté zvolte **Otevřít**. Pokud budete vyzváni k autorizaci pro připojení ke službě Regulatory Configuration Service, postupujte podle pokynů k autorizaci.
4. Na stránce **Úložiště konfigurace** vyberte ve stromu konfigurací v levém podokně konfiguraci formátu **Prodejní faktury Peppol**.
5. Na záložce s náhledem **Verze** vyberte verzi **11.2.2**.
6. Volbou **Importovat** stáhnete vybranou verzi z globálního úložiště.

![Stránka úložiště konfigurace](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> Pokud máte potíže s přístupem na [globální úložiště](er-download-configurations-global-repo.md), můžete si místo toho [stáhnout konfigurace](download-electronic-reporting-configuration-lcs.md) ze služby Microsoft Dynamics Lifecycle Services (LCS).

### <a name="review-the-imported-er-configurations"></a>Kontrola importovaných konfigurací ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace** rozbalte pevnou záložku **Konfigurační komponenty**.
4. V konfiguračním stromu v levém podokně rozbalte **Model faktury** a poté rozbalte **Prodejní faktura UBL**.

Všimněte si, že kromě vybraného formátu ER **Prodejní faktura Peppol** byly importovány další požadované konfigurace ER. Protože nové verze konfigurací ER jsou neustále publikovány do globálního úložiště a LCS, aby odpovídající řešení vyhovovala novým požadavkům, nejnovější verze požadované konfigurace [datového modelu](general-electronic-reporting.md#data-model-and-model-mapping-components) a jeho konfigurace [mapování modelu](general-electronic-reporting.md#data-model-and-model-mapping-components) byly importovány.

![Stránka Konfigurace](./media/er-quick-start3-imported-solution1a.png)

Pro simulaci stavu, ve kterém by byly konfigurace ER v aktuální instanci Finance, pokud jste importovali verzi **11.2.2** formátu ER **Prodejní faktura Peppol** v minulosti (například 7. srpna 2019), postupujte takto.

- V podokně akcí vyberte **Odstranit** a odstraňte všechny konfigurace ER, které byly publikovány po 7. srpnu 2019. Ponechány musí bát pouze konfigurace **Model faktury**, **Mapování modelu faktury** (původně pojmenovaná **Mapování modelu faktury zákazníka**), **Prodejní faktura UBL** a **Prodejní faktura Peppol**.
- U zbývajících konfigurací ER na pevné záložce **Verze** vyberte **Odstranit** a odstraňte všechny verze konfigurací ER, které byly publikovány po 7. srpnu 2019.

Potom se ujistěte, že ve stromu konfigurací jsou k dispozici následující konfigurace:

- Konfigurace datového modelu ER **Model faktury** (původně pojmenovaná **Model faktury zákazníka**):

    - Verze 11 obsahuje verzi 10 komponenty ER [datový model](general-electronic-reporting.md#data-model-and-model-mapping-components), která představuje datovou strukturu fakturační obchodní domény. Tato konfigurace ER byla importována jako předchůdce formátu ER **Prodejní faktura Peppol**, který byl vybrán pro import.
    - Verze 50 obsahuje verzi 31 komponentu ER datového modelu. Tato konfigurace ER byla importována jako předchůdce verze z 7. srpna 2019 konfigurace mapování modelu ER **Mapování modelu faktury**.

    ![Konfigurace datového modelu modelu ER na stránce Konfigurace](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Pokud nevidíte verzi 50 tohoto datového modelu, otevřete globální úložiště a importujte verzi 50.19 konfigurace ER **Mapování modelu faktury**.

- Konfigurace mapování modelu ER **Mapování modelu faktury** (původně pojmenovaná **Mapování modelu faktury zákazníka**):

    - Verze 50.19 byla importována jako nejnovější implementace verze 50 konfigurace datového modelu ER **Model faktury**. Obsahuje dvě komponenty ER [mapování modelu](general-electronic-reporting.md#data-model-and-model-mapping-components), které popisují, jak je datový model vyplněn daty aplikace za běhu.

    ![Konfigurace mapování modelu ER mapování faktury na stránce Konfigurace](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Pokud nevidíte verzi 50.19 tohoto mapování modelu, otevřete globální úložiště a importujte verzi 50.19 konfigurace ER **Mapování modelu faktury**.

- Konfigurace formátu elektronického výkaznictví **Prodejní faktura UBL**:

    - Verze 11.2 obsahuje [formát](general-electronic-reporting.md#FormatComponentOutbound) a komponenty ER mapování formátu. Komponenta formát určuje rozvržení sestavy. Komponenta mapování formátu obsahuje zdroj dat modelu a určuje, jak se tento zdroj dat používá k vyplnění rozvržení sestavy za chodu. Tento formát ER byl nakonfigurován tak, aby generoval e-faktury ve formátu Universal Business Language (UBL). Byla importována jako nadřazená verze formátu ER **Prodejní faktura Peppol**, který byl vybrán pro import.

- Konfigurace formátu elektronického výkaznictví **Prodejní faktura Peppol**:

    - Verze 11.2.2 obsahuje komponenty ER pro formátování a formátování mapování, které byly konfigurovány pro generování elektronických faktur ve formátu PEPPOL (Pan-European Public Procurement OnLine).

    ![Konfigurace formátu ER prodejní faktury Peppol na stránce Konfigurace](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>Konfigurujte parametry pohledávek.

1. Přejděte do **Pohledávky** \> **Nastavení** \> **Parametry pohledávek**.
2. Na kartě **Elektronické dokumenty** na pevné záložce **Elektronické výkaznictví** v poli **Prodejní a volná faktura** vyberte **Prodejní faktura Peppol**.
3. Zvolte **Uložit**.

![Karta Elektronické dokumenty na stránce Parametry pohledávek](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>Nakonfigurujte parametry právnické osoby

1. Přejděte do části **Správa organizace** \> **Organizace** \> **Právnické osoby**.
2. Pro vybranou společnost **DEMF** na pevné záložce **Informace o bankovním účtu** v poli **Směrovací číslo** zadejte **1234**.
3. Zvolte **Uložit**.
4. Zavřete stránku **Právnické osoby**.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Příprava záznamu odběratele

1. Přejděte na **Pohledávky** \> **Odběratelé** \> **Všichni odběratelé**.
2. Na stránce **Všichni zákazníci** vyberte odkaz na zákaznický účet **DE-014**.

### <a name="add-a-customer-contact"></a>Přidat kontakt na odběratele

1. Přejděte na **Pohledávky** \> **Odběratelé** \> **Všichni odběratelé**.
2. V podokně akcí na kartě **Odběratel** ve skupině **Obchodní vztahy** zvolte **Kontakty**.
3. Vyberte **Přidat kontakty**.
4. Na stránce **Kontakty** v poli **Jméno** otevřete vyhledávání, vyberte **Adam Carter** a potom vyberte **Vybrat** pro zavření vyhledávání.
5. Zvolte **Uložit**.
6. Zavřete stránku **Kontakty**.

### <a name="define-a-primary-contact"></a>Definujte primární kontakt

1. Přejděte na **Pohledávky** \> **Odběratelé** \> **Všichni odběratelé**.
2. Na pevné záložce **Demografie prodeje** v poli **Primární kontakt** vyberte **Adam Carter**.

### <a name="set-the-e-invoicing-option"></a>Nastavte možnost elektronické fakturace

1. Přejděte na **Pohledávky** \> **Odběratelé** \> **Všichni odběratelé**.
2. Na pevné záložce **Faktura a doručení** nastavte možnost **eFaktura** na **Ano**.
3. Zvolte **Uložit**.
4. Zavřete stránku **Všichni zákazníci**.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Zpracujte fakturu zákazníka pomocí standardních konfigurací ER.

Nyní můžete použít standardní konfigurace ER, které jste importovali, k elektronickému odeslání faktury s volným textem zákazníkovi.

### <a name="add-a-new-invoice"></a>Přidejte novou fakturu.

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Na stránce **Voná faktura** vyberte **Nová**.
3. Na pevné záložce **Záhlaví volné faktury** v poli **Zákaznický účet** vyberte **DE-014**.
4. Na pevné záložce **Řádky faktur** se automaticky přidá řádek faktury. Na tomto řádku nastavte následující pole:

    - V poli **Popis** zadejte **Poznámkový blok**.
    - V poli **Hlavní účet** vyberte **401100**.
    - Do pole **Jednotková cena** zadejte **1000**.

5. Zvolte **Uložit**.

![Stránka Volná faktura](./media/er-quick-start3-add-invoice.png)

Více informací naleznete v tématu [Vytvoření volné faktury](../../../finance/accounts-receivable/create-free-text-invoice-new.md).

### <a name="post-a-new-invoice"></a>Zaúčtujte novou fakturu.

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Na stránce **Volná faktura** v podokně akcí vyberte **Zaúčtovat**.
3. V dialogovém okně **Zaúčtovat volnou fakturu** vyberte **OK**.

![Stránka Podrobnosti volné faktury](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Odešlete zaúčtovanou fakturu.

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Na stránce **Volná faktura** v podokně Akce ve skupině **Dokument** vyberte **Poslat** \> **Originál**.

    ![Náhled původní faktury](./media/er-quick-start3-send-invoice.png)

3. Zavřete stránku **Volná faktura**.

### <a name="analyze-a-generated-e-invoice"></a>Analyzujte vygenerovanou e-fakturu

1. Přejděte na **Správa organizace** \> **Elektronická sestava** \> **Úlohy elektronických sestav**.
2. Na stránce **Úlohy elektronických sestav** vyberte počáteční záznam, který má popis úkolu **Poslat efakturu XML**.
3. Vyberte **Zobrazit soubory** pro přístup k seznamu vygenerovaných souborů.

    ![Stránka úloh elektronického vykazování](./media/er-quick-start3-jobs-list.png)

4. Vyberte **Otevřít**, chcete-li stáhnout vygenerovaný soubor XML e-faktury.
5. Analyzujte soubor XML e-faktury. Všimněte si, že schéma daně zákazníků je aktuálně reprezentováno atributy XML **schemeID** a **schemeAgencyID**. Všimněte si také, že prvek XML **cbc: CustomizationID** aktuálně obsahuje následující text: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.

    ![Náhled na vygenerovaný soubor XML e-faktury](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Přidejte vlastní databázové pole

Můžete použít funkci [Vlastní pole](../../fin-ops/get-started/user-defined-fields.md) a provést následující přizpůsobení v aktuální instanci Finance:

- Přizpůsobte strukturu databáze přidáním nového vlastního databázového pole, které ukládá federální daňový identifikační kód pro každého zákazníka.
- Přizpůsobte stránku **Zákazník** přidáním nového pole pro zadávání údajů, které lze použít k zadání hodnoty daňového kódu do nového pole vlastní databáze.

Podle těchto pokynů proveďte přizpůsobení.

1. Přejděte na **Pohledávky** \> **Odběratelé** \> **Všichni odběratelé**.
2. Na stránce **Všichni zákazníci** vyberte odkaz na zákaznický účet **DE-014**.
3. Na pevné záložce **Všeobecné** klikněte pravým tlačítkem do libovolné prázdné oblasti pod polem **Jazyk** a poté vyberte **Personalize: UpperGroup**.

    Obsah pevné záložky **Všeobecné** je zvýrazněný a zobrazí se nabídka **Přizpůsobit**.

4. V nabídce **Přizpůsobit** vyberte **Přidat pole**.
5. V dialogovém okně **Přidat sloupce** vyberte **Vytvořit nové pole**.
6. V dialogovém okně **Vytvořit nové pole** v poli **Název tabulky** vyberte **Zákazníci**.
7. Do pole **Předpona názvu** zadejte **FederalTaxID**.

    > [!NOTE]
    > Název celého pole byl automaticky definován jako **FederalTaxID\_Custom**.

8. Do pole **Popisek** zadejte **ID federální daně**.
9. V poli **Typ** vyberte **Text**.
10. Do pole **Délka** zadejte hodnotu **20**.
11. Zvolte **Uložit**.
12. V zobrazeném okně se zprávou vyberte **Ano** a potvrďte, že chcete vytvořit novou položku pole **FederalTaxID** pro tabulku **Zákazníci**.
13. Vyberte **Vložit** pro <a name="insert_custom_field"></a>přidání pole **FederalTaxID\_Custom** na aktuální stránku.

    ![Stránka Všichni odběratelé](./media/er-quick-start3-create-new-field.gif)

14. Zavřete stránku **Všichni zákazníci**.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>Obnovte metadata ER

Musíte aktualizovat metadata ER, abyste vytvořili vlastní pole, které jste přidali [viditelné](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) v návrháři mapování modelu ER.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Opětovné sestavení odkazů tabulky**.
2. V dialogovém okně **Aktualizovat datový model** vyberte **OK**.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>Navrhněte vlastní konfigurace ER

Pomocí konfigurací ER poskytovaných společností Microsoft můžete navrhnout své vlastní konfigurace ER tak, aby generovaly e-faktury, které obsahují nový daňový kód.

### <a name="customize-the-data-model-configuration"></a>Přizpůsobte konfiguraci datového modelu

Jako uživatel v roli konzultanta funkčních elektronických zpráv můžete navrhnout svůj vlastní datový model ER.

#### <a name="add-a-custom-data-model-configuration"></a>Přidání vlastní konfigurace datového modelu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně vyberte **Model faktury zákazníka**.
3. V podokně akcí vyberte **Vytvořit konfiguraci**.
4. V rozevíracím dialogovém okně v poli **Nový** vyberte **Odvozeno z názvu: Model faktury zákazníka, Microsoft** k označení, že vaše nová vlastní konfigurace datového modelu ER by měla být založena na konfiguraci datového modelu ER.
5. V poli **Název** zadejte **Model faktury (Litware)**.
6. Vyberte **Vytvořit konfiguraci** pro přidání nové konfigurace ER.

Nyní můžete použít návrháře datových modelů ER k úpravě verze 50.1 konfigurace ER **Model faktury (Litware)** v **Návrhu** [stavu](general-electronic-reporting.md#component-versioning).

![Verze 50.1 konfigurace ER na stránce Konfigurace](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Konfigurace vlastního datového modelu

Musíte upravit svůj vlastní datový model přidáním nového pole a poskytnout hodnotu federálního daňového identifikačního kódu. Tento kód je součástí údajů o zákaznících pro každý formát ER, který bude tento datový model používat jako zdroj dat.

1. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně vyberte **Model faktury (Litware)**.
2. Na záložce s náhledem **Verze** vyberte verzi **50.1** vybrané konfigurace datového modelu ER ve stavu **Koncept**.
3. V podokně akcí vyberte **Návrhář** pro vybranou verzi konfigurace.
4. Na stránce **Návrhář datových modelů** ve stromu datového modelu vyberte **Informace o zákazníkovi (zákazník)**.
5. Zvolte **Nové**.
6. V rozevíracím dialogovém okně v poli **Nový uzel jako** přijměte výchozí hodnotu **Podřízená úroveň aktivního uzlu**.
7. Do pole **Název** zadejte **FederalTaxID\_Litware**.
8. V poli **Typ položky** přijměte výchozí hodnotu **Řetězec**.
9. Vyberte **Přidat** a potom **Uložit**.

    ![Stránka Návrhář modelu dat](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > Pole **Označení** a **Popis** popisují účel nového pole. Tato pole můžete vyplnit ve více jazycích. Další informace najdete v tématu [Návrh vícejazyčných sestab v elektronickém výkaznictví](er-design-multilingual-reports.md).

10. Zavřete stránku **Návrhář datového modelu**.

#### <a name="complete-a-custom-data-model-configuration"></a>Dokončete vlastní konfigurace datového modelu

Musíte [dokončit](general-electronic-reporting.md#component-versioning) práci s verzí 50.1 vaší vlastní konfigurace datového modelu ER, abyste ji zpřístupnili, aby bylo možné přidat další vlastní konfigurace ER.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury** a vyberte možnost **Model faktury (Litware)**.
3. Na záložce s náhledem **Verze** vyberte možnost **Změnit stav** \> **Dokončeno** a poté klikněte na **OK**.

Stav verze 50.1 se změní z **Koncept** na **Dokončeno** a verze se změní tak, že bude pouze pro čtení. Byla přidána nová editovatelná verze 50.2, která je nyní ve stavu **Koncept**. Tuto verzi můžete použít k provedení dalších změn ve vlastní konfiguraci datového modelu ER.

![Verze 50.1 dokončena na stránce Konfigurace](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>Přizpůsobte konfiguraci mapování modelu

Jako uživatel v roli vývojáře elektronických zpráv můžete navrhnout svůj vlastní mapování modelu ER.

#### <a name="add-a-custom-model-mapping-configuration"></a>Přidání vlastní konfigurace mapování modelu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury zákazníka** a vyberte možnost **Mapování modelu faktury zákazníka**.
3. V podokně akcí vyberte **Vytvořit konfiguraci**.
4. V rozevíracím dialogovém okně v poli **Nový** vyberte **Odvozeno z názvu: Mapování modelu faktury zákazníka, Microsoft** k označení, že vaše nová vlastní konfigurace mapování modelu ER by měla být založena na konfiguraci mapování modelu ER.
5. V poli **Název** zadejte **Mapování modelu faktury (Litware)**.
6. V poli **Cílový model** vyberte **Model faktury (Litware)**.

    > [!IMPORTANT]
    > Tento krok je velmi důležitý. Pokud ho vynecháte, nebudete moci v mapování nakonfigurovaného modelu použít svůj vlastní datový model.

7. Vyberte **Vytvořit konfiguraci** pro přidání nové konfigurace ER.

![Přidání vlastní konfigurace mapování modelu na stránce Konfigurace](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Konfigurace vlastního mapování modelu

Musíte upravit mapování vlastního modelu a určit, jak by mělo vlastní pole **FederalTaxID\_Litware** vlastního datového modelu být za běhu vyplněno daty aplikace.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury zákazníka** \> **Mapování modelu faktury zákazníka** a vyberte **Mapování modelu faktury (Litware)**.
3. V podokně akcí zvolte **Návrhář**.
4. Na stránce **Mapování modelu na zdroj dat** vyberte mapování **Faktury zákazníka**.

    ![Stránka Mapování modelu na zdroj dat](./media/er-quick-start3-select-customer-mapping.png)

5. Vyberte možnost **Návrhář**.
6. Na stránce **Návrhář mapování modelů** v podokně **Zdroje dat** rozbalte datový zdroj **CustInvoiceJour**, který představuje tabulku aplikkace **CustInvoiceJour**.
7. V **CustInvoiceJour** rozbalte **Vztahy** pro kontrolu seznamu vztahů typu N:1 pro tabulku **CustInvoiceJour**.
8. V **CustInvoiceJour** \> **Vztahy** rozbalte **Zákazníci (CustTable)** pro přístup k polím a vztahům tabulky **Zákazníci (CustTable)**.
9. Vyberte pole zdroje dat **FederalTaxID\_Custom**, které jste implementovali [dříve](#insert_custom_field).
10. V podokně **Datový model** rozbalte **Informace o zákazníkovi (zákazník)** a vyberte pole datového modelu **FederalTaxID\_Litware**.
11. Vyberte možnost **vazba**.

    ![Stránka návrháře mapování modelu](./media/er-quick-start3-customize-model-mapping.gif)

12. Zvolte **Uložit**.
13. Zavřete stránku **Návrhář mapování modelu**.
14. Zavřete stránku **Mapování modelu na zdroj dat**.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Dokončete vlastní konfigurace mapování datového modelu

Musíte [dokončit](general-electronic-reporting.md#component-versioning) práci s verzí 50.19.1 vaší vlastní konfigurace mapování modelu ER, aby byla k dispozici pro použití.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury zákazníka** \> **Mapování modelu faktury zákazníka** a vyberte **Mapování modelu faktury (Litware)**.
3. Na záložce s náhledem **Verze** vyberte možnost **Změnit stav** \> **Dokončeno** a poté klikněte na **OK**.

Stav verze 50.19.1 se změní z **Koncept** na **Dokončeno** a verze se změní tak, že bude pouze pro čtení. Byla přidána nová editovatelná verze 50.19.2, která je nyní ve stavu **Koncept**. Tuto verzi můžete použít k provedení dalších změn ve vlastní konfiguraci mapování modelu ER.

![Verze 50.19.1 dokončena na stránce Konfigurace](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> Podporovaná konfigurace [životního cyklu](general-electronic-reporting-manage-configuration-lifecycle.md) nepokrývá životní cyklus databázových změn. Pokud exportujete verzi 50.19.1 konfigurace **Mapování modelu faktury (Litware)** z aktuální instance Finance a zkusíte ji importovat do jiné instance, která neobsahuje vlastní pole **FederalTaxID\_Custom** v tabulce **CustTable**, dojde k výjimce. Výjimkou bude uvedeno, že importovaná konfigurace ER není kompatibilní s metadaty cílové instance Finance.

### <a name="customize-the-format-configuration"></a>Přizpůsobení konfigurace formátu

Jako uživatel v roli konzultanta funkčních elektronických zpráv můžete navrhnout svůj vlastní formát ER.

#### <a name="add-a-custom-format-configuration"></a>Přidání vlastní konfigurace formátu ER

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury zákazníka** \> **Prodejní faktura UBL** a vyberte možnost **Prodejní faktura Peppol**.
3. V podokně akcí vyberte **Vytvořit konfiguraci**.
4. V rozevíracím dialogovém okně v poli **Nový** vyberte **Odvozeno z názvu: Prodejní faktura Peppol, Microsoft** k označení, že vaše vlastní konfigurace formátu ER by měla být založena na konfiguraci formátu ER.
5. V poli **Název** zadejte **Prodejní faktura Peppol (Litware)**.
6. V poli **Datový model** vyberte **Model faktury (Litware)**, chcete-li používat svůj vlastní datový model a komponenty mapování modelu.

    > [!NOTE]
    > Tento krok je velmi důležitý. Pokud ho vynecháte, nebudete moci v nakonfigurovaném formátu použít svůj vlastní datový model.

7. V poli **Datový model** vyberte kořenovou definici **InvoiceCustomer**.
8. Vyberte **Vytvořit konfiguraci** pro přidání nové konfigurace ER.

![Přidání vlastní konfigurace formátu na stránce Konfigurace](./media/er-quick-start3-adding-custom-format.png)

Nyní můžete použít návrháře operací ER k úpravě verze 11.2.2.1 konfigurace ER **Prodejní faktury Peppol (Litware)** v **Koncept** [stavu](general-electronic-reporting.md#component-versioning).

![Verze 11.2.2.1 konfigurace ER na stránce Konfigurace](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Konfigurace vlastního formátu

Svůj vlastní formát musíte upravit přidáním nového prvku formátu, který vyplní hodnotu federálního daňového identifikačního kódu fakturovaného zákazníka.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury zákazníka** \> **Prodejní faktura UBL** \> **Prodejní faktura Peppol** a vyberte možnost **Prodejní faktura Peppol (Litware)**.
3. V podokně akcí zvolte **Návrhář**.
4. Ve stromě formátů rozbalte **XMLHeader** \> **Faktura** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** a vyberte **cbc:ID**.
5. Vyberte **Přidat** a potom **XML** \> **Atribut**.
6. V dialogovém okně **Vlastnost komponenty** do pole **Název** zadejte **FederalTaxID**.
7. Vyberte **OK**, chcete-li přidat nový prvek formátu a vytvořit nový atribut XML **FederalTaxID** v generovaném souboru XML.
8. Ve stromě formátů v **XMLHeader** \> **Faktura** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** vyberte **FederalTaxID**.
9. Vyberte **Přesunout nahoru**.

![Nový prvek formátu na stránce Návrhář formátu](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Konfigurace vlastního mapování formátu

1. Na stránce **Návrhář formátu** na kartě **Mapování** rozbalte zdroj dat **Faktura** typu **Model**.
2. Ve **Faktuře** rozbalte **Informace o zákazníkovi (zákazník)** a vyberte **FederalTaxID\_Litware**.
3. Vyberte možnost **vazba**.

    ![Stránka návrháře formátu](./media/er-quick-start3-customized-format-mapping.png)

4. Vyberte zdroj dat **Faktura** typu **Model** a potom vyberte **Upravit**.
5. V poli **Verze** vyberte verzi **1** vašeho vlastního datového modelu a poté vyberte **OK**.
6. Zvolte **Uložit**.
7. Zavřete stránku **Návrhář formátu**.

#### <a name="complete-a-custom-format-configuration"></a>Dokončete vlastní konfigurace formátu

Musíte [dokončit](general-electronic-reporting.md#component-versioning) práci s verzí 11.2.2.1 vaší vlastní konfigurace formátu ER, aby byla k dispozici pro použití.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury zákazníka** \> **Prodejní faktura UBL** \> **Prodejní faktura Peppol** a vyberte možnost **Prodejní faktura Peppol (Litware)**.
3. Na záložce s náhledem **Verze** vyberte možnost **Změnit stav** \> **Dokončeno** a poté klikněte na **OK**.

Stav verze 11.2.2.1 se změní z **Koncept** na **Dokončeno** a verze se změní tak, že bude pouze pro čtení. Byla přidána nová editovatelná verze 11.2.2.2, která je nyní ve stavu **Koncept**. Tuto verzi můžete použít k provedení dalších změn ve vlastní konfiguraci formátu ER.

![Verze 11.2.2.1 dokončena na stránce Konfigurace](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Nakonfigurujte parametry pohledávek, abyste mohli začít používat vlastní konfigurace ER.

1. Přejděte do **Pohledávky** \> **Nastavení** \> **Parametry pohledávek**.
2. Na kartě **Elektronické dokumenty** na pevné záložce **Elektronické výkaznictví** v poli **Prodejní a volná faktura** vyberte **Prodejní faktura Peppol (Litware)**.
3. Zvolte **Uložit**.

![Stránka Parametry pohledávek, karta Elektronické dokumenty, pevná záložka Elektronické vykazování](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Aktualizujte záznam zákazníka přidáním federálního daňového identifikačního kódu

1. Přejděte na **Pohledávky** \> **Odběratelé** \> **Všichni odběratelé**.
2. Na stránce **Všichni zákazníci** vyberte odkaz na zákaznický účet **DE-014**.
3. Na pevné záložce **Všeobecné** v poli **ID federální daně** zadejte **LITWARE-6789**.
4. Zvolte **Uložit**.

    ![Stránka podrobnosti o zákazníkovi De-014](./media/er-quick-start3-added-tax-id-value.png)

5. Zavřete stránku **Všichni zákazníci**.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Zpracujte fakturu zákazníka pomocí vlastních konfigurací ER.

### <a name="select-and-send-a-posted-invoice"></a>Zvolte a odešlete zaúčtovanou fakturu.

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Na stránce **Volná faktura** vyberte fakturu, kterou jste dříve přidali a zaúčtovali.
3. V podokně akcí ve skupině **Dokument** vyberte **Poslat** \> **Originál**.
4. Zavřete stránku **Volná faktura**.

### <a name="analyze-a-generated-e-invoice"></a>Analyzujte vygenerovanou e-fakturu

1. Přejděte na **Správa organizace** \> **Elektronická sestava** \> **Úlohy elektronických sestav**.
2. Na stránce **Úlohy elektronických sestav** vyberte poslední záznam, který má popis úkolu **Poslat efakturu XML**.
3. Vyberte **Zobrazit soubory** pro přístup k seznamu vygenerovaných souborů.
4. Vyberte **Otevřít**, chcete-li stáhnout vygenerovaný soubor XML e-faktury.
5. Analyzujte soubor XML e-faktury. Všimněte si, že v souladu s vaším přizpůsobením zahrnuje schéma daně pro zákazníky vlastní atribut XML **FederalTaxID** vedle atributů XML **schémeID** a **schemeAgencyID**. Hodnotu tohoto nového atributu XML určuje ID federální daně **LITWARE-6789**, které bylo zadáno pro fakturovaného zákazníka.

    ![Náhled na vygenerovaný soubor XML e-faktury s vašimi přizpůsobeními](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>Importujte poslední verze standardních konfigurací ER

Chcete-li zachovat sadu standardních konfigurací ER ve vaší instanci Finance [aktuální](general-electronic-reporting-manage-configuration-lifecycle.md), musíte importovat nové verze, kdykoli budou k dispozici v ER [úložišti](general-electronic-reporting.md#Repository), které bylo nakonfigurováno pro danou instanci.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Chcete-li zobrazit seznam úložišť pro poskytovatele Microsoft, klikněte na stránce **Konfigurace lokalizace** v části **Poskytovatelé konfigurací** na dlaždici **Microsoft** a poté vyberte možnost **Úložiště**.
3. Na stránce **Úložiště konfigurací** vyberte úložiště typu **Globální** a poté zvolte **Otevřít**. Pokud budete vyzváni k autorizaci pro připojení ke službě Regulatory Configuration Service, postupujte podle pokynů k autorizaci.
4. Na stránce **Úložiště konfigurace** vyberte ve stromu konfigurací v levém podokně konfiguraci formátu **Prodejní faktury Peppol**.
5. Na pevné záložce **Verze** vyberte verzi **32.6.7** vybrané konfigurace formátu ER, která byla vydána na podporu elektronických faktur zákazníků ve formátu PEPPOL BIS 3. Další informace naleznete v článku [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).
6. Vyberte **Importovat**. Vybraná verze se stáhne z globálního úložiště do aktuální instance aplikace Finance.

![Verze 32.6.7 vybraná na stránce Konfigurační úložiště](./media/er-quick-start3-import-solution2.png)

Informace o tom, jak lze tento proces automatizovat, najdete v části [Importujte aktualizované verze konfigurací ER](er-download-updated-versions-global-repo.md).

### <a name="review-the-imported-er-configurations"></a>Kontrola importovaných konfigurací ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.
3. Rozbalte pevnou záložku **Komponenty konfigurace**.
4. Ve stromu konfigurace v levém podokně rozbalte **Model faktury**. Všimněte si, že název **Model faktury zákazníka** byl změněn na **Model faktury** v jedné z importovaných konfigurací datového modelu ER.
5. Ve stromu konfigurace v levém podokně rozbalte **Mapování modelu faktury**. Všimněte si, že název **Mapování modelu faktury zákazníka** byl změněn na **Mapování modelu faktury** v jedné z importovaných konfigurací naoivání modelu ER.
6. Rozbalte **Prodejní faktura UBL** \> **Prodejní faktura Peppol**.

Všimněte si, že kromě vybraného formátu ER **Prodejní faktura Peppol** byly importovány poslední verze dalších požadovaných konfigurací ER. Protože nové verze konfigurací ER jsou neustále publikovány do globálního úložiště a LCS, aby odpovídající řešení ER vyhovovala novým požadavkům, nejnovější verze požadované konfigurace datového modelu a jeho konfigurace mapování modelu byly importovány.

Ujistěte se, že ve stromu konfigurací jsou nakonec k dispozici následující konfigurace ER:

- Konfigurace datového modelu ER **Model faktury**:

    - Verze 206 (nebo pozdější) obsahuje verzi 24 (nebo pozdější) komponenty ER datový model, která představuje datovou strukturu fakturační obchodní domény. Tato konfigurace ER byla importována jako předchůdce nejnovějšího dostupné konfigurace mapování modelu ER **Mapování modelu faktury**.

    ![Verze 206 na stránce Konfigurace](./media/er-quick-start3-imported-solution2b1.png)

- Konfigurace mapování modelu ER **Mapování modelu faktury**:

    - Verze 206.132 (nebo pozdější) byla importována jako nejnovější implementace verze 206 konfigurace datového modelu ER **Model faktury**. Obsahuje několik komponent ER mapování modelu, které popisují, jak je datový model vyplněn daty aplikace za běhu.

    ![Verze 206.132 na stránce Konfigurace](./media/er-quick-start3-imported-solution2b2.png)

- Konfigurace formátu elektronického výkaznictví **Prodejní faktura UBL**:

    - Verze 32.6 obsahuje formát a komponenty ER mapování formátu. Komponenta formát určuje rozvržení sestavy. Komponenta mapování formátu obsahuje zdroj dat modelu a určuje, jak se tento zdroj dat používá k vyplnění rozvržení sestavy za chodu. Tento formát ER byl nakonfigurován tak, aby generoval e-faktury ve formátu UBL. Byla importována jako nadřazená verze formátu ER **Prodejní faktura Peppol**, který byl vybrán pro import.

- Konfigurace formátu elektronického výkaznictví **Prodejní faktura Peppol**:

    - Verze 32.6.7 obsahuje komponenty ER pro formátování a formátování mapování, které byly konfigurovány pro generování elektronických faktur ve formátu PEPPOL.

    ![Verze 32.6.7 na stránce Konfigurace](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>Přijměte změny nových verzí standardních konfigurací ER ve svých vlastních konfiguracích ER.

### <a name="adopt-your-custom-er-data-model"></a>Přijměte svůj vlastní datový model ER

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury** a vyberte možnost **Model faktury (Litware)**.
3. Na záložce s náhledem **Verze** u verze konceptu **50.2** vybrané konfigurace datového modelu vyberte **Přeskládat**.
4. V poli **Cílová verze** potvrďte výběr verze **206** základní konfigurace datového modelu ER a poté vyberte **OK**.

    Koncept verze vaší vlastní konfigurace datového modelu ER je přečíslován z **50.2** na **206.2** k označení, že nyní obsahuje vaše přizpůsobení, které bylo sloučeno se změnami v nejnovější verzi (206) konfigurace základního datového modelu ER.

    > [!NOTE]
    > Akce přestavby je vratná. Chcete-li tuto přestavbu zrušit, vyberte verzi **50.1** modelu **Model faktury (Litware)** na záložce s náhledem **Verze** a poté vyberte možnost **Získat tuto verzi**. Verze 206.2 se poté přečísluje zpět na **50.2** a obsah konceptové verze 50.2 bude odpovídat obsahu verze 50.1.

5. Na záložce s náhledem **Verze** vyberte možnost **Změnit stav** \> **Dokončeno** a poté klikněte na **OK**.

Stav verze 206.2 se změní z **Koncept** na **Dokončeno** a verze se změní tak, že bude pouze pro čtení. Byla přidána nová editovatelná verze 206.3, která je nyní ve stavu **Koncept**. Tuto verzi můžete použít k provedení dalších změn ve vlastní konfiguraci datového modelu ER.

![Verze 206.2 dokončena na stránce Konfigurace](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Přijměte svůj vlastní mapování modelu ER

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury** \> **Mapování modelu faktury** a vyberte **Mapování modelu faktury (Litware)**.
3. Na záložce s náhledem **Verze** u verze konceptu **50.19.2** vybrané konfigurace mapování modelu vyberte **Přeskládat**.
4. V poli **Cílová verze** potvrďte výběr verze **206.132** základní konfigurace mapování modelu ER a poté vyberte **OK**.

    Koncept verze vaší vlastní konfigurace mapování modelu ER je přečíslován z **50.19.2** na **206.132.2** k označení, že nyní obsahuje vaše přizpůsobení, které bylo sloučeno se změnami v nejnovější verzi (206.132) konfigurace základního mapování modelu ER.

    Všimněte si, že byly objeveny některé konflikty přeskládání. Nyní musíte tyto konflikty vyřešit ručně.

    ![Zpráva konfliktů přeskládání na stránce Konfigurace](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. V podokně akcí vyberte **Návrhář** a poté v seznamu mapování vyberte **zákaznická faktura**.
6. U každého konfliktu přeskládání vyberte **Zachovat vlastní hodnotu**, protože pro každou uvedenou komponentu musíte zachovat číslo verze svého vlastního datového modelu.

    ![Konflikty přeskládání na stránce návrháře mapování modelů](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. Vyberte **Uložit** a poté zavřete stránku **Návrhář mapování modelů**.
8. V seznamu mapování vyberte **Projektová faktura**.
9. U každého konfliktu přeskládání vyberte **Zachovat vlastní hodnotu**, protože pro každou uvedenou komponentu musíte zachovat číslo verze svého vlastního datového modelu.
10. Vyberte **Uložit** a poté zavřete stránku **Mapování modelů**.

    > [!NOTE]
    > Akce přestavby je vratná. Chcete-li toto přeskládání zrušit, vyberte verzi **50.19.1** mapování modelu **Mapování modelu faktury (Litware)** na záložce s náhledem **Verze** a poté vyberte možnost **Získat tuto verzi**. Verze 206.132.2 se poté přečísluje zpět na **50.19.2** a obsah konceptové verze 50.19.2 bude odpovídat obsahu verze 50.19.1.

11. Na záložce s náhledem **Verze** vyberte možnost **Změnit stav** \> **Dokončeno** a poté klikněte na **OK**.

Stav verze 206.132.2 se změní z **Koncept** na **Dokončeno** a verze se změní tak, že bude pouze pro čtení. Byla přidána nová editovatelná verze 206.132.3, která je nyní ve stavu **Koncept**. Tuto verzi můžete použít k provedení dalších změn ve vlastní konfiguraci mapování modelu ER.

![Verze 206.132.2 dokončena na stránce Konfigurace](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Přijměte svůj vlastní formát ER

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model faktury** \> **Prodejní faktura UBL** \> **Prodejní faktura Peppol** a vyberte možnost **Prodejní faktura Peppol (Litware)**.
3. Na záložce s náhledem **Verze** u verze konceptu **11.2.2.2** vybrané konfigurace formátu vyberte **Přeskládat**.
4. V poli **Cílové** verze potvrďte výběr verze **32.6.7** základní konfigurace formátu ER a poté vyberte **OK**.

    Koncept verze vaší vlastní konfigurace formátu ER je přečíslován z **11.2.2.2** na **32.6.7.2** k označení, že nyní obsahuje vaše přizpůsobení, které bylo sloučeno se změnami v nejnovější verzi (32.6.7) konfigurace základního formátu ER.

    Všimněte si, že byly objeveny některé konflikty přeskládání. Nyní musíte tyto konflikty vyřešit ručně.

5. V podokně akcí zvolte **Návrhář**.
6. U každého konfliktu přeskládání vyberte **Zachovat vlastní hodnotu**, protože pro každou uvedenou komponentu musíte zachovat číslo verze svého vlastního datového modelu.
7. Zvolte **Uložit**.
8. Na kartě **Mapování** vyberte zdroj dat **Faktura** typu **Model** a potom vyberte **Upravit**.
9. V poli **Verze** vyberte verzi **2** vašeho vlastního datového modelu a poté vyberte **OK**.
10. Zvolte **Uložit**.

    > [!NOTE]
    > Akce přestavby je vratná. Chcete-li toto přeskládání zrušit, vyberte verzi **11.2.2.1** formátu **Prodejní faktura Peppol (Litware)** na záložce s náhledem **Verze** a poté vyberte možnost **Získat tuto verzi**. Verze 32.6.7.2 se poté přečísluje zpět na **11.2.2.2** a obsah konceptové verze 11.2.2.2 bude odpovídat obsahu verze 11.2.2.1.

11. Zavřete stránku **Návrhář formátu**.
12. Na záložce s náhledem **Verze** vyberte možnost **Změnit stav** \> **Dokončeno** a poté klikněte na **OK**.

Stav verze 32.6.7.2 se změní z **Koncept** na **Dokončeno** a verze se změní tak, že bude pouze pro čtení. Byla přidána nová editovatelná verze 32.6.7.3, která je nyní ve stavu **Koncept**. Tuto verzi můžete použít k provedení dalších změn ve vlastní konfiguraci formátu ER.

![Verze 32.6.7.2 dokončena na stránce Konfigurace](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Zpracujte fakturu zákazníka pomocí nových verzí vlastních konfigurací ER.

### <a name="select-and-send-a-posted-invoice"></a>Zvolte a odešlete zaúčtovanou fakturu.

1. Přejděte na **Pohledávky** \> **Faktury** \> **Všechny volné faktury**.
2. Na stránce **Volná faktura** vyberte fakturu, kterou jste dříve přidali a zaúčtovali.
3. V podokně akcí ve skupině **Dokument** vyberte **Poslat** \> **Originál**.

    > [!NOTE] 
    > Protože nyní máte dvě verze **Prodejní faktura Peppol (Litware)** konfigurace formátu ER a žádná verze nemá [datum účinnosti](general-electronic-reporting.md#component-date-effectivity), k vygenerování e-faktury se použije nejnovější verze.

4. Zavřete stránku **Volná faktura**.

### <a name="analyze-a-generated-e-invoice"></a>Analyzujte vygenerovanou e-fakturu

1. Přejděte na **Správa organizace** \> **Elektronická sestava** \> **Úlohy elektronických sestav**.
2. Na stránce **Úlohy elektronických sestav** vyberte nejnovější záznam, který má popis úkolu **Poslat efakturu XML**.
3. Vyberte **Zobrazit soubory** pro přístup k seznamu vygenerovaných souborů.
4. Vyberte **Otevřít**, chcete-li stáhnout vygenerovaný soubor XML e-faktury.
5. Analyzujte soubor XML e-faktury. Všimněte si, že v souladu s vaším přizpůsobením stále zahrnuje schéma daně pro zákazníky vlastní atribut XML **FederalTaxID** vedle atributů XML **schémeID** a **schemeAgencyID**. Navíc proto, že změny v nové verzi základního formátu **Prodejní faktura UBL** byly sloučeny s vaším přizpůsobením, text prvku XML **cbc:CustomizationID** byl změněn z `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` na `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.

    ![Náhled na vygenerovaný soubor XML e-faktury s přizpůsobeními](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Stažení konfigurací ER z Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [Stažení konfigurací ER z Globálního úložiště konfigurační služby](er-download-configurations-global-repo.md)
- [Vytvořit volnou fakturu](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/create-free-text-invoice-new)
- [Vytvoření vlastních polí a práce s nimi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
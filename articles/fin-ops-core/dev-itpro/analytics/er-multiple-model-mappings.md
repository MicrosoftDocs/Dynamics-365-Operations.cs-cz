---
title: Správa několika odvozených mapování pro jeden kořen modelu
description: Toto téma vysvětluje, jak spravovat několik odvozených mapování, která byla nakonfigurována pro jeden kořen modelu.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a774a0edf00a17be674b7a1bb07f6494e90554c3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743672"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Správa několika odvozených mapování pro jeden kořen modelu

[!include [banner](../includes/banner.md)]

Komponenta [Elektronické výkaznictví (ER)](general-electronic-reporting.md) datového [modelu](general-electronic-reporting.md#data-model-and-model-mapping-components) se používá v každé konfigurované komponentě ER [formát](general-electronic-reporting.md#FormatComponentOutbound) jako zdroj dat ke generování odchozích dokumentů. Chcete-li popsat jednu obchodní doménu, nakonfigurujte komponentu datového modelu, který má mnoho kořenových definic. 

Každá definice kořenového adresáře umožňuje reprezentovat data dané domény způsobem, který se nejlépe hodí pro konkrétní účely vytváření sestav. Pro každou definici kořene můžete nakonfigurovat ER [mapování modelu](general-electronic-reporting.md#data-model-and-model-mapping-components) komponenta jako implementaci specifickou pro Microsoft Dynamics 365 Finance – vašeho datového modelu. Tímto způsobem popisujete, jak bude váš datový model vyplněn za běhu.

Součásti mapování modelu ER mohou být umístěny v datovém modelu ER [konfigurace](general-electronic-reporting.md#Configuration) a konfigurace mapování modelu ER. Jedna konfigurace ER může obsahovat mnoho mapovacích komponent, z nichž každá je nakonfigurována pro definici jednoho kořene. Případně jedna konfigurace ER může obsahovat jen jednu mapovací komponentu, která je nakonfigurována pro definici jednoho kořene.

Mnoho poskytovatelů konfigurace může nabídnout konfigurace mapování modelu ER pro stejný datový model ER. Tyto konfigurace mapování modelů mohou obsahovat komponenty mapování pro různé definice kořenů. Můžete použít mapování modelu pro jednu kořenovou definici, kterou nabízí jeden [poskytovatel](general-electronic-reporting.md#Provider) a použít mapování modelu pro jinou definici kořene, kterou nabízí jiný poskytovatel.

Postupy v tomto tématu vysvětlují, jak spravovat více konfigurací mapování modelu ER datového modelu ER, pokud obsahují různé komponenty mapování modelu nakonfigurované pro stejnou definici kořene. 

Abyste mohli dokončit postupy v tomto tématu, musíte mít přiřazenou roli správce systému nebo vývojáře elektronického vykazování.

Všechny následující procedury lze provést ve společnosti USMF. Není nutné žádné kódování.

## <a name="configure-the-er-framework"></a>Konfigurace rámce ER

Jako uživatel v roli vývojáře elektronického výkaznictví musíte [nakonfigurovat minimální sadu parametrů ER](er-quick-start2-customize-report.md#ConfigureFramework), abyste mohli začít používat rámec ER k navrhovánínového ER řešení.

## <a name="import-the-standard-er-format-configurations"></a>Import standardních konfigurací formátu ER

Chcete-li přidat standardní konfigurace ER do aktuální instance, musíte je importovat z úložiště ER, jež je pro tuto instanci nakonfigurováno. Postupujte podle pokynů v části [Stažení konfigurací ER z globálního úložiště konfigurační služby](er-download-configurations-global-repo.md) pro import následující konfigurace formátu ER:

- **Volná textová faktura (Excel)**, verze 220.106
- **Projektová faktura (Excel)**, verze 226.27

## <a name="review-the-imported-er-configurations"></a>Kontrola importovaných konfigurací ER

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Na stránce **Konfigurace lokalizace** v části **Konfigurace** vyberte dlaždici **Konfigurace výkaznictví**.
3. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte **Model faktury**.

    ![Kontrola importovaných konfigurací na stránce Konfigurace](./media/er-multiple-model-mappings-image1.png)

4. Zkontrolujte formát **Volná textová faktura (Excel)**:

    1. Ve stromu konfigurace v levém podokně vyberte **Volná textová faktura (Excel)**.
    2. V podokně akcí zvolte **Návrhář**.
    3. Na stránce **Návrhář formátu** na kartě **Mapování** v seznamu zdroje dat vyberte **Model**.
    4. Vyberte **Zobrazit**.
    
       Aktuální formát ER je nakonfigurován pro použití kořenové definice **Zákazníka faktury** **Modelu faktury**. Když je tento formát spuštěn, a je volán zdroj dat **Model**, mapování modelu, které je nakonfigurováno pro kořenovou definici **Zákazníka faktury** se používá pro přístup k datům aplikace a vyplnění datového modelu.

        ![Kontrola modelového zdroje dat na stránce návrháře mapování formátu](./media/er-multiple-model-mappings-image2.png)

    6. Zavřete stránku **Návrhář formátu**.

5. Zkontrolujte obsah konfigurace **Mapování modelu faktury**:

    1. Ve stromu konfigurace v levém podokně vyberte **Mapování modelu faktury**.
    2. V podokně akcí zvolte **Návrhář**.
    3. Na stránce **Mapování modelu na zdroj dat** si všimněte, že aktuální konfigurace mapování modelu ER obsahuje několik komponent mapování modelu:

        + Mapování modelu **Zákaznická faktura** je nakonfigurováno pro kořenovou definici **Zákaznická faktura** **Modelu faktury**. Proto, když je spuštěn formát **Volná textová faktura (Excel)** ER, mapování modelu **Zákaznická faktura** lze zvolit pro přístup k datům aplikace a vyplnění datového modelu této konfigurace ER.
        + Mapování modelu **Projektová faktura** je nakonfigurováno pro kořenovou definici **InvoiceProject** **Modelu faktury**. Proto, když je spuštěn formát **Projektová faktura (Excel)** ER, lze mapování modelu **Projektová faktura** zvolit pro přístup k datům aplikace a vyplnění datového modelu této konfigurace ER.

        ![Mapování modelu faktury na model na stránce mapování zdroje dat](./media/er-multiple-model-mappings-image3.png)

    4. Zavřete stránku **Mapování modelu na zdroj dat**.
    5. Na pevné záložce **Verze** vyberte **Vymazat** pro odstranění všech verzí této konfigurace ER, které jsou novější než verze 240.175.

6. Zkontrolujte obsah konfigurace **Mapování modelu projektové faktury (RDP)**:

    1. Ve stromu konfigurace v levém podokně vyberte **Mapování modelu projektové faktury (RDP)**.
    2. V podokně akcí zvolte **Návrhář**.
    3. Na stránce **Mapování modelu na zdroj dat** si všimněte, že aktuální konfigurace mapování modelu ER obsahuje mapování modelu **InvoiceProject** a že toto mapování modelu je nakonfigurováno pro kořenovou definici **InvoiceProject** **Modelu faktury**. Když je spuštěn formát ER **Projektová faktura (Excel)**, vyberte mapování modelu **InvoiceProject** této konfigurace ER pro přístup k datům aplikace a vyplnění datového modelu.

        ![Mapování modelu projektové faktury na model na stránce mapování zdroje dat](./media/er-multiple-model-mappings-image4.png)

    4. Zavřete stránku **Mapování modelu na zdroj dat**.
    5. Na pevné záložce **Verze** vyberte **Vymazat** pro odstranění všech verzí této konfigurace ER, které jsou novější než verze 226.35.

## <a name="customize-the-imported-er-configurations"></a>Přizpůsobení importovaných konfigurací ER

Tato část vysvětluje, jak [přizpůsobit](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) mapování modelů poskytované společností Microsoft. Například může být vyžadováno přizpůsobení k implementaci vaší vlastní logiky nebo přidání chybějících vazeb.

### <a name="customize-the-invoice-model-mapping-configuration"></a>Přizpůsobení konfigurace mapování modelu faktury

1. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně vyberte **Mapování modelu faktury**.
2. V podokně akcí vyberte **Vytvořit konfiguraci**.
3. V rozevíracím dialogovém okně **Vytvořit konfiguraci** v poli **Nový** vyberte **Odvodit z názvu: mapování modelu faktury, Microsoft**.
4. V poli **Název** zadejte **Mapování modelu faktury Litware**.
5. Vyberte **Vytvořit konfiguraci**.
6. [Označte](er-quick-start2-customize-report.md#MarkFormatRunnable) [návrh](general-electronic-reporting.md#component-versioning) verze odvozeného mapování, která je k dispozici pro použití za běhu:

    1. V podokně akcí na kartě **Konfigurace** ve skupině **Upřesnit nastavení** vyberte **Parametry uživatele**.
    2. V dialogovém okně **Uživatelské parametry** nastavte u možnosti **Spustit nastavení** hodnotu **Ano** a poté stiskněte **OK**.
    3. Je-li třeba vyberte možnost **Upravit**, má-li být stránka editovatelná.
    4. Pro konfiguraci **Mapování modelu faktury Litware**, která je aktuálně vybrána ve stromu konfigurace, nastavte možnost **Spustit koncept** na **Ano**.

7. V podokně akcí vyberte **Návrhář** ke kontrole mapování modelů této konfigurace.

    ![Kontrola mapování modelu faktury na model na stránce mapování zdroje dat](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > Nyní můžete v návrháři otevřít kteroukoli z komponent mapování modelu ER této konfigurace ER a nakonfigurovat vlastní logiku. Další informace viz [Přizpůsobení konfigurace mapování modelu](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. Zavřete stránku **Mapování modelu na zdroj dat**.

Nyní máte konfigurace **Mapování modelu faktury** a **Mapování modelu faktury Litware**, z nichž každá má mapování modelu nakonfigurované pro kořenovou definici **Zákazník faktury**. Explicitně přiřaďte jedno z mapování modelu jako výchozí mapování modelu, které používá jakýkoli z formátů ER, například **Faktura RTF (Excel)**, který obsahuje zdroj dat modelu, který má kořenovou definici **Zákazník faktury**. Jinak se při spuštění, úpravě nebo ověření jednoho z formátů ER vyvolá následující výjimka, která vás upozorní, že nebylo explicitně přiřazeno žádné výchozí mapování modelu:
 
> Existuje více než jedno mapování modelu pro datový model '\<model name\> (\<root descriptor\>)' v konfiguracích \<configuration names separated by commas\>. Nastavte jednu z konfigurací jako výchozí.

![Otevření formátu pro úpravy na stránce Konfigurace](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>Přizpůsobení konfigurace mapování modelu projektu (RDP)

1. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně vyberte **Mapování modelu projektové faktury (RDP)**.
2. V podokně akcí vyberte **Vytvořit konfiguraci**.
3. V rozevíracím dialogovém okně **Vytvořit konfiguraci** v poli **Nový** vyberte **Odvodit z názvu: mapování modelu projektové faktury (RDP), Microsoft**.
4. V poli **Název** zadejte **Mapování modelu projektové faktury Litware**.
5. Vyberte **Vytvořit konfiguraci**.
6. Pro konfiguraci **Mapování modelu projektové faktury**, která je aktuálně vybrána ve stromu konfigurace, nastavte možnost **Spustit koncept** na **Ano**.
7. V podokně akcí vyberte **Návrhář** ke kontrole mapování modelů této konfigurace.

    ![Kontrola mapování modelu faktury přizpůsobeného projektu na stránce mapování zdroje dat](./media/er-multiple-model-mappings-image7.png)

8. Zavřete stránku **Mapování modelu na zdroj dat**.

Nyní máte konfigurace **Mapování modelu faktury**, **Mapování modelu faktury projektu (RDP)**, a **Mapování modelu faktury projektu Litware**. Každá z těchto konfigurací má pro model nakonfigurované mapování modelu kořenová definice **InvoiceProject**. Explicitně přiřaďte jedno z mapování modelu jako výchozí mapování modelu, které používá kterýkoli z formátů ER. Například použijte formát **Projektová faktura (Excel)**, který obsahuje zdroj dat modelu, který má kořenovou definici **InvoiceProject**. Jinak se při spuštění nebo úpravě jednoho z formátů ER vyvolá následující výjimka, která vás upozorní, že nebylo explicitně přiřazeno žádné výchozí mapování modelu.

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Vyberte odvozenou konfiguraci mapování modelu faktury Litware jako konfiguraci, která obsahuje výchozí mapování modelu

1. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně vyberte **Mapování modelu faktury Litware**.
2. Nastavte možnost **Výchozí pro mapování modelu’** na **Ano**.

    ![Nastavení mapování modelu jako výchozího mapování modelu na stránce Konfigurace](./media/er-multiple-model-mappings-image8.png)

    Z tohoto důvodu se mapování modelu **Kopie faktury zákazníka** používá při spuštění **volné textové faktury (Excel)**, nebo když jej upravíte nebo ověříte. Mapování modelu **Zákaznická faktura** z konfigurace **mapování modelu faktury** je ignorováno.

    Nyní můžete otevřít formát **Volná textová faktura (Excel)** ke kontrole v návrháři formátu.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Vyberte odvozenou konfiguraci mapování modelu projektu Litware jako konfiguraci, která obsahuje výchozí mapování modelu

1. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně vyberte **Mapování modelu projektové faktury Litware**.
2. Nastavte možnost **Výchozí pro mapování modelu’** na **Ano**.

    V tomto případě, na rozdíl od případu popsaného pro konfiguraci **Mapování modelu faktury Litware** v předchozí části, nemůžete začít používat mapování modelu **Kopie InvoiceProject** z konfigurace **Mapování modelu faktury projektu Litware**. Dvě konfigurace, které obsahují mapování modelu pro kořenovou definici **InvoiceProject** jsou aktuálně označeny jako výchozí konfigurace. Proto mají stejnou prioritu použití. Chcete-li tento problém vyřešit, proveďte zbývající kroky tohoto postupu.

3. Ve stromu konfigurace v levém podokně vyberte **Mapování modelu faktury Litware**.
4. V podokně akcí zvolte **Návrhář**.
5. Na stránce **Mapování modelu na zdroj dat** vyberte **Upravit**, aby byla stránka podle potřeby upravitelná.
6. Vyberte mapování modelu **Kopie faktury projektu** a poté zaškrtněte zaškrtávací políčko **Je odstraněno**.

    ![Nastavení mapování modelu jako virtuálně odstraněného na stránce Mapování modelu na zdroj dat](./media/er-multiple-model-mappings-image9.png)

    Z tohoto důvodu se konfigurace **Mapování modelu faktury Litware** chová, jako by pro model neměla žádné mapování modelu kořenové definice **InvoiceProject**. Mapování modelu **Kopie projektové faktury** vydané ve výchozím nastavení. Konfigurace **mapování modelu projektu Litware** která obsahuje toto mapování modelu, je označená jako výchozí. Protože je označen jako výchozí, má vyšší prioritu než mapování modelu **InvoiceProject** z konfigurace **Mapování modelu faktury projektu (RDP)**.

## <a name="other-considerations"></a>Ostatní úvahy

Mapování modelu **Kopie InvoiceProject** konfigurace **Mapování modelu faktury projektu Litware** je navržena pro použití zdroje dat **ReportDataProvider**. Zdroj dat je součástí typu *Objekt*, který odkazuje na třídu aplikace **PsaProjInvoiceDP**. Tato třída je implementována jako poskytovatel dat pro sestavu faktury projektu SQL Server Reporting Services (SSRS) rámce správy tisku. Vyberte tento zdroj dat jako ER [bod integrace](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents). Aktuální implementace ER pro sestavy správy tisku bere toto nastavení v úvahu. Další podrobnosti najdete ve zdrojovém kódu souboru třídy aplikace **ERPrintMgmtDataProviderReport**. Za běhu přiřazení zdroj dat **ReportDataProvider** jako integrační bod mapování modelu nutí Finance zacházet s touto komponentou mapování s vyšší prioritou než s komponentou mapování **InvoiceProject** z konfigurace **Mapování modelu faktury projektu (RDP)**.

## <a name="see-also"></a>Viz také

- [Správa mapování modelu elektronického výkaznictví v samostatných konfiguracích elektronického výkaznictví](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [Konfigurace mapování modelu elektrického výkaznictví závislého na kontextu země](er-country-dependent-model-mapping.md)
- [Změny API rámce architektury elektronického výkaznictví](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
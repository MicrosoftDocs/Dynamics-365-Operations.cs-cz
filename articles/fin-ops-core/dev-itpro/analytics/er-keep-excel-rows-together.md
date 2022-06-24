---
title: Návrh formátu elektronického výkaznictví pro udržení řádků pohromadě na stejné stránce aplikace Excel
description: Tento článek vysvětluje, jak navrhnout formát elektronického výkaznictví (ER), který udržuje řádky pohromadě na stejné stránce Microsoft Excel.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.openlocfilehash: 98e6dd4f926908f65239f3e4f3608f9c9408f9d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854662"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Návrh formátu elektronického výkaznictví pro udržení řádků pohromadě na stejné stránce aplikace Excel

[!include [banner](../includes/banner.md)]


Tento článek vysvětluje, jak může uživatel s rolí Správce systému nebo Funkční konzultant elektronického výkaznictví konfigurovat [formát](er-overview-components.md#format-component) [elektronického vykazování (ER)](general-electronic-reporting.md) pro generování odchozích dokumentů v aplikaci Microsoft Excel a spravovat stránkování dokumentů tak, aby byly vytvořené řádky na stejné stránce.

V tomto příkladu upravíte formát ER poskytovaný společností Microsoft, který se používá k tisku faktur s volným textem v aplikaci Excel. Vaše úpravy vám umožní spravovat stránkování vygenerovaného výkazu faktur s volným textem tak, aby všechny řádky jednoho řádku faktury byly pokud možno zachovány na stejné stránce.

Postupy v tomto článku lze provést ve společnosti **USMF**. Není nutné žádné kódování.

V tomto příkladu vytvoříte požadované [konfigurace](general-electronic-reporting.md#Configuration) ER pro vzorovou společnost **Litware, Inc**. Ověřte, že je dostupný poskytovatel konfigurace ukázkové společnosti **Litware, Inc.** (`http://www.litware.com`) uveden pro rámec ER a že označen jako **Aktivní**. Není-li tento poskytovatel konfigurace uveden v seznamu nebo není-li označen jako **Aktivní**, postupujte podle kroků v tématu [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>Zadání nové volné faktury

1. Postupujte podle kroků v části [Vytvoření volné faktury](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) k přidání volné faktury.

    1. Přidejte do faktury jeden řádek.
    2. Přidejte pět poznámek na řádek faktury.

    ![Kontrola poznámek k řádkům faktury na stránce Přílohy.](./media/er-keep-excel-rows-together-notes.png)

2. Postupujte podle kroků v části [Kopírovat řádky](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) k vytvoření pěti dalších řádků faktury, které jsou kopiemi řádku faktury, který jste přidali v předchozím kroku.

    ![Kontrola řádků faktury s volným textem na stránce faktury s volným textem.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>Konfigurace rámce ER

Postupujte podle kroků uvedených v části [Konfigurace architektury ER](er-quick-start2-customize-report.md#ConfigureFramework) a nastavte minimální sadu parametrů ER. Toto nastavení musíte dokončit, než začnete používat architekturu ER k návrhu vlastní verze standardního formátu ER.

## <a name="import-the-standard-er-format-configuration"></a>Import standardní konfigurace formátu ER

Postupujte podle kroků uvedených v části [Import standardní konfigurace formátu ER](er-quick-start2-customize-report.md#ImportERSolution1) a přidejte standardní konfigurace ER do vaší aktuální instance Dynamics 365 Finance. Například importujte verzi **252.116** konfigurace formátu **Faktura s volným textem (Excel)**. Základní verze **252** základní konfigurace **Vzor faktury** se automaticky importuje z úložiště spolu s požadovanou konfigurací **Mapování modelu faktury**.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Nastavení správy tisku tak, aby používala standardní formát ER

Postupujte podle kroků v [Nastavení správy tisku](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1) ke konfiguraci správy tisku pro modul **Pohledávky** tak, aby se pro tisk faktur s volným textem používal standardní formát ER.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Nakonfigurujte cíl formátu pro standardní formát ER

Postupujte podle kroků v části [Konfigurace cíle formátu pro náhled na obrazovce](er-quick-start1-new-solution.md#ConfigureDestination) ke konfiguraci cíle ER [Obrazovka](er-destination-type-screen.md) standardního formátu ER, aby se vygenerované sestavy převedly do formátu PDF a zobrazily se náhledy na nové kartě prohlížeče.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Tisk faktury s volným textem pomocí standardního formátu ER

1. Postupujte podle kroků v části [Tisk faktury s volným textem](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) k použití standardního formátu ER k vygenerování volné textové faktury ve formátu Excel pro přidanou fakturu.
2. Stáhněte si vygenerovaný excelový sešit a prohlédněte si ho v počítačové aplikaci Excel.

    Všimněte si, že šestý řádek faktury začíná na první stránce sestavy a pokračuje na druhé stránce. Poslední poznámka se objeví na druhé stránce a není zřejmé, že patří do šestého řádku faktury. Proto konec stránky uprostřed obsahu řádku faktury ztěžuje čtení tohoto dokumentu.

    ![Kontrola stránkování vygenerované faktury s volným textem v desktopové aplikaci Excel.](./media/er-keep-excel-rows-together-invoice1.gif)

Zbývající postupy v tomto článku ukazují, jak můžete vyladit standardní formát ER, abyste zlepšili vzhled a čitelnost sestavy faktury tím, že veškerý obsah jednoho řádku faktury ponecháte na stejné stránce.

## <a name="create-a-custom-format"></a>Vytvoření vlastního formátu

Postupujte podle kroků v části [Vytvoření vlastního formátu](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) k odvození formátu z importovaného formátu ER a vytvoření konfigurace ER **Vlastní faktura s volným textem (Excel)**, která je k dispozici pro úpravy a modifikace.

## <a name="edit-the-custom-format"></a>Úprava vlastního formátu

1. Postupujte podle kroků v části [Vytvoření vlastního formátu](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) k otevření odvozeného formátu ER pro úpravy v návrháři formátů ER.
2. Na stránce **Návrhář formátu** ve stromu komponent formátu v levém podokně rozbalte komponentu **Volná faktura \> List \> InvoiceLines** a vyberte komponentu **InvoiceLines_Values**.
3. Na kartě **Formát** nastavte možnost **Udržovat řádky pohromadě** na **Ano**.

    ![Nastavení možnosti Ponechat řádky pohromadě pro upravitelný formát ER na stránce Návrhář formátů.](./media/er-keep-excel-rows-together-format.png)

4. Zvolte **Uložit** a zavřete stránku.

## <a name="mark-the-custom-format-as-runnable"></a>Označení vlastního formátu jako spustitelného

Postupujte podle kroků v části [Označení vlastního formátu jako spustitelného](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable), aby byla upravená verze vlastního formátu ER spustitelná.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Nastavení správy tisku tak, aby používala vlastní formát ER

Postupujte podle kroků v [Nastavení správy tisku](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2) ke konfiguraci správy tisku pro modul **Pohledávky** tak, aby se pro tisk faktur s volným textem používal vlastní formát ER.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Nakonfigurujte cíl formátu pro vlastní formát ER

Postupujte podle kroků v části [Konfigurace cíle formátu pro náhled na obrazovce](er-quick-start1-new-solution.md#ConfigureDestination) ke konfiguraci cíle ER **Obrazovka** vlastního formátu ER, aby se vygenerované sestavy převedly do formátu PDF a zobrazily se náhledy na nové kartě prohlížeče.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Tisk faktury s volným textem pomocí vlastního formátu ER

1. Postupujte podle kroků v části [Tisk faktury s volným textem](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) k použití vlastního formátu ER k vygenerování volné textové faktury ve formátu Excel pro přidanou fakturu.
2. Stáhněte si vygenerovaný excelový sešit a prohlédněte si ho v počítačové aplikaci Excel.

    Všimněte si, že šestý řádek faktury začíná na druhé stránce a všechny řádky Excelu, které představují tento řádek faktury, se na této stránce zobrazují společně.

    ![Kontrola aktualizovaného stránkování vygenerované faktury s volným textem v desktopové aplikaci Excel.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Další prostředky

[Návrh konfigurace pro generování dokumentů ve formátu Excel](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

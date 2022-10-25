---
title: Pravidla mapování řešení Invoice Capture
description: Tento článek poskytuje informace o nastavení pravidel mapování v řešení Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691146"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Pravidla mapování řešení Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Pravidla mapování přinášejí základní hlavní data z Microsoft Dynamics 365 Finance nebo systému plánování podnikových zdrojů (ERP). Po nastavení pravidel mapování se odvodí informace, které jsou nutné k vytvoření faktur dodavatele ve Finance. Při použití pravidel mapování zkontroluje referent závazků (AP) stav namísto ručního vyplňování všech chybějících hodnot polí.

Existují čtyři typy pravidel mapování:

- Právnická osoba
- Účet dodavatele
- Položka
- Typ výdajů

## <a name="manage-mapping-rules-by-using-the-app"></a>Spravujte pravidla mapování pomocí aplikace

Chcete-li spravovat pravidla mapování pomocí aplikace, vyberte **Nastavení**. Karta **Nastavení pravidel mapování** nabízí čtyři možnosti:

- Právnická osoba 
- Účet dodavatele 
- Mapování položek 
- Typ výdajů

Například vyberete možnost **Pravidla mapování právnických osob**. Kód právnické osoby bude identifikován pomocí názvu společnosti, adresy a daňového registračního čísla. Pro pravidlo, které je pojmenováno **LE-USPM**, pokud název společnosti obsahuje text „Contoso Robotics USA“, bude kód právnické osoby **USPM**.

Stránka zobrazuje všechna aktivní pravidla mapování. Pokud chcete zobrazit neaktivní pravidla mapování, vyberte **Aktivní pravidla mapování právnických osob** a poté vyberte **Neaktivní pravidla mapování právnických osob**.

K dispozici jsou následující akce pro pravidla mapování.

### <a name="create-a-mapping-rule"></a>Vytvoření pravidla mapování

K vytvoření pravidla mapování můžete použít dvě metody:

- Vyberte **Vové** pro vytvoření nového pravidla mapování. Poté zadejte informace o pravidlu mapován. Hodnota **Název pravidla** by měla být jedinečná pro každý typ pravidla mapování.
- Pokud vyberete existující pravidlo mapování, zpřístupní se tlačíto **Kopírovat**. Vyberte jej a pak v dialogovém okně, které se zobrazí, vyberte **OK**. Pravidlo mapování se vytvoří duplikováním vybraného pravidla.

### <a name="edit-a-mapping-rule"></a>Úprava pravidla mapování

Chcete-li upravit pravidlo mapování, vyberte pole a změňte hodnotu.

### <a name="activatedeactivate-mapping-rules"></a>Aktivovat/deaktivovat pravidla mapování

Chcete-li deaktivovat jedno nebo více pravidel mapování, vyberte je na stránce **Aktivní pravidla mapování** a poté vyberte **Deaktivovat**. Pravidla jsou přesunuta ze stránky **Aktivní pravidla mapování** na stránku **Neaktivní pravidla mapování**.

Stejným způsobem, chcete-li aktivovat pravidla mapování, vyberte je na stránce **Neaktivní pravidla mapování** a poté vyberte **Aktivovat**.

### <a name="remove-mapping-rules"></a>Odebrat pravidla mapování

Chcete-li odebrat pravidla mapování, vyberte je a pak vyberte **Odstranit**.

### <a name="check-for-conflicts"></a>Zkontrolovat konflikty

Pokud mají dvě pravidla mapování stejné hodnoty **Právnická osoba** a **Účet dodavatele**, ale jiné hodnoty **Název položky**, bude detekován konflikt a pravidlo mapování nebude vytvořeno ani aktualizováno.

## <a name="importexport-mapping-rules-from-excel"></a>Import/export pravidel mapování z Excelu

Ke správě pravidel v dávce lze použít doplněk aplikace Excel. Existují tyto možnosti:

- Stáhnout excelovou šablonu.
- Export do aplikace Excel.
- Import z aplikace Excel.

### <a name="download-an-excel-template"></a>Stáhnout excelovou šablonu

Chcete-li stáhnout šablonu Excel, vyberte **Stáhnout šablonu**. Pak vyberte pole, která se mají zahrnou do šablony.

### <a name="export-to-excel"></a>Export do aplikace Excel

Exportovat můžete dvěma způsoby:

- Vyberte **Otevřít v Excelu Online** k otevření souboru v Excelu. Poté můžete upravit soubor online. Po dokončení zvolte **Uložit**. Všechny vaše změny budou uloženy na stránce **Pravidlo mapování**.
- Vyberte **Stáhnout list**, chcete-li stáhnout soubor Excel, který obsahuje pravidla mapování. Poté můžete upravit soubor. Až budete hotovi, vyberte **Import z Excelu** pro nahrání aktualizovaného listu.

### <a name="import-from-excel"></a>Import z aplikace Excel

1. Vyberte **Import z Excelu** pro import dat z XLSX souboru. Můžete také importovat z hodnot oddělených čárkami (CSV) nebo souborů XML. Před importem byste se měli rozhodnout, zda jsou povoleny duplikáty.
2. Vyberte **Zkontrolovat mapování**, chcete-li zkontrolovat mapování atributů a určit, zda je správné. Vztah mapování lze upravovat.
3. Po dokončení vyberte **Dokončit Importovat** ke spuštění importu.
4. Můžete vybrat **Sledovat proces** a sledovat průběh importu.

    Stav importu je aktualizován z **Dokončit** na **Analýza**, pak na **Transformace** a nakonec na **Dokončeno**.

Po dokončení procesu importu se zobrazí statistika úspěšnosti, dílčích selhání, chyb a celkového počtu zpracování.

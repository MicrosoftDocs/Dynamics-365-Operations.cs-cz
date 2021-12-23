---
title: Import a export výpočtu daní
description: Toto téma poskytuje informace o funkci importu a exportu služby pro výpočet daně.
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 76ea99510455e984d94a93d87ee788fdcf00c376
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891305"
---
# <a name="import-and-export-tax-calculations"></a>Import a export výpočtu daní

Toto téma poskytuje informace o funkci importu a exportu služby pro výpočet daně. Tato funkce pomáhá zajistit flexibilní a efektivní prostředí konfigurace.

## <a name="import-and-export-tax-codes"></a>Import a export daňových kódů

### <a name="export-templates"></a>Export šablon

1. Přihlaste se ke službě [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/).
2. V pracovním prostoru **Funkce globalizace** vyberte **Funkce** a poté vyberte dlaždici **Výpočet daně**.
3. Vyberte stávající funkci nebo [vytvořte novou funkci](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. V mřížce **Verze** vyberte **Upravit**.
5. Na stránce funkce **Výpočet daně** nastavte [verzi konfigurace](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Na kartě **Daňové kódy** vyberte **Import**.
7. Volbou **Exportovat šablonu daňového kódu** stáhněte soubor **TaxCodesTemplate.zip**.
8. Rozbalte soubor **TaxCodesTemplate.zip**. Šablony daňových kódů jsou komprimovány samostatně podle hodnoty **Původ výpočtu**.
9. Rozbalte soubor **By Net Amount.zip**, který obsahuje následující soubory s hodnotami oddělenými čárkami (CSV):

    - **TaxCode.csv** – Zadejte daňové kódy.
    - **TaxLimit.csv** – Zadejte daňová omezení pro každý daňový kód.
    - **TaxRate.csv** – Zadejte daňové sazby pro každý daňový kód.

> [!NOTE]
> Ve výchozím nastavení jsou položky pro **vzorový** daňový kód k dispozici v šablonách. Pokud **vzorový** daňový kód nebude ze souborů CSV odstraněn, bude importován do funkce.

### <a name="import-tax-codes"></a>Import daňových kódů

Pro import **ukázkového** daňového kódu v šabloně do funkce výpočtu daně postupujte následovně.

1. V RCS na stránce funkce **Výpočet daně** na kartě **Daňové kódy** vyberte **Import**.
2. Vyberte **Procházet**, vyhledejte a vyberte soubor **TaxCode.csv** a poté v poli **Cílová tabulka** vyberte **Daňový kód**.
3. Kliknutím na tlačítko **OK** importujte daňový kód.
4. Vyhledejte a vyberte soubor **TaxRate.csv** a poté v poli **Cílová tabulka** vyberte **Daňová sazba**.
5. Kliknutím na tlačítko **OK** importujte daňovou sazbu.
6. Vyhledejte a vyberte soubor **TaxLimit.csv** a poté v poli **Cílová tabulka** vyberte **Daňové omezení**.
7. Kliknutím na tlačítko **OK** importujte daňové omezení.

Můžete také přímo importovat soubor zip, který obsahuje všechny tři soubory CSV. Tímto způsobem můžete rychle a snadno provést import.

1. V RCS na stránce funkce **Výpočet daně** na kartě **Daňové kódy** vyberte **Import**.
2. Vyberte **Procházet**, vyhledejte a vyberte soubor **By Net Amount.zip** a poté vyberte **OK**.

### <a name="export-tax-codes"></a>Export daňových kódů

1. V RCS na stránce funkce **Výpočet daně** na kartě **Daňové kódy** vyberte **Export**.

    Tlačítko **Export** je dostupné, když je v poli alespoň jeden daňový kód v mřížce **Daňové kódy**.

2. Tlačítkem **OK** exportujte všechny daňové kódy funkce v souboru zip.

> [!NOTE]
> Použijte exportovaný soubor jako šablonu pro import daňových kódů do odpovídající funkce.

## <a name="import-and-export-applicability-rules"></a>Import a export pravidel použitelnosti

### <a name="export-applicability-rules"></a>Export pravidel použitelnosti

1. Přihlaste se do [RCS](https://marketing.configure.global.dynamics.com/).
2. V pracovním prostoru **Funkce globalizace** vyberte **Funkce** a poté vyberte dlaždici **Výpočet daně**.
3. Vyberte stávající funkci nebo [vytvořte novou funkci](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. V mřížce **Verze** vyberte **Upravit**.
5. Na stránce funkce **Výpočet daně** nastavte [verzi konfigurace](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Na kartě **Použitelnost daňové skupiny** vyberte řádky v mřížce **Nastavení použitelnosti daňové skupiny**.
7. Vyberte tlačítko **Otevřít v Microsoft Office** a poté vyberte **Dynamická matice použitelnosti daňové služby**.

    [![Export pravidel použitelnosti do Microsoft Excel na stránce funkce Výpočet daně.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Volbou **Stáhnout** exportujte vybrané řádky do listu Microsoft Excel.

### <a name="import-applicability-rules"></a>Import pravidel použitelnosti

List aplikace Excel, který jste si stáhli, obsahuje strukturu mřížky **Nastavení použitelnosti daňové skupiny**. Nová pravidla můžete přidat přímo v listu. Po dokončení postupujte dle následujících kroků, abyste importovali nová pravidla zpět do mřížky **Nastavení použitelnost daňové skupiny**.

1. V listu aplikace Excel vyberte a zkopírujte řádky, které chcete importovat.
2. V RCS na stránce funkce **Výpočet daně** na kartě **Použitelnost daňové skupiny** volbou **Přidat** vložte prázdný záznam do spodu mřížky **Nastavení použitelnosti daňové skupiny**.
3. Kombinací kláves **Ctrl+V** vložte zkopírované řádky do mřížky.
4. Zvolte možnost **Uložit**.

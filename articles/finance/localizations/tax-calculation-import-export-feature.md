---
title: Import a export výpočtu daní
description: Tento článek poskytuje informace o funkci importu a exportu služby pro výpočet daně.
author: Kai-Cloud
ms.date: 10/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8666d4971e36279ebd2b1396de7cab37680980e6
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690226"
---
# <a name="import-and-export-tax-calculations"></a>Import a export výpočtu daní

Tento článek poskytuje informace o funkci importu a exportu služby pro výpočet daně. Tato funkce pomáhá zajistit flexibilní a efektivní prostředí konfigurace.

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

## <a name="import-feature-demo-data"></a>Importujte ukázková data funkcí

Chcete-li importovat ukázková data funkcí, postupujte takto.

1. Přihlaste se do [RCS](https://marketing.configure.global.dynamics.com/).
2. V pracovním prostoru **Funkce globalizace** vyberte **Funkce** a poté vyberte dlaždici **Výpočet daně**.
3. Vyberte **Import** a poté na stránce **Importujte funkci z globálního úložiště** vyberte **Synchronizovat**. 
4. V tabulce vyberte funi **tax-calculation-feature-demo-data** a poté vyberte **Import**.
5. Vyberte **Zobrazení** pro kontrolu daňových kódů, skupin a pravidel použitelnosti, které jsou definovány v importované funkci.
6. Ve Finance přepněte na **DEMF** a pak přejděte na **Daň** \> **Nastavení** \> **Konfigurace daně** \> **Parametry výpočtu daně**.
7. Na kartě **Obecné** vyberte **Povolit službu výpočtu daně**.
8. V poli **Název nastavení funkce** vyberte **tax-calculation-feature-demo-data**.
9. Vyberte **Vypořádací období** a **Skupina zaúčtování hl. knihy** pro nové ukázkové daňové kódy a poté vyberte **Potvrdit**.
10. Zvolte možnost **Uložit**.

> [!NOTE]
> Demo funkce **tax-calculation-feature-demo-data** je založena na verzi funkce **40.54.234** a určená pro ukázkovou právnickou osobu **DEMF**. Ujistěte se, že Finance a RCS jsou upgradovány na verzi 10.0.26 nebo novější.

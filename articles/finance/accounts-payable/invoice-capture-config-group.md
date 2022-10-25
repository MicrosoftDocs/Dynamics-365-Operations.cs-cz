---
title: Skupiny konfigurace řešení Invoice Capture
description: Tento článek poskytuje obecné informace o konfiguračních skupinách v řešení Invoice Capture.
author: sunfzam
ms.date: 09/28/2022
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
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691142"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Skupiny konfigurace řešení Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Uživatelé mohou spravovat seznam polí faktur a nastavení ruční kontroly pro právnické osoby pomocí konfiguračních skupin. Uživatelé mohou nastavit konfigurace faktur pro různé právnické osoby ve skupinách. Všechny právnické osoby ve stejné konfigurační skupině používají stejná pole faktury a nastavení ruční kontroly.

## <a name="manage-configuration-groups"></a>Spravovat konfigurační skupiny

Chcete-li spravovat konfigurační skupiny pomocí aplikace, přejděte na **Nastavení** a poté vyberte **Nastavení systému \> Definujte komponentu konfiguračních skupin**.

Na nstránce **Definujte konfigurační skupiny** hlavní záložka zobrazuje seznam konfiguračních skupin, které byly definovány. Zobrazuje také výchozí konfigurační skupinu. Pro každou konfigurační skupinu jsou k dispozici následující akce:

- **Zkopírujte konfigurační skupinu** – Novou konfigurační skupinu můžete vytvořit duplikováním existující skupiny. Nová skupina má stejné hodnoty jako původní skupina pro všechna pole kromě **Název skupiny** a **Popis skupiny**. Po zduplikování konfigurační skupiny vyberte **OK**.
- **Odstranit konfigurační skupiny** – Chcete-li odstranit konfigurační skupinu, vyberte ji a poté vyberte **Odstranit**.

    > [!NOTE]
    > Výchozí konfigurační skupinu nelze odstranit.

- **Upravit ID konfigurační skupiny** – Chcete-li upravit ID konfigurační skupiny, vyberte pole **ID skupiny** a aktualizujte hodnotu. ID skupiny by nemělo obsahovat mezery ani speciální znaky a nemělo by přesáhnout 20 znaků.

    > [!NOTE]
    > Hodnota pole **ID skupiny** lze aktualizovat pouze jednou.

- **Upravit popis konfigurační skupiny** – Chcete-li upravit popis konfigurační skupiny, vyberte pole **Popis** a aktualizujte hodnotu.
- **Změnit nastavení ruční kontroly** – Uživatelé se mohou rozhodnout, zda musí být faktura zkontrolována ručně. Chcete-li změnit nastavení ruční kontroly, vyberte možnost **Potřebuje ruční kontrolu**. Existují tyto možnosti:

    - **Vždy ruční kontrola** – Tuto možnost vyberte, pokud faktury v konfigurační skupině vždy vyžadují ruční kontrolu.
    - **Pro chyby a varování** – Tuto možnost vyberte, pokud faktury, které obsahují chybové zprávy nebo varovné zprávy, vyžadují ruční kontrolu.
    - **Pro chyby** – Tuto možnost vyberte, pokud faktury, které obsahují chybové zprávy, vyžadují ruční kontrolu.

- **Změňte nastavení skóre spolehlivosti** – Skóre spolehlivosti jsou metadata, která řešení pro zachycení faktur poskytuje k vykazování přesnosti rozpoznaných fakturačních údajů. Čím vyšší je skóre, tím přesnější mohou být rozpoznaná data. Konfigurace umožňuje uživatelům definovat, kdy je vyžadována ruční kontrola, na základě skóre spolehlivosti. Uživatelé mohou změnit práh skóre spolehlivosti pro faktury. Chcete-li aktualizovat nastavení skóre spolehlivosti, vyberte pole **Skóre důvěry** a aktualizujte hodnotu.

    Pro skóre spolehlivosti existují dva typy upozornění:

    - **Varování** – Pole faktury, která mají skóre spolehlivosti nad prahem varování, jsou považována za správná. Varovný práh musí být vyšší než práh chyby a menší než 100.
    - **Chyba** – Pole faktury, která mají skóre spolehlivosti pod prahem chyb, jsou považována za selhaná. Uživateli se zobrazí chybové zprávy. Práh musí chyb musí být vyšší než 0 a nižší než práh varování. Varovné zprávy se zobrazí pro pole faktury, která mají skóre spolehlivosti mezi prahem varování a prahem chyby.

- **Správa polí faktury** – Uživatelé mohou spravovat seznam polí faktur, který se zobrazuje v prohlížeči vedle sebe. Na kartě **Správa fakturačních polí** vyberte symbol ozubeného kola, vyberte pole faktury, která chcete přidat, a poté vyberte **Uložit**. Vybraná pole budou přidána do seznamu. Chcete-li odebrat pole faktury ze seznamu, vyberte **Odstranit** na poli.

### <a name="manage-file-filters-optional"></a>Správa filtrů souborů (volitelné)

Správa filtrů souborů umožňuje uživatelům definovat další filtry pro soubory příchozích faktur. Soubory, které nesplňují kritéria filtru, budou přijaty a zobrazí se v seznamu **Přijaté soubory**, ale zobrazí chyby ověření souboru. Toto chování se liší od chování pro filtry, které jsou definovány v kanálu. U těchto filtrů nebudou soubory, které nesplňují kritéria, přijaty vůbec. Uživatelé mohou zkontrolovat příchozí soubory a rozhodnout, zda je každý soubor neplatnou fakturou, a mohou soubor zastarat nebo jej ručně zahrnout pro rozpoznání a zahrnutí do zachycených faktur.

Když je nainstalováno řešení pro zachycení faktur, je definován výchozí filtr souborů. Tento filtr souborů je globální. Pokud chcete jiná nastavení filtru, můžete aktualizovat výchozí filtr. Pokud je pole povinné, vyberte **Požadované**. 

### <a name="accepted-file-size"></a>Přijatá velikost souboru

Můžete si vybrat přijímanou velikost souboru.

> [!NOTE]
> Soubory větší než 20 480 kilobajtů (KB) nejsou podporovány.

### <a name="supported-file-types"></a>Podporované typy souborů

V současné době jsou podporovány následující typy souborů:

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF

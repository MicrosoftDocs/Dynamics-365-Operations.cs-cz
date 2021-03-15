---
title: Sestava úložiště hodnot zásob
description: V tomto tématu je vysvětleno, jak spustit sestavu úložiště hodnot zásob a zpřístupnit výstup digitálně, a to buď jako interaktivní stránku v Microsoft Dynamics 365 Supply Chain Management nebo jako exportovaný dokument v některém z několika formátů.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0f54c02fc828d60f4ddb28be932bbf8eb137ee92
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008148"
---
# <a name="inventory-value-storage-report"></a>Sestava úložiště hodnot zásob

V tomto tématu je vysvětleno, jak spustit sestavu **Úložiště hodnot zásob** a zpřístupnit výstup digitálně, a to buď jako interaktivní stránku v Microsoft Dynamics 365 Supply Chain Management nebo jako exportovaný dokument v některém z několika formátů.

Pokud zobrazíte sestavu ve svém prohlížeči, sloupce a agregované zůstatky jsou v závislosti na vámi konfigurovaném rozvržení dynamicky upravovány. Výsledky můžete řadit, filtrovat, přecházet k podrobnostem atd.

Výsledky sestavy se ukládají do datové entity data **Hodnota zásob**. Z tohoto důvodu můžete výsledky filtrovat a exportovat do formátu CSV nebo Microsoft Excel.

Sestava **Úložiště hodnot zásob** je užitečná, pokud výstup obsahuje mnoho řádků. Máte například 50 000 položek a 300 úložišť bylo vytvořeno jako sklady. V takovém případě, pokud vyžádáte konečné zůstatky zásob podle zboží, pracoviště a skladu, bude výstup obsahovat mnoho řádků.

> [!NOTE]
> V sestavě nebudou zahrnuty mezisoučty definované v jejím rozvržení. Nezahrne také zůstatky hlavní knihy, i když jsou definovány v rozvržení sestavy. Odsouhlasení do hlavní knihy je nutné provést pomocí předvah.

## <a name="turn-on-the-inventory-value-storage-feature"></a>Zapnutí funkce úložiště hodnot zásob

Dříve než budete moci vygenerovat sestavu **Úložiště hodnoty zásob**, je nutné zapnout funkci ve vašem systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul** – správa nákladů
- **Název funkce** – úložiště hodnot zásob

## <a name="generate-an-inventory-value-storage-report"></a>Generování sestavy úložiště hodnot zásob

Chcete-li vytvořit a uložit sestavu **Úložiště hodnot zásob**, postupujte takto.

1. Přejděte na **Správa zásob \> Dotazy a sestavy \> Úložiště sestavy hodnot zásob**.
1. Zvolte **Nové**.
1. V dialogovém okně **Hodnota zásob**, které se zobrazí, nastavte následující hodnoty, které definují, které záznamy budou zahrnuty do sestavy:

    - Na záložce s náhledem **Parametry** zadejte jedinečný název sestavy a pomocí polí v části **Časový interval** definujte, které záznamy budou do sestavy zahrnuty. Chcete-li definovat časový interval, můžete buď vybrat přednastavený rozsah (relativně k datu generování sestavy) v poli **Kód časového intervalu**, nebo vybrat konkrétní data v polích **Od data** a **Do data**.
    - Na pevné záložce **Záznamy, které mají být zahrnuty** nastavte filtry a omezení, která definují, která data mají být do sestavy zahrnuta.
    - N záložce s náhledem **Spustit na pozadí** určete, kdy a jak často bude sestava generována.

    > [!NOTE]
    > Tato sestava se vždy spustí jako součást dávkové úlohy.

1. Vyberte **OK**, pokud chcete použít své nastavení a zavřete dialogové okno.

Po dokončení dávkové úlohy se sestava zobrazí na stránce **Úložiště sestavy hodnot zásob**. Možná bude nutné pro zobrazení sestavy aktualizovat stránku.

## <a name="explore-an-inventory-value-storage-report"></a>Prozkoumání sestavy úložiště hodnot zásob

Po vygenerování sestavy ji můžete kdykoli zobrazit a prozkoumat následujícím způsobem.

1. Přejděte na **Správa zásob \> Dotazy a sestavy \> Úložiště sestavy hodnot zásob**.
1. V seznamu vyberte sestavu.
1. Chcete-li zobrazit obsah sestavy, vyberte možnost **Zobrazit podrobnosti**.
1. Prozkoumejte sestavu pomocí některého z následujících kroků:

    - Stejně jako u většiny standardních formulářů v Supply Chain Management můžete vybrat téměř libovolné záhlaví sloupce, podle jehož hodnot chcete seřadit nebo filtrovat mřížku.
    - Pro filtrování sestavy podle libovolné hodnoty v několika dostupných sloupcích vyberte pole **Filtr**.
    - Pomocí nabídky Zobrazení (nad polem **Filtr**) uložte a načtěte oblíbené kombinace možností řazení a filtrování.

## <a name="export-an-inventory-value-storage-report"></a>Export sestavy úložiště hodnot zásob

Každá generovaná sestava je uložena v datové entitě **Hodnota zásob**. Pomocí standardních funkcí Supply Chain Management můžete exportovat data z této entity do libovolného podporovaného formátu dat, včetně formátu CSV nebo Excel.

Následující příklad ukazuje, jak exportovat sestavu **Hodnota zásob**.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa dat**.
1. V oddílu **Import/export** vyberte dlaždici **Export**. 
1. Na stránce **Export**, která se zobrazí, nastavte úlohu exportu. Nejprve zadejte název skupiny dané úlohy.
1. V části **Vybrané entity** vyberte **Přidat entitu**.
1. V zobrazeném dialogovém okně nastavte následující pole:

    - **Název entity** – vyberte **Hodnota zásob**.
    - **Formát cílových dat** – vyberte formát, do kterého mají být exportována data.

1. Volbou **Přidat** přidejte nový řádek a volbou **Zavřít** zavřete dialogové okno.
1. Obvykle se exportuje vždy jedna sestava. Při exportu jedné sestavy nastavte filtr pro řádek, který jste právě přidali do dialogového okna **Dotaz**. Tímto způsobem můžete definovat, která sestava z entity **Hodnota zásob** bude zahrnuta do exportu. Pomocí těchto kroků nastavíte následující možnosti filtru pro export jedné sestavy:

    1. Na kartě **Rozsah** vyberte možnost **Přidat** a přidejte řádek.
    2. Pole **Tabulka** nastavte na **Hodnota zásob**.
    3. Pole **Odvozená tabulka** nastavte na **Hodnota zásob**.
    4. Pole **Pole** nastavte na pole, podle kterého chcete filtrovat. Obvykle použijete pole **Název spuštění** nebo **Čas spuštění**.
    5. Ve vybraném poli nastavte pole **Kritéria** na hodnotu, kterou chcete vyhledat. (Pokud jste v předchozím kroku vybrali pole **Název spuštění**, tato hodnota bude názvem sestavy. Pokud jste vybrali pole **Čas spuštění**, názvem bude čas, kdy byla sestava vygenerována.)
    6. V případě potřeby přidejte na kartu **Rozsah** další řádky, dokud neidentifikujete jedinečnou sestavu, kterou hledáte.

1. Volbou **OK** uložte svá nastavení a zavřete dialogové okno.
1. Nastavení exportu uložíte výběrem možnosti **Uložit**.
1. Na kartě **Možnosti exportu** volbou **Exportovat nyní** vygenerujte exportovaný soubor.
1. Na otevřené stránce **Souhrn spuštění** můžete zobrazit stav úlohy exportu a seznam exportovaných entit. V části **Stav zpracování entity** vyberte v seznamu entitu **Hodnota zásob** a poté volbou **Stáhnout soubor** stáhněte data, který byla exportována z této entity.

Další informace o tom, jak používat správu dat k exportu dat, naleznete v tématu [Přehled úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
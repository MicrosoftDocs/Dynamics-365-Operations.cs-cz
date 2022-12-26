---
title: Finanční konsolidace online
description: Tento článek popisuje online finanční konsolidace v hlavní knize.
author: aprilolson
ms.date: 12/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 5843ac78adf32e738d9882c7f4e9e04a79200700
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838249"
---
# <a name="online-financial-consolidations"></a>Finanční konsolidace online

[!include [banner](../includes/banner.md)]

Tento článek popisuje online finanční konsolidace v hlavní knize. Než si přečtete tento článek, seznamte se s článkem [Přehled finančních konsolidací a převodu měny](financial-consolidations-currency-translation.md).

Po dokončení nastavení zadejte podrobnosti konsolidace na stránce **Konsolidace [Online]**. Po dokončení můžete kliknout na **OK** nebo **Dávka** pro zpracování konsolidace.

## <a name="criteria"></a>Kritéria
Na kartě **Kritéria** na stránce **Konsolidace [Online]** definujete účty, období a typ dat, která jsou konsolidována.

![Karta Kritéria.](./media/criteria-consolidate-online.png "Karta Kritéria")

Zde je vysvětlení různých polí na této kartě:

- **Popis** – Zadejte přesný popis pro období, které konsolidujete.
- **Hlavní účet** – Použijte pole v této části definování hlavních účtů, které budou zpracovány.

    - **Od** a **Do** – Určete rozsah účtů, které chcete zpracovat. Ponecháte-li tato pole prázdná, budou všechny účty ze všech společností přesunuty do konsolidované společnosti. Proto při konsolidaci čtyř společností, když má každá společnost jinou účtovou osnovy, všechny účty ze všech čtyř společností budou vytvořeny v konsolidační společnosti.
    - **Použít konsolidační účet** – Když nastavíte tuto možnost na hodnotu **Ano**, pole **Vybrat konsolidační účet z** bude k dispozici. V tomto poli vyberte, zda mají být konsolidovány všechny účty na konsolidační účet, který je nastaven na stránce **Hlavní účty**, nebo zda chcete vybrat účet z jedné ze skupin konsolidačních účtů.
    - **Skupina konsolidačních účtů** – Vyberte skupinu, kterou chcete použít pro mapování hlavního účtu pro konsolidaci.

- **Období konsolidace** – Použijte pole v této části k definování období konsolidace.

    - **Od** a **Do** – Určete rozmezí dat pro konsolidaci. Ponecháte-li tato pole prázdná, konsolidace bude zpracována za všechna období, která jsou definována v kalendáři hlavní knihy společnosti. Nedoporučujeme ponechat tato pole prázdná.
    - **Vybrat konsolidační částku z** – Toto pole použijte k určení, zda se k aktualizaci částek zúčtovací měny konsolidační společnosti použijí částky zúčtovací měny nebo částky měny vykazování ze zdrojových společností.

        - Volbou **Zúčtovací měna** použijete částky zúčtovací měny ze zdrojových společností k aktualizaci částek zúčtovací měny v konsolidační společnosti. Když je tato hodnota vybrána, použijte pole **Konsolidace zúčtovací měny** k definování způsobu výpočtu zúčtovacích měn v konsolidační společnosti.
        - Volbou **Měna vykazování** použijete částky měny vykazování ze zdrojových společností k výpočtu částek zúčtovací měny v konsolidační společnosti.

            - Pokud je měna vykazování ze zdrojové společnosti stejná jako zúčtovací měna konsolidační společnosti, částky měny vykazování se zkopírují ze zdrojové společnosti do konsolidační společnosti.
            - Pokud se měna vykazování ze zdrojové společnosti liší od zúčtovací měny konsolidační společnosti, hodnoty se převedou pomocí informací o směně, které jsou definovány na kartě **Převod měn** této stránku pro výpočet konsolidačních hodnot společnosti.

    - **Konsolidace zúčtovací měny** – Toto pole je dostupné pouze v případě, že pole **Vybrat konsolidační částku z** je nastaveno na **Zúčtovací měna**. Použijte jej k určení, zda jsou částky zúčtovací měny ze zdrojových společností převáděny prostřednictvím směnných kurzů nebo zkopírovány do konsolidační společnosti. Vyberte **Použít převod měny**, chcete-li k výpočtu zůstatků konsolidačního účetnictví použít informace o směnném kurzu definované na kartě **Převod měn**. Vyberte **Použít částku v zúčtovací měně**, chcete-li zkopírovat částky zúčtovací měny ze zdrojových společností do konsolidační společnosti.

        - Pokud je zúčtovací měna ze zdrojové společnosti stejná jako zúčtovací měna konsolidační společnosti, částky měny se zkopírují ze zdrojové společnosti do konsolidační společnosti.
        - Pokud se zúčtovací měna ze zdrojové společnosti liší od zúčtovací měny konsolidační společnosti, hodnoty se převedou pomocí informací o směně, které jsou definovány na kartě **Převod měn** pro výpočet konsolidačních hodnot společnosti.

    - **Zahrnout skutečné částky** – Nastavte tuto možnost na **Ano** pro konsolidaci vašich skutečných dat.
    - **Zahrnout rozpočtové částky** – Nastavte tuto možnost na **Ano** pro konsolidaci dat z registru rozpočtu.
    - **Znovu vytvořit zůstatky během procesu konsolidace** – Nedoporučujeme nastavit tuto možnost na **Ano**. Místo toho znovu sestavte zůstatky jako samostatnou dávkovou úlohu.

- **Rozpočtové modely** – Pokud jste vybrali konsolidaci dat rozpočtu, použijte pole v této části k definování rozpočtových modelů.

    - **Od** a **Do** – Určete rozsah modelů, které chcete použít.
    - **Typ rozpočtové sazby** – Vyberte typ rozpočtové sazby, kterou chcete použít pro převod měny dat rozpočtu.

## <a name="financial-dimensions"></a>Finanční dimenze
Na kartě **Finanční dimenze** definujete dimenze, které mají být zahrnuty v konsolidační společnosti. Chcete-li vybrat dimenze, nastavte pole **Specifikace** na **dimenze** a pak definujte pořadí dimenze v konsolidační společnosti.

![Karta Finanční dimenze.](./media/financial-dimensions-cons.png "Karta Finanční dimenze")

Bez ohledu na pořadí, které definujete, bude **Hlavní účet** vždy prvním segmentem.

## <a name="legal-entities"></a>Právnické osoby
Na kartě **Právnické osoby** definujete společnosti, které mají být zahrnuty v konsolidační společnosti. Můžete také definovat procento vlastnictví těchto společností. Zadáte-li nižší než 100% vlastnictví, zadané procento bude zahrnuto do konsolidační společnosti. Pro všechny rozdíly převodu se použije pole **Typ účtu pro rozdíly převodu** k výběru hlavního účtu z nastavení na stránce **Účty pro automatické transakce**.

![Karta Právnické osoby.](./media/legal-entities-cons.png "Karta Právnické osoby")

![Stránka Účty pro automatické transakce.](./media/accounts-for-automatic-cons.png "Stránka Účty pro automatické transakce")

## <a name="elimination"></a>Eliminace
Na kartě **Eliminace** máte tři možnosti pro zpracování eliminací:

- Vyberte pravidlo eliminace a poté v poli **Možnosti návrhu** vyberte **Pouze návrh**. Tato možnost zpracuje eliminaci během procesu konsolidace, ale nezaúčtuje vše v jednom kroku. Zaúčtovat deník můžete později.
- Vyberte pravidlo eliminace a poté v poli **Možnosti návrhu** vyberte **Pouze zaúčtovat**. Tato možnost zpracuje eliminaci během procesu konsolidace a zaúčtuje vše v jednom kroku.
- Spusťte návrh eliminace odděleně od procesu konsolidace pomocí deníku eliminace.

![Karta Eliminace.](./media/elimination-cons-onl.png "Karta Eliminace")

Další informace o eliminacích naleznete v tématu [Pravidla eliminace](./elimination-rules.md).

## <a name="currency-translation"></a>Převod měny
Na kartě **Převod měny** definujete právnickou osobu, účet a typ směnného kurzu a sazbu. Je-li konsolidační společnost přiřazena k jiným hlavním účtům než zdrojová společnost, musí být hlavní účet konsolidační společnosti uveden v polích **Od data** a **Do data**, nikoli hlavní účty zdrojové společnosti. Pro každý řádek právnické osoby a hlavních účtů jsou v poli **Použít směnný kurz z** k dispozici tři možnosti:

- **Datum konsolidace** – Datum, které je definováno v poli **Do data období konsolidace** na kartě **Kritéria** pro konsolidaci se použije k získání směnného kurzu. Tento kurz je ekvivalentem místního kurzu nebo kurzu na konci měsíce. Zobrazí se náhled kurzu, ale nelze ho upravovat.
- **Datum transakce** – Datum každé transakce se použije k výběru směnného kurzu. Tato možnost se nejčastěji používá pro dlouhodobý majetek a obvykle se označuje jako historický kurz. Nelze zobrazit náhled kurzu, protože existuje mnoho kurzů pro různé transakce v rozsahu účtu.
- **Sazba definovaná uživatelem** – Když vyberete tuto možnost, můžete zadat směnný kurz, který chcete. Tato možnost může být užitečná pro průměrné směnné kurzy, nebo pokud konsolidujete proti pevnému směnnému kurzu.

![Karta Převod měny.](./media/currency-translation-cons-online.png "Karta Převod měny")

## <a name="additional-resources"></a>Další prostředky

Další informace o konsolidaci a převodech měn naleznete v nadřazeném článku [Přehled finanční konsolidace a převodu měny](./financial-consolidations-currency-translation.md).

Další informace o scénářích, kde můžete vygenerovat konsolidační finanční výkazy naleznete v tématu [Generování konsolidovaných finančních výkazů](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

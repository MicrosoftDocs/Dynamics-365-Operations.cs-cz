---
title: Finanční konsolidace online
description: Toto téma popisuje online finanční konsolidace v hlavní knize.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: fd29dc5f932c9cd274a42923e1ff659dd5d8e9d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "341251"
---
# <a name="consolidate-online"></a>Konsolidovat online

[!include [banner](../includes/banner.md)]

Toto téma popisuje online finanční konsolidace v hlavní knize. Než si přečtete toto téma, seznamte se s tématem [Finanční konsolidace a převod měny](financial-consolidations-currency-translation.md).

Po dokončení nastavení zadejte podrobnosti konsolidace na stránce **Konsolidace [Online]**. Po dokončení můžete kliknout na **OK** nebo **Dávka** pro zpracování konsolidace.

## <a name="criteria"></a>Kritéria
Na kartě **Kritéria** na stránce **Konsolidace [Online]** definujete účty, období a typ dat, která jsou konsolidována.

![Karta Kritéria](./media/criteria-consolidate-online.png "Karta kritéria")

Zde je vysvětlení různých polí na této kartě:

- **Popis** – Zadejte přesný popis pro období, které konsolidujete.
- **Hlavní účet** – Použijte pole v této části definování hlavních účtů, které budou zpracovány.

    - **Od** a **Do** – Určete rozsah účtů, které chcete zpracovat. Ponecháte-li tato pole prázdná, budou všechny účty ze všech společností přesunuty do konsolidované společnosti. Proto při konsolidaci čtyř společností, když má každá společnost jinou účtovou osnovy, všechny účty ze všech čtyř společností budou vytvořeny v konsolidační společnosti.
    - **Použít konsolidační účet** – Když nastavíte tuto možnost na hodnotu **Ano**, pole **Vybrat konsolidační účet z** bude k dispozici. V tomto poli vyberte, zda mají být konsolidovány všechny účty na konsolidační účet, který je nastaven na stránce **Hlavní účty**, nebo zda chcete vybrat účet z jedné ze skupin konsolidačních účtů.
    - **Skupina konsolidačních účtů** – Vyberte skupinu, kterou chcete použít pro mapování hlavního účtu pro konsolidaci.

- **Období konsolidace** – Použijte pole v této části k definování období konsolidace.

    - **Od** a **Do** – Určete rozmezí dat pro konsolidaci. Ponecháte-li tato pole prázdná, konsolidace bude zpracována za všechna období, která jsou definována v kalendáři hlavní knihy společnosti. Nedoporučujeme ponechat tato pole prázdná.
    - **Zahrnout skutečné částky** – Nastavte tuto možnost na **Ano** pro konsolidaci vašich skutečných dat.
    - **Zahrnout rozpočtové částky** – Nastavte tuto možnost na **Ano** pro konsolidaci dat z registru rozpočtu.
    - **Znovu vytvořit zůstatky během procesu konsolidace** – Nedoporučujeme nastavit tuto možnost na **Ano**. Místo toho znovu sestavte zůstatky jako samostatnou dávkovou úlohu.

- **Rozpočtové modely** – Pokud jste vybrali konsolidaci dat rozpočtu, použijte pole v této části k definování rozpočtových modelů.

    - **Od** a **Do** – Určete rozsah modelů, které chcete použít.
    - **Typ rozpočtové sazby** – Vyberte typ rozpočtové sazby, kterou chcete použít pro převod měny dat rozpočtu.

## <a name="financial-dimensions"></a>Finanční dimenze
Na kartě **Finanční dimenze** definujete dimenze, které mají být zahrnuty v konsolidační společnosti. Chcete-li vybrat dimenze, nastavte pole **Specifikace** na **dimenze** a pak definujte pořadí dimenze v konsolidační společnosti.

![Karta Finanční dimenze](./media/financial-dimensions-cons.png "karta Finanční dimenze")

Bez ohledu na pořadí, které definujete, bude **Hlavní účet** vždy prvním segmentem.

## <a name="legal-entities"></a>Právnické osoby
Na kartě **Právnické osoby** definujete společnosti, které mají být zahrnuty v konsolidační společnosti. Můžete také definovat procento vlastnictví těchto společností. Zadáte-li nižší než 100% vlastnictví, zadané procento bude zahrnuto do konsolidační společnosti. Pro všechny rozdíly převodu se použije pole **Typ účtu pro rozdíly převodu** k výběru hlavního účtu z nastavení na stránce **Účty pro automatické transakce**.

![Karta Právnické osoby](./media/legal-entities-cons.png "Karta Právnické osoby")

![Stránka Účty pro automatické transakce](./media/accounts%20for%20automatic%20(cons).png "Stránka Účty pro automatické transakce")

## <a name="elimination"></a>Eliminace
Na kartě **Eliminace** máte tři možnosti pro zpracování eliminací:

- Vyberte pravidlo eliminace a poté v poli **Možnosti návrhu** vyberte **Pouze návrh**. Tato možnost zpracuje eliminaci během procesu konsolidace, ale nezaúčtuje vše v jednom kroku. Zaúčtovat deník můžete později.
- Vyberte pravidlo eliminace a poté v poli **Možnosti návrhu** vyberte **Pouze zaúčtovat**. Tato možnost zpracuje eliminaci během procesu konsolidace a zaúčtuje vše v jednom kroku.
- Spusťte návrh eliminace odděleně od procesu konsolidace pomocí deníku eliminace.

![Karta Eliminace](./media/elimination-cons-onl.png "Karta Eliminace")

Další informace o eliminacích naleznete v tématu [Pravidla eliminace](./elimination-rules.md).

## <a name="currency-translation"></a>Převod měny
Na kartě **Převod měny** definujete právnickou osobu, účet a typ směnného kurzu a sazbu. V poli **Použít směnný kurz z** jsou k dispozici tři možnosti:

- **Datum konsolidace** – Datum konsolidace se použije k získání směnného kurzu. Tento kurz je ekvivalentem místního kurzu nebo kurzu na konci měsíce. Zobrazí se náhled kurzu, ale nelze ho upravovat.
- **Datum transakce** – Datum každé transakce se použije k výběru směnného kurzu. Tato možnost se nejčastěji používá pro dlouhodobý majetek a obvykle se označuje jako historický kurz. Nelze zobrazit náhled kurzu, protože existuje mnoho kurzů pro různé transakce v rozsahu účtu.
- **Sazba definovaná uživatelem** – Když vyberete tuto možnost, můžete zadat směnný kurz, který chcete. Tato možnost může být užitečná pro průměrné směnné kurzy, nebo pokud konsolidujete proti pevnému směnnému kurzu.

![Karta Převod měny](./media/currency-translation-cons-online.png "Karta Převod měny")

## <a name="additional-resources"></a>Další zdroje

Další informace o konsolidaci a převodech měn naleznete v nadřazeném tématu [Finanční konsolidace a převod měny](./financial-consolidations-currency-translation.md).

Další informace o scénářích, kde můžete vygenerovat konsolidační finanční výkazy naleznete v tématu [Generování konsolidovaných finančních výkazů](./generating-consolidated-financial-statements.md).

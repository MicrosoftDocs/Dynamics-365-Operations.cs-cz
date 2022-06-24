---
title: Export dat dceřiných společností do souborů
description: Tento článek vysvětluje, jak připravit export dat z aplikace Microsoft Dynamics 365 Finance a poté je importovat do konsolidované právnické osoby.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 7c5334e206d28a5ae1c8097db5356cd1057b7180
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876146"
---
# <a name="export-subsidiary-data-to-files"></a>Export dat dceřiných společností do souborů

[!include [banner](../includes/banner.md)]

Stránka **Export** (**Správa systému \> Pracovní prostory \> Import/export**) slouží k přípravě exportu dat dceřiných společností do souborů, které lze poté importovat do konsolidované právnické osoby. Další informace o importu a exportu naleznete v tématu [Přehled úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Vytvořte právnickou osobu pro proces konsolidace. Další informace, jak vytvořit právnické osoby, najdete v části [Vytvoření právnícké osoby](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Další informace viz [Připrava právnické osoby pro použití v procesu konsolidace](prepare-company-for-consolidation.md) a [Založení dceřiné právnické osoby ke konsolidaci](set-up-subsidiary-company-for-consolidation.md). 

2. Přejděte na **Konsolidace \> Export zůstatků společnosti**. Na stránce **Export zůstatků společnosti** na kartě **Kritéria** zadejte podrobnosti konsolidace nastavením následujících polí.

    | Pole                             | popis |
    |-----------------------------------|-------|
    | Hlavní účet                      | Určete účty, které chcete konsolidovat. Chcete-li zahrnout všechny účty, nechte toto pole prázdné. |
    | Použití konsolidačního účtu         | Pokud jste zadali konsolidační účty, nastavte tuto možnost na **Ano**. |
    | Vybrat konsolidační účet z | Vyberte **Hlavní účet** nebo **Skupina konsolidačních účtů**. |
    | Skupina konsolidačních účtů       | Vyberte skupinu konsolidačních účtů pro konsolidační účet, který jste vybrali. |
    | Období konsolidace              | Pro konsolidaci zadejte data „od“ a „do“. |
    | Zahrnout skutečné částky            | Tuto možnost nastavte na **Ano**, chcete-li zahrnout skutečné částky. |
    | Zahrnout rozpočtové částky            | Tuto možnost nastavte na **Ano**, chcete-li zahrnout částky rozpočtu do konsolidací. |
    | Rozpočtové modely                     | Zadejte rozpočtový model, který chcete zahrnout. |

3. Na kartě **Finanční dimenze** upřesněte podrobnosti konsolidace:

    - Upřesněte informace o finanční dimenzi, které se mají převést z transakcí v účtech dceřiné společnosti do transakcí v konsolidovaném právním subjektu.
    - Vyberte finanční dimenze v seznamu.
    - Určete správnou specifikaci pro každou finanční dimenzi, která je konsolidována. Dostupné možnosti zahrnují **Dimenze**, **Skupinová dimenze**, **Firemní účty** a **Účet**.

        > [!NOTE]
        > Možnost **Skupinová dimenze** umožňuje definovat hodnotu dimenze, kterou používá skupina společností, která se konsoliduje.

    - Určete pořadí segmentů, do kterých chcete konsolidovat.

4. Na kartě **Právnické osoby** pomocí těchto pokynů zadejte právnickou osobu, kterou exportujete:

    1. Zvolte **Nové**.
    2. Do pole **Zdrojová právnická osoba** zadejte právnickou osobu.

        Jestliže lze stejná kritéria použít pro několik dceřiných společností ve stejné databázi, můžete v rámci jedné operace přenést data z těchto dceřiných společností do oddělených souborů pro export:

        1. Vytvořte řádek pro každou dceřinou právnickou osobu, jejíž účty budou exportovány do souborů. Tyto soubory budou importovány do konsolidované právnické osoby později.
        2. Pro každou dceřinou společnost zadejte název. Dále zadejte název exportního souboru, který bude vytvořen v průběhu exportní úlohy.

    3. V poli **Typ účtu pro rozdíly převodu** vyberte **Zisky a ztráty** nebo **Rozvaha**.
    4. Zadejte název souboru pro exportovaný soubor, který bude vytvořen.

5. Tlačítkem **OK** spustíte export.

Po dokončení exportu se zobrazí zpráva s počtem záznamů uložených do každého souboru. Soubory pak můžete importovat do konsolidované právnické osoby.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

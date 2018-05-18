---
title: "Přidání finančních dimenzí k pracovnímu prostoru CFO"
description: "Toto téma vysvětluje postup při přidání finančních dimenzí do pracovního prostoru CFO tak, aby bylo možné je používat pro hlavní knihu a sestavy rozpočtu."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5faefe5da8c3a64987a38ebef92eb87049ebe874
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Přidání finančních dimenzí k pracovnímu prostoru CFO

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje postup při přidání finančních dimenzí do pracovního prostoru CFO (Chief Financial Officer) tak, aby bylo možné je používat pro hlavní knihu a sestavy rozpočtu. Pracovní prostor CFO má kartu **Přehled** a kartu **Finanční**. Sestavy na těchto dvou kartách jsou podloženy dvěma měřeními: LedgerActivityMeasure a BudgetActivityMeasure. V aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (červenec 2017) existuje vztah mezi těmito dvěma měřeními a entitou DimensionCombinationEntity. Z tohoto důvodu lze vybrat dimenze.

1. V aplikaci Finance and Operations aktualizujte měření **LedgerActivityMeasure** a **BudgetActivityMeasure** na stránce **Úložiště entit**.
2. V aplikaci Microsoft Visual Studio otevřete Průzkumníka aplikace a vyhledejte **LedgerCFO**.
3. Pod položkou **Zdroje** otevřete **LedgerCFOWorkspacePBIX**.
4. Když se zdroj otevře v Microsoft Power BI Desktop, vyberte **Načíst data**, vyberte **Databáze SQL Server** a poté vyberte **Připojit**.
5. Zadejte název serveru a zadejte **AxDW** jako databázi. Vyberte možnost **DirectQuery** a pak zvolte **OK**.
6. Vyhledejte a vyberte **LedgerActivityMeasure\_DimensionCombination** a poté vyberte **Načíst**.

    > [!TIP]
    > V seznamu **Pole** přejmenujte tabulku **Finanční dimenze**, aby ji bylo možné snadno identifikovat.

7. Vyberte **Spravovat relace** a poté vyberte **Nový**.
8. V prvním poli vyberte **Aktivity hlavní knihy** a poté vyberte **LedgerDimension**.
9. V druhém poli vyberte **LedgerActivityMeasure\_DimensionCombination** (nebo **Finanční dimenze**, pokud jste přejmenovali tabulku). Vyberte záhlaví **DimensionCombinationRECID**.
10. V poli **Kardinalita** vyberte **N:1**.
11. Změňte hodnotu **Směr křížového filtru** na **Jednoduchý**.
12. Zvolte **Aktivovat tuto relaci** a **Předpokládat referenční integritu**, vyberte **OK** a poté vyberte **Zavřít**.

    [![Vytvoření relace](./media/Create-relationship.png)](./media/Create-relationship.png)

13. V seznamu **Pole** by se měla zobrazit tabulka a dostupné finanční dimenze. Přetáhněte finanční dimenze, které chcete mít ve filtrech na úrovni sestavy.
14. Uložte změny.
15. Ve stromu aplikačních objektů (AOT) klikněte pravým tlačítkem myši a poté vyberte **Synchronizovat**.
16. Vytvořte svůj projekt a potom otevřete aplikaci pro zobrazení výsledků.

    [![Dokončený pracovní prostor](./media/workspace.png)](./media/workspace.png)


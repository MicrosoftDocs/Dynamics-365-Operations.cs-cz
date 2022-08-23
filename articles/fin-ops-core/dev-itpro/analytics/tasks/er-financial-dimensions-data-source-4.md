---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 4 - spuštění sestavy)
description: Tento článek popisuje, jak nakonfigurovat model elektronického výkaznictví (ER) tak, aby používal finanční dimenze jako zdroj dat pro zprávy ER. (část 4)
author: kfend
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, SysQueryForm
ms.openlocfilehash: d0fca8b1a6139b71782af05531d9494c968ef9f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290747"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 4 - spuštění sestavy)

[!include [banner](../../includes/banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví. Tyto kroky lze provést v rámci společnosti DEMF.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 3: návrh sestavy"). Na stránce Parametry elektronického výkaznictví musíte také nakonfigurovat výchozí typy dokumentů. Výchozí typy dokumentů jsou nastaveny také při stahování a importu konfigurace všech elektronických výkazů. 


## <a name="run-report"></a>Spuštění sestavy
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte Vzorový model finančních dimenzí.
3. Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí\Sestava deníku hlavní knihy.
4. Klikněte na Spustit.
![Stránka konfigurací elektronického výkaznictví.](../media/er-financial-dimensions-guides-run1.png)
5. V poli Název dimenze zadejte nebo vyberte hodnotu.
    * Chcete-li vybrat všechny dimenze v aktuální společnosti, zadejte následující informace: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![Vysunou se parametry elektronické zprávy, rozevírací seznam Název dimenze.](../media/er-financial-dimensions-guides-run2.png)
6. Rozbalte oddíl Záznamy k zahrnutí.
7. Klepněte na tlačítko Filtr.
8. Vyberte řádek v tabulce Deník hlavní knihy a v poli Číslo dávky deníku.
9. Zadejte hodnotu 00057 do pole Kritéria.
10. Klepněte na tlačítko OK.
11. Klepněte na tlačítko OK.
![Vysouvají se parametry elektronické zprávy, sekce Výkazy k zahrnutí.](../media/er-financial-dimensions-guides-run3.png)
    * Prohlédněte si generovaný výstup. Pro každou transakci vybrané dávky jsou uvedeny finanční dimenze z odpovídající sady dimenzí. Spusťte tuto sestavu a vyberte různé dimenze k ověření, že sestava není závisí na počtu vybraných dimenzí nebo několika dimenzí nakonfigurovaných pro tuto instanci.  
![Konfigurace ER generuje výstup.](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

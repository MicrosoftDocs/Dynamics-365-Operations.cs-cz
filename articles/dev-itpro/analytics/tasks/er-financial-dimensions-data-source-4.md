---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 4 - spuštění sestavy)
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 917eae141bbb8792f02d3323054e2a4096dae551
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544649"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4-run-the-report"></a>Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 4: spuštění sestavy)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví. Tyto kroky lze provést v rámci společnosti DEMF.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 3: návrh sestavy"). Na stránce Parametry elektronického výkaznictví musíte také nakonfigurovat výchozí typy dokumentů. Výchozí typy dokumentů jsou nastaveny také při stahování a importu konfigurace všech elektronických výkazů. 


## <a name="run-report"></a>Spuštění sestavy
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte Vzorový model finančních dimenzí.
3. Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí\Sestava deníku hlavní knihy.
4. Klikněte na Spustit.
5. V poli Název dimenze zadejte nebo vyberte hodnotu.
    * Chcete-li vybrat všechny dimenze v aktuální společnosti, zadejte následující hodnoty:   BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
6. Rozbalte oddíl Záznamy k zahrnutí.
7. Klepněte na tlačítko Filtr.
8. Vyberte řádek v tabulce Deník hlavní knihy a v poli Číslo dávky deníku.
9. Zadejte hodnotu 00057 do pole Kritéria.
10. Klikněte na tlačítko OK.
11. Klikněte na tlačítko OK.
    * Prohlédněte si generovaný výstup. Všimněte si, že pro každou transakci vybrané dávky jsou uvedeny finanční dimenze z odpovídající sady dimenzí. Spusťte tuto sestavu a vyberte různé dimenze k ověření, že sestava není závisí na počtu vybraných dimenzí nebo několika dimenzí nakonfigurovaných pro tuto instanci Dynamics 365 for Finance and Operations Enterprise edition.  


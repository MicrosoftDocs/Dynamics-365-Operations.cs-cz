--- 
title: "Spuštění sestavy používající finanční dimenze jako zdroj dat pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: cdecf5fb3f3047a56353ee6d4a8f94957f508e4b
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Spuštění sestavy používající finanční dimenze jako zdroj dat pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

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
    * Prohlédněte si generovaný výstup. Všimněte si, že pro každou transakci vybrané dávky jsou uvedeny finanční dimenze z odpovídající sady dimenzí. Spusťte tuto sestavu a vyberte různé dimenze k ověření, že sestava není závisí na počtu vybraných dimenzí nebo několika dimenzí nakonfigurovaných pro tuto instanci Dynamics 365 for Finance and Operations, edice Enterprise.  



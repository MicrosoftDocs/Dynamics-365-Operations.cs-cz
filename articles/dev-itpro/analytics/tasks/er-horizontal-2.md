--- 
title: "Spuštění formátu používajícího vodorovně rozbalovací oblasti k dynamickému přidání sloupců v sestavách aplikace Excel pro elektronické výkaznictví (ER)"
description: "Následující postup vysvětluje, jak uživatel s přiřazenou rolí správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formát elektronických sestav (ER) ke generování sestav jako soubory s listy OPENXML (Excel), ve kterých lze dynamicky vytvářet požadované sloupce jako vodorovně rozbalitelné rozsahy."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3ca72ab5c7ac15f3a788ea457a360d93a0b505b0
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Spuštění formátu používajícího vodorovně rozbalovací oblasti k dynamickému přidání sloupců v sestavách aplikace Excel pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující postup vysvětluje, jak uživatel s přiřazenou rolí správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formát elektronických sestav (ER) ke generování sestav jako soubory s listy OPENXML (Excel), ve kterých lze dynamicky vytvářet požadované sloupce jako vodorovně rozbalitelné rozsahy. Tyto kroky lze provést v rámci společnosti DEMF.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel (část 1: formát návrhu).

Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.


## <a name="find-created-format"></a>Vyhledání vytvořeného formátu
1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
2. Ve stromovém zobrazení rozbalte Vzorový model finančních dimenzí.
3. Ve stromové struktuře vyberte 'Vzorový model finančních dimenzí\Vzorová sestava s vodorovně rozbalitelnými rozsahy'.

## <a name="execute-format-to-create-excel-output"></a>Spuštění formátu k vytvoření výstupu v Excelu
1. Klikněte na položku Spustit.
2. Do pole Název dimenze zadejte 'BusinessUnit;CostCenter;Department'.
    * V poli Název dimenze zadejte nebo vyberte hodnotu.  Chcete-li vybrat všechny dimenze pro aktuální společnost, zadejte následující hodnoty:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Rozbalte oddíl Záznamy k zahrnutí.
4. Klepněte na tlačítko Filtr.
5. Vyberte řádek v tabulce Deník hlavní knihy a v poli Číslo dávky deníku.
6. Zadejte hodnotu '00057..00058' do pole Kritéria.
    * 00057..00058  
7. Klikněte na tlačítko OK.
8. Klikněte na tlačítko OK.
    * Prohlédněte si generovaný výstup. Všimněte si, že nově vytvořený soubor aplikace Excel obsahuje stejný počet sloupců, které byly vybrány pro finanční dimenze. Záhlaví sestavy v těchto sloupcích představuje názvy finančních dimenzí. Řádky transakce v těchto sloupcích představují finančních dimenze. Spusťte tuto sestavu a vyberte různé dimenze k ověření, že sestava nezávisí na počtu vybraných dimenzí nebo několika dimenzí nakonfigurovaných pro tuto instanci Dynamics 365 for Finance and Operations.  



---
title: Elektronické výkaznictví – Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel (část 2 - Formát spuštění)
description: Tento článek popisuje, jak nakonfigurovat formát elektronického výkaznictví (ER) pro generování sestav jako soubory listů OPENXML (Excel). (část 2)
author: kfend
ms.date: 08/29/2018
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
ms.openlocfilehash: 08755eafa2a18993ba669f0deccd75477bfae410
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290387"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>Elektronické výkaznictví – Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel (část 2 - Formát spuštění)

[!include [banner](../../includes/banner.md)]

Následující postup vysvětluje, jak uživatel s přiřazenou rolí správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formát elektronických sestav (ER) ke generování sestav jako soubory s listy OPENXML (Excel), ve kterých lze dynamicky vytvářet požadované sloupce jako vodorovně rozbalitelné rozsahy. Tyto kroky lze provést v rámci společnosti DEMF.

K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití vodorovně rozbalovacích oblastí k dynamickému přidání sloupců v tabulkách aplikace Excel (část 1: formát návrhu).

Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


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
    * Prohlédněte si generovaný výstup. Všimněte si, že nově vytvořený soubor aplikace Excel obsahuje stejný počet sloupců, které byly vybrány pro finanční dimenze. Záhlaví sestavy v těchto sloupcích představuje názvy finančních dimenzí. Řádky transakce v těchto sloupcích představují finančních dimenze. Spusťte tuto sestavu a vyberte různé dimenze k ověření, že sestava není závisí na počtu vybraných dimenzí nebo několika dimenzí nakonfigurovaných pro tuto instanci.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

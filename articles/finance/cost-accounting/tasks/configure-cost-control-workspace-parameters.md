---
title: Konfigurace parametrů pracovního prostoru řízení nákladů
description: Pomocí tohoto postupu nastavte pracovní prostor řízení nákladů tak, aby vedoucí pracovníci na různých úrovních v rámci organizace mohli získat přehled o svých objektech nákladů, jako jsou nákladová střediska nebo skupiny produktů.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca05f6174541a6e97ec94db209a99424a87550eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441305"
---
# <a name="configure-cost-control-workspace-parameters"></a>Konfigurace parametrů pracovního prostoru řízení nákladů

[!include [banner](../../includes/banner.md)]

Pomocí tohoto postupu nastavte pracovní prostor řízení nákladů tak, aby vedoucí pracovníci na různých úrovních v rámci organizace mohli získat přehled o svých objektech nákladů, jako jsou nákladová střediska nebo skupiny produktů. K vytvoření tohoto záznamu jsou použita ukázková data společnosti USP2.

1. Přejděte na Nákladové účetnictví > Nastavení > Konfigurace pracovního prostoru pro řízení nákladů.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. Zadejte nějakou hodnotu do pole Popis.
5. Vyberte možnost Ano v poli Publikováno.
    * Pokud tuto možnost nastavíte na Ano, uživatelé s přiřazenou některou z těchto rolí si mohou zobrazit sestavu v pracovním prostoru řízení nákladů: manažer nákladového účetnictví, nákladový účetní, úředník na pozici nákladového účetního nebo kontrolor objektu nákladů. Pokud tuto možnost nastavíte na Ne, pouze uživatelé s přiřazenou některou z těchto rolí si mohou zobrazit sestavu v pracovním prostoru řízení nákladů: manažer nákladového účetnictví, nákladový účetní nebo úředník na pozici nákladového účetního.  
6. Rozbalte oddíl Filtrování dat.
7. V poli Jednotka řízení nákladů zadejte nebo vyberte hodnotu.
8. V poli Původní verze rozpočtu zadejte nebo vyberte hodnotu.
9. V poli Hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.
10. V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
11. Rozbalte část Přiřazení záznamů výpočtů.
12. Klikněte na možnost Nový.
13. Označte na seznamu vybraný řádek.
14. V poli Období fiskálního kalendáře zadejte nebo vyberte hodnotu.
15. V poli Aktuální verze zadejte nebo vyberte hodnotu.
16. Rozbalte část Fiskální období dle sloupce.
17. Vyberte možnost Ano v poli Aktuální období.
18. Rozbalte část Sloupce k zobrazení nákladů.
19. Vyberte možnost Ano v poli Pevné náklady.
20. Vyberte možnost Ano v poli Proměnné náklady.
21. Vyberte možnost Ano v poli Celkové náklady.
22. Klikněte na položku Uložit.
23. Zavřete stránku.
24. Přejděte do části Nákladové účetnictví > Pracovní prostory > Řízení nákladů.
25. Vyberte výpis podle toho, zda chcete zobrazit pevné, proměnné, celkové nebo nezatříděné náklady pro vybraná fiskální období.
26. V poli Období fiskálního kalendáře zadejte nebo vyberte hodnotu.
27. V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Po výběru hierarchie dimenzí objektu nákladů rozbalte hierarchii dimenzí prvku nákladů a prohlédněte si požadované nákladové hodnoty. Můžete například rozbalit hierarchii Výrobní režie a zjistit z ní hodnoty.  


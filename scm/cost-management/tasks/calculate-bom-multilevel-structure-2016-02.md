--- 
title: "Výpočet kusovníku pomocí víceúrovňové struktury (jen ve verzi z února 2016)"
description: "Tento postup ukazuje, jak vypočítat náklady na dokončený výrobek s použitím víceúrovňového rozpadu založeného na nákladovém formuláři."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 1ad38f67bba299bbd581aba6010b4028c91fbf3a
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a>Výpočet kusovníku pomocí víceúrovňové struktury (jen ve verzi z února 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup ukazuje, jak vypočítat náklady na dokončený výrobek s použitím víceúrovňového rozpadu založeného na nákladovém formuláři. Je to sedmá úloha v řadě Kalkulace kusovníku. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.

1. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte produkt BOM_1.  
3. V podokně akcí klikněte na možnost Spravovat náklady.
4. Klikněte na možnost Cena položky.
5. Klikněte na Vypočítat náklady na zboží.
    * Můžete kliknout na tlačítko se třemi tečkami (...) a v horní nabídce se zobrazí tato možnost.  
6. V poli Nákladová verze zadejte nebo vyberte hodnotu.
    * Zvolte položku Nákladová verze 20, protože se jedná o typ Plánované náklady a Režim rozpadu je Víceúrovňový.   Režim rozpadu na více úrovních je pro plánované náklady a simulace. Nepoužívá se pro standardní náklady.  
7. Klikněte na tlačítko OK.
8. Klepněte na Zobrazit podrobnosti výpočtu.
    * Můžete kliknout na tlačítko se třemi tečkami (...) a v horní nabídce se zobrazí tato možnost.  V takovém případě si všimněte, jak byl BOM_2 vypočítán s ohledem na suroviny, proces a režii s celkovým nákladem 29,40 namísto standardního nákladu 10, který byl aktivován v počátečním průvodci záznamem úloh v této řadě.  
9. Klikněte na kartu Nákladový formulář.
    * Když se přesuneme na kartu Nákladový formulář, součty podle nákladových skupin se liší ve srovnání s výpočtem provedeným v předchozím průvodci záznamem úloh.  
10. V poli Úroveň vyberte 'Vícenásobná'.
    * Pokud vyberete Vícenásobné, jsou náklady klasifikovány podle složení BOM_2, kde 10 je odvozeno od M1 nákladové skupiny (ITEM_C) a 15,60 je odvozeno od jeho výroby, kde nákladová skupina je L2. Nepřímé náklady se též liší.  
11. Zavřete stránku.
12. Zavřete stránku.



---
title: Výpočet kusovníku pomocí víceúrovňové struktury (únor 2016)
description: Tento postup ukazuje, jak vypočítat náklady na dokončený výrobek s použitím víceúrovňového rozpadu založeného na nákladovém formuláři.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 859f7b7c828dcdad1aa836044d2cc26847630f1e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821410"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Výpočet kusovníku pomocí víceúrovňové struktury (únor 2016)

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Výpočet kusovníku pomocí struktury jediné úrovně (únor 2016)
description: Tento postup ukazuje, jak vypočítat náklady na dokončený výrobek s použitím jednoúrovňového rozpadu založeného na nákladovém formuláři.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013eddf1ba8e8cab3c87cb1f063d9bf886b0f833
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821386"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Výpočet kusovníku pomocí struktury jediné úrovně (únor 2016)

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje, jak vypočítat náklady na dokončený výrobek s použitím jednoúrovňového rozpadu založeného na nákladovém formuláři. Je to šestá úloha v řadě Kalkulace kusovníku. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.

1. Přejděte na Uvolněné produkty.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte produkt BOM_1.  
3. V podokně akcí klikněte na možnost Spravovat náklady.
4. Klikněte na možnost Cena položky.
5. Klikněte na Vypočítat náklady na zboží.
    * Můžete kliknout na tlačítko se třemi tečkami (...) a v horní nabídce se zobrazí tato možnost.  
6. V poli Nákladová verze klikněte na tlačítko rozevíracího seznamu a otevřete vyhledávání.
    * V této ukázce vyberte 10. Jedná se o stejnou nákladovou verzi sloužící k přidání nákladové ceny ke komponentám.  
7. Klikněte na tlačítko OK.
8. Klepněte na Zobrazit podrobnosti výpočtu.
    * Můžete kliknout na tlačítko se třemi tečkami (...) a v horní nabídce se zobrazí tato možnost.    Zde je složení nákladů  *    10 je odvozeno z ITEM_A, 10 z ITEM_B, 10 z BOM_2. V tomto případě nejsou žádné podrobnosti pro BOM_2, protože tato položka byla zadána jako standardní náklady 10, ale nebyl proveden výpočet.  *    7 je odvozeno z přípravného času, který je konstantním nákladem, a dalších 7 pochází z operace běhu (procesu).  *    Existují i jiné částky, které odpovídají nepřímým nákladům.  
9. @SysTaskRecorder:_RequestClose



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
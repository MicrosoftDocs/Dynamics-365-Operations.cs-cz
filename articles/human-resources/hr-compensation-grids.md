---
title: Nastavit kompenzační mřížky
description: Kompenzační mřížky umožňují definovat a spravovat struktury plateb pro plány fixní kompenzace.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51b98320eac539e49787d352f32683efadc11f41
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071411"
---
# <a name="set-up-compensation-grids"></a>Nastavit kompenzační mřížky


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompenzační mřížky umožňují definovat a spravovat struktury plateb pro plány fixní kompenzace. Kompenzační mřížky můžete sdílet mezi několika plány nebo zkopírovat při vytvoření nového plánu kompenzace.  Před vytvořením kompenzační mřížky, je nutné nastavit úrovně a referenční body. V tomto příkladu vytvoříme nový typ třídy kompenzační mřížky pomocí ukázkových dat pro úrovně a referenční body. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Nastavit informace o kompenzační mřížce
1. Přejděte do nabídky **Lidské zdroje** > **Kompenzace** > **Fixní kompenzace** > **Kompenzační mřížky**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Mřížka**.
4. Zadejte hodnotu do pole **Popis**.
5. Vyberte volbu v poli **Typ**.
6. V poli nastavení **Reference** zadejte nebo vyberte hodnotu.
7. V poli **Měna** zadejte nebo vyberte hodnotu.
8. Zadejte datum do pole **Datum platnosti**.

## <a name="add-levels-to-the-compensation-structure"></a>Přidání úrovní do kompenzační struktury
1. Klikněte na možnost **Struktura kompenzací**.
2. Označte v seznamu vybraný řádek.
3. V poli **Úroveň** zadejte nebo vyberte hodnotu.
4. Klepněte na možnost **Nový**.
5. Označte v seznamu vybraný řádek.
6. V poli **Úroveň** zadejte nebo vyberte hodnotu.
7. Klepněte na možnost **Nový**.
8. Označte v seznamu vybraný řádek.
9. V poli **Úroveň** zadejte nebo vyberte hodnotu.
10. Klepněte na možnost **Nový**.
11. Označte v seznamu vybraný řádek.
12. V poli **Úroveň** zadejte nebo vyberte hodnotu.
13. Klepněte na možnost **Nový**.
14. Označte v seznamu vybraný řádek.
15. V poli **Úroveň** zadejte nebo vyberte hodnotu.

## <a name="fill-in-the-compensation-structure-with-values"></a>Vyplňte hodnoty do kompenzační struktury
1. Označte v seznamu vybraný řádek.
    * V tomto okamžiku lze zadat ručně náhradní hodnoty do každého pole tabulky, nebo lze použít funkci hromadné změny ke snadnému vyplnění více polí a provádění základních výpočtů.  
2. Klikněte na **Hromadná změna**.
    * U této tabulky nejprve použijeme hodnotu pro středový bod první úrovně ke všem polím v tabulce. To bude základem pro kompenzační matici.  
3. V poli **Typ úprav** vyberte možnost.
4. Zadejte číslo do pole **Částka úpravy**.
5. V seznamu označte všechny řádky nebo jejich označení zrušte.
6. Klikněte na **Použít na mřížku**.
    * Nyní použijeme funkci hromadné změny ke zvýšení částek v jednotlivých úrovních určitým procentem nebo částkou. V tomto příkladu bude mít každá třída rozšíření 12,5 % mezi jejich středními body.  
7. V poli **Typ úprav** vyberte možnost.
8. Zadejte číslo do pole **Částka úpravy**.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. Klikněte na **Použít na mřížku**.
    * Nyní použijeme funkci hromadné změny pro úpravu minimálních a maximálních referenčních bodů pro každou úroveň. V tomto příkladu použijeme 50% rozložení, takže minimální referenční bod bude upraven na hodnotou -20 % a maximum bude upraveno na +20 %.  
11. Zadejte číslo do pole **Částka úpravy**.
12. V poli **Referenční bod** zadejte nebo vyberte hodnotu.
13. V seznamu označte všechny řádky nebo jejich označení zrušte.
14. Klikněte na **Použít na mřížku**.
15. Zadejte číslo do pole **Částka úpravy**.
16. V poli **Referenční bod** zadejte nebo vyberte hodnotu.
17. V seznamu označte všechny řádky nebo jejich označení zrušte.
18. Klikněte na **Použít na mřížku**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]

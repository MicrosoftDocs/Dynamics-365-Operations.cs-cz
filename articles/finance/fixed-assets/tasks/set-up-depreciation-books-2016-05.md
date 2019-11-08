---
title: Nastavení knih odpisů (květen 2016)
description: Tento průvodce úkolem vytvoří novou knihu odpisů a přiřadí ji ke skupině dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186893"
---
# <a name="set-up-depreciation-books-may-2016"></a>Nastavení knih odpisů (květen 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem vytvoří novou knihu odpisů a přiřadí ji ke skupině dlouhodobého majetku.  Využívá účetní role a ukázková data pro právnické osoby USMF.


## <a name="create-a-depreciation-book"></a>Vytvoření knihy odpisů
1. Přejděte do části Dlouhodobý majetek > Nastavení > Knihy odpisů.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Kniha odpisů.
4. Zadejte nějakou hodnotu do pole Popis.
5. Zaškrtněte nebo zrušte zaškrtnutí políčka Vypočítat odpis.
6. V poli Odpisový plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyhledejte na seznamu požadovaný odpisový plán a vyberte ho.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. V poli Alternativní odpisový plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
10. V seznamu vyberte požadovaný odpisový plán.
11. Klikněte na odkaz na vybraném řádku v seznamu.
    * Plán mimořádných odpisů se používá pro dodatečný odpis majetku při neobvyklých okolností. Například to můžete použít k záznamu odpisů, které je výsledkem živelné pohromy.  
12. Zaškrtněte nebo zrušte zaškrtnutí políčka Vytvořit úpravy odpisů s úpravami základu.
13. V poli Kalendář kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
14. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Přiřazení knihy odpisů ke skupině dlouhodobého majetku
1. Klikněte na Skupiny dlouhodobého majetku.
2. V poli Skupina dlouhodobého majetku kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Vyberte volbu v poli Způsob odpisu.
6. Zadejte číslo do pole Doba životnosti.
    * Všimněte si, že hodnota pole Období odpisu se vypočítá po nastavení doby životnosti.  

---
title: Nastavení knih odpisů
description: Tento postup prochází procesem vytvoření nové knihy odpisů a jejím přidružením ke skupině dlouhodobého majetku.
author: moaamer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a4713d949fe119cde1b1187a7c485d291281a8f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725645"
---
# <a name="set-up-depreciation-books"></a>Nastavení knih odpisů 

[!include [banner](../../includes/banner.md)]

Tento postup prochází procesem vytvoření nové knihy odpisů a jejím přidružením ke skupině dlouhodobého majetku. 

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

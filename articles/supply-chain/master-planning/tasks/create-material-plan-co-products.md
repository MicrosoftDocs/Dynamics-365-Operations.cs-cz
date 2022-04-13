---
title: Vytvoření materiálového plánu pro vedlejší produkty
description: Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27bba54db915b7ccc31fda43a00a8c9435493e07
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469526"
---
# <a name="create-a-material-plan-for-co-products"></a>Vytvoření materiálového plánu pro vedlejší produkty

[!include [banner](../../includes/banner.md)]

Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury. K vytvoření tohoto postupu jsou použita ukázková data společnosti USP2.

## <a name="create-requirement-for-a-co-product"></a>Vytvoření požadavku pro vedlejší produkt

1. Přejděte do **Prodej a marketing \> Pracovní prostory \> Zpracování a poptávka prodejní objednávky**.
1. Zvolte **Nové**.
1. Vyberte **Prodejní objednávka**.
1. V poli **Účet odběratele** zadejte hodnotu.
    * Příklad: US-001  
1. Vyberte **OK**.
1. Zadejte hodnotu do pole **Číslo zboží**.
    * Příklad: P6003  
1. Zadejte číslo do pole **Množství**.
    * Příklad: 50000  
1. Zvolte **Uložit**.

## <a name="create-a-material-plan-for-co-products"></a>Vytvoření materiálového plánu pro vedlejší produkty

1. Zavřete stránku.
1. Zavřete stránku.
1. Vyberte **Hlavní plánování**.
1. V poli **Plán** zvolením tlačítka rozevíracího seznamu otevřete vyhledávání.
1. Vyberte odkaz na vybraném řádku v seznamu.
    * Příklad: MasterPlan  
1. Vyberte **Spustit**.
1. Rozbalte nebo sbalte oddíl **Záznamy k zahrnutí**.
1. Vyberte **Filtr**.
1. V seznamu vyberte řádek pro **Pole** = *číslo položky*.
1. Zadejte hodnotu do pole **Kritéria**.
    * Příklad: P6003  
1. Vyberte **OK**.
1. Vyberte **OK**.
1. Vyberte **Plánované objednávky**.
1. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat pole **Číslo položky** pomocí hodnoty „P6000“.
    * Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.  
1. Označte na seznamu vybraný řádek.
    * Vyberte libovolné řádky vrácené filtrem.  
1. Vyberte odkaz na vybraném řádku v seznamu.
1. Rozbalte sekci **Doložení**.
1. Vyberte odkaz na vybraném řádku v seznamu.
    * Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.  
1. Zavřete stránku.

## <a name="create-a-second-requirement-for-a-co-product"></a>Vytvoření druhého požadavku pro vedlejší produkt

1. Přejděte do **Prodej a marketing \> Pracovní prostory \> Zpracování a poptávka prodejní objednávky**.
1. Zvolte **Nové**.
1. Vyberte **Prodejní objednávka**.
1. V poli **Účet odběratele** zadejte hodnotu.
    * Příklad: US-001  
1. Vyberte **OK**.
1. Zadejte hodnotu do pole **Číslo zboží**.
    * Příklad: P6003  
1. Zadejte číslo do pole **Množství**.
    * Příklad: 50000  
1. Zvolte **Uložit**.

## <a name="create-a-second-material-plan-for-co-products"></a>Vytvoření druhého materiálového plánu pro vedlejší produkty

1. V poli **Plán** zvolením tlačítka rozevíracího seznamu otevřete vyhledávání.
2. Vyberte odkaz na vybraném řádku v seznamu.
    * Příklad: MasterPlan  
3. Vyberte **Spustit**.
4. Rozbalte nebo sbalte oddíl **Záznamy k zahrnutí**.
5. Vyberte **Filtr**.
6. V seznamu vyberte řádek pro **Pole** = *číslo položky*.
7. Zadejte hodnotu do pole *Kritéria*.
    * Příklad: P6003  
8. Vyberte **OK**.
9. Vyberte **OK**.
10. Vyberte **Plánované objednávky**.
11. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat pole **Číslo položky** pomocí hodnoty „P6000“.
    * Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.  
12. Označte na seznamu vybraný řádek.
    * Vyberte libovolné řádky vrácené filtrem.  
13. Vyberte odkaz na vybraném řádku v seznamu.
14. Rozbalte nebo sbalte oddíl **Doložení**.
15. Vyberte odkaz na vybraném řádku v seznamu.
    * Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.  
16. Zavřete stránku.
17. Vyberte **Hlavní plánování**.
18. Přejděte na **Hlavní plánování \> Nastavení \> Parametry hlavního plánování**.
19. V poli **Zakázat všechny procesy plánování** vyberte *Ne*.
20. Zavřete stránku.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
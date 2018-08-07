---
title: "Inicializace úrovní zásob ve skladu"
description: "Tento postup popisuje, jak manuálně aktualizovat zásoby na skladě pomocí deníku pohybu zásob."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 3b4685b034f7e6a3af0259fb921230e7b3397754
ms.contentlocale: cs-cz
ms.lasthandoff: 11/02/2017

---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Inicializace úrovní zásob ve skladu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak manuálně aktualizovat zásoby na skladě pomocí deníku pohybu zásob. (Lze rovněž aktualizovat zásoby na skladě pomocí importu transakcí v datových entitách.) Tohoto průvodce můžete spustit v ukázkových datech společnosti USMF, kde všechny požadavky, jako je název deníku, nastavení položky, účetní profily nebo účty jsou k dispozici. Průvodce navrhuje hodnoty specifické pro položku a dimenze, které se používají. Pokud vyberete jinou položku, může být vyžadováno zadání hodnot pro různé dimenze.

1. Přejděte do Řízení zásob > Položky deníku > Zboží > Pohyb.
2. Klikněte na položku Nová.
3. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyberte pohyb zboží
    * Je vhodné použít jiné šablony názvů deníků pro jiné obchodní účely.  
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Zadejte hodnotu „140200“ do pole Protiúčet.
    * Toto je protiúčet, který bude výchozím protiúčtem na řádcích deníku. Je možné přepsat výchozí nastavení pro přiřazení různých protiúčtů na každém řádku.  
7. Klikněte na tlačítko OK.
8. Klikněte na položku Nová.
9. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
10. Vyberte položku A0001.
11. Klikněte na odkaz na vybraném řádku v seznamu.
12. Klepněte na kartu Dimenze zásob.
13. V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
14. Vyberte lokalitu 1.
15. V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
16. Vyberte sklad 13.
17. Klikněte na odkaz na vybraném řádku v seznamu.
18. V poli Umístění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
19. Vyberte umístění 13.
20. Zadejte číslo do pole Množství.
21. Klikněte na položku Uložit.
22. Klikněte na položku Zaúčtovat.
23. Zaškrtněte nebo zrušte zaškrtnutí políčka Převést všechny chyby zaúčtování do nového deníku.
    * Povolíte-li tuto možnost, budou do nového deníku zkopírovány všechny řádky, které se nepodařilo se zaúčtovat. Informace můžete do protokolu za účelem opravy problémů a poté zaúčtovat řádky znovu.  
24. Klikněte na tlačítko OK.
25. Zavřete stránku.
26. Zavřete stránku.


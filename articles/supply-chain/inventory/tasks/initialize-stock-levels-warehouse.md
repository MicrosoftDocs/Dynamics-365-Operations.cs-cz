---
title: Inicializace úrovní zásob ve skladu
description: Tento postup popisuje, jak manuálně aktualizovat zásoby na skladě pomocí deníku pohybu zásob.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0746b799c701c569f0ae5c657ac3302ab6626287
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823474"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Inicializace úrovní zásob ve skladu

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak manuálně aktualizovat zásoby na skladě pomocí deníku pohybu zásob. (Lze rovněž aktualizovat zásoby na skladě pomocí importu transakcí v datových entitách.) Tohoto průvodce můžete spustit v ukázkových datech společnosti USMF, kde všechny požadavky, jako je název deníku, nastavení položky, účetní profily nebo účty jsou k dispozici. Průvodce navrhuje hodnoty specifické pro položku a dimenze, které se používají. Pokud vyberete jinou položku, může být vyžadováno zadání hodnot pro různé dimenze.

1. Přejděte do Řízení zásob > Položky deníku > Zboží > Pohyb.
2. Klikněte na položku Nová.
3. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
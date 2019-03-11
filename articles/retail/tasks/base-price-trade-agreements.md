---
title: " Základní cena a obchodní smlouvy"
description: Tato procedura vás provede postupem vytváření obchodních smluv prodejních cen specifických pro kanál.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4830ac553318cfbb3cb74395d1662e74dff75290
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "320413"
---
# <a name="base-price-and-trade-agreements"></a> Základní cena a obchodní smlouvy

[!include[task guide banner](../includes/task-guide-banner.md)]

Tato procedura vás provede postupem vytváření obchodních smluv prodejních cen specifických pro kanál. Tato procedura používá data ukázkové společnosti USRT.

1. Přejděte na možnost Maloobchodní a velkoobchodní prodej > Tvorba cen a slevy > Cenové skupiny > Všechny cenové skupiny.
    * Cenové skupiny představují způsob přiřazování obchodních smluv konkrétním kanálům. Pomocí cenových skupin pro přiřazení obchodních smluv kanálu lze určovat ceny specifické pro kanál.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Cenové skupiny.
4. Zadejte hodnotu do pole Název.
5. Klikněte na položku Uložit.
6. Zavřete stránku.
7. Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Kanály > Maloobchody > Všechny maloobchody.
8. Ze seznamu vyberte možnost „New York“.
9. V podokně akcí klikněte na možnost Obchod.
10. Klikněte na možnost Cenové skupiny.
11. Klikněte na položku Nová.
12. V poli Cenové skupiny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
13. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
14. Klikněte na položku Uložit.
15. Zavřete stránku.
16. Zavřete stránku.
17. Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Produkty a kategorie > Uvolněné produkty podle kategorie.
18. Klikněte na odkaz na vybraném řádku v seznamu.
19. Klikněte na možnost Upravit.
20. Přepněte rozšíření oddílu Prodej.
21. Zadejte číslo do pole Cena.
    * Tato cena je použita, pokud jsou nalezeny žádné použitelné obchodní smlouvy.  
22. Klikněte na položku Uložit.
23. V podokně akcí klikněte na možnost Prodej.
24. Klikněte na Vytvořit obchodní smlouvy.
25. Klepněte na možnost Nový.
26. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
27. Vyberte ze seznamu možnost „Maloobchod“.
    * V ukázkových datech má deník s názvem „Maloobchod“ výchozí vztah „Cena (prodej)“. To znamená, že všechny vytvořené nové řádky budou přednastaveny jako výchozí prodejní ceny obchodních smluv.  
28. Klikněte na položku Řádky.
29. V poli Kód účtu vyberte možnost „Skupina“.
30. V poli Výběr účtu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
31. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Tím dokončíte propojení kanálu se skupinou cen pro obchodní smlouvu.  
32. Zadejte hodnotu do pole Vztah položky.
33. Zadejte číslo do pole Částka v měně.
34. Zaškrtněte nebo zrušte zaškrtnutí políčka Najít další.
    * Pokud možnost Najít další je nastavena na hodnotu „Ano“, bude oceňovací modul dále hledat použitelné obchodní smlouvy s nižší prodejní cenou. Pokud možnost Najít další je nastavena na hodnotu „Ne“, oceňovací modul zastaví hledání a použije obchodní smlouvu.  
35. Klikněte na položku Zaúčtovat.
36. Klikněte na tlačítko OK.
37. Zavřete stránku.
38. V podokně akcí klikněte na možnost Prodej.
39. Klikněte na možnost Prodejní cena.


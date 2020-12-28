---
title: " Základní cena a obchodní smlouvy"
description: Tato procedura vás provede postupem vytváření obchodních smluv prodejních cen specifických pro kanál.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
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
ms.openlocfilehash: 44dc059f7bfc3ba83a375c197ce67f1378a9bc9b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410843"
---
# <a name="base-price-and-trade-agreements"></a> Základní cena a obchodní smlouvy

[!include [banner](../includes/banner.md)]

Tato procedura vás provede postupem vytváření obchodních smluv prodejních cen specifických pro kanál. Tato procedura používá data ukázkové společnosti USRT.

1. V **navigačním podokně** přejděte na **Moduly > Retail and Commerce > Správa cen a slev > Cenové skupiny > Všechny cenové skupiny**. Cenové skupiny představují způsob přiřazování obchodních smluv konkrétním kanálům. Pomocí cenových skupin pro přiřazení obchodních smluv kanálu lze určovat ceny specifické pro kanál.  
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Cenové skupiny**.
4. Zadejte hodnotu do pole **Název**.
5. Klikněte na možnost **Uložit**.
6. Zavřete stránku.
7. V **Navigačním podokně** přejděte na **Moduly > Retail and Commerce > Kanály > Obchody > Všechny obchody**.
8. Ze seznamu vyberte možnost „New York“.
9. V podokně akcí klikněte na možnost **Obchod**.
10. Klikněte na možnost **Cenové skupiny**.
11. Klepněte na možnost **Nový**.
12. V poli **Cenové skupiny** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
13. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
14. Klikněte na možnost **Uložit**.
15. Zavřete stránku.
16. Zavřete stránku.
17. V **navigačním podokně** přejděte na **Moduly > Retail and Commerce > Produkty a kategorie > Uvolněné produkty podle kategorie**.
18. Klikněte na odkaz na vybraném řádku v seznamu.
19. Klikněte na možnost **Upravit**.
20. Rozbalte záložku s náhledem **Prodej**.
21. Zadejte číslo do pole **Cena**. Tato cena je použita, pokud jsou nalezeny žádné použitelné obchodní smlouvy.  
22. Klikněte na možnost **Uložit**.
23. V **podokně akcí** klikněte na možnost **Prodej**.
24. Klikněte na **Vytvořit obchodní smlouvy**.
25. Klepněte na možnost **Nový**.
26. V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
27. V seznamu vyberte **Commerce**. V ukázkových datech má deník s názvem **Commerce** výchozí vztah **Cena (prodej)**. To znamená, že všechny vytvořené nové řádky budou přednastaveny jako výchozí prodejní ceny obchodních smluv.  
28. V **Podokně akcí** klikněte na **Řádky**.
29. V poli **Typ kódu strany** vyberte „Skupina“.
30. V poli **Výběr účtu** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
31. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Tím dokončíte propojení kanálu se skupinou cen pro obchodní smlouvu.  
32. Zadejte hodnotu do pole **Vztah položky**.
33. Zadejte číslo do pole **Částka v měně**.
34. Na záložce s náhledem **Podrobnosti** zaškrtněte nebo zrušte zaškrtnutí políčka **Najít další**. Pokud možnost **Najít další** je nastavena na hodnotu „Ano“, bude oceňovací modul dále hledat použitelné obchodní smlouvy s nižší prodejní cenou. Pokud je možnost **Najít další** nastavena na hodnotu „Ne“, oceňovací modul zastaví hledání a použije obchodní smlouvu.  
35. Klikněte na možnost **Zaúčtovat**.
36. Klikněte na tlačítko **OK**.
37. Zavřete stránku.
38. V **podokně akcí** klikněte na možnost Prodej.
39. Klikněte na možnost **Prodejní cena**.


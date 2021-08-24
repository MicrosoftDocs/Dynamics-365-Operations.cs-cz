---
title: Vytvoření záznamu deníku pomocí šablony
description: Zaúčtované deníky lze uložit jako šablony dokladů a použít v novém dokladu deníku.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c015bbba6784f511ac51802ea005d2114e703861370e33350cff62b6005d630c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730523"
---
# <a name="create-a-journal-entry-using-template"></a>Vytvoření záznamu deníku pomocí šablony

[!include [banner](../../includes/banner.md)]

Zaúčtované deníky lze uložit jako šablony dokladů a použít v novém dokladu deníku. Tato procedura používá ukázkovou společnost USMF.

1. Přejděte na **Navigační podokno > Moduly > Hlavní kniha > Položky deníku > Hlavní deníky**.
2. V **podokně akcí** klikněte na možnost **Nový**. Tento postup se spustí vytvořením a zaúčtováním dokladu deníku, ale ne všechny dříve zaúčtované doklady deníku lze uložit jako šablonu.  
3. V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klikněte na možnost **Řádky**.
7. Zadejte hodnotu do pole **Typ účtu**.
8. Zadejte hodnotu do pole **Popis**.
9. Zadejte hodnotu do pole **Má dáti**.
10. Klepněte na možnost **Nový**.
11. Zadejte hodnotu do pole **Typ účtu**.
12. Zadejte hodnotu do pole **Popis**.
13. Zadejte hodnotu do pole **Má dáti**.
14. Klepněte na možnost **Nový**.
14. Zadejte požadované hodnoty do pole **Účet**.
15. Zadejte hodnotu do pole **Popis**.
16. V poli **Dal** zadejte hodnotu pro vyrovnání dokladu.
17. V **podokně akcí** klikněte na **Zaúčtovat**.
18. Klikněte na **Funkce**.
19. Klikněte na šablonu **Uložit doklad**.
20. Tento postup předpokládá, že je typ šablony **Procento**. Klepněte na tlačítko OK.
    - Procento: částky v dokladu jsou převedeny na procentuální faktory, což umožní při výběru šablony dokladu použít jakoukoli částku.
    - Částka: skutečné částky, které budou uloženy a použity.  
21. Klikněte na **Hlavní deníky**.
22. Klepněte na možnost **Nový**.
23. V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
24. Klikněte na odkaz na vybraném řádku v seznamu.
25. Klikněte na možnost **Řádky**.
26. Klikněte na **Funkce**.
27. Klikněte na **Vybrat šablonu dokladu**.
28. Vyberte šablonu, kterou jste vytvořili dříve. Klikněte na tlačítko **OK**. Může být nutné kliknout na **předchozí krok** a poté vybrat správnou šablonu, pokud existují další šablony.  
29. V poli **Částka** zadejte částku, kterou chcete použít pro doklad. Pole **Částka** se zobrazí pouze pokud je typ šablony dokladu Procento.  
30. Klikněte na tlačítko **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
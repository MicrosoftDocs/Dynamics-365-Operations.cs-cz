--- 
title: "Vytvoření posloupnosti upomínek"
description: "Tento průvodce úkolem slouží k vytvoření posloupnosti upomínek."
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6331c3680169b305c4bfbfada4ba106b619be092
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-collection-letter-sequence"></a>Vytvoření posloupnosti upomínek

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem slouží k vytvoření posloupnosti upomínek. Tento úkol používá ukázkovou společnost USMF.

1. Přejděte na Úvěry a inkasa > Nastavení > Nastavit pořadí upomínek.
2. Klikněte na položku Nová.
3. V poli Posloupnost upomínek zadejte ID posloupnosti, které bude představovat číselnou řadu. Použije se při nastavování profilu zaúčtování.
4. Zadejte nějakou hodnotu do pole Popis.
    * Platební podmínky jsou volitelné. Pokud zde zadáte hodnotu, faktura upomínky na poplatek bude používat platební podmínky namísto podmínek platby, které jsou uloženy pro odběratele.  
5. V poli s kódem kolekce upomínky vyberte kód pro první upomínku, kterou chcete odeslat.
    * První upomínka se vytvoří podle data splatnosti na faktuře, hodnoty zadané pro období odkladu v poli Dny na tomto řádku a dalších informací, které zadáte do tohoto řádku.  
6. Zadejte nějakou hodnotu do pole Popis.
    * Měna poplatku je výchozí měnou odběratele. Kód měny může být jiný, než jaká je měna faktury.  
7. Kliknutím na tlačítko Přidat přidejte následující upomínku, která se odešle v řadě
    * V mnoha případech první upomínka je pouze upozornění. V případě potřeby můžete přidat poplatky.  
8. V poli s kódem kolekce upomínky vyberte další upomínku, kterou chcete odeslat v posloupnosti.
9. Zadejte hodnotu do pole Popis.
10. V poli hlavního účtu vyberte účet výnosů, který bude použit pro poplatky.
11. Zadejte poplatek, který bude účtován po zaúčtování této upomínky.
12. V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyberte skupinu DPH položky, pokud DPH musí být vypočítáno u poplatku.  
13. Klikněte na odkaz na vybraném řádku v seznamu.
14. Zadejte minimální zůstatek po datu splatnosti požadovaný před odesláním upomínky.
15. Zadejte počet dnů odkladu, které povolíte.
    * Toto je počet dnů po datu splatnosti, ve které mohou být generovány upomínky. Datum splatnosti použité pro výpočet závisí na pozici upomínky v posloupnosti upomínek:   ⦁   Období odkladu pro upomínku 1 je relativní k datu splatnosti faktury.  ⦁ Období odkladu pro upomínky 2 a výše vychází z data zaúčtování nebo tisku upomínky, v závislosti na výběru v poli Aktualizovat kód upomínky na stránce Parametry pohledávek.  
16. Kliknutím na tlačítko Přidat přidejte poslední upomínku v řadě.
    * Pro posloupnost upomínek můžete přidat až pět kódů upomínek.  
17. V poli s kódem kolekce upomínky vyberte další upomínku, kterou chcete odeslat v posloupnosti.
18. Zadejte hodnotu do pole Popis.
19. Zadejte požadované hodnoty do pole Hlavní účet.
20. Zadejte číslo do pole Poplatek v měně.
21. V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
22. Klikněte na odkaz na vybraném řádku v seznamu.
23. V poli Minimální zůstatek po datu splatnosti zadejte číslo.
24. Zadejte číslo do pole Dny.
25. Zaškrtnutím tohoto políčka se zablokují další dodávky a fakturace pro odběratele.
    * Pro odblokování účtu vyberte možnost Ne v poli Fakturace a dodávka na stránce Odběratelé.  
26. Rozbalte pevnou záložku Poznámka.
27. Zadejte text, který se má zobrazit v upomínce pro vybraný kód upomínky.
    * Tento text lze přeložit do několika jazyků pomocí nabídky Překlady nad polem.  



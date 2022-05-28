---
title: Vytvoření posloupnosti upomínek
description: Tato procedura slouží k vytvoření posloupnosti upomínek.
author: JodiChristiansen
ms.date: 12/07/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af5d0a001fbe705834e116516933be67f2de8826
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734151"
---
# <a name="create-a-collection-letter-sequence"></a>Vytvoření posloupnosti upomínek

[!include [banner](../../includes/banner.md)]

Tato procedura slouží k vytvoření posloupnosti upomínek. Tento úkol využívá ukázkovou společnost USMF.

1. Přejděte na **Úvěry a inkasa > Nastavení > Nastavit pořadí upomínek**.
2. Klepněte na možnost **Nový**.
3. V poli **Posloupnost upomínek** zadejte ID posloupnosti, které bude představovat číselnou řadu. Použije se při nastavování profilu zaúčtování.
4. Zadejte hodnotu do pole **Popis**. Platební podmínky jsou volitelné. Pokud zde zadáte hodnotu, faktura upomínky na poplatek bude používat platební podmínky namísto podmínek platby, které jsou uloženy pro odběratele.  
5. V poli **Kód upomínky inkasa** vyberte kód pro první upomínku, kterou chcete odeslat. První upomínka se vytvoří podle data splatnosti na faktuře, hodnoty zadané pro období odkladu v poli Dny na tomto řádku a dalších informací, které zadáte do tohoto řádku.  
6. Zadejte hodnotu do pole **Popis**. 
7. Výchozí měnou poplatku je měna právnické osoby. Kód měny může být jiný, než jaká je měna faktury.   
8. Kliknutím na tlačítko **Přidat** přidejte následující upomínku, která se odešle v řadě V mnoha případech první upomínka je pouze upozornění. V případě potřeby můžete přidat poplatky.  
9. V poli **Kód upomínky kolekce** vyberte další upomínku, kterou chcete odeslat v posloupnosti.
10. V poli **Hlavní účet** vyberte účet výnosů, který bude použit pro poplatky.
11. Zadejte poplatek, který bude účtován po zaúčtování této upomínky.
12. V poli **Skupina DPH zboží** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání. Vyberte skupinu DPH položky, pokud DPH musí být vypočítáno u poplatku.  
13. Klikněte na odkaz na vybraném řádku v seznamu.
14. Do pole **Minimální zůstatek po splatnosti** zadejte minimální zůstatek, který je požadován před odesláním upomínky.
15. Do pole **Počet dnů** zadejte počet dnů odkladu, které povolíte. Toto je počet dnů po datu splatnosti, ve které mohou být generovány upomínky. Datum splatnosti použité pro výpočet závisí na pozici upomínky v posloupnosti upomínek:
    - Období odkladu pro upomínku 1 je relativní vzhledem k datu splatnosti faktury.
    - Období odkladu pro upomínky 2 a výše vychází z data zaúčtování nebo tisku upomínky, v závislosti na výběru v poli Aktualizovat kód upomínky na stránce Parametry pohledávek.  
16. Kliknutím na tlačítko **Přidat** přidejte poslední upomínku v řadě. Pro posloupnost upomínek můžete přidat až pět kódů upomínek.  
17. V poli **Kód upomínky kolekce** vyberte další upomínku, kterou chcete odeslat v posloupnosti.
18. Zadejte hodnotu do pole **Popis**.
19. Zadejte požadované hodnoty do pole **Hlavní účet**.
20. Zadejte číslo do pole **Poplatek v měně**.
21. V poli **Skupina DPH zboží** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
22. Klikněte na odkaz na vybraném řádku v seznamu.
23. V poli **Minimální zůstatek po datu splatnosti** zadejte číslo.
24. Zadejte číslo do pole **Dny**.
25. Zaškrtnutím políčka **Blok** se zablokují další dodávky a fakturace pro odběratele. Pro odblokování účtu vyberte možnost **Ne** v poli **Fakturace a dodávka** na stránce **Odběratelé**.  
26. Rozbalte pevnou záložku **Poznámka**.
27. Zadejte text, který se má zobrazit v upomínce pro vybraný kód upomínky. Tento text lze přeložit do několika jazyků pomocí nabídky **Překlady** nad polem.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: " Definování věrnostních schémat"
description: Tato procedura vás provede definování věrnostního schématu.
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 362d6cf877c484c438641980d109b3bed4464b68
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564663"
---
# <a name="define-loyalty-schemes"></a> Definování věrnostních schémat

[!include [task guide banner](../includes/task-guide-banner.md)]

Tato procedura vás provede definování věrnostního schématu. Věrnostní schémata jsou pravidla pro získání odměny a jejich uplatnění v rámci věrnostního programu. Tato procedura používá data ukázkové společnosti USRT.

1. Přejděte na Maloobchodní a velkoobchodní prodej > Odběratelé > Věrnost > Věrnostní schémata.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID schématu.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Můžete mít více věrnostních schémat pro věrnostní program. Věrnostní schémata mohou být pro všechny kanály nebo pouze dílčí sadu kanálů.  
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Klepněte na tlačítko Uložit.
9. Klikněte na položku Přidat řádek.
10. Vyberte možnost v poli Typ aktivity.
    * Vyberte Zakoupit produkty podle částky, pokud chcete odběratelům přidělovat odměny, které jsou založené na způsobu jejich útraty. Vyberte Zakoupit produkty podle množství, pokud chcete odběratelům přidělovat odměny, které jsou založené na zakoupeném množství.  Počet prodejních transakcí, chcete-li odběratelům umožnit získávat odměny za každou prodejní transakci bez ohledu na to, co nebo jak moc je nakoupeno.  
    * Vyberte kategorii. Kategorie omezí, na které produkty se toto pravidlo příjmů bude vztahovat.  
    * Chcete-li použít pravidlo přidělení pro všechny produkty, ponechte toto pole prázdné.  
11. V poli Částka/množství aktivity zadejte číslo.
    *  Pro typ aktivity Počet prodejních transakcí bude nejlepší vždy použít hodnotu 1,0. Pro typy aktivity typu Nákup podle částky nebo Nákup podle množství všechny transakce nižší než zadaná hodnota nespustí pravidlo pro získání. Například pokud je daný typ aktivity Nákup podle částky a zadáte hodnotu „10,00“, tak prodejní transakce „9,00“ u tohoto pravidla nezíská odměnu.  
12. Zadejte hodnotu do pole Měna aktivity.
13. V poli ID bodu odměny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
14. Klikněte na odkaz na vybraném řádku v seznamu.
15. V poli Body odměny zadejte číslo.
    * Body odměny typu částky budou zaznamenávat získané částky s desetinnými místy. Například pokud pravidlo příjmů uvádí získaní 1 bodu odměny za každý 1 utracený kanadský dolar a odběratel utratí 1,25 dolaru, pak odběratel získá 1,25 bodu odměny. Body odměny typu množství budou zaznamenávat získané částky jako celá čísla. Například pokud pravidlo příjmů uvádí získaní 1 bodu odměny za každý 1 utracený kanadský dolar a odběratel utratí 1,25 dolaru, pak odběratel získá 1,0 bodu odměny.  
16. Klikněte na položku Uložit.
17. Klikněte na položku Přidat řádek.
    * Pravidla uplatnění se používají při uplatnění věrnostního způsobu platby.  
18. V poli ID bodu odměny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Zobrazí se pouze uplatnitelné body odměny.  
19. Klikněte na odkaz na vybraném řádku v seznamu.
20. V poli Body odměny zadejte číslo.
21. V poli Typ využití vyberte možnost.
    * Výběrem Platba podle částky určíte, že pole Částka nebo množství bude považováno za hodnotu měny. V takovém případě je množství bodů odměny použitých na jednotku měny platby pevný poměr. Výběrem Platba podle množství určíte, že pole Částka nebo množství bude považováno za hodnotu množství. V tomto případě je množství bodů odměny použité pro množství zboží pevným poměrem, zatímco částka v měně se může lišit, pokud cena zaplaceného zboží pomocí bodů věrnostních odměn pro stejné množství se liší. Typ využití slev za věrnostní body je platný pouze pokud je povolen konfigurační klíče specifických funkcí pro zemi/oblast Rusko a funkční profily POS mají kód ISO „RU“.  
    * Vyberte kategorii. Kategorie omezí, na které produkty se toto pravidlo uplatnění bude vztahovat.  
    * Chcete-li použít pravidlo uplatnění pro všechny produkty, ponechte toto pole prázdné.  
22. V poli Množství nebo částka zadejte číslo.
23. Zadejte hodnotu do pole Měna.
24. Klikněte na položku Uložit.
25. Klikněte na položku Přidat řádek.
    * Vyberte jeden nebo více uzlů ze seznamu Dostupné organizační uzly a přesuňte je na seznam Vybrané organizační uzly kliknutím na šipku mezi dvěma seznamy.  
26. Klikněte na tlačítko OK.
27. Klikněte na položku Uložit.
    * Kdykoli změníte kanály pro věrnostní schéma, musíte zahájit akci Zpracovat věrnostní schémata. Tímto způsobem budou kanály aktualizovány pomocí věrnostních schémat.  


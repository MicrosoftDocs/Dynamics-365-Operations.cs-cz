--- 
title: "Vytvoření nákupní smlouvy"
description: "Tento postup vám pomůže vytvořit nákupní smlouvu."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0d0cc6508071bea3f622bc21f06aa55d2b757b6f
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-agreement"></a>Vytvoření nákupní smlouvy

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup vám pomůže vytvořit nákupní smlouvu. Toto by obvykle prováděl vedoucí nákupu. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Než začnete, je třeba nastavit klasifikace nákupní smlouvy. Vytvořenou smlouvu můžete použít při vytváření nákupní objednávky; tím se zkopírují podmínky nákupní smlouvy do záhlaví a jakýchkoli řádků objednávky ovlivněných touto smlouvou.


## <a name="create-a-new-purchase-agreement"></a>Vytvoření nové nákupní smlouvy
1. Přejděte do nabídky Zásobování a zdroje > Nákupní smlouvy > Nákupní smlouvy.
2. Klikněte na položku Nová.
3. V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. V poli Klasifikace nákupní smlouvy kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Rozbalte sekci Obecné.
10. Do pole Datum vypršení platnosti zadejte datum.
    * Toto datum vypršení platnosti bude výchozí pro všechny řádky závazků a určí, jak dlouho budou jednotlivé závazky platné.  
11. V poli Název dokumentu zadejte název nákupní smlouvy.
    * Ponechejte pole Výchozí závazek nastavené na hodnotu Závazek – množství produktu (nebo pokud je nastavená jiná hodnota, změňte ji).  
    * Výchozí hodnota závazku určuje možnosti na řádcích smlouvy. Pokud potřebujete nový typ závazku při vytváření řádků smlouvy, je nutné změnit výchozí závazek v záhlaví.  Jsou k dispozici 4 typy závazků: „Závazek – množství produktu“ pro určité množství produktu; „Závazek – hodnota produktu“ pro konkrétní částku měny pro produkt; „Závazek – hodnota kategorie produktu“ pro konkrétní částku měny v kategorii zásobování, kde částka může být pro katalogovou položku nebo nekatalogovou položku; „Závazek ohledně hodnoty“ pro konkrétní částku měny, která může být splněna jakýmkoli produktem nebo jakoukoli kategorií zásobování.  
12. Klikněte na tlačítko OK.

## <a name="add-a-commitment"></a>Přidání závazku
1. Klikněte na položku Přidat řádek.
2. Označte v seznamu vybraný řádek.
3. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyberte produkt, pro který chcete přidat závazek.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Zadejte číslo do pole Množství.
    * Toto je celkového množství, které podle dohody zakoupíte od dodavatele.  
7. Zadejte číslo do pole Jednotková cena.
8. Rozbalte sekci Podrobnosti řádku.
9. Nastavte možnost Max je vynuceno na hodnotu Ano.
    * Možnost Max je vynuceno omezuje použití závazku. Můžete produkt zakoupit pouze do množství zadaného v poli Množství pro daný řádek.  
10. Sbalte oddíl Podrobnosti řádku.

## <a name="add-header-conditions"></a>Přidání podmínek záhlaví
1. V podokně akcí klikněte na Možnosti.
2. Klikněte na tlačítko Změnit zobrazení.
3. Klikněte na možnost Zobrazení záhlaví.
4. Rozbalte část Podmínky.
5. V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Zde jsou ve výchozím nastavení zobrazené platební podmínky z účtu dodavatele.       
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. V poli Způsob dodání kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Klikněte na odkaz na vybraném řádku v seznamu.
10. V poli Dodací podmínky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="confirm-and-activate-the-agreement"></a>Potvrzení a aktivace smlouvy
1. V podokně akcí klikněte na možnost Nákupní smlouva.
2. Klikněte na možnost Potvrzení.
    * Nastavte možnost Označit smlouvu jako platnou na hodnotu Ano.  
3. Klepněte na tlačítko OK.
4. V podokně akcí klikněte na možnost Nákupní smlouva.
5. Klikněte na možnost Potvrzení nákupní smlouvy.
    * Možnost Náhled/tisk umožňuje generovat dokument pro nákupní smlouvu, který pak můžete vytisknout nebo odeslat dodavateli. Pokud smlouvu aktualizujete a znovu potvrdíte později, zobrazí se zde obě verze.  
6. Zavřete stránku.



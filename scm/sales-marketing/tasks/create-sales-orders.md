--- 
title: "Vytvářet prodejní objednávky"
description: "Tato procedura popisuje způsob vytváření prodejní zakázky."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 62276765e1cc76b2328a7b5b57bd18593d93e4ab
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-orders"></a>Vytvářet prodejní objednávky

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje způsob vytváření prodejní zakázky. Tento postup můžete projít v ukázkových datech společnosti USMF. Prodejní objednávku obvykle vytváří zpracovatel prodejních objednávek. 




## <a name="enter-sales-order-header-details"></a>Zadejte informace ze záhlaví prodejní objednávky
1. Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu záznam odběratele a vyberte ho.
    * V tomto příkladu vyberte číslo odběratele US-004.  
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klikněte na tlačítko OK.

## <a name="enter-sales-order-line-details"></a>Zadejte informace z řádků prodejní objednávky
    * Produkty prodané vaší organizací mohou nabízet více variant rozlišených podle dimenzí, jako je například konfigurace, barva, velikost a styl. Dále produkty lze nastavit tak, aby používaly dimenze uskladnění, jako je například pracoviště, sklad a palety, a sledovací dimenze, jako například dávky nebo sériové číslo. Když jsou tyto dimenze přiřazeny, je nutné vybrat hodnoty pro tyto dimenze na řádku objednávky. Ke zvýšení efektivity zadání objednávky můžete přidat odpovídající pole dimenze do mřížky objednávky.  
1. Klikněte na položku Řádek prodejní objednávky.
2. Klikněte na Dimenze.
    * V tomto příkladu vyberte Barva, Pracoviště a Sklad. Zde zvolené dimenze se zobrazí v mřížce prodejní objednávky. Podle potřeby můžete svůj výběr uchovávat tím, že nastavíte možnost Uložit nastavení na hodnotu Ano.   
3. Klikněte na tlačítko OK.
4. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. V tomto příkladu vyberte číslo položky T0004.
6. Klikněte na odkaz na vybraném řádku v seznamu.
    * Pokud je položka součástí kategorie prodeje, název položky se automaticky zobrazí v poli Prodejní kategorie.  
    * Pokud pole s dimenzí produktu již obsahuje hodnotu, je to proto, že hodnota byla zkopírována ze záznamu produktu, kde je definována jako výchozí dimenze produktu. Výchozí hodnotu lze kdykoli změnit.   
7. V poli Barva kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
8. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
9. Klikněte na odkaz na vybraném řádku v seznamu.
10. Zadejte číslo do pole Množství.
    * Pokud je jednotka prodána v odlišných jednotkách, než ve kterých byla zakoupena, vyrobena a uložena, a měrná jednotka prodeje je nastavena na záznam produktu, tato hodnota se zobrazí v poli Jednotka. Hodnotu lze kdykoli změnit.   
    * Pokud pole Pracoviště již obsahuje hodnotu, hodnota byla zkopírována ze záhlaví objednávky nebo z nastavení objednávky, která je přidružena k produktu. Hodnotu lze kdykoli změnit. Pokud je pole prázdné, vyberte hodnotu.   
    * Pokud pole Cena jednotky již obsahuje hodnotu, hodnota byla zkopírována z platné obchodní smlouvy nebo ze záznamu produktu. (Jednotková cena může také pocházet z prodejní smlouvy, ale proces vytváření prodejních objednávek z prodejních smluv se liší od toho, který je zobrazen zde.) Pokud je pole prázdné, zadejte hodnotu.   
    * Pole Sleva obsahuje částku slevy za každou jednotku produktu. Pokud chcete vypočítat celkovou řádkovou slevu, hodnota slevy bude vynásobena množstvím na řádku.    Pokud pole Sleva jednotky již obsahuje hodnotu, hodnota byla zkopírována z platné obchodní smlouvy. Pokud je pole prázdné a vy chcete přiřadit odběrateli řádkovou slevu, můžete zadat hodnotu.  
    * Pole Procento slevy obsahuje procentuální hodnotu, o kterou má být snížena celková hrubá částka na řádku.  Pokud pole Procento slevy již obsahuje hodnotu, hodnota byla zkopírována z platné obchodní smlouvy. Pokud je pole prázdné a vy chcete přiřadit odběrateli řádkovou slevu, můžete zadat hodnotu.  
    * Pole Čistá částka obsahuje hodnotu, která se vypočte podle množství a jednotkové ceny na řádku, upravenou o slevu.  Je možné přepsat vypočtené hodnoty na jiné.  

## <a name="review-the-order-totals"></a>Kontrola součtů objednávky
1. V podokně akcí klikněte na položku Prodejní objednávka.
2. Klikněte na položku Součty.
    * Stránka Součty zobrazí podrobnosti o celé objednávce. Jedná se o mezisoučtu částkou, která představuje součet všech čistých částek na řádku upravených pro případné řádkové slevy, celkovou částku faktury, která tvoří mezisoučet upravený pro případnou slevu na úrovni objednávky, náklady, DPH, situaci limitního úvěru zákazníka apod.  Částka faktury je částka, která se zobrazí na dokladu pro fakturu odběratele.  
3. Klikněte na tlačítko OK.



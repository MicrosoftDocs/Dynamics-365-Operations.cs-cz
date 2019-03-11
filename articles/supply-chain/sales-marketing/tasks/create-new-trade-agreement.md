---
title: Vytvoření nové obchodní smlouvy
description: Tento postup popisuje vytvoření obchodní dohody, u které zaregistrujete novou prodejní cenu produktu odsouhlasenou se specifickým odběratelem.
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "323495"
---
# <a name="create-a-new-trade-agreement"></a>Vytvoření nové obchodní smlouvy

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje vytvoření obchodní dohody, u které zaregistrujete novou prodejní cenu produktu odsouhlasenou se specifickým odběratelem. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Při použití vlastních dat před zahájením tohoto průvodce ověřte, že existuje název deníku obchodních smluv, kde je výchozí vztah je nastaven na „Cena (prodej)“.


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Vytvoření a zaúčtování nového deníku obchodní smlouvy
1. Přejděte do nabídky Prodej a marketing > Ceny a slevy > Deníky obchodních smluv.
2. Klikněte na položku Nová.
3. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klikněte na položku Řádky.
7. V poli Kód účtu vyberte možnost Tabulka.
    * V tomto příkladu aktualizujete cenu pro určitého odběratele, což znamená, že je nutné vybrat tabulku. Pokud byste aktualizovali katalogovou cenu produktu, vybrali byste Vše, aby nová cena platila pro všechny odběratele. Pokud byste používali různé ceny v různých segmentech odběratelů, vybrali byste možnost Skupina. Chcete-li vybrat skupinu, musíte nastavit možnost Cenové skupiny odběratele.  
8. V poli Výběr účtu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. V poli Kód položky vyberte položku Tabulka.
    * Při zadávání typu obchodní smlouvy Cena (prodej) je nutné vybrat pouze „Tabulka“ v poli Kód položky. Důvodem je skutečnost, že cena je absolutní hodnota a nesmí být stejná pro všechny produkty nebo skupinu produktů.  
11. V poli Vztah položky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
12. V seznamu vyberte produkt, který chcete do smlouvy zahrnout.
    * Poznamenejte produkt, který jste vybrali.  
13. Klikněte na odkaz na vybraném řádku v seznamu.
14. Zadejte minimální množství do pole Od.
    * Pokud odběratel musí objednávat minimální množství, je třeba zde zadat množství, jinak nebude mít na novou cenu nárok.  
    * Zadáním hodnoty do pole Do určete maximální množství, nad které nebude cena ve smlouvě platit. Pokud nabízíte ceny a slevy založené na několika množstevních kategoriích, zadejte každou množstevní kategorii jako pár minimálního a maximálního množství do polí Od a Do.  
15. Zadejte cenu do pole Částka v měně.
16. V poli Od data zadejte datum, od kterého bude tato smlouva platit.
17. Klikněte na položku Uložit.
18. Klikněte na tlačítko Ověřit.
19. Klikněte na možnost Ověřit vybrané řádky.
20. Klikněte na tlačítko OK.
21. Klikněte na položku Zaúčtovat.
22. Klikněte na tlačítko OK.

## <a name="view-trade-agreements-for-a-product"></a>Zobrazení obchodních smluv pro produkt
1. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
2. V seznamu najděte a vyberte produkt, jehož cenu jste právě aktualizovali.
3. V podokně akcí klikněte na možnost Prodej.
4. Klikněte na možnost Zobrazit obchodní smlouvy.
    * Zkontrolujte podrobnosti obchodní smlouvy o cenách, kterou jste právě vytvořili.    
5. Zavřete stránku.

## <a name="additional-resources"></a>Další prostředky
### <a name="community-blogs"></a>Blogy komunity
- [Prodejní ceny v Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)

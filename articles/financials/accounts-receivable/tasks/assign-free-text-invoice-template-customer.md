--- 
title: "Přiřazení šablony volné faktury odběrateli"
description: "Tato úloha demonstruje způsob, jak přiřadit šablonu volné faktury pro odběratele."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3bcb59c6edd04877dc2a052002be513205ae840a
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Přiřazení šablony volné faktury odběrateli

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato úloha demonstruje způsob, jak přiřadit šablonu volné faktury pro odběratele. Tento úkol využívá ukázkovou společnost USMF a je určen pro uživatele, který je odpovědný za správu a zpracování faktur pohledávek.

1. Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. V podokně akcí klikněte na položku Faktura.
4. Klikněte na Opakované faktury.
    * Na této stránce můžete přiřadit šablony volných faktur k odběratelům a určit, jak často faktury budou odesílány odběrateli.  
5. Klikněte na možnost Nový a přiřaďte tak novou šablonu k odběrateli.
6. Vybrat šablonu volné faktury, kterou chcete přiřadit odběrateli.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Zadejte datum, kdy bude vygenerována první faktura.
    * Zadejte koncové datum opakování.  
    * Vyberte jednu z následujících možností: Bez koncového data – faktury budou generovány neomezeně dlouho, dokud šablony nebude odebrána z účtu odběratele.  Koncové datum fakturace – Vyberte tuto možnost a zadejte poslední datum, kdy lze fakturu generovat.  
    * Maximální kumulativní částka, po které se zastaví generování faktury.  
    * Zadejte maximální kumulativní částku, které lze dosáhnout pomocí vybrané šablony. Například zadáte-li 1 000,00 a necháte vygenerovat měsíční faktury vždy pro 100,00, faktury zastaví generování po vygenerování desáté faktury.  
    * Vygenerujte opakované faktury pomocí výchozích hodnot ze šablony volné faktury nebo účtu odběratele.  
    * Vyberte, zda chcete při vytvoření faktury k určení výchozích hodnot pro jazyk, účetní profil, skupinu DPH, skupinu DPH položky, kód seznamu, zemi/oblast pro dodávku, měnu, platební podmínky, způsob platby, specifikaci plateb, platební kalendář, platební slevu, finanční dimenze a převodní poukázku žira využít šablonu volné faktury nebo účet odběratele.  
10. Vyberte způsob opakování.
    * Denně – Vyberte tuto možnost a zadejte počet dní do pole Za. Například pokud zadáte 15, faktura bude pro tohoto odběratele vygenerována každých 15 dnů.  Týdně – Vyberte tuto možnost a zadejte počet týdnů do pole Za. Například pokud zadáte 2, faktura bude pro tohoto odběratele vygenerována každé dva týdny.  Měsíčně – Vyberte tuto možnost a zadejte počet měsíců do pole Za. Například pokud zadáte 6, faktura bude pro tohoto odběratele vygenerována každých šest měsíců.  Ročně – Vyberte tuto možnost a zadejte počet roků do pole Za. Například pokud zadáte 2, faktura bude pro tohoto odběratele vygenerována každé dva roky.  
11. Do pole Za zadejte číslo.



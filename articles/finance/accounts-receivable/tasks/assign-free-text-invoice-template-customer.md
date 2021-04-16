---
title: Přiřazení šablony volné faktury odběrateli
description: Tato úloha demonstruje způsob, jak přiřadit šablonu volné faktury pro odběratele.
author: ShivamPandey-msft
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0219521867d1cfb1fa4edcdf20dd70eea8a3d0e1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819883"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Přiřazení šablony volné faktury odběrateli

[!include [banner](../../includes/banner.md)]

Tato úloha demonstruje způsob, jak přiřadit šablonu volné faktury pro odběratele. Tento úkol využívá ukázkovou společnost USMF a je určen pro uživatele, který je odpovědný za správu a zpracování faktur pohledávek.

1. V **navigační podokně** přejděte na **Moduly > Pohledávky > Odběratelé > Všichni odběratelé**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. V **podokně akcí** klikněte na **Faktura**.
4. Klikněte na **Opakované faktury**. Na této stránce můžete přiřadit šablony volných faktur k odběratelům a určit, jak často faktury budou odesílány odběrateli.  
5. Klikněte na možnost **Nová** a přiřaďte tak novou šablonu k odběrateli.
6. V poli **Šablona** vyberte šablonu volné faktury, kterou chcete přiřadit odběrateli.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Do pole **Počáteční datum fakturace** zadejte datum, kdy bude vygenerována první faktura.
10. V části **Konec opakování** zadejte koncové datum opakování.  
    * Vyberte jednu z následujících možností: Bez koncového data – faktury budou generovány neomezeně dlouho, dokud šablony nebude odebrána z účtu odběratele.
    * Koncové datum fakturace – Vyberte tuto možnost a zadejte poslední datum, kdy lze fakturu generovat.  
11. Do pole **Maximální kumulativní částka** zadejte maximální kumulativní částku, po jejímž uplynutí se generování faktury zastaví. Zadejte maximální kumulativní částku, které lze dosáhnout pomocí vybrané šablony. Například zadáte-li 1 000,00 a necháte vygenerovat měsíční faktury vždy pro 100,00, faktury zastaví generování po vygenerování desáté faktury.  
12. V části **Generováníe opakované faktury pomocí výchozích hodnot z** zvolte buď šablonu volné faktury nebo účtu odběratele. Vyberte, zda chcete při vytvoření faktury k určení výchozích hodnot pro jazyk, účetní profil, skupinu DPH, skupinu DPH položky, kód seznamu, zemi/oblast pro dodávku, měnu, platební podmínky, způsob platby, specifikaci plateb, platební kalendář, platební slevu, finanční dimenze a převodní poukázku žira využít šablonu volné faktury nebo účet odběratele.  
13. V poli **Způsob opakování** vyberte způsob opakování.
    + Denně – Vyberte tuto možnost a zadejte počet dní do pole Za. Například pokud zadáte 15, faktura bude pro tohoto odběratele vygenerována každých 15 dnů.
    + Týdně – Vyberte tuto možnost a zadejte počet týdnů do pole Za. Například pokud zadáte 2, faktura bude pro tohoto odběratele vygenerována každé dva týdny.
    + Měsíčně – Vyberte tuto možnost a zadejte počet měsíců do pole Za. Například pokud zadáte 6, faktura bude pro tohoto odběratele vygenerována každých šest měsíců.
    + Ročně – Vyberte tuto možnost a zadejte počet roků do pole Za. Například pokud zadáte 2, faktura bude pro tohoto odběratele vygenerována každé dva roky.  
14. Do pole **Za** zadejte číslo.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
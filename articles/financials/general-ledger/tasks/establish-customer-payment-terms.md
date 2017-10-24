--- 
title: "Stanovení platebních podmínek odběratele"
description: "Tento postup definuje platební slevu a nastavení data splatnosti."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e0e43962bea3ff1c3adafa73da4ce3862963a51
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-payment-terms"></a>Stanovení platebních podmínek odběratele

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup definuje platební slevu a nastavení data splatnosti. Tento průvodce úlohou používá ukázkovou společnost USMF.

1. Přejděte do nabídky Pohledávky > Nastavení platby > Dny platby.
    * Nastavení platebních podmínek je sdíleno pro pohledávky a závazky. Pokud je definujete v jednom modulu, bude k dispozici i ve druhém modulu. Pro tohoto průvodce úkolem jsou nastaveny všechny podmínky platby v části Pohledávky.  
2. Klikněte na položku Nová.
    * Vytvořte den platby, pokud vaše platební podmínky vyžadují určitý den v týdnu (pondělí, úterý atd.) nebo určité datum v měsíci (5., 10. atd.).  
3. V poli Den platby zadejte ID dne platby do pole se dnem platby.
4. Do pole Popis zadejte popis dne platby.
5. V poli Týden/Měsíc vyberte týden nebo měsíc.
    * Pokud chcete zadat den v týdnu, jako je pondělí, vyberte Týden. Pokud chcete zadat datum v měsíci, jako například 10., vyberte Měsíc. V tomto příkladu vyberte možnost Měsíc.  
6. Do pole Den v měsíci zadejte datum a čas.
    * Datum by mělo být zadáno jako číslo, jako například „10“ a nikoli „10.“.  
7. Klikněte na položku Uložit.
8. Zavřete stránku.
9. Přejděte do nabídky Pohledávky > Nastavení platby > Platební podmínky.
10. Klikněte na položku Nová.
    * Podmínky platby lze použít pro definování způsobu výpočtu dat splatnosti. Nastavení data platební slevy je definováno na samostatné stránce.  
11. V poli Platební podmínky zadejte ID do pole Platební podmínky.
12. Zadejte popis do pole Popis.
13. Vyberte způsob platby, jako například platbu na dobírku, netto, aktuální měsíc atd.
    * Způsob platby lze použít pro definování začátku způsobu výpočtu data splatnosti.  Například Netto se používá v případě, že datum splatnosti bude vždy pevný počet měsíců nebo dnů po datu faktury. Platbu na dobírku lze použít v případě, že platba je požadována při fakturaci, takže neproběhne výpočet data splatnosti. Pro tohoto průvodce úkolem vyberte Aktuální měsíc.  
14. Zvolte Den platby, jsou-li určitý den týdne nebo datum zahrnuty do výpočtu.
    * V závislosti na vašich platebních podmínkách můžete zadat množství do pole Měsíce a Dny Nebo můžete použít pole Platební kalendář nebo Platební den a přidat je na konec metody platby. Pokud datum splatnosti bude vždy 10. den dalšího měsíce, vyberte v poli Platební den hodnotu „10“.  
15. Klikněte na položku Uložit.
16. Zavřete stránku.
17. Přejděte do nabídky Pohledávky > Nastavení plateb > Platební slevy.
18. Klikněte na položku Nová.
    * Tato stránka se nepoužívá při definování způsobu výpočtu data platební slevy.  
19. V poli Platební sleva zadejte ID do pole Platební sleva.
20. Zadejte popis do pole Popis.
21. Pokud jsou k dispozici vrstvené platební slevy, vyberte Další kód slevy, který následuje za touto novou platební slevou.
22. Zadejte počet dní, které se používají k výpočtu data platební slevy.
    * Pokud byla vybrána možnost Pravidlo Netto, počet dnů bude přidán k datu faktury pro výpočet data platební slevy.  
23. Zadejte procentuální hodnotu platební slevy.
24. Zadejte hlavního účtu, ke kterému bude platební sleva zaúčtována pro faktury odběratele.
25. V poli Slevové protiúčty vyberte možnost.
    * Pokud vyberete možnost Účty na řádcích faktury, platební sleva se zaúčtuje do stejného hlavního účtu majetku / nákladů na řádky faktury dodavatele. Použít vyberete možnost Použít hlavní účet pro faktury dodavatele, platební slevy se zaúčtují do hlavního účtu, který definujete v části Hlavní účet pro faktury dodavatele. V tomto příkladu vyberte možnost Použít hlavní účet pro faktury dodavatele.  
26. Zadejte hlavního účtu, ke kterému bude platební sleva zaúčtována pro faktury dodavatele.
27. Klikněte na položku Uložit.



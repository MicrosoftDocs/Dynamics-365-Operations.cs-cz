---
title: Stanovení platebních podmínek odběratele
description: Tento postup definuje platební slevu a nastavení data splatnosti.
author: aprilolson
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b2ae5e63a2efb4bc913efa4d88c65a70133a2d9
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752769"
---
# <a name="establish-customer-payment-terms"></a>Stanovení platebních podmínek odběratele

[!include [banner](../../includes/banner.md)]

Tento postup definuje platební slevu a nastavení data splatnosti. Tento průvodce úlohou používá ukázkovou společnost USMF.

1. Přejděte na **Podokno navigace > Moduly > Pohledávky > Nastavení plateb > Dny platby**. Nastavení možností **Platební podmínky** je sdíleno pro **Pohledávky** a **Závazky**. Pokud je definujete v jednom modulu, bude k dispozici i ve druhém modulu. Pro tohoto průvodce záznamem úloh jsou nastaveny všechny podmínky platby v části **Pohledávky**.
2. Klepněte na možnost **Nový**. Vytvořte den platby, pokud vaše platební podmínky vyžadují určitý den v týdnu (pondělí, úterý atd.) nebo určité datum v měsíci (5., 10. atd.). 
3. V poli **Den platby** zadejte ID.
4. Do pole **Popis zadejte** popis dne platby.
5. V poli **Týden/Měsíc** vyberte Týden nebo Měsíc. Pokud chcete zadat den v týdnu, jako je pondělí, vyberte Týden. Pokud chcete zadat datum v měsíci, jako například 10., vyberte Měsíc. V tomto příkladu vyberte možnost Měsíc. 
6. Do pole **Den v měsíci** zadejte datum a čas. Datum by mělo být zadáno jako číslo, jako například „10“ a nikoli „10.“. 
7. Klikněte na možnost **Uložit**.
8. Zavřete stránku.
9. Přejděte na **Podokno navigace > Moduly > Pohledávky > Nastavení plateb > Platební podmínky**. 

>[!NOTE] 
>Pokud pro **Platební podmínky** nastavena **Hotovost**, pole **Platba v hotovosti** na stránce **Platební podmínky** musí být **Ne**.

10. Klepněte na možnost **Nový**. **Podmínky platby** lze použít pro definování způsobu výpočtu dat splatnosti. Nastavení data platební slevy je definováno na samostatné stránce. 
11. V poli **Platební podmínky** zadejte ID.
12. Zadejte popis do pole **Popis**.
13. Vyberte **Způsob platby**, například **dobírka**, **netto**, **aktuální měsíc** atd. **Způsob platby** se používá k definování začátku výpočtu splatnosti. Například **Netto** se používá v případě, že datum splatnosti bude vždy pevný počet měsíců nebo dnů po datu faktury. **Platbu na dobírku** lze použít v případě, že platba je požadována při fakturaci, takže neproběhne výpočet data splatnosti. Pro tohoto průvodce záznamem úloh vyberte **Aktuální měsíc**.  
14. Zvolte **Den platby**, jsou-li určitý den týdne nebo datum zahrnuty do výpočtu. V závislosti na vašich platebních podmínkách můžete zadat množství do pole Měsíce a Dny Nebo můžete použít pole Platební kalendář nebo Platební den a přidat je na konec metody platby. Případně můžete použít **Platební kalendář** nebo **Den platby** pro přidání konce **platební metody**. Pokud je den splatnosti 10. příštího měsíce, vyberte v poli **Den platnosti** hodnotu „10“. Pokud používáte **Platební kalendář**, můžete definovat, jak se určí datum splatnosti, když vypočítané datum připadne na nepracovní den. Počáteční datum splatnosti se počítá pomocí kalendářních dnů. Pokud vypočítané datum připadne na nepracovní den, můžete vypočítané datum splatnosti upravit na následující pracovní den nebo dřívější pracovní den.
15. Klikněte na tlačítko **Uložit**.
16. Zavřete stránku.
17. Přejděte do nabídky **Pohledávky > Nastavení plateb > Platební slevy**.
18. Klepněte na možnost **Nový**. Tato stránka se nepoužívá při definování způsobu výpočtu data platební slevy. 
19. V poli **Platební slevy** zadejte ID.
20. Zadejte popis do pole **Popis**.
21. Pokud jsou k dispozici vrstvené platební slevy, vyberte **Další kód slevy**, který následuje za touto novou platební slevou.
22. V poli **Dny** zadejte počet dní, které se používají k výpočtu data platební slevy. Pokud byla vybrána možnost Pravidlo **Netto**, počet dnů bude přidán k datu faktury pro výpočet data platební slevy.  
23. Zadejte procentuální hodnotu platební slevy do pole **Procento slevy**.
24. V **Hlavní účet slev odběratele** zadejte hlavní účet, na který bude platební sleva účtována pro faktury odběratelů.
25. V poli **Slevové protiúčty** vyberte možnost. Pokud vyberete možnost Účty na řádcích faktury, platební sleva se zaúčtuje do stejného hlavního účtu majetku / nákladů na řádky faktury dodavatele. Použít vyberete možnost **Použít hlavní účet pro faktury dodavatele**, platební slevy se zaúčtují do hlavního účtu, který definujete v části **Hlavní účet pro faktury dodavatele**. V tomto příkladu vyberte možnost **Použít hlavní účet pro faktury dodavatele**. 
26. V poli **Hlavní účet slev dodavatele** zadejte hlavní účet, na který bude platební sleva účtována pro faktury dodavatelů.
27. Klikněte na možnost **Uložit**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: "Kontrola dostupnosti zásob"
description: "Tento postup popisuje způsob kontroly množství na skladě a zásob fyzicky k dispozici pro určité číslo položky."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: d103eb52a498e6273b1fdb43fc10dae4133e76b2
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# Kontrola dostupnosti zásob

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob kontroly množství na skladě a zásob fyzicky k dispozici pro určité číslo položky. Také ukazuje, jak získat informace o zásobách související s položkou. Fyzické zásoby na skladě je množství na skladě, které je k dispozici – tedy, je zakoupené, přijaté a registrované. Množství na skladě zahrnuje dostupné zásoby na skladě, ale i zásoby, které byly objednány a jsou očekávané, ale dosud nebyly přijaty nebo registrovány. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat. Pokud používáte USMF, můžete použít ukázkové hodnoty, které jsou zobrazeny. Tyto úkoly obvykle provádějí pracovníci skladu.


## Kontrola zásob na skladě pro konkrétní položku
1. Přejděte na Řízení zásob > Dotazy a sestavy > Zásoby na skladě.
2. Vyberte řádek Číslo položky.
    * Pokud chcete vytvořit dotaz na množství na skladě podle čísla položky, vyberte řádek, kde je Tabulka nastavena na Množství na skladě, a Pole je nastaveno na Číslo položky.  
3. V poli Kritéria vyberte položku, pro kterou chcete vytvořit dotaz.
    * V případě, že používáte ukázková data společnosti USMF, můžete vybrat 'M9201'.  
4. Klepněte na tlačítko OK.
5. Klikněte na Dimenze.
    * Karta Dimenze umožňuje vybrat způsob, jak podrobné údaje chcete zobrazit o množství na skladě. Pokud potřebujete data související s rezervací, musíte zobrazit všechny dimenze zásob pro položky používající procesy rozšířené skladu (řízení skladu).  
6. Klepněte na tlačítko OK.
7. V podokně akcí klikněte na možnost Související informace.
    * Pokud tyto informace vidět nepotřebujete, klikněte na tlačítko se třemi tečkami (...) a otevřete tak další možnosti v podokně.  
8. Klikněte na Přehled dodávek.
    * Karta Přehled dodávek obsahuje informace o zásobách pro určitou položku, jako je například množství na skladě, doba realizace a informace o dodavateli.  
9. Rozbalte sekci Na skladě.
10. Rozbalte sekci Dodavatelé.
11. Zavřete stránku.
12. Zavřete stránku.

## Kontrola fyzického množství na skladě
1. Přejděte na Řízení skladu > Dotazy a sestavy > Fyzické množství na skladě.
2. Zadejte hodnotu do pole Číslo zboží.
    * Chcete-li filtrovat seznam položek, můžete použít pole Pracoviště a Sklad.  
3. Aktualizujte stránku.
4. Klikněte na Zobrazit dimenze.
    * Karta Zobrazit dimenze umožňuje vybrat způsob, jak podrobné údaje chcete zobrazit o množství na skladě.  
5. Klikněte na tlačítko OK.
6. Zavřete stránku.

## Kontrola množství na skladě podle skladového místa
1. Přejděte na Řízení skladu > Dotazy a sestavy > Množství na skladě podle skladového místa.
2. Zadejte hodnotu do pole Sklad.
    * V případě, že používáte ukázková data společnosti USMF, můžete použít „51“.  
3. Aktualizujte stránku.
4. Klikněte na Zobrazit dimenze.
5. Klikněte na tlačítko OK.
6. Zavřete stránku.

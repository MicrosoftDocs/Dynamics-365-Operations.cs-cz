---
title: Fiktivní položky
description: Toto téma popisuje, jakým způsobem lze použít fiktivní typ řádku pro řádky kusovníku a receptury v aplikaci Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5c9768381d35709611e4bec3d2b7793a4d896b34
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713239"
---
# <a name="phantom-items"></a>Fiktivní položky

[!include [banner](../includes/banner.md)]

Toto téma podrobně popisuje, jakým způsobem lze použít fiktivní typ řádku pro řádky kusovníku a receptury.

Na obrázku č. 1 je (a) kusovník pro produkt H a části F a G, a (b) je tabulka postupů pro produkty H a část F.

![Obrázek 1: Strojírenský kusovník.](media/product-H-part-F.png)
*Obrázek 1: Strojírenský kusovník*

Na obrázku č. 1 je uveden příklad struktury kusovníku ve dvou úrovních. Dokončený produkt H představuje produkt pro sestavení stroje. Sestavení stroje se skládá ze dvou částí, z elektrické jednotky (F), která má dva materiály (A a B), a skupiny obalových materiálů (G), která má rovněž dva materiály (C a D). Další materiál (E) se používá při obecném sestavení stroje.

Obrázek č. 1 představuje vývojový kusovník pro produkt H. Tato struktura poskytuje dobrý přehled o součástech a komponentách celkového sestavení stroje. I když návrháři produktu mohou upřednostňovat zobrazení kusovníku tímto způsobem, tato struktura nemusí správně představovat způsob, jakým je stroj sestaven na dílně.

Například vývojový kusovník na obrázku č. 1 označuje, že elektrická jednotka F je sestavena jako samostatná část na samostatné pracovní objednávce. V dílně však mohou usoudit, že je optimálnější sestavit elektrickou jednotku jako součást celkového sestavení stroje, nikoliv jako samostatný pracovní příkaz.

Tento vývojový kusovník také označuje, že část G je samostatná část. V této struktuře však část G nereprezentuje fyzickou část, ale kolekci obalových materiálů.

Proto i když vývojový kusovník poskytuje velkou hodnotu pro návrh produktu a údržbu tohoto návrhu, nemusí se jednat o nejlogičtější způsob podpory proces provádění výroby produktu. Naopak výrobní kusovník představuje nejlepší způsob sestavení produktu.

Obrázek č. 2 znázorňuje, jak je předchozí vývojový kusovník převeden na výrobní kusovník. Na obrázku č. 2 je (a) kusovník pro produkt H a (b) je tabulka postupů pro produkt H.

![Obrázek 2: Výrobní kusovník.](media/product-H-part-B.png)
*Obrázek 2: Výrobní kusovník*

V této struktuře můžete vidět, že neexistuje zmínka o částech F a G, a že materiály, ze kterých se tyto části skládají, byly povýšeny na další úroveň kusovníku.

Na rozdíl od vývojového kusovníku, který měl dva listy operací, výrobní kusovník obsahuje pouze jeden list operací. Operace balení, která byla navázána na část G, byla také povýšena a je nyní součástí listu operací pro produkt H. Sestavení elektrické jednotky je první operace. Tento výrobní příkaz dává smysl, vzhledem k tomu, že tato jednotka se používá v další operace, kterou je sestavení stroje. Poslední operace je operace balení, které spotřebuje dva obalové materiály (C a D).

Přechod mezi vývojovým kusovníkem a výrobním kusovníkem povolen prostřednictvím typu řádku kusovníku Phantom. Jako naznačuje termín „fiktivní“, části F a G během převodu mezi dvěma typy kusovníku zmizely. V tomto příkladu je fiktivní typ řádku použit na řádky kusovníku pro části F a G ve vývojovém kusovníku. Když je vytvořena výrobní zakázka nebo dávková objednávka, je vývojový kusovník zkopírován do výrobní zakázky nebo dávkové objednávky. Když je pak zakázka oceněna, dojde k přechodu z vývojového kusovníku na výrobní kusovník, jak je uvedeno na obrázku č. 2. Z listu operace na obrázku č. 2 jsou obalové materiály C a D vstupem pro operaci.

## <a name="multilevel-phantom-bom-structures"></a>Víceúrovňové struktury fiktivního kusovníku

Typ fiktivního řádku lze použít ve víceúrovňových strukturách kusovníku, jak je uvedeno na obrázku č. 3. Na obrázku č. 3 je (a) kusovník pro produkt G a (b) je tabulka postupů pro části E a F a produkt G.

![Obrázek 3: Strojírenský kusovník, produkt G.](media/product-G.png)
*Obrázek 3: Strojírenský kusovník, produkt G*

Obrázek č. 4 znázorňuje výsledný výrobní kusovník a tabulku postupu, pokud jsou řádky kusovníku pro části E a F nakonfigurovány tak, aby byl typ řádku fiktivní. Na obrázku č. 4 je (a) kusovník pro produkt G a (b) je tabulka postupů pro produkt G.

![Obrázek 4: Výrobní kusovník, produkt G.](media/product-G-route-sheet-G.png)
*Obrázek 4: Výrobní kusovník, produkt G*

## <a name="phantom-and-route-network"></a>Fiktivní a síťový postup

Fiktivní kusovníky lze také použít pro kusovník, který má síťový postup. V síťovém postupu běží jedna nebo více operací současně. Obrázek č. 5 znázorňuje příklad síťového postupu, který se používá ve víceúrovňovém kusovníku. Na obrázku č. 5 je (a) kusovník pro produkt G a část F a (b) je tabulka postupů pro produkt G a část F, která má síťový postup.

![Obrázek 5: Inženýrský kusovník, produkt G, síťový postup.](media/product-G-part-F.png)
*Obrázek 5: Inženýrský kusovník, produkt G, síťový postup*

Na obrázku č. 6 je (a) kusovník pro produkt G a část F, (b) je tabulka postupů pro produkt G a část F.

![Obrázek 6: Výrobní kusovník, produkt G, síťový postup.](media/product-G-part-F-with-route-sheet.png)
*Obrázek 6: Výrobní kusovník, produkt G, síťový postup*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
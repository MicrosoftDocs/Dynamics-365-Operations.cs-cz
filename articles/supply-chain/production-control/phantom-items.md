---
title: Fiktivní položky
description: Toto téma podrobně popisuje, jakým způsobem lze použít fiktivní typ řádku pro řádky kusovníku a receptury v aplikaci Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b14bebadd7088c9bbcfb6b1c5df1fe1a3c98694d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423997"
---
# <a name="phantom-items"></a>Fiktivní položky

[!include [banner](../includes/banner.md)]

Toto téma podrobně popisuje, jakým způsobem lze použít fiktivní typ řádku pro řádky kusovníku a receptury. Na následujícím obrázku, (a) je kusovník pro produkt H a části F a G, a (b) je tabulka postupů pro produkty H a část F.

![Produkt H a část F](media/product-H-part-F.png)


Na obrázku je uveden příklad struktury kusovníku ve dvou úrovních. Dokončený produkt H představuje produkt pro sestavení stroje. Sestavení stroje se skládá ze dvou částí, z elektrické jednotky (F), která má dva materiály (A a B), a skupiny obalových materiálů (G), která má rovněž dva materiály (C a D). Další materiál (E) se používá při obecném sestavení stroje.

![Produkt H a část F](media/product-H-part-B.png)

Předcházející obrázek představuje vývojový kusovník pro produkt H. Tato struktura poskytuje dobrý přehled o součástech a komponentách celkového sestavení stroje. I když návrháři produktu mohou upřednostňovat zobrazení kusovníku tímto způsobem, tato struktura nemusí správně představovat způsob, jakým je stroj sestaven na dílně. 

Například vývojový kusovník na předcházejícím obrázku označuje, že elektrická jednotka F je sestavena jako samostatná část na samostatné pracovní objednávce. V dílně však mohou usoudit, že je optimálnější sestavit elektrickou jednotku jako součást celkového sestavení stroje, nikoliv jako samostatný pracovní příkaz.

Tento vývojový kusovník také označuje, že část G je samostatná část. V této struktuře však část G nereprezentuje fyzickou část, ale kolekci obalových materiálů. 

Proto i když vývojový kusovník poskytuje velkou hodnotu pro návrh produktu a údržbu tohoto návrhu, nemusí se jednat o nejlogičtější způsob podpory proces provádění výroby produktu. Naopak výrobní kusovník představuje nejlepší způsob sestavení produktu.

Následující obrázek znázorňuje, jak je předchozí vývojový kusovník převeden na výrobní kusovník. Na tomto obrázku (a) je kusovník pro produkt H a b je tabulka postupů pro produkt H.

V této struktuře můžete vidět, že neexistuje zmínka o částech F a G, a že materiály, ze kterých se tyto části skládají, byly povýšeny na další úroveň kusovníku. 

Na rozdíl od vývojového kusovníku, který měl dva listy operací, výrobní kusovník obsahuje pouze jeden list operací. Operace balení, která byla navázána na část G, byla také povýšena a je nyní součástí listu operací pro produkt H. Sestavení elektrické jednotky je první operace. Tento výrobní příkaz dává smysl, vzhledem k tomu, že tato jednotka se používá v další operace, kterou je sestavení stroje. Poslední operace je operace balení, které spotřebuje dva obalové materiály (C a D).

Přechod mezi vývojovým kusovníkem a výrobním kusovníkem povolen prostřednictvím typu řádku kusovníku Phantom. Jako naznačuje termín „fiktivní“, části F a G během převodu mezi dvěma typy kusovníku zmizely. V tomto příkladu je fiktivní typ řádku použit na řádky kusovníku pro části F a G ve vývojovém kusovníku. Když je vytvořena výrobní zakázka nebo dávková objednávka, je vývojový kusovník zkopírován do výrobní zakázky nebo dávkové objednávky. Když je pak zakázka oceněna, dojde k přechodu z vývojového kusovníku na výrobní kusovník, jak je uvedeno na předchozím obrázku. Z listu operace na druhém obrázku jsou obalové materiály C a D vstupem pro operaci. 

## <a name="multilevel-phantom-bom-structures"></a>Víceúrovňové struktury fiktivního kusovníku
Fiktivní typ řádku typu lze použít ve víceúrovňových strukturách kusovníku, jak je uvedeno na následujícím obrázku. Na tomto obrázku je (a) kusovník pro produkt G a (b) je tabulka postupů pro části E a F a produkt G. 

![Produkt G a část F s tabulkami postupů](media/product-G-route-sheet-G.png)


Následující obrázek znázorňuje výsledný výrobní kusovník a tabulku postupu, pokud jsou řádky kusovníku pro části E a F nakonfigurovány tak, aby byl typ řádku fiktivní. Na tomto obrázku (a) je kusovník pro produkt G a (b) je tabulka postupů pro produkt G.

![Produkt G](media/product-G.png)


## <a name="phantom-and-route-network"></a>Fiktivní a síťový postup
Fiktivní kusovníky lze také použít pro kusovník, který má síťový postup. V síťovém postupu běží jedna nebo více operací současně. Následující obrázek znázorňuje příklad síťového postupu, který se používá ve víceúrovňovém kusovníku. Na tomto obrázku je (a) kusovník pro produkt G a část F a (b) je tabulka postupů pro produkt G a část F, která má síťový postup.

![Produkt G a část F](media/product-G-part-F.png)


Na následujícím obrázku, (a) je kusovník pro produkt G a část F, a (b) je tabulka postupů pro produkt G a část F.

![Produkt G a část F s tabulkami postupů](media/product-G-part-F-with-route-sheet.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
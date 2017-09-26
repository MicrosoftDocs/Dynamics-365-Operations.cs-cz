--- 
title: "Vytvoření prodejní objednávky pro konfigurovatelný produkt"
description: "Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6546d504a2fda255cb5183408dfe84a3074543ab
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Vytvoření prodejní objednávky pro konfigurovatelný produkt

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura znázorňuje způsob použití šablony konfigurace pro produkt na prodejní objednávce. Tento příklad využívá model reproduktoru D0006 v ukázkové datové společnosti USMF. Zpracovatel prodejních objednávek obvykle používá tuto proceduru.


## <a name="create-a-sales-order"></a>Vytvořit prodejní objednávku
1. Klikněte na Zpracování a dotaz na prodejní objednávku.
2. Klikněte na položku Nová.
3. Klikněte na Prodejní objednávka.
4. V poli Účet odběratele vyberte US-001. 
5. Klikněte na tlačítko OK.
6. Do pole Číslo položky vyberte „D0006“.
    * Pro tento úkol je nutné vybrat konfigurovatelný produkt.  
7. Klikněte na Produkt a dodávka.
8. Klikněte na Řádek konfigurace.
    * Všimněte si, že se změnila cena, na základě konfigurace, která byla vybrána, a že pole Zahrnout kabel je nyní nastaveno na hodnotu True.  
    * Všimněte si výchozí ceny a nastavení, která jsou vybrána pro kabel.  
9. Klikněte na Šablona nákladu.
    * Tento příklad ukazuje, jak lze použít šablonu pro výběr předdefinované konfigurace. Pokud používáte tuto proceduru jako průvodce záznamem úloh a chcete zjistit další dostupné hodnoty atributů, musíte klepnout na tlačítko Odemknout.  
10. Klikněte na tlačítko OK.
11. Klikněte na tlačítko OK.
12. Rozbalte sekci Podrobnosti řádku.
13. Klepněte na kartu Produkt.
    * Konfigurace položky je nyní uvedena pod dimenzemi produktu.  
14. Zavřete stránku.

## <a name="select-the-product-configuration"></a>Vyberte konfiguraci produktu.



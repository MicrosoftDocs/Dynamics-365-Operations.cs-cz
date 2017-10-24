--- 
title: "Plánování vytížení a dodávek s použitím pracovní plochy plánování vytížení"
description: "Tento postup popisuje použití pracovní plochy plánování vytížení k vytvoření vytížení pro prodejní objednávku."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Plánování vytížení a dodávek s použitím pracovní plochy plánování vytížení

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje použití pracovní plochy plánování vytížení k vytvoření vytížení pro prodejní objednávku. Jako nutnou podmínku si nejprve vytvoříte prodejní objednávku. Tento postup je součástí každodenní práce koordinátora přepravy. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-a-sales-order"></a>Vytvořit prodejní objednávku
1. Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyberte účet US-004.
5. Klepněte na tlačítko OK.
6. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyberte položku A0001.
    * A0001 je povoleno pro správu přepravy.  
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Zadejte číslo do pole Množství.
10. Zadejte hodnotu 24 do pole Sklad.
    * V tomto příkladu vyberte sklad 24. Tento sklad jej povolen pro správu přepravy a rozšířenou správu skladu.  
11. Klikněte na položku Uložit.
12. Zavřete stránku.

## <a name="create-a-new-load"></a>Vytvoření nového vytížení
1. Přejděte do nabídky Správa přepravy > Plánování > Pracovní plocha plánování vytížení.
2. Klikněte na kartu Řádky prodeje.
    * Nyní budete vytvářet vytížení pro prodejní objednávku, kterou jste právě vytvořili. Vytížení lze vytvořit podle nabídky a poptávky z nákupních objednávek, převodních příkazů a prodejních objednávek.  
3. V podokně akcí klikněte na možnost Nabídka a poptávka.
4. Klikněte na možnost Do nového vytížení.
5. V poli ID šablony nákladu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Šablona vytížení definuje maximální měření pro hmotnost a objem celého vytížení. Šablona vytížení může například představovat velikost kontejneru nebo nákladního automobilu.  
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Klikněte na tlačítko OK.

## <a name="rate-and-route-the-load"></a>Hodnocení a směrování vytížení
1. Klikněte na možnost Hodnocení a směrování.
2. Klikněte na možnost Pracovní plocha sazeb trasy.
3. Klikněte na možnost Sazba – obchod.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na možnost Přiřadit.
6. Zavřete stránku.
7. Zavřete stránku.



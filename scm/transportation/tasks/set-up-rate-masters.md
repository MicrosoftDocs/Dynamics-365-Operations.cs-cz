--- 
title: "Nastavení hlavních sazeb"
description: "Tento postup popisuje, jak nastavíte hlavní sazby."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 263c912594dcf61985094dab30eab8f72cd731e9
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-rate-masters"></a>Nastavení hlavních sazeb

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak nastavíte hlavní sazby. Hlavní sazby obvykle nastavuje manažer logistiky v závislosti na smlouvách podepsaných s dopravci. V tomto scénáři nastavíte hlavní sazbu pro leteckého dopravce. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="set-up-rate-master"></a>Nastavení hlavní sazby
1. Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Hlavní sazba.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Hlavní sazba.
4. Zadejte hodnotu do pole Název.
5. V poli ID metadat sazeb kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * ID metadat sazeb určí data potřebná pro hlavní sazbu, protože definuje metadata očekávaná modulem systému TMS, který používá tuto hlavní sazbu.  
6. V tomto příkladu vyberte možnost P2P.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Klikněte na položku Uložit.

## <a name="set-up-rate-base"></a>Nastavení základní sazby
1. Klikněte na možnost Základní sazba.
    * Nastavení základní sazby určuje sazbu dopravce a slouží k nastavení struktury sazby, protože definuje strukturu kurzů v zarážkách definovaných ve hlavní změně.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Základní sazba.
4. Zadejte hodnotu do pole Název.
5. V poli Hlavní změna kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Hlavní změny slouží k definování struktury cen a použitých zarážek. Cenové struktury používají vrstvené ceny vycházející z fyzických rozměrů.  
6. V tomto příkladu použijte hmotnost
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Přepněte rozšíření oddílu Podrobnosti.
9. Klepněte na možnost Nový.
10. V poli PSČ místa vyložení – od zadejte „30301“.
11. V poli PSČ místa vyložení – do zadejte „30318“.
12. V poli Země/oblast vyložení zadejte „USA“ .
13. Do pole <1,00 libry zadejte hodnotu „100“.
    * Vložte sazba za libru, pokud je celková hmotnost vytížení nižší než 1 libra.  
14. Do pole < 5,00 liber zadejte hodnotu „300“.
    * Vložte sazba za libru, pokud je celková hmotnost vytížení nižší než 5 liber.  
15. Do pole < 20,00 liber zadejte hodnotu „500“.
    * Vložte sazba za libru, pokud je celková hmotnost vytížení nižší než 20 liber.  
16. Do pole < 100,00 liber zadejte hodnotu „1000“.
    * Vložte sazba za libru, pokud je celková hmotnost vytížení nižší než 100 liber.  
17. Do pole < 1.000,00 liber zadejte hodnotu „3000“.
    * Vložte sazba za libru, pokud je celková hmotnost vytížení nižší než 1000 liber.  
18. Klikněte na položku Uložit.
19. Zavřete stránku.

## <a name="assign-rate-base"></a>Přiřazení základní sazby
1. Rozbalte oddíl Přiřazení základní sazby.
2. Klikněte na položku Nová.
    * Můžete mít několik přiřazení základní sazby pro jednotlivé hlavní sazby. Díky tomu lze vytvořit několik různých cenových bodů pro každého dopravce v závislosti na cílech, službách nebo jiných základech sazby. V tomto postupu můžete vytvořit pouze jedno přiřazení základní sazby.  
3. Zadejte hodnotu do pole Název.
4. V poli Základní sazba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. V poli Služba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Do pole PSČ pro vyzvednutí PSČ zadejte „98052“.
    * Určete, pro které PSČ toto přiřazení základní sazby bude platné.    
10. Do pole Země/oblast pro vyzvednutí zadejte „USA“.
11. Klikněte na položku Uložit.



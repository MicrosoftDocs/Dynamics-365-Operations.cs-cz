--- 
title: " Používání programu kontinuity"
description: "Tento postup vás provede prodejem programu trvání a zpracováním souvisejících prodejních objednávek."
author: scott-tucker
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: bd584bbb49ea83c4debf11ad0169c346ef0f9637
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="use-a-continuity-program"></a> Používání programu kontinuity

[!include[task guide banner](../includes/task-guide-banner.md)]

Tento postup vás provede prodejem programu trvání a zpracováním souvisejících prodejních objednávek. Aby bylo možné tuto proceduru dokončit, musí být uživatel nastaven jako uživatel kontaktního střediska. Tato procedura používá data ukázkové společnosti USRT.

1. Přejděte na Maloobchodní a velkoobchodní prodej > Odběratelé > Služby odběratele.
2. Do pole SearchText zadejte Karen a pak stiskněte klávesu Tab.
    * Mělo by se otevřít překryvné dialogové okno Rozšířené hledání. Pokud tomu tak není, klepněte na tlačítko Hledat vpravo od tohoto pole.  
3. Označte v seznamu vybraný řádek.
    * Měla by existovat pouze jeden řádek se zobrazením Karen Berg. Vyberte řádek klepnutím na znak zaškrtnutí zcela vlevo v mřížce.  
4. Klepněte na tlačítko Vybrat.
5. Klepněte na položky Nová prodejní objednávka.
    * Je vhodné poznamenat si číslo prodejní objednávky. Budete je potřebovat později v této proceduře.  
6. Do pole Číslo položky zadejte '88000' a pak stiskněte klávesu Tab.
    * Toto je trvalé zboží v demo datech USRT.  
7. Klikněte na tlačítko Dokončit.
8. Do pole Způsob platby zadejte 'Visa'.
9. Klikněte na Přidat kreditní kartu.
    * Na této stránce zadejte požadované informace o platební kartě.  
10. Klikněte na tlačítko OK.
11. Rozbalte sekci Platba.
    * Pro objednávku musí být zadány platby, aby bylo možné odeslat objednávku do kontaktního střediska.  
12. Klikněte na tlačítko OK.
13. Klepněte na tlačítko Odeslat.
    * Teď máte vytvořenou novou trvalou objednávku. Potom spustíte dvě výrobní dávky, které slouží ke zpracování trvalých objednávek.  
14. Zavřete stránku.
15. Přejděte na Maloobchodní a velkoobchodní prodej > Trvání > Zpracovat trvalé platby.
16. V poli Položka trvání zadejte "88000" a potom stiskněte klávesu Tab.
17. Klikněte na tlačítko OK.
18. Přejděte na Maloobchodní a velkoobchodní prodej > Trvání > Vytvořit trvalé podřízené objednávky.
    * Tento proces vytvoří nové prodejní objednávky na základě nastavení programů trvání.  
19. V poli Položka trvání zadejte "88000" a potom stiskněte klávesu Tab.
    * Zboží '88000 je trvalé zboží v ukázkových datech USRT.  
20. V poli Prodejní objednávka zadejte nebo vyberte hodnotu.
    * Zadejte číslo prodejní objednávky, které jste si poznamenali dříve v proceduře. Tím zachováte dobu zpracování pro tuto proceduru jako minimální. Pole Prodejní objednávka je volitelné – můžete zpracovat všechny objednávky pro jakýkoli program.  
21. Klikněte na tlačítko OK.



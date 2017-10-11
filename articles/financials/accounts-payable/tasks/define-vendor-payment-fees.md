--- 
title: "Definování platebních poplatků dodavatelů"
description: "Nastavte poplatky pro platby dodavatelů."
author: abruer
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
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 844badb3b3037df8c4f22be558f01ea3dbf37f9d
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="define-vendor-payment-fees"></a>Definování platebních poplatků dodavatelů

[!include[task guide banner](../../includes/task-guide-banner.md)]

Nastavte poplatky pro platby dodavatelů. Tento úkol používá ukázkovou společnost USMF.

1. Přejděte do nabídky Závazky > Nastavení platby > Platební poplatek.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole ID poplatku.
    * ID poplatku by mělo nabízet popis v případě, že bude tento poplatek použit (například "EFT_Fee").  
4. Zadejte hodnotu do pole Název.
5. Zadejte hodnotu do pole Popis poplatku.
    * Přidejte popis a poskytněte tak více podrobností o tom, kdy je poplatek vyměřen.  
6. V poli Náklady vyberte dodavatele nebo hlavní knihu.
    * Hlavní kniha se používá, pokud bude poplatek zanesen do výdajů pro vaši organizaci.  Dodavatel se používá, pokud bude poplatek zanesen dodavateli.  
7. Zadejte hlavní účet, pokud budou poplatky zaneseny.
    * Tato volba je k dispozici pouze tehdy, pokud jako možnost Náklady vyberete Hlavní kniha.  
8. Vyberte deník, u kterého lze použít tento poplatek. 
    * Pro platební poplatky dodavatele vyberte deník Úhrady dodavateli.  
9. Klikněte na položku Uložit.
10. Klikněte na Nastavení platebního poplatku.
    * Pokračujte k nastavení platebních poplatků a definujte, kdy má poplatek být upraven na výchozí pro deník, který jste vybrali.  
11. Vyberte možnost Tabulka, Skupina nebo Vše.
    * Tabulka slouží k výběru jednoho bankovního účtu, Skupina slouží k výběru bankovní skupiny a Vše umožňuje použití tohoto nastavení poplatků pro všechny bankovní účty  
12. Vyberte bankovní účet nebo bankovní skupinu.
    * Vyhledávání zobrazí bankovní skupinu, pokud jste vybrali možnost Skupina, a bude popisovat bankovní účty, jestliže jste vybrali Tabulka.  
13. Vyberte metodu platby, pro kterou se vyhodnotí tento poplatek.
14. Vyberte specifikaci platby pro vybraný způsob platby.
    * Specifikace platby se používají pro platbu metodou elektronického převodu finančních prostředků.  
15. Určete, zda poplatek budou procenta, částka nebo interval.
16. Zadejte procento nebo částku poplatku.
    * Pokud je Poplatek procentuální hodnotu, zadejte procento. Pokud ke Poplatek částkou, zadejte částku poplatku. U poplatku ve formě intervalu použijte kartu Interval pro definování vrstvených poplatků.  
17. V poli Měna poplatku vyberte měnu, v níž bude poplatek vyměřen.
    * Tato měna je pro poplatek. Měna platby slouží k definování toho, kdy se pravidla poplatku musí vyhodnotit na základě měny platby. Například vaše banka může účtovat poplatek, když je provedena platba v EUR, ale pro všechny ostatní platby není určen poplatek.  
18. Klikněte na položku Uložit.


--- 
title: " Vytvoření, výpočet a zaúčtování výkazu pro maloobchod"
description: "Tento postup vás provede manuálním postupem pro vytvoření, výpočet a zaúčtování výpisu pro obchod."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 60bcafffc922e6d57e52a5dff104a0fbb252f6ce
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a> Vytvoření, výpočet a zaúčtování výkazu pro maloobchod

[!include[task guide banner](../includes/task-guide-banner.md)]

Tento postup vás provede manuálním postupem pro vytvoření, výpočet a zaúčtování výpisu pro obchod. Existují také dávkové úlohy, které lze konfigurovat pro stejné úkoly. Postup pro konfiguraci a spuštění dávkových úlohy můžete najít v jiných tématech. Chcete-li provést tento postup, musíte mít transakce, které byly dokončeny v POS a potom převedeny do aplikace Dynamics AX. Tento záznam používá v ukázkových datech společnost USRT. Tento postup může odkazovat na Microsoft Dynamics AX. Všimněte si, Dynamics AX se nyní nazývá Microsoft Dynamics 365 for Operations.

1. Přejděte na Všechny pracovní prostory > .. > Finance maloobchodu.
2. Klikněte na Nový výkaz.
3. V poli Číslo obchodu kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Klikněte na tlačítko OK.
    * Nastavení skupiny obsahuje nastavení, která řídí, které transakce budou zahrnuty do výkazu a způsob jejich seskupení do řádků výkazu. Můžete otevřít nastavení skupiny a tato nastavení změnit, nebo můžete použít výchozí hodnoty.  
    * Pole Metoda výkazu definuje způsob, jak budou seskupeny řádky výkazu.  
    * Pokud chcete vypočítat výkaz pouze pro konkrétního zaměstnance nebo registr, vyberte zaměstnance nebo registrační pokladnu.  
6. Vyberte možnost v poli Metoda uzávěrky.
7. Klikněte na Vypočítat výkaz.
8. Klepněte na tlačítko Ano.
    * Po výpočtu výkazu, by měly být vytvořený řádky s celkovými částkami pro každý použitý způsob platby a metodu výkazu.  
    * Zadejte do každého řádku spočtenou částka, pokud je nutné ji zadávat nebo aktualizovat. Vypočtená pole budou vyplněna částkami z výkazů úhrad provedených v POS.  
9. Klikněte na Zaúčtovat výkaz.
10. Klikněte na tlačítko Zavřít.
11. Přejděte na Maloobchodní a velkoobchodní prodej > Kanály > Finance maloobchodu.
12. Klepněte na kartu Zaúčtované výpisy.



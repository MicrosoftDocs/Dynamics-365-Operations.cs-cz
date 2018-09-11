--- 
title: " Vytvoření, výpočet a zaúčtování výkazu pro maloobchod"
description: "Tento postup vás provede manuálním postupem pro vytvoření, výpočet a zaúčtování výpisu pro obchod."
author: jashanno
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 33ebb28196baa9ae944dbd124274b05cb587fea4
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

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



--- 
title: "Přehled plateb dodavatele"
description: "Tento průvodce úkolem vás provede různými metodami pro vytvoření plateb dodavatelů, včetně použití návrhu platby nebo ručního zadání jednorázové platby."
author: kweekley
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
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 44b7c02e7c238dcea83c5900620731a7befbbb42
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="vendor-payment-overview"></a>Přehled plateb dodavatele

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce úkolem vás provede různými metodami pro vytvoření plateb dodavatelů, včetně použití návrhu platby nebo ručního zadání jednorázové platby. Tato procedura používá ukázkovou společnost USMF.

1. Přejděte na Závazky > Platby > Deník plateb.
2. Klikněte na položku Nová.
3. Vyberte deník plateb pro uložení plateb dodavatele. 
4. Vyberte deník nebo jej zadejte ručně.
5. Klikněte na položku Řádky.
6. Klikněte na Návrh platby.
7. Klikněte na Vytvořit návrh plateb.
    * Návrh plateb je dotaz sloužící k výběru faktur k platbě. Před vytvořením nebo vygenerováním plateb dodavatele můžete upravit seznam faktur k úhradě.  
8. Vyberte faktury k platbě podle data splatnosti, platební slevy nebo obou možností. 
9. Zadejte datum pro porovnání s datem splatnosti nebo platební slevou. 
10. Volitelně: Zadejte datum platby použité pro všechny platby.
    * Zde zadané datum bude datum plateb pro všechny vytvořené platby bez ohledu na datum splatnosti nebo datum platební slevy.  
11. Volitelně: Zadejte minimální datum platby, které může být použito jako datum platby.
    * Minimální datum platby bude nejbližší datum použité při vytváření plateb. Například pokud má faktura datum splatnosti po minimálním datu platby, datum splatnosti bude datem platby namísto minimálního data platby k zaplacení faktury v nejzazší možné datum.  
12. Zadejte další omezení dotazu v části Záznamy k zahrnutí.
    * Filtr se často používá k omezení faktur vybraných k zaplacení podle skupin dodavatelů nebo způsobu platby. Můžete například přidat filtr pouze pro úhradu faktur šekem v rámci daného zpracování výplat.  
13. Zadejte další omezení dotazu nebo výchozí nastavení plateb. 
    * Další parametry lze použít k definování měny plateb nebo k povolení centralizovaných plateb v rámci daného zpracování výplat.  
14. Klikněte na tlačítko OK.
    * Po kliknutí na tlačítko OK se zobrazí výsledky dotazu. Pokud nechcete zobrazit náhled seznamu faktur vybraných k zaplacení, můžete přejít zpět na pevnou záložku Parametry a změnit nastavení Vytvořit platby bez náhledu faktury = Ano.  
15. Pomocí tlačítka Zobrazit přehled plateb zobrazte platby, které budou vytvořeny pro dodavatele na vybrané faktuře.
16. Pomocí tlačítka Skrýt přehled plateb můžete platby skrýt. 
17. Klikněte na Vytvořit platby.
    * Před výběrem možnosti Vytvořit platby můžete kliknout pravým tlačítkem myši na mřížku a exportovat do formátu aplikace Excel na seznam faktur. Tlačítko Vytvořit platby vytvoří platby dodavatele v deníku plateb.  
18. Naskenujte platby a ujistěte se, že je u všech plateb definován způsob platby. 
    * Při generování plateb, jako je například tisk šeku nebo vytváření elektronické platby, musí být definován způsob platby. Způsob platby také použije standardně bankovní účet z provedené platby.  
19. Klikněte na tlačítko Nový a vytvořte jednorázovou platbu.
    * Jednorázovou platbu lze přidat do deníku plateb kdykoli před zaúčtováním. To lze provést kliknutím na tlačítko Nový a přidáním informací o platbě ručně, ne pomocí návrhu platby.  
20. Vyberte dodavatele, kterému bude platba určena.
21. Existuje-li faktura k úhradě, zvolením možnosti Vyrovnat transakce vyberte fakturu k platbě.
    * Pokud se jedná o zálohu, tento krok je volitelný. Můžete vytvořit platbu bez výběru faktury.  
22. Označte veškeré faktury, které budou zaplaceny.
    * Použijete-li možnost Vyrovnat transakce k výběru faktur k uhrazení, částka k úhradě bude automaticky vypočítána z faktury vámi označené pro zaplacení a z částky vámi zadané v poli Částka k vyrovnání.  
23. Klikněte na tlačítko OK.
24. Chcete-li odstranit platbu, označte řádek.
25. Klepněte na tlačítko Odstranit.
    * Odstranění platby odstraní pouze danou platbu. Všechny faktury označené k platbě budou i nadále dostupné k uhrazení jinou platbou.  
26. Klepněte na tlačítko Ano.
27. Vyberte generování plateb pro tisk šeků nebo vytvoření souborů elektronické platby.
28. Vyberte způsob platby, kterou chcete vygenerovat.
    * Deník plateb může obsahovat platby pro šeky i elektronické platby, ale v rámci jedné operace lze vygenerovat pouze jeden typ platby.  
29. Vyberte bankovní účet, ze kterého lze platby generovat.
30. Klikněte na tlačítko OK.
    * Platby budou generovány pouze pro platby, které odpovídají vámi vybranému způsobu platby a bankovnímu účtu.  
31. Pokud generujete šeky, vyberte možnost Dokument k zajištění správnosti cíle tisku pro šeky.
32. Klikněte na tlačítko OK.
33. Platby vygenerujte kliknutím na tlačítko OK.
34. Jsou-li všechny platby schválené a vygenerované, klikněte na možnost Zaúčtovat. 



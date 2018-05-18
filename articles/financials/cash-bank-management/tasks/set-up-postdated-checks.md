--- 
title: "Nastavení postdatovaných šeků"
description: "Toto téma vysvětluje, jak určit, zda se mají zaúčtovat položky deníku pro postdatované šeky a které účetní deníky se mají použít pro vymazání položek a plateb dodavatele."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d83713f9d54b396a10894995024ac1c8dd47a6f1
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-postdated-checks"></a>Nastavení postdatovaných šeků

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toto téma vysvětluje, jak určit, zda se mají zaúčtovat položky deníku pro postdatované šeky a které účetní deníky se mají použít pro vymazání položek a plateb dodavatele. Můžete také určit clearingové účty pro vydané šeky, přijaté šeky a srážkové daně. Postdatované šeky jsou vydány za účelem provedení a přijetí platby v budoucí datu. Můžete zadat, zda se má šek odrazit ve vašich účetních knihách před datem splatnosti.



Role tohoto postupu je Pokladník. Tato procedura používá ukázkovou společnost USMF.


## <a name="set-up-postdated-checks"></a>Nastavení postdatovaných šeků
1. Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.
2. Klikněte na kartu Postdatované šeky.
3. Zaškrtněte políčko Povolit postdatované šeky nebo jeho zaškrtnutí zrušte.
4. Zaškrtněte políčko Zaúčtovat položky deníku pro postdatované šeky nebo jeho zaškrtnutí zrušte.
5. V poli Clearingový účet pro vydané šeky zadejte požadované hodnoty.
6. V poli Clearingový účet pro přijaté šeky zadejte požadované hodnoty.
7. V poli Hlavní deník pro položky clearingu zadejte hodnotu.
8. V poli Přenést postdatované šeky do tohoto deníku plateb dodavatelů zadejte hodnotu.
9. Zadejte požadované hodnoty do pole Clearingový účet srážkové daně.
10. Klikněte na položku Uložit.
11. Zavřete stránku.
12. Přejděte do nabídky Závazky > Nastavení platby > Metody platby.
13. Klikněte na položku Nová.
14. V poli Způsob platby zadejte hodnotu.
15. Zvolením možnosti Clearingové zaúčtování postdatovaných šeků určete, že je částka šeku zaúčtována na clearingový účet.
16. V poli Typ účtu vyberte „Banka“.
    * Pole pro protiúčet způsobu platby bude prázdné.  
17. Zadejte požadované hodnoty do pole Platební účet.
    * Vyberte bankovní účet, který se používá k odečtu částky faktury.  
18. Zavřete stránku.
19. Přejděte do nabídky Pohledávky > Nastavení platby > Metody platby.
20. Klikněte na položku Nová.
21. V poli Způsob platby zadejte hodnotu.
22. Zvolením možnosti Clearingové zaúčtování postdatovaných šeků určete, že je částka šeku zaúčtována na clearingový účet.
23. V poli Typ účtu vyberte „Banka“.
    * Pole pro protiúčet způsobu platby bude prázdné.  
24. Zadejte požadované hodnoty do pole Platební účet.
    * Vyberte bankovní účet, který se používá k odečtu částky faktury.  
25. Zavřete stránku.



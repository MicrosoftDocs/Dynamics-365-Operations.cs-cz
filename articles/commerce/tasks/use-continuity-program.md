---
title: Používání programů trvání
description: Tento postup vás provede prodejem programu trvání a zpracováním souvisejících prodejních objednávek.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baf0127a35cc62952fd78daaf8204d35ec8d2b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410812"
---
# <a name="using-continuity-program"></a>Používání programů trvání

[!include [banner](../includes/banner.md)]

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
17. Klepněte na tlačítko OK.
18. Přejděte na Maloobchodní a velkoobchodní prodej > Trvání > Vytvořit trvalé podřízené objednávky.
    * Tento proces vytvoří nové prodejní objednávky na základě nastavení programů trvání.  
19. V poli Položka trvání zadejte "88000" a potom stiskněte klávesu Tab.
    * Zboží '88000 je trvalé zboží v ukázkových datech USRT.  
20. V poli Prodejní objednávka zadejte nebo vyberte hodnotu.
    * Zadejte číslo prodejní objednávky, které jste si poznamenali dříve v proceduře. Tím zachováte dobu zpracování pro tuto proceduru jako minimální. Pole Prodejní objednávka je volitelné – můžete zpracovat všechny objednávky pro jakýkoli program.  
21. Klikněte na tlačítko OK.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
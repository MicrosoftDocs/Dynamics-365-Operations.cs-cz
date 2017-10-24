--- 
title: "Vystavení vstupního certifikátu EU"
description: "Tento postup vás provede povolením vstupního certifikátu EU, konfigurací účtu odběratele pro použití vstupních certifikátů a vydáním certifikátu."
author: mrolecki
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ff00ff0df3835ee2cbf21219ad6f07bfeba6e7ac
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="issue-an-eu-entry-certificate"></a>Vystavení vstupního certifikátu EU

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup vás provede povolením vstupního certifikátu EU, konfigurací účtu odběratele pro použití vstupních certifikátů a vydáním certifikátu. Tato procedura byla vytvořena pomocí ukázkových dat společnosti DEMF.


## <a name="enable-entry-certificate-management"></a>Povolit správu vstupních certifikátů
1. Přejděte do nabídky Pohledávky > Nastavení > Parametry pohledávek.
2. Klikněte na kartu Dodávky.
3. Rozbalte oddíl Vstupní certifikát.
4. Zvolte Ano v poli Povolit správu vstupních certifikátů.
5. Zvolte Ano v poli Povolit vystavování vstupních certifikátů.
6. Klikněte na kartu Číselné řady.
7. V seznamu najděte a vyberte řádek vstupního certifikátu.
8. V poli Kód číselné řady zadejte nebo vyberte hodnotu.

## <a name="set-up-a-customer"></a>Nastavení odběratele
1. Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.
2. Použijte rychlý filtr pro hledání záznamů. V poli Účet můžete například filtrovat pomocí hodnoty „DE-015“.
3. Otevřete podrobnosti o účtu odběratele.
4. Klikněte na možnost Upravit.
5. Rozbalte oddíl Faktury a dodávky.
6. Zvolte Ano v poli Požadován vstupní certifikát.
7. Zvolte Ano v poli Vystavit vstupní certifikát.
8. Klikněte na položku Uložit.

## <a name="create-an-eu-entry-certificate-automatically"></a>Automatické vytvoření vstupního certifikátu EU
1. Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele zadejte nebo vyberte hodnotu.
4. Klepněte na tlačítko OK.
5. V poli Číslo zboží zadejte nebo vyberte hodnotu.
6. Klikněte na položku Uložit.
7. V podokně akcí klikněte na položku Vyskladnit a zabalit.
8. Klikněte na položku Zaúčtovat dodací list.
9. Rozbalte sekci Parametry.
10. V poli Množství vyberte možnost Vše.
11. Zrušte zaškrtnutí políčka Vystavit vstupní certifikát.
    * Při zaúčtování dodacího listu nebo při fakturaci objednávky lze vydat vstupní certifikát. Ponechte políčko Vystavit vstupní certifikát nezaškrtnuté, abyste mohli certifikát vystavit později.  
12. Klikněte na tlačítko OK.
13. Klikněte na tlačítko OK.
14. V podokně akcí klikněte na položku Faktura.
15. Klikněte na položku Faktura.
    * Ověřte, zda jsou zaškrtnuta políčka Požadován vstupní certifikát a Vystavit vstupní certifikát v části Přehled.  Můžete také vybrat políčko Vytisknout vstupní certifikát k povolení tisku certifikátu.  
16. Klikněte na tlačítko OK.
17. Klikněte na tlačítko OK.
18. V podokně akcí klikněte na položku Faktura.
19. Klikněte na položku Faktura.
20. V podokně akcí klikněte na položku Faktura.
21. Klikněte na možnost Zobrazit vystavené vstupní certifikáty.
22. Klepněte na položku Tisk.
23. Zavřete stránku.
24. Klikněte na položku Změnit stav.
25. Vyberte možnost v poli Nový stav.
26. Klikněte na tlačítko OK.
27. Zavřete stránku.

## <a name="create-an-eu-entry-certificate-manually"></a>Ruční vytvoření vstupního certifikátu EU
1. V podokně akcí klikněte na položku Faktura.
2. Klikněte na možnost Vytvořit vstupní certifikát.
3. Klepněte na tlačítko OK.
4. V podokně akcí klikněte na položku Faktura.
5. Klikněte na možnost Zobrazit vystavené vstupní certifikáty.



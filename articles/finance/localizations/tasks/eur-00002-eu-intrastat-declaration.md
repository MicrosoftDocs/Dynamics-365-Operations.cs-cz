---
title: EUR-00002 Generování prohlášení Intrastat EU
description: Tento postup vás provede kroky nutnými k exportu prohlášení systému Intrastat ve formátu elektronického souboru a náhledu dat výkazu ve formátu aplikace Excel.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 581a837049f239cb9b9fa41eb978304751cb3b54
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989974"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a>EUR-00002 Generování prohlášení Intrastat EU

[!include [banner](../../includes/banner.md)]

Tento postup vás provede kroky nutnými k exportu prohlášení systému Intrastat ve formátu elektronického souboru a náhledu dat výkazu ve formátu aplikace Excel. 

Před provedením tohoto postupu je nutné převést transakce do systému Intrastat. 

Tato procedura byla vytvořena pomocí ukázkových dat společnosti DEMF.


## <a name="import-configurations-with-settings"></a>Importování konfigurací s nastavením
1. Přejděte na Pracovní prostory > Elektronické sestavy
2. Klikněte na možnost Nastavit jako aktivní.
3. Klikněte na možnost Úložiště.
4. Klikněte na možnost Otevřít.
5. Otevřete filtr sloupce Název konfigurace.
6. Použijte filtr v poli Název konfigurace, s hodnotou Intrastat (DE) a za použití operátoru filtru "začíná".
    * Musíte vybrat název konfigurace platný pro zemi vaší právnické osoby. Tento postup používá jako příklad právnickou osobu (DEMF) pro Německo a měla by být proto zvolena možnost "Intrastat (DE)".  
    * Klikněte na položku Import a poté na možnost Ano.  
7. Otevřete filtr sloupce Název konfigurace.
8. Použijte filtr v poli Název konfigurace, s hodnotou Sestava Intrastat a za použití operátoru filtru "začíná".
    * Klikněte na položku Import a poté na možnost Ano.  

## <a name="set-up-foreign-trade-parameters"></a>Nastavení parametrů zahraničního obchodu
1. Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.
2. Rozbalte část Elektronické výkaznictví.
3. V poli Mapování formátu souboru zadejte nebo vyberte hodnotu Intrastat (DE).
4. V poli Mapování formátu sestavy zadejte nebo vyberte hodnotu Sestava Intrastat.
5. Rozbalte položku Pravidla zaokrouhlování.
    * Měli byste nastavit pravidla zaokrouhlení, která jsou platná ve vaší zemi/oblasti pro vykazování v systému Intrastat.  
6. V poli Pravidlo zaokrouhlování zadejte číslo.
    * Zadejte přesnost zaokrouhlení, například zadejte hodnotu 0,01.  
7. Do pole Počet desetinných míst částky zadejte číslo.
    * Například zadejte 2.  
8. Vyberte možnost v poli Zaokrouhlování pod 1 kg.
    * Vyberte například 'Zaokrouhlování nahoru na 1 kg'.  
9. V poli Pravidlo zaokrouhlování zadejte číslo.
    * Například zadejte hodnotu 1 pro zaokrouhlování hmotnosti na celé číslo.  
10. Rozbalte oddíl Minimální limit.
11. Zadejte číslo do pole Hmotnost.
    * Například zadejte hodnotu 10 jako minimální hmotnost.  
12. Zadejte číslo do pole Částka.
    * Například zadejte hodnotu 200 jako minimální částku.  
13. V poli Komodita zadejte nebo vyberte hodnotu.

## <a name="set-up-compression-of-intrastat"></a>Nastavení komprese pro systém Intrastat
1. Přejděte na Daň > Nastavení > Zahraniční obchod > Komprese Intrastat.
2. Klepněte na tlačítko Odebrat.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * V oddílu Dostupné vyberte například Zboží.  
4. Klepněte na možnost Přidat.

## <a name="generate-intrastat-declaration"></a>Generování prohlášení Intrastat
1. Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat
2. Klikněte na tlačítko Ověřit.
    * Ověření se provádí podle pole Zkontrolovat nastavení na stránce Parametry zahraničního obchodu.  
3. Klikněte na tlačítko OK.
4. Klepněte na položku Aktualizovat.
5. Klikněte na Minimální limit.
6. Zadejte datum do pole Počáteční datum.
    * V tomto příkladu zadejte 1. ledna 2015.  
7. Vyberte Ano v poli Komprese.
8. Zadejte datum do pole Koncové datum.
    * V tomto příkladu zadejte 31. ledna 2015.  
9. Klikněte na tlačítko OK.
10. Klepněte na položku Aktualizovat.
11. Klikněte na Komprese.
    * Tato komprese proběhne podle nastavení komprese v systému Intrastat.  
12. Zadejte datum do pole Počáteční datum.
    * V tomto příkladu zadejte 1. ledna 2015.  
13. Zadejte datum do pole Koncové datum.
    * V tomto příkladu zadejte 31. ledna 2015.  
14. Klikněte na tlačítko OK.
15. Klepněte na položku Aktualizovat.
16. Klikněte na Znovu vygenerovat číselnou řadu.
17. Klikněte na tlačítko OK.
18. Klepněte na Výstup.
19. Klikněte na možnost Sestava.
20. V poli Od data zadejte první datum období vykazování.
    * Například můžete nastavit datum na 1. ledna 2015.  
21. Do pole Do data zadejte datum.
    * V tomto příkladu zadejte 31. ledna 2015.  
22. Vyberte možnost Ano v poli Generovat soubor.
23. Zadejte hodnotu do pole Název souboru.
24. Vyberte možnost Ano v poli Generovat sestavu.
25. Zadejte hodnotu do pole Název souboru sestavy.
26. Vyberte volbu v poli Směr.
    * V tomto příkladu vyberte Expedice.  
27. Klikněte na tlačítko OK.


---
title: Nastavení a generování informací o splatnosti pohledávek
description: Tento průvodce vám pomůže nastavit definici sledování splatnosti, splatné zůstatky odběratelů a zobrazit zůstatky v seznamu Splatný zůstatek a na stránce Kolekce.
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fd8738cfd3466464c9fec1760e9a369ff3a4a67
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "334627"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Nastavení a generování informací o splatnosti pohledávek

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento průvodce vám pomůže nastavit definici sledování splatnosti, splatné zůstatky odběratelů a zobrazit zůstatky v seznamu Splatný zůstatek a na stránce Kolekce. Tento záznam používá ukázkovou společnost USMF.


## <a name="create-an-aging-period-definition"></a>Vytvoření definice období pro sledování splatnosti
1. Přejděte do nabídky na Kredit a inkasa > Nastavení > Definice období pro sledování splatnosti.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Období pro sledování splatnosti.
4. Zadejte hodnotu do pole Popis.
5. Klepnutím na položku Přidat níže vložte nové období pro sledování splatnosti.
6. V poli Období zadejte popis, který se zobrazí v sestavách pro sledování splatnosti.
7. Do pole Jednotka zadejte číslo.
8. Vyberte volbu v poli Interval.
    * Období hlavní knihy odpovídá období kalendáře hlavní knihy. Den, týden, měsíc, čtvrtletí a roky definují velikost intervalu podle typu data. Hodnota Neomezeno vybere všechny transakce před nebo po předchozím období v závislosti na tom, zda se jedná o první nebo poslední období.  
9. Vyberte volbu v poli Indikátor sledování splatnosti.
10. Vyberte období v horní části mřížky. Aktualizace popisu popisujícího nejstarší období v definici období pro sledování splatnosti
11. V poli Období zadejte nový popis pro období pro sledování splatnosti.
12. Zavřete stránku.

## <a name="age-the-balances"></a>Splatnost zůstatku
1. Přejděte na Kredit a inkasa > Pravidelné úlohy > Splatné zůstatky odběratelů.
2. V poli Období pro sledování splatnosti vyberte definici období pro sledování splatnosti, kterou jste vytvořili.
    * Lze nastavit jeden aktivní snímek pro každou definici období pro sledování splatnosti.  
    * Ve výchozím nastavení se zpracují všichni odběratelé. Tento výběr můžete použít pro výpočet jednoho inkasního fondu zákazníků.  
    * Vyberte datum z transakce, kterou chcete použít pro sledování splatnosti.  
    * Vyberte pro sledování splatnosti možnost „k datu“. Výchozí hodnota je dnešní, ale při změně tohoto pole na Vybrané datum bude možné vybrat požadované datum. Pro dávkové zpracování použijte Dnešní datum.  
3. Rozbalte Rozsah společností. Můžete vybrat společnosti, které budou zahrnuty do snímku. Standardně je vybraná aktuální společnost.
4. Klepnutím na tlačítko OK spustíte zpracování snímku. Akce bude chvíli trvat. Počkejte, než zmizí posuvník, a zkontrolujte centrum zpráv, zda se vám nedoručila zpráva.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Prohlédnutí zůstatků na stránce se seznamem Splatné zůstatky a Kolekce
1. Přejděte do nabídky Kredit a inkasa > Inkasa > Splatné zůstatky.
    * Stránka seznamu zobrazí zůstatky pro odběratele. Ikona sledování splatnosti zobrazuje období pro sledování splatnosti nejstarší transakce.  
2. Vyberte odběratele se zůstatkem.
3. Rozbalte oblast okna s fakty Sledování splatnosti a prohlédněte si splatné zůstatky.
    * Definice období pro sledování splatnosti pro okno s fakty je převzata z výchozí definice období pro sledování splatnosti stanovené v parametrech. Její změna je možná pomocí nabídky Shromažďovat.  


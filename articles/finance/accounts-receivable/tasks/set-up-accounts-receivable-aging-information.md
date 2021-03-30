---
title: Nastavení a generování informací o splatnosti pohledávek
description: Tento průvodce vám pomůže nastavit definici sledování splatnosti, splatné zůstatky odběratelů a zobrazit zůstatky v seznamu Splatný zůstatek a na stránce Kolekce.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b21fe217aacd11821ff8d5cf7c7682b2181e36c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220076"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Nastavení a generování informací o splatnosti pohledávek

[!include [banner](../../includes/banner.md)]

Tento průvodce vám pomůže nastavit definici sledování splatnosti, splatné zůstatky odběratelů a zobrazit zůstatky v seznamu Splatný zůstatek a na stránce Kolekce. Tento záznam používá ukázkovou společnost USMF.


## <a name="create-an-aging-period-definition"></a>Vytvoření definice období pro sledování splatnosti
1. Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Nastavení > Definice období pro sledování splatnosti**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Období pro sledování splatnosti**.
4. Zadejte hodnotu do pole **Popis**.
5. Klepnutím na položku **Přidat níže** vložte nové období pro sledování splatnosti.
6. V poli **Období** zadejte popis, který se zobrazí v sestavách pro sledování splatnosti.
7. Do pole **Jednotka** zadejte číslo.
8. Vyberte volbu v poli **Interval**. Období hlavní knihy odpovídá období kalendáře hlavní knihy. Den, týden, měsíc, čtvrtletí a roky definují velikost intervalu podle typu data. Hodnota Neomezeno vybere všechny transakce před nebo po předchozím období v závislosti na tom, zda se jedná o první nebo poslední období.  
9. Vyberte volbu v poli **Indikátor sledování splatnosti**.
10. Vyberte období v horní části mřížky. Aktualizace popisu popisujícího nejstarší období v definici období pro sledování splatnosti
11. V poli **Období** zadejte nový popis pro období pro sledování splatnosti.
12. Zavřete stránku.

## <a name="age-the-balances"></a>Splatnost zůstatku
1. Přejděte na **Kredit a inkasa > Pravidelné úlohy > Splatné zůstatky odběratelů**.
2. V poli **Definice období pro sledování splatnosti** vyberte definici období pro sledování splatnosti, kterou jste vytvořili.
    + Lze nastavit jeden aktivní snímek pro každou definici období pro sledování splatnosti.  
    + Ve výchozím nastavení se zpracují všichni odběratelé. Tento výběr můžete použít pro výpočet jednoho inkasního fondu zákazníků.  
    + Vyberte datum z transakce, kterou chcete použít pro sledování splatnosti.  
    + Vyberte pro sledování splatnosti možnost „k datu“. Výchozí hodnota je dnešní, ale při změně tohoto pole na Vybrané datum bude možné vybrat požadované datum. Pro dávkové zpracování použijte Dnešní datum.  
3. Rozbalte rozsah **Společnost**. Můžete vybrat společnosti, které budou zahrnuty do snímku. Standardně je vybraná aktuální společnost.
4. Klepnutím na tlačítko **Ok** spustíte zpracování snímku. Akce bude chvíli trvat. Počkejte, než zmizí posuvník, a zkontrolujte centrum zpráv, zda se vám nedoručila zpráva.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>Prohlédnutí zůstatků na stránce se seznamem Splatné zůstatky a Kolekce
1. Přejděte do nabídky **Kredit a inkasa > Inkasa > Splatné zůstatky**. Stránka seznamu zobrazí zůstatky pro odběratele. Ikona sledování splatnosti zobrazuje období pro sledování splatnosti nejstarší transakce.  
2. Vyberte odběratele se zůstatkem.
3. Rozbalte oblast okna s fakty **Sledování splatnosti** a prohlédněte si splatné zůstatky. Definice období pro sledování splatnosti pro okno s fakty je převzata z výchozí definice období pro sledování splatnosti stanovené v parametrech. Její změna je možná pomocí nabídky Shromažďovat.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
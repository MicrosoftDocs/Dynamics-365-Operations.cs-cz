---
title: Vyhledání platných cen a slev
description: Tento postup popisuje vyhledání ceny a/nebo slevy produktu, které jsou aktuálně platné pro určitého odběratele, aniž by byla vytvořena prodejní objednávka.
author: omulvad
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d5188c4a0e06f116e1fdcab33546e3e0745c4f483c72f954b65b2307a683080
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753884"
---
# <a name="look-up-applicable-prices-and-discounts"></a>Vyhledání platných cen a slev

[!include [banner](../../includes/banner.md)]

Tento postup popisuje vyhledání ceny a/nebo slevy produktu, které jsou aktuálně platné pro určitého odběratele, aniž by byla vytvořena prodejní objednávka. Postup vás provede konkrétním příkladem a aby bylo možné vybrat potřebné hodnoty, je nutné v příkladu použít ukázkovou společnost USMF.


## <a name="find-the-applicable-price"></a>Vyhledání platné ceny
1. Přejděte do nabídky Prodej a marketing > Ceny a slevy > Vyhledat ceny.
2. V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. V seznamu vyhledejte a vyberte odběratele US-001.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Do pole Číslo položky zadejte T0004.
    * Ve výchozím nastavení je pole Množství nastaveno na hodnotu 1. Pokud však znáte velikost objednávky, kterou chce odběratel podat pro daný produkt, zadejte tuto hodnotu. Tyto informace jsou relevantní, pokud mají obchodní smlouvy s odběratelem množstevní kategorie, takže v případě, že cena závisí na minimálním nakoupeném množství.  
6. V poli Datum zadejte datum, kdy má odběratel podat objednávku. 
    * Datem může být aktuální den nebo jakékoli budoucí datum.  
    * Systém nyní vrátí cenu, která platí pro vybraný produkt při nákupu vybraným odběratelem ve vybrané datum a se zadaným množstvím. Pokud by v tomto příkladu odběratel US-001 koupil dnes 1 jednotku produktu T0004, bylo by mu účtováno 350 CAD za jednotku. Tato cena je převzata z existující a aktivní obchodní smlouvy s odběratelem.      Ostatní pole na stránce poskytují podrobnosti o ceně produktu a nákladech produktu (pokud to je nastaveno v základním produktu) a vypočtené ziskovosti.  
    * Je-li vybrána možnost Zobrazit související varianty produktu, znamená to, že existují další obchodní smlouvy pro varianty produktu.  
7. Klikněte na políčko Zobrazit související varianty produktu.
    * Zobrazí se seznam variant produktu a také informace o jejich dimenzích.  
8. V seznamu označte řádek představující bílou barvu.
    * Všimněte si, že cena produktu je nyní jiná než cena zobrazená dříve, když nebyla zadána pro dimenzi.  
9. Klikněte na možnost Zobrazit prodejní ceny.
    * Stránka Cena (prodej) zobrazí všechny obchodní smlouvy vztahující se k produktu, včetně jeho variant.  
10. Zavřete stránku.

## <a name="find-the-applicable-discount"></a>Vyhledání platné slevy
Ověřte, že pole Účet odběratele obsahuje číslo odběratele US-001.   
1. Do pole Číslo položky zadejte T0012.
    * Ujistěte se, že je v poli Množství nastavena hodnota 1.  
    * Následující podrobnosti o ceně zobrazené pro produkt T0012 pocházejí z jedné nebo více obchodních smluv: Jednotková cena je 1 000 CAD a procento slevy je 5.  
2. Nastavte množství na hodnotu 20.
    * Vyšší objednané množství způsobí, že se řádková sleva, která bude nabídnuta odběrateli, změní z 5 na 7 procent.  
    * Čistá částka se vypočítá na základě jednotkové ceny, slevy a celkového množství.  
3. Klikněte na možnost Zobrazit řádkovou slevu.
    * Jsou zde dvě smlouvy řádkových slev pro produkt T0012, kde je zadána sleva 5 procent pro množství na řádku objednávky od 1 do 10 a 7% sleva na množství objednávky vyšší než 10. Všimněte si, že slevy platí pro skupinu produktů, v tomto příkladu to je kód skupiny 01, do které produkt T0012 patří.  
4. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
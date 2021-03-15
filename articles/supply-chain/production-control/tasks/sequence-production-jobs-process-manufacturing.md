---
title: Seřazení výrobních úloh pro procesní výrobu
description: Tento postup používá barevné výrobky jako příklad popisující to, jak seřadit plánované objednávky podle priority barvy a velikosti obalu.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e22c767a3de8fd937d9032a5bf285dfb4ced3d55
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981049"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Seřazení výrobních úloh pro procesní výrobu

[!include [banner](../../includes/banner.md)]

Tento postup používá barevné výrobky jako příklad popisující to, jak seřadit plánované objednávky podle priority barvy a velikosti obalu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USPI. Tento postup je určen pro plánujícího produkce.


## <a name="run-master-planning-for-uspi"></a>Spuštění hlavního plánování pro USPI
1. Přejděte na Hlavní plánování > Hlavní plánování > Spustit > Hlavní plánování.
2. V poli Hlavní plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte MasterPlan.  
4. Klikněte na tlačítko OK.
    * Tím se spustí hlavní plánování, včetně zpracování pořadí. Tento proces může trvat několik minut.  

## <a name="view-planned-orders-for-the-paint-products"></a>Zobrazení plánovaných objednávek pro barevné výrobky
1. Přejděte na Hlavní plánování > Hlavní plánování > Plánované objednávky.
2. Rozbalte okno s fakty Podrobnosti o zboží.
3. Rozbalte okno s fakty Podrobnosti plánu.
4. V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte MasterPlan.  
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Použijte rychlý filtr k filtrování v poli Číslo položky na základě hodnoty P300.
    * Po odemknutí se přesuňte doprava a prohlédněte si datum objednávky a datum dodání. Všimněte si, že tyto položky mají datum objednávky Dnes, a data dodání pro plánované objednávky nejsou klasifikovány po prioritě barvy a velikosti balení, jak je uvedeno v názvu produktu. Můžete ponechat číslo položky a zobrazit tak název produktu a prioritu.  

## <a name="sequence-planned-orders-for-paint"></a>Seřazení plánovaných objednávek pro barvu
1. Zavřete stránku.
2. Přejděte na Hlavní plánování > Hlavní plánování > Plánovaná objednávka s klasifikací.
3. Rozbalte okno s fakty Podrobnosti o zboží.
4. Rozbalte okno s fakty Podrobnosti plánu.
    * Poznámka: v této části můžete vidět, že Počáteční datum a čas pro plánované objednávky je klasifikován podle barvy a velikosti obalu v rámci období intervalu 28 dnů. Tato období jsou definovány číslem v poli Kampaň. Formulář plánované objednávky s klasifikací funguje stejně jako typický formulář pro plánované objednávky, a plánovač výroby lze může potvrdit plánované objednávky.  
5. Označte všechny řádky.
6. Klepněte na možnost Akceptovat.
    * Dojde k aktualizaci plánovaných objednávek s vybranou akcí posloupnosti Odklady nebo Zálohy.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Kontrola seřazení plánovaných objednávek
1. Zavřete stránku.
2. Přejděte na Hlavní plánování > Hlavní plánování > Plánované objednávky.
3. Rozbalte okno s fakty Podrobnosti o zboží.
4. Rozbalte okno s fakty Podrobnosti plánu.
5. V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte MasterPlan.  
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Použijte rychlý filtr k filtrování v poli Číslo položky na základě hodnoty P300.
    * Všimněte si, že objednávky nyní jsou seřazeny podle priority barev a velikostí, a plánované objednávky začínají k prvnímu datu objednání a datu dodání. Ověřte údaje ve sloupci Datum objednávky nebo Počáteční datum v okně s fakty Podrobnosti plánu.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
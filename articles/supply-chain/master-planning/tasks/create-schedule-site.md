---
title: Vytvoření plánu pro pracoviště
description: Tento postup popisuje způsob plánování výrobních zakázek, které nebyly dosud pro pracoviště zahájeny.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0db5095020bc14d56ae3680e7d0caa68789180e
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469275"
---
# <a name="create-a-schedule-for-a-site"></a>Vytvoření plánu pro pracoviště

[!include [banner](../../includes/banner.md)]

Tento postup popisuje způsob plánování výrobních zakázek, které nebyly dosud pro pracoviště zahájeny.  K dokončení tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="identify-production-orders-that-are-not-started"></a>určení výrobních zakázek, které nebyly zahájeny
1. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Pracoviště pomocí hodnoty „1“.
    * 1 představuje pracoviště v rámci USMF. Pokud nepoužíváte USMF, vyberte pracoviště z vlastní společnosti.  
3. Otevřete filtr sloupce Stav.
4. Použijte filtr v poli Stav, s hodnotou Plánováno a za použití operátoru filtru „je přesně“.

## <a name="create-a-schedule"></a>Vytvoření plánu
1. V seznamu označte všechny řádky nebo jejich označení zrušte.
2. V podokně akcí klikněte na možnost Plán.
3. Klikněte na Plánovat úlohy.
4. V poli Způsob plánování vyberte „Zpět od data dodání“.
5. Vyberte Ne v poli Omezená kapacita.
6. Vyberte Ne v poli Omezený materiál.
7. Klikněte na tlačítko OK.
    * Tato operace může chvíli trvat.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Zobrazení výsledků naplánovaných výrobních zakázek
1. Označte v seznamu vybraný řádek.
    * Můžete označit libovolné řádky.  
2. V podokně akcí klikněte na položku Výrobní zakázka.
3. Klikněte na Všechny úlohy.
    * Na této stránce můžete vidět seznam úloh. Na kartě Plánování můžete zobrazit počáteční datum a koncové datum úlohy.  
4. Klepněte na Kusovníky.
    * Na této stránce se zobrazí odhad spotřeby materiálu pro operace ve výrobní zakázce, a aktuální dostupné zásoby.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
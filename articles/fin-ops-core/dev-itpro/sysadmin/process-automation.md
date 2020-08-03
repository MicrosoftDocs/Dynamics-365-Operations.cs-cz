---
title: Automatizace procesů
description: Toto téma uvádí podrobnosti o automatizace procesů, jež umožňuje jednoduše plánovat procesy, které budou spouštěny dávkovým serverem.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508178"
---
# <a name="process-automation"></a>Automatizace procesů

[!include[banner](../includes/banner.md)]

Automatizace procesů umožňuje jednoduše plánovat procesy, které budou spouštěny dávkovým serverem. Aktualizované kalendářové zobrazení naplánované práce umožňuje koncovým uživatelům prohlížet plánované a dokončené práce a provádět ve vztahu k nim různé akce.

## <a name="administration"></a>Správa

Centrální administrační stránka pro veškerou automatizaci procesů se nachází v modulu správy systému v nabídce **Nastavení**. Na této stránce najdete všechny automatizované procesy (řady), které jsou v systému nastaveny. Přímo z této stránky je též možné přidávat nové automatizace procesů. Po nastavení řady můžete z tohoto seznamu každou jednotlivou řadu spravovat. Můžete upravit celou řadu, smazat ji, zobrazit všechny výskyty jako seznam nebo řadu zakázat, chcete-li plánovanou práci na určitou dobu pozastavit. 

## <a name="calendar-view"></a>Kalendářové zobrazení 
Jednou z klíčových výhod automatizace procesů je možnost vidět plánovanou práci v jednoduchém kalendářovém zobrazení.  Toto zobrazení umožňuje zobrazit najednou práci na období jednoho týdne. Toto zobrazení uvidíte na pravé straně na stránce **Automatizace procesů**. Bude naplněno naplánovanou prací pro vybranou řadu. 

[![Kalendář automatizace procesů](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Změny výskytů
Každý výskyt lze upravit, aniž by to mělo vliv na jiné výskyty definované řadou, z níž daný výskyt pochází. Výskyt plánované práce lze upravit v kalendářovém zobrazení stiskem tlačítka **Zobrazit/upravit** a výběrem možnosti **Výskyt**. Získáte tak přístup ke všem nastavením původně zobrazeným v průvodci nastavením řady. Můžete provést jednorázovou změnu vybraného výskytu. Výskyt plánované práce lze také vypnout v kalendářovém zobrazení výběrem možnosti **Zakázat**. 

## <a name="developer-documentation"></a>Dokumentace pro vývojáře 
V současné době se zpracovává dokumentace pro vývojáře, která vývojářům umožní rámec automatizace procesů rozšířit. Tato dokumentace bude poskytovat informace o tom, jak vytvářet vlastní procesy, jež mají být spouštěny dávkovým serverem, jak je plánovat pomocí průvodce automatizací procesů a automaticky zobrazovat v kalendářovém zobrazení.
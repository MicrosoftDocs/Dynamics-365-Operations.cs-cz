---
title: Automatizace procesů
description: Tento článek uvádí podrobnosti o automatizace procesů, jež umožňuje jednoduše plánovat procesy, které budou spouštěny dávkovým serverem.
author: RyanCCarlson2
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 1a1d152a01e0ebe6a20e2e6b31f12ed7b8deb024
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2022
ms.locfileid: "9423952"
---
# <a name="process-automation"></a>Automatizace procesů

[!include[banner](../includes/banner.md)]

Automatizace procesů umožňuje jednoduše plánovat procesy, které budou spouštěny dávkovým serverem. Aktualizované kalendářové zobrazení naplánované práce umožňuje koncovým uživatelům prohlížet plánované a dokončené práce a provádět ve vztahu k nim různé akce.

## <a name="administration"></a>Správa

Centrální administrační stránka pro veškerou automatizaci procesů se nachází v modulu správy systému v nabídce **Nastavení**. Na této stránce najdete všechny automatizované procesy (řady), které jsou v systému nastaveny. Přímo z této stránky je též možné přidávat nové automatizace procesů. Po nastavení řady můžete z tohoto seznamu každou jednotlivou řadu spravovat. Můžete upravit celou řadu, smazat ji, zobrazit všechny výskyty jako seznam nebo řadu zakázat, chcete-li plánovanou práci na určitou dobu pozastavit. 

Použijte kartu **Procesy na pozadí** na této stránce pro správu všech procesů na pozadí, které jsou spuštěny ve vašem prostředí. Vyberte **Upravit** k provádění změn plánu pro jakýkoli proces na pozadí. Tyto změny mohou zahrnovat časové období spánku, které způsobí, že se proces „uspí“ nebo přeruší běh na určitou dobu každý den. Vyberte **Zobrazit nejnovější výsledky** pro zobrazení výsledků provádění pro každý proces na pozadí.

Všechny procesy, které jsou zakázány ve správě prvků, se po deaktivaci funkce nezobrazí. Navíc plánovací modul automatizace procesů nebude plánovat žádné události ani procesy na pozadí pro zakázanou funkci. Opětovné povolení funkce způsobí okamžité spuštění všech minulých naplánovaných událostí nebo procesů na pozadí. Proces plánování automatizace procesů se potřebuje mít spuštěnou dávkovou úlohu systému **Úloha systému dotazování na automatizaci procesů**. Úloha by neměla být nikdy měněna nebo upravována. Pokud tato dávková úloha neběží nebo je v chybovém stavu, vyberte **Inicializovat automatizaci procesů** k resetování dávkové úlohy. Tento reset zajišťuje, že všechny nové automatizace vydané v novější verzi aplikace budou inicializovány. 

## <a name="calendar-view"></a>Kalendářové zobrazení

Jednou z klíčových výhod automatizace procesů je možnost vidět plánovanou práci v jednoduchém kalendářovém zobrazení.  Toto zobrazení umožňuje zobrazit najednou práci na období jednoho týdne. Toto zobrazení uvidíte na pravé straně na stránce **Automatizace procesů**. Bude naplněno naplánovanou prací pro vybranou řadu. 

[![Kalendář automatizace procesů.](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Změny výskytů

Každý výskyt lze upravit, aniž by to mělo vliv na jiné výskyty definované řadou, z níž daný výskyt pochází. Výskyt plánované práce lze upravit v kalendářovém zobrazení stiskem tlačítka **Zobrazit/upravit** a výběrem možnosti **Výskyt**. Získáte tak přístup ke všem nastavením původně zobrazeným v průvodci nastavením řady. Můžete provést jednorázovou změnu vybraného výskytu. Výskyt plánované práce lze také vypnout v kalendářovém zobrazení výběrem možnosti **Zakázat**.

## <a name="developer-documentation"></a>Dokumentace pro vývojáře

Rámec automatizace procesů umožňuje vývojářům rozšířit rámec automatizace procesů. Dokumentace k [rámci automatizace procesu](../process-automation/process-automation-framework.md) poskytuje informace o tom, jak vytvářet vlastní procesy, jež mají být spouštěny dávkovým serverem, jak je plánovat pomocí průvodce automatizací procesů a automaticky zobrazovat v kalendářovém zobrazení.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

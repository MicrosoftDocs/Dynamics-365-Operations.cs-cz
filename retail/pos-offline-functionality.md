---
title: "Funkcí POS offline"
description: "V tomto článku jsou informace o offline režimu pro Retail Modern POS, ve kterém se zařízeních POS automaticky přepínají z databáze kanálů na offline databázi, není-li maloobchodní server k dispozici. Tento článek také obsahuje informace o obecném nastavení offline režimu a vysvětlení synchronizace dat mezi offline databází a databází kanálů."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>Funkcí POS offline

[!include[banner](includes/banner.md)]


V tomto článku jsou informace o offline režimu pro Retail Modern POS, ve kterém se zařízeních POS automaticky přepínají z databáze kanálů na offline databázi, není-li maloobchodní server k dispozici. Tento článek také obsahuje informace o obecném nastavení offline režimu a vysvětlení synchronizace dat mezi offline databází a databází kanálů.

<a name="overview"></a>Přehled
--------

V Retail POS moderní místa prodeje (POS) zařízení přejde do režimu offline při každém maloobchodní server není k dispozici. Proto pokud dojde ke ztrátě spojení se serverem maloobchodu, moderní Retail POS automaticky přepne do offline databáze. Během prodejní transakce, pokud požadavek na data není úspěšně vyřešen v určeném časovém limitu nakonfigurovaném v offline profilu, aplikace Retail Modern POS se automaticky přepne do offline databáze a pokračuje v prodejní transakci. Když je zařízení POS v offline režimu, aplikace Retail Modern POS se pokusí připojit k serveru maloobchodu po intervalu pokusu o obnovení připojení, který je konfigurován v offline profilu. Tento pokus o opětovné připojení proběhne pouze na začátku transakce.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>Určení způsobu připojení aplikace Retail Modern POS

Stavové záhlaví v programu Retail Modern POS určuje aktuální stav připojení a okno **Stav připojení** zobrazuje stav posledního pokusu o synchronizaci s offline databází. [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Vytváření tlačítka k ručnímu přepínání mezi režimem online a offline

Můžete přidat tlačítko do aplikace Retail Modern POS k ručnímu přepínání mezi režimem online a offline. Vytvořte tlačítko pro POS operaci **917 – Stav připojení databáze**. Název tohoto tlačítka je **Odpojit**, když je aplikace Retail Modern POS připojena k serveru maloobchodu, a **Připojit**, když je odpojena. Toto tlačítko lze použít k zobrazení připojení a odpojení od serveru maloobchodu nebo k jeho připojení. [![V programu Retail POS moderní tlačítko Odpojit](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Nastavení
Povolit podporu offline pro POS zařízení (registr), nastavte **podporu offline** možnost na **Ano** na **registrovat** stránky. Vytvoření nové entity databáze kanálu je vytvořen a přidán do skupiny dat kanálu obchodu. Poté spusťte všechny požadované plány distribuce a vygenerujte balíčky dat pro offline databázi. Dále nainstalujte offline verze programu Retail POS moderní. Proces instalace vytvoří databáze v režimu offline. Navíc nainstalujte Microsoft SQL Server 2014 Express je-li požadováno. Offline synchronizace dat se spustí po prvním přihlášení k programu Retail Modern POS.

## <a name="data-synchronization"></a>Synchronizace dat
Maloobchodní plánovač slouží k odeslání hlavních dat do offline databáze. Ve výchozím nastavení při spuštění plánu distribuce budou změny dat odeslány do databáze kanálu a offline databáze. Aplikace Retail Modern POS zahrnuje asynchronní knihovnu synchronizace, která stahuje všechny dostupné balíčky dat a vloží je do offline databáze. Jsou-li transakce vytvořeny offline, aplikace Retail Modern POS je odešle na server maloobchodu, aby je bylo možné vložit do databáze kanálů. Offline synchronizace dat může být provedena pouze v případě, že je spuštěna aplikace Retail Modern POS. [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)





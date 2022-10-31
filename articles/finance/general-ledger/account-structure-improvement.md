---
title: Vylepšení výkonu aktivace účetní struktury
description: Tento článek vysvětluje nové vylepšení výkonu procesu aktivace účetní struktury.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713992"
---
# <a name="account-structure-activation-performance-enhancement"></a>Vylepšení výkonu aktivace účetní struktury

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Toto vylepšení výkonu umožňuje rychleji aktivovat účetní struktury tím, že spustí více aktualizací transakcí najednou. Kromě toho je samotná struktura po ověření označena jako aktivní. Zpracování transakcí může pokračovat, zatímco stávající nezaúčtované transakce jsou aktualizovány na novou strukturu. Protože aktualizace transakcí může nějakou dobu trvat, můžete stav své aktivace sledovat výběrem možnosti **Zobrazit stav aktivace** nad mřížkou na stránce **Účetní struktury**. Stav aktivace můžete zobrazit také tím, že na panelu akcí vyberete možnost **Zobrazit** a v rozevírací nabídce vyberete možnost **Stav aktivace**.

[![Stránka účetních struktur.](./media/AccountStructure1.png)](./media/AccountStructure1.png)

Po výběru možnosti **Zobrazit stav aktivace** se zobrazí dialogové okno se zobrazením jednotlivých úloh, které probíhají v rámci procesu aktivace. U každého úkolu můžete zobrazit jeho stav a po jeho dokončení datum a čas dokončení.

[![Časová osa aktivace účetní struktury.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Tipy pro aktivaci účetní struktury

Dialogové okno aktivace účetní struktury, které se zobrazí po výběru možnosti **Aktivovat** koncept účetní struktury, obsahuje sekci karty s názvem **Aktualizovat nezaúčtované transakce**. Tato sekce obsahuje možnost s názvem **Vynutit aktualizaci**. Tuto možnost můžete zvolit pro aktualizaci všech nezaúčtovaných transakcí do aktuální struktury. Tuto možnost byste však měli použít pouze v případě, že došlo k chybě nebo vám ji nařídila podpora Microsoftu.

Níže jsou uvedeny některé faktory, které mohou ovlivnit výkon procesu aktivace:

- Velký počet nezaúčtovaných záznamů deníku.
- Velké množství záznamů opensourcových dokumentů, jako jsou faktury s volným textem, faktury dodavatelů a související dokumenty, které využívají architekturu zdrojových dokumentů a mají otevřené rozúčtování.
- Množství dat v TaxUncommitted.
- Množství otevřených rozpočtových dat.
- Import dat deníku v době, kdy aktivační úlohy stále probíhají.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

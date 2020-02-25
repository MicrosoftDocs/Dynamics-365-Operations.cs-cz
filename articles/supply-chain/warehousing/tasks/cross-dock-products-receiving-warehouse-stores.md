---
title: Používání cross dockingu pro distribuci produktů z přijímacího skladu do obchodů
description: Tato procedura vás provede postupem, jak vytvořit a zpracovat cross docking k distribuci produktů ze skladové místa příjmů nákupní objednávky do jednoho nebo více obchodů.
author: ShylaThompson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f38c2ad9561cc1a1c775c27aec54681124cffeec
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004081"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>Používání cross dockingu pro distribuci produktů z přijímacího skladu do obchodů

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura vás provede postupem, jak vytvořit a zpracovat cross docking k distribuci produktů ze skladové místa příjmů nákupní objednávky do jednoho nebo více obchodů. Můžete definovat více konfigurací a nechat systém navrhovat, jak budou produkty distribuovány, nebo ručně zadat, kam budou produkty distribuovány a kolik jich bude distribuováno do jednotlivých obchodů. Procedura neobsahuje nastavení dat, která lze použít pro cross docking, jako jsou například pravidla doplnění, organizační hierarchie a skladovací hmotnosti. Procedura používá ukázkovou společnost USRT.

1. Přejděte na Všechny nákupní objednávky.
2. Vyberte nákupní objednávku ze seznamu a kliknutím na odkaz ji otevřete.
3. V podokně akcí klikněte na Retail and Commerce.
4. Klikněte na Cross docking.
5. Klikněte na možnost Upravit.
    * Kategorie lze použít k filtrování položek v části Řádky.  
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. V poli Množství pro cross docking zadejte hodnotu, která určuje, jaká část zakoupeného množství vybraného produktu by měla být distribuována.
8. Do pole Další množství pro cross docking zadejte hodnotu, která určuje množství pro distribuci dostupných produktů, které jsou kupovány.
9. V poli Distribuce zadejte „Váha místa“.
    * Můžete vybrat ostatní typy pro používání různých pravidel pro distribuci.  
10. V poli Hierarchie doplnění zadejte nebo vyberte hodnotu.
11. Vyberte možnost Ano v poli Uznat sortimenty.
12. Klikněte na Výpočet množství.
13. Klepněte na Vytvořit objednávku.
14. Klepněte na tlačítko Ano.
15. Vyhledejte a vyberte na seznamu sklad, který obdržel produkty.
16. Klikněte na objednávku, abyste zobrazili objednávky, které byly vytvořeny pro vybraný sklad.


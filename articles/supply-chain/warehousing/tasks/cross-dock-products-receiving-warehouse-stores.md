---
title: Používání cross dockingu pro distribuci produktů z přijímacího skladu do obchodů
description: Tato procedura vás provede postupem, jak vytvořit a zpracovat cross docking k distribuci produktů ze skladové místa příjmů nákupní objednávky do jednoho nebo více obchodů.
author: Mirzaab
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e65535a1879eab229f185e0e97d81a304fd292d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572954"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>Používání cross dockingu pro distribuci produktů z přijímacího skladu do obchodů

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
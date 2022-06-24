---
title: Dostupnost zásob v dvojitém zápisu
description: Tento článek obsahuje informace o kontrole dostupnosti zásob ve dvojím zapisování.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: efd175dfbe49549561bdb7d697c8bc47016f1d5d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908255"
---
# <a name="inventory-availability-in-dual-write"></a>Dostupnost zásob v dvojitém zápisu

[!include [banner](../../includes/banner.md)]

Pomocí dostupnosti zásob můžete zkontrolovat své zásoby před přidáním produktu do formulářů **Nabídky**, **Objednávky** nebo **Faktury** v modelem řízených aplikacích v Microsoft Dynamics 365 Sales. Například kontrolujete zásoby a určíte, že jednou z klíčových úloh ve [zpeněžení potenciálního zákazníka](dual-write-prospect-to-cash.md) je určení data plnění.

Pokud nemáte dostatek zásob, můžete odhadnout datum dodání na základě předpokládaných příjmů a problémů se zásobami. Můžete také zkontrolovat dostupné informace o produktu Lze slíbit (ATP), kde najdete množství ATP v předem definované ochranné době.

## <a name="on-hand-inventory"></a>Zásoby na skladě

V Dynamics 365 Sales bylo přidáno nové tlačítko **Zásoby na skladě** do záhlaví stránek **Nabídky**, **Objednávky** a **Faktury**. Po výběru tohoto tlačítka se zobrazí dialogové okno, kde můžete určit společnost a produkt, u kterého chcete zkontrolovat zásoby na skladě. Toto dialogové okno zobrazuje stejné informace jako [Zásoby na skladě](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Dialogové okno vrací informace o zásobách z Dynamics 365 Supply Chain Management. Tato informace obsahuje následující množství:

- Množství na skladě
- Rezervované množství na skladě
- Dostupné množství na skladě
- Objednané množství
- Množství na objednávce
- Rezervované objednané množství
- Celkové dostupné množství

## <a name="atp-information"></a>Informace ATP

Do aplikace Sales bylo přidáno nové tlačítko **Informace ATP** k položkám řádku na stránkách **Nabídky**, **Objednávky** a **Faktury**. Po výběru tlačítka se zobrazí dialogové okno, kde můžete určit společnost, produkt, skladové pracoviště, sklad zásob a množství na objednávce. Toto dialogové okno má stejná nastavení, jaká jsou popsána v části [Příslib objednávky](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Dialogové okno vrací informace ATP ze Supply Chain Management. Tato informace obsahuje následující množství:

- Množství ATP
- Množství příjmu
- Množství výdeje
- Množství na skladě

## <a name="how-it-works"></a>Jak to funguje

Když vyberete tlačítko **Zásoby na skladě** na stránce **Nabídky**, **Objednávky** nebo **Faktury**, provede se živé volání rozhraní API duálního zápisu **Zásoby na skladě**. API vypočítá zásoby na skladě pro daný produkt. Výsledek se uloží do tabulek **InventCDSInventoryOnHandRequestEntity** a **InventCDSInventoryOnHandEntryEntity** a poté se zapíše do Dataverse duálním zápisem. Chcete-li použít tuto funkci, musíte spustit následující mapy duálního zápisu. Při spuštění map přeskočte počáteční synchronizaci.

- Ruční záznamy o zásobách CDS (msdyn_inventoryonhandentries)
- Ruční žádosti o zásoby CDS (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Šablony

Následující šablony jsou k dispozici pro vystavení údajů o přímých zásobách.

Aplikace Finance and Operations | Aplikace Customer Engagement     | popis
---|---|---
[Položky zásob na skladě CDS](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[Požadavky na zásoby na skladě CDS](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

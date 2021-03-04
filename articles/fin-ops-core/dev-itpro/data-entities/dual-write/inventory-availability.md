---
title: Dostupnost zásob v dvojitém zápisu
description: Toto téma obsahuje informace o kontrole dostupnosti zásob ve dvojím zapisování.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4450575"
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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
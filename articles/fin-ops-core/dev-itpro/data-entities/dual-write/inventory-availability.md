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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426975"
---
# <a name="inventory-availability"></a>Dostupnost zásob

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Pomocí dostupnosti zásob můžete zkontrolovat své zásoby před přidáním produktu do formulářů **Nabídky**, **Objednávky** nebo **Faktury** v modelem řízených aplikacích v Dynamics 365. Například kontrola zásob a určení data plnění je klíčovým úkolem v procesu [zpeněžení potenciálního zákazníka](dual-write-prospect-to-cash.md). Pokud nemáte dostatek zásob, můžete odhadnout datum dodání na základě předpokládaných příjmů a problémů se zásobami. Můžete také zkontrolovat dostupné informace o produktu Lze slíbit (ATP), kde najdete množství ATP v předem definované ochranné době.

## <a name="on-hand-inventory"></a>Zásoby na skladě 

V záhlaví formulářů **Nabídky**, **Objednávky** nebo **Faktury** v Dynamics 365 Sales je přidáno nové tlačítko **Zásoby na skladě**. Po kliknutí na tlačítko se zobrazí dialogové okno a můžete určit společnost a produkt, u kterého chcete zkontrolovat zásoby na skladě. Vrací informace o zásobách z Dynamics 365 Supply Chain Management a zobrazuje stejné informace jako [Zásoby na skladě](../../../../supply-chain/inventory/tasks/check-availability-stock.md). Informace zahrnují tato množství:

- **Množství na skladě**
- **Rezervované množství na skladě**
- **Dostupné množství na skladě**
- **Množství objednávky**
- **Množství na objednávce.**
- **Rezervované objednané množství**
- **Celkové dostupné množství**

## <a name="atp-information"></a>Informace ATP

Položkám na řádcích formulářů **Nabídky**, **Objednávky** nebo **Faktury** v Dynamics 365 Sales je přidáno nové tlačítko **Informace ATP**. Po kliknutí na tlačítko se zobrazí dialogové okno a můžete určit společnost a produkt, Skladové pracoviště, sklad zásob a množství na objednávce. Vrací **Informace ATP** ze Supply Chain Management a zobrazuje nastavení popsaná v [Příslibu objednávky](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations). Tyto informace zahrnují **Množství ATP**, **Přijaté množství**, **Vydané množství**, a **Množství na skladě**.

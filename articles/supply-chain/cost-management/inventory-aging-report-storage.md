---
title: Uložení sestavy stáří zásob
description: V tomto článku je popsána funkce, která umožňuje spustit sestavu sledování splatnosti zásob a zpřístupnit výstup jako formulář a graf.
author: JennySong-SH
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d810ec90c85f2f7758ec01ef4b24611e026cc80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875561"
---
# <a name="inventory-aging-report-storage"></a>Uložení sestavy stáří zásob

[!include [banner](../includes/banner.md)]

V aplikaci Microsoft Dynamics 365 Supply Chain Management můžete spustit sestavu **Úložiště sestavy prodlení zásob** a zpřístupnit výstup jako formulář a graf. Ve formuláři jsou sloupce a agregované zůstatky v závislosti na konfigurovaném rozvržení dynamicky upravovány. Graf poskytuje vizuální přehled, který podporuje filtrování a umožňuje důkladné procházení podrobností. Dále vám datová entita nazvaná **Sestava zastarávání zásad** umožňuje exportovat výsledky sestavy **Úložiště sestavy prodlení zásob** spuštění ve formátu, jako je soubor Microsoft Excel nebo PDF.

Tato metoda spuštění sestavy **Úložiště sestavy prodlení zásob** je užitečná v případech, kdy výstup obsahuje mnoho řádků. Výstup bude například obsahovat mnoho řádků, pokud máte 50 000 položek a 300 obchodů, které jsou vytvořeny jako sklady, a požadujete splatnost zásob podle položky, pracoviště a skladu.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Povolení funkce sestavy úložiště hodnot zásob

Než můžete použít tuto funkci, musíte ji povolit ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby. Tato funkce je uvedena jako:

- **Modul** - Správa nákladů
- **Název funkce** - Úložiště sestavy prodlení zásob

## <a name="run-an-inventory-aging-report-storage"></a>Spuštění úložiště sestavy prodlení zásob

1. Přejděte na **Správa zásob \> Dotazy a sestavy \> Úložiště sestavy zastarávání zásob**.
1. Zvolte **Nové**.
1. V poli **Identifikátor procesu - název** zadejte jedinečný název sestavy.
1. Vyberte sestavu **Identifikace – ID** a filtrujte ji podle potřeby.

    Spuštění sestavy je vždy provedeno v dávkové úloze.

1. Po dokončení dávkové úlohy se výstup zobrazí na stránce **Úložiště sestavy prodlení zásob**.
1. Chcete-li zobrazit výstup jako formulář s tradičním rozvržením mřížky, vyberte možnost **zobrazit podrobnosti**. Chcete-li zobrazit výstup jako agregovaný graf, vyberte možnost **zobrazit graf**.

    > [!NOTE]
    > Ve formuláři nebudou zahrnuty mezisoučty definované v rozvržení sestavy.

Datová entita **Sestava prodlení zásob** umožňuje exportovat výstup sestavy **Úložiště sestavy prodlení zásob** použitím filtru pro pole **Identifikátor procesu – název** na libovolný formát, který správa dat podporuje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
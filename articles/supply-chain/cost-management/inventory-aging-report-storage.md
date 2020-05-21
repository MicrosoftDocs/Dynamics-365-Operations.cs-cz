---
title: Uložení sestavy stáří zásob
description: V tomto tématu je popsána funkce, která umožňuje spustit sestavu sledování splatnosti zásob a zpřístupnit výstup jako formulář a graf.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e68833cc2b4430f66419a67b1cba5f6c8c209f4
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323616"
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

---
title: Sestava prodlení zásob
description: V tomto tématu je popsána funkce, která umožňuje spustit sestavu sledování splatnosti zásob a zpřístupnit výstup jako formulář a graf.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810244"
---
# <a name="inventory-aging-report"></a>Sestava prodlení zásob


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

V aplikaci Microsoft Dynamics 365 Supply Chain Management můžete spustit sestavu **Prodlení zásob** a zpřístupnit výstup jako formulář a graf. Ve formuláři jsou sloupce a agregované zůstatky v závislosti na konfigurovaném rozvržení dynamicky upravovány. Graf poskytuje vizuální přehled, který podporuje filtrování a umožňuje důkladné procházení podrobností. Dále vám datová entita nazvaná **Sestava zastarávání zásad** umožňuje exportovat výsledky sestavy **Prodlení zásob** spuštění ve formátu, jako je soubor Microsoft Excel nebo PDF.

Tato metoda spuštění sestavy **Prodlení zásob** je užitečná v případech, kdy výstup obsahuje mnoho řádků. Výstup bude například obsahovat mnoho řádků, pokud máte 50 000 položek a 300 obchodů, které jsou vytvořeny jako sklady, a požadujete splatnost zásob podle položky, pracoviště a skladu.

## <a name="run-an-inventory-aging-report"></a>Spuštění sestavy prodlení zásob

1. Přejděte na **Správa zásob \> Dotazy a sestavy \> Úložiště sestavy zastarávání zásob**.
1. Zvolte **Nové**.
1. V poli **Identifikátor procesu - název** zadejte jedinečný název sestavy.
1. Vyberte sestavu **Identifikace – ID** a filtrujte ji podle potřeby.

    Spuštění sestavy je vždy provedeno v dávkové úloze.

1. Po dokončení dávkové úlohy se výstup zobrazí na stránce **Úložiště sestavy prodlení zásob**.
1. Chcete-li zobrazit výstup jako formulář s tradičním rozvržením mřížky, vyberte možnost **zobrazit podrobnosti**. Chcete-li zobrazit výstup jako agregovaný graf, vyberte možnost **zobrazit graf**.

    > [!NOTE]
    > Ve formuláři nebudou zahrnuty mezisoučty definované v rozvržení sestavy.

Datová entita **Sestava prodlení zásob** umožňuje exportovat výstup sestavy **Zastarávání zásob** použitím filtru pro pole **Identifikátor procesu – název** na libovolný formát, který správa dat podporuje.

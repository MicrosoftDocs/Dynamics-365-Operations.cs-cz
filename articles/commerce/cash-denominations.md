---
title: Konfigurace nominálních hodnot hotovosti pro pokladní místo (POS)
description: Nominální hodnoty hotovosti pro bankovky a mince lze definovat v účetním systému, aby je mohli používat pokladníci, zaměstnanci a manažeři v obchodě z POS.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 356552fd1c2001619785b6a03b8ec4cba92725da
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351314"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>Konfigurace nominálních hodnot hotovosti pro pokladní místo (POS)

[!include [banner](includes/banner.md)]

Nominální hodnoty hotovosti pro bankovky a mince lze definovat v účetním systému, aby je mohli používat pokladníci, zaměstnanci a manažeři v obchodě z POS. Tyto nominální hodnoty lze použít pro pomoc při inventuře hotovosti pro výkazy úhrad na konci dne nebo pro rychlé úhrady prodeje.

## <a name="define-denominations"></a>Definování nominálních hodnot

Nominální hodnoty se nastavují na úrovni obchodu v možnosti **Nastavit** \> **Výkaz hotovosti** ze stránky vlastnosti obchodu.

![Možnost výkazu hotovosti.](./media/image1-denomination.png)

Jak definovat nominální hodnotu:

1. Klepněte na možnost **Nový**.
1. Zadejte typ (mince nebo bankovka).
1. Zadejte částku (hodnota).

![Stránka nominální hodnoty výkazu hotovosti.](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Konfigurace funkčního profilu

Při platbě hotovosti v POS může uživatel použít nominální hodnoty k rychlému zadání částky placené odběratelem. Ve funkčním profilu můžete nakonfigurovat dvě možnosti pro zobrazení nominálních hodnot v POS.

- **Větší nebo rovno splatné částce** - Ve výchozím nastavení POS zobrazí pouze nominálních hodnoty, které jsou větší než splatná částka, což umožňuje úhradu jedním dotykem. Pokud je například dlužná částka 7,5 USD, POS zobrazí následující nominální hodnoty: 10 USD, 20 USD, 50 USD a 100 USD. Dotyk jedné z těchto částek automaticky uhradí prodej za tuto částku. Bankovky 1 USD a 5 USD se nezobrazují, protože tyto částky jsou menší než částka k zaplacení.
- **Všechny nominální hodnoty** - Zvolte tuto možnost, aby se vždy zobrazily všechny nominální hodnoty v POS, bez ohledu částku k úhradě. To znamená, že uživatel může použít kombinaci bankovek k dosažení splatné částky. Například pokud je dlužná částka 25,00 USD, uživatel si může zvolit 20 USD a 5 USD k dokončení prodeje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Konfigurace nominálních hodnot hotovosti pro pokladní místo (POS)
description: Nominální hodnoty hotovosti pro bankovky a mince lze definovat v účetním systému, aby je mohli používat pokladníci, zaměstnanci a manažeři v obchodě z POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: b2fb6676f45bc7efa4652de60e829b507292ac37
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213179"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>Konfigurace nominálních hodnot hotovosti pro pokladní místo (POS)

[!include [banner](includes/banner.md)]

Nominální hodnoty hotovosti pro bankovky a mince lze definovat v účetním systému, aby je mohli používat pokladníci, zaměstnanci a manažeři v obchodě z POS. Tyto nominální hodnoty lze použít pro pomoc při inventuře hotovosti pro výkazy úhrad na konci dne nebo pro rychlé úhrady prodeje.

## <a name="define-denominations"></a>Definování nominálních hodnot

Nominální hodnoty se nastavují na úrovni obchodu v možnosti **Nastavit** \> **Výkaz hotovosti** ze stránky vlastnosti obchodu.

![Možnost výkazu hotovosti](./media/image1-denomination.png)

Jak definovat nominální hodnotu:

1. Klepněte na možnost **Nový**.
1. Zadejte typ (mince nebo bankovka).
1. Zadejte částku (hodnota).

![Stránka nominální hodnoty výkazu hotovosti](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Konfigurace funkčního profilu

Při platbě hotovosti v POS může uživatel použít nominální hodnoty k rychlému zadání částky placené odběratelem. Ve funkčním profilu můžete nakonfigurovat dvě možnosti pro zobrazení nominálních hodnot v POS.

- **Větší nebo rovno splatné částce** - Ve výchozím nastavení POS zobrazí pouze nominálních hodnoty, které jsou větší než splatná částka, což umožňuje úhradu jedním dotykem. Pokud je například dlužná částka 7,5 USD, POS zobrazí následující nominální hodnoty: 10 USD, 20 USD, 50 USD a 100 USD. Dotyk jedné z těchto částek automaticky uhradí prodej za tuto částku. Bankovky 1 USD a 5 USD se nezobrazují, protože tyto částky jsou menší než částka k zaplacení.
- **Všechny nominální hodnoty** - Zvolte tuto možnost, aby se vždy zobrazily všechny nominální hodnoty v POS, bez ohledu částku k úhradě. To znamená, že uživatel může použít kombinaci bankovek k dosažení splatné částky. Například pokud je dlužná částka 25,00 USD, uživatel si může zvolit 20 USD a 5 USD k dokončení prodeje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Skrytí způsobů dodání mimo dopravce z možností dodávky v POS
description: V tomto tématu je popsána možnost konfigurace, která může zabránit zobrazení režimů dodání mimo dopravce pro výběr, když jsou v aplikaci pokladní místo (POS) vytvořeny objednávky dodávky.
author: hhainesms
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: a5f08fc86dc093fd0ead219b808fa720a43f6b6b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797111"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Skrytí způsobů dodání mimo dopravce z možností dodávky v POS


[!include [banner](includes/banner.md)]

Toto téma popisuje možnost konfigurace, která je k dispozici pro aplikaci v pokladním místě (POS). Tato možnost konfigurace mění chování při výběru způsobu dodání v případě, že objednávky dodávek jsou vytvořeny v POS.

Když uživatelé vytvářejí objednávky dodávek odběratele v POS, mohou vybrat způsob dodání pro danou dodávku. Tato funkce je k dispozici bez ohledu na to, zda je právě expedována celá objednávka nebo pouze vybrané řádky.

Ve výchozím nastavení jsou v dialogovém okně, ve kterém je vybrán způsob dodání, zobrazeny všechny platné způsoby dodání pro kombinaci kanálu, položky a dodací adresy. Tyto způsoby dodání jsou definovány na stránce **Způsoby dodání** v Headquarters (**Prodej a marketing \> Nastavení \> Distribuce \> Režimy dodání**). REžimy dodání momo dopravce, například **Carryout** nebo **Pickup**, se mohou v dialogovém okně rovněz zobrazit pro výběr.

Byla však přidána funkce, která umožňuje skrýt režimy dodání mimo dopravce v dialogovém okně. Chcete-li tuto funkci zapnout, na stránce **Parametry Commerce** na kartě **Objednávky zákazníka** nastavte možnost **Zobrazit pouze režim dopravce možnosti pro dodací objednávky** na **Ano**. Po zapnutí této funkce a spuštění příslušných distribučních úloh za účelem synchronizace informací do databáze kanálů se při procesu vytváření objednávek dodávek v POS nezobrazí režimy dodání mimo dopravce jako možnost k výběru.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
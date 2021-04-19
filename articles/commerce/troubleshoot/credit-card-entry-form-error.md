---
title: Na stránce zadání kreditní karty se při placení zobrazuje chyba
description: Toto téma poskytuje pokyny k řešení potíží, které mohou pomoci, když se nenačte část Platební metoda, a zobrazuje chybovou zprávu.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d2c5f01d17df79c9b23fd513aaeb5c0605d657e9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801764"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Na stránce zadání kreditní karty se při placení zobrazuje chyba

[!include [banner](../../includes/banner.md)]

Toto téma poskytuje pokyny k řešení potíží, které mohou pomoci, když se nenačte část **Platební metoda**, a zobrazuje chybovou zprávu.

## <a name="description"></a>popis

Když otevřete stránku pokladny online obchodu, část **Způsob platby** se nenačte a zobrazí se následující chybová zpráva: „Něco se pokazilo. Prosím zkuste to znovu později.“

![Chyba platebního modulu](media/payment-module-error.jpg)

## <a name="resolution"></a>Rozlišení

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Počkejte, než vyprší platnost mezipaměti Commerce Scale Unit

Nastavení platebních služeb na stránce pokladny internetového obchodu jsou uložena v mezipaměti v jednotce Commerce Scale Unit a jejich zobrazení na webu elektronického obchodování může trvat až 15 minut. Tato nastavení platebních služeb zahrnují změny ID obchodního účtu, klíče cloudového API a různá nastavení konfigurace, která souvisí s platební metodou.

## <a name="additional-resources"></a>Další prostředky

[Nastavení online kanálu](../channel-setup-online.md)

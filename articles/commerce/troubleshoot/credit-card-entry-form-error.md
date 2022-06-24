---
title: Na stránce zadání kreditní karty se při placení zobrazuje chyba
description: Tento článek poskytuje pokyny k řešení potíží, které mohou pomoci, když se nenačte část Platební metoda, a zobrazuje chybovou zprávu.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 6d1f7ba2d1a63430431af94ed4bed3222c85f14d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910436"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Na stránce zadání kreditní karty se při placení zobrazuje chyba

[!include [banner](../../includes/banner.md)]

Tento článek poskytuje pokyny k řešení potíží, které mohou pomoci, když se nenačte část **Platební metoda**, a zobrazuje chybovou zprávu.

## <a name="description"></a>popis

Když otevřete stránku pokladny online obchodu, část **Způsob platby** se nenačte a zobrazí se následující chybová zpráva: „Něco se pokazilo. Prosím zkuste to znovu později.“

![Chyba platebního modulu.](media/payment-module-error.jpg)

## <a name="resolution"></a>Řešení

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Počkejte, než vyprší platnost mezipaměti Commerce Scale Unit

Nastavení platebních služeb na stránce pokladny internetového obchodu jsou uložena v mezipaměti v jednotce Commerce Scale Unit a jejich zobrazení na webu elektronického obchodování může trvat až 15 minut. Tato nastavení platebních služeb zahrnují změny ID obchodního účtu, klíče cloudového API a různá nastavení konfigurace, která souvisí s platební metodou.

## <a name="additional-resources"></a>Další prostředky

[Nastavení online kanálu](../channel-setup-online.md)

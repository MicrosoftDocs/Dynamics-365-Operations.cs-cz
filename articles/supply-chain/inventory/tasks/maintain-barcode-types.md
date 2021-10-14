---
title: Udržování typů čárových kódů
description: Tento postup popisuje, jak nastavit novou definici čárového kódu, který lze použít v rámci sestavy seznamu výdejek.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b689d1fc85d59ac87efa1903fd7122ae5ff011da
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571106"
---
# <a name="maintain-bar-code-types"></a>Udržování typů čárových kódů

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak nastavit novou definici čárového kódu, který lze použít v rámci sestavy seznamu výdejek. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat. Pokud používáte USMF, můžete použít ukázkové hodnoty, které jsou zobrazeny. Tyto úkoly obvykle provádějí vedoucí skladu.

1. Přejděte k **čárovým kódům**.
1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **Nastavení čárového kódu**.
1. Zadejte hodnotu do pole **Popis**.
1. Vyberte možnost v poli **Typ čárového kódu**.
    * Pokud používáte data USMF, můžete vybrat „Kód 39“.
1. V poli **ID masky** zadejte ID masky čárového kódu. Masky čárových kódů se používají k vytvoření čárových kódů a rychlé identifikaci čárových kódů, které jsou skenovány do systému pokladního místa (POS). Podrobnosti viz [Nastavení masek čárových kódů](../../../commerce/set-up-bar-code-masks.md).
1. Do pole **Velikost** zadejte číslo.
1. Zadejte číslo do pole **Maximální délka**.
1. Zvolte možnost **Uložit**.
1. Zavřete stránku.
1. Přejděte do **parametrů modulu Řízení zásob a skladu**.
1. V poli **Nastavení čárového kódu** zadejte nebo vyberte hodnotu.
    * Vyberte nastavení čárového kódu, který jste předtím vytvořili, nezapomeňte však, že formát čárového kódu musí odpovídat formátu jedinečného identifikátoru pro typ záznamu používaného v procesu. Například pro postupy výdeje by formát čárového kódu měl odpovídat formátu odkazu postupu výdeje, což je obvykle číselná řada.  
1. Zvolte možnost **Uložit**.
1. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

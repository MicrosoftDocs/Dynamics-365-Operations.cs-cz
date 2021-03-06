---
title: Údržba typů čárového kódu
description: Tento postup popisuje, jak nastavit novou definici čárového kódu, který lze použít v rámci sestavy seznamu výdejek.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 937384f14d88dafd537888d862ee1e363ea20626
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809511"
---
# <a name="maintain-barcode-types"></a>Údržba typů čárového kódu

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak nastavit novou definici čárového kódu, který lze použít v rámci sestavy seznamu výdejek. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat. Pokud používáte USMF, můžete použít ukázkové hodnoty, které jsou zobrazeny. Tyto úkoly obvykle provádějí vedoucí skladu.

1. Přejděte k čárovým kódům.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Nastavení čárového kódu.
4. Zadejte nějakou hodnotu do pole Popis.
5. Vyberte možnost v poli Typ čárového kódu.
    * Pokud používáte data USMF, můžete vybrat „Kód 39“.  
6. Do pole Velikost zadejte číslo.
7. Zadejte číslo do pole Maximální délka.
8. Klepněte na tlačítko Uložit.
9. Zavřete stránku.
10. Přejděte do parametrů modulu Řízení zásob a skladu
11. V poli Nastavení čárového kódu zadejte nebo vyberte hodnotu.
    * Vyberte nastavení čárového kódu, který jste předtím vytvořili, nezapomeňte však, že formát čárového kódu musí odpovídat formátu jedinečného identifikátoru pro typ záznamu používaného v procesu. Například pro postupy výdeje by formát čárového kódu měl odpovídat formátu odkazu postupu výdeje, což je obvykle číselná řada.  
12. Klikněte na položku Uložit.
13. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
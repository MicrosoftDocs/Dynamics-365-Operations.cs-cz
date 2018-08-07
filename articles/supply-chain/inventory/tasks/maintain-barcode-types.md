---
title: "Udržování typů čárových kódů"
description: "Tento postup popisuje, jak nastavit novou definici čárového kódu, který lze použít v rámci sestavy seznamu výdejek."
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45323206550d1b0ed66d89f4be7b995c60af63fc
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="maintain-bar-code-types"></a>Udržování typů čárových kódů

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


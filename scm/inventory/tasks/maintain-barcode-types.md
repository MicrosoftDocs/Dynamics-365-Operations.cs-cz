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
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 57ad3f2cb4f4a246af4d58001c6ef56c440b5431
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="maintain-bar-code-types"></a>Udržování typů čárových kódů

[!include[task guide banner](../../includes/task-guide-banner.md)]

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



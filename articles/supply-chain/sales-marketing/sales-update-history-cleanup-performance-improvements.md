---
title: Vylepšení výkonu čištění historie prodeje
description: Toto téma popisuje funkci vylepšení výkonu vyčištění historie prodeje a způsob, jak ji povolit.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1b2de9d6a7b1b7793b6bb753dd580d052d3c2841
ms.sourcegitcommit: 96515ddbe2f65905140b16088ba62e9b258863fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/04/2021
ms.locfileid: "7891761"
---
# <a name="saleshistorycleanupperformanceimprovements"></a>Vylepšení výkonu čištění historie prodeje

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.24 -->

Pravidelná dávková úloha **Vyčištění historie prodeje** může trvat dlouho, pokud se zřídka spouští v prostředích s velkým objemem aktualizací prodeje. V těchto situacích funkce *Vylepšení výkonu vyčištění historie prodeje* může pomoci zkrátit dobu běhu a zlepšit spolehlivost.

Tato funkce zlepšuje stávající úlohu vyčištění následujícími způsoby:

- Rozděluje vyčištění na dávky (velikost dávky můžete změnit pomocí přizpůsobení).
- Poběží maximálně 2 hodiny (dobu trvání můžete změnit pomocí přizpůsobení).
- Kde je to možné, využívá se možnosti databáze, aby se minimalizovalo omezení zamykáním a zabránilo se spojování transakčních tabulek během čištění.

Po aktivaci funkce dávková úloha **Vyčištění historie aktualizace prodeje** (**Prodej a marketing \> Pravidelné úkoly \> Čištění \> Vyčištění historie aktualizace prodeje**) poběží jako předtím, ale s lepším výkonem a maximálně 2 hodiny. To znamená, že může být nutné několikrát spustit, abyste vyčistili všechna data pro konkrétní časový rámec uchování.

## <a name="turn-on-the-saleshistorycleanupperformanceimprovements-feature"></a>Zapnutí funkce vylepšení výkonu čištění historie prodeje

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Přehled prodeje a marketingu*
- **Název funkce:** *Vylepšení výkonu čištění historie prodeje*

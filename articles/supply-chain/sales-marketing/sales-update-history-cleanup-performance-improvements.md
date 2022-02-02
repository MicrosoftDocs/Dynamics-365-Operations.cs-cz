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
ms.openlocfilehash: 3c8ad7b0bd46c49fc989be091f44630a6a3eebc1
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985904"
---
# <a name="sales-history-cleanup-performance-improvements"></a>Vylepšení výkonu čištění historie prodeje

[!include [banner](../includes/banner.md)]

Pravidelná dávková úloha **Vyčištění historie prodeje** může trvat dlouho, pokud se zřídka spouští v prostředích s velkým objemem aktualizací prodeje. V těchto situacích funkce *Vylepšení výkonu vyčištění historie prodeje* může pomoci zkrátit dobu běhu a zlepšit spolehlivost.

Tato funkce zlepšuje stávající úlohu vyčištění následujícími způsoby:

- Rozděluje vyčištění na dávky (velikost dávky můžete změnit pomocí přizpůsobení).
- Poběží maximálně 2 hodiny (dobu trvání můžete změnit pomocí přizpůsobení).
- Kde je to možné, využívá se možnosti databáze, aby se minimalizovalo omezení zamykáním a zabránilo se spojování transakčních tabulek během čištění.

Po aktivaci funkce dávková úloha **Vyčištění historie aktualizace prodeje** (**Prodej a marketing \> Pravidelné úkoly \> Čištění \> Vyčištění historie aktualizace prodeje**) poběží jako předtím, ale s lepším výkonem a maximálně 2 hodiny. To znamená, že může být nutné několikrát spustit, abyste vyčistili všechna data pro konkrétní časový rámec uchování.

## <a name="turn-on-the-sales-history-cleanup-performance-improvements-feature"></a>Zapnutí funkce vylepšení výkonu čištění historie prodeje

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Přehled prodeje a marketingu*
- **Název funkce:** *Vylepšení výkonu čištění historie prodeje*

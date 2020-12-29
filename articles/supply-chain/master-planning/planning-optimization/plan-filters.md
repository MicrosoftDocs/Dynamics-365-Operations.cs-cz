---
title: Použití filtrů v plánu
description: Toto téma vysvětluje způsob použití filtrů v plánu při použití funkce Optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9ddf9934965bd06ec805731a1cc1a667846fa180
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423783"
---
# <a name="apply-filters-to-a-plan"></a>Použití filtrů v plánu

[!include [banner](../../includes/banner.md)]

Při použití funkce Optimalizace plánování můžete aplikovat filtr na plán. **Filtr plánu** bude vždy použit při spuštění hlavního plánování. **Filtr plánu** je užitečný v případě, že chcete omezit plán na určitou skupinu položek a ujistit se, že jako součást výsledného hlavního plánování nejsou zahrnuty žádné další položky.

Pokud je použit **Filtr plánu** a v průběhu spuštění hlavního plánování je také použit filtr běhu, je do spuštění plánování zahrnut pouze průnik těchto dvou filtrů.

K **Filtru plánu** se lze dostat z **Hlavních plánů** při použití Optimalizace plánování.

## <a name="example-scenario"></a>Příklad

Je nastaven filtr plánu, který zahrnuje položky A, B a C. Běhy hlavního plánování se potom spustí pro stejný plán, ale jsou použity různé běhové filtry:

- **Běhový filtr, který zahrnuje položku D:** žádné položky nejsou plánovány, protože mezi filtrem plánu a běhovým filtrem nejsou žádné průniky.
- **Běhový filtr který zahrnuje položky A a D**: v běhu plánování je zahrnuta pouze položka A, protože položka D není součástí filtru plánu.
- **Běhový filtr který zahrnuje položku B**: v běhu plánování je zahrnuta pouze položka B a je zachován předchozí výstup plánování pro položku A.
- **Běhový filtr, který zahrnuje všechny položky (prázdný filtr):** položky a, B a C jsou zahrnuty do spuštění plánování a předchozí výstup plánování pro položky A a B bude přepsán.

> [!NOTE]
> Neměli byste nastavovat filtr plánu v plánu, který je vybrán jako **Aktuální dynamický hlavní plán** na stránce **parametry hlavního plánování**. V opačném případě bude funkce dynamického hlavního plánu omezena na filtrované položky. Jsou-li například aktualizovány požadavky netto pro položku, která není součástí filtru plánu, nebudou vygenerovány žádné výsledky.

## <a name="related-resources"></a>Související prostředky

[Přehled optimalizace plánování](planning-optimization-overview.md)

[Začínáme s optimalizací plánování](get-started.md)

[Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)

[Zobrazení historie plánu a protokolů plánování](plan-history-logs.md)

[Zrušení úlohy plánování](cancel-planning-job.md)

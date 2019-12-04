---
title: Analýza přizpůsobení pro optimalizaci plánování
description: V tomto tématu je vysvětleno, jak ověřit aktuální nastavení a data proti funkcím funkce optimalizace plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 1030/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 26b067f8526df16474c0ab52d0abf816170ff5cb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773918"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a>Analýza přizpůsobení pro optimalizaci plánování

Chcete-li zjistit, jakým způsobem jsou aktuální nastavení a data kompatibilní s funkcí Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Analýza shody optimalizace plánování** a vyberte **Spustit analýzu**. Pokud analýza nalezne nějaké nekonzistence, budou uvedeny na stejné stránce. (Provádění analýzy může trvat několik minut.)

> [!NOTE]
> Pokud jsou nalezeny nekonzistence, můžete stále používat optimalizaci plánování. Výsledky analýzy přizpůsobení zobrazují pouze místa, kde plánovací služba nerespektuje vaše aktuální nastavení. Jinými slovy, zobrazují místa, kde některé procesy mohou být ignorovány nebo nejsou podporovány.

## <a name="analysis-results-example-1"></a>Výsledky analýzy: Příklad 1

- **Funkce:** Výroba
- **Problém:** Položky s úrovní kusovníku větší než nula: 56
- **Vysvětlení:** Analýza přizpůsobení nalezla 56 položek, které mají pro výrobu nastaven kusovník. Vzhledem k tomu, že aktuální verze optimalizace plánování nepodporuje výrobu, optimalizace plánování vygeneruje plánované nákupní objednávky namísto plánovaných výrobních zakázek. Zobrazí se také upozornění, které obsahuje seznam ovlivněných položek.

### <a name="analysis-results-example-2"></a>Výsledky analýzy: Příklad 2

- **Funkce:** Akce
- **Problém:** Skupiny disponibility s povolenou kalkulací akcí: 6
- **Vysvětlení:** Analýza přizpůsobení našla šest skupin disponibility, kde je zapnut výpočet akce. Vzhledem k tomu, že aktuální verze optimalizace plánování nepodporuje akce, nebudou při hlavním plánování generovány žádné akce.

## <a name="related-resources"></a>Související prostředky

[Přehled optimalizace plánování](planning-optimization-overview.md)

[Začínáme s optimalizací plánování](get-started.md)

[Zobrazení historie plánu a protokolů plánování](plan-history-logs.md)

[Použití filtrů v plánu](plan-filters.md)

[Zrušení úlohy plánování](cancel-planning-job.md)

---
title: "Pravidla přidělení hlavní knihy"
description: "Tento článek obsahuje informace o pravidlech přidělení hlavní knihy. Popisuje různé aspekty těchto pravidel přidělení a metod přidělení, které lze pro ně použít."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 63562cde3f2813fdcfc9df7ccbfc623aa2fbe9b1
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="ledger-allocation-rules"></a>Pravidla přidělení hlavní knihy

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o pravidlech přidělení hlavní knihy. Popisuje různé aspekty těchto pravidel přidělení a metod přidělení, které lze pro ně použít.

Pravidla přidělení hlavní knihy se používají k automatickému výpočtu a generování deníků přidělení a účetních položek pro přidělování zůstatků hlavní knihy nebo pevných částek. Metody přidělení mohou být proměnné nebo pevné. Pro pravidla přidělení hlavní knihy můžete použít následující metody přidělení:

-   **Základ** – tato proměnná metody se používá, když přidělení závisí na skutečném zůstatku hlavní knihy na základě kritérií filtru. Příklad: Výdaje společnosti na reklamu lze přidělit úměrně podle prodeje jednotlivých oddělení vzhledem k celkovému prodeji oddělení.
-   **Pevné procento** a **Pevná váha** – pro tyto metody je procentuální hodnota nebo váha přidělení definována přímo pro pravidlo. Například výdaje na reklamu lze alokovat tak, aby oddělení A přijalo 70 procent výdajů na reklamu a oddělení B 30 procent.
-   **Rovnoměrně** – tato metoda distribuuje částku rovnoměrně mezi jednotlivé definované cíle. Například pokud jsou místa určení definována pro oddělení A a B, náklady na reklamu lze rozdělit tak, aby na obě oddělení A a B připadlo 50 procent výdajů na reklamu.

Je-li použita metoda přidělení Základ pro pravidlo přidělení, je nutné definovat také samostatná pravidla základu přidělení hlavní knihy. Proces "Požadavek na přidělení procesu" umožňuje uživatelům zpracovat pravidlo přidělení hlavní knihy a zobrazit náhled výsledných položek deníku přidělení před zaúčtováním nebo odstraněním vypočítaných přidělení.

## <a name="components-of-ledger-allocation-rules"></a>Součásti pravidel přidělení hlavní knihy
Každé pravidlo přidělení má čtyři komponenty: obecné údaje, zdroj, cíl a protiúčet. Další komponenta, pravidla základu přidělení hlavní knihy, jsou požadována, je-li Základ použit jako metoda přidělení. Každá komponenta poskytuje důležité informace potřebné ke zpracování přidělení.

-   **Obecné** – v této součásti uživatel určuje volby, jako například metodu přidělení, nastavení mezipodnikových pravidel a také to, zda má být pravidlo aktivní.
-   **Zdroj** – tato součást slouží uživateli k určení zdrojových dat pro přidělení. Přidělení může být založeno na zůstatcích hlavní knihy (**Zdroj dat** = **Hlavní kniha**) nebo pevných částkách (**Zdroj dat** = **Pevná hodnota**). Při nastavení možnosti **Zdroj dat** na hodnotu **Hlavní kniha** musí být definována kritéria filtru zdroje pro pravidlo přidělení hlavní knihy (například pro výdaje na reklamu).
-   **Cíl** – tato komponenta určuje způsob, jak má být výsledek výpočtu přidělení distribuován a zaúčtován. Například může existovat jeden řádek cíle pro každé oddělení.
-   **Protiúčet** – tato komponenta určuje, jak mají být hlavní účty a dimenze určeny pro položky protiúčtu, které vyrovnávají položky cíle. Namísto účtů a dimenzí založených na zdroji se obvykle používají uživatelem definované možnosti. Při nastavení možnosti **Zdroj dat** na hodnotu **Pevná hodnota** nelze použít možnost **Zdroj**.
-   **Pravidla základu přidělení hlavní knihy** – tato pravidla používají vlastní kritéria filtru zdroje k určení, které zůstatky hlavní knihy mají být použity pro přidělení (například výnosy pro jednotlivá oddělení). Každé pravidlo základu přidělení lze použít s více pravidly přidělení.






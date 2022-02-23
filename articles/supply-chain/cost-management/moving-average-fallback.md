---
title: Klouzavý průměr, posloupnost záložních nákladů
description: Toto téma obsahuje informace o posloupnosti záložních nákladů pro výpočty klouzavých průměrů v Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 541b7ecca5c1c36999f573d6d0f2dc0c9e901631
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967576"
---
# <a name="moving-average-fallback-cost-sequence"></a>Klouzavý průměr, posloupnost záložních nákladů

Jedním ze způsobů, jak lze vypočítat náklady na zásoby, je použití _klouzavého průměru_. K jednotlivým skladovým položkám lze přidružit až tři hodnoty nákladů:

- **Poslední výdej** – náklady na poslední výdej, které byly přiřazeny před tím, než se zásoby staly zápornými
- **Aktivní náklady** – nejnovější náklady, které byly aktivovány v nákladové verzi
- **Cena položky** – náklady, které jsou zadány pro uvolněný produkt

Chcete-li určit, které z těchto nákladových hodnot by se měly použít při výpočtech klouzavých průměrnů, systém použije _posloupnost záložních nákladů_ k určení pořadí priority pro hodnoty. Není-li upřednostňovaná hodnota nákladů k dispozici, systém použije další upřednostňovanou hodnotu atd.

V předchozích verzích Microsoft Dynamics 365 Supply Chain Management používal systém fixní posloupnost záložních nákladů (_Poslední výdej – aktivní náklady – cena položky_). Ve verzi 10.0.11 je toto pořadí stále výchozí řadou. Můžete však také zapnout funkci, která vám umožní vybírat ze tří posloupností záložních nákladů. Tato funkce je užitečná zejména pro organizace, které pravidelně používají záporné hodnoty zásob.

Chcete-li umožnit výběr pro posloupnost záložních nákladů, musíte vy (nebo správce) použít [Správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapnout funkci s názvem _Klouzavý průměr, posloupnost záložních nákladů_.

Chcete-li vybrat posloupnost záložních nákladů pro klouzavý průměr, postupujte podle následujících kroků.

1. Otevřete stránku **Parametry**.
2. Na kartě **Skladové účetnictví** v části **Klouzavý průměr** nastavte hodnotu pole **Posloupnost záložních nákladů** na jednu z následujících hodnot:

    - **Poslední výdej – aktivní náklady – cena položky** – toto pořadí je výchozí. Jedná se o stejnou řadu, která se použije v případě, že funkce _Klouzavý průměr, posloupnost záložních nákladů_ není zapnuta.
    - **Aktivní náklady – poslední výdej**
    - **Aktivní náklady – cena položky** – organizace mohou mít problémy s výkonem v případě, že používají obchodní procesy, v nichž sklad pravidelně vychází záporný, a zároveň je objem transakce vysoký. Toto nastavení může pomoci při zmírnění těchto potíží s výkonem.

![Parametry skladového účetnictví](media/inventory-accounting-parameters.png "Parametry skladového účetnictví")

---
title: Posloupnost záložních nákladů klouzavého průměru
description: Tento článek obsahuje informace o posloupnosti záložních nákladů pro výpočty klouzavých průměrů v Microsoft Dynamics 365 Supply Chain Management.
author: JennySong-SH
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: ad67828e2608f4754a3dffd76c64292f6a91e95f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868007"
---
# <a name="moving-average-fallback-cost-sequence"></a>Klouzavý průměr, posloupnost záložních nákladů

[!include [banner](../includes/banner.md)]

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

![Parametry skladového účetnictví.](media/inventory-accounting-parameters.png "Parametry skladového účetnictví")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
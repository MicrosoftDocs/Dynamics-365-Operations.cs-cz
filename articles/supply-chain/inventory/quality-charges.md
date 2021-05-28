---
title: Náklady kvality pro operace neshod
description: Toto téma popisuje, jak vytvořit náklady kvality, které lze použít s operacemi pro neshodu.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022293"
---
# <a name="charges-for-nonconformance-operations"></a>Náklady kvality pro operace neshod

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvořit náklady kvality, které lze použít s operacemi pro neshodu.

Na stránce **Náklady kvality** definujte typy nákladů, které můžete přidat k operacím neshod. Poplatky vám umožňují sledovat podrobnosti poplatků, které dlužíte zákazníkovi za neshodné výrobky, nebo které vám prodejce dluží za neshodné výrobky, které jste obdrželi. Můžete také použít poplatky ke sledování nákladů, které jsou požadovány pro externí dodavatele nebo služby k provedení operace.

## <a name="examples-of-quality-charges"></a>Příklady nákladů kvality

Pracujete pro výrobní společnost. Vaše společnost má smlouvy s několika dodavateli. Tyto smlouvy uvádějí standardy pro včasné odeslání, poškození a kvalitu produktu pro zboží. Podobně má několik vašich zákazníků s vaší společností dohody o vrácení, poškození a kvalitě produktu.

Struktura poplatků je definována pro každou okolnost a specifikována ve smlouvě. Můžete nakonfigurovat náklady kvality tak, aby obsahovaly různé typy poplatků, například *Poškození*, *Pozdní dodávka* a *Kvalita*. Poté, když vytvoříte neshodu, přidáte jednu nebo více operací. Pro každou operaci vyberete **Náklady** k definování podrobnosti o poplatcích.

## <a name="create-a-quality-charge"></a>Vytvoření nákladu kvality

1. Přejděte na **Řízení zásob \> Nastavení \> Správa kvality \> Náklady kvality**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Kód nákladu** - Zadejte jedinečné ID nebo název nákladu kvality.
    - **Popis** - Zadejte podrobný popis typu nákladu kvality.

1. Zavřete stránku.

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a>Přidejte do operace náklad kvality kvůli neshodě

Podrobnosti o tom, jak přidat operace k neshodě a účtovat jim náklady, viz [Operace pro neshody](quality-operations.md).

## <a name="additional-resources"></a>Další prostředky

- [Přehled správy kvality](quality-management-processes.md)
- [Povolit správu kvality a neshod](enable-quality-management.md)
- [Zaměstnanci odpovědní za schvalování neshod](quality-responsible-workers.md)
- [Karanténní zóny pro neshody](quality-quarantine-zones.md)
- [Diagnostické typy pro neshody](quality-diagnostic-types.md)
- [Kódy kvality pro náklady.](quality-charges.md)
- [Operace pro neshody](quality-operations.md)
- [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

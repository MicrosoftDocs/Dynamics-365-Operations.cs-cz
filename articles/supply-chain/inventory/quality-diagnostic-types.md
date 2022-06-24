---
title: Diagnostické typy pro neshody
description: Tento článek popisuje, jak používat a vytvářet diagnostické typy, které lze použít s neshodami.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b7a051f807c9faab3169d2672d47f663892225
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852440"
---
# <a name="diagnostic-types-for-nonconformances"></a>Diagnostické typy pro neshody

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak používat a vytvářet diagnostické typy, které lze použít s neshodami.

Pomocí stránky **Typy diagnostiky** definujte klasifikaci akcí diagnostiky. Poté, co vytvoříte opravu pro neshodu, vyberete diagnostiku. Oprava určuje, jaký typ diagnostické akce se má provést pro schválenou neshodu a kdo ji má provést. Určuje rovněž požadované datum dokončení a plánované datum dokončení.

## <a name="examples-of-diagnostic-types"></a>Příklady typů diagnostik

Pracujete pro výrobní společnost a několik položek prošlo testy kvality. Tyto položky jsou přesunuty do oblasti karantény a označeny jako nevyhovující produkty. V Microsoft Dynamics 365 Supply Chain Management se vytvoří záznam o neshodě ke sledování podrobností pomocí řešení problému.

V tomto případě dochází k problémům s kvalitou, protože ložiska ve stroji, který balí položky, se pokazily a přehřívají se. Oprava tohoto problému spočívá ve výměně dílů ve stroji.

Když konfigurujete typy diagnostiky, můžete vytvořit více záznamů, z nichž každý představuje jiný typ problému, který může stroj mít. Alternativně můžete vytvořit jeden obecný diagnostický typ, který představuje opravu stroje.

## <a name="create-a-diagnostic-type"></a>Vytvoření typu diagnostiky

1. Přejděte na **Řízení zásob \> Nastavení \> Správa kvality \> Typy diagnostiky**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Diagnostika** - Zadejte jedinečné ID nebo název pro typ diagnostiky.
    - **Popis** - Zadejte podrobný popis typu diagnostiky.

1. Zavřete stránku.

## <a name="additional-resources"></a>Další prostředky

- [Přehled správy kvality](quality-management-processes.md)
- [Povolit správu kvality a neshod](enable-quality-management.md)
- [Zaměstnanci odpovědní za schvalování neshod](quality-responsible-workers.md)
- [Karanténní zóny pro neshody](quality-quarantine-zones.md)
- [Typy problémů pro neshody](quality-problem-types.md)
- [Kódy kvality pro náklady.](quality-charges.md)
- [Operace pro neshody](quality-operations.md)
- [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

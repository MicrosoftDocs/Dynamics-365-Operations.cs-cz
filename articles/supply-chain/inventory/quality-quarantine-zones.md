---
title: Karanténní zóny pro neshody
description: Toto téma popisuje, jak vytvářet a používat karanténní zóny pro neshody.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f4b9dfc7882af4570bf1908784b8d114396402
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021797"
---
# <a name="quarantine-zones-for-nonconformances"></a>Karanténní zóny pro neshody

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvářet a používat karanténní zóny pro neshody.

K definici zón, které lze neshodám přiřadit, použijte stránku **Karanténní zóny**. Když vytvoříte neshodu, můžete nastavit pole **Karanténní zóna** a **Typ karantény** na kartě **Obecné** stránky **Neshody**. Pole **Karanténní zóna** obvykle označuje oblast nebo umístění, kde se položka nachází. Pole **Typ karantény** definuje položku buď jako *Omezené použití*, nebo *Nepoužitelné*.

Když vytisknete sestavu o neshodě nebo opravách pro neshodu, můžete zobrazit karanténní zónu, kde je položka umístěna.

Můžete také vytisknout značku neshody pro neshodu. V této sestavě se zobrazí přiřazená karanténní zóna a informace o použití, které poskytují návod, jak manipulovat s vadným materiálem. Karanténní zóny mohou odpovídat umístěním zásob nebo provozním prostředkům.

## <a name="examples-of-quarantine-zones"></a>Příklady karanténních zón

### <a name="example-1"></a>Příklad 1

Pracujete ve společnosti vyrábějící elektroniku, která vyrábí a distribuuje televizory, reproduktory a přehrávače médií. V tomto případě můžete nakonfigurovat karanténní zónu tak, aby představovala každý typ produktu.

### <a name="example-2"></a>Příklad 2

Tři přihrádky a dva stojany se používají k ukládání položek s neshodou. V tomto případě můžete nakonfigurovat pět karanténních zón, jednu pro každou přihrádku a každý stojan.

## <a name="create-a-quarantine-zone"></a>Vytvoření karanténní zóny

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Správa kvality \> Karanténní zóny**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Karanténní zóna** – zadejte jedinečné ID nebo název karanténní zóny.
    - **Popis** – zadejte podrobný popis karanténní zóny.

1. Zavřete stránku.

## <a name="additional-resources"></a>Další prostředky

- [Přehled správy kvality](quality-management-processes.md)
- [Povolit správu kvality a neshod](enable-quality-management.md)
- [Zaměstnanci odpovědní za schvalování neshod](quality-responsible-workers.md)
- [Typy problémů pro neshody](quality-quarantine-zones.md)
- [Diagnostické typy pro neshody](quality-diagnostic-types.md)
- [Kódy kvality pro náklady.](quality-charges.md)
- [Operace pro neshody](quality-operations.md)
- [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

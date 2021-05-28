---
title: Zásady snižování rabatu
description: Toto téma popisuje, jak nastavit zásady snížení. Zásady snížení řídí chování, když se na stejnou položku nebo transakci vztahuje více rabatů.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: f586e0f40b5362510333263a985eada39d3c53f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020356"
---
# <a name="rebate-reduction-principles"></a>Zásady snižování rabatu

[!include [banner](../includes/banner.md)]

Můžete seskupit nabídky správ rabatu do *zásad snížení* pro snížení dalších dodávek spojených s položkou anebo snížení výsledných hodnot výpočtů rabatů. Po nastavení zásad snížení rabatu je můžete podle potřeby volitelně přiřadit k řádkům vašich nabídek správy rabatů.

Pravidla zásad snižování rabatu se použijí pouze v případě, že se nabídky rabatů překrývají. Proto mohou garantovat více rabatů v situacích, kdy více rabatů není dlužných.

## <a name="manage-rebate-reduction-principles"></a>Správa zásad snižování rabatu

Chcete-li pracovat se zásadami snížení rabatu, přejděte na **Správa rabatů \> Nastavit \> Zásady snižování rabatu**. Poté použijte tlačítka na panelu akcí a podle potřeby přidejte a odeberte zásady snížení. Pro každou zásadu nastavte pole podle popisu v následující tabulce.

| Pole | popis |
|---|---|
| Zásady snižování rabatu | Zadejte jedinečný název pro zásady snížení rabatu. |
| popis | Zadejte popis zásady snížení rabatu. |
| Použít snížení | Zaškrtnutím tohoto políčka použijete základ snížení na rabaty, které patří k této zásadě snižování rabatu. |
| Základ snížení | Pokud jste vybrali zaškrtávací políčko **Použít snížení**, vyberte základ snížení (*Dodávka*, *Rabaty* nebo *Oboje*). Pokud vyberete *Oba* a pokud byla u předchozí nabídky zaúčtována dodávka i rabat, použije se pouze rabat. |
| Vyloučení ze snížení | Pokud je toto políčko zaškrtnuto, dodávky a rabaty, které patří k této zásadě snížení rabatu, budou z následných snížení vyloučeny. Nastavení pole **Základ snížení** se na toto nastavení nevztahuje. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>Příklady nastavení zásad snížení rabatu

V následující tabulce jsou uvedeny některé typické příklady nastavení zásad snížení rabatu. Pro každou z těchto zásad snížení rabatu popisuje hodnota pole **Popis** účel zásad snížení rabatu.

| zásady snižování rabatu | popis | Použít snížení | Základ snížení | Vyloučení ze snížení |
|---|---|---|---|---|
| Odloženo | Snížit rabat | Ano | Oboje | Žádný |
| Exclreb | Vyloučit rabat | Ano | Rabat | Ano |
| Více | Vícenásobné rabaty | Ano | Oboje | Ano |
| Není | Pouze dodávky a rabaty | Žádný | Oboje | Ano |
| Zřízení | Pouze dodávka | Ano | Zřízení | Žádný |
| Rabat | Pouze rabat | Ano | Rabat | Ano |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>Příklady výpočtů zásad snížení rabatu

Máte prodejní objednávku, která má jeden řádek prodejní objednávky. Tento řádek má hodnotu 1 000 USD. Následující nabídky se použijí pro objednávku:

- **Nabídka 1:** 10 procent na 1 000 USD
- **Nabídka 2:** 15 procent na 1 000 USD
- **Nabídka 3:** 20 procent na 1 000 USD
- **Nabídka 4:** 25 procent na 1 000 USD

Pořadí zpracování je velmi důležité. Pořadí zpracování je založena na způsobu, jakým pracujete, jak je popsáno v části [Zpracování, kontrola a zaúčtování rabatu](process-review-post.md).

Například následující tabulka shrnuje výsledek, pokud použijete pořadí *1, 2, 3, 4*, a pokud zpracováváte pouze dodávky.

| Dohoda | Popis a nastavení | Výsledek dodávky |
|---|---|---|
| 1 | <p>Klasifikace nekontroluje snížení u jiných nabídek. Kontrola se provádí u dodávek i rabatů.</p><ul><li>**Použít snížení:** *Ne*</li><li>**Základ snížení:** *Oboje*</li><li>**Vyloučení ze snížení:** *Ne*</li></ul> | 1 000 × 10% = 100 USD |
| 2 | <p>Klasifikace kontroluje snížení u jiných nabídek, ale je označena tak, že je sama ignorována. Kontrola se provádí pouze u rabatů.</p><ul><li>**Použít snížení:** *Ano*</li><li>**Základ snížení:** *Rabat*</li><li>**Vyloučení ze snížení:** *Ano*</li></ul> | 1 000 × 15% = 150 USD |
| 3 | <p>Klasifikace kontroluje snížení u jiných nabídek. Kontrola se provádí u dodávek i rabatů.</p><ul><li>**Použít snížení:** *Ano*</li><li>**Základ snížení:** *Oboje*</li><li>**Vyloučení ze snížení:** *Ne*</li></ul> | (1 000 – Nabídka 1) × 20% = 180 USD |
| 4 | <p>Klasifikace kontroluje snížení u jiných nabídek. Kontrola se provádí u dodávek i rabatů.</p><ul><li>**Použít snížení:** *Ano*</li><li>**Základ snížení:** *Oboje*</li><li>**Vyloučení ze snížení:** *Ne*</li></ul> | (1 000 – Nabídka 1 – Nabídka 3) × 25% = 180 USD |

V následující tabulce jsou uvedeny některé příklady, kdy se dodávka zpracovává v různých objednávkách a kde se proto dosahuje různých součtů. Odchylka v dodávkách závisí na pořadí, ve kterém systém zpracovává nabídky. Je důležité, abyste pochopili, jak pořadí zpracování ovlivňuje konečnou částku rabatu.

| Pořadí | Výpočet |
|---|---|
| 1<br>(1, 2, 3, 4) | <ul><li>**Nabídka 1:** 1 000 × 10% = 100 USD</li><li>**Nabídka 2:** 1 000 × 15% = 150 USD</li><li>**Nabídka 3:** (1 000 – Nabídka 1) × 20% = 180 USD</li><li>**Nabídka 4:** (1 000 USD - Nabídka 1 - Nabídka 2) × 25% = 180 USD</li><li>**Celková dodávka:** 610 USD</li></ul> |
| 2<br>(4, 3, 2, 1) | <ul><li>**Nabídka 4:** 1 000 x 25% = 250 USD</li><li>**Nabídka 3:** (1 000 – Nabídka 4) × 20% = 150 USD</li><li>**Nabídka 2:** 1 000 x 15% = 150 USD</li><li>**Nabídka 1:** 1 000 x 10% = 100 USD</li><li>**Celková dodávka:** 650 USD</li></ul> |
| 3<br>(3, 2, 1, 4) | <ul><li>**Nabídka 3:** 1 000 x 20% = 200 USD</li><li>**Nabídka 2:** 1 000 x 15% = 150 USD</li><li>**Nabídka 1:** 1 000 x 10% = 100 USD</li><li>**Nabídka 4:** (1 000 USD - Nabídka 3 - Nabídka 1) × 25% = 175 USD</li><li>**Celková dodávka:** 625 USD</li></ul> |
| 4<br>(2, 4, 1, 3) | <ul><li>**Nabídka 2:** 1 000 × 15% = 150 USD</li><li>**Nabídka 4:** 1 000 × 25% = 250 USD</li><li>**Nabídka 1:** 1 000 × 10% = 100 USD</li><li>**Nabídka 3:** (1 000 USD - Nabídka 4 - Nabídka 1) × 20% = 130 USD</li><li>**Celková dodávka:** 630 USD</li></ul> |

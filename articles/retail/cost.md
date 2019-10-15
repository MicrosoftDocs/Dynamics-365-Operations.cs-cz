---
title: Konfigurace nákladů pro distribuovanou správu objednávek
description: Toto téma popisuje konfiguraci nákladů pro funkcionalitu distribuované správy objednávek v aplikaci Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b5e3e1997f3d3b61b7b3c7486f5531e386293537
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019432"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Konfigurace nákladů pro distribuovanou správu objednávek

[!include [banner](../includes/banner.md)]

Organizace zvažují více komponent nákladů, aby určily optimální umístění, odkud se bude plnit objednávka. Některými z těchto komponent nákladů jsou náklady na přepravu, náklady na zpracování a náklady balení. Pro určení místa plnění se vypočítává kombinace těchto nákladů.

Když první iterace správy distribuovaných objednávek v aplikaci Dynamics 365 Retail optimalizovala přiřazení objednávek do míst plnění, byla tato skutečnost zohledněna pouze ve vzdálenosti. Ačkoli vzdálenost může vzájemně souviset s náklady, není totéž jako náklady. Například náklady metody doručení na druhý den stojí více, než doručení na tutéž vzdálenost do tří nebo do sedmi dnů.

Funkce konfigurace nákladů umožňuje maloobchodníkům definovat a konfigurovat další komponenty nákladů, které budou vypočítány a zohledněny při určování optimálního umístění, odkud se budou plnit řádky objednávky.

Když jsou komponenty nákladů nakonfigurovány, řešitel DOM používá k určení optimálního umístění pro plnění objednávky pouze tyto definice nákladů. Nepovažuje komponentu vzdálenosti jako náklady. Když však nejsou nakonfigurovány žádné komponenty nákladů, řešitel DOM používá komponentu vzdálenosti jako náklad pro určení optimálního umístění pro plnění objednávky.

## <a name="set-up-cost-components"></a>Nastavení komponent nákladů

V systému lze definovat dva hlavní typy komponent nákladů: **Expedice** a **Jiné**.

Oba typy komponent nákladů podporují více základů výpočtu, jak je znázorněno v následující tabulce.

<table>
<thead>
<tr>
<th>Typ komponenty nákladu</th>
<th>Základ výpočtu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Expedice</td>
<td>
<ul>
<li>Jednoduchý</li>
<li>Vrstvený</li>
</ul>
</td>
</tr>
<tr>
<td>Jiný</td>
<td>
<ul>
<li>Prodejní objednávka</li>
<li>Řádek prodeje</li>
<li>Umístění</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Typ komponenty nákladu Expedice

Tato část vysvětluje, jak nastavit každou kombinaci typu komponenty nákladu **Expedice** a základ výpočtu pro přepravní náklady. Také vysvětluje, jak jsou řešitel DOM používá každou kombinaci.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Typ komponenty nákladů = Expedice a základ výpočtu = Jednoduchý

Pokud se použije kombinace typu komponenty nákladů **Expedice** a základ výpočtu **Jednoduchý**, přepravní náklady pro režim doručení jsou založeny buď na paušálních nákladech nebo na vzdálenosti.

Pro tuto kombinaci musíte nastavit následující pole:

- **Koeficient nákladů** - Zadejte jedinečný identifikátor pro koeficient nákladů.
- **Popis** – Zadejte název a popis koeficientu nákladů.
- **Počáteční datum** a **Koncové datum** – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah. Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.
- **Aktivní** - Označuje, zda je koeficient nákladů aktivní. Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.
- **Společnost** - Určuje právnickou osobu, pro kterou je koeficient nákladů nakonfigurován. Všechny řádky kritérií výpočtu musí být pro stejnou právnickou osobu.
- **Způsoby dodání** - Určují způsoby dodání, pro které jsou nakonfigurovány náklady.
- **Typ výpočtu** – Určuje, jak mají být vypočítány náklady pro konkrétní způsob dodání. Jsou podporovány dva typy výpočtu:

    - **Pevný** – Pro způsob dodání se používá jednotný paušální náklad. Pokud vyberete tento typ výpočtu, pole **Náklady** definuje jednotný paušální náklad.
    - **Podle jednotky vzdálenosti** – Náklad pro způsob dodání se vypočítá jako hodnota nákladů specifikovaná v poli **Náklady** krát vzdálenost mezi adresou doručení a místy.

- **Náklady** – Určuje hodnotu nákladů používanou ve spojení s polem **Typ výpočtu** pro výpočet nákladů pro způsob dodání.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Typ komponenty nákladů = Expedice a základ výpočtu = Vrstvený

Pokud se použije kombinace typu komponenty nákladů **Expedice** a základ výpočtu **Vrstvený**, přepravní náklady pro režim doručení jsou založeny buď na paušálních nákladech nebo na vzdálenosti. V této kombinaci je však vzdálenost založena na vrstveném rozsahu vzdáleností.

Pro tuto kombinaci musíte nastavit následující pole:

- **Koeficient nákladů** - Zadejte jedinečný identifikátor pro koeficient nákladů.
- **Popis** – Zadejte název a popis koeficientu nákladů.
- **Výchozí náklady** – Určují náklady, které by měly být použity pro způsob dodání, pokud vzdálenost mezi adresou doručení a místem nespadá do žádné z vrstvených vzdáleností pro způsob dodání.
- **Počáteční datum** a **Koncové datum** – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah. Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.
- **Aktivní** - Označuje, zda je koeficient nákladů aktivní. Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.
- **Společnost** - Určuje právnickou osobu, pro kterou je koeficient nákladů nakonfigurován. Všechny řádky kritérií výpočtu musí být pro stejnou právnickou osobu.
- **Způsoby dodání** - Určují způsoby dodání, pro které jsou nakonfigurovány náklady.
- **Typ vzdálenosti** – Určuje, zda definice vrstvené vzdálenosti je vzdušná vzdálenost nebo vzdálenost po silnici.
- **Jednotky vzdálenosti** – Určuje jednotku, ve které se měří vrstvená vzdálenost.
- **Vzdálenost od** – Určuje počátek rozsahu pro vrstvenou vzdálenost.
- **Vzdálenost do** – Určuje konec rozsahu pro vrstvenou vzdálenost.
- **Typ výpočtu** – Určuje, jak mají být vypočítány náklady pro konkrétní způsob dodání a vrstvenou vzdálenost. Jsou podporovány dva typy výpočtu:

    - **Pevný** – Pro způsob dodání se používá jednotný paušální náklad. Pokud vyberete tento typ výpočtu, pole **Náklady** definuje jednotný paušální náklad.
    - **Podle jednotky vzdálenosti** – Náklad pro způsob dodání a vrstvenou vzdálenost se vypočítá jako hodnota nákladů specifikovaná v poli **Náklady** krát vzdálenost mezi adresou doručení a místy.

- **Náklady** – Určuje hodnotu nákladů používanou ve spojení s polem **Typ výpočtu** pro výpočet nákladů pro způsob dodání.

> [!NOTE]
> - Když definujete vrstvené vzdálenosti, systém ověří, zda se vzdálenosti nepřekrývají nebo nechybí.
> - Typ vzdálenosti používaný pro způsob dodání musí být shodný napříč všemi vrstvenými vzdálenostmi.

### <a name="other-cost-component-type"></a>Jiný typ komponenty nákladu

Tato část vysvětluje, jak nastavit každou kombinaci typu komponenty nákladu **Jiný** a jiný typ nákladů pro jiné než přepravní náklady. Také vysvětluje, jak jsou řešitel DOM používá každou kombinaci.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Typ komponenty nákladů = Jiný a jiný typ nákladů = Prodejní objednávka

Kombinace typu nákladů **Jiný** a jiného typu nákladů **Prodejní objednávka** se používá pro definování nepřepravních nákladů na úrovni prodejní objednávky.

Pro tuto kombinaci musíte nastavit následující pole:

- **Koeficient nákladů** - Zadejte jedinečný identifikátor pro koeficient nákladů.
- **Popis** – Zadejte název a popis koeficientu nákladů.
- **Počáteční datum** a **Koncové datum** – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah. Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.
- **Aktivní** - Označuje, zda je koeficient nákladů aktivní. Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.
- **Náklady** – Určuje hodnotu nákladů pro nepřepravní náklady na úrovni prodejní objednávky.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Typ komponenty nákladů = Jiný a jiný typ nákladů = Prodejní řádek

Kombinace typu nákladů **Jiný** a jiného typu nákladů **Prodejní řádek** se používá pro definování nepřepravních nákladů na úrovni řádku prodejní objednávky.

Pro tuto kombinaci musíte nastavit následující pole:

- **Koeficient nákladů** - Zadejte jedinečný identifikátor pro koeficient nákladů.
- **Popis** – Zadejte název a popis koeficientu nákladů.
- **Počáteční datum** a **Koncové datum** – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah. Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.
- **Aktivní** - Označuje, zda je koeficient nákladů aktivní. Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.
- **Náklady** – Určuje hodnotu nákladů pro nepřepravní náklady na úrovni řádku prodejní objednávky.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Typ komponenty nákladů = Jiný a jiný typ nákladů = Místo

Kombinace typu nákladů **Jiný** a jiného typu nákladů **Místo** se používá pro definování nepřepravních nákladů pro skupinu míst nebo jednotlivé místo.

Pro tuto kombinaci musíte nastavit následující pole:

- **Koeficient nákladů** - Zadejte jedinečný identifikátor pro koeficient nákladů.
- **Popis** – Zadejte název a popis koeficientu nákladů.
- **Počáteční datum** a **Koncové datum** – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah. Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.
- **Aktivní** - Označuje, zda je koeficient nákladů aktivní. Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.
- **Skupina plnění** – Určuje skupinu míst, pro která jsou definovány nepřepravní náklady.
- **Místo plnění** – Určuje místo, pro které jsou definovány nepřepravní náklady.

    > [!NOTE]
    > Pro kritéria výpočtu na základě místa nelze určit skupinu plnění a místo plnění na stejném řádku.

- **Náklady** – Určuje hodnotu nákladů pro nepřepravní náklady na úrovni skupiny plnění nebo na úrovni místa plnění.

> [!IMPORTANT]
> Aby distribuovaná správa objednávek zvažovala při svém spuštění tyto náklady, musíte přidat koeficient nákladů do příslušného profilu plnění.

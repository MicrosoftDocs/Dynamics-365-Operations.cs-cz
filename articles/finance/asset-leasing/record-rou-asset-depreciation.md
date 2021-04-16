---
title: Záznam odpisu používaného majetku (Preview)
description: Toto téma vysvětluje, jak vytvořit položku deníku pro amortizaci požadovanou pro leasingy, které jsou uznány v rozvaze organizace.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c64f19d4cf334a6cbcacaaa3753dbafe8cbf1ffe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823064"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Záznam odpisu používaného majetku (Preview)

[!include [banner](../includes/banner.md)]

U leasingů, které jsou vykázány v rozvaze organizace, se používaný majetek (ROU) odepisuje měsíčně. Toto téma vysvětluje, jak vytvořit položku deníku pro amortizaci. Amortizace zaúčtuje na vrub účtu hlavní knihy výdajů a připíše na účet akumulovaných odpisů na základě nastavení vašeho profilu účtování a typu pronájmu. Tyto položky lze vytvořit pro každý leasing nebo je lze vytvořit pro více leasingů pomocí funkce dávkového deníku.

## <a name="asset-depreciation-schedule"></a>Plánu odpisu majetku

1. Na stránce **Souhrn leasingu** vyberte leasing. Pak vyberte **Knihy \> Plán odpisu majetku** k otevření stránky **Plán odpisu majetku**.

    Položka deníku výdajů na odpisy používaného majetku je založena na částce ve sloupci **Náklady na odpisy**. Příklad pokynů pro dodržování účetních standardů získáte v části [Výpočet nákladů na amortizaci používaného majetku u finančního leasingu](#calculation-of-rou-asset-amortization-expense-for-finance-leases) dále v tomto tématu.

2. Vyberte období odpisování a poté vyberte **Vytvořit deník**. Zobrazí se zpráva s oznámením, že byl vytvořen deník, který bude použit k záznamu odpisů.
3. Vyberte **Deníky \> Deníky leasingu majetku** k otevření stránky **Deník leasingu majetku**, kde si můžete zobrazit deníkovou položku výdajů, která byla vytvořena.
4. Vyberte položku deníku a poté vyberte **Zaúčtovat** k zaznamenání položky odpisu do hlavní knihy.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>Výpočet nákladů na amortizaci používaného majetku u operativního leasingu

Odpisy operativního leasingu se počítají jako rozdíl mezi měsíčním lineárním nákladem na leasing a měsíčním úrokovým nákladem na leasingový závazek v souladu s tématem Kodifikace účetních standardů 842 (ASC 842), což je standard Obecně přijímaných účetních zásad v USA (US GAAP). Přímý náklad na leasing se počítá jako součet všech leasingových splátek dělený dobou leasingu v měsících. (Součet leasingových plateb zahrnuje veškeré zálohy, počáteční přímé náklady, náklady na demontáž a leasingové pobídky.) Následující tabulka ukazuje příklad amortizačních nákladů na operativní leasing.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>Příklad výdaje na amortizaci používaného majetku u operativního leasingu

| Pole                                          | Hodnota       |
|------------------------------------------------|-------------|
| Částka platby                                 | 1 000       |
| Četnost plateb                              | Měsíčně     |
| Doba trvání leasingu (měsíce)                            | 24          |
| Leasingové splátky celkem                           | 24,000      |
| Přírůstková výpůjční úroková sazba                     | 5 %          |
| Typ anuity                                   | Splatná anuita |
| Interval úročení                           | Měsíčně     |
| Současná hodnota budoucích minimálních leasingových splátek | 22,888.87   |

Jak bylo uvedeno dříve, přímý náklad na leasing se počítá jako součet všech leasingových splátek dělený dobou leasingu v měsících. Systém automaticky vypočítá měsíční úrokové náklady podle plánu amortizace závazků. Úrokové náklady se vypočítají pomocí metody efektivní úrokové sazby. Systém použije přímé leasingové náklady k odečtení úrokových nákladů za každý měsíc. Hodnota se používá k redukci používaného majetku.

| Měsíc | Přímé náklady na leasing | Výdaje na úroky                        | Výpočet nákladů na amortizaci používaného majetku |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24,000 ÷ 24) = 1,000.00 | (22,888.87 – 1,000) × (5% ÷ 12) = 91.20 | 1,000 – 91.20 = 908.80                        |
| 2     | (24,000 ÷ 24) = 1,000.00 | (21,980.08 – 1,000) × (5% ÷ 12) = 87.42 | 1,000 – 87.42 = 912.58                        |
| 3     | (24,000 ÷ 24) = 1,000.00 | (21,067.49 – 1,000) × (5% ÷ 12) = 83.62 | 1,000 – 83.62 = 916.39                        |

> [!NOTE]
> Podle ASC 842 je odpis používaného majetku u operativního leasingu ve výkazu zisku a ztráty klasifikován jako leasingový náklad. Pro přehlednost leasing majetku popisuje položku jako odpis používaného majetku. Debetní položka by však měla být přiřazena k účtu nákladů na operativní leasing a kreditní položka by měla být přiřazena přímo k používaného majetku pro operativní leasing. V parametrech leasingu však můžete určit, že by se měly kreditní položky provádět na akumulovaném účtu odpisů pro provozní používaný majetek.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>Výpočet nákladů na amortizaci používaného majetku u finančního leasingu

U leasingů, které mají finanční klasifikaci, systém vypočítává amortizaci používaného majetku rovnoměrně. Proto budou náklady na odpisy pro každý měsíc stejné.

V souladu s Mezinárodní normou pro finanční výkaznictví 16 (IFRS 16) a ASC 842 bude majetek odepisován buď po dobu leasingu, nebo po dobu jeho použitelnosti, podle toho, která doba je kratší. Navíc, pokud je parametr **Převod vlastnictví** zapnutý pro leasing, bude leasing automaticky odepisován po dobu životnosti majetku.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>Příklad výdaje na amortizaci používaného majetku u finančního leasingu

| Pole                                | Hodnota                                   |
|--------------------------------------|-----------------------------------------|
| Počáteční zůstatek používaného majetku | 22,889.87                               |
| Doba trvání leasingu (měsíce)                  | 24                                      |
| Očekávaná doba použitelnosti majetku (měsíce)           | 36                                      |
| Měsíc                                | Výdaje na amortizaci používaného majetku |
| 1                                    | 22,889.87 ÷ 24 = 953.74                 |
| 2                                    | 22,889.87 ÷ 24 = 953.74                 |
| 3                                    | 22,889.87 ÷ 24 = 953.74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
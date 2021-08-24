---
title: Platby DPH a pravidla zaokrouhlení
description: Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.
author: ShylaThompson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: pacheren
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1838666b57bf2ce4eb78f5d3486c03e4c2447646a121a537efd6bffa0019b96f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760679"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Platby DPH a pravidla zaokrouhlení

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.

DPH musí být vykázána a zaplacena v pravidelných intervalech finančnímu úřadu. Toto lze provést spuštěním procesu vyúčtování a následného poprodejního daňového procesu na stránce Daň z prodeje. Daň z prodeje za určité období bude vypořádána proti účtům daně z prodeje a zůstatek daně z prodeje bude účtován na účet vypořádání daně z prodeje. Zůstatek DPH, který se zaúčtuje na účet pro vyrovnání DPH, je možné zaokrouhlit podle požadavků finančního úřadu nastavením pravidla zaokrouhlování na stránce DPH. 

Rozdíl v zaokrouhlení se zaúčtuje na účet pro zaokrouhlení DPH, který je vybrán v poli Účty pro automatické transakce v hlavní knize.

Níže naleznete příklady popisující princip pravidla zaokrouhlování pro finanční úřad.

## <a name="examples"></a>Příklad

Celková částka DPH pro období se zobrazí jako kreditní zůstatek -98 765,43. Právnická osoba shromáždila vyšší částku DPH než kolik zaplatila. Proto právnická osoba dluží peníze daňovému úřadu. 

Právnická osoba chce použít metodu zaokrouhlení, která zaokrouhluje zůstatek na nejbližší násobek 1,00. Uživatel odpovědný za účtování DPH musí provést následující akce.

1. Klikne na **Daň** > **Nepřímé daně** > **DPH** > **Finanční úřady**.
2. Na pevné kartě **Obecné** vybere v poli **Způsob zaokrouhlování** možnost **Normální**.
3. V poli **Zaokrouhlení** zadejte číslo 1,00.
4. V době, kdy je nutné zaplatit DPH daňovému úřadu, přejděte na **Daň** > **Deklarace** > **DPH** > **Vyrovnat a zaúčtovat DPH**. V účtu pro vyrovnání DPH můžete vidět, že částka daňové povinnosti **98 765,43** je zaokrouhlena na zaokrouhlena na **98 765**.

Následující tabulka ukazuje, jak je zaokrouhlena částka 98 765,43 pomocí každé z metod zaokrouhlení, která je k dispozici v poli **Způsob zaokrouhlování** na stránce **Finanční úřady**.

> [!NOTE]                                                                                  
> Je-li hodnota zaokrouhlení nastavena na 0,00, pak:
>
> - Pro normální zaokrouhlování je chování zaokrouhlení stejné jako při **zaokrouhlení = 0,01**.
> - U možností **Způsob zaokrouhlování**, **dolů**, **Zaokrouhlení nahoru** a **Vlastní výhoda** je chování stejné jako při **Zaokrouhlení = 1.00**.

| Možnost zaokrouhlování                | Zaokrouhlená hodnota = 0,01 | Zaokrouhlená hodnota = 0,10 | Zaokrouhlená hodnota = 1,00 | Zaokrouhlená hodnota = 100,00 | Zaokrouhlená hodnota = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Normální                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Dolů                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Zaokrouhlení nahoru                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Vlastní výhoda pro kreditní zůstatek | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Vlastní výhoda pro debetní zůstatek  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

### <a name="normal-round-and-round-precision-is-001"></a>Normální zaokrouhlení a přesnost zaokrouhlení je 0,01

<table>
  <tr>
    <td>Zaokrouhlení
    </td>
    <td>Proces výpočtu
    </td>
  </tr>
    <tr>
    <td>round(1,015, 0,01) = 1,02
    </td>
    <td>
      <ol>
        <li>round(1,015 / 0,01, 0) = round(101,5, 0) = 102
        </li>
        <li>102 * 0,01 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1,014, 0,01) = 1,01
    </td>
    <td> <ol>
        <li>round(1,014 / 0,01, 0) = round(101,4, 0) = 101
        </li>
        <li>101 * 0,01 = 1,01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1,011, 0,02) = 1,02
    </td>
    <td> <ol>
        <li>round(1,011 / 0,02, 0) = round(50,55, 0) = 51
        </li>
        <li>51 * 0,02 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1,009, 0,02) = 1,00
    </td>
    <td> <ol>
        <li>round(1,009 / 0,02, 0) = round(50,45, 0) = 50
        </li>
        <li>50 * 0,02 = 1,00
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> Vyberete-li možnost Vlastní výhoda, zaokrouhlení je vždy ve prospěch právnické osoby. 

Další informace naleznete v následujících tématech:
- [Přehled DPH](indirect-taxes-overview.md)
- [Vytvoření platby DPH](tasks/create-sales-tax-payment.md)
- [Vytváření transakcí DPH v dokladech](tasks/create-sales-tax-transactions-documents.md)
- [Zobrazení zaúčtovaných transakcí DPH](tasks/view-posted-sales-tax-transactions.md)
- [Funkce round](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))




[!INCLUDE[footer-include](../../includes/footer-banner.md)]

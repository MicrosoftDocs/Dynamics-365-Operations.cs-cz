---
title: Platby DPH a pravidla zaokrouhlení
description: Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e66a62007025964b3d58ff0620ebecd6d9769f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771745"
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

1.  Klikněte na Daň &gt; Nepřímé daně &gt; DPH &gt; Finanční úřady
2.  Na pevné kartě Obecné vybere v poli Způsob zaokrouhlování možnost Normální.
3.  V poli Zaokrouhlení zadejte číslo 1,00.
4.  V době, kdy je nutné zaplatit DPH daňovému úřadu, otevře stránku Vyrovnat a zaúčtovat DPH. (Klikněte na Daň &gt; Přiznání &gt; DPH &gt; Vyrovnat a zaúčtovat DPH.)
5.  V účtu pro vyrovnání DPH je částka daňové povinnosti 98 765,43 zaokrouhlena na 98 765.

Následující tabulka ukazuje, jak je zaokrouhlena částka 98 765,43 pomocí každé z metod zaokrouhlení, která je k dispozici v poli Způsob zaokrouhlování na stránce Finanční úřady.

| Možnost zaokrouhlování                | Zaokrouhlená hodnota = 0,01 | Zaokrouhlená hodnota = 0,10 | Zaokrouhlená hodnota = 1,00 | Zaokrouhlená hodnota = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Normální                              | 98 765,43              | 98 765,40              | 98 765,00              | 98 800,00                |
| Dolů                            | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Zaokrouhlení nahoru                         | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |
| Vlastní výhoda pro kreditní zůstatek | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Vlastní výhoda pro debetní zůstatek  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a>Žádné zaokrouhlování, protože zaokrouhlení je 0,00

round(1,0151, 0.00) = 1,0151 round(1,0149, 0.00) = 1,0149

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
- [Funkce round](https://msdn.microsoft.com/library/aa850656.aspx)



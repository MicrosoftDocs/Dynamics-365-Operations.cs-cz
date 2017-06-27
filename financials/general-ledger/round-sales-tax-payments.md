---
title: "Platby DPH a pravidla zaokrouhlení"
description: "Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7ec117598a6a008e5b274179659b515824029874
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="sales-tax-payments-and-rounding-rules"></a>Platby DPH a pravidla zaokrouhlení

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.

DPH musí být vykázána a zaplacena v pravidelných intervalech finančnímu úřadu. Toto lze provést spuštěním procesu vyúčtování a následného poprodejního daňového procesu na stránce Daň z prodeje. Daň z prodeje za určité období bude vypořádána proti účtům daně z prodeje a zůstatek daně z prodeje bude účtován na účet vypořádání daně z prodeje. Zůstatek DPH, který se zaúčtuje na účet pro vyrovnání DPH, je možné zaokrouhlit podle požadavků finančního úřadu nastavením pravidla zaokrouhlování na stránce DPH. 

Rozdíl v zaokrouhlení se zaúčtuje na účet pro zaokrouhlení DPH, který je vybrán v poli Účty pro automatické transakce v hlavní knize.

Níže naleznete příklady popisující princip pravidla zaokrouhlování pro finanční úřad.

### <a name="example"></a>Příklad:

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

> [!NOTE]                                                                                  
> Vyberete-li možnost Vlastní výhoda, zaokrouhlení je vždy ve prospěch právnické osoby. 

Další informace naleznete v tématu [Přehled o DPH](indirect-taxes-overview.md). 





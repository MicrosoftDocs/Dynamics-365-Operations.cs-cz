---
title: Výkon výpočtu daně ovlivňuje transakce
description: Toto téma poskytuje informace o řešení potíží, které souvisejí s výkonem výpočtu daně a jeho účinkem na transakce.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947611"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Výkon výpočtu daně ovlivňuje transakce

[!include [banner](../includes/banner.md)]

Někdy je transakce ovlivněna problémy s výkonem, které má výpočet daně. Chcete-li tento problém vyřešit, postupujte podle pokynů v následujících částech.

## <a name="review-the-transaction-line-count"></a>Kontrola počtu řádků transakce

Určete, zda má transakce velký počet řádků (například více než několik set). Pokud nemá, přejděte k další části. Pokud má transakce několik stovek řádků, odložte výpočet daně. Další informace viz [Povolení výpočtu opožděné daně v denících](enable-delayed-tax-calculation.md). 

Dále můžete určit, zda je splněna některá z následujících podmínek:

- Dochází k transakcím importu z velkých souborů.
- Více relací zpracovává stejnou transakci výpočtu daně současně.
- Transakce má více řádků a zobrazení se aktualizují v reálném čase. Například pole **Vypočítaná částka prodejní daně** na stránce **Hlavní deník** se aktualizuje v reálném čase při změně polí řádku.

   [![Pole Vypočítaná částka prodejní daně na stránce dokladu deníku](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Pokud je některá z těchto podmínek splněna, odložte výpočet daně.

## <a name="review-the-call-stack"></a>Kontrola zásobníku volání

Zkontrolujte zásobník volání a určete, zda je výpočet daně volán vícekrát. Pokud není, přejděte k další části. Pokud je zásobník volání volán vícekrát, postupujte podle těchto kroků a snižte počty výpočtu daně.

1. Pokud deník zvažoval transakci, odložte výpočet daně. Další informace viz [Povolení výpočtu opožděné daně v denících](enable-delayed-tax-calculation.md).
2. Pokud je transakcí nákupní objednávka a verze aplikace je pozdější než 10.0.15, můžete odložit výpočet daně až do konečného výpočtu povolením testování pro **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.

## <a name="review-the-call-stack-timeline"></a>Kontrola časové osy zásobníku volání

Zkontrolujte časovou osu zásobníku volání a zjistěte, zda existují následující problémy. Pokud ano, povolte testování pro možnost **TaxUncommittedDoIsolateScopeFlighting**, abyste problém vyřešili.

- Transakce způsobí, že systém přestane reagovat, dokud relace neskončí. Transakce proto nemůže vypočítat výsledek daně. Následující obrázek ukazuje okno se zprávou „Relace skončila“, kterou obdržíte.

    [![Zpráva o skončení relace](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- Metody **TaxUncommitted** trvají déle než jiné metody. Například na následujícím obrázku trvá metoda **TaxUncommitted::updateTaxUncommitted()** 43 347,42 sekundy, ale jiné metody trvají 0,09 sekundy.

    [![Trvání metod](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Přizpůsobení a volání výpočtu daně

Když přizpůsobujete, nevolejte výpočet daně metodou **insert()** nebo **update()** pro každý řádek. Výpočet daně by měl být vyvolán na úrovni transakce.

## <a name="determine-whether-customization-exists"></a>Zjištění, zda existuje přizpůsobení

Pokud jste dokončili kroky v předchozích částech, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení. Pokud neexistuje žádné přizpůsobení, vytvořte požadavek na službu Microsoft pro další podporu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

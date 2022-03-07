---
title: Použití předpovědí plateb zákazníka
description: Toto téma prochází předpoklady a rozsáhlými kroky, které jsou nutné k použití zkušební verze Finančních přehledů.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: ed70e133b93c783542d4669b679fc5b6d2d20240
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968905"
---
# <a name="use-customer-payment-predictions"></a>Použití předpovědí plateb zákazníka

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak používat předpovědi plateb zákazníka. Než použijete tuto funkci, musí pro ni být dokončené kroky instalace. Další informace naleznete v tématu [Povolit předpovědi odběratelů](enable-cust-paymnt-prediction.md).

Předpovědi plateb zákazníků si můžete prohlédnout v pracovním prostoru **Správa kreditů a kolekcích zákazníků** a na dvou nových stránkách se seznamem: **Předpovědi plateb transakce** a **Předpovědi plateb zákazníka**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Správa pracovního prostoru kreditu a kolekcí zákazníka

Pracovní prostor **Správa kreditu a kolekcí zákazníka** obsahuje dvě nové dlaždice: **Předpovědi plateb transakce** a **Předpovědi plateb zákazníka**.

### <a name="transaction-payment-predictions-list-page"></a>Stránka se seznamem Předpovědi plateb transakce

Na stránce se seznamem **Předpovědi plateb transakce** můžete zobrazit pravděpodobnost platby za otevřené transakce v intervalech **Včas**, **Pozdě** a **Velmi pozdě**. Pro každou transakci v mřížce sloupec **Pravděpodobnost dodání včas** zobrazuje pravděpodobnost, že faktura bude zaplacena v den splatnosti nebo před datem splatnosti. Pokud je pravděpodobnost včasné platby menší než 50 procent, vedle procenta ve sloupci **Pravděpodobnost včastné platby** se zobrazí červený kroužek označující riziko opožděné platby.

[![Stránka se seznamem předpovědi plateb na transakci.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Podokno **Související informace** na pravé straně stránky zobrazuje další podrobnosti o předpovědích:

- U transakce, která je vybrána v mřížce, se na pevné záložce **Předpověď platby** zobrazuje podrobnosti platebních předpovědí v intervalech **Včas**, **Pozdě**, a **Velmi pozdě**. Část **Hlavní faktory** ukazuje hlavní faktory, které ovlivnily předpovědi. Nejdůležitějšími faktory jsou atributy vybrané transakce a / nebo zákazníka pro danou transakci.
- Pevná záložka **Customer Insights** zobrazuje aktuální statistiky faktur, plateb a inkas pro zákazníka pro vybranou transakci.
- Na pevné záložce **Historie zákazníků** se zobrazuje platební historii zákazníka v intervalech **Včas**, **Pozdě**, a **Velmi pozdě**.

Údaje v části **Hlavní faktory** a na pevné záložce **Customer Insights** a **Historie zákazníků** pomáhá vysvětlit platební předpovědi. Může to pomoci zvýšit vaši důvěru v účinnost předpovědí.

[![Grafické ukazatele pro předpovědi plateb v podokně Související informace.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="customer-payment-predictions-list-page"></a>Stránka se seznamem Předpovědi plateb zákazníka

Stránka se seznamem **Předpovědi plateb zákazníka** zobrazuje celkový otevřený zůstatek a částku, která má být podle očekávání vyplacena v intervalech **Včas**, **Pozdě** a **Velmi pozdě**.

[![Předpovědi platby na stránce se seznamem zákazníků.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Částka platby v každém bloku se vypočítá jako součet váženého průměru zůstatku transakce. Tato částka se počítá na základě pravděpodobnosti platby v každém segmentu.

Například zákazník má tři otevřené transakce, které mají v každém segmentu následující pravděpodobnosti platby.

| Transakce | Množství | Pravděpodobnost včasné platby | Pravděpodobnost pozdní platby | Pravděpodobnost velmi pozdní platby |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 procent                  | 50 procent               | 40 procent                    |
| T2          | 1 000  | 50 procent                  | 30 procent               | 20 procent                    |
| T3          | 10,000 | 1 procent                   | 4 procent                | 95 procent                    |

V tomto případě se platby promítají pro každý segment následujícím způsobem.

| Intervaly   | Transakce T1      | Transakce T2         | Transakce T3            | Celkem |
|-----------|---------------------|------------------------|---------------------------|-------|
| Včas   | 100 × 10 ÷ 100 = 10 | 1,000 × 50 ÷ 100 = 500 | 10,000 × 1 ÷ 100 = 100    | 610   |
| Pozdě      | 100 × 50 ÷ 100 = 50 | 1,000 × 30 ÷ 100 = 300 | 10,000 × 4 ÷ 100 = 400    | 750   |
| Velmi pozdě | 100 × 40 ÷ 100 = 40 | 1,000 × 20 ÷ 100 = 200 | 10,000 × 95 ÷ 100 = 9,500 | 9,740 |

Část **Související informace** na pravé straně stránky zobrazuje další podrobnosti o předpovědích:

- U transakce, která je vybrána v mřížce, se na pevné záložce **Předpověď platby** zobrazuje podrobnosti platebních předpovědí v intervalech **Včas**, **Pozdě**, a **Velmi pozdě**.
- Pevná záložka **Customer Insights** zobrazuje aktuální statistiky faktur, plateb a inkas pro zákazníka pro vybranou transakci.
- Na pevné záložce **Historie zákazníků** se zobrazuje platební historii zákazníka v intervalech **Včas**, **Pozdě**, a **Velmi pozdě**.

Údaje na záložkách s náhledem **Customer Insights** a **Historie zákazníků** pomáhají vysvětlit platební předpovědi. Může to pomoci zvýšit vaši důvěru v účinnost předpovědí.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Zlepšení přesnosti předpovědí platby

Přesnost předpovědí plateb můžete zobrazit na stránce **Úvěr a inkasa \> Nastavení \> Finanční přehledy \> Parametry finančního přehledu**. Na kartě **Statistiky plateb zákazníků** v části **Predikční model** je ukázána přesnost modelu předpovědi v procentech.

[![Přesnost předpovědí platby.](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Pokud nejste spokojeni s přesností, vyberte odkaz **Zlepšit přesnost modelu** pro otevření rozšíření AI Builder. V prostředí rozšíření AI Builder můžete vybrat nebo zrušit výběr polí, dokud nevyberete pole, která jsou podle vás nejdůležitější pro přesnou předpověď pravděpodobnosti platby. Po dokončení můžete snadno proškolit model předpovědi a publikovat změny. Nově trénovaný model předpovědi se automaticky spustí a vygeneruje předpovědi v Dynamics 365 Finance.

[![Prostředí rozšíření AI Builder.](./media/ai-builder.png)](./media/ai-builder.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Použití předpovědí plateb zákazníka (náhled)
description: Toto téma prochází předpoklady a rozsáhlými kroky, které jsou nutné k použití zkušební verze Finančních přehledů.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: aa4a4975fc2ccdd91d5beb32060d68f7e77dbcb7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645642"
---
# <a name="use-customer-payment-predictions-preview"></a>Použití předpovědí plateb zákazníka (náhled)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma vysvětluje, jak používat předpovědi plateb zákazníka. Než použijete tuto funkci, musí pro ni být dokončené kroky instalace. Další informace naleznete v tématu [Povolit předpovědi odběratelů](enable-cust-paymnt-prediction.md).

Předpovědi plateb zákazníků si můžete prohlédnout v pracovním prostoru **Správa kreditů a kolekcích zákazníků** a na dvou nových stránkách se seznamem, **Předpovědi plateb za transakci** a **Předpověď platby na zákazníka**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Správa pracovního prostoru kreditu a kolekcí zákazníka

Pracovní prostor **Správa kreditu a kolekcí zákazníka** obsahuje dvě nové dlaždice, **Predikce platby na transakci** a **Zákazníci s předpokládanými vysokými pozdními zůstatky**.

- Dlaždice **Predikce platby na transakci** zobrazuje počet otevřených transakcí zákazníka, u nichž je pravděpodobnost platby menší než 50 procent v intervalu **Včas**. Tuto dlaždici můžete vybrat a otevřít tak stránku se seznamem **Předpovědi plateb za transakci**.
- Dlaždice **Zákazníci s předpokládanými vysokými pozdními zůstatky** zobrazuje počet zákazníků, u nichž se předpokládá, že více než polovina (50 procent) z celkového zůstatku bude vyplacena pozdě nebo velmi pozdě. Tuto dlaždici můžete vybrat a otevřít tak stránku se seznamem **Předpovědi plateb na zákazníka**.

[![Správa pracovního prostoru kreditu a kolekcí zákazníka](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>Stránka se seznamem předpovědí plateb na transakci

Na stránce se seznamem **Předpovědi plateb za transakci** můžete zobrazit pravděpodobnost platby za otevřené transakce v intervalech **Včas**, **Pozdě** a **Velmi pozdě**. Pro každou transakci v mřížce sloupec **Pravděpodobnost dodání včas** zobrazuje pravděpodobnost, že faktura bude zaplacena v den splatnosti nebo před datem splatnosti. Pokud je pravděpodobnost včasné platby menší než 50 procent, vedle procenta ve sloupci **Pravděpodobnost včastné platby** se zobrazí červený kroužek označující riziko opožděné platby.

[![Stránka se seznamem předpovědi plateb na transakci](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Podokno **Související informace** na pravé straně stránky zobrazuje další podrobnosti o předpovědích:

- U transakce, která je vybrána v mřížce, se na pevné záložce **Předpověď platby** zobrazuje podrobnosti platebních předpovědí v intervalech **Včas**, **Pozdě**, a **Velmi pozdě**. Část **Hlavní faktory** ukazuje hlavní faktory, které ovlivnily předpovědi. Nejdůležitějšími faktory jsou atributy vybrané transakce a / nebo zákazníka pro danou transakci.
- Pevná záložka **Customer Insights** zobrazuje aktuální statistiky faktur, plateb a inkas pro zákazníka pro vybranou transakci.
- Na pevné záložce **Historie zákazníků** se zobrazuje platební historii zákazníka v intervalech **Včas**, **Pozdě**, a **Velmi pozdě**.

Údaje v části **Hlavní faktory** a na pevné záložce **Customer Insights** a **Historie zákazníků** pomáhá vysvětlit platební předpovědi. Může to pomoci zvýšit vaši důvěru v účinnost předpovědí.

[![Grafické ukazatele pro předpovědi plateb v podokně Související informace](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>Předpověď platby na stránce se seznamem zákazníků

Stránka se seznamem **předpověď platby na zákazníka** zobrazuje celkový otevřený zůstatek a částku, která má být podle očekávání vyplacena v intervalech **Včas**, **Pozdě** a **Velmi pozdě**.

[![Předpovědi platby na stránce se seznamem zákazníků](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

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

- U transakce, která je vybrána v mřížce, se na pevné záložce **Předpověď platby** zobrazuje podrobnosti platebních předpovědí v intervalech **Včas**, **Pozdě**, a **Velmi pozdě**. Část **Hlavní faktory** ukazuje hlavní faktory, které ovlivnily platby. Nejdůležitějšími faktory jsou atributy vybrané transakce a / nebo zákazníka pro danou transakci.
- Pevná záložka **Customer Insights** zobrazuje aktuální statistiky faktur, plateb a inkas pro zákazníka pro vybranou transakci.
- Na pevné záložce **Historie zákazníků** se zobrazuje platební historii zákazníka v intervalech **Včas**, **Pozdě**, a **Velmi pozdě**.

Údaje v části **Hlavní faktory** a na pevné záložce **Customer Insights** a **Historie zákazníků** pomáhá vysvětlit platební předpovědi. Může to pomoci zvýšit vaši důvěru v účinnost předpovědí.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Zlepšení přesnosti předpovědí platby

Přesnost předpovědí plateb můžete zobrazit na stránce **Úvěr a inkasa \> Nastavení \> Finanční přehledy \> Parametry finančního přehledu**. Na kartě **Statistiky plateb zákazníků** v části **Predikční model** je ukázána přesnost modelu předpovědi v procentech.

[![Přesnost předpovědí platby](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Pokud nejste spokojeni s přesností, vyberte odkaz **Zlepšit přesnost modelu** pro otevření rozšíření AI Builder. V prostředí rozšíření AI Builder můžete vybrat nebo zrušit výběr polí, dokud nevyberete pole, která jsou podle vás nejdůležitější pro přesnou předpověď pravděpodobnosti platby. Po dokončení můžete snadno proškolit model předpovědi a publikovat změny. Nově trénovaný model předpovědi se automaticky spustí a vygeneruje předpovědi v Dynamics 365 Finance.

[![Zkušenosti s rozšířením AI Builder](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>Podrobnosti uvolnění

Veřejný náhled finančních přehledů je k dispozici pro zkušební nasazení v USA, Evropě a Velké Británii. Microsoft postupně přidává podporu pro další regiony.

Funkce veřejného náhledu mohou a měly by být zapnuty pouze v prostředích sandbox vrstvy 2. Modely nastavení a AI vytvořené v prostředí sandboxu nelze migrovat do produkčního prostředí. Další informace viz [Doplňkové podmínky použití pro náhledy Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
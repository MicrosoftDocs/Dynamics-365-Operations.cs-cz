---
title: Vyhodnotit počáteční predikční model platby zákazníka (náhled)
description: Toto téma popisuje kroky, které můžete podniknout, abyste porozuměli modelu predikce plateb zákazníků a vyhodnotili jeho účinnost.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 9cbe0308902071c066d18ce71e6e33422207e8ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245585"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a>Vyhodnotit počáteční predikční model platby zákazníka (náhled)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma vysvětluje, jak vyhodnotit predikční model poté, co jste zapnuli finanční přehledy a poté vygenerovali a proškolili svůj první model. Toto téma se zabývá modely předpovídání plateb od zákazníků. Popisuje kroky, které můžete podniknout, abyste porozuměli modelu predikce plateb zákazníků a vyhodnotili jeho účinnost.

## <a name="getting-details-about-the-model"></a>Získání podrobností o modelu

Na stránce **Parametry finančních přehledů** v Microsoft Dynamics 365 Finance se objeví odkaz **Zlepšete přesnost modelu** vedle skóre přesnosti.

[![Odkaz Zlepšete přesnost modelu](./media/prediction-model.png)](./media/prediction-model.png)

Tento odkaz vás přenese do AI Builderu, kde se můžete dozvědět více o aktuálním modelu a také podniknout kroky k jeho vylepšení. Na následující ilustraci je zobrazena otevřená stránka.

[![AI Builder](./media/what-to-predict.png)](./media/what-to-predict.png)

Na otevřené stránce se zobrazí následující informace:

- V části **Výkon** poskytuje stupeň výkonu modelu pohled na kvalitu modelu. Další informace o tomto stupni viz [Predikční výkon modelu](https://docs.microsoft.com/ai-builder/prediction-performance) v dokumentaci AI Builderu.
- Čáset **Nejvlivnější data** ukazuje, jak důležité byly různé typy vstupních dat pro váš model. Tento seznam a odpovídající procenta můžete vyhodnotit, abyste zjistili, zda jsou informace v souladu s informacemi o vašem podnikání a trhu.

    [![Výkonové a nejvlivnější datové sekce pro predikční model](./media/models.png)](./media/models.png)

- V části **Výkon** vyberte **Zobrazit podrobnosti**, chcete-li se dozvědět více o stupni a dalších aspektech. Na následujícím obrázku podrobnosti ukazují, že model používá méně informací, než je doporučeno. Proto systém vygeneroval varovnou zprávu.

    [![Varování ohledně výkonu modelu](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>Podrobnější informace

Ačkoli přesnost je dobrým výchozím bodem pro hodnocení modelu a stupeň výkonu poskytuje perspektivu, AI Builder poskytuje podrobnější metriky, které můžete použít pro své vyhodnocení. Chcete-li stáhnout podrobnosti, v části **Výkon** vyberte tlačítko se třemi tečkami (**...**) vedle tlačítka **Použít model** a poté vyberte **Stáhnout podrobné metriky**.

[![Stáhnout podrobný příkaz metriky](./media/performance.png)](./media/performance.png)

Následující obrázek ukazuje formát, ve kterém si můžete data stáhnout.

[![Formát stažených dat](./media/data-format.png)](./media/data-format.png)

Pro hlubší analýzu výsledků je dobrým výchozím bodem kontrola metriky „Matice zmatků“. Například zde jsou data, která se pro tuto metriku zobrazují na předchozím obrázku.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

Tato data můžete rozšířit následujícím způsobem.

|                          | Předpovídáno včas | Předpovězeno pozdě | Předpovězeno velmi pozdě |
|--------------------------|-------------------|----------------|---------------------|
| Skutečná včasná platba   | **71**            | 0              | 21                  |
| Skutečná pozdní platba      | 5                 | **0**          | 27                  |
| Skutečná velmi pozdní platba | 2                 | 0              | **45**              |

Matice zmatků ukazuje výsledky náhodně vybrané testovací datové sady z tréninkového procesu. Protože tyto uzavřené faktury nebyly použity k trénování modelu, jsou pro model dobrým testovacím případem. Protože je znám skutečný stav faktury, lze také vidět výkon modelu.

První věc, kterou je třeba hledat, je nejběžnější skutečná hodnota. Ačkoli tato hodnota nemusí být dokonale sladěna s celkovou datovou sadou, je to přiměřená aproximace. V tomto případě se **Skutečná včasná platba** vyskytuje u 92 ze 171 celkových faktur a je nejběžnější skutečnou hodnotou. Proto je pro váš model dobrým výchozím bodem. Pokud jste jen uhodli, že všechny faktury budou včas, měli byste pravdu 92 ze 171krát (tj. 54 procent času).

Je důležité, abyste pochopili, jak vyvážená je vaše datová sada. V tomto případě bylo 92 ze 171 faktur zaplaceno včas, 32 bylo zaplaceno pozdě a 47 bylo zaplaceno velmi pozdě. Tyto hodnoty označují rozumně vyvážený datový soubor, protože v každé klasifikaci existují netriviální výsledky. Situace, kdy jeden ze států má velmi málo výsledků, může být pro model strojového učení náročná.

Přesnost modelu udává počet správných předpovědí pro testovací datovou sadu. Tyto správné předpovědi jsou hodnoty, které jsou v předchozím příkladu zobrazeny tučně. V tomto případě hodnoty produkují vypočítanou přesnost 67,8 procenta (= \[71 + 0 + 45\] ÷ 171). Tato hodnota představuje zlepšení o 14 procent oproti základnímu odhadu 54 procent a je jedním z ukazatelů kvality modelu.

Pokud se podrobněji podíváte na matici zmatků, všimnete si, že model dělá dobrou práci při předpovídání včasných a velmi pozdních plateb na faktuře. Mýlí se však u všech 32 faktur, které byly skutečně zaplaceny pozdě (ale ne příliš pozdě). Tento výsledek naznačuje, že je nutný další průzkum a vylepšení modelu.

Číslo, které představuje výkon modelu lépe než přesnost, je skóre F1 Makro. Toto skóre bere v úvahu výsledky každého stavu klasifikace (včas, pozdě a velmi pozdě). Například zde jsou data, která se pro tuto metriku "F1 Makro" zobrazují na předchozím obrázku.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

V tomto případě skóre F1 Makro přibližně 49,3 procent naznačuje, že model neposkytuje efektivní předpovědi napříč každým stavem, a to navzdory celkovému skóre přesnosti, které se zdá být přiměřeně vysoké.

## <a name="improving-the-model"></a>Vylepšení modelu

Poté, co lépe pochopíte výsledky svého prvního modelu, možná budete chtít vylepšit model přidáním nebo odebráním sloupců funkcí nebo filtrováním všech částí datové sady, které nepodporují přesné předpovědi. Zavřete AI Builder a poté použijte odkaz **Vylepšit model** v Dynamics 365 Finance pro restart procesu AI Builder. Můžete experimentovat s různými charakteristikami, aniž byste ovlivnili publikovaný model. Publikovaný model bude ovlivněn, pouze když vyberete **Publikovat**. Nezapomeňte, že pro vaši instanci je použit jeden model Dynamics 365 Finance. Před publikováním byste proto měli pečlivě zkontrolovat každý nový model.

## <a name="for-more-information"></a>Získání dalších informací

Další informace o tom, jak vyhodnotit predikční modely, naleznete ve [Výsledcích modelů strojového učení](/confusion-matrix.md)

#### <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů
Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
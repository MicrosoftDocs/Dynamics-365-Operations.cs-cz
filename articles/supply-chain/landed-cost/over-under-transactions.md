---
title: Transakce nad/pod
description: Toto téma poskytuje informace, které vám pomohou nastavit podrobnosti zásad pro transakce nadměrného nebo nedostatečného množství, takže systém může určit, jak spravovat nadměrné zpracování a nedostatečné zpracování zboží v době přijetí.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 53b1ebf27a58b1c16c6c249ca044fd746cce1436
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020904"
---
# <a name="overunder-transactions"></a>Transakce nad/pod

[!include [banner](../../includes/banner.md)]

Když jsou zpracovány objednávky na cestě, systém očekává, že množství zboží, které je přijato do konečného cílového skladu pro spotřebu, odpovídá množství uvedenému na řádcích nákupní objednávky, které jsou spojeny s cestou. Protože však přesné množství na řádcích nákupní objednávky není vždy přijato do skladu, modul **Náklady za doručení** definuje sadu pravidel, která se používají pro příjem většího a menšího množství nákladu. Tato pravidla jsou obzvláště důležitá, protože původní objednávka byla fakturována a již ji nelze upravovat. Nastavením podrobností zásad pro transakce s příjmem nadměrného nebo nedostatečného množství může systém určit, jak spravovat nadměrné zpracování a nedostatečné zpracování zboží v době přijetí. Můžete také ručně spravovat nadměrné nebo nedostatečné množství pomocí stránky **Transakce nadměrného nebo nedostatečného množství**.

## <a name="overunder-tolerances"></a>Tolerance nad/pod

Nastavíte tolerance nadměrného nebo nedostatečného množství, abyste určili nadměrné a nedostatečné množství nebo objemy, které lze zpracovat na cestě bez způsobení chyby. Pokud je potvrzení o plavbě mimo tyto tolerance, musí být upraveno a vyřešeno, než bude možné trasu plavby uzavřít pro další zpracování.

Chcete-li nakonfigurovat tolerance, přejděte na **Náklady za doručení \> Nastavení nad/pod \> Tolerance nad/pod**. Zde můžete prohlížet, upravovat přidávat a odebírat záznamy tolerance. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Kód účtu | <p>Výběrem jedné z následujících hodnot definujte rozsah dodavatelů, na které se tolerance vztahuje:</p><ul><li>**Tabulka** - Tolerance nad / pod platí pouze pro dodavatele, který je vybrán pro řádek.</li><li>**Skupina** - Tolerance nad / pod platí pro všechny dodavatele ze skupiny tolerance dodavatele, která je vybrána pro řádek.</li><li>**Všichni** – tolerance nad/pod platí pro všechny dodavatele.</li></ul> |
| Odkaz na účet | Vyberte dodavatele nebo skupinu dodavatelů, na které se vztahuje tolerance nad / pod, v závislosti na hodnotě, kterou jste vybrali v poli **Kód účtu**. |
| Kód položky | <p>Výběrem jedné z následujících hodnot definujte rozsah položek, na které se tolerance vztahuje:</p><ul><li>**Tabulka** - Tolerance nad / pod platí pouze pro položku, která je vybrána pro řádek.</li><li>**Skupina** - Tolerance nad / pod platí pro všechny položky ze skupiny tolerance položek, která je vybrána pro řádek.</li><li>**Všichni** – tolerance nad/pod platí pro všechny položky.</li></ul> |
| Vztah položky | Vyberte položku nebo skupinu položek, na které se vztahuje tolerance nad / pod, v závislosti na hodnotě, kterou jste vybrali v poli **Kód položky**. |
| Tolerance částky | Zadejte toleranci množství, která má být použita na celou nákupní objednávku. |
| Procentní tolerance | Zadejte procentuální toleranci, která má být použita na jeden řádek nákupní objednávky. |

## <a name="overunder-reasons"></a>Důvody nad/pod

Pokud je nadměrné nebo nedostatečné množství přidruženo k přijaté linii plavby, možná budete muset zjistit příčinu nadměrného nebo nedostatečného množství. V takovém případě můžete na řádku příjmu při převzetí zboží vybrat důvod nadměrného nebo nedostatečného doručení.

Chcete-li nastavit důvody nadměrné anebo nedostačující dodávky, přejděte na **Náklady za doručení \> Nastavení nad/pod \> Důvody nad/pod**. Zde můžete zobrazit, upravit, přidat a odebrat dostupné důvody pro nadměrné a nedostatečné doručení. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý důvod.

| Pole | popis |
|---|---|
| Důvod nad/pod | Zadejte jedinečný název důvodu transakce s nadměrným nebo nedostatečným příjmem. |
| popis | Zadejte popis důvodu nad/pod. |
| Přesun | Vyberte deník pohybu, který je přidružen k důvodu nad/pod. V tomto poli jsou uvedeny všechny dostupné deníky, jejichž typ *pohybu* je spojen se stránkou **Názvy deníku zásob** (**Nastavení správy zásob \> Názvy deníků \> Zásoby**). |

## <a name="item-overunder-tolerance-groups"></a>Skupina tolerance nad/pod položky

Položky, které mají podobné tolerance, lze seskupit. Tímto způsobem můžete nastavit toleranci nad/pod pro všechny položky v této skupině současně.

Chcete-li nastavit důvody nadměrné anebo nedostačující tolerance položky, přejděte na skupiny tolerance **Náklady za doručení \> Nastavení nad/pod \> Důvody nad/pod**. Zde můžete prohlížet, upravovat přidávat a odebírat záznamy skupiny nad/pod tolerancí. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Skupina tolerance nad/pod | Zadejte jednoznačný název skupiny. Vyberte název, který popisuje toleranci, například *1% Var*. |
| popis | Zadejte popis skupiny. |

## <a name="vendor-overunder-tolerance-groups"></a>Skupina tolerance nad/pod dodavatele

Můžete seskupit dodavatele, kteří pravidelně dodávají nadměrné nebo nedostatečné množství. Potom můžete nastavit toleranci nad/pod podle jednotlivých skupin.

Chcete-li nastavit důvody nadměrné anebo nedostačující tolerance dodavatele, přejděte na **Náklady za doručení \> Nastavení nad/pod \> Důvody skupin tolerance dodavatele nad/pod**. Zde můžete prohlížet, upravovat přidávat a odebírat záznamy skupiny nad/pod tolerancí. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Skupiny nad / pod | Zadejte jednoznačný název skupiny. Vyberte název, který popisuje typ dodavatelů, kteří patří do skupiny. |
| popis | Zadejte popis skupiny. |

## <a name="view-and-process-overunder-transactions"></a>Zobrazení a zpracování transakcí nad a pod

Transakce nad a pod se generují, když množství odloženého zboží neodpovídá inicializovanému množství. Množství v deníku příjezdu by mělo být aktualizováno pouze s množstvím, které je odloženo.

Při zpracování příjmu řádků plavby lze u dodavatele nastavit tolerance nad / pod. Položky pak budou zkontrolovány a ověřeny. Toleranci lze nastavit jako procento, místní částku nebo obojí.

Pokud je přijatá položka uvnitř tolerance, systém vygeneruje deník pohybu. Tento deník lze specifikovat na stránce parametrů cesty. Kromě toho bude vytvořena transakce nad / pod. Například hodnota objednávky je 100 USD, hodnota příjmu je 99 USD a tyto hodnoty splňují pravidla tolerance. V tomto případě bude vytvořen deník negativního pohybu pro nedostatečně přijaté množství.

Pokud je přijatá položka mimo toleranci, systém vygeneruje transakci nad / pod pro rozdíl v množství.

Chcete-li zobrazit a zpracovat transakce nad a pod, přejděte na **Náklady za doručení \> Dotazy \> Transakce nad / pod**. Tam bude transakce nad / pod přidružena ke všem položkám na cestě, které jsou nadměrně nebo nedostatečně přijaty. Doporučujeme použít stránku **Transakce nad / pod** k vyřešení všech transakcí nad / pod, které jsou spojeny s cestami. Také vám doporučujeme **nepoužívat** deníky pohybů nebo inventur k ručnímu vyřešení skladových transakcí s nedostatečným množstvím. Místo toho byste měli použít stránku **Transakce nad/pod** pro správu nedostatečného množství doručení do skladu.

### <a name="upper-overview-tab"></a>Karta Přehled horního limitu

Chcete-li zobrazit transakce nad a pod, vyberte kartu **Přehled** v horní části stránky **Transakce nad/pod**. V následující tabulce jsou popsána pole, která jsou k dispozici v mřížce.

| Pole | popis |
|---|---|
| Číslo transakce nad/pod | Jedinečný název záznamu transakce nad/pod, který byl automaticky vytvořen při zpracování deníku příjezdu. |
| Cesta | Cesta, ke které byl připojen řádek nákupu. |
| Přepravní kontejner | Kontejner, ke kterému byl připojen řádek nákupu. |
| Deník doručení | Deník příjezdu, ze kterého byl vygenerován řádek nad/pod. |
| Odkaz | Odkaz na nákupní objednávku nebo objednávku převodu, která je spojena s transakcí nad/pod. |
| Počet | Nákupní objednávka, na kterou se odkazuje v transakci nad/pod. |
| Účet dodavatele | Prodejce, s nímž souvisí nadměrné nebo nedostatečné množství. |
| Číslo přepravovaného zboží | Číslo přepravovaného zboží, je-li k dispozici. |
| Č. položky | Číslo položky, s nímž souvisí nadměrné nebo nedostatečné množství. |
| Původní množství | Originální množství na řádku nákupní objednávky, která je připojená k dodávce. |
| Přijaté množství | Množství, které bylo skutečně přijato. |
| Rozdíl | Rozdíl mezi očekávanou částkou deníku příjezdu a částkou, která byla zaúčtována v deníku příjezdu. Záporná hodnota označuje nadměrnou dodávku zboží. |
| Zbývající množství | Množství, které zbývá na řádku deníku příjezdu. |
| Nadměrná/nedostatečná dodávka | Hodnota, která označuje, zda přijaté množství je nadměrné nebo nedostatečné. |
| Stav | Stav transakce s nadměrným/nedostatečným množstvím. V závislosti na nastavení na stránce **[Parametry nákladů za doručení](landed-cost-parameters.md)** může nadměrné doručení automaticky vytvořit deník pohybu pro částku nadměrného doručení a zaúčtovat deník. V tomto případě bude mít transakce nad/pod stav *Dokončeno*. Je-li k přesunu zboží z mimo nedostatečný sklad nutná nějaká akce, bude mít záznam stav *Zpracovává se*. |
| Důvod nad/pod | Důvod, který je spojen s transakcí s nadměrným/nedostatečným množstvím. |
| Karta Ostatní zásoby | Podle potřeby můžete zobrazit sloupce pro další dimenze v mřížce. Mezi tyto dimenze patří číslo šarže, stav zásob a sklad. V podokně akcí výběrem příkazu **Zásoby \> Zobrazit dimenze** otevřete dialogové okno, kde můžete vybrat použité dimenze. |

### <a name="upper-general-tab"></a>Karta Horní obecné množství

Chcete-li zobrazit více informací o řádku, který je aktuálně vybrán v horní části karty **Přehled**, vyberte kartu **Obecné** v horní části stránky **Transakce nad / pod**. Informace na této kartě zahrnují hodnoty pro všechny dostupné dimenze. Tyto informace jsou získány z původní nákupní objednávky.

### <a name="lower-overview-tab"></a>Karta Přehled dolního limitu

Chcete-li zobrazit typ dokumentu pro řádek, který je aktuálně vybrán v horní části karty **Přehled**, vyberte kartu **Přehled** v dolní části stránky **Transakce nad / pod**. V následující tabulce jsou popsána pole, která jsou k dispozici.

| Pole | popis |
|---|---|
| Typ nového dokumentu | Toto pole je nastaveno buď na *Deník pohybů* nebo na *Nákupní objednávka*, v závislosti na akci, která se zobrazí na vybraném řádku transakce nad / pod. |
| Počet | Reference a odkaz na nákupní objednávku nebo objednávku deníku pohybů, která je spojena s vybraným řádkem transakce nad/pod. |
| Důvod nad/pod | Důvod, který je spojen s transakcí s vybranou transakcí nad/pod. |
| Množství | Množství, které jste vybrali pro nákupní objednávku nebo deník pohybů, které jsou spojeny s vybraným řádkem transakce nad/pod. |

### <a name="lower-general-tab"></a>Karta Dolní obecné množství

Chcete-li zobrazit číslo transakce nad / pod, ID šarže a číslo dimenze, které jsou přidruženy k vybranému řádku transakce nad / pod, vyberte kartu **Obecné** ve spodní části stránky **Transakce nad/pod**. 

### <a name="process-overunder-transactions"></a>Zpracování transakcí nad a pod

Podokno akcí na stránce **Transakce nad / pod** poskytuje následující příkazy pro zpracování transakcí, které jsou na stránce vybrány. Každý příkaz umožňuje zvolit způsob zpracování každé transakce.

- **Vytvořit \> Pohyb** - Vytvořte a zaúčtujte deník pohybu pro vybranou transakci. U transakcí s nedostatečným množstvím se automaticky vytvoří deník pohybů a zaúčtuje se pro rozdíl mezi očekávaným a skutečným přijatým množstvím. Pokud chcete, aby prodejce realizoval rozdíl v nákladech, vyberte tento příkaz pro transakce s nadměrným množstvím.
- **Vytvořit \> Nákupní objednávka** - Vytvořte nákupní objednávku pro rozdíl mezi očekávaným a skutečně přijatým množstvím vybrané transakce. Pokud chcete, aby si organizace uvědomila rozdíl v nákladech, vyberte tento příkaz pro transakce s nadměrným množstvím.
- **Vytvořit \> Přesun na místo určení** - Tento příkaz se vztahuje pouze na příkazy k převodu. Vyberte jej, pokud chcete přenést nadměrné nebo nedostatečné množství do cílového skladu.
- **Vytvořit \> Přesun k původu** - Tento příkaz se vztahuje pouze na příkazy k převodu. Vyberte jej, pokud chcete přenést nadměrné nebo nedostatečné množství do původního skladu.

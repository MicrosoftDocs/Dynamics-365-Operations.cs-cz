---
title: Seznam zásob na skladě
description: Toto téma popisuje, jak pomocí stránky Seznam na skladě zkontrolovat podrobnosti zásob na skladě. Ukazuje několik způsobů, jak různé možnosti filtrování a třídění spolupracují, a jak mohou tyto možnosti někdy při jejich kombinaci přinést neočekávané výsledky.
author: sherry-zheng
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem, InventOnHandItemListPage, WHSOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 94e54220a68889fd31ac3b269f7a7f6f8dd98c8e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005195"
---
# <a name="inventory-on-hand-list"></a>Seznam zásob na skladě

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak pomocí stránky **Seznam na skladě** zkontrolovat podrobnosti zásob na skladě. Ukazuje několik způsobů, jak různé možnosti filtrování a třídění spolupracují, a jak mohou tyto možnosti někdy při jejich kombinaci přinést neočekávané výsledky.

## <a name="query-your-on-hand-inventory"></a>Dotaz na zásoby na skladě.

Chcete-li zkontrolovat dostupnost zásob, přejděte na **Řízení zásob \> Dotazy a sestavy \> Seznam na skladě**.

Stránka **Seznam skladu** se automaticky aktualizuje při provádění transakcí se zásobami. Tyto transakce mohou být předpovídané, fyzické nebo finanční transakce.

K vyhledání sady produktů, které hledáte, použijte následující nástroje:

- Na podokně akcí vyberte [**Dimenze**](#dimensions) a otevřete dialogové okno, ve kterém můžete přidat nebo odebrat sloupce, které jsou zobrazeny v mřížce **Na skladě**.
- V [podokně **Filtry**](#filters-pane) zadejte hodnoty pro konkrétní pole, aby se zobrazovaly pouze záznamy, které odpovídají těmto hodnotám. Filtry, které zde definujete, se vztahují na zdrojové tabulky, které mohou být později agregovány podle rozměrů, které jste vybrali k zobrazení. Informace o tom, jak toto chování může ovlivnit vaše výsledky, naleznete na stránce [příklady](#examples) dále v tomto tématu.
- V podokně **Filtry** vyberte **Použít**, chcete-li vygenerovat seznam odpovídajících zásob na skladě v mřížce **Na skladě**.
- V mřížce **Na skladě** vyberte libovolný nadpis sloupce, který chcete seřadit nebo filtrovat podle hodnot v tomto sloupci. QuickFilter v horní části mřížky poskytuje další možnosti filtrování. Tyto filtry se vztahují na výsledky, nikoli na zdrojové tabulky. Informace o tom, jak toto chování může ovlivnit vaše výsledky, naleznete na stránce [příklady](#examples) dále v tomto tématu.

Pro každou odpovídající položku mřížka **Na skladě** poskytuje následující sloupce informací o zásobách.

| Sloupcový | popis |
|---|---|
| Fyzické zásoby | Fyzické množství dostupné ve skladu. |
| Fyzicky rezervováno | Celkové množství, které bylo fyzicky rezervováno. |
| Fyzicky k dispozici | Dostupné (nerezervované) množství, které je dostupné ve fyzickém inventáři.<p>**Dostupné fyzické** je vypočítané pole. Hodnota se rovná hodnotě **Fyzické zásoby** mínus hodnota **Fyzické rezervované**.</p> |
| Dostupné fyzické v dalších rozměrech | Dostupné fyzické množství pro všechny rozměry, které jsou zobrazeny v mřížce. |
| Celkem objednáno | Celkové množství, které je zahrnuto v příchozích objednávkách nebo které má kladné množství v různých denících zásob. |
| Na objednávce | Celkové množství, které je zahrnuto v odchozích objednávkách nebo které má záporné množství v různých denících zásob. |
| Rezervováno k objednání | Celkové množství, které je rezervováno na objednaných příjmech. Hodnota v tomto poli představuje celkové množství položek v odchozích transakcích, které mají stav _Objednáno rezervováno_. Položky, které jsou rezervovány jako objednané, nejsou v inventáři fyzicky dostupné. Proto je nelze přímo vyzvednout a doručit. |
| K dispozici pro rezervaci | Celkové množství zásob na skladě, které lze rezervovat.<p>**Poznámka:** Pokud je zaškrtnuto políčko **Rezervujte objednané položky** na stránce **Parametry řízení zásob a skladu**, hodnota v tomto poli zahrnuje očekávané příjmy. Pokud je zaškrtávací políčko zrušeno, hodnota nezahrnuje očekávané příjmy.</p> |
| Dostupné celkem | Celkové dostupné množství<p>**Celkové dostupné** je vypočítané pole. Hodnota se rovná hodnotě **Dostupné fyzické** plus hodnota **Celkem objednáno** mínus hodnota **Na objednávce**.</p> |

## <a name="apply-filters-to-find-the-records-that-youre-looking-for"></a><a name="filters-pane"></a>Použijte filtry k nalezení záznamů, které hledáte

Použijte podokno **Filtry**, chcete-li filtrovat seznam zásob na skladě tak, aby obsahoval pouze záznamy, kde hodnoty pole odpovídají kritériím filtrování. Chcete-li definovat filtr, postupujte takto.

1. V podokně **Filtry** vyhledejte pole, dle kterého chcete filtrovat.
2. V poli pod názvem cílového pole vyberte logický operátor (například *začíná na*, *rovná se*, nebo *větší než*).
3. Zadejte nebo vyberte hledanou hodnotu.

> [!IMPORTANT]
> Stránka **Seznam na skladě** je sestavena z podrobné tabulky zásob na skladě, která obsahuje všechny dostupné rozměry. Seznam na této stránce je však shrnutím. Proto by mohl kombinovat řádky ze zdrojové tabulky agregováním hodnot podle zobrazených rozměrů.
>
> Filtry, které definujete v podokně **Filtry** se vztahují na zdrojovou tabulku, nikoli na agregovaný seznam. Toto chování může někdy vést k neočekávaným výsledkům. Informace o tom, jak toto chování může ovlivnit vaše výsledky, naleznete na stránce [příklady](#examples) dále v tomto tématu.
> 
> Nicméně, [filtry poskytované v mřížce](#grid-filters) *platí* pro agregovaný seznam. Tyto filtry zahrnují QuickFilter v horní části mřížky a filtr pro každou hlavičku sloupce.

Můžete upravit sadu filtrů, které jsou k dispozici v podokně **Filtry** pomocí následujících kroků.

- Chcete-li odebrat filtr z podokna, vyberte jeho tlačítko **Zavřít** (**X**).
- Chcete-li přidat filtr, vyberte **Přidat** v horní části podokna **Filtry**. Dialogové okno **Přidejte pole filtru**, které se objeví, zobrazí seznam dostupných polí. Zobrazí také informace o datovém typu a tabulce pro každé pole. Použijte záhlaví sloupců k filtrování a třídění seznamu podle potřeby a poté zaškrtněte políčko u každého pole, které chcete přidat do podokna **Filtr**. Po dokončení vyberte **Vložit** pro použití změn.

## <a name="select-which-dimensions-to-show"></a><a name="dimensions"></a>Vyberte, které rozměry chcete zobrazit

Rozměry vám řeknou více o každé položce v seznamu zásob na skladě a poskytují vám více způsobů třídění a filtrování seznamu. Rozměry, které se rozhodnete zobrazit, také ovlivňují způsob agregace řádků na stránce **Seznam na skladě**. Tato agregace zase může ovlivnit, jak se řádky ze zdrojových tabulek kombinují ve výsledcích, které vidíte. Informace o tom, jak toto chování může ovlivnit vaše výsledky, naleznete na stránce [příklady](#examples) dále v tomto tématu.

Chcete-li přizpůsobit výběr zobrazených rozměrů, postupujte takto.

1. V podokně akcí zvolte **Rozměry**.

    Dialogové okno **Zobrazení rozměrů** ,které se objeví, zobrazuje každou dimenzi.

2. Zaškrtněte políčko pro každou dimenzi, kterou chcete do mřížky zahrnout.
3. Pokud chcete, aby se váš výběr použil standardně při příštím otevření stránky **Seznam na skladě**, nastavte možnost **Uložit nastavení** na **Ano**. Pokud nastavíte tuto možnost na **Ne**, bude váš výběr použit pouze během aktuální relace. Proto při příštím otevření stránky bude použit aktuální výchozí výběr.
4. Vyberte **OK**, pokud chcete změny použít a zavřít dialogové okno.

## <a name="filter-on-the-output-of-the-inventory-on-hand-list"></a><a name="grid-filters"></a>Filtrujte na výstupu seznamu zásob na skladě

Můžete vybrat jakýkoliv nadpis sloupce v mřížce **Na skladě** a seřadit nebo filtrovat podle hodnot v tomto sloupci. QuickFilter v horní části mřížky poskytuje další možnosti filtrování. Tyto filtry se vztahují na výsledky, nikoli na zdrojové tabulky. Informace o tom, jak toto chování může ovlivnit vaše výsledky, naleznete na stránce [příklady](#examples) dále v tomto tématu.

> [!NOTE]
> Nemůžete filtrovat a třídit podle všech sloupců. Většina sloupců množství neobsahuje ovládací prvky řazení a filtrování, protože se jedná o pole vypočtená. Sloupec **Na objednávce** je výjimkou.

## <a name="examples"></a><a name="examples"></a>Příklad

Váš systém obsahuje podrobnou (neagregovanou) tabulku zásob, která ukazuje následující zásoby na skladě.

| Č. položky | Lokalita | Sklad | Fyzické zásoby | Fyzicky k dispozici |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 2 | 2 | 2 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-1"></a>Scénář 1

Srtánka **Seznam na skladě** je nastavena tak, aby zobrazovala následující konečné rozměry:

- Č. položky
- Lokalita
- Sklad

V podokně **Filtry** jsou nastavena následující kritéria filtrování:

- **Číslo položky** \| **je přesně** \| _IA0001_
- **Dostupné fyzicky** \| **menší nebo rovno** \| _1_

Zde je výsledný výstup.

| Č. položky | Lokalita | Sklad | Fyzické zásoby | Fyzicky k dispozici |
|---|---|---|---|---|
| IA0001 | 1 | 1 | 1 | 1 |
| IA0001 | 1 | 3 | 1 | 1 |

### <a name="scenario-2"></a>Scénář 2

Srtánka **Seznam na skladě** je nastavena tak, aby zobrazovala následující konečné rozměry:

- Č. položky
- Lokalita

V podokně **Filtry** jsou nastavena následující kritéria filtrování:

- **Číslo položky** \| **je přesně** \| _IA0001_
- **Dostupné fyzicky** \| **menší nebo rovno** \| _1_

Zde je výsledný výstup.

| Č. položky | Lokalita | Fyzické zásoby | Fyzicky k dispozici |
|---|---|---|---|
| IA0001 | 1 | 2 | 2 |

Všimněte si, že nastavení v podokně **Filtry** se vztahuje na podrobnou (neagregovanou) tabulku zásob, která je zobrazena na začátku této sekce. Proto kritérium **Dostupné fyzicky** \| **menší nebo rovno** \| _1_ najde z této tabulky dva řádky (první a třetí řádek, z nichž každý zobrazuje hodnotu **Dostupné fyzicky** _1_). V tomto scénáři však stránka **Seznam na skladě** není nastavena pro zobrazení dimenze **Sklad**. Proto agreguje dva původní řádky do jednoho výsledného řádku, protože oba řádky mají stejné hodnoty ve všech zobrazených rozměrech. Zdá se, že tento řádek porušuje kritérium filtrování, protože hodnota **Dostupné fyzicky** je zobrazena jako _2_. Výsledek je však správný, protože nastavení v podokně **Filtry** se vztahuje na zdrojovou tabulku, nikoli na agregovanou tabulku, která je zobrazena na stránce **Seznam na skladě**.

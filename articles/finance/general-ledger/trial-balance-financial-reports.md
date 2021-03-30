---
title: Finanční sestavy předvah
description: Tento článek popisuje výchozí sestavy pro předvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám, a způsob změn sestav tak, aby odpovídaly vašim obchodním požadavkům.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d753b99b126bf8097e8270f4774db854fa2d279
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240633"
---
# <a name="trial-balance-financial-reports"></a>Finanční sestavy předvah

[!include [banner](../includes/banner.md)]

Tento článek popisuje výchozí sestavy pro předvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám, a způsob změn sestav tak, aby odpovídaly vašim obchodním požadavkům. 

<a name="default-trial-balance-reports"></a>Výchozí finanční sestavy předvah
-----------------------------

Ve finančním vykazování existují tři sestavy předvah.

| Výchozí sestava                                 | Jak funguje                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Podrobná předvaha – výchozí               | Obsahuje informace o zůstatku na všech účtech, včetně zůstatků má dáti a dal a jejich čisté hodnoty, spolu s datem transakce, dokladu a popisem deníku.                  |
| Souhrnná předvaha – výchozí                | Obsahuje informace o zůstatku pro všechny účty a zahrnuje počáteční a závěrkové zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem.                                        |
| Souhrnná roční předvaha – výchozí | Obsahuje informace o zůstatku pro všechny účty a zahrnuje počáteční a závěrkové zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem pro aktuální a minulý rok. |

## <a name="building-blocks"></a>Stavební bloky
Finanční sestavy předvahy používají následující stavební bloky.

| Výchozí sestava                                 | Definice řádku          | Definice sloupce                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Podrobná předvaha – výchozí               | Předvaha – výchozí | Podrobná předvaha – výchozí               |
| Souhrnná předvaha – výchozí                | Předvaha – výchozí | Souhrnná předvaha – výchozí                |
| Souhrnná roční předvaha – výchozí | Předvaha – výchozí | Souhrnná roční předvaha – výchozí |

### <a name="row-definition"></a>Definice řádku

Definice řádku, předvaha – výchozí nastavení, obsahuje jediný řádek, který se shromažďuje ve všech hlavních účtech. Z toho vyplývá, že každý může generovat sestavu bez nutnosti provádět změny. Při zobrazení sestavy přejděte do jednoho řádku a podívejte se na podrobnosti o jednotlivých účtech. Definici řádku můžete upravit tak, aby obsahovala více podrobností. Chcete-li změnit řádek definice Předvaha – výchozí, aby obsahoval řádky všech účtů, postupujte takto.

1.  Klikněte na tlačítko **Upravit** a poté klikněte na tlačítko **Vložit řádky z dimenzí**. Příkaz **Vložit řádky z dimenzí** umožňuje vybrat dimenze, které mají být v definici řádku. Pro tuto definici řádku použijete **hlavní účet**.
2.  Ujistěte se, že **hlavní účet** obsahuje všechny ampersandy (&), a klikněte na tlačítko **OK**.

Definice řádku nyní obsahuje všechny hlavní účty pro výchozí právnickou osobu.

### <a name="column-definition"></a>Definice sloupce

Každá sestavu předvahy používá jinou definici sloupců. Tyto definice sloupců obsahují různé typy sloupců, které poskytují různé úrovně podrobností a finanční údaje.

-   **Podrobná předvaha – výchozí typy sloupce:**
    -   **DESC** – popis z definice řádku
    -   **ACCT** – kódy účtů
    -   **ATTR (3)** – atributy:
        -   Datum transakce
        -   Doklad
        -   Popis deníku
    -   **FD** – finanční data, která obsahují pouze položky má dáti
    -   **FD** – finanční data, která obsahují pouze položky dal
    -   **CALC** – čistý rozdíl
-   **Podrobná předvaha – výchozí typy sloupců:**
    -   **ACCT** – kódy účtů
    -   **DESC** – popis z definice řádku
    -   **ATTR** – atribut:
        -   Doklad
    -   **FD** – počáteční zůstatek finančních dat
    -   **FD** – finanční data, která obsahují pouze položky má dáti
    -   **FD** – finanční data, která obsahují pouze položky dal
    -   **CALC** – čistý rozdíl
    -   **CALC** – konečný zůstatek
-   **Souhrnná roční předvaha – výchozí**
    -   **ACCT** – kódy účtů
    -   **DESC** – popis z definice řádku
    -   **ATTR** – atribut
        -   Doklad
    -   **FD** – Finanční zůstatek od začátku roku pro aktuální rok
    -   **FD** – finanční data, která obsahují pouze položky má dáti pro aktuální rok
    -   **FD** – finanční data, která obsahují pouze položky dal pro aktuální rok
    -   **CALC** – čistý rozdíl
    -   **CALC** – konečný zůstatek
    -   **FD** – finanční data, která obsahují pouze položky má dáti pro předchozí rok
    -   **FD** – finanční data, která obsahují pouze položky dal pro předchozí rok



<a name="additional-resources"></a>Další zdroje
--------

[Přehled finančního výkaznictví](financial-reporting-getting-started.md)

[Zobrazení finančních sestav](view-financial-reports.md)

[Blog o finančním výkaznictví v Dynamics](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
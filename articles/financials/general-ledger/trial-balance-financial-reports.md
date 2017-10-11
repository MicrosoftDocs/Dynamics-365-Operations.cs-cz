---
title: "Finanční sestavy předvah"
description: "Tento článek popisuje výchozí sestavy pro předvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám, a způsob změn sestav tak, aby odpovídaly vašim obchodním požadavkům."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 86e8e91f2af474999d89bb63ac9e2afad7843c8a
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="trial-balance-financial-reports"></a>Finanční sestavy předvah

[!include[banner](../includes/banner.md)]


Tento článek popisuje výchozí sestavy pro předvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám, a způsob změn sestav tak, aby odpovídaly vašim obchodním požadavkům. 

<a name="default-trial-balance-reports"></a>Výchozí finanční sestavy předvah
-----------------------------

Pro finanční výkaznictví v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition jsou k dispozici tři předvahy.

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

 

<a name="see-also"></a>Viz také
--------

[Finanční výkaznictví](financial-reporting-getting-started.md)

[Zobrazení finančních sestav](view-financial-reports.md)

[Blog o finančním výkaznictví v Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)




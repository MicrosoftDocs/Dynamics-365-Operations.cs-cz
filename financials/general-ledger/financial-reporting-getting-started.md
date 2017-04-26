---
title: "Finanční výkaznictví"
description: "Toto téma popisuje přístupu účetního výkaznictví v 365 Microsoft Dynamics pro operace a použití finanční možnosti vytváření sestav. Obsahuje popis výchozí finanční sestavy, které jsou k dispozici."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d13747f17b5f382b3a530b1f166681eeec0b9d73
ms.lasthandoff: 03/31/2017


---

# <a name="financial-reporting"></a>Finanční výkaznictví

[!include[banner](../includes/banner.md)]


Toto téma popisuje přístupu účetního výkaznictví v 365 Microsoft Dynamics pro operace a použití finanční možnosti vytváření sestav. Obsahuje popis výchozí finanční sestavy, které jsou k dispozici.

<a name="accessing-financial-reporting"></a>Přístup k finančnímu výkaznictví
-----------------------------

Můžete najít **účetního výkaznictví** umístí 365 Dynamics pro operace v následující nabídce:

-   **Finance**&gt;**dotazy a sestavy**
-   **Rozpočet**&gt;**Inquires a zprávy o**&gt;**základní rozpočtování**
-   **Rozpočet**&gt;**dotazy a sestavy**&gt;**plánování rozpočtu**
-   **Rozpočet**&gt;**dotazy a sestavy**&gt;**kontrolu rozpočtu.**
-   Konsolidace

Chcete-li vytvořit a generovat finanční sestavy pro právnickou osobu, nastavte následující informace pro tuto právnickou osobu:

-   Fiskální kalendář
-   Hlavní kniha
-   Účtová osnova
-   Měna

Funkce finančního vykazování jsou k dispozici pro uživatele, kteří mají odpovídající oprávnění a funkční oprávnění přiřazené prostřednictvím jejich rolí zabezpečení. Následujících oddíly uvádí tato oprávnění a funkční oprávnění, jakož i související role.

### <a name="duties"></a>Funkční oprávnění

| Popisek pro funkční oprávnění                            | Popis                                                             | Název AOT                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Udržovat zabezpečení finančního výkaznictví | Udržujte zabezpečení finančního výkaznictví a provádějte úkoly správy. | FinancialReportsSecurityMaintain |
| Udržovat finanční sestavy            | Navrhujte a udržujte finanční sestavy.                                  | FinancialReportsMaintain         |
| Generovat finanční sestavy            | Generujte a aktualizujte finanční sestavy.                                 | FinancialReportsGenerate         |
| Posoudit finanční výkonnost          | Posuzujte a analyzujte finanční výkonnost.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Oprávnění

| Popisek pro oprávnění                       | Popis                                                             | Název AOT                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Udržovat zabezpečení finančního výkaznictví | Udržujte zabezpečení finančního výkaznictví a provádějte úkoly správy. | FinancialReportsSecurityMaintain |
| Udržovat finanční sestavy            | Navrhujte a udržujte finanční sestavy.                                  | FinancialReportsMaintainReports  |
| Generovat finanční sestavy            | Generujte a aktualizujte finanční sestavy.                                 | FinancialReportsGenerateReports  |
| Zobrazit finanční sestavy                | Zobrazujte finanční sestavy.                                                 | FinancialReportsView             |

### <a name="roles"></a>Role

| Popisek pro oprávnění                       | Clo                                  | Role                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Udržovat zabezpečení finančního výkaznictví | Udržovat zabezpečení finančního výkaznictví | Manažer zabezpečení                                                          |
| Udržovat finanční sestavy            | Udržovat finanční sestavy            | Hlavní účetní, Účetní supervizor finančnímu kontrolorovi, správce rozpočtu |
| Generovat finanční sestavy            | Generovat finanční sestavy            | CEO, CFO, účetní                                                            |
| Zobrazit finanční sestavy                | Posoudit finanční výkonnost          | Nepřiřazeno                                                                   |

Jakmile je uživatel přidán nebo se změní role, měl by mít uživatel během několika minut možnost přístupu k finančnímu výkaznictví. **Poznámka:** členem role je přidán do všech rolí ve finančních výkazech.

## <a name="default-reports"></a>Výchozí sestavy
Finanční vykazování poskytuje 22 výchozích finančních výkazů. Každá sestava používá výchozí kategorie hlavního účtu v Dynamics 365 pro operace. Tyto sestavy lze použít tak, jak jsou, nebo slouží jako výchozí bod vaše potřeby finančního vykazování. Kromě tradiční finančních výkazů, například výkaz zisků a ztrát nebo rozvaha, tyto výchozí sestavy zahrnují sestavy, které zobrazují různé typy finančních výkazů, které je možné vytvořit. Každá zpráva následující tabulky odkazy na prezentaci aplikace Office Mix o sestavě.

| Výchozí sestava                                                                                         | popis                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 Month Rolling Single Column Income Statement – Default](https://mix.office.com/watch/76kc7bm3wnt1) | Zobrazte ziskovost organizace za posledních 12 měsíců v jednom sloupci.                                                                                                                                                                                                                                      |
| [12 Month Trend Income Statement – Default](https://mix.office.com/watch/12brmfge5p8r)                 | Zobrazte ziskovost organizace za každý ze 12 posledních měsíců. Těchto 12 měsíců může zahrnovat více než jeden fiskální rok.                                                                                                                                                                                             |
| [Actual vs Budget – Default](https://mix.office.com/watch/fi439lkwr0no)                                | Zobrazte podrobné informace o zůstatku pro všechny účty původního rozpočtu a porovnejte revidovaný rozpočet se skutečnými hodnotami, které vykazují odchylku.                                                                                                                                                                          |
| [Audit Details – Default](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Zobrazte podrobné informace o zůstatku pro všechny účty. Tato sestava zobrazuje debetní a kreditní zůstatky v měně vykazování a místní měně, společně s dalšími informacemi o transakci, jako je například ID uživatele, uživatel, který naposledy upravil data, datum poslední změny a kód ID deníku. |
| [Balance List – Default](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Zobrazte podrobné informace o zůstatku pro všechny účty. Tato sestava zobrazuje počáteční a konečné zůstatky a debetní a kreditní zůstatky pro aktuální období a rok k datu, společně s dalšími informacemi o transakci, jako je například doklad.                                                                    |
| [Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                                   | Zobrazte přehled finanční pozice organizace pro rok.                                                                                                                                                                                                                                                             |
| [Balance Sheet and Income Statement Side by Side - Default](https://mix.office.com/watch/zkgq0u7visw9) | Zobrazte finanční pozici a ziskovost organizace za rok vedle sebe.                                                                                                                                                                                                                              |
| [Cash Flow – Default](https://mix.office.com/watch/jd3go9pz6390)                                       | Získejte přehled o hotovosti, která přichází do organizace a odchází z ní.                                                                                                                                                                                                                                   |
| [Detailed JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Zobrazte počáteční zůstatek a informace o aktivitě pro všechny účty.                                                                                                                                                                                                                                                      |
| [Detailed Trial Balance - Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Zobrazte informace o zůstatku na všech účtech, které mají zůstatky má dáti a dal, a jejich čisté hodnoty, spolu s datem transakce, dokladem a popisem deníku.                                                                                                                                  |
| [Expenses Three Year Quarterly Trend – Default](https://mix.office.com/watch/gwm4zu7tmtj8)             | Získejte přehled o výdajích za posledních 12 čtvrtletí v předchozích třech letech.                                                                                                                                                                                                                                   |
| [Financial Captions JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Zobrazte přehled zůstatků a aktivity pro finanční popisky aktiv, pasiv, jmění vlastníka, výnosů, výdajů, zisků nebo ztrát.                                                                                                                                                                           |
| [Income Statement – Default](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Umožňuje zobrazit ziskovost organizace za aktuální období a také od začátku roku.                                                                                                                                                                                                                                   |
| [Ledger Transaction List – Default](https://mix.office.com/watch/19h9v2rmh48vy)                        | Zobrazte podrobné informace o zůstatku pro všechny účty. Tato sestava zobrazuje zůstatky má dáti a dal a další informace o transakci, jako je například datum transakce, číslo deníku, doklad, typ zaúčtování a sledovací číslo.                                                                            |
| [Ratios – Default](https://mix.office.com/watch/b08hfc5h92me)                                          | Umožňuje zobrazit poměry solventnosti, ziskovosti a efektivnosti vaší organizace za rok.                                                                                                                                                                                                                           |
| [Rolling 12 Month Expenses – Default](https://mix.office.com/watch/iywod5qmqhz7)                       | Získejte přehled o výdajích pro každý z posledních 12 měsíců. Těchto 12 měsíců může zahrnovat více než jeden fiskální rok.                                                                                                                                                                                                       |
| [Rolling Quarter Income Statement – Default](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Zobrazte ziskovost organizace čtvrtletně minulý rok a od začátku roku.                                                                                                                                                                                                                   |
| [Side by Side Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                      | Zobrazte přehled finanční pozice organizace pro rok. Tato sestava uvádí aktiva a pasiva a jmění akcionářů vedle sebe.                                                                                                                                                                                |
| [Summary Trial Balance – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Obsahuje informace o zůstatku pro všechny účty s počátečními a závěrkovými zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem.                                                                                                                                                                  |
| [Summary Trial Balance Year Over Year – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Zobrazit informace o zůstatku pro všechny účty, které mají otevírací a uzavírací zůstatky a MD a Dal sald a jejich Čistý rozdíl pro aktuální rok a minulý rok.                                                                                                                           |
| [Weekly Sales and Discounts - Default](https://mix.office.com/watch/112ng0hy5de0j)                     | Získejte přehled o prodeji a slevách pro každý týden v měsíci. Tato sestava zahrnuje součet za čtyři týdny.                                                                                                                                                                                                              |
| [Dostupné finanční prostředky rozpočtu - výchozí](https://mix.office.com/watch/15hcpezcbx7tv)                         | Zobrazit podrobné porovnání revidovaného rozpočtu, skutečné výdaje, rezervace rozpočtu a rozpočtových prostředků, které jsou k dispozici pro všechny účty                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Otevření finančních výkazů
Po kliknutí na nabídku **Finanční vykazování** se zobrazí seznam výchozí finančních výkazů pro danou společnost. Poté můžete otevřít nebo upravit sestavu. Chcete-li otevřít jednu z výchozích sestav, vyberte název sestavy. Při prvním otevření se sestava automaticky generuje pro předchozí měsíc. Například pokud otevřete sestavu v srpnu 2016 poprvé, je sestava generována pro 31. července 2016. Po otevření sestavy můžete začít s prohlížením rozbalením specifických částí dat a změnou možností sestavy.

## <a name="creating-and-modifying-financial-reports"></a>Vytváření a úpravy finančních výkazů
Ze seznamu finančních výkazů lze vytvořit novou sestavu nebo upravit existující sestavu. Pokud máte příslušná oprávnění, můžete vytvořit nové finanční sestavy klepnutím na **nové** v podokně akcí. Sestavy návrháře aplikace se stahují do zařízení. Po spuštění Návrhář sestavy pak můžete vytvořit novou sestavu. Po uložení nové sestavy se zobrazí v seznamu finančních výkazů. V seznamu jsou uvedeny pouze sestavy, které byly vytvořeny pro společnosti, které používáte v Dynamics 365 pro operace. Další informace o procesu vytváření a úpravy finančních sestav v 365 Dynamics pro operace odkazovat na tyto [příspěvky blogu](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) z Dynamics finanční vykazování blogu. **Poznámka:** počítače, který stahujete sestavy návrháře klienta musí mít verzi rozhraní.NET Framework Microsoft nainstalovanými 4.6.2. Tuto verzi rozhraní.NET Framework společnosti Microsoft mohou být staženy a nainstalovány z [zde](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Pokud používáte Chrome, je nutné nainstalovat rozšíření ClickOnce Chcete-li stáhnout klienta návrháře sestav. Pokud používáte v režimu incognito, zkontrolujte, zda že je povoleno rozšíření ClickOnce pro incognito režim. Také lze upravit sestavu, která se zobrazí v seznamu finančních výkazů. Jakmile se vybere oblast kolem názvu sestavy, klikněte na tlačítko **Upravit** v podokně akcí. Spustí se program Návrhář sestav.

<a name="see-also"></a>Viz také
--------

[View financial reports](view-financial-reports.md)

[Blog o finančním výkaznictví v Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)





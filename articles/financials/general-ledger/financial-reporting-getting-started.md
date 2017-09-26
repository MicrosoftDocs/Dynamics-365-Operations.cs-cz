---
title: "Finanční výkaznictví"
description: "Toto téma popisuje, kde získat přístup k finančnímu výkaznictví v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition a jak používat příslušné funkce. Obsahuje popis výchozích finančních sestav, které jsou k dispozici."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fedde78a563939fd7080e748c412c89c71586823
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="financial-reporting"></a>Finanční výkaznictví

[!include[banner](../includes/banner.md)]


Toto téma popisuje, kde získat přístup k finančnímu výkaznictví v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition a jak používat příslušné funkce. Obsahuje popis výchozích finančních sestav, které jsou k dispozici.

<a name="accessing-financial-reporting"></a>Přístup k finančnímu výkaznictví
-----------------------------

Nabídku **Finanční výkaznictví** najdete v aplikaci Finance and Operations na těchto místech:

-   **Hlavní kniha** &gt; **Dotazy a sestavy**
-   **Rozpočet** &gt; **Dotazy a sestavy** &gt; **Základní rozpočtování**
-   **Rozpočet** &gt; **Dotazy a sestavy** &gt; **Plánování rozpočtu**
-   **Rozpočtování** &gt; **Dotazy a sestavy** &gt; **Kontrola rozpočtu**
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
| Udržovat finanční sestavy            | Udržovat finanční sestavy            | Hlavní účetní, Účetní supervizor, Finančním kontrolor, Správce rozpočtu |
| Generovat finanční sestavy            | Generovat finanční sestavy            | CEO, CFO, Účetní                                                            |
| Zobrazit finanční sestavy                | Posoudit finanční výkonnost          | Nepřiřazeno                                                                   |

Jakmile je uživatel přidán nebo se změní role, měl by mít uživatel během několika minut možnost přístupu k finančnímu výkaznictví. **Poznámka:** Role sysadmin je přidána do všech rolí ve finančních výkazech.

## <a name="default-reports"></a>Výchozí sestavy
Finanční vykazování poskytuje 22 výchozích finančních výkazů. Každý výkaz používá výchozí kategorie hlavního účtu v aplikaci Finance and Operations. Tyto sestavy lze použít tak, jak jsou, nebo slouží jako výchozí bod vaše potřeby finančního vykazování. Kromě tradiční finančních výkazů, například výkaz zisků a ztrát nebo rozvaha, tyto výchozí sestavy zahrnují sestavy, které zobrazují různé typy finančních výkazů, které je možné vytvořit. Každá sestava v následující tabulce odkazuje na prezentaci aplikace Office Mix o sestavě.

| Výchozí sestava                                                                                         | popis                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12měsíční kumulativní výkaz příjmu s jedním sloupcem – výchozí](https://mix.office.com/watch/76kc7bm3wnt1) | Zobrazte ziskovost organizace za posledních 12 měsíců v jednom sloupci.                                                                                                                                                                                                                                      |
| [12měsíční výkaz příjmu trendů – výchozí](https://mix.office.com/watch/12brmfge5p8r)                 | Zobrazte ziskovost organizace za každý ze 12 posledních měsíců. Těchto 12 měsíců může zahrnovat více než jeden fiskální rok.                                                                                                                                                                                             |
| [Skutečnost vs rozpočet – výchozí](https://mix.office.com/watch/fi439lkwr0no)                                | Zobrazte podrobné informace o zůstatku pro všechny účty původního rozpočtu a porovnejte revidovaný rozpočet se skutečnými hodnotami, které vykazují odchylku.                                                                                                                                                                          |
| [Podrobnosti auditu – výchozí](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Zobrazte podrobné informace o zůstatku pro všechny účty. Tato sestava zobrazuje debetní a kreditní zůstatky v měně vykazování a místní měně, společně s dalšími informacemi o transakci, jako je například ID uživatele, uživatel, který naposledy upravil data, datum poslední změny a kód ID deníku. |
| [Výpis zůstatků – výchozí](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Zobrazte podrobné informace o zůstatku pro všechny účty. Tato sestava zobrazuje počáteční a konečné zůstatky a debetní a kreditní zůstatky pro aktuální období a rok k datu, společně s dalšími informacemi o transakci, jako je například doklad.                                                                    |
| [Rozvaha – výchozí](https://mix.office.com/watch/zkgq0u7visw9)                                   | Zobrazte přehled finanční pozice organizace pro rok.                                                                                                                                                                                                                                                             |
| [Rozvaha a výpis příjmu vedle sebe – výchozí](https://mix.office.com/watch/zkgq0u7visw9) | Zobrazte finanční pozici a ziskovost organizace za rok vedle sebe.                                                                                                                                                                                                                              |
| [Cashflow – výchozí](https://mix.office.com/watch/jd3go9pz6390)                                       | Získejte přehled o hotovosti, která přichází do organizace a odchází z ní.                                                                                                                                                                                                                                   |
| [Podrobná revize JE a TB – výchozí](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Zobrazte počáteční zůstatek a informace o aktivitě pro všechny účty.                                                                                                                                                                                                                                                      |
| [Podrobná předvaha – výchozí](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Zobrazte informace o zůstatku na všech účtech, které mají zůstatky má dáti a dal, a jejich čisté hodnoty, spolu s datem transakce, dokladem a popisem deníku.                                                                                                                                  |
| [Čtvrtletní trend výdajů za tři roky – výchozí](https://mix.office.com/watch/gwm4zu7tmtj8)             | Získejte přehled o výdajích za posledních 12 čtvrtletí v předchozích třech letech.                                                                                                                                                                                                                                   |
| [Podrobná revize finančních popisků JE a TB – výchozí](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Zobrazte přehled zůstatků a aktivity pro finanční popisky aktiv, pasiv, jmění vlastníka, výnosů, výdajů, zisků nebo ztrát.                                                                                                                                                                           |
| [Výkaz příjmu – výchozí](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Umožňuje zobrazit ziskovost organizace za aktuální období a také od začátku roku.                                                                                                                                                                                                                                   |
| [Seznam účetních transakcí – výchozí](https://mix.office.com/watch/19h9v2rmh48vy)                        | Zobrazte podrobné informace o zůstatku pro všechny účty. Tato sestava zobrazuje zůstatky má dáti a dal a další informace o transakci, jako je například datum transakce, číslo deníku, doklad, typ zaúčtování a sledovací číslo.                                                                            |
| [Poměry – výchozí](https://mix.office.com/watch/b08hfc5h92me)                                          | Umožňuje zobrazit poměry solventnosti, ziskovosti a efektivnosti vaší organizace za rok.                                                                                                                                                                                                                           |
| [12měsíční kumulované výdaje – výchozí](https://mix.office.com/watch/iywod5qmqhz7)                       | Získejte přehled o výdajích pro každý z posledních 12 měsíců. Těchto 12 měsíců může zahrnovat více než jeden fiskální rok.                                                                                                                                                                                                       |
| [Kumulovaný výkaz čtvrtletích příjmů – výchozí](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Zobrazte ziskovost organizace čtvrtletně za minulý rok a rok k datu.                                                                                                                                                                                                                   |
| [Rozvaha vedle sebe – výchozí](https://mix.office.com/watch/zkgq0u7visw9)                      | Zobrazte přehled finanční pozice organizace pro rok. Tato sestava uvádí aktiva a pasiva a jmění akcionářů vedle sebe.                                                                                                                                                                                |
| [Souhrnná předvaha – výchozí](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Obsahuje informace o zůstatku pro všechny účty s počátečními a závěrkovými zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem.                                                                                                                                                                  |
| [Souhrnná roční předvaha – výchozí](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Obsahuje informace o zůstatku pro všechny účty s počátečními a závěrkovými zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem pro aktuální a minulý rok.                                                                                                                           |
| [Týdenní prodeje a slevy – výchozí](https://mix.office.com/watch/112ng0hy5de0j)                     | Získejte přehled o prodeji a slevách pro každý týden v měsíci. Tato sestava zahrnuje součet za čtyři týdny.                                                                                                                                                                                                              |
| [Dostupné rozpočtové prostředky – výchozí](https://mix.office.com/watch/15hcpezcbx7tv)                         | Zobrazení podrobného porovnání revidovaného rozpočtu, skutečných výdajů, rezervací rozpočtu a rozpočtových prostředků, které jsou k dispozici pro všechny účty                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Otevření finančních výkazů
Po kliknutí na nabídku **Finanční vykazování** se zobrazí seznam výchozí finančních výkazů pro danou společnost. Poté můžete otevřít nebo upravit sestavu. Chcete-li otevřít jednu z výchozích sestav, vyberte název sestavy. Při prvním otevření se sestava automaticky generuje pro předchozí měsíc. Například pokud otevřete sestavu poprvé v srpnu 2016, je sestava generována pro 31. července 2016. Po otevření sestavy můžete začít s prohlížením rozbalením specifických částí dat a změnou možností sestavy.

## <a name="creating-and-modifying-financial-reports"></a>Vytváření a úpravy finančních výkazů
Ze seznamu finančních výkazů lze vytvořit novou sestavu nebo upravit existující sestavu. Pokud máte příslušná oprávnění, můžete vytvořit novou finanční sestavu klepnutím na **Nové** v podokně akcí. Program Sestava návrháře se stáhne do zařízení. Po spuštění Návrháře sestavy pak můžete vytvořit novou sestavu. Po uložení nové sestavy se zobrazí v seznamu finančních výkazů. V seznamu se zobrazí pouze sestavy, které byly vytvořeny pro společnost, kterou právě používáte v aplikaci Finance and Operations. Další informace o procesu vytváření a úprav finančních výkazů v aplikaci Finance and Operations najdete v těchto [příspěvcích](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) na blogu finančního výkaznictví Dynamics. **Poznámka:** Počítač, do kterého stahujete klienta návrháře sestav musí mít nainstalovanou verzi 4.6.2 rozhraní Microsoft .NET Framework. Tuto verzi rozhraní Microsoft .NET Framework si můžete stáhnout a nainstalovat [zde](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Pokud používáte Chrome, je nutné nainstalovat rozšíření ClickOnce, abyste mohli stáhnout klienta návrháře sestav. Pokud používáte režim incognito, zkontrolujte, zda že je povoleno rozšíření ClickOnce pro režim incognito. Také lze upravit sestavu, která se zobrazí v seznamu finančních výkazů. Jakmile se vybere oblast kolem názvu sestavy, klikněte na tlačítko **Upravit** v podokně akcí. Spustí se program Návrhář sestav.

<a name="see-also"></a>Viz také
--------

[Zobrazit finanční sestavy](view-financial-reports.md)

[Blog o finančním výkaznictví v Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)





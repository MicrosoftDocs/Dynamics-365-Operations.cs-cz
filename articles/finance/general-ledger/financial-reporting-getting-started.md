---
title: Přehled finančního výkaznictví
description: Toto téma popisuje, kde získat přístup k účetnímu výkaznictví v Microsoft Dynamics 365 Finance a jak používat finanční možnosti vytváření sestav. Obsahuje popis výchozích finančních sestav, které jsou k dispozici.
author: aprilolson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01fcc7c4f3e1eb7aadfc93b120cd57e62077d0c0
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249053"
---
# <a name="financial-reporting-overview"></a>Přehled finančního výkaznictví

[!include [banner](../includes/banner.md)]

Toto téma popisuje, kde získat přístup k účetnímu výkaznictví a jak používat finanční možnosti vytváření sestav. Obsahuje také popis výchozích finančních sestav, které jsou k dispozici.

<a name="accessing-financial-reporting"></a>Přístup k finančnímu výkaznictví
-----------------------------

Nabídku **Finanční vykazování** lze najít na následujících místech:

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
| Udržovat zabezpečení finančního výkaznictví | Udržujte zabezpečení finančního výkaznictví a provádějte úkoly správy. | FinancialReportsSecuritySystemMaintain |
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

## <a name="report-deletions-and-expirations"></a>Odstranění a vypršení platnosti sestav
Uživatelé, kteří vygenerovali sestavu, ji mohou i odstranit. Uživatelé s povinností **Udržovat zabezpečení finančního výkaznictví** mohou odstranit sestavy jiných uživatelů. 

Počínaje vydáním 10.0.7 byl zaveden koncept dat vypršení platnosti. V pracovním prostoru pro správu funkcí bude povolena nová povinná funkce. Tato funkce obsahuje následující změny:
* Nově generované sestavy budou automaticky označeny datem vypršení platnosti 90 dní od jejich vygenerování.
* Všechny existující sestavy před instalací této funkce budou mít dobu platnosti 90 dní. Datum se může po krátkou dobu zobrazit jako prázdné, dokud není spuštěna služba finančního výkaznictví, vygeneruje se sestava a služba provede aktualizaci existujících sestav s prázdným datem vypršení platnosti. 
* K této funkci mají přístup uživatelé s povinností **Udržovat zabezpečení finančního výkaznictví**. Uživatel s povinností **Udržovat finanční sestavy** s oprávněním **Udržovat vypršení platnosti finančních sestav** má také možnost změnit dobu vypršení platnosti. Nyní jsou k dispozici dvě možnosti uchování sestav: 
  * Vypršení platnosti za 90 dní
  * Možnost nastavení nekonečné doby vypršení platnosti sestavy

Je-li vybráno vypršení platnosti 90 dnů, zaručuje platnost 90 dní ode dneška, což je odlišné chování, než 90 dnů od data původního generování nastaveného během generování sestavy. 

## <a name="default-reports"></a>Výchozí sestavy
Finanční vykazování poskytuje 22 výchozích finančních výkazů. Každá sestava používá výchozí kategorie hlavního účtu. Tyto sestavy lze použít tak, jak jsou, nebo slouží jako výchozí bod vaše potřeby finančního vykazování. Kromě tradiční finančních výkazů, například výkaz zisků a ztrát nebo rozvaha, tyto výchozí sestavy zahrnují sestavy, které zobrazují různé typy finančních výkazů, které je možné vytvořit. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Výchozí sestava                                                                                         | Popis                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12měsíční kumulativní výkaz příjmu s jedním sloupcem – výchozí | Zobrazte ziskovost organizace za posledních 12 měsíců v jednom sloupci.                                                                                                                                                                                                                                      |
| 12měsíční výkaz příjmu trendů – výchozí                 | Zobrazte ziskovost organizace za každý ze 12 posledních měsíců. Těchto 12 měsíců může zahrnovat více než jeden fiskální rok.                                                                                                                                                                                             |
| Skutečnost vs rozpočet – výchozí                                | Zobrazte podrobné informace o zůstatku pro všechny účty původního rozpočtu a porovnejte revidovaný rozpočet se skutečnými hodnotami, které vykazují odchylku.                                                                                                                                                                          |
| Podrobnosti auditu – výchozí                                  | Zobrazte podrobné informace o zůstatku pro všechny účty. Tato sestava zobrazuje debetní a kreditní zůstatky v měně vykazování a místní měně, společně s dalšími informacemi o transakci, jako je například ID uživatele, uživatel, který naposledy upravil data, datum poslední změny a kód ID deníku. |
| Výpis zůstatků – výchozí                                   | Zobrazte podrobné informace o zůstatku pro všechny účty. Tato sestava zobrazuje počáteční a konečné zůstatky a debetní a kreditní zůstatky pro aktuální období a rok k datu, společně s dalšími informacemi o transakci, jako je například doklad.                                                                    |
| Rozvaha – výchozí                                   | Zobrazte přehled finanční pozice organizace pro rok.                                                                                                                                                                                                                                                             |
| Rozvaha a výpis příjmu vedle sebe – výchozí | Zobrazte finanční pozici a ziskovost organizace za rok vedle sebe.                                                                                                                                                                                                                              |
| Cashflow – výchozí                                       | Získejte přehled o hotovosti, která přichází do organizace a odchází z ní.                                                                                                                                                                                                                                   |
| Podrobná revize JE a TB – výchozí                      | Zobrazte počáteční zůstatek a informace o aktivitě pro všechny účty.                                                                                                                                                                                                                                                      |
| Podrobná předvaha – výchozí                         | Zobrazte informace o zůstatku na všech účtech, které mají zůstatky má dáti a dal, a jejich čisté hodnoty, spolu s datem transakce, dokladem a popisem deníku.                                                                                                                                  |
| Čtvrtletní trend výdajů za tři roky – výchozí             | Získejte přehled o výdajích za posledních 12 čtvrtletí v předchozích třech letech.                                                                                                                                                                                                                                   |
| Podrobná revize finančních popisků JE a TB – výchozí            | Zobrazte přehled zůstatků a aktivity pro finanční popisky aktiv, pasiv, jmění vlastníka, výnosů, výdajů, zisků nebo ztrát.                                                                                                                                                                           |
| Výkaz příjmu – výchozí                                | Umožňuje zobrazit ziskovost organizace za aktuální období a také od začátku roku.                                                                                                                                                                                                                                   |
| Seznam účetních transakcí – výchozí                        | Zobrazte podrobné informace o zůstatku pro všechny účty. Tato sestava zobrazuje zůstatky má dáti a dal a další informace o transakci, jako je například datum transakce, číslo deníku, doklad, typ zaúčtování a sledovací číslo.                                                                            |
| Poměry – výchozí                                          | Umožňuje zobrazit poměry solventnosti, ziskovosti a efektivnosti vaší organizace za rok.                                                                                                                                                                                                                           |
| 12měsíční kumulované výdaje – výchozí                       | Získejte přehled o výdajích pro každý z posledních 12 měsíců. Těchto 12 měsíců může zahrnovat více než jeden fiskální rok.                                                                                                                                                                                                       |
| Kumulovaný výkaz čtvrtletích příjmů – výchozí               | Zobrazte ziskovost organizace čtvrtletně za minulý rok a rok k datu.                                                                                                                                                                                                                   |
| Rozvaha vedle sebe – výchozí                      | Zobrazte přehled finanční pozice organizace pro rok. Tato sestava uvádí aktiva a pasiva a jmění akcionářů vedle sebe.                                                                                                                                                                                |
| Souhrnná předvaha – výchozí                          | Obsahuje informace o zůstatku pro všechny účty s počátečními a závěrkovými zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem.                                                                                                                                                                  |
| Souhrnná roční předvaha – výchozí           | Obsahuje informace o zůstatku pro všechny účty s počátečními a závěrkovými zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem pro aktuální a minulý rok.                                                                                                                           |
| Týdenní prodeje a slevy – výchozí                     | Získejte přehled o prodeji a slevách pro každý týden v měsíci. Tato sestava zahrnuje součet za čtyři týdny.                                                                                                                                                                                                              |
| Dostupné rozpočtové prostředky – výchozí                         | Zobrazení podrobného porovnání revidovaného rozpočtu, skutečných výdajů, rezervací rozpočtu a rozpočtových prostředků, které jsou k dispozici pro všechny účty                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Otevření finančních výkazů
Po kliknutí na nabídku **Finanční vykazování** se zobrazí seznam výchozí finančních výkazů pro danou společnost. Poté můžete otevřít nebo upravit sestavu. Chcete-li otevřít jednu z výchozích sestav, vyberte název sestavy. Při prvním otevření se sestava automaticky generuje pro předchozí měsíc. Například pokud otevřete sestavu poprvé v srpnu 2016, je sestava generována pro 31. července 2016. Po otevření sestavy můžete začít s prohlížením rozbalením specifických částí dat a změnou možností sestavy.

## <a name="creating-and-modifying-financial-reports"></a>Vytváření a úpravy finančních výkazů
Ze seznamu finančních výkazů lze vytvořit novou sestavu nebo upravit existující sestavu. Pokud máte příslušná oprávnění, můžete vytvořit novou finanční sestavu klepnutím na **Nové** v podokně akcí. Program Sestava návrháře se stáhne do zařízení. Po spuštění Návrháře sestavy pak můžete vytvořit novou sestavu. Po uložení nové sestavy se zobrazí v seznamu finančních výkazů. V seznamu se zobrazí pouze sestavy, které byly vytvořeny pro společnost, kterou právě používáte v aplikaci Finance. 

> [!NOTE] 
> Počítač, do kterého stahujete klienta návrháře sestav musí mít nainstalovanou verzi 4.6.2 rozhraní Microsoft .NET Framework. Tuto verzi rozhraní Microsoft .NET Framework si můžete stáhnout a nainstalovat z [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53345). Pokud používáte Chrome, je nutné nainstalovat rozšíření ClickOnce, abyste mohli stáhnout klienta návrháře sestav. Pokud používáte režim incognito, zkontrolujte, zda že je povoleno rozšíření ClickOnce pro režim incognito. Také lze upravit sestavu, která se zobrazí v seznamu finančních výkazů. Jakmile se vybere oblast kolem názvu sestavy, klikněte na tlačítko **Upravit** v podokně akcí. Spustí se program Návrhář sestav.

## <a name="additional-resources"></a>Další zdroje
- [Zobrazení finančních sestav](view-financial-reports.md)




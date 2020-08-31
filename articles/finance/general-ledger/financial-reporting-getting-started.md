---
title: Přehled finančního výkaznictví
description: Toto téma popisuje, kde získat přístup k účetnímu výkaznictví v Microsoft Dynamics 365 Finance a jak používat finanční možnosti vytváření sestav.
author: aprilolson
manager: AnnBe
ms.date: 08/14/2020
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
ms.openlocfilehash: 1944eda5fe933ff9fdf2b9a837eb2336e8b3a0d5
ms.sourcegitcommit: 1322b94f10470e1728cf330d2d64f1471838c055
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/14/2020
ms.locfileid: "3696681"
---
# <a name="get-started-with-financial-reporting"></a>Začínáme s Financial reporting 

[!include [banner](../includes/banner.md)]

Toto téma popisuje, kde získat přístup k účetnímu výkaznictví a jak používat finanční možnosti vytváření sestav. Obsahuje také popis výchozích finančních sestav, které jsou k dispozici.

<a name="accessing-financial-reporting"></a>Přístup k finančnímu výkaznictví
-----------------------------

Nabídku **Finanční výkaznictví** lze najít v následujících umístěních:

-   **Hlavní kniha** &gt; **Dotazy a sestavy**
-   **Rozpočet** &gt; **Dotazy a sestavy** &gt; **Základní rozpočtování**
-   **Rozpočet** &gt; **Dotazy a sestavy** &gt; **Plánování rozpočtu**
-   **Rozpočtování** &gt; **Dotazy a sestavy** &gt; **Kontrola rozpočtu**
-   Konsolidace

Chcete-li vytvořit a generovat finanční sestavy pro právnickou osobu, nastavte následující informace pro tuto právnickou osobu:

-   Fiskální kalendář
-   Ledger
-   Účtová osnova
-   Měna

## <a name="granting-security-access-to-financial-reporting"></a>Poskytnutí bezpečnostního přístupu k Financial Reporting
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

Jakmile je uživatel přidán nebo se změní role, měl by mít uživatel během několika minut možnost přístupu k finančnímu výkaznictví. 

> [!NOTE]
> Role sysadmin je přidána do všech rolí ve financial reporting.

## <a name="report-deletions-and-expirations"></a>Odstranění a vypršení platnosti sestav
Uživatelé, kteří vygenerovali sestavu, ji mohou i odstranit. Uživatelé s povinností **Udržovat zabezpečení finančního výkaznictví** mohou odstranit sestavy jiných uživatelů. 

Ve vydání 10.0.8 byla zavedena koncepce dat vypršení platnosti. Nová požadovaná funkce je povolena na stránce **Vše** v pracovním prostoru Správa funkcí. Funkce **Zásady uchovávání finančních sestav** obsahuje následující změny:
* Nově generované sestavy budou automaticky označeny datem vypršení platnosti 90 dní od jejich vygenerování.
* Všechny existující sestavy před instalací této funkce budou mít dobu platnosti 90 dní. Datum se může po krátkou dobu zobrazit jako prázdné, dokud není spuštěna služba finančního výkaznictví, vygeneruje se sestava a služba provede aktualizaci existujících sestav s prázdným datem vypršení platnosti. 
* K této funkci mají přístup uživatelé s povinností **Udržovat zabezpečení finančního výkaznictví**. Uživatel s povinností **Udržovat finanční sestavy** s oprávněním **Udržovat vypršení platnosti finančních sestav** má také možnost změnit dobu vypršení platnosti. Nyní jsou k dispozici dvě možnosti uchování sestav: 
  * Vypršení platnosti za 90 dní.
  * Možnost nastavení nekonečné doby vypršení platnosti sestavy.
  
Pokud je vybrána doba platnosti, například 90 dní, použije se 90 dní ode dneška. Toto chování je jiné než 90 dnů od původního data generování, které bylo nastaveno při vygenerování sestavy. 
  
Další možnosti budou zváženy v budoucích funkcích. Doba vypršení 90 dnů bude výchozí a uživatelé s příslušnými oprávněními mohou přepsat výchozí nastavení na stránce se seznamem **finančních sestav**.    

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
Po výběru nabídky **Finanční výkaznictví** se zobrazí seznam výchozích finančních výkazů pro danou společnost. Poté můžete otevřít nebo upravit sestavu. Chcete-li otevřít jednu z výchozích sestav, vyberte název sestavy. Při prvním otevření se sestava automaticky generuje pro předchozí měsíc. Například pokud otevřete sestavu poprvé v srpnu 2019, je sestava generována pro 31. července 2019. Po otevření sestavy můžete začít s prohlížením rozbalením specifických částí dat a změnou možností sestavy.

## <a name="creating-and-modifying-financial-reports"></a>Vytváření a úpravy finančních výkazů
Ze seznamu finančních výkazů lze vytvořit novou sestavu nebo upravit existující sestavu. Pokud máte příslušná oprávnění, můžete vytvořit novou finanční sestavu výběrem **Nové** v podokně akcí. Program Sestava návrháře se stáhne do zařízení. Po spuštění Návrháře sestavy pak můžete vytvořit novou sestavu. Po uložení nové sestavy se zobrazí v seznamu finančních výkazů. V seznamu se zobrazí pouze sestavy, které byly vytvořeny pro společnost, kterou právě používáte v Dynamics 365 Finance. 

## <a name="reporting-tree-definitions"></a>Definice stromu výkaznictví 
Jednou ze součástí, která se používá k sestavování finančních výkazů, je definice stromu výkaznictví. Definice stromu výkaznictví pomáhá definovat strukturu a hierarchii organizace. Jedná se o strukturu hierarchie s více dimenzemi na základě vztahů mezi dimenzemi ve finančních datech. Poskytuje informace na úrovni výkazové jednotky a na souhrnné úrovni pro všechny jednotky ve stromu.

Můžete vytvořit neomezený počet stromů výkaznictví k zobrazování dat vaší organizace různými způsoby. Každý strom výkaznictví může obsahovat libovolnou kombinaci oddělení a souhrnných jednotek, ale definice sestavy může najednou odkazovat pouze na jeden strom hlášení. 


## <a name="troubleshooting-issues-opening-report-designer"></a>Problémy při otevírání Návrháře sestav
Při otevírání Návrháře sestav může dojít k několika běžným problémům. Tyto problémy a kroky k jejich vyřešení jsou následující.

Problém 1: Návrhář sestav se nespustí, když vyberete **Nový** nebo **Upravit**.

* V Internet Explorer vyberte **Nastavení**, poté vyberte **Možnosti internetu**. Vyberte kartu **Zabezpečení**. Vyberte Důvěryhodné servery a poté vyberte **Weby**. V **Přidejte tento web do zóny** zadejte "\*\.dynamics.com" (bez uvozovek) a poté vyberte **Přidat**. 
* V Internet Explorer vyberte **Nastavení**, poté vyberte **Možnosti internetu**. Vyberte kartu **Zabezpečení**. Vyberte Důvěryhodné servery. V oblasti Úroveň zabezpečení pro tuto zónu změňte možnost na **Střední-Nízká**.
* Zakažte blokování vyskakovacích oken v prohlížeči.
* K instalaci jsou vyžadovány pracovní stanice Visual Studio.NET 4.6.2 nebo vyšší.

Tuto verzi rozhraní Microsoft .NET Framework si můžete stáhnout a nainstalovat z [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53345).
* Pokud používáte prohlížeč Chrome, je nutné nainstalovat rozšíření ClickOnce, abyste mohli stáhnout klienta návrháře sestav. Pokud používáte režim incognito, zkontrolujte, zda že je povoleno rozšíření ClickOnce pro režim incognito. Pokud se nemůžete přihlásit pomocí Chromu, zkuste použít kroky nastavení popsané v 1. vydání Internet Explorer nebo Edge. 

Problém 2: Uživateli nebyla přidělena požadovaná oprávnění k používání Financial Reporting. 

* Chcete-li ověřit, zda uživatel nemá oprávnění, vyberte **Ano** u chyby „Nelze se připojit k serveru Financial Reporting. Zvolte Ano, pokud chcete pokračovat a zadejte jinou adresu serveru." Pak vyberte **Test připojení**. Pokud nemáte povolení, zobrazí se zpráva „Pokus o připojení selhal. Uživatel nemá příslušná oprávnění pro připojení k serveru. Obraťte se na vašeho správce systému."
* Požadovaná oprávnění jsou uvedena výše v [Poskytnutí bezpečnostního přístupu k Financial Reporting](#granting-security-access-to-financial-reporting). Zabezpečení ve Financial Reporting je založeno na těchto oprávněních. Nebudete mít přístup, dokud vám tato oprávnění (nebo jiná role zabezpečení, která tato oprávnění zahrnují) nebudou přiřazena. 
* Integrační úloha **Poskytovatel uživatelských služeb společnosti** (která je také odpovědná a známá jako integrace uživatelů) běží v 5minutovém intervalu. Změny oprávnění se ve Financial Reporting projeví až po 10 minutách. 
  Pokud jiný uživatel může otevřít Návrháře sestav, vyberte **Nástroje** a poté vyberte **Stav integrace**. Ověřte, zda integrační mapa „Poskytovatel firemních uživatelů pro společnost“ úspěšně fungovala, protože vám bylo uděleno oprávnění k používání Financial Reporting. 
* Je možné, že další chyba zabránila **Integrace uživatele Dynamics do Financial Reporting** v dokončení. Nebo je možné, že reset datamartu byl zahájen a ještě nebyl dokončen, nebo že došlo k jiné systémové chybě. Zkuste proces spustit znovu později. Pokud problém přetrvává, kontaktujte správce systému.

Problém 3: Můžete pokračovat předs přihlašovací stránku ClickOnce Report Designer, ale nemůžete dokončit přihlášení v návrháři sestav. 

* Čas nastavený v místním počítači po zadání přihlašovacích údajů musí být do pěti minut od času na serveru Financial Reporting. Pokud je rozdíl delší než pět minut, systém neumožní přihlášení. 
* V tomto případě doporučujeme povolit možnost Windows pro automatické nastavení času vašeho počítače. 

## <a name="additional-resources"></a>Další prostředky
- [Zobrazit finanční sestavy](view-financial-reports.md)
- [Definice organizačního stromu ve finančních sestavách](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)

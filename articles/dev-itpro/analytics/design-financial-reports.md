---
title: "Zobrazení a navržení finančních sestav"
description: "Tento článek obsahuje cvičení, která vás provedou zobrazením a vytvářením finančních sestav pro aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReportingSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 86597a81b4dcfb14cbc88667fbb1db214133c6e5
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="view-and-design-financial-reports"></a>Zobrazení a navržení finančních sestav

[!include [banner](../includes/banner.md)]

Tento článek obsahuje cvičení, která vás provedou zobrazením a vytvářením finančních sestav pro aplikaci Microsoft Dynamics 365 for Finance and Operations. Finanční výkaznictví se skládá z lepšího způsobu prohlížení v rámci aplikace Finance and Operations a návrháře sestav na jedno kliknutí, který vám umožní vytvářet a upravovat finanční sestavy.  

<a name="exercise-1-generate-and-explore-a-default-financial-report"></a>Cvičení 1: generování a prohlížení výchozí finanční sestavy
-----------------------------------------------------------

Pro toto cvičení budete generovat a prohlížet existující výchozí sestavu. Tato sestava zahrnuje všechny účty a také obsahuje vlastnosti účtu (atributy) pro účty. Budete procházet detaily transakce, používat filtry dimenzí a měnit měny v sestavě. Doporučujeme nejprve aktualizovat pořadí zobrazení dimenzí pro finanční vykazování. Tímto způsobem lze vybrat počet zobrazených dimenzí nejen při vytváření a zobrazování finančních sestav.

1.  Přejděte do části **Konfigurace finanční dimenze pro integraci aplikací** pod částí **Dimenze v účetní osnově** v hlavní knize.
2.  Přesuňte dimenze do následujícího pořadí:
    1.  Hlavní účet
    2.  Obchodní jednotka
    3.  Nákladové středisko
    4.  Oddělení

    Poznámka: jiné dimenze mohou zůstat v pořadí, ve kterém jsou.
3.  Uložte konfiguraci dimenze. Dále budeme generovat sestavu a prohlížet data v sestavě.
4.  Přejděte do části **Finanční sestavy** pod částí **Dotazy a sestavy** v hlavní knize.
5.  Vyberte řádek sestavy s názvem **Podrobnosti hlavní knihy – výchozí.**
6.  Vyberte možnost **Upravit.** Poznámka: zobrazí se výzva ke stažení návrháře sestav na jedno kliknutí a přihlášení. Přihlaste se pomocí vlastních přihlašovacích údajů.
7.  Změňte základní rok na 2012 a vyberte **Generovat**. Po vygenerování sestavy v návrháři sestav se sestava otevře na nové kartě prohlížeče. Sestavu můžete procházet buď na nové kartě prohlížeče, nebo můžete přejít do na svou původní kartu prohlížeče a otevřít sestavu tam pomocí volby ze seznamu **Finanční sestavy**.
8.  V otevřené sestavě vyberte jednu z částek k procházení podrobností o účtu pro sestavu.
9.  V podrobnostech účtu vyberte účet s daty a **procházejte na úroveň sestavy transakcí**. Na úrovni sestavy transakcí se zobrazí vlastnosti (atributy), které jsou zahrnuty do návrhu této sestavy. V závislosti na transakci a účtu mohou být zobrazeny jen některé nebo všechny atributy.
10. Zavřete úroveň transakce sestavy.
11. Vyberte stejný nebo jiný účet a **otevřete transakce dokladu.** Transakce dokladu jsou filtrovány do kombinace období, roku a účtu + dimenze vybraného účtu. Z transakcí dokladu můžete zvolit prohlížení dalších informací o transakci.
12. Zavřete transakce dokladu. V rámci finanční sestavy můžete zobrazit data pro jiné období a rok, nebo s jinými použitými atributy a dimenzemi. Tato operace se provádí pomocí volby **Možnosti sestavy**.
13. Vyberte volbu **Možnosti sestavy**.
14. Vyberte možnost **Přidat filtr dimenze** a zvolte možnost **Obchodní jednotka**.
15. Do pole zadejte „001” a stiskněte tlačítko **OK**. Sestava nyní zobrazí pouze data obchodní jednotky 001. To je přizpůsobené zobrazení sestavy není k dispozici pro ostatní
16. Zavřete filtrovanou sestavu. Finanční sestavy lze zobrazit v libovolné měně, která je přidána do aplikace Finance and Operations.
17. Vyberte možnost **Měna**, poté možnost **EUR.** Sestava se nyní zobrazuje v měně euro. Všechny kódy měn nebo symboly měny zahrnuté v návrhu sestavy se nyní zobrazí v použité měně. Není-li definován žádný symbol měny pro měnu, nebude symbol měny zobrazen.
18. Zavřít sestavu **Podrobnosti hlavní knihy**.
19. Zavřete **Návrháře sestav**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>Cvičení 2: Přidání dalších účetních vlastností do návrhu sestavy
V tomto cvičení budete upravovat existující výchozí sestavu. Budete aktualizovat definici řádku k zahrnutí do všech účtů i definici sloupce, která má obsahovat atributy účtu. Po dokončení aktualizace budete vygenerovat sestavu nově vytvořené sestavy a prohlížet sestavu. Začneme ze seznamu Finanční výkazy.

1.  Přejděte do části **Finanční sestavy** pod částí Dotazy a sestavy v hlavní knize.
2.  Vyberte řádek sestavy s názvem **Souhrnná předvaha – výchozí.**
3.  Vyberte možnost **Upravit**. **Souhrnná předvaha – výchozí** bude otevřena v Návrháři sestav.
4.  Vyberte nabídku **Soubor**, poté **Uložit jako** a zadejte název sestavy Podrobná předvaha s atributy. Poznámka: při každém vytvoření nové sestavy v návrháři sestav se seznam finančních sestav v aplikaci Finance and Operations aktualizuje.
5.  Z definice sestavy vyberte ikonu definice řádku a otevřete možnost **Předvaha – výchozí definice řádku**.
6.  Uložit definici řádku jako **Podrobná předvaha s atributy**
7.  S kurzorem na řádku 50 vyberte možnost **Upravit**, poté **Vložit řádky z dimenzí**. Příkaz Vložit řádky z dimenzí umožňuje vybrat dimenze, které mají být v definici řádku. U tohoto cvičení vytvoříme definici řádku pomocí hlavního účtu.
8.  Ujistěte se, že **hlavní účet** obsahuje všechny ampersandy (&), a klikněte na tlačítko **OK**. Definice řádku nyní obsahuje všechny hlavní účty pro výchozí právnickou osobu USMF.
9.  Přejděte k řádku 11110 a odstraňte řádek 11110.
10. V řádku 11080 vyberte **---(podtržítko částek)**.
11. V řádku 11140 zadejte **součet všech účtů** ve sloupci B.
12. Ve sloupci C vyberte **TOT** z rozevírací nabídky.
13. Zadejte **50:11080** do sloupce D.
14. **Uložte** definici řádku. Definice řádku nyní obsahuje všechny účty a dále řádek součtu k přidání všech účtů společně. Dále budeme aktualizovat definici sloupce, aby zahrnovala další atributy účtu.
15. Z definice sestavy **Podrobná předvaha s atributy** vyberte ikonu definice sloupce a otevřete definici sloupců **Souhrnná předvaha – výchozí**.
16. Uložit definici sloupce jako **Podrobná předvaha s atributy**. Definice sloupce obsahuje sloupce finančních údajů, sloupec popisu a sloupec výpočtu. Budeme přidávat sloupce atributů pro definici sloupce k poskytnutí dalších podrobností o účtech.
17. Tyto atributy budou přidány do definice sloupců:
    -   Číslo deníku
    -   Popis deníku
    -   Datum transakce
    -   Vytvořil(a)
    -   Naposledy změněno uživatelem

18. Ve sloupci I vyberte **ATTR** jako typ sloupce. Poté vyberte **Číslo deníku** jako kategorii atributu.
19. Pokračujte v přidávání sloupců pro zbývající atributy.
20. V řádku **Záhlaví 2** přidejte popis jednotlivých nových sloupců, které byly přidány.
21. Uložte definici sloupce. Nyní po aktualizaci definice řádků a sloupců je nutné přidat je do definice sestavy.
22. Z definice sestavy **Podrobná předvaha s atributy** vyberte možnost Podrobná předvaha s atributy pro definici řádků i sloupců.
23. Změňte základní rok na **2012.**
24. **Uložte** definici sestavy a **generujte**. Po dokončení generování sestavy a jejím otevření můžete procházet sestavu stejně jako v prvním cvičení. Procházejte různé účty a podívejte se na zobrazení dalších atributů.
25. Zavřete sestavu **Podrobná předvaha s atributy**.
26. Zavřete **Návrháře sestav**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>Cvičení 3: Vytvoření multidimenzionální sestavy pomocí stromu výkaznictví
V tomto cvičení budete upravovat existující výchozí sestavu. Vytvoříte strom výkaznictví a budete přidávat do definice sestavy, abyste vytvořili výpis nákladového střediska / divizních příjmů. Po dokončení aktualizace budete generovat výpis nákladového střediska / divizních příjmů a prohlížet sestavu pomocí stromu výkaznictví. Začneme ze seznamu Finanční výkazy.

1.  Přejděte do části **Finanční sestavy** pod částí Dotazy a sestavy v hlavní knize.
2.  Vyberte řádek sestavy s názvem **Výkaz příjmu – výchozí**
3.  Vyberte možnost **Upravit**. **Výkaz příjmu – výchozí** se otevře v Návrháři sestav.
4.  V nabídce **Soubor** se přesuňte na tlačítko **Nový** a vyberte možnost **Definice stromu výkaznictví**
5.  V nabídce **Upravit** klikněte na tlačítko **Vložit jednotky výkaznictví z dimenzí**...
6.  Zrušte zaškrtnutí políček pro všechny dimenze s výjimkou **Nákladového střediska**.
7.  Klikněte na pole **Od dimenze** pro dimenzi nákladového střediska, zapište **007** a stiskněte klávesu tabulátor. Do pole **Do dimenze** zapište **018**.
8.  **Uložte** výsledný strom pod názvem **Nákladová střediska podle divizí.** Nyní, když byl vytvořen strom výkaznictví, upravte strom výkaznictví, aby obsahoval tři nové kumulativní jednotky: Marketing, Operace a Maloobchod.
9.  V nabídce **Okno** klikněte na tlačítko **Nákladová střediska podle divizí**. (Pokud byl strom výkaznictví uzavřen, vyberte ho z Definic stromu výkaznictví v navigačním podokně.)
10. Klikněte na jednotku číslo dvě, **Veletrhy**, a klikněte na ikonu **Vložit jednotku výkaznictví**.
11. Poklepejte na sloupec entity pro prázdném řádku a vyberte **USMF**.
12. Zapište **Marketing** do sloupců B a C.
13. Klikněte na jednotku číslo pět, **Servisní operace**, a klikněte pravým tlačítkem myši. **Zvolte možnost Vložit jednotku výkaznictví**.
14. Opakujte krok 11.
15. Zapište **Operace** do sloupců B a C.
16. Klikněte na jednotku číslo dvanáct, **Prodejna**, a klikněte pravým tlačítkem myši. Zvolte možnost **Vložit jednotku výkaznictví**.
17. Opakujte krok 11.
18. Zapište **Maloobchod** do sloupců B a C. Všimněte si, že jednotky Marketing, Operace a Maloobchod se zobrazí na stejné úrovni jako aktuální kumulativní jednotky. Nové jednotky jsou uspořádány dále. Jednotky vykazování jsou uspořádány prostřednictvím voleb po kliknutí pravým tlačítkem myši: posunutím nahoru a dolů nebo přetažením myší.
19. Ověřte, že jednotka tři, **Veletrhy**, je aktivní a klikněte na ni pravým tlačítkem myši.
20. Zvolte možnost **Snížit úroveň jednotky výkaznictví**. Všimněte si, že se jednotka nyní zobrazí jako podřízená **Marketingu**.
21. Klikněte na jednotku čtyři, **Marketingová** **kampaň** a klikněte na ni pravým tlačítkem myši.
22. Zvolte možnost **Snížit úroveň jednotky výkaznictví**.
23. Klikněte na možnost **Servisní operace** v grafickém zobrazení. Stiskněte a podržte levé tlačítko myši při přetažení jednotky do **Operací**. Uvolněte levé tlačítko myši a upusťte jednotku do kumulativní skupiny Operace. Zopakujte pro položky **Výroba, Řízení kvality, Logistika, Zásobování a Správa**.
24. Nastavte položky **Prodejna**, **Super**, **Market** a **Online** jako podřízené položky **Maloobchod** snížením úrovně nebo přetažením.
25. Uložte výslednou reorganizaci. Nyní když máme vytvořený a uspořádaný strom výkaznictví, můžeme jej přidat k definici sestavy.
26. V nabídce **Okno** klikněte na příkaz **Výkaz příjmu – výchozí** a otevřete definice sestavy.
27. Klikněte na šipku rozevíracího seznamu **Typ stromu** a vyberte **Strom výkaznictví**.
28. Kliknutím na šipku rozevíracího seznamu stromu vyberte **Nákladová střediska podle divizí**.
29. Změňte základní rok na **2012**, **uložte** změny a **generujte** sestavu. Po dokončení generování sestavy a jejím otevření můžete sestavu prohlížet.
30. Vyberte rozevírací seznam **Strom výkaznictví** a zobrazte jednotky vykazování. Rovněž je možné procházet podrobnosti řádku zprávy a zobrazit všechny zůstatky všech jednotek stromu výkaznictví.
31. Zavřete **Výkaz příjmu – výchozí**.
32. Zavřete **Návrháře sestav**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>Cvičení 4: Vytvoření konsolidované sestavy pomocí organizační hierarchie
V tomto cvičení budete upravovat existující výchozí sestavu. Budete přidávat organizační hierarchii v definici sestavy, abyste vytvořili výkaz konsolidovaných příjmů a rozvahu. Po dokončení aktualizace budete generovat výpis konsolidovanou sestavu a prohlížet sestavu pomocí stromu výkaznictví. Začneme ze seznamu Finanční výkazy.

1.  Přejděte do části **Finanční sestavy** pod částí Dotazy a sestavy v hlavní knize.
2.  Vyberte řádek sestavy s názvem **Rozvaha a výkaz příjmů vedle sebe – výchozí**
3.  Vyberte možnost **Upravit**. **Rozvaha a výkaz příjmů vedle sebe – výchozí** se otevře v návrháři sestav.
4.  Vyberte nabídku **Soubor** &gt; **Uložit jako** a zadejte název sestavy **Konsolidovaná rozvaha a výkaz příjmů vedle sebe**.
5.  Změňte základní rok na 2012.
6.  Klikněte šipku rozevíracího seznamu typ stromu a vyberte **Organizační hierarchie**.
7.  Klikněte šipku rozevíracího seznamu typ stromu a vyberte **Contoso Holdings.**.
8.  Uložte změny a generujte sestavu. Pokud se zobrazí dotaz, vyberte všechny jednotky sestavy. Po dokončení generování sestavy a jejím otevření můžete sestavu prohlížet.
9.  Vyberte volbu **Možnosti sestavy**.
10. Vyberte možnost **Přidat filtr dimenze** a zvolte možnost **Oddělení**.
11. Do pole zadejte **022** a klikněte na tlačítko **OK**.
12. Zavřete filtrovanou sestavu.
13. Vyberte rozevírací seznam **Strom** výkaznictví a zobrazte jednotky vykazování. Rovněž je možné procházet podrobnosti řádku zprávy a zobrazit všechny zůstatky všech jednotek stromu výkaznictví.
14. Zavřete **Konsolidovanou rozvahu a výpis příjmu vedle sebe – výchozí**.
15. Zavřete **Návrháře sestav**.

## <a name="exercise-5-create-a-sidebyside-departmental-report"></a>Cvičení 5: Vytvoření sestavy oddělení vedle sebe
V tomto cvičení budete vytvářet novou sestavu. Sestava je výkaz příjmu oddělení vedle sebe. Použijete existující definici řádku, ale vytvoříte novou definici sestavy a novou definici sloupce, která používá filtry dimenzí. Začneme ze seznamu Finanční výkazy.

1.  Přejděte do části **Finanční sestavy** pod částí Dotazy a sestavy v hlavní knize.
2.  Vyberte možnost **Nový**. Otevře se návrhář sestav s prázdnou definicí sestavy. Váš první úkol bude vytvoření definice sloupců.
3.  Kliknutím na nabídku **Soubor**, pak **Nový** a pak **Definice sloupce** vytvoříte novou definici sloupce .
4.  Ve **sloupci A** vyberte **DESC** jako typ sloupce.
5.  Ve **sloupci B** vyberte **FD** jako typ sloupce.
6.  Poklepejte na pole **Filtr dimenze**.
7.  V okně **Dimenze** poklepejte na sloupec **Oddělení**.
8.  V části Jednotlivec nebo rozsah dialogového okna klikněte **elipsu** pole **Od**, abyste zobrazili seznam oddělení.
9.  Vyberte oddělení **022**, **Prodej a marketing** a klikněte na tlačítko **OK**.
10. Zopakujte kroky 5 až 8 pro oddělení 23–25.
11. Na řádku **Záhlaví 2** pro každý sloupec FD zadejte následující popisy oddělení:
    -   Sloupec B – Prodej a marketing
    -   Sloupec C – Operace
    -   Sloupec D – Finance
    -   Sloupec E – IT

12. Definici sloupce uložte jako Oddělení vedle sebe. Vzhledem k tomu, že používáme existující definici řádku, definici sestavy nyní lze změnit, aby používala nově vytvořené definice sloupců a existující definici řádku.
13. V nabídce **Okno** klikněte na příkaz **Nová definice sestavy** a otevřete definice sestavy.
14. Vyberte **Výkaz příjmu – výchozí** jako definici řádků a **Oddělení vedle sebe** jako definici sloupců.
15. Uložte definici sestavy jako **Výkaz příjmu oddělení vedle sebe**.
16. Změňte základní rok na **2012.**
17. Nastavte úroveň podrobností na **Finanční, účetní a transakční**.
18. **Uložte** provedené změny a **generujte**. Po dokončení generování sestavy a jejím otevření můžete sestavu prohlížet.

## <a name="additional-resources"></a>Další prostředky
[Finanční vykazování](../../financials/general-ledger/financial-reporting-getting-started.md) 
[Zobrazit finanční sestavy](../../financials/general-ledger/view-financial-reports.md) 
[Blog Dynamics Financial Reporting](http://blogs.msdn.com/b/dynamics_financial_reporting/)





---
title: "Nákladové účetnictví analýzy obsahu Power BI"
description: "Toto téma popisuje, co je zahrnuto do analýzy nákladového účetnictví obsahu Power BI. Popisuje, jak přístup k sestavám Power BI a obsahuje informace o datovém modelu a entit, které byly použity k sestavení obsahu."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-02-10 15 - 07 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Nákladové účetnictví analýzy obsahu Power BI

Toto téma popisuje, co je zahrnuto do analýzy nákladového účetnictví obsahu Power BI. Popisuje, jak přístup k sestavám Power BI a obsahuje informace o datovém modelu a entit, které byly použity k sestavení obsahu.

<a name="overview"></a>Přehled
--------

**Analýzy nákladového účetnictví** obsah Microsoft Power BI je určen pro náklady řadiče nebo kdokoli, kdo je odpovědný za provádění řízení nákladů organizace. Zahrnuje klíčové metriky, jako jsou náklady, velikost a nákladové sazby podle skutečných nákladů, rozpočtové náklady a Náklady pružného rozpočtu. Používá data transakce nákladového účetnictví do Microsoft Dynamics 365 pro operace a poskytuje agregované zobrazení nákladů pro celou organizaci, v jedné měně pro hlášení. Vedoucí data můžete filtrovat podle nákladové objekty pro provádění řízení nákladů organizačních jednotek, i v případě, že organizace může mít více právních subjektů. Vzhledem k tomu, **analýzy nákladového účetnictví** obsahu Power BI zvýrazní rozdíly mezi skutečnými náklady a rozpočtové náklady, vedoucí můžete upozorněni o pozitivní a negativní trendy pro jejich provozní jednotky. Vedoucí k podrobnostem cena prvek hierarchie nebo jednotlivých nákladových položek chcete-li získat podrobný přehled o jak odchylky nákladů došlo a potom přijmout účinná opatření. **Analýzy nákladového účetnictví** Power BI obsahu Řekněme analyzovat náklady účetní náklady jak prochází nákladové objekty v celé organizaci. Další informace o nákladovém účetnictví naleznete v tématu [nákladového účetnictví domovské stránky](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Definování zabezpečení úroveň přístupu v nákladovém účetnictví a kombinace s zabezpečení na úrovni řádků v Power BI, můžete povolit všechny vlastníky objektů náklady přístup k **analýzy nákladového účetnictví** obsahu Power BI. Všechna data vizualizace bude poté filtrovat na základě úroveň přístupu, který je řízen v nákladovém účetnictví. Další informace o zabezpečení na úrovni přístupu a zabezpečení na úrovni řádku, naleznete v [nastavení zabezpečení obsahu nákladového účetnictví pro Power BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Můžete najít **analýzy nákladového účetnictví** obsahu Power BI v knihovně Sdílené datové zdroje v Microsoft Dynamics Lifecycle Services (LCS). Další informace o tom, jak stáhnout obsah a připojit k vaší 365 Dynamics pro datové operace, viz [obsahu Power BI od společnosti Microsoft a partnerů LCS](power-bi-content-microsoft-partners.md). **Poznámka:** KB4011327 ** ** je nezbytným předpokladem pro to **analýzy nákladového účetnictví** obsahu Power BI.  Po přihlášení k poskytování služeb, můžete přistupovat KB zde: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
Obsah zahrnuje sadu stránky sestavy. Každá stránka obsahuje sadu metriky, které jsou zobrazována jako grafy, kameny a tabulky. Následující tabulka obsahuje přehled vizualizace v **analýzy nákladového účetnictví** obsahu Power BI.

| Stránky sestavy                      | Graf                                                                                                                         | Dlaždice                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Řízení nákladů podle fiskálního období    | Skutečné náklady a podle úrovně hierarchie prvek nákladů                                                                   | Skutečné náklady vs rozpočtových nákladů                    |
|                                  | Odchylka rozpočtu podle úrovně hierarchie prvek nákladů                                                                               | Skutečné náklady vs kurzu rozpočtu nákladová sazba          |
|                                  | Odchylka rozpočtu prvních 10 v procentech podle nákladové složky                                                                          | Velikost rozpočtu vs skutečné velikosti          |
| Řízení nákladů podle roku     | Skutečné náklady a podle období kalendářního roku                                                                           | Skutečné náklady vs rozpočtových nákladů                    |
|                                  | Odchylka rozpočtu podle období kalendářního roku                                                                                       | Skutečné náklady vs kurzu rozpočtu nákladová sazba          |
|                                  | Odchylka rozpočtu prvních 10 v procentech podle nákladové složky                                                                          | Velikost rozpočtu vs skutečné velikosti          |
| Nákladová sazba podle fiskálního roku         | Skutečná nákladová sazba nákladů chováním.                                                                                             | Skutečné náklady vs kurzu rozpočtu nákladová sazba          |
|                                  | Skutečná nákladová sazba rozpočtové sazby pole Odchylka nákladů, rozpočtu nákladů procentní sazbou a rozpočtu nákladová sazba podle úrovně hierarchie prvek nákladů | Velikost rozpočtu vs skutečné velikosti          |
|                                  | Odchylka rozpočtu podle úrovně hierarchie prvek nákladů                                                                               |                                               |
|                                  | Odchylka rozpočtu prvních 10 v procentech podle nákladové složky                                                                          |                                               |
| Pružný rozpočet podle fiskálního období | Skutečné náklady, rozpočtové náklady a Náklady pružného rozpočtu podle úrovně hierarchie prvek nákladů                                             | Velikost rozpočtu vs skutečné velikosti          |
|                                  | Odchylka rozpočtu a rozptyl pružný rozpočet podle úrovně hierarchie prvek nákladů                                                  | Skutečné náklady vs pružný rozpočet nákladů           |
|                                  | Skutečných nákladů, rozpočtu nákladů a flexibilních nákladů podle nákladových chování a nákladů úroveň hierarchie prvek                                  | Skutečné náklady na kurz vs pružného rozpočtu nákladová sazba |
| Výpis nákladů podle fiskálního období  | Úroveň hierarchie prvek nákladů a název členu dimenze objektu náklady skutečné náklady                                             |                                               |
|                                  | Název členu dimenze náklady objektu a název členu dimenze prvek náklady skutečné náklady                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Dynamics 365 pro data operace se používá k vyplnění stránky sestavy **analýzy nákladového účetnictví** obsahu Power BI. Tato data jsou reprezentována jako agregační hodnoty, které jsou připraveny v úložišti Entity, což je databáze Microsoft SQL, která je optimalizována pro analytics. Další informace naleznete v tématu [BI napájení Přehled integrace s úložištěm Entity](power-bi-integration-entity-store.md). Následující klíče souhrnné měření slouží jako základ pro obsah.

| Celek                  | Agregované míry klíče | Zdroj dat pro Dynamics 365 pro operace | Pole     | popis                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Náklady účetní položky | SUM(amount)               | CAMDATAAggregatedCostEntry                  | Částka    | Částka v měně knihy nákladového účetnictví |
| Statistické položky     | SUM(MAGNITUDE)            | CAMDATAAggregatedStatisctialEntry           | Hodnota |                                               |

Následující tabulka zobrazuje, jak agregační klíčové měření slouží k vytvoření několika vypočtené rozměry v obsahu dataset.

| Měřítko                                       | Jak vypočítat rozměr                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Skutečné náklady                                   | Výpočet ("položky Nákladové účetnictví"\[opatření\], 'Transakce verze'\[ISSOURCEVERSIONBUDGET\_hodnoty\] = 0)            |
| Rozpočtové náklady                                   | Výpočet ("položky Nákladové účetnictví"\[opatření\], 'Transakce verze'\[ISSOURCEVERSIONBUDGET\_hodnoty\] = 1)            |
| Odchylka rozpočtu nákladů                          | \[Rozpočet nákladů\] - \[skutečné náklady\]                                                                                      |
| Procentuální odchylka rozpočtu                    | IF (\[rozpočtové náklady\] = 0, blank(), \[odchylka rozpočtu\] / \[rozpočtové náklady\])                                                |
| Skutečná velikost                              | Výpočet ('Statistické položky'\[FullMagnitude\], 'Transakce verze'\[ISSOURCEVERSIONBUDGET\_hodnoty\] = 0)          |
| Velikost rozpočtu                              | Výpočet (\[FullMagnitude\], 'Transakce verze'\[ISSOURCEVERSIONBUDGET\_hodnoty\] = 1)                               |
| Odchylka rozpočtu statistické                   | \[Velikost rozpočtu\] - \[skutečná velikost\]                                                                            |
| Procento odchylky statistických rozpočtu        | IF (\[velikosti rozpočtu\] = 0, blank(), \[rozpočtu statistický rozptyl\] / \[velikosti rozpočtu\])                          |
| Skutečná nákladová sazba                              | IF (\[skutečná velikost\] = 0, BLANK(), \[skutečné náklady\] / \[skutečná velikost\])                                          |
| Rozpočtová nákladová sazba                              | IF (\[velikosti rozpočtu\] = 0, BLANK(), \[rozpočtové náklady\] / \[velikosti rozpočtu\])                                          |
| Míra odchylky rozpočtových nákladů                     | \[Rozpočtu nákladová sazba\] - \[Skutečná nákladová sazba.\]                                                                            |
| Rozpočtové náklady procento odchylky          | IF (\[rozpočtové náklady\] = 0, blank(), \[rychlost odchylka nákladů rozpočtu\] / \[rozpočtu nákladová sazba\])                                 |
| Dlouhodobý rozpočet nákladů                             | Výpočet (\[rozpočtové náklady\], 'Nákladové účetnictví položky'\[COSTBEHAVIOR\] = 1)                                              |
| Proměnná rozpočtové náklady                          | Výpočet (\[rozpočtové náklady\], 'Nákladové účetnictví položky'\[COSTBEHAVIOR\] = 2)                                              |
| Pevné pružné rozpočtové náklady                    | \[Dlouhodobý rozpočet nákladů\]                                                                                                  |
| Náklady variabilní pružný rozpočet                 | IF (\[velikosti rozpočtu\] = 0, BLANK(), (\[proměnné rozpočtové náklady\] / \[velikosti rozpočtu\]) \*\[skutečná velikost\])       |
| Pružný rozpočet nákladů                          | \[Pevné náklady pružného rozpočtu\] + \[proměnné pružný rozpočet nákladů\]                                                     |
| Rozptyl pružný rozpočet                      | \[Pružný rozpočet nákladů\] - \[skutečné náklady\]                                                                             |
| Procentuální odchylka pružný rozpočet           | IF (\[pružný rozpočet nákladů\] = 0, BLANK(), \[rozptyl pružný rozpočet\] / \[pružný rozpočet nákladů\])                     |
| Pružný rozpočet nákladů sazby                     | IF (\[skutečná velikost\] = 0, BLANK(), \[pružný rozpočet nákladů\] / \[skutečná velikost\])                                 |
| Odchylka rychlosti pružný rozpočet nákladů            | \[Pružný rozpočet nákladová sazba\] - \[Skutečná nákladová sazba.\]                                                                   |
| Procento odchylky nákladů pružný rozpočet | IF (\[pružného rozpočtu nákladová sazba\] = 0, BLANK(), \[odchylka frekvence pružný rozpočet nákladů\] / \[pružného rozpočtu nákladová sazba\]) |

Následující klíče dimenze slouží jako filtry k řezu agregovaných měr dosáhnout větší rozlišovací schopnost a poskytují hlubší analytické poznatky.

| Celek                             | Příklady atributů                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Hlavní knihy nákladového účetnictví            | Hlavní kniha nákladového účetnictví                                                                                               |
| Jednotky řízení nákladů                 | Název jednotky řízení nákladů                                                                                               |
| Dimenze prvku nákladů            | Dimenze Nákladové prvky název, název členu dimenze prvek nákladů, popis člena dimenze prvek nákladů          |
| Dimenze objektu nákladů             | Název dimenze nákladový objekt, název členu dimenze náklady objektu, popis člena dimenze náklady objektu              |
| Statistické dimenze             | Název statistické dimenze, název členu dimenze statistické, popis členu dimenze statistické              |
| Nákladový objekt hierarchie dimenzí  | Název hierarchie dimenze objektu nákladů, nákladů úroveň hierarchie dimenze objekt, stromové hierarchii dimenze objektu náklady    |
| Hierarchie dimenzí nákladové složky | Název hierarchie dimenze prvek nákladů, nákladů úroveň hierarchie dimenze prvek, stromové hierarchii dimenze prvek nákladů |
| Hierarchie dimenzí statistické  | Název hierarchie dimenze statistické, úroveň hierarchie dimenze statistické, stromové struktury hierarchie dimenze statistické    |
| Verze transakce               | Název verze                                                                                                         |
| Fiskální kalendáře                   | Kalendář, Kalendář – popis                                                                                       |
| Fiskální roky                       | Kalendářní rok                                                                                                        |
| Fiskální období                     | Období kalendářního roku                                                                                                 |

## <a name="additional-resources"></a>Další prostředky
Zde uvádíme některé užitečné odkazy související s entitami a vytvářením obsahu v aplikaci Power BI:

-   [Datové entity](..\data-entities\data-entities.md)
-   [Vytvoření organizačního balíčku obsahu](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Modelování dat pomocí aplikace Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Přidání dlaždic Power BI do pracovních prostorů](configure-power-bi-integration.md)
-   [Nastavení zabezpečení obsahu nákladového účetnictví pro Power BI](setup-security-cost-accounting-content-pack.md)



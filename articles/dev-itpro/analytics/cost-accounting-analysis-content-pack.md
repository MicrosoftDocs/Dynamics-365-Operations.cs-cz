---
title: "Obsah analýzy nákladového účetnictví v Power BI"
description: "Toto téma popisuje, co je součástí obsahu analýzy nákladového účetnictví v Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4d2966954ccb9df03227edab1fe7c471ddd20f32
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="cost-accounting-analysis-power-bi-content"></a>Obsah analýzy nákladového účetnictví v Power BI

[!include[banner](../includes/banner.md)]

Toto téma popisuje, co je součástí obsahu **Analýza nákladového účetnictví** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah **Analýza nákladového účetnictví** v Power BI je určen pro kontrolory nákladů nebo jakoukoli osobu, která je odpovědná za provádění kontroly nákladů organizace. Zahrnuje klíčové metriky, jako jsou náklady, velikost a nákladové sazby podle skutečných nákladů, rozpočtových nákladů a nákladů pružného rozpočtu. Používá data transakce z modulu **Nákladové účetnictví** a poskytuje agregované zobrazení nákladů pro celou organizaci v jedné měně vykazování. Manažeři mohou data filtrovat podle objektů nákladů pro provádění kontroly nákladů jejich organizačních jednotek, a to i v případě, že organizace má několik právnických osob. 

Vzhledem k tomu, že obsah **Analýza nákladového účetnictví** zvýrazňuje rozdíly mezi skutečnými náklady a rozpočtovými náklady, mohou být manažeři upozorněni na pozitivní a negativní trendy pro jejich provozní jednotky. Manažeři mohou přejít k podrobnostem hierarchií prvků nákladů nebo jednotlivým prvků nákladů. Tímto způsobem mohou získat manažeři podrobný přehled o tom, jak došlo k odchylce nákladů, a následně provést účinné akce. 

Obsah **Analýza nákladového účetnictví** umožní účetním analyzovat způsoby, jak náklady prochází přes objekty nákladů v celé organizaci. 

Další informace o nákladovém účetnictví naleznete v tématu [Domovská stránka nákladového účetnictví](../../financials/cost-accounting/cost-accounting-home-page.md). 

Definováním zabezpečení na úrovni přístupu v nákladovém účetnictví a jejím zkombinováním se zabezpečením na úrovni řádků v Power BI můžete povolit všem vlastníkům objektů nákladů přístup k obsahu **analýzy nákladového účetnictví** v Power BI. Všechna data ve vizualizaci budou poté vyfiltrována na základě úroveň přístupu, který je řízen v nákladovém účetnictví. Další informace o zabezpečení na úrovni přístupu a zabezpečení na úrovni řádku, naleznete v [Nastavení zabezpečení pro obsah nákladového účetnictví v Power BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Přístup k obsahu Power BI
Obsah **analýzy nákladového účetnictví** v Power BI naleznete v knihovně sdíleného majetku ve službě Microsoft Dynamics Lifecycle Services (LCS). Další informace o stažení obsahu a jeho implementaci ve vaší organizaci naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md). Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.

Nezapomeňte si stáhnout obsah **Analýza nákladového účetnictví**, který se vztahuje k vámi používané verzi aplikace Microsoft Dynamics 365.

> [!NOTE]
> Předpokladem pro obsah Power BI je KB 4011327. Po přihlášení ke službě LCS můžete přejít k článku znalostní báze zde: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
Obsah zahrnuje sadu stránek sestav. Každá stránka obsahuje sadu metrik, které jsou zobrazovány jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizace v obsahu **analýzy nákladového účetnictví** v Power BI.

| Stránka sestavy                      | Graf                                                                                                                         | Dlaždice                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kontrola nákladů podle fiskálního období    | Skutečné náklady a rozpočtové náklady podle úrovně hierarchie prvků nákladů                                                                   | Skutečné náklady vs rozpočtové náklady                    |
|                                  | Odchylka rozpočtu podle úrovně hierarchie prvků nákladů                                                                               | Skutečná nákladová sazba vs rozpočtová nákladová sazba          |
|                                  | Prvních 10 odchylek rozpočtu v procentech podle prvku nákladů                                                                          | Skutečná velikost vs velikost rozpočtu          |
| Kontrola nákladů podle od počátku roku     | Skutečné náklady a rozpočtové náklady podle období kalendářního roku                                                                           | Skutečné náklady vs rozpočtové náklady                    |
|                                  | Odchylka rozpočtu podle období kalendářního roku                                                                                       | Skutečná nákladová sazba vs rozpočtová nákladová sazba          |
|                                  | Prvních 10 odchylek rozpočtu v procentech podle prvku nákladů                                                                          | Skutečná velikost vs velikost rozpočtu          |
| Nákladová sazba podle fiskálního roku         | Skutečná nákladová sazba podle chování nákladů                                                                                             | Skutečná nákladová sazba vs rozpočtová nákladová sazba          |
|                                  | Skutečná nákladová sazba, odchylka rozpočtové nákladové sazby, procento rozpočtové nákladové sazby, rozpočtová nákladová sazba a úroveň hierarchie prvků nákladů | Skutečná velikost vs velikost rozpočtu          |
|                                  | Odchylka rozpočtu podle úrovně hierarchie prvků nákladů                                                                               |                                               |
|                                  | Prvních 10 odchylek rozpočtu v procentech podle prvku nákladů                                                                          |                                               |
| Pružný rozpočet podle fiskálního období | Skutečné náklady, rozpočtové náklady a náklady pružného rozpočtu podle úrovně hierarchie prvků nákladů                                             | Skutečná velikost vs velikost rozpočtu          |
|                                  | Odchylka rozpočtu, odchylka pružného rozpočtu podle úrovně hierarchie prvků nákladů                                                  | Skutečné náklady vs náklady pružného rozpočtu           |
|                                  | Skutečné náklady, rozpočtové náklady a pružné náklady podle chování nákladů a podle úrovně hierarchie prvků nákladů                                  | Skutečná nákladová sazba vs nákladová sazba pružného rozpočtu |
| Výpis nákladů podle fiskálního období  | Skutečné náklady podle úrovně hierarchie prvků nákladů a názvu člena dimenze objektu nákladů                                             |                                               |
|                                  | Skutečné náklady podle názvu člena dimenze objektu nákladů a názvu člena dimenze prvku nákladů                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Informace o datovém modelu a entitách
Následující data se používají k naplnění stránek sestavy v obsahu **Analýza nákladového účetnictví** v Power BI. Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit. Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu. Další informace naleznete v tématu [Přehled integrace Power BI úložištěm entit](power-bi-integration-entity-store.md). 

Následujících klíčové měrné systémy agregace byly použity jako základ obsahu.

| Celek                  | Klíčové měření agregace | Zdroj dat pro Dynamics 365.      | Pole     | popis                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Položky nákladového účetnictví | SUM(Částka)               | CAMDATAAggregatedCostEntry        | Částka    | Částka v měně hlavní knihy nákladového účetnictví. |
| Statistické položky     | SUM(Velikost)            | CAMDATAAggregatedStatisctialEntry | Hodnota |                                                    |

Následující tabulka zobrazuje, jak se používají klíčové měrné systémy agregace k vytvoření několika vypočtených hodnot v souboru dat obsahu.

| Měřítko                                       | Jak vypočítat míru                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Skutečné náklady                                   | CALCULATE('Položky nákladového účetnictví'\[Míra\], 'Verze transakce'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Rozpočtové náklady                                   | CALCULATE('Položky nákladového účetnictví'\[Míra\], 'Verze transakce'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| Odchylka rozpočtových nákladů                          | \[Rozpočtové náklady\] - \[Skutečné náklady\]                                                                                      |
| Procento odchylky rozpočtu                    | IF (\[Rozpočtové náklady\] = 0, blank(), \[Odchylka rozpočtu\] / \[Rozpočtové náklady\])                                                |
| Skutečná velikost                              | CALCULATE('Statistické položky'\[Plná velikost\], 'Verze transakce'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| Velikost rozpočtu                              | CALCULATE(\[Plná velikost\], 'Verze transakce'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)                               |
| Statistická odchylka rozpočtu                   | \[Velikost rozpočtu\] - \[Skutečná velikost\]                                                                            |
| Procento statistické odchylky rozpočtu        | IF (\[Velikost rozpočtu\] = 0, blank(), \[Statistická odchylka rozpočtu\] / \[Velikost rozpočtu\])                          |
| Skutečná nákladová sazba                              | IF (\[Skutečná velikost\] = 0, BLANK(), \[Skutečné náklady\] / \[Skutečná velikost\])                                          |
| Rozpočtová nákladová sazba                              | IF (\[Velikost rozpočtu\] = 0, BLANK(), \[Rozpočtové náklady\] / \[Velikost rozpočtu\])                                          |
| Odchylka rozpočtové nákladové sazby                     | \[Rozpočtová nákladová sazba\] - \[Skutečná nákladová sazba\]                                                                            |
| Procento odchylky rozpočtové nákladové sazby          | IF (\[Rozpočtové náklady\] = 0, blank(), \[Odchylka rozpočtové nákladové sazby\] / \[Rozpočtová nákladová sazba\])                                 |
| Pevné rozpočtové náklady                             | CALCULATE(\[Rozpočtové náklady\], 'Položky nákladového účetnictví'\[COSTBEHAVIOR\] = 1)                                              |
| Variabilní rozpočtové náklady                          | CALCULATE(\[Rozpočtové náklady\], 'Položky nákladového účetnictví'\[COSTBEHAVIOR\] = 2)                                              |
| Pevné náklady pružného rozpočtu                    | \[Pevné rozpočtové náklady\]                                                                                                  |
| Variabilní náklady pružného rozpočtu                 | IF (\[Velikost rozpočtu\] = 0, BLANK(), (\[Variabilní rozpočtové náklady\] / \[Velikost rozpočtu\]) \*\[Skutečná velikost\])       |
| Náklady pružného rozpočtu                          | \[Pevné náklady pružného rozpočtu\] + \[Variabilní náklady pružného rozpočtu\]                                                     |
| Odchylka pružného rozpočtu                      | \[Náklady pružného rozpočtu\] - \[Skutečné náklady\]                                                                             |
| Procento odchylky pružného rozpočtu           | IF (\[Náklady pružného rozpočtu\] = 0, BLANK(), \[Odchylka pružného rozpočtu\] / \[Náklady pružného rozpočtu\])                     |
| Nákladová sazba pružného rozpočtu                     | IF (\[Skutečná velikost\] = 0, BLANK(), \[Náklady pružného rozpočtu\] / \[Skutečná velikost\])                                 |
| Odchylky nákladové sazby pružného rozpočtu            | \[Nákladová sazba pružného rozpočtu\] - \[Skutečná nákladová sazba\]                                                                   |
| Procento odchylky nákladové sazby pružného rozpočtu | IF (\[Nákladová sazba pružného rozpočtu\] = 0, BLANK(), \[Odchylky nákladové sazby pružného rozpočtu\] / \[Nákladová sazba pružného rozpočtu\]) |

Následující klíčové dimenze se používají jako filtry k řezu měrných systémů agregace pro dosažení většího rozlišení a poskytnutí hlubších analytických poznatků.

| Celek                             | Příklady atributů                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Hlavní knihy nákladového účetnictví            | Hlavní kniha nákladového účetnictví                                                                                               |
| Jednotky řízení nákladů                 | Název jednotky řízení nákladů                                                                                               |
| Dimenze prvku nákladů            | Název dimenze prvku nákladů, název člena dimenze prvku nákladů a popis člena dimenze prvku nákladů          |
| Dimenze objektu nákladů             | Název dimenze objektu nákladů, název člena dimenze objektu nákladů a popis člena dimenze objektu nákladů              |
| Statistické dimenze             | Název statistické dimenze, název člena statistické dimenze a popis člena statistické dimenze              |
| Hierarchie dimenze objektu nákladů  | Název hierarchie dimenze objektu nákladů, úroveň hierarchie dimenze objektu nákladů, stromová hierarchie dimenze objektu nákladů    |
| Hierarchie dimenze prvku nákladů | Název hierarchie dimenze prvku nákladů, úroveň hierarchie dimenze prvku nákladů, stromová hierarchie dimenze prvku nákladů |
| Hierarchie statistické dimenze  | Název hierarchie statistické dimenze, úroveň hierarchie statistické dimenze, stromová hierarchie statistické dimenze    |
| Verze transakce               | Název verze                                                                                                         |
| Fiskální kalendáře                   | Kalendář, Popis kalendáře                                                                                       |
| Fiskální roky                       | Kalendářní rok                                                                                                        |
| Fiskální období                     | Kalendářní roční období                                                                                                 |


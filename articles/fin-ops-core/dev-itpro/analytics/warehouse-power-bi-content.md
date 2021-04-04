---
title: Obsah výkonnosti skladu v Power BI
description: Toto téma popisuje, co je součástí obsahu výkonu skladu v Power BI.
author: Mirzaab
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWarehousePerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.region: Global
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 29acf305a275ac9d7047c3aceec726019951654c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563789"
---
# <a name="warehouse-performance-power-bi-content"></a>Obsah výkonnosti skladu v Power BI

[!include [banner](../includes/banner.md)]

Toto téma popisuje, co je součástí obsahu **výkonu skladu** v Microsoft Power BI. Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.

## <a name="overview"></a>Přehled

Obsah **výkonu skladu** v Power BI byl vytvořen tak, aby vedoucí skladu a operací mohli sledovat důležité vstupní, výstupní a skladové metriky. Používá Řízení skladu, produkt a další data transakcí z vašeho systému a poskytuje agregované zobrazení výkonnosti skladu a rozdělení pro dodavatele, produktové skupiny a produkty, stejně jako pracoviště a sklady.

Vedoucí skladu mohou používat obsah **výkonu skladu** v Power BI k měření následujících tří oblastí:

- **Vstupní výkon** – Měří, jak dobře si stojí dodavatel v porovnání s požadavky zákazníka (jinými slovy, měří výkonnosti dodání) a měří výkonnost vyskladnění, abyste mohli identifikovat problémy zahrnující pracovníky nebo zboží za období. Je důležité vědět, zda dodavatelé dodávají včas, předčasně nebo pozdě, abyste mohli určit, jak výkonnost dodavatele ovlivňuje celkový výkonu výdeje. Dodavatel, který dodává mimo odsouhlasené dny, může vytvářet dodatečný tlak na sklad kvůli neočekávané práci a může prodloužit průměrný čas výdeje.
- **Výkon expedice** – Měří, zda váš sklad dodává v plném rozsahu a včas odběratelům (jinými slovy, měří odchozí expedice a výkon dodání), takže můžete identifikovat problémy, které zahrnují produkty, pracoviště nebo sklady, či vyhrazené odběratele. Pokud zjistíte, že do konkrétních oblastí nebo měst dodáváte se zpožděním, můžete věnovat větší pozornost přepravě nebo správě klienta.
- **Přesnost umístění zásob** – Přesnost zásob je důležitá interní skladová business intelligence. Je velmi důležité, abyste stanovili, s jakou přesností obecně provádíte inventuru. Také je však důležité určit, jak přesní jste při skladování zboží na správných místech, a poukázat na nesrovnalosti, abyste mohli najít pro zboží lepší umístění nebo zahájit celkovou inventuru konkrétního zboží. (V současné době nová funkce inventury podle zboží je poskytována jako oprava hotfix.) Používáte-li tento obsah Power BI k určení správnosti údajů množství na skladě podle skladového místa, můžete též určit krádeže ve vašich obchodech. Můžete také určit, zda má nějaké skladové místo na skladě taková množství, která se liší od údajů v systému plánování podnikových zdrojů. Taková skladová místa mohou být příliš velká nebo v nich nelze inventuru provést. Případně některá fyzická umístění mohou být nesprávná, takže je obtížné udržet jeden typ zboží v souladu s daty o zásobách na skladě.

## <a name="accessing-the-power-bi-content-pack"></a>Přístup k balíčku obsahu Power BI
Obsah **Výkon skladu** v Power BI se zobrazuje na stránce **Výkon skladu** (**Řízení skladu** \> **dotazy a sestavy** \> **Analýza výkonu skladu** \> **Výkon skladu**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metriky, které jsou součástí obsahu Power BI
Obsah **Výkonu skladu** v Power BI zahrnuje sestavu. Tato sestava obsahuje sadu metrik, které jsou zobrazovány jako grafy, dlaždice a tabulky. Následující tabulka poskytuje přehled vizualizace v obsahu **Výkon skladu** v Power BI.

| Stránka sestavy                 | Grafy                                   | popis |
|-----------------------------|------------------------------------------|-------------|
| Vstupní výkon         | Celková vyskladnění                          | Počet řádků práce vyskladnění, které jsou zpracovány za dané období. |
| Vstupní výkon         | Průměrná doba vyskladnění                    | Průměrná doba v hodinách pro všechny řádky vyskladnění nákupní objednávky zpracované od registrace zboží až po zpracování posledního vložení. |
| Vstupní výkon         | Dodávka byla přijata dříve.                           | Počet řádků nákupní objednávky, které byly přijaty předčasně. |
| Vstupní výkon         | Dodávka byla přijata včas.                         | Počet řádků nákupní objednávky, které byly přijaty včas. |
| Vstupní výkon         | Zpožděné přijetí                            | Počet řádků nákupní objednávky, které byly přijaty pozdě. |
| Vstupní výkon         | Včas podle dodavatele                        | Zobrazení procenta řádků nákupní objednávky, které jsou přijaté od dodavatele nebo skupiny dodavatelů předčasně, včas nebo pozdě. |
| Vstupní výkon         | Průměrné vyskladnění z překladiště do skladu (v hodinách) | Průměrná doba vyskladnění z překladiště na sklad v hodinách v čase. |
| Vstupní výkon         | Průměrné vyskladnění podle pracovníka               | Průměrná doba v hodinách, kterou pracovníkovi trvalo zpracování vyskladnění řádků nákupní objednávky. |
| Vstupní výkon         | Průměrné vyskladnění podle dodavatele          | Průměrná doba vyskladnění v hodinách podle dodavatele nebo skupiny dodavatelů. |
| Vstupní výkon         | Průměrné vyskladnění podle produktu         | Průměrná doba vyskladnění v hodinách podle zboží nebo skupiny zboží. |
| Přesnost umístění zásob | Celkový počet                              | Počet řádků práce inventury, které jsou zpracovány za dané období. |
| Přesnost umístění zásob | Míra nesrovnalostí                         | Celková míra nesrovnalostí jako procento všech řádků, pro které je provedena inventura za dané období. |
| Přesnost umístění zásob | Počet bez nesrovnalostí                | Počet řádků zpracovaných bez nesrovnalostí z celkového počtu zpracovaných řádků práce inventury. |
| Přesnost umístění zásob | Zboží inventarizované v čase                  | Procento zboží, inventarizované s a bez nesrovnalostí v čase. |
| Přesnost umístění zásob | Nesrovnalosti množství zboží vyšší než % | Zobrazení tabulky řádků inventury, které mají nesrovnalosti překračující určené procento. Tabulka obsahuje informace o umístění, zboží, průměrné nesrovnalosti, celkovém počtu inventarizovaných řádků práce, počtu řádků inventury, které mají nesrovnalosti v umístění, průměrném inventarizovaném množství, očekávaném celkovém inventarizovaném množství a skutečném množství inventarizovaného zboží. |
| Přesnost umístění zásob | Počet položek podle pracovníka                     | Výkonnost zaměstnanců při inventuře. Výkon je vyjádřený jako procento řádků práce inventury, které mají a nemají nesrovnalosti. |
| Přesnost umístění zásob | Počet položek podle pracoviště nebo skladu           | Výkonnost inventury podle počtu zpracovaných řádků práce podle pracoviště nebo skladu, které mají a nemají nesrovnalosti. |
| Přesnost umístění zásob | Míra nesrovnalostí podle produktu              | Míra nesrovnalostí pro výkonnost inventury. Míra je vyjádřená jako procento zpracovaných řádků práce inventury podle zboží nebo skupin zboží. |
| Výkon expedice        | Expedované řádky                            | Celkový počet řádků dodávky, které jsou dodány za dané období. |
| Výkon expedice        | Včasné                                    | Procento předčasně expedovaných řádků dodávky. |
| Výkon expedice        | Včas                                  | Procento včasně expedovaných řádků dodávky. |
| Výkon expedice        | Zpožděné                                     | Procento pozdě expedovaných řádků dodávky. |
| Výkon expedice        | Dodávky v čase                      | Procento řádků dodávky expedovaných včas, předčasně nebo pozdě za dané období. Řádek trendu zobrazí trend pro řádky, které jsou expedovány včas. |
| Výkon expedice        | Zpožděná expedice podle města                     | Vizualizace mapy měst a oblastí, které jsou ovlivněny zpožděnými dodávkami. |
| Výkon expedice        | Expedice podle produktu                       | Procento dodávané předčasně, včas nebo pozdě podle zboží nebo skupiny zboží. |
| Výkon expedice        | Expedováno podle odběratele                      | Procento dodávané předčasně, včas nebo pozdě podle odběratele nebo skupiny odběratelů. |
| Výkon expedice        | Expedováno podle pracoviště nebo skladu              | Procento dodávané předčasně, včas nebo pozdě podle pracoviště nebo skladu. |

## <a name="understanding-the-data-model-and-calculations"></a>Informace o datovém modelu a výpočtech
Následující data se používají k naplnění stránek sestavy v obsahu **Výkonn skladu** v Power BI. Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit. Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu. Další informace naleznete v tématu [Integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).

Následujících klíčové měrné systémy agregace byly použity jako základ obsahu.

| Stránka sestavy                 | Grafy                                   | Tabulky                                | Popisy výpočtů |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Vstupní výkon         | Celková vyskladnění                          | WHSWorkLine                           | Počet řádků práce s typem práce **vložení**. |
| Vstupní výkon         | Průměrná doba vyskladnění                    | WHSWorkLine                           | Součet maximálního času řádků práce dělený počtem maximálního času řádků práce, kde maximální čas řádků práce je maximální mezera mezi datem vytvoření práce a datem uzavření. |
| Vstupní výkon         | Dodávka byla přijata dříve.                           | WHSWorkLine                           | Počet řádků práce, kde datum vytvoření práce je dřívější než použité datum dodání. V případě, že není nastaveno datum potvrzení dodání, použijte výchozí datum dodání. |
| Vstupní výkon         | Dodávka byla přijata včas.                         | WHSWorkLine                           | Počet řádků práce, kde datum vytvoření práce je stejné jako použité datum dodání. V případě, že není nastaveno datum potvrzení dodání, použijte výchozí datum dodání. |
| Vstupní výkon         | Zpožděné přijetí                            | WHSWorkLine                           | Počet řádků práce, kde datum vytvoření práce je pozdější než použité datum dodání. V případě, že není nastaveno datum potvrzení dodání, použijte výchozí datum dodání. |
| Vstupní výkon         | Včas podle dodavatele                        | WHSWorkLine                           | Přijato předčasně, Přijato včas a Přijato pozdě (viz dřívější popis v této tabulce). |
| Vstupní výkon         | Průměrné vyskladnění z překladiště do skladu (v hodinách)   | WHSWorkLine                           | Průměrná doba vyskladnění (viz dřívější popis v této tabulce). |
| Vstupní výkon         | Průměrné vyskladnění podle pracovníka               | WHSWorkLine                           | Průměrná doba vyskladnění (viz dřívější popis v této tabulce). |
| Vstupní výkon         | Průměrné vyskladnění podle dodavatele          | WHSWorkLine                           | Průměrná doba vyskladnění (viz dřívější popis v této tabulce). |
| Vstupní výkon         | Průměrné vyskladnění podle produktu         | WHSWorkLine                           | Průměrná doba vyskladnění (viz dřívější popis v této tabulce). |
| Přesnost umístění zásob | Celkový počet                              | WHSWorkLineCycleCount                 | Cyklické inventury, kde absolutní nesrovnalost množství je rovna nebo větší než 0 (nula). |
| Přesnost umístění zásob | Míra nesrovnalostí                         | WHSWorkLineCycleCount                 | Cyklické inventury s odlišnostmi, rozdělen podle celkového počtu Cyklická inventura má nesrovnalosti tehdy, pokud je absolutní množství nesrovnalosti větší než 0 (nula). |
| Přesnost umístění zásob | Inventura bez nesrovnalostí                | WHSWorkLineCycleCount                 | Cyklické inventury, kde absolutní nesrovnalost množství je větší než 0 (nula). |
| Přesnost umístění zásob | Inventura s nesrovnalostí                   | WHSWorkLineCycleCount                 | Cyklické inventury, kde absolutní nesrovnalost množství je rovna 0 (nula). |
| Přesnost umístění zásob | Zboží inventarizované v čase                  | WHSWorkLineCycleCount                 | Inventura bez nesrovnalosti a inventura s nesrovnalostí s odchylkou (Viz dřívější popis v této tabulce.) |
| Přesnost umístění zásob | Nesrovnalosti množství zboží vyšší než % | WHSWorkLineCycleCount                 | Průměrná nesrovnalost je absolutní množství nesrovnalosti dělené očekávaným množstvím, kde absolutní množství nesrovnalosti je větší něž 0 (nula). Průměrné množství nesrovnalosti je průměrné absolutní množství nesrovnalosti, kde absolutní množství nesrovnalosti je větší něž 0 (nula). Inventura s nesrovnalostí, celková inventura, očekávané množství a inventarizované množství, kde je celé množství seskupeno podle zboží a skladového místa (viz dřívější popis v této tabulce). |
| Přesnost umístění zásob | Počet položek podle pracovníka                     | WHSWorkLineCycleCount                 | Inventura bez nesrovnalosti a inventura s nesrovnalostí s odchylkou (viz dřívější popis v této tabulce). |
| Přesnost umístění zásob | Počet položek podle pracoviště nebo skladu           | WHSWorkLineCycleCount                 | Inventura bez nesrovnalosti a inventura s nesrovnalostí s odchylkou (viz dřívější popis v této tabulce). |
| Přesnost umístění zásob | Míra nesrovnalostí podle produktu              | WHSWorkLineCycleCount                 | Míra nesrovnalostí (viz dřívější popis v této tabulce). |
| Výkon expedice        | Expedované řádky                            | SalesLine               | Počet řádků prodeje, kde jsou řádky prodeje dodány. |
| Výkon expedice        | Včasné                                    | CustPackingSlipOnTimeStatus           | Řádky prodeje se stavem data expedice **1 (předčasná)**. Předčasně znamená, že datum expedice dodacího listu je dřívější než potvrzené datum expedice řádku prodeje. Pokud není potvrzené datum expedice nastaveno, použijte požadované datum expedice. |
| Výkon expedice        | Včas                                  | CustPackingSlipOnTimeStatus           | Řádky prodeje se stavem data expedice **2 (včasná)**. Včas znamená, že datum expedice dodacího listu je stejné jako potvrzené datum expedice řádku prodeje. Pokud není potvrzené datum expedice nastaveno, použijte požadované datum expedice. |
| Výkon expedice        | Zpožděné                                     | CustPackingSlipOnTimeStatus           | Řádky prodeje se stavem data expedice **3 (zpožděná)**. Pozdě znamená, že datum expedice dodacího listu je pozdější než potvrzené datum expedice řádku prodeje. Pokud není potvrzené datum expedice nastaveno, použijte požadované datum expedice. |
| Výkon expedice        | Dodávky v čase                      | SalesLine CustPackingSlipOnTimeStatus | Objednávky, které jsou zcela vyexpedovány, kde je vyexpedováno celé množství řádku prodeje, předčasně, včas a pozdě (Viz dřívější popis v této tabulce.) |
| Výkon expedice        | Zpožděná expedice podle města                     | CustPackingSlipOnTimeStatus           | Pozdě (viz dřívější popisy v této tabulce). |
| Výkon expedice        | Expedice podle produktu                       | CustPackingSlipOnTimeStatus           | Předčasně, Včas a Pozdě (viz dřívější popisy v této tabulce). |
| Výkon expedice        | Expedováno podle odběratele                      | CustPackingSlipOnTimeStatus           | Předčasně, Včas a Pozdě (viz dřívější popisy v této tabulce). |
| Výkon expedice        | Expedováno podle pracoviště nebo skladu              | CustPackingSlipOnTimeStatus           | Předčasně, Včas a Pozdě (viz dřívější popisy v této tabulce). |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
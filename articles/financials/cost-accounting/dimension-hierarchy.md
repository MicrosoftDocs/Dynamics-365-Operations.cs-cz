---
title: "Hierarchie dimenzí"
description: "V tomto tématu jsou informace o hierarchiích dimenzí. Hierarchie dimenzí se používá k definování struktury sestav, zásad nákladů a nastavení zabezpečení v nákladovém účetnictví."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d183654ada9cdca23cf906f250988a967ffcf1f6
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="dimension-hierarchy"></a>Hierarchie dimenzí

[!include[banner](../includes/banner.md)]

V tomto tématu jsou informace o hierarchiích dimenzí. Hierarchie dimenzí se používá k definování struktury sestav, zásad nákladů a nastavení zabezpečení v nákladovém účetnictví.  

## <a name="overview"></a>Přehled

Hierarchie dimenzí se používají na různých místech v nákladovém účetnictví. Hierarchie dimenzí vám umožňuje určit následující informace:

-  Struktura sestav, která vyhovuje požadavkům vaší organizace
-  Zásady nákladů
-  Nastavení zabezpečení

Následuje příklad hierarchie dimenzí.

![Příklad hierarchie dimenzí](./media/dimension-hierarchy.png)

Hierarchii dimenzí lze vytvořit pro následující typy dimenzí:

-  Dimenze prvku nákladů
-  Dimenze objektu nákladů
-  Statistické dimenze

> [!NOTE]
> - Můžete vytvořit několik hierarchií dimenzí pro stejnou dimenzi, pokud je zapotřebí různých perspektiv.
> - Hierarchie dimenzí může být přidružena pouze k jedné dimenzi.
> - Hierarchie dimenzí může mít neomezený počet úrovní ve své struktuře. Všechny úrovně budou dostupné v pracovním prostoru **Řízení nákladů**. Při použití aplikace Microsoft Excel nebo Microsoft Power BI pro účely vykazování je exportováno pouze prvních 15 úrovní hierarchie dimenzí. Toto omezení existuje proto, že aplikace Excel a Power BI vyžadují pevné schéma.
> - Hierarchie dimenzí není platné od data. To znamená, že každá změna hierarchie dimenzí je okamžitě uložena do záznamu a nelze porovnávat datum před a datum po.

## <a name="dimension-hierarchy-type"></a>Typ hierarchie dimenzí

Při vytvoření nové hierarchie dimenzí je nutné zvolit typ hierarchie. Přejděte na **Nákladové účetnictví** > **Dimenze** > **Hierarchie dimenzí**. Klikněte na **Nový** a vyberte typ hierarchie dimenzí. Můžete vybrat buď možnost **Hierarchie kategorizace dimenzí** nebo **Hierarchie klasifikace dimenzí**.

### <a name="dimension-categorization-hierarchy"></a>Hierarchie kategorizace dimenzí

Typ **Hierarchie kategorizace dimenzí** se používá pro účely vykazování. Podporuje pouze dimenze prvku nákladů. Při zvolení tohoto typu platí následující pravidla:

-  Člena dimenze můžete přiřadit více než jednou ve struktuře hierarchie.
-  Člena dimenze prvku nákladů lze zadat do různých uzlů přiřazením chování nákladů k listovému uzlu.

### <a name="dimension-classification-hierarchy"></a>Hierarchie klasifikace dimenzí

Typ **Hierarchie klasifikace dimenzí** se používá k definování pravidel pro účely vykazování. Podporuje všechny dimenze, například objekty nákladů, prvky nákladů a statistické dimenze. Když zvolíte tento typ, můžete člena dimenze přiřadit pouze jednou ve struktuře hierarchie.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Vytvoření a údržba hierarchie dimenzí

Hierarchie dimenzí je vytvořena jako stromové struktura, která má vztahy uzel a uzel listu.

-  Uzel může mít 1:_n_ dílčích uzlů.
-  Uzel nemůže mít k sobě přiřazené současně podřízené uzly a listové uzly.
-  Uzel listu lze přiřadit pouze na nejnižší úroveň v hierarchii.

### <a name="example"></a>Příklad

Malá společnost má následující strukturu organizace, kde finance a lidské zdroje jsou oddělení pod správou a montáž a balení jsou oddělení v rámci výroby.

![Příklad organizační struktury](./media/dimension-hierarchy-org.png)

Dimenze objektu nákladů představuje všechna nákladová střediska v organizaci.

- Dimenze objektu nákladů
    - Nákladová střediska

Dimenze objektu nákladů představující všechna nákladová střediska lze nastavit tak, jak je uvedeno zde.

| Nákladová střediska | popis |
|--------------|-------------|
| CC001        | HR          |
| CC002        | Finance     |
| CC003        | Daň         |
| CC007        | POHLEDÁVKY A ZÁVAZKY       |
| CC005        | Sestavení    |
| CC006        | Balení   |

Dimenze prvku nákladů představuje všechny prvky nákladů v organizaci.

- Dimenze prvku nákladů
    - Prvky nákladů

Dimenze objektu nákladů představující všechna nákladová střediska lze nastavit tak, jak je uvedeno zde.

| Prvky nákladů | popis |
|---------------|-------------|
| 10001         | Elektrické energie |
| 10010         | Úklid    |
| 10011         | Topení     |
| 40001         | COGS        |

Hierarchii dimenzí, která splňuje požadavky organizace na výkazy, lze nastavit tak, jak je uvedeno zde.

**Podrobnosti hierarchie dimenze**

| Název hierarchie dimenze | Dimenze    | Název typu hierarchie dimenze      | Hierarchie přístupového seznamu |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizace             | Nákladová střediska | Hierarchie klasifikace dimenzí | Žádný                    |

Hierarchii dimenzí pro vykazování lze nastavit tak, jak je uvedeno zde.

|                   | Rozsahy členu dimenze   |                         |
|-------------------|---------------------------|-------------------------|
| **Uzly**         | **Od členu dimenze** | **Po člen dimenze** |
| Organizace      |                           |                         |
| &nbsp;&nbsp;Správce         |                           |                         |
|&nbsp;&nbsp;&nbsp;&nbsp;Finance   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | CC001                     | CC001                   |
| &nbsp;&nbsp;Výroba    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Balení | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Sestavení  | CC006                     | CC006                   |

Hierarchii dimenzí, která splňuje požadavky zásad, lze nastavit zde uvedeným způsobem.

**Podrobnosti hierarchie dimenze**

| Název hierarchie dimenze | Dimenze     | Název typu hierarchie dimenze      |
|--------------------------|---------------|------------------------------------|
| Chování nákladů            | Prvky nákladů | Hierarchie klasifikace dimenzí |

Hierarchii dimenzí pro zásady lze nastavit tak, jak je uvedeno zde.

|                   | Rozsahy členu dimenze   |                         |
|-------------------|---------------------------|-------------------------|
| **Uzly**         | **Od členu dimenze** | **Po člen dimenze** |
| Chování nákladů     |                           |                         |
| &nbsp;&nbsp;Pevné náklady    | 10001                     | 10011                   |
|&nbsp;&nbsp;Variabilní náklady | 40001                     | 40010                   |

> [!NOTE]
> Pod možností **Rozsahy členu dimenze** může uzel obsahovat 1:_n_ rozsahů členu dimenze. Můžete vložit ID členů dimenze, která ještě neexistují jako členy dimenze. Tento postup dělá hierarchii odolnou do budoucna.  

### <a name="copy-a-hierarchy"></a>Kopírování hierarchie

Aktuální hierarchii dimenzí můžete kopírovat jako výchozí bod pro novou hierarchii dimenzí. Tento přístup může být užitečný v případě, že chcete porovnat předchozí hierarchii dimenzí s novou hierarchií dimenzí.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Změna uspořádání uzlů v hierarchii

Uzel lze přesunout nahoru nebo dolů v rámci jeho aktuální úrovně ve struktuře. Tímto způsobem můžete změnit uspořádání pořadí uzlů pro vykazování v pracovním prostoru **Řízení nákladů**.

Přesun uzlu do nového umístění v hierarchii provedete volbou cílového uzlu. Existují dva způsoby přesunu uzlu:

- **Přesunout níže** – Přesuňte vybraný uzel z jeho aktuálního umístění v hierarchii a vložte ho **pod** zvolený cílový uzel.
- **Přesunout za** – Přesuňte vybraný uzel z jeho aktuálního umístění v hierarchii a vložte ho **za** zvolený cílový uzel na jeho úrovni hierarchie.

> [!NOTE] 
> Pořadí uzlů není zachováno při exportu dat do aplikace Excel nebo Power BI, protože tyto nástroje používají alfanumerické pořadí řazení jako výchozí. Řazení byste měli změnit ručně.

## <a name="define-dimension-hierarchies-for-reporting"></a>Definování hierarchie dimenzí pro vykazování

Hierarchie dimenzí jsou důležité pro vykazování. Umožňují vám definovat konkrétní strukturu, která vyhovuje jednotlivým organizacím. Agregace uskutečněné na úrovni uzlu hierarchie dimenzí umožňují zúčastněným stranám na kterékoli úrovni organizace prohlížet data na všech úrovních.

Hierarchie dimenzí jsou k dispozici v následujících nástrojích pro vykazování. Tento přístup pomáhá zajistit soulad ve struktuře vykazování.

- Pracovní prostor **Řízení nákladů** (klient):

    - Řízeno konfigurací.

- Pracovní prostor **Řízení nákladů** (mobilní aplikace):

    - Řízeno konfigurací.

- Aplikace Excel

    - Umožňuje vybrat hierarchie dimenzí specifické podle definice exportu:

        - Jedna hierarchie dimenze prvku nákladů (povinná)
        - Jedna hierarchie dimenze objektu nákladů (volitelná)
        - Jedna hierarchie statistické dimenze (volitelná)

- Power BI:

    - K dispozici jsou všechny hierarchie dimenzí.
    
Při vytváření sestav pomocí aplikace Excel nebo Power BI bude exportováno pouze prvních 15 úrovní hierarchií dimenzí. Toto omezení existuje proto, že aplikace Excel a Power BI vyžadují pevné schéma. Má-li hierarchie více než 15 úrovní nebudou další úrovně exportovány. Normalizovaná tabulka obsahuje záznam pro každého člena dimenze v hierarchii. Proto dochází k automatické agregaci. Toto chování pomáhá zajistit, že zůstatky na všech 15 dostupných úrovních v hierarchii jsou stále správné.

Následující příklad ukazuje, jak může hierarchie dimenzí vypadat ve struktuře vykazování.

| Hierarchie dimenze objektu nákladů – Úroveň 1 | Hierarchie dimenze objektu nákladů – Úroveň 2 | Hierarchie dimenze objektu nákladů – Úroveň 3 | Hierarchie dimenze objektu nákladů – Úroveň 4 | Hierarchie dimenze objektu nákladů – Úroveň 15 |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Organizace                              | Správce                                     | Finance                                   | CC002                                     |                                            |
| Organizace                              | Správce                                     | Finance                                   | CC003                                     |                                            |
| Organizace                              | Správce                                     | Finance                                   | CC007                                     |                                            |
| Organizace                              | Správce                                     | HR                                        | CC001                                     |                                            |
| Organizace                              | Výroba                                | Balení                                 | CC005                                     |                                            |
| Organizace                              | Výroba                                | Sestavení                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Aktualizace hierarchií dimenzí, které se používají pro vykazování 

V průběhu času bude třeba aktualizovat hierarchie dimenzí, které se používají ve výše uvedených nástrojích pro vykazování. Hierarchie dimenzí lze aktualizovat obnovením klienta.

- Pracovní prostor **Řízení nákladů** (klient)
- Pracovní prostor **Řízení nákladů** (mobilní aplikace)

Aktualizace hierarchií dimenzí se vyzvedávají každých 24 hodin pomocí úlohy předem uložené do mezipaměti. Po aktualizaci exportovaných dat jsou aktualizované dimenze hierarchií k dispozici v následujících nástrojích:

- Aplikace Excel
- Power BI

> [!NOTE] 
> Chcete-li spustit ručně aktualizaci mezipaměti hierarchií dimenzí, můžete vytvořit nový export do aplikace Excel pro hierarchii dimenzí nebo hierarchie, které je třeba aktualizovat.

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Definování hierarchie dimenzí pro zásady nákladů

Nákladové účetnictví se skládá z několik zásada, kde jsou definována podrobná pravidla. Je nutné definovat jednu nebo více hierarchií dimenzí pro následující zásady:

- Chování nákladů
- Distribuce nákladů
- Přidělení nákladů
- Shrnutí nákladů

Hierarchie dimenzí usnadňují vytváření pravidel. Abyste nemuseli vytvořit pravidla pro jednotlivé členy dimenze, můžete využít agregací členů dimenze, které poskytují úrovně hierarchií dimenzí. Pokud máte překrývající se pravidla, je nutné definovat konkrétní pravidla, která systém zváží při provádění výpočtu režijních nákladů.

### <a name="example-define-a-cost-behavior-policy"></a>Příklad: Definování zásad chování nákladů

Vytvoření nové zásady chování nákladové a hierarchie dimenzí odpovídající přiřazenou zásady, jak je uvedeno v tomto poli.

**Zásady chování nákladů**

| Název zásady   | Hierarchie dimenze prvku nákladů | Hierarchie dimenze objektu nákladů | Zúčtovací měna |
|---------------|----------------------------------|---------------------------------|---------------------|
| Chování nákladů | Chování nákladů                    | Organizace                    | USD                 |

**Pravidla**

| Uzel hierarchie dimenze prvku nákladů | Uzel hierarchie dimenze objektu nákladů | Pevné procento | Pevná částka | Platné od | Platné do |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Pevné náklady                            | Organizace                         | 100,00           | 0,00         | 1. 1. 2017   | Nikdy    |
| 10001                                 | Organizace                         | 0,00             | 150,00       | 1. 1. 2017   | Nikdy    |
| 10001 (\*)                             | Finance                              |                  | 50,00        | 1. 1. 2017   | Nikdy    |
| Chování nákladů nebo variabilní náklady (\*\*)   | Organizace                         | 0,00             | 0,00         | 1. 1. 2017   | Nikdy    |

\* Není požadován uzel variabilních nákladů. Pokud nejsou náklady klasifikovány jako pevné náklady, musí se jednat o variabilní náklady.

\*\* Podrobné pravidlo je vytvořeno pro kombinaci člena prvku nákladů 10001 a všechny členy objektu nákladů agregované pod úrovní hierarchie Finance(CC002 CC003, CC007).

Předchozí pravidla zobrazují flexibilitu, kterou hierarchie dimenzí poskytují. Definováním pravidel vysoké úrovně pomáháte minimalizovat údržbu. Poté lze definovat pravidla tak, aby vyhovovala konkrétnímu obchodnímu cíli.

Když se hierarchie dimenzí, které se používají v pravidlech, aktualizují, systém automaticky posune aktualizace dopředu.

Pokud není úroveň rozlišení v pravidlech již nadále požadováno, můžete platnost pravidla vypršet.

Například konkrétní pravidlo chování nákladů pro uzel hierarchie dimenzí objektu nákladů Finance již není nadále požadováno. V tomto případě klikněte na tlačítko **Vypršení platnosti pravidla** a platnost pravidla skončí.

| Uzel hierarchie dimenze prvku nákladů | Uzel hierarchie dimenze objektu nákladů | Pevné procento | Pevná částka | Platné od | Platné do  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Pevné náklady                            | Organizace                         | 100,00           | 0,00         | 1. 1. 2017   | Nikdy     |
| 10001                                 | Organizace                         | 0,00             | 150,00       | 1. 1. 2017   | Nikdy     |
| 10001                                 | Finance                              |                  | 50,00        | 1. 1. 2017   | 20. 1. 2017 |
| Chování nákladů nebo variabilní náklady        | Organizace                         | 0,00             | 0,00         | 1. 1. 2017   | Nikdy     |

Všechny výpočty režijních nákladů spuštěné po 20. lednu 2017 již toto pravidlo neberou v úvahu.

> [!NOTE] 
> Pole **Platné od** a **platné do** platí od data a času. Můžete nechat vypršet platnost pravidla a ve stejný den spustit nový výpočet režijních nákladů.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Definování hierarchie dimenzí pro nastavení zabezpečení

Data nákladového účetnictví by měla být k dispozici pro všechny vedoucí pracovníky, kteří odpovídají za jednotku výkaznictví. V terminologii nákladového účetnictví představuje jednotka výkaznictví objektu nákladů nebo sadu objektů nákladů.

Všichni manažeři budou potenciálně mít přístup k vysoce citlivým obchodním datům, jako jsou výnosy a marže. Proto je důležité nastavit zabezpečení, aby vedoucí pracovníci mohli vidět pouze data, která jsou pro ně relevantní. K usnadnění kontroly zabezpečení dat definujete hierarchie dimenzí.

- Použití hierarchie dimenzí platí pouze v případě, když je hodnota dimenze, která je vybrána v odkazu hierarchie dimenzí, dimenzí objektu nákladů.
- Pro dimenzi objektu nákladů v hierarchii seznamu přístupu lze povolit pouze jednu dimenzi hierarchie.

**Podrobnosti hierarchie dimenze**

| Název hierarchie dimenze | Dimenze    | Název typu hierarchie dimenze      | Hierarchie přístupového seznamu |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizace             | Nákladová střediska | Hierarchie klasifikace dimenzí | **Ano**               |

V návrháři hierarchie je k dispozici nová pevná záložka **Uživatelé**. Zde můžete vložit jedno nebo více ID uživatelů na každém uzlu v hierarchii.

|                 | Uživatelé            | Rozsahy členu dimenze   |                         |
|-----------------|------------------|---------------------------|-------------------------|
| **Uzly**       | **ID uživatele**      | **Od členu dimenze** | **Po člen dimenze** |
| Organizace    | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Správce         | Duben            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finance   | Alicia           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Výroba    | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Balení | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Sestavení  | Chris            | CC006                     | CC006                   |

> [!NOTE] 
> Nákladoví účetní musí být přiřazeni do hierarchie nejvyšší úrovně, aby mohli nahlížet do všech položek nákladového účetnictví.

Chcete-li povolit hierarchii seznamu přístupu a jeho nastavení zabezpečení, přejděte na **Nákladové účetnictví** > **Nastavení** > **Parametry** > **Obecné**. Zvolte parametr **Povolit přístup k zobrazení pro členy dimenze objektu nákladů**.

Nastavení pro hierarchii seznamu přístupu se používají ke kontrole dat, zobrazených v následujících oblastech:

- Pracovní prostor **Řízení nákladů** (klient):

    - Data ve formulářích, které se používají k procházení podrobností scénáře

- Pracovní prostor **Řízení nákladů** (mobilní aplikace):

    - Zůstatky na kartách

- Power BI:

    - Data zobrazená ve vizualizacích Power BI
    - Vizualizace dat Power BI, vložená do aplikace Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, klient

> [!NOTE] 
> - Než může hierarchie přístupového seznamu ovlivnit data v Power BI, musí být spárována hierarchie přístupového seznamu a zabezpečení na úrovni řádku v Power BI. Další informace naleznete v tématu [Nastavení zabezpečení pro balíček obsahu nákladového účetnictví](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Hierarchie seznamu přístupu nepomáhá zabezpečit export dat do aplikace Excel. Z toho vyplývá, že nástroj pro vytváření sestav by měl být použit pouze nákladovými účetními a vedoucími pracovníky, kteří mají úplný přístup k zobrazení dat.


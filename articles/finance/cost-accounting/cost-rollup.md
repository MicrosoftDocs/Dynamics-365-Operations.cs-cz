---
title: Zásady shrnutí nákladů a výpočet režijních nákladů
description: Tento článek obsahuje informace o tom, jak určit správnou úroveň sekundárních prvků nákladů a vytvořit pravidla shrnutí nákladů, které spadají do výkaznictví organizace a sledovatelnosti nákladů.
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy, CAMOverheadRatePolicy
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f35bf3e900b8dd9c1864be8668f7ff7296924c4d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874602"
---
# <a name="cost-rollup-policy-and-overhead-calculation"></a>Zásady shrnutí nákladů a výpočet režijních nákladů 

[!include [banner](../includes/banner.md)]

Nákladové účetnictví vám umožní získat přehled o vztahu toku nákladů k produktům a službám, které jsou dodávány v rámci organizace. Pro zobrazení transparentních nákladů je velmi důležité dosáhnout přidělení nákladů mezi objekty nákladů na základě příslušného základu přidělení. Ve výchozím nastavení je dosaženo přidělení nákladů pro primární prvek nákladů, který je v některých situacích vyžadován, ale je zde několik důsledků, které je třeba zvážit.

-   Pomocné objekty nákladů budou končit s nulovým zůstatkem pro primární prvek nákladů po výpočtu režijních nákladů.
-   Objem položek nákladů vygenerovaný při výpočtu režijních nákladů může být velmi vysoký.
-   Není možné sledovat tok nákladů mezi objekty nákladů.

Abyste zabránili těmto důsledkům, nákladové účetnictví vám umožní nakonfigurovat přidělení nákladů tak, aby vyhovovalo manažerským požadavkům na vykazování ve vaší organizaci. Tento článek se zabývá tím, jak určit správnou úroveň sekundárních prvků nákladů a vytvořit pravidla shrnutí nákladů, které spadají do výkaznictví organizace a sledovatelnosti nákladů.

> [!NOTE]
> Konfigurace můžete měnit, pokud se požadavky na vykazování změní.

## <a name="example-of-cost-rollup-policy-setup"></a>Příklad nastavení zásad shrnutí nákladů

Představte si, že organizace má následující strukturu se čtyřmi nákladovými středisky.

![Příklad organizační struktury.](./media/dimension-hierarchy-org.png)

**Dimenze objektu nákladů**

| Nákladová střediska | popis          |
|--------------|-----------|
| CC001        | HR        |
| CC002        | Finance   |
| CC003        | Sestavení  |
| CC004        | Balení |

**Dimenze prvku nákladů**

| Prvky nákladů | popis | Typ    |
|---------------|-------------|---------|
| 1 001          | Elektrické energie | Primární |
| 1 002          | Platy    | Primární |
| 1003          | Reklama | Primární |

Hierarchii dimenzí, která splňuje požadavky organizace na výkazy, lze nastavit následujícím způsobem.

**Podrobnosti hierarchie dimenze**

| Název hierarchie dimenze | Dimenze    | Název typu hierarchie dimenze      | Hierarchie přístupového seznamu |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizace             | Nákladová střediska | Hierarchie klasifikace dimenzí | Ne                    |

**Hierarchie dimenzí**

|    &nbsp;    | Rozsahy členu dimenze | &nbsp;              |
|--------------|-------------------------|---------------------|
| **Uzly**        | **Od členu dimenze**   | **Po člen dimenze** |
| Organizace |                         |                     |
| &nbsp;&nbsp;Správce             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Finance              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;HR               | CC002                   | CC002               |
| &nbsp;&nbsp;Výroba               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Balení              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Sestavení             | CC004                   | CC004               |

Hierarchii dimenzí, která splňuje požadavky zásad, lze nastavit následujícím způsobem.

**Podrobnosti hierarchie dimenze**

| Název hierarchie dimenze | Dimenze     | Název typu hierarchie dimenze      |
|--------------------------|---------------|------------------------------------|
| Výkaz zisků a ztrát  | Prvky nákladů | Hierarchie klasifikace dimenzí |

**Hierarchie dimenzí**

|      &nbsp;             | Rozsahy členu dimenze |      &nbsp;         |
|-------------------------|-------------------------|---------------------|
| Uzly                   | Od členu dimenze   | Po člen dimenze |
| Výkaz zisků a ztrát |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Primární náklady                    | 10001                   | 10003               |

Po zpracování položky hlavní knihy vypadá položka zůstatku nákladů podle objektu nákladů takto.

|      &nbsp;          | **Objekt nákladů** | &nbsp;    |  &nbsp;   |  &nbsp;   | **Celkem**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **Prvek nákladů**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 Elektřina** | 100,00          | 200,00    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 Platy**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 Reklama** | 0,00            | 4.000,00  | 0,00      | 0,00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**Statistická dimenze**

| Statistické prvky |    popis   |
|----------------------|------------------|
| SE-1                 | Služby HR      |
| SE-2                 | Finanční služby |

Objekt nákladů CC001 HR přispívá k několika objektům nákladů.

HR služby jsou spotřebovávány následující distribucí velikosti.

| Objekt nákladů | popis |   Služby HR |
|-------------|-------------|----|
| CC002       | Finance     | 35 |
| CC003       | Sestavení    | 55 |
| CC004       | Balení   | 10 |

Objekt nákladů CC002 Finance přispívá k několika objektům nákladů.

Finanční služby jsou spotřebovávány následující distribucí velikosti.

| Objekt nákladů |   popis    |  Finanční služby   |
|-------------|------------------|----|
| CC003       | Sestavení         | 65 |
| CC004       | Balení        | 35 |

Zásady přidělení nákladů můžete nastavit následujícím způsobem.

| Název zásady | popis     | Hierarchie dimenze objektu nákladů | Statistická dimenze | Dimenze prvku nákladů |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | Přidělení nákladů | Organizace                    | Statistické prvky  | Prvky nákladů          |

Pravidla přidělení nákladů můžete nastavit následujícím způsobem.

| Uzel hierarchie dimenze objektu nákladů | Chování nákladů | Základ přidělení        |
|--------------------------------------|---------------|------------------------|
| CC001                                | Celkem         | **Služby HR**        |
| CC002                                | Celkem         | **Finanční služby** |

## <a name="brhow-cost-flows-between-cost-centers"></a><br>Tok nákladů mezi nákladovými středisky 

Pokud chcete zjistit, jaký je tok nákladů mezi nákladovými středisky v organizaci, můžete vytvořit prvky nákladů typu **Sekundární** pro každé nákladové středisko. Tyto prvky nákladů budou poté použity k přenosu zůstatků mezi nákladovými středisky během výpočtu režijních nákladů.

Členy dimenze prvku nákladů můžete nastavit následujícím způsobem.

| Prvky nákladů | Typ          |     &nbsp;    |
|---------------|---------------|---------------|
| 1 001          | Elektrické energie   | Primární       |
| 1 002          | Platy      | Primární       |
| 1003          | Reklama   | Primární       |
| **SC-CC001**  | **HR**        | **Sekundární** |
| **SC-CC002**  | **Finance**   | **Sekundární** |
| **SC-CC003**  | **Sestavení**  | **Sekundární** |
| **SC-CC004**  | **Balení** | **Sekundární** |

Hierarchie dimenzí **Výkaz zisků a ztrát** musí být aktualizována novými členy dimenze, aby hierarchie dimenzí obsahovala správná data, která lze použít k definování sestav a zásad.

**Podrobnosti hierarchie dimenze**

| Název hierarchie dimenze | Dimenze     | Název typu hierarchie dimenze      |
|--------------------------|---------------|------------------------------------|
| Výkaz zisků a ztrát  | Prvky nákladů | Hierarchie klasifikace dimenzí |

**Hierarchie dimenzí**

|      &nbsp;             | Rozsahy členu dimenze |  &nbsp;             |
|-------------------------|-------------------------|---------------------|
| Uzly                   | Od členu dimenze   | Po člen dimenze |
| Výkaz zisků a ztrát |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Primární náklady                        | 10001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Sekundární náklady                         | **SC-CC001**            | **SC-CC004**        |

Vytvořte **Zásady shrnutí nákladů**, kde je každé nákladové středisko je namapováno na odpovídající prvek nákladů typu **Sekundární**.

**Zásady shrnutí nákladů**

| Název zásady | popis | Hierarchie dimenze objektu nákladů | Hierarchie dimenze prvku nákladů |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | Tok nákladů   | Organizace                    | Výkaz zisků a ztrát          |

**Pravidla shrnutí nákladů**

| Uzel hierarchie dimenze objektu nákladů | Uzel hierarchie dimenze prvku nákladů | Prvek druhotných nákladů |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | Výkaz zisků a ztrát               | **SC-CC001**           |
| CC002                                | Výkaz zisků a ztrát               | **SC-CC002**           |
| CC003                                | Výkaz zisků a ztrát               | **SC-CC003**           |
| CC004                                | Výkaz zisků a ztrát               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>Provedení výpočtu režijních nákladů

**Deník**

| Deník | Typ deníku            | Fiskální kalendářní období | Rok | Období | Verze       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | Deník přidělení nákladů | Fiskální                 | 2017    | Období 1 | Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1 |

Systém nyní použije **Zásady shrnutí nákladů** při vytváření **položek deníku pro zůstatek objektu nákladů**.

**Položky deníku pro zůstatek objektu nákladů**

| Datum účtování | Objekt nákladů | popis  | Prvek nákladů | popis |  Částka |
|-----------------|-------------|--------------|----------|-----------|-----------|
| 31. 01. 2017      | CC001       | HR           | SC-CC001 | HR        | 10.100,00 |
| 31. 01. 2017      | CC002       | Finance      | SC-CC002 | Finance   | 17.735,00 |
| 31. 01. 2017      | CC003       | Sestavení     | SC-CC003 | Sestavení  | 31.082,75 |
| 31. 01. 2017      | CC004       | Balení    | SC-CC004 | Balení | 15.717,25 |

> [!NOTE]
> Položky deníku jsou vytvořeny na základě pravidel v možnosti **Zásady shrnutí nákladů**, pokud zásady existují. Zobrazený zůstatek je zůstatek výpočtu režijních nákladů.

Stránka **Podrobnosti položky deníku zůstatku nákladů objektu nákladů**, ke které je přístup z položek deníku, zobrazuje, jakým způsobem se získá zůstatek.

**Příklad: Položka deníku pro objekt nákladů CC002 Finance**

**Podrobnosti položky deníku zůstatku nákladů objektu nákladů**

| Člen dimenze prvku nákladů | popis |  Částka   |
|-------------------------------|-------------|-----------|
| 1 001                          | Elektrické energie | 200,00    |
| 1 002                          | Platy    | 10.000,00 |
| 1003                          | Reklama | 4.000,00  |
| SC-CC001                      | HR          | 3.535,00  |

**Položky nákladů generované výpočtem režijních nákladů**

| Objekt nákladů | popis  | Prvek nákladů   | popis  |        Částka     |       Datum účtování     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | HR           | SC-CC001 | HR              | 10.100,00. \- | 31. 01. 2017 |
| CC002       | Finance      | SC-CC001 | HR              | 3.535,00    | 31. 01. 2017 |
| CC003       | Sestavení     | SC-CC001 | HR              | 5.555,00    | 31. 01. 2017 |
| CC004       | Balení    | SC-CC001 | HR              | 1.010,00    | 31. 01. 2017 |
| CC002       | Finance      | SC-CC002 | Finance         | 17.735,00. \- | 31. 01. 2017 |
| CC003       | Sestavení     | SC-CC002 | Finance         | 11.527,75   | 31. 01. 2017 |
| CC004       | Balení    | SC-CC002 | Finance         | 6.207,25    | 31. 01. 2017 |

Po dokončení **výpočtu režijních nákladů** můžete vykázat výsledky pomocí nástrojů, jako je například Microsoft SharePoint Workspace, aplikace Excel nebo Power BI.

## <a name="view-reporting-in-excel"></a>Zobrazení vykazování v aplikaci Excel 

Hierarchie dimenzí umožňuje zobrazit data v různých úrovních agregace.

Následuje příklad výkazu Power Pivot v aplikaci Excel.

| **Výkaz zisků a ztrát** | **Objekt nákladů** |      &nbsp;    |   &nbsp;      |     &nbsp;    |  **Celkem**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **Primární náklady**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| 1001. &nbsp;&nbsp;&nbsp;&nbsp;                            | 100,00          | 200,00         | 6.000,00      | 2.000,00      | **8.300,00**  |
| 1002. &nbsp;&nbsp;&nbsp;&nbsp;                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|1003. &nbsp;&nbsp;&nbsp;&nbsp;                             | 0,00            | 4.000,00       | 0,00          | 0,00          | **4.000,00**  |
|**Sekundární náklady**                            | **-10.100,00**  | **-14.200,00** | **17,082,75** | **7.217,25**  | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | 10.100,00. \-     | 3.535,00       | 5.555,00      | 1.010,00      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0,00            | 17.735,00. \-    | 11.527,75     | 6.207,25      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
| **Celkem**                   | **0,00**        | **0,00**       | **31.082,75** | **15.717,25** | **46.800,00** |

Pomocí **zásad shrnutí nákladů** a **prvků nákladů sekundárního typ** můžete ponechat primární náklady na objektu nákladů pro interní sestavy jako primární náklady, které zbývají po **výpočtu režijních nákladů**.

Pokud byste provedli stejný příklad bez vytvoření **zásad shrnutí nákladů**, výsledek vykazování by byl takový, jak je zobrazeno níže. Tok nákladů je správný, ale sledovatelnost a vhled do toku nákladů mezi nákladovými středisky se ztratí.

| **Výkaz zisků a ztrát** | **Objekt nákladů** |   &nbsp;  |    &nbsp;     |  &nbsp;       |          **Celkem**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **Primární náklady**            | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|1001. &nbsp;&nbsp;&nbsp;&nbsp;                              | 0,00            | 0,00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| 1002. &nbsp;&nbsp;&nbsp;&nbsp;                             | 0,00            | 0,00      | 22.275,00     | 12.225,00     | **34.500,00** |
|1003. &nbsp;&nbsp;&nbsp;&nbsp;                              | 0,00            | 0,00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**Sekundární náklady**                            | **0,00**        | **0,00**  | **0,00**      | **0,00**      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC001                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC002                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC003                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp; SC-CC004                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
| **Celkem**                   | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |

V závislosti na vykazování a sledovatelnosti požadavků ve vaší organizaci můžete určit správnou úroveň sekundárních prvků nákladů a vytvořit pravidla shrnutí nákladů, která budou vyhovovat vašim potřebám.

Smazání oddělení mezi **přidělením nákladů** a **zásadami shrnutí nákladů** poskytuje možnost provádět souvislé aktualizace, aniž by jedna ovlivňovala druhou.



## <a name="additional-resources"></a>Další zdroje
-  [Dimenze objektu nákladů](cost-objects.md)
-  [Dimenze prvku nákladů](cost-elements.md)
-  [Hierarchie dimenzí](dimension-hierarchy.md)
-  [Výpočet režijních nákladů](overhead-calculation.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

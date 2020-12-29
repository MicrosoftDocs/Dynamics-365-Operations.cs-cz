---
title: Položky nákladů
description: Tento článek obsahuje informace o položkách nákladů a o tom, kdy se vytváří. Položka nákladů je záznam, který registruje množství a náklady na danou událost.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3116f9fd2d1fe6a0967b114a069f495cea6217a1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423480"
---
# <a name="cost-entries"></a>Položky nákladů

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o položkách nákladů a o tom, kdy se vytváří. Položka nákladů je záznam, který registruje množství a náklady na danou událost.

Položky nákladů jsou seskupení skladových transakcí, které jsou zaznamenány v aktivních dimenzích finančních zásob.

## <a name="examples"></a>Příklad
### <a name="example-1-no-cost-entries-are-created"></a>Příklad 1: Nejsou vytvořeny žádné položky nákladů

Je registrována událost deníku převodů. Událost převede jeden kus zboží A z místa A do místa B. Dimenze zásob skladového místa není považována za součást objektu nákladů. Událost tedy vytvoří dvě skladové transakce a žádné položky nákladů.

### <a name="example-2-cost-entries-are-created"></a>Příklad 2: Jsou vytvořeny položky nákladů

Je registrována událost deníku převodů. Událost převede jeden kus zboží A z pracoviště 1 na pracoviště 2. Dimenze zásob pracoviště je považována za součást objektu nákladů. Událost tedy vytvoří dvě skladové transakce a dvě položky nákladů.

### <a name="example-3-one-cost-entry-is-created"></a>Příklad 3: Je vytvořena jedna položka nákladů

Událost příjemky produktu je registrována pro nákupní objednávku. Událost registruje 100 kusů položky A za pořizovací cena 10,00 amerických dolarů (USD). Vzhledem k tomu, že položka A používá pro sledování účel řízení zásob sériové číslo, bude pro každou přijatou položku vytvořeno jedinečné sériové číslo. Událost tedy vytvoří 100 skladových transakcí a jednu položku nákladů.

## <a name="cost-entries-page"></a>Stránka Položky nákladů
Nová stránka **Položky nákladů** umožňuje zobrazit a kontrolovat registrace množství a nákladů. Tato stránka doplňuje stránky **Skladová transakce** a **Vyrovnání zásob**. Záznamy jsou registrovány v chronologickém pořadí pro událost. Lze tedy rychle vyhledat a zkontrolovat akumulované náklady na určitou událost nebo všechny události, které se vztahují k dokumentu. Zde je příklad:

-   Události příjemky produktu je registrována pro zboží A. Sto kusů je přijato za pořizovací cenu 10,00 USD.
-   Několik dní po registraci události faktury se náklady zvýší na 11,00 USD. Celková částka je tedy 1 100 USD. Je vytvořen druhý doklad na rozdíl 100 USD.
-   O několik dní později jsou v nákupní objednávce registrovány vedlejší náklady ve výši 15,00 USD k pokrytí nákladů na přepravu.

| Doklad | Datum       | Odkaz      | Počet | ID šarže  | Množství | Částka  |
|---------|------------|----------------|--------|---------|---------------|----|
| 00001   | 01. 01. 2015 | Nákupní objednávka | 100001 | 0000101 | 100,00   | 1000,00 |
| 00002   | 20. 01. 2015 | Nákupní objednávka | 100001 | 0000101 |          | 100,00  |
| 00003   | 31. 01. 2015 | Úprava     | 100001 | 0000101 |          | 15:00   |

Stránka **Položky nákladů** umožňuje filtrovat podle ID doklad a data dokladu. 

> [!NOTE]
> Položky nákladů jsou k dispozici pouze pro [objekty nákladů](cost-object.md) nebo uvolněné produkty.

<a name="additional-resources"></a>Další zdroje
--------

[Nákladové objekty](cost-object.md)




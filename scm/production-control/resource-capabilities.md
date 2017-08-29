---
title: "Schopnosti prostředku"
description: "V tomto článku jsou informace o možnostech prostředků. Schopnost je možnost provozních prostředků provádět určitou aktivitu. Článek vysvětluje způsob použití možností a souvisejících koncepcí, například úrovní znalosti a priority, k volbě vhodných prostředků pro aktivitu."
author: sorenva
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f6b4ccf4d7f9727819831b07221d859e3c5cdd39
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017

---

# <a name="resource-capabilities"></a>Schopnosti prostředku

[!include[banner](../includes/banner.md)]


V tomto článku jsou informace o možnostech prostředků. Schopnost je možnost provozních prostředků provádět určitou aktivitu. Článek vysvětluje způsob použití možností a souvisejících koncepcí, například úrovní znalosti a priority, k volbě vhodných prostředků pro aktivitu.

Schopnost je možnost provozních prostředků provádět určitou aktivitu. Prostředek operace může mít více než jednu možnost přiřazení a možnost může být přiřazen více zdrojům. Chcete-li dočasně přiřadit schopnosti k provozním prostředkům, určete počáteční datum a datum vypršení platnosti při přiřazování schopnosti. Po uplynutí schopnosti prostředku prostředek nelze naplánovat pro projekt nebo výrobu, které vyžadují tuto možnost. Schopnost, která vypršela, lze obnovit. Možnosti můžete odstranit za předpokladu, že nejsou v relaci postupu nebo v rámci výrobního postupu aktivní výrobní objednávky. Obecně platí při odstranění možností postupovat opatrně. Místo toho zvažte úpravu data vypršení platnosti pro zdroje, které mají tuto možnost. Schopnosti lze přiřadit ke všem typům prostředků: nástroj, dodavatel, stroj, umístění, zařízení nebo lidské zdroje.

## <a name="level"></a>Úroveň
Více zdrojů často má stejnou schopnost funkce, avšak na různých úrovních způsobilosti (například síla, rychlost zpracování a přesnost). Z toho vyplývá, přiřadíte-li schopnost k prostředku, můžete určit hodnotu **úrovně**. Úroveň je jednoduchá číselná hodnota. Pokud zadáte, že na schopnost je požadavek na zdroj pro výrobní postup, je také možné určit **minimální potřebnou úroveň** hodnoty této možnosti. Modul plánování potom vybere pouze prostředky, které mají požadované možnosti na úrovni, která se rovná nebo je větší než minimální úroveň zadaná v požadavku na zdroj.

## <a name="priority"></a>Priorita
Provozní prostředky, které mají stejné možnosti, mohou přiřadit prioritu. Potom, pokud má více zdrojů schopnosti, které splňují požadavky na plánování na požadované úrovni a mají volnou kapacitu, plánovací modul můžete volit mezi těmito prostředky. Pokud je vybraná **Priorita** v poli **Výběr primárního prostředku** na stránce **Parametry plánování**, prostředek, který má nejvyšší prioritu (nejnižší číselnou hodnotu v poli **Priorita**), je vybrán během plánování jako první.

## <a name="resource-requirements"></a>Požadavky na prostředek
Při definování požadavků na prostředek pro výrobní postup, můžete jako požadavky určit jednu nebo více možností. Při plánování výroby, možnosti, které jsou definovány v požadavcích na zdroje v operaci postupu jsou pak párovány s možnostmi, které jsou definovány pro zdroje. Jsou vybrány zdroje, které mají možnosti, které odpovídají požadavkům. Má-li více zdrojů stejnou funkční schopnost, ale různé dovednosti (například síla, rychlost zpracování a přesnost), můžete buď definovat více možností, nebo použít úroveň schopností pro kvalifikaci schopnosti prostředku. Zde je příklad:

-   Podle postupu je čas procesu vrtání nastaven na 10 jednotek za hodinu, ale samotný požadavek je definován jako Vrtání.
-   Máte dvě vrtačky, M1 a M2.
-   Schopnost vrtání je přiřazena oběma prostředkům, vrtačce M1 i M2.
-   Vrtačka M1, může vyvrtat dvě jednotky za hodinu a vrtačka M2, může vyvrtat 11 jednotek za hodinu.

V tomto příkladu obě vrtačky mohou být vybrány modulem plánování, protože obě splňují požadavek na základní schopnost (Vrtání). Nicméně vrtačka M1 může vyvrtat pouze dvě jednotky za hodinu. Vzhledem k tomu, že toto číslo je mnohem menší než 10 jednotek za hodinu, které jsou zadány v postupu, při výběru způsobí vrtačka M1 potíže ve výrobě. Dvěma způsoby můžete vyřešit tento problém a ujistit se, že bude vybrána vrtačka M2:

-   Vytvořte dvě samostatné funkce: pomalé vrtání a vrtání na vyšší rychlost. Definujte pomalé vrtání, jako vrtání, které má čas zpracování jednu až devět jednotek za hodinu. Definujte vrtání na vyšší rychlost jako vrtání, které má čas vrtání 10 až 19 jednotek za hodinu. Potom přiřaďte stroji M1 schopnost vrtání nízkou rychlostí a stroji M2 schopnost vrtání vysokou rychlostí. Nakonec změňte požadavek na schopnost prostředku na trase na vysokorychlostní vrtání. Plánovací modul poté vybere správnou vrtačku (M2).
-   Používejte úroveň schopností pro kvalifikaci možnosti vrtání, která je přiřazená k vrtačce. Určete, že stroj M1 má schopnost vrtání na úrovni 2.0 a M2 má schopnost vrtání na úrovni 11.0. Potom zadejte, že 10.0 je minimální úroveň, která je vyžadována pro požadavek na schopnost vrtání na trase. Plánovací modul poté určí, že pouze vrtačka M2 splňuje požadavky na prostředek.

## <a name="competencies-for-human-resources"></a>Kompetence pro lidské zdroje
Když máte provozní prostředky typu **lidské zdroje**, které jsou přiřazeny k zaměstnancům v lidských zdrojích, můžete také využít kompetencí pracovníků při definování požadavků na prostředky ve výrobním postupu. Jinak řečeno můžete také nastavit také požadavky pro konkrétní dovednosti, kurzy, certifikáty nebo tituly. Modul plánování zdrojů může poté vybrat, které prostředky jsou přiřazeny zaměstnancům a výběr bude založen na kompetencích těchto zaměstnanců. Kompetence jsou nastaveny v lidských zdrojích, ne na stránce **Schopnosti prostředku**. Při definování dovedností, kurzů, certifikátů nebo titulů jako požadavků na prostředek musíte použít funkci modulu lidské zdroje a spojit každý prostředek typu **lidských zdrojů** s odpovídajícím pracovníkem. Pokud nepoužíváte funkce lidských zdrojů, je možné určit schopnosti na stránce **Schopnosti prostředku**, která se podobá nebo duplikuje kompetence z lidských zdrojů. Avšak stránka **Schopnosti prostředku** neobsahuje funkce, které jsou potřebné za účelem úprav dovedností, kurzů, certifikátů nebo titulů.





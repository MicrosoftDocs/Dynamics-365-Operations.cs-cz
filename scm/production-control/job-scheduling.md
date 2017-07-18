---
title: "Plánování úlohy"
description: "Tento článek obsahuje informace o plánování úloh, což je podrobnější forma plánování než plánování operací. Plánování úkolů můžete použít k jednotlivých úkolů nebo dílenských zakázek a k řízení výrobního prostředí."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3c7224390ce336439c2e43188c19b4b93cf793b8
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017

---

# <a name="job-scheduling"></a>Plánování úlohy

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o plánování úloh, což je podrobnější forma plánování než plánování operací. Plánování úkolů můžete použít k jednotlivých úkolů nebo dílenských zakázek a k řízení výrobního prostředí.

Plánování úkolů můžete použít k jednotlivých úkolů nebo dílenských zakázek a k řízení výrobního prostředí. Plánování úkolů je rozděleno na jednotlivé úkoly nebo práce. Tyto úkoly jsou následně přiřazeny k zdrojům operace, které je budou provádět. Také plánování práce umožňuje synchronizaci všech úloh, které odkazují na vybranou úlohu. Můžete zadat čas zahájení nebo skončení úkolu a dobu trvání úkolu a tyto údaje pak použít při plánování. Zadaný čas může být časem zahájení nebo časem skončení, v závislosti na výběru způsobu plánování. Tato funkce je užitečná, když úlohu může například být spuštěna pouze na jednom stroji současně, nebo chcete-li optimalizovat úlohy, která se provede pro každý zdroj.

## <a name="tasks-in-the-job-scheduling-process"></a>Úlohy v procesu plánování práce
Proces plánování úlohy poptávky zahrnuje následující úkoly:

-   Rozdělte operace na úkoly.
-   Plánování úkolů podle data a času pro zdroje určených pro související operace.
-   Vypočítejte časy zahájení a ukončení jednotlivých úloh. Můžete použít omezenou kapacitu, abyste se ujistili, že neexistují žádné překrývající se časy.
-   Určete, které prostředky ve skupině prostředků se mají použít ke spuštění úlohy. Tento úkol vyžaduje zadání skupiny prostředků pro operaci. Plánování práce vybere prostředky nebo skupiny prostředků na základě nejkratší době realizace a také bere v úvahu všechny předchozí rezervace na prostředky.
-   Operace se rozrostou na úkoly při spuštění plánování úloh. Úkoly jsou plánovány podle data a času podle pořadí stanoveného výrobním postupem. Nastavení operace určuje úlohy, které se během procesu plánování rozrůstají. Skupina postupu, která je přiřazena k operaci, řídí, zda jsou generovány úkoly. Úkol je vytvořen pouze tehdy, pokud má konkrétní dobu trvání. Například úloha s dopravním časem bude generován, jestliže byl pro vybranou operaci zadán dopravní čas.

## <a name="scheduling-direction"></a>Způsob plánování
Můžete naplánovat úlohy dopředu nebo dozadu.

-   **Vpřed** – Metodu plánování Vpřed od použijte, chcete-li zahájit výrobu co nejdříve. Pro tuto metodu se rovněž používá označení metoda nabízení, protože výroba je protlačena výrobním procesem vpřed. Výroba je naplánována k zahájení a ukončení na nejbližší možná data.
-   **Dozadu** – Metodu plánování Dozadu od použijte, chcete-li zahájit výrobu co nejpozději. Je též známá jako tahová metoda, protože je založena na datu, kdy musí být výroba dokončena. Plánování dozadu se plánuje zpětně k nejpozdějšímu možnému datu zahájení výroby, kdy bude ještě možné dodržet termín dokončení.

## <a name="finite-capacity"></a>Omezená kapacita
Můžete naplánovat úlohy s použitím omezené kapacity. Při použití omezené kapacity nesmí být naplánována kapacita větší, než kapacita, která je k dispozici pro prostředek. Dostupný čas je definován jako interval, v němž je prostředek k dispozici a kapacita není jiným způsobem rezervována. Plánování na základě omezené kapacity se ujistí, aby se k určitému datu nepřekrývaly počáteční a koncové časy operace. Brána do úvahy je kapacita prostředku, která již byla rezervovaná a také překrývající se počáteční a koncové časy. Omezená kapacita určuje množství kapacity, která musí být k dispozici pro zdroj v rámci dosažení optimálního využití prostředku. Toto určení je vyváženo proti výpočtu co nejkratší doby realizace mezi operacemi.

## <a name="finite-materials"></a>Omezený materiál
Plánování úkolů založené na omezeném materiálu zajišťuje dostupnost požadovaných materiálů při zahájení operace. Pravidla disponibility pro položky definují tato omezení. Plánování využívá růstu požadavku ke stanovení, kdy jsou položky součástí k dispozici. Pokud plánujete bez nastavení omezených materiálů, systém předpokládá, že všechny položky jsou k dispozici, kdy je potřeba.

## <a name="finite-properties"></a>Omezené vlastnosti
Plánování úkolů se zvláštními vlastnostmi vyžaduje zadání vlastností pro operace výrobního postupu. K zajištění kapacity musí být tyto vlastnosti splněny.

## <a name="references"></a>Odkazy
Při plánování úkolů jsou plánovány všechny výroby odkazující k aktuální výrobě. Pokud výroba obsahuje jednu nebo více dílčích výrob, měly by dílčí výroby být naplánovány současně s hlavní výrobou, protože hlavní výrobu nelze zahájit, dokud nejsou dokončeny související dílčí výroby.

## <a name="schedule-resources"></a>Plánovat prostředky
Plánovací modul prozkoumá kombinace prostředků pro identifikaci těchto kombinací, které mohou splnit požadavky. Kritéria výběru můžete zadat výběrem některé z následujících hodnot v poli **Výběr primárního prostředku** na stránce **Parametry plánování**:

-   **Doba trvání** – Modul plánování vybere zdroj s nejkratší dobou realizace. **Poznámka:** Plánování podle trvání může způsobit snížený výkon, pokud stejná skupina prostředků obsahuje mnoho prostředků a jsou použity sekundární operace. Lze naplánovat nejvýše 32 prostředků na operaci. Pokud toto množství překročíte, bude zobrazena zpráva informačního protokolu a plánování úloh nenalezne nejlepší alternativní zdroj.
-   **Priorita** – Plánovací modul vybere prostředek, který má vyšší prioritu. Jestliže dva nebo více prostředků mají stejné možnost výkonem a úrovní. Prostředek, který má nejnižší číslo v tomto poli, má nejvyšší prioritu.

Při spuštění plánování úloh systém naplánuje prostředky potřebné na základě omezení, která jsou definovaná v parametrech prostředků. Kalendářním nastavením můžete řídit kapacitu zdrojů. Systém vypočítá náklady pro zdroje během procesu plánování. **Poznámka:** U výrob, které využívají funkci plánování operací, můžete spustit plánování úloh po plánování operací. Jestliže nepoužíváte plánování operací, můžete spustit plánování úloh samostatně.

## <a name="maximum-capacities-for-resources-per-job-order"></a>Maximální kapacita pro prostředky na pracovní zakázku
Prostředky mají během plánování práce přidělovány úlohy. Pro zdroje lze na pracovní zakázku zajistit maximální kapacity. Systém lze například nastavit k naplánování, že pro jednu výrobní zakázku není možné přidělit více než 50 procent celkové kapacity. Toto nastavení vám poskytuje větší kontrolu nad plánováním zdrojů na úrovni plánování úloh. Lze tak zabránit potížím, když není dostatečná disponibilní kapacita pro souběžné výroby.

## <a name="resource-efficiency"></a>Účinnost zdrojů
Při plánování úkolů jsou brány v úvahu použitá procenta účinnosti určená pro prostředky. Procenta účinnosti prodlužují nebo zkracují čas vyhrazený pro prostředek. Následně je rovněž prodloužena nebo zkrácena doba realizace. Následující vzorec je použitý k výpočtu: Plánovaný čas = Čas × 100 ÷ procento účinnosti v tomto vzorci, *čas* zahrnuje operační čas a dobu nastavení.





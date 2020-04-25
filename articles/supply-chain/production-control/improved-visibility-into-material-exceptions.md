---
title: Přehled výjimek materiálu
description: Toto téma popisuje, jak získat lepší přehled výjimek surovin pro výrobní zakázky a dávkové objednávky.
author: johanhoffmann
manager: tfehr
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 37d0841b656153255b9230a60229d30064b81fbe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212611"
---
# <a name="visibility-into-material-exceptions"></a>Přehled výjimek materiálu

[!include [banner](../includes/banner.md)]

V pracovním prostoru **Správa výrobního provozu** prostoru vám poskytují lepší přehled výjimek surovin pro výrobní zakázky a dávkové objednávky tři dlaždice:

- Neuvolněné řádky materiálu vyžadující pozornost
- Nezpracované vlny vyžadující pozornost
- Otevřená skladová práce vyžadující pozornost

Pro všechny tři dlaždice se srovnává datum surovin řádků kusovníku a řádků receptury s datem pracovního prostoru a s filtry možností **Výrobní jednotka**, **Skupinu prostředků** a **Prostředek**, které jsou nastavovány v nabídce **Konfigurovat můj pracovní prostor**. Ve výchozím nastavení je datum pracovního prostoru nastaveno na aktuální datum, které ale lze změnit.

Nevydaný řádek kusovníku nebo receptury vyžaduje pozornost, pokud datum suroviny na řádku je stejné nebo dřívější než datum pracovního prostoru a pokud splňuje kritéria, která se definují podle filtrů v pracovním prostoru.

Na následujícím obrázku představuje modrý panel výrobní úlohu, která je naplánována na zdroji. Počátek úlohy je naplánován na 1. května 2017. Toto datum je datem surovin. Jinými slovy, materiály, které jsou přiřazeny k úloze na řádcích kusovníku a receptury musí být připraveny k tomuto datu. Jiné datum na obrázku, 6. května 2017, představuje datum pracovního prostoru. V tomto příkladu je datum materiálu dřívější než datum pracovního prostoru. Z toho vyplývá, že datum předpokládaného začátku spotřeby materiálu již uplynulo, a řádky kusovníku a řádky receptury splňují kritéria pro vyžadování pozornosti.

![Příklad výrobní úlohy, kde je datum materiálu dřívější než datum pracovního prostoru](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a>Neuvolněné řádky materiálu vyžadující pozornost

Řádek kusovníku nebo receptury může být uvolněn do skladu třemi způsoby:

- Jako součásti uvolnění výrobní objednávky nebo dávkové objednávky
- Jako ruční uvolnění
- Automaticky pomocí dávkové úlohy

Další informace naleznete v tématu [Uvolnění řádků kusovníku a receptury do skladu](releasing-bom-and-formula-lines-to-warehouse.md). 

Pokud nebyl řádek kusovníku nebo receptury uvolněn, nebo byl uvolněn částečně, a pokud jsou splněna kritéria data a filtru pracovního prostoru, je řádek obsažen ve výpočtu čísla, které se objeví v dlaždici **Neuvolněné řádky vyžadující pozornost**.

Vyberete-li tuto dlaždici, otevře se stránka **Uvolnit do skladu**. Tato stránka zobrazuje počet neuvolněných řádků kusovníku a receptury, který je označen číslem na dlaždici. Neuvolněný řádek se zobrazí v horní mřížce. Tato mřížka ukazuje množství, které byly původně odhadované pro řádek, množství, které již bylo uvolněné, a zbývající množství, které je ještě nutné uvolnit. Můžete přidat řádky z horní mřížky do dolní mřížky. Z dolní mřížky lze poté uvolnit vybrané řádky do skladu. Z dolní mřížky můžete také upravit množství pro uvolnění tak, aby bylo uvolněno pouze částečné množství.

## <a name="unprocessed-waves-needing-attention"></a>Nezpracované vlny vyžadující pozornost

Pokud byl uvolněn řádek kusovníku nebo receptury, je přidán do nové vlny výroby nebo do stávající otevřené vlny, v závislosti na konfiguraci šablony vlny výroby. Při konfiguraci šablony vlny je lze také nastavit vlnu tak, aby se automaticky zpracovala při uvolnění řádku kusovníku nebo receptury. Při zpracování vlny se vytvoří skladová práce vyskladnění surovin. Pokud je šablona vlny nakonfigurována tak, aby nebyly vlny zpracovány v době uvolnění, vlna zůstává v nezpracovaném stavu. Dlaždice **Nezpracované vlny vyžadující pozornost** zobrazuje počet řádků kusovníku a receptury, které byly uvolněny do skladu na nezpracovaných vlnách a které mají datum surovin dřívější nebo stejné jako datum pracovního prostoru. Řádky musí být spotřebovány provozním prostředkem, který se použije na filtrování pracovního prostoru.

Když vyberete tuto dlaždici, otevře se stránka **Všechny vlny výroby**. Tato stránka je filtrována podle počtu otevřených vln, které obsahují řádky z uvolněných řádků kusovníku a receptury splňujících kritéria dlaždice. Ze stránky **Všechny vlny výroby** můžete vlnu zpracovat ručně.

## <a name="open-warehouse-work-needing-attention"></a>Otevřená skladová práce vyžadující pozornost

Dlaždice **Otevřená skladová práce vyžadující pozornost** zobrazuje počet řádků kusovníku a receptury, které byly uvolněny do skladu, mají nezpracovanou práci a které mají datum surovin dřívější nebo stejné jako datum pracovního prostoru. Řádky musí být spotřebovány provozním prostředkem, který se použije na filtrování pracovního prostoru.

Když vyberete tuto dlaždici, otevře se stránka **Veškerá práce**. Tato stránka je filtrována podle počtu otevřených záhlaví práce, které obsahují řádky práce z uvolněných řádků kusovníku a receptury splňujících kritéria dlaždice. Ze stránky **Veškerá práce** můžete práci zpracovat ručně.

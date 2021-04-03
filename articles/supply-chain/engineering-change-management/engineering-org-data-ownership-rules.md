---
title: Pravidla technických společností a vlastnictví dat
description: Toto téma vysvětluje, jak můžete pomocí jedné nebo více technických společností zajistit, aby byla kmenová data produktů centrálně vytvářena a udržována. Technická společnost zastupuje společnost, která vlastní technické výrobky a její technicky relevantní data.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 837960a628ef03df4d73909e96713e256d0f5e60
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262302"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Pravidla technických společností a vlastnictví dat

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Technické a provozní společnosti

K zajištění, že jsou produkty hlavních dat centrálně vytvářeny a spravovány, můžete použít jednu nebo více *technických společností*. Technická společnost má vlastní technické výrobky a jejich technicky relevantní data. Je vždy spojena s (založena na) existující *právnické osobě*, což je také společnost. Prostřednictvím tohoto spojení systém vytváří centrální vstupní bod pro všechna data relevantní pro technické produkty v technické společnosti. V tomto centrálním vstupním bodě se vytvářejí technické produkty a udržují se relevantní data. Z něj budou uvolněny technické produkty a relevantní data pro *provozní společnosti*, což jsou další právnické osoby. (Další informace o správě uvolnění najdete v části [Uvolnění struktury produktu](release-product-structure.md).) Tyto provozní společnosti budou používat technická data tak, jak byla navržena technickou společností. Veškerá logistická data jsou lokálně udržována každou technickou a provozní společností.

Chcete-li vytvořit technickou společnost, přejděte na **Řízení technických změn \> Nastavení \> Technické organizace**. Vyberte **Nový**, zadejte název technické společnosti a vyberte existující společnost (právnickou osobu), na které je založena.

Pokud provádíte integraci s externími systémy správy životního cyklu produktu (PLM), musíte vytvořit obchodní jednotku (typ společnosti), která se stane externí společností.

## <a name="engineering-product-categories-and-engineering-companies"></a>Kategorie technických produktů a technické společnosti

*Kategorie technických výrobků* pomáhají zajistit, aby technické produkty byly vytvářeny v souladu s obchodními pravidly vaší společnosti a chovaly se podle potřeby. Další informace o kategoriích technických produktů najdete v části [Technické verze a kategorie technických produktů](engineering-versions-product-category.md).

Každá kategorie technických produktů patří konkrétní technické společnosti a může vytvářet pouze výrobky, které této společnosti patří. Podobně pak právo na údržbu technického produktu náleží společnosti, která je spojena s kategorií technických výrobků tohoto produktu.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Data, která vlastní technická společnost

Protože technická společnost vlastní data relevantní pro techniku, řídí následující procesy:

- **Tvorba technických produktů:** Každá technická společnost může vytvářet pouze nové technické produkty založené na kategorii technických produktů, které vlastní. V některých případech provozní společnosti udržují svá vlastní místní data, která se vztahují k těmto produktům.
- **Vytvoření technických verzí:** Když společnost vytvoří nový technický produkt, systém pro něj automaticky vytvoří počáteční technickou verzi. Pouze vlastnící technická společnost bude moci vytvářet nové verze tohoto produktu.
- **Vytvoření a správa technických verzí technických atributů:** Když společnost vytvoří nový technický produkt, systém pro něj automaticky vytvoří počáteční technickou verzi. Pouze vlastnická technická společnost bude moci vytvářet a udržovat hodnoty těchto atributů. Další informace o technických atributech získáte v části [Technické atributy a vyhledávání technických atributů](engineering-attributes-and-search.md).
- **Vytváření a údržba kusovníků (BOM), které jsou připojeny k technickým verzím:** Vlastnící technická společnost může přímo připojit kusovník k verzi technického produktu. Když jsou tyto kusovníky vydány jiným právnickým osobám, jsou změny technických údajů v kusovnících omezeny následujícími způsoby:

    - Provozní společnost nemůže odstranit vydané řádky kusovníku.
    - Technická pole na linkách kusovníku jsou pro provozní společnost jen pro čtení. Všechna ostatní pole jsou logistickými implementačními poli a mohou být editována provozní společností.
    - Provozní společnost může přidat řádky kusovníku ke stejnému kusovníku. Tímto způsobem může přidávat místní přísady, jako jsou obalový materiál nebo mazací kapaliny.
    - Provozní společnost může přidat zcela nový místní kusovník. Tato změna může být vyžadována v případech, kdy například během vydání není poskytnut žádný kusovník. Provozní společnost vlastní a udržuje tyto místní kusovníky. Další informace o správě vydání najdete v části [Uvolnění struktur produktu](release-product-structure.md).
    - Když místní technická společnost aktualizuje svůj kusovník, zůstanou zachovány všechny místní kusovníky a řádky kusovníku.

- **Vytváření a údržba tras, které jsou připojeny k technickým verzím:** Vlastnící technická společnost může přímo připojit kusovník k verzi technického produktu. Když jsou tyto trasy vydány jiným právnickým osobám, jsou změny technických údajů v trasách omezeny následujícími způsoby:

    - Ostatní právnické osoby nemohou odstranit technická data v trasách.
    - Ostatní právní subjekty mohou přidávat operace na trasu. Tímto způsobem mohou přidat místní kroky trasy.
    - Provozní společnosti mohou přidat zcela nové místní trasy. Tato změna může být vyžadována například v případech, kdy jste během vydání nepřidali trasy. Provozní společnosti vlastní a udržují tyto místní trasy. Další informace o správě vydání najdete v části [Uvolnění struktur produktu](release-product-structure.md).
    - Všechny změny provedené místně se zachovají, když se na trasy znovu vydají aktualizace od technické společnosti.

- **Tvorba a údržba technických dokumentů:** Technická společnost může ke každé technické verzi připojit technické dokumenty.

    - Když jsou tyto dokumenty předány jiným právnickým osobám, jsou chráněny před odstraněním provozní společností.
    - Jiné právnické osoby mohou přidávat zcela nové místní dokumenty. Provozní společnost vlastní a udržuje tyto místní dokumenty.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
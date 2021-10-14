---
title: Přehled konfigurace produktu založeného na dimenzích
description: Konfigurace produktu založená na dimenzích představuje jednoduché řešení pro vytváření mnoho variant produktu z jednoho hlavního produktu a příslušných kusovníků.
author: t-benebo
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19821"
- intro-internal
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1eb610cc0eaa687ca2552cd71227fe48e379eb5c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568560"
---
# <a name="dimension-based-product-configuration-overview"></a>Přehled konfigurace produktu založeného na dimenzích

[!include [banner](../includes/banner.md)]

Konfigurace produktu založená na dimenzích představuje jednoduché řešení pro vytváření mnoho variant produktu z jednoho hlavního produktu a příslušných kusovníků.

Konfigurace produktu založená na dimenzích je jednou ze tři předdefinovaných technologií konfigurace produktu. Zbývající dvě technologie jsou předdefinované varianty a konfigurace založená na omezeních. Všechny tři technologie používají základní produkt jako výchozí bod a umožňují uživateli vytvořit mnoho variant produktu pro jeden základní produkt.

## <a name="key-concepts"></a>Klíčové koncepty
Konfigurace produktu založená na dimenzích vychází z následujících klíčových konceptů:

-   Základní produkty
-   Konfigurační dimenze produktu
-   Konfigurační skupiny
-   Kusovník
-   Konfigurační postup
-   Konfigurační pravidla

### <a name="product-masters"></a>Základní produkty

Základní produkt je výchozím bodem pro všechny procesy konfigurace produktu. Pro konfiguraci produktu založenou na dimenzích je vyžadován základní produkt s konkrétní technologií konfigurace a skupina dimenzí produktu, která zahrnuje konfigurační dimenzi produktu.

### <a name="configuration-product-dimension"></a>Konfigurační dimenze produktu

Konfigurační dimenze produktu se používá k identifikaci variant produktu pro základní produkt s technologií konfigurace založené na dimenzích. Hodnotu dimenze pro konfiguraci zadává uživatel a měla by pomoci k určení individuálních variant produktu.

### <a name="configuration-groups"></a>Konfigurační skupiny

Konfigurační skupiny se definují v centrálním úložišti a lze je použít pro všechny modely konfigurace produktu založené na dimenzích. Konfigurační skupiny jsou připojeny k jednotlivým řádkům kusovníku a společně tvoří skupinu řádků, které se vzájemně vylučují. To znamená, že pro jednu variantu produktu lze vybrat pouze jeden řádek v určité skupině.

### <a name="bill-of-materials-bom"></a>Kusovník

Kusovník představuje stavební kameny konfigurace produktu založené na dimenzích. Musí obsahovat všechny jiné produkty, které lze použít v kterékoli variantě produktu. Každý řádek v kusovníku může odkazovat na konfigurační skupinu. Pokud řádek neodkazuje na konfigurační skupinu, zahrne se do všech variant produktu.

### <a name="configuration-route"></a>Konfigurační postup

Konfigurační postup určuje pořadí skupin konfigurace, ve kterém se uživateli zobrazují během procesu konfigurace produktu.

### <a name="configuration-rules"></a>Konfigurační pravidla

Konfigurační pravidla představují mechanismus, který zajišťuje, že produkt zahrnutý v jedné konfigurační skupině v kusovníku vynutí buď zahrnutí, nebo vyloučení produktu v jiné konfigurační skupině ve stejném kusovníku.

## <a name="product-modeling-process"></a>Proces modelování produktu
Přirozená sekvence vytváření modelu produktu začíná pro produkty založené na dimenzích určením odpovídajících konfiguračních skupin. Je důležité zajistit, aby se všechny produkty, které se použijí v kusovníku, uvolnily společnosti, pro kterou se model produktu vytváří. Pomocí těchto stavebních bloků může uživatel vytvořit kusovník a přiřadit konfigurační skupiny všem odpovídajícím řádkům kusovníku. Po dokončení kusovníku lze definovat konfigurační postup pro řazení konfiguračních skupin ve správném pořadí. [![Proces modelování produktů na základě dimenzí.](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Pokud existují určité produkty z různých konfiguračních skupin, které musí nebo naopak nemusí být použité společně, můžete vytvořit konfigurační pravidla, která vynutí vztahy mezi těmito výrobky. Poté, co se kusovník provázal se základním produktem založeným na dimenzích pomocí verze kusovníku a oba jsou schválené a aktivované, lze vytvořit konfiguraci produktu zadat název pro každou konfigurace. Konfigurace lze definovat předtím, než se vygenerují transakce, nebo to lze provést, jakmile dojde k potřebě určité konfigurace.

### <a name="suggested-use"></a>Předpokládané použití

Technologie konfigurace založené na dimenzích je nejvhodnější pro produkty s omezenou variabilitou a kombinací standardní velikosti, barvy a stylu dimenzí produktu. Konfigurace není vhodná pro identifikaci konkrétní varianty produktu. Příkladem může být jízdní kolo s výškou rámu, velikostí kola, typem brzd a různým vybavením.

### <a name="next-step"></a>Další krok 

Následujících osm průvodců záznamem úloh by mělo být dokončeno v pořadí, v jakém jsou uvedeny. 

1.  [Vytvoření základního produktu založeného na dimenzích](tasks/create-dimension-based-product-master.md)
2.  [Uvolnění základního produktu založeného na dimenzích](tasks/release-dimension-based-product-master.md)
3.  [Základní nastavení uvolněného základního produktu](tasks/complete-basic-setup-released-product-master.md)
4.  [Definování konfiguračních skupin](tasks/define-configuration-groups.md)
5.  [Vytvoření kusovníku pro základní produkt založený na dimenzích](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Definování konfiguračních postupů](tasks/define-configuration-route.md)
7.  [Vytváření konfiguračních pravidel](tasks/create-configuration-rules.md)
8.  [Vytváření konfigurací založených na dimenzích](tasks/create-dimension-based-configurations.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: "Konfigurace produktu založené na dimenzích"
description: "Konfigurace produktu založená na dimenzích představuje jednoduché řešení pro vytváření mnoho variant produktu z jednoho hlavního produktu a příslušných kusovníků."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7fbf69dc217a2f61ec3aeda952ff221491e9385a
ms.lasthandoff: 03/31/2017


---

# <a name="dimension-based-product-configuration"></a>Konfigurace produktu založené na dimenzích

[!include[banner](../includes/banner.md)]


Konfigurace produktu založená na dimenzích představuje jednoduché řešení pro vytváření mnoho variant produktu z jednoho hlavního produktu a příslušných kusovníků.

Konfigurace produktu založené na dimenzích je jedním z tři konfigurace technologie integrovaný produkt. Zbývající dvě technologie jsou předdefinované varianty a konfigurace založená na omezeních. Všechny tři technologie používají základní produkt jako výchozí bod a umožňují uživateli vytvořit mnoho variant produktu pro jeden základní produkt.

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
Přirozená sekvence vytváření modelu produktu začíná pro produkty založené na dimenzích určením odpovídajících konfiguračních skupin. Je důležité zajistit, aby se všechny produkty, které se použijí v kusovníku, uvolnily společnosti, pro kterou se model produktu vytváří. Uživatel s těmito stavebními bloky na místě, můžete vytvořit Kusovník a konfigurační skupiny přiřadit všechny příslušné řádky Kusovníku. Po dokončení Kusovníku lze definovat postup konfigurace pro konfiguraci skupin pořadí ve správném pořadí. \[Titulek id = "Příloha\_282671" Zarovnat = "alignnone" width = "1187"\][![založené na dimenzích produktu proces modelování](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) založené na dimenzích produktu proces modelování\[/titulek\] Pokud jsou některé produkty z různých konfiguračních skupin, které musí nebo nesmí být použity současně, můžete vytvořit pravidla konfigurace, které budou uplatňovat tyto vztahy produktu. Poté, co se kusovník provázal se základním produktem založeným na dimenzích pomocí verze kusovníku a oba jsou schválené a aktivované, lze vytvořit konfiguraci produktu zadat název pro každou konfigurace. Konfigurace lze definovat předtím, než se vygenerují transakce, nebo to lze provést, jakmile dojde k potřebě určité konfigurace.

### <a name="suggested-use"></a>Předpokládané použití

Technologie konfigurace založené na dimenzích je nejvhodnější pro produkty s omezenou variabilitou a kombinací standardní velikosti, barvy a stylu dimenzí produktu. Konfigurace není vhodná pro identifikaci konkrétní varianty produktu. Příkladem může být jízdní kolo s výškou rámu, velikostí kola, typem brzd a různým vybavením.





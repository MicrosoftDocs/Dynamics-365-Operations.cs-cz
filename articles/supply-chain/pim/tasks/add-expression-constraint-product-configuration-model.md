---
title: Přidání omezení výrazu do modelu konfigurace produktu
description: Tento postup popisuje, jak můžete přidat nový výraz omezení pro model konfigurace produktu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56f94b82f8b2642b12a993bde7d6bb323da79f98
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "360571"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Přidání omezení výrazu do modelu konfigurace produktu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak můžete přidat nový výraz omezení pro model konfigurace produktu. Ukazuje, jak se můžete vyhlásit, že ochrana rohu musí být uplatněna na reproduktor, pokud uživatel vybral přední mřížkou kovovou. Postup používá komponentu špičkového reproduktoru v ukázkové společnosti USMF.


## <a name="create-an-expression-constraint"></a>Vytvoření omezení výrazu
1. Klepněte na Definice modelu varianty produktu.
2. Klepněte na Modely konfigurace produktu.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Tento příklad používá model Špičkového reproduktoru.  
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Rozbalte sekci Omezení.
6. Klepněte na možnost Přidat.
7. Klikněte na položku Vytvořit.
8. Zadejte hodnotu do pole Název.

## <a name="enter-expression"></a>Zadat výraz
1. Klepněte na Upravit výraz.
    * Pokud odemknete uživatelské rozhraní v záznamu úkolů v této fázi, můžete používat IntelliSense a seznam symbolů k vytváření omezení výrazu.  
2. V poli Základ omezení zadejte hodnotu „Implikuje [Přední mřížka == "Kov", Ochrana rohu]“.
    * Tento logický výraz uvádí: Pokud přední mřížka je kovová, je nutné vybrat možnost ochrany rohu.  
3. Klikněte na tlačítko Ověřit.
    * Ověřovací funkce je spuštěna prostřednictvím omezení výrazu a kontroluje chyby syntaxe.  
4. Klikněte na tlačítko Zavřít.
5. Klikněte na tlačítko OK.


--- 
title: "Přidání omezení výrazu do modelu konfigurace produktu"
description: "Tento postup popisuje, jak můžete přidat nový výraz omezení pro model konfigurace produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b8286eba5c799789ebba9a501a5a0b06ccdaabb1
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Přidání omezení výrazu do modelu konfigurace produktu

[!include[task guide banner](../../includes/task-guide-banner.md)]

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



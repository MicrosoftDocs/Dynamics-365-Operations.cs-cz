---
title: Přidání omezení výrazu do modelu konfigurace produktu
description: Tento postup popisuje, jak můžete přidat nový výraz omezení pro model konfigurace produktu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920874"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>Přidání omezení výrazu do modelu konfigurace produktu

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak můžete přidat nový výraz omezení pro model konfigurace produktu. Ukazuje, jak se můžete vyhlásit, že ochrana rohu musí být uplatněna na reproduktor, pokud uživatel vybral přední mřížkou kovovou. Postup používá komponentu špičkového reproduktoru v ukázkové společnosti USMF.

## <a name="create-an-expression-constraint"></a>Vytvoření omezení výrazu

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Tento příklad používá model Špičkového reproduktoru.  
4. Vyberte odkaz na vybraném řádku v seznamu.
5. Rozbalte sekci **Omezení**.
6. Vyberte **přidat**.
7. Vyberte **Vytvořit**.
8. Zadejte hodnotu do pole **Název**.

## <a name="enter-expression"></a>Zadat výraz

1. Vyberte **Upravit výraz**.
    * Pokud odemknete uživatelské rozhraní v záznamu úkolů v této fázi, můžete používat IntelliSense a seznam symbolů k vytváření omezení výrazu.  
2. V poli **Základ omezení** zadejte hodnotu „Implies[FrontGrill=="Metal", CornerProtection]“.
    * Tento logický výraz uvádí: Pokud přední mřížka je kovová, je nutné vybrat možnost ochrany rohu.  
3. Vyberte **Ověřit**.
    * Ověřovací funkce je spuštěna prostřednictvím omezení výrazu a kontroluje chyby syntaxe.  
4. Vyberte **Zavřít**.
5. Vyberte **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
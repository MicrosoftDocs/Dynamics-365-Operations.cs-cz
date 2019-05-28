---
title: Přidání výpočtu do modelu konfigurace produktu
description: Tento postup popisuje, jak přidat nový výpočet pro model konfigurace produktu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9754c46010e7bbdb2edef0d6e68162f344bb1257
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570404"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Přidání výpočtu do modelu konfigurace produktu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak přidat nový výpočet pro model konfigurace produktu. Zobrazuje vytvoření logického výrazu za použití operátoru „Jestliže“ k nastavení výšky reproduktoru až 10 pro bílé reproduktory a 15 pro jiné povrchové úpravy skříně. Postup používá komponentu špičkového reproduktoru v ukázkové společnosti USMF.


## <a name="add-a-calculation"></a>Přidání výpočtu

## <a name="create-calculation-expression"></a>Vytvoření vzorce výpočtu
1. Klepněte na Upravit výraz.
2. Do pole Základ omezení zadejte „Jestliže [Povrchová úprava skříně == „bílá“, 10, 15]“.
3. Klikněte na tlačítko Ověřit.
4. Klikněte na tlačítko Zavřít.
5. Klikněte na tlačítko OK.


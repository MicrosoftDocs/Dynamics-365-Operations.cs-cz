---
title: Přidání výpočtu do modelu konfigurace produktu
description: Tento postup popisuje, jak přidat nový výpočet pro model konfigurace produktu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d09a3544631960e3f6b292dbdd8927dd499f07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987047"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Přidání výpočtu do modelu konfigurace produktu

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak přidat nový výpočet pro model konfigurace produktu. Zobrazuje vytvoření logického výrazu za použití operátoru „Jestliže“ k nastavení výšky reproduktoru až 10 pro bílé reproduktory a 15 pro jiné povrchové úpravy skříně. Postup používá komponentu špičkového reproduktoru v ukázkové společnosti USMF.


## <a name="add-a-calculation"></a>Přidání výpočtu

## <a name="create-calculation-expression"></a>Vytvoření vzorce výpočtu
1. Klepněte na Upravit výraz.
2. Do pole Základ omezení zadejte „Jestliže [Povrchová úprava skříně == „bílá“, 10, 15]“.
3. Klikněte na tlačítko Ověřit.
4. Klikněte na tlačítko Zavřít.
5. Klikněte na tlačítko OK.


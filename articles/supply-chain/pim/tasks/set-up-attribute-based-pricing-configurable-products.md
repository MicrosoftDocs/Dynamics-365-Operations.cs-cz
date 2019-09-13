---
title: Nastavení ocenění podle atributů pro konfigurovatelné produkty
description: Toto téma vysvětluje, jak nastavit ceny na základě atributů.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 534e9c9332c107afebd814cf2090ecbdf0ec6459
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914692"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Nastavení ocenění podle atributů pro konfigurovatelné produkty

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toto téma vysvětluje, jak nastavit ceny na základě atributů. Jako předpoklad musíte mít model konfigurace produktu, který má jednu nebo více komponent a atributů. Tento příklad využívá model špičkového reproduktoru v ukázkové datové společnosti USMF. Manažer produktu obvykle používá tuto proceduru.


## <a name="create-a-new-price-model"></a>Vytvoření nového cenového modelu
1. Vyberte **Definici modelu varianty produktu** na domovské stránce.
2. Vyberte **Modely konfigurace produktu** v části **odkazy**.
3. V seznamu vyberte řádek **Špičkový reproduktor**, ale nevybírejte odkaz pro název.
4. V podokně akcí zvolte **Model**.
5. Vyberte **Cenové modely**.
6. Zvolte **Nové**.
7. Do pole **Název cenového modelu** zadejte hodnotu. Použijte název, který usnadňuje identifikaci modelu.  
8. Zadejte hodnotu do pole **Popis**.
9. Zvolte **Uložit**.

## <a name="add-price-elements"></a>Přidání cenových prvků
1. Vyberte možnost **Upravit**. Každá komponenta v produktovém modelu u může mít element základní ceny a libovolný počet pravidel výrazu ceny. Můžete také přidat ceny v různých měnách.  
2. Zadejte hodnotu do pole **Výraz základní ceny**. Zadejte například 100. Výraz základní ceny může být číselná hodnota nebo se může skládat z aritmetického výpočtu, který zahrnuje jeden nebo více atributů.  
3. Vyberte **přidat**.
4. Do pole **Název** zadejte `Rosewood`. Název cenový výraz pomáhá určit, co představuje cenový prvek. V tomto příkladu vytváříme cenový prvek pro možnost Dokončení skříňky z růžového dřeva.  
5. Vyberte **Podmínku úpravy**. Cenové podmínky pomáhají zaručit, že prvek cenového výrazu je součástí prodejní ceny pouze v případě, že existuje určité kombinace atributů.  
6. Do pole **ConstraintBody** zadejte `CabinetFinish=="Rosewood"`.
7. Vyberte **OK**.
8. Zadejte hodnotu do pole **Výraz**. Zadejte například typ `50`. 
9. Zavřete stránku.


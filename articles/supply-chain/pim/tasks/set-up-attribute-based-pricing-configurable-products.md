---
title: Nastavení ocenění podle atributů pro konfigurovatelné produkty
description: Tato procedura popisuje, jak nastavit ceny na základě atributů.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8568b5f4933ae58bc2d55a169c798668e03bed2a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "333776"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Nastavení ocenění podle atributů pro konfigurovatelné produkty

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje, jak nastavit ceny na základě atributů. Jako předpoklad musíte mít model konfigurace produktu, který má jednu nebo více komponent a atributů. Tento příklad využívá model špičkového reproduktoru v ukázkové datové společnosti USMF. Manažer produktu obvykle používá tuto proceduru.


## <a name="create-a-new-price-model"></a>Vytvoření nového cenového modelu
1. Klepněte na Definice modelu varianty produktu.
2. Klepněte na Modely konfigurace produktu.
3. V seznamu vyberte řádek Špičkový reproduktor, ale neklepejte na odkaz pro název.
4. V podokně akcí klepněte na možnost Model.
5. Klikněte na Cenové modely.
6. Klikněte na položku Nová.
7. Do pole Název modelu zadejte hodnotu.
    * Použijte název, který usnadňuje identifikaci modelu.  
8. Zadejte nějakou hodnotu do pole Popis.
9. Klikněte na položku Uložit.

## <a name="add-price-elements"></a>Přidání cenových prvků
1. Klikněte na položku Upravit.
    * Každá komponenta v produktovém modelu u může mít element základní ceny a libovolný počet pravidel výrazu ceny. Můžete také přidat ceny v různých měnách.  
2. Zadejte hodnotu do pole Výraz základní ceny.
    * Zadejte například 100.   Výraz základní ceny může být číselná hodnota nebo se může skládat z aritmetického výpočtu, který zahrnuje jeden nebo více atributů.  
3. Klepněte na možnost Přidat.
4. Zadejte text „Růžové dřevo“ do pole Název.
    * Název cenový výraz pomáhá určit, co představuje cenový prvek. V tomto příkladu vytváříme cenový prvek pro možnost Dokončení skříňky z růžového dřeva.  
5. Klikněte na Upravit podmínku.
    * Cenové podmínky pomáhají zaručit, že prvek cenového výrazu je součástí prodejní ceny pouze v případě, že existuje určité kombinace atributů.  
6. Do pole Základ omezení zadejte Povrchová úprava skříně == „růžové dřevo“.
7. Klikněte na tlačítko OK.
8. Zadejte hodnotu do pole Výraz.
    * Zadejte například 50.  
9. Zavřete stránku.
10. Zavřete stránku.


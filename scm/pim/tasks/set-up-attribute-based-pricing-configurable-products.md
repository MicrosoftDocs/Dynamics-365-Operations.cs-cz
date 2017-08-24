--- 
title: "Nastavení ocenění podle atributů pro konfigurovatelné produkty"
description: "Tato procedura popisuje, jak nastavit ceny na základě atributů."
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 473d01ecddfd58aa72a972ee901673534c9d7c9c
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Nastavení ocenění podle atributů pro konfigurovatelné produkty

[!include[task guide banner](../../includes/task-guide-banner.md)]

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



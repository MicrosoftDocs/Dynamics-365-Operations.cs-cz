--- 
title: "Registrace položek pro položky umožňující základní uskladnění s použitím deníku doručení zboží"
description: "Tento postup popisuje, jak zaregistrovat položky pomocí deníku doručení položek, když použijete \"základní funkce skladu\" v modulu Řízení zásob."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: c7148bd807ef29b0dd89204a0fbe9b8480095aba
ms.contentlocale: cs-cz
ms.lasthandoff: 11/02/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a>Registrace položek pro položky umožňující základní uskladnění s použitím deníku doručení zboží

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak zaregistrovat položky pomocí deníku doručení položek, když použijete "základní funkce skladu" v modulu Řízení zásob. To obvykle provádí přijímající pracovník. Tento postup můžete spustit s ukázkovými daty společnosti USMF s ukázkovými hodnotami, které jsou zobrazeny.  Pokud nepoužíváte USMF, musíte mít před zahájením tohoto průvodce potvrzenou nákupní objednávku s otevřeným řádkem nákupní objednávky. Položky na řádku musí být na skladě a nesmí používat varianty produktu a nesmí obsahovat sledovací dimenze. Položka zároveň musí být přidružena ke skupině dimenzí úložiště, kde jsou aktivní pracoviště a sklad.


## <a name="create-item-arrival-journal-header"></a>Vytvoření záhlaví deníku pro doručení položky
1. Přejděte do Řízení zásob > Položky deníku > Doručení položky > Doručení položky.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
    * Pokud používáte data USMF, můžete zadat „WHS“. Pokud používáte jiná data, deník s názvem, který zvolíte, musí mít následující vlastnosti: u možnosti Zkontrolovat výdejní skl. místo musí být nastavena hodnota Ne a u Řízení karantény musí být nastavena hodnota Ne.  
4. Zadejte hodnotu do pole Dodací list.
    * Jedná se o ID dodacího listu z dodacího listu vydaného dodavatelem. Přidejte jedinečné číslo.  
5. V poli Číslo vyberte nákupní objednávku.
6. Klikněte na tlačítko OK.

## <a name="add-lines-to-item-arrival-journal"></a>Přidání řádků do deníku doručení zboží
1. Klepněte na možnost Funkce.
2. Klikněte na Vytvořit řádky.
    * Řádky lze zadat ručně do tohoto deníku, nebo je vytvořit automaticky. Tím se zobrazí, jak lze vytvoření provést automaticky.  
3. Zaškrtněte nebo zrušte zaškrtnutí políčka Inicializovat množství.
    * To zahájí sledování množství na řádcích deníku, u kterých není množství zaregistrováno z řádku nákupní objednávky.  
4. Klikněte na tlačítko OK.

## <a name="post-the-journal"></a>Zaúčtovat deník
1. Klikněte na položku Zaúčtovat.
2. Klikněte na tlačítko OK.

## <a name="generate-the-product-receipt"></a>Generování příjemky produktu
1. Klepněte na možnost Funkce.
2. Klikněte na položku Příjemka produktu.
3. Klikněte na tlačítko OK.



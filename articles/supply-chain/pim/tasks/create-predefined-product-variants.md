---
title: Vytváření předdefinovaných variant produktů
description: Tento postup vás provede vytvořením variant produktu pro základní produkt za pomoci kombinací dimenzí produktu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fa9c6d4862a49bbf0b5ecbb8c0c3d573e0f49e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423813"
---
# <a name="create-predefined-product-variants"></a>Vytváření předdefinovaných variant produktů

[!include [banner](../../includes/banner.md)]

Tento postup vás provede vytvořením variant produktu pro základní produkt za pomoci kombinací dimenzí produktu. K vytvoření tohoto postupu je použita ukázková společnost USMF.


## <a name="create-a-product-master"></a>Vytvoření základního produktu
1. Přejděte do nabídky Řízení informací o produktech > Produkty > Základní produkty.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Číslo produktu.
    * Ruční zadání čísla produktu je povinné, pouze není-li nastavena číselná řada pro pole čísla produktu. Jinak řečeno tento krok přeskočte, je-li pro dané pole nastavena číselná řada.  
4. Do pole Název produktu zadejte hodnotu.
5. V poli Skupina dimenze produktu zadejte nebo vyberte hodnotu.
    * Vyberte skupinu dimenzí produktu SizeCol (velikost a barva).  
6. Klikněte na tlačítko OK.

## <a name="add-product-dimensions"></a>Přidání dimenzí produktu
1. Klikněte na Dimenze produktu.
    * Tento příklad ukazuje, jak zadávat dimenze produktu ručně. Rovněž je možné vybrat velikost, barvu nebo skupinu stylů, která obsahuje hodnoty dimenze produktu, které chcete použít.  
2. Klikněte na položku Nová.
3. Označte v seznamu vybraný řádek.
4. V poli Velikost zadejte nebo vyberte hodnotu.
5. Zadejte hodnotu do pole Název.
6. Klepněte na možnost Nový.
7. Označte v seznamu vybraný řádek.
8. V poli Velikost zadejte nebo vyberte hodnotu.
9. Zadejte hodnotu do pole Název.
10. Klikněte na kartu Barvy.
11. Klikněte na položku Nová.
12. Označte v seznamu vybraný řádek.
13. V poli Barva zadejte nebo vyberte hodnotu.
14. Zadejte hodnotu do pole Název.
15. Klepněte na možnost Nový.
16. Označte v seznamu vybraný řádek.
17. V poli Barva zadejte nebo vyberte hodnotu.
18. Zadejte hodnotu do pole Název.
19. Klikněte na položku Uložit.
20. Zavřete stránku.

## <a name="generate-product-variants"></a>Vytvoření variant produktů
1. Klikněte na Varianty produktu.
2. Klikněte na Návrhy variant.
3. Klikněte na Vybrat vše.
    * V tomto příkladu jsou vybrány všechny možné varianty. Pokud se použije pouze podmnožina možných kombinací dimenzí produktu pro vytváření variant, můžete vybrat jednotlivé položky.  
4. Klikněte na položku Vytvořit.
    * Popisy je možné generovat pro všechny vaše varianty na základě kombinace hodnot dimenze produktu. Popisy jsou volitelné.  
5. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
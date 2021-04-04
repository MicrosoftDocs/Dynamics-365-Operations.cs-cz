---
title: Vytvoření názvosloví čísel produktů pro nakonfigurované varianty produktu
description: Tato procedura ukazuje, jak nastavit názvosloví čísel produktu pro nakonfigurované varianty produktu a jak je přiřadit konfigurovatelnému základnímu produktu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07922a20d5c99640f32bb28ddddaffe846440667
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258868"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Vytvoření názvosloví čísel produktů pro nakonfigurované varianty produktu

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak nastavit názvosloví čísel produktu pro nakonfigurované varianty produktu a jak je přiřadit konfigurovatelnému základnímu produktu. Tato procedura také ukazuje, jak lze vytvářet názvosloví konfigurace komponenty modelu konfigurace produktu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Základnímu produktu D0004 je přiřazeno nové názvosloví čísla produktu. Tento úkol obvykle provádí návrhář produktu.


## <a name="create-a-product-number-nomenclature"></a>Vytvoření názvosloví čísla produktu
1. Klepněte na Definice modelu varianty produktu.
2. Klikněte na Zobrazit názvosloví produktu.
3. Klepněte na možnost Nový.
4. Zadejte hodnotu do pole Název.
5. Zadejte nějakou hodnotu do pole Popis.
6. Klepněte na možnost Přidat.
7. Klikněte na Číslo základního produktu.
8. Klepněte na možnost Přidat.
9. Klikněte na Textová konstanta.
10. Označte v seznamu vybraný řádek.
11. Zadejte hodnotu do pole Text.
12. Klepněte na možnost Přidat.
13. Klikněte na Konfigurace.
14. Zavřete stránku.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Přiřazení názvosloví čísla produktu základnímu produktu
1. Klikněte na Základní produkty.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat pole Číslo produktu pomocí hodnoty „D“.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Klikněte na možnost Upravit.
5. Vyberte možnost Ano v poli Použít názvosloví.
6. V poli Názvosloví čísla varianty produktu zadejte nebo vyberte hodnotu.
7. Zavřete stránku.
8. Zavřete stránku.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Vytvoření názvosloví pro komponentu modelu konfigurace produktu
1. Klepněte na Modely konfigurace produktu.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Klikněte na možnost Upravit.
5. Vyberte možnost Ano v poli Použít konfiguraci.
6. Klepněte na možnost Přidat.
7. Klikněte na Hodnota atributu dávky.
8. Označte v seznamu vybraný řádek.
9. V poli Atribut zadejte nebo vyberte hodnotu.
10. Klepněte na možnost Přidat.
11. Klikněte na Textová konstanta.
12. Označte v seznamu vybraný řádek.
13. Zadejte hodnotu do pole Text.
14. Klepněte na možnost Přidat.
15. Klikněte na Hodnota atributu dávky.
16. Označte v seznamu vybraný řádek.
17. V poli Atribut zadejte nebo vyberte hodnotu.
18. Klepněte na možnost Přidat.
19. Klikněte na Textová konstanta.
20. Označte v seznamu vybraný řádek.
21. Zadejte hodnotu do pole Text.
22. Klepněte na možnost Přidat.
23. Klikněte na Hodnota atributu dávky.
24. Označte v seznamu vybraný řádek.
25. V poli Atribut zadejte nebo vyberte hodnotu.
26. Klepněte na možnost Přidat.
27. Klikněte na Textová konstanta.
28. Označte v seznamu vybraný řádek.
29. Zadejte hodnotu do pole Text.
30. Klepněte na možnost Přidat.
31. Klikněte na Hodnota atributu dávky.
32. Označte v seznamu vybraný řádek.
33. V poli Atribut zadejte nebo vyberte hodnotu.
34. Klepněte na možnost Přidat.
35. Klikněte na Textová konstanta.
36. Označte v seznamu vybraný řádek.
37. Zadejte hodnotu do pole Text.
38. Klepněte na možnost Přidat.
39. Klikněte na Hodnota číselné řady.
40. Označte v seznamu vybraný řádek.
41. V poli Číselná řada zadejte nebo vyberte hodnotu.
42. Zavřete stránku.
43. Zavřete stránku.
44. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
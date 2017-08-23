--- 
title: "Vytvoření čísla produktu pro předdefinované varianty produktu"
description: "Tato příručka ukazuje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu."
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: f14ee57564ad70bb7f28cd9274fc97d07974ec32
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a>Vytvoření čísla produktu pro předdefinované varianty produktu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato příručka ukazuje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Nové názvosloví čísel produktů je přiřazeno skupině dimenzí produktu Barva a Velikost. Tento úkol obvykle provádí návrhář produktu.


## <a name="create-a-product-number-nomenclature"></a>Vytvoření názvosloví čísla produktu
1. Klepněte na Definice modelu varianty produktu.
2. Klikněte na Zobrazit názvosloví produktu.
3. Klepněte na možnost Nový.
4. V poli Název zadejte název názvosloví, který pomáhá identifikovat cílovou skupinu dimenzí produktu, například ColorSize.
5. Zadejte nějakou hodnotu do pole Popis.
6. Klepněte na možnost Přidat.
7. Klikněte na Číslo základního produktu.
8. Klepněte na možnost Přidat.
9. Klikněte na Textová konstanta.
10. Zadejte hodnotu do pole Text.
11. Klepněte na možnost Přidat.
12. Klikněte na Barva.
13. Klepněte na možnost Přidat.
14. Klikněte na Textová konstanta.
15. Zadejte hodnotu do pole Text.
16. Klepněte na možnost Přidat.
17. Klepněte na Velikost.
18. Zavřete stránku.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Přiřazení názvosloví základnímu produktu
1. Klikněte na Skupiny dimenzí produktů.
2. Vyberte skupinu dimenzí produktu SizeCol.
3. Klikněte na možnost Upravit.
4. Vyberte možnost Ano v poli Použít názvosloví.
5. V poli Názvosloví čísla varianty produktu zadejte nebo vyberte hodnotu.
6. Zavřete stránku.



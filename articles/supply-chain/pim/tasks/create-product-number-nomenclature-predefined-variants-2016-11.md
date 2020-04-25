---
title: Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu
description: Toto téma vysvětluje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c39d383c15bcc838e09bc417f7e961c3647828da
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213278"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Nové názvosloví čísel produktů je přiřazeno skupině dimenzí produktu Barva a Velikost. Tento úkol obvykle provádí návrhář produktu.


## <a name="create-a-product-number-nomenclature"></a>Vytvoření názvosloví čísla produktu
1. Zvolte **Definice modelu varianty produktu**.
2. Zvolte **Názvosloví produktu**.
3. Zvolte **Nové**.
4. V poli **Název** zadejte název názvosloví, který pomáhá identifikovat cílovou skupinu dimenzí produktu, například `ColorSize`.
5. Zadejte hodnotu do pole **Popis**.
6. Vyberte **přidat**.
7. Zvolte **Číslo základního produktu**.
8. Vyberte **přidat**.
9. Zvolte **Textová konstanta**.
10. Zadejte hodnotu do pole **Text**.
11. Vyberte **přidat**.
12. Vyberte **Barva**.
13. Vyberte **přidat**.
14. Zvolte **Textová konstanta**.
15. Zadejte hodnotu do pole **Text**.
16. Vyberte **přidat**.
17. Vyberte **Velikost**.
18. Zavřete stránku.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Přiřazení názvosloví základnímu produktu
1. Vyberte **Skupiny dimenzí produktů**.
2. Vyberte **skupinu dimenzí produktu SizeCol**.
3. Vyberte možnost **Upravit**.
4. Vyberte možnost **Ano** v poli **Použít názvosloví**.
5. V poli **Názvosloví čísla varianty produktu** zadejte nebo vyberte hodnotu.
6. Zavřete stránku.


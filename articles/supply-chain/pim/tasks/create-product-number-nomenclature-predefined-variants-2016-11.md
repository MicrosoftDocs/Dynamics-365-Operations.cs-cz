---
title: Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu
description: Toto téma vysvětluje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5179dd54f22de11dc4c0f54113376f13b2f59c48
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569570"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak nastavit názvosloví čísel produktu pro předdefinované varianty produktu a jak je přiřadit vhodné skupině dimenzí produktu. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Nové názvosloví čísel produktů je přiřazeno skupině dimenzí produktu Barva a Velikost. Tento úkol obvykle provádí návrhář produktu.


## <a name="create-a-product-number-nomenclature"></a>Vytvoření názvosloví čísla produktu

1. Přejděte do nabídky **Řízení informací o produktech \> Nastavení \> Nomenklatura produktu**.
1. Zvolte **Nové**.
1. V poli **Název** zadejte název názvosloví, který pomáhá identifikovat cílovou skupinu dimenzí produktu, například `ColorSize`.
1. Zadejte hodnotu do pole **Popis**.
1. Vyberte **přidat**.
1. Zvolte **Číslo základního produktu**.
1. Vyberte **přidat**.
1. Zvolte **Textová konstanta**.
1. Zadejte hodnotu do pole **Text**.
1. Vyberte **přidat**.
1. Vyberte **Barva**.
1. Vyberte **přidat**.
1. Zvolte **Textová konstanta**.
1. Zadejte hodnotu do pole **Text**.
1. Vyberte **přidat**.
1. Vyberte **Velikost**.
1. Zavřete stránku.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Přiřazení názvosloví základnímu produktu

1. Vyberte **Skupiny dimenzí produktů**.
2. Vyberte **skupinu dimenzí produktu SizeCol**.
3. Vyberte možnost **Upravit**.
4. Vyberte možnost **Ano** v poli **Použít názvosloví**.
5. V poli **Názvosloví čísla varianty produktu** zadejte nebo vyberte hodnotu.
6. Zavřete stránku.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
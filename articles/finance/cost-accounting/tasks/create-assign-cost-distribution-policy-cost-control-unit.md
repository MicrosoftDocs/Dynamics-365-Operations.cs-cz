---
title: Vytvoření zásad distribuce nákladů a jejich přiřazení jednotce řízení nákladů
description: Pravidla pro rozdělení nákladů se používají k rozdělení nákladů, které byly finančně vypočítány z hromadného nákladového střediska.
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: CAMCostDistributionRule
ms.openlocfilehash: 23adea279cad3fcf69cc6926d6f8dee485150221
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272391"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Vytvoření zásad distribuce nákladů a jejich přiřazení jednotce řízení nákladů

[!include [banner](../../includes/banner.md)]

Pravidla pro rozdělení nákladů se používají k rozdělení nákladů, které byly finančně vypočítány z hromadného nákladového střediska. Nákladový účetní zajišťuje, že jsou náklady distribuovány do nákladových středisek na základě vybraného základu přidělení. Kontrolní jednotce nákladů jsou přiřazeny zásada a odpovídajících pravidla. Tento průvodce záznamem úloh slouží jako příklad toho, jak vytvořit zásadu distribuce nákladů a odpovídajících pravidel.


## <a name="create-a-policy"></a>Vytvořte zásadu
1. Přejděte na Nákladové účetnictví > Zásady > Zásady distribuce nákladů.
2. Klikněte na položku Nová.
3. Do pole Název zásady zadejte hodnotu.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Vyberte organizaci.  
6. V poli Hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.
    * Vyberte CDS P/L.  
7. V poli Statistická dimenze zadejte nebo vyberte hodnotu.
    * Vyberte Statistické prvky.  
8. Klikněte na položku Uložit.

## <a name="create-rules-for-the-policy"></a>Vytvoření pravidel zásady
1. Klikněte na položku Nová.
2. Označte v seznamu vybraný řádek.
3. V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Rozbalte hierarchii a vyberte 094.  
4. V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.
    * Vyberte Další provozní výdaje a poté vyberte 605110 čištění.  
5. V poli Chování nákladů vyberte možnost.
    * Vyberte Pevné náklady.  
6. V poli Základ přidělení zadejte nebo vyberte hodnotu.
7. Klikněte na položku Nová.
8. Označte na seznamu vybraný řádek.
9. V poli Uzel hierarchie dimenze objektu nákladů zadejte nebo vyberte hodnotu.
    * Rozbalte hierarchii a vyberte 094.  
10. V poli Uzel hierarchie dimenze prvku nákladů zadejte nebo vyberte hodnotu.
    * Vyberte Další provozní výdaje a poté vyberte 605150 Renta.  
11. V poli Chování nákladů vyberte možnost.
    * Vyberte Pevné náklady.  
12. V poli Základ přidělení zadejte nebo vyberte hodnotu.
13. Klikněte na položku Uložit.

## <a name="assign-rules-to-a-cost-control-unit"></a>Přiřazení pravidel k jednotce pro řízení nákladů
1. Klikněte na Přiřazení zásady pro kontrolní jednotky nákladů.
2. Klikněte na položku Nová.
3. Označte v seznamu vybraný řádek.
4. Zadejte datum do pole Platné od data účtování.
    * Vyberte platný fiskální rok – 1. září.  
5. V poli Jednotka řízení nákladů zadejte nebo vyberte hodnotu.
6. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

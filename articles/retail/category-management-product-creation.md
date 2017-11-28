---
title: "Správa a vytvoření kategorií produktů"
description: "Toto téma popisuje vylepšení provedená pro správu kategorií maloobchodního produktu. Tato zlepšení umožní obchodním manažerům udržovat korelaci mezi hierarchií maloobchodních produktů a podrobnostmi o uvolněném produktu."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Retail
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 98250062892e0c5f665616dc3944181a3ff8599a
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="product-category-management-and-creation"></a>Správa a vytvoření kategorií produktů

[!include[banner](./includes/banner.md)]

Vylepšení provedená pro správu kategorií maloobchodního produktu umožní obchodním manažerům udržovat korelaci mezi hierarchií maloobchodních produktů a podrobnostmi o uvolněném produktu. Chcete-li zobrazit tato vylepšení, zvolte v pracovním prostoru **Správa kategorií a produktů** možnost **Hierarchie maloobchodních produktů** a otevřete stránku **Nová struktura kategorií maloobchodních produktů**. 

V předchozích verzích byly vlastnosti produktu rozděleny do vlastností základních produktů a vlastností maloobchodních produktů, podle rozsahu použitelnosti. Vlastnosti maloobchodních produktů byly *globální*. Jinými slovy, pro danou vlastnost produktu se stejná hodnota sdílí mezi všemi právnickými osobami. Vlastnosti základních produktů byly *specifické pro právnickou osobu*. Jinými slovy, daná vlastnost produktu se může lišit napříč právnickými osobami, v závislosti na obchodních požadavcích.

Pomocí těchto vylepšení vlastností produktů v kategorii maloobchodních produktů pokračujeme v oddělování polí, podle jejich použitelnosti v rámci skupiny tak, aby odrážela strukturu formuláře podrobností uvolněného produktu.

Můžete přepínat mezi správou vlastností specifických pro právnickou osobu mezi všemi právnickými osobami a spravovat je pro konkrétní právnickou osobu. Pouze vyberte podle potřeby buď **Zobrazit/upravit pro všechny právnické osoby** nebo **Zobrazit/upravit pro konkrétní právnickou osobu**.

Obchodní manažeři mohou také definovat výchozí hodnoty pro další sadu vlastností produktu na úrovni jednotlivé kategorie. Tyto hodnoty vlastností produkt dědí na základě jejich přidružení k kategorii v době vytvoření produktu.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Vyberte vlastnosti, abyste aktualizovali produkty z formuláře kategorií maloobchodních produktů

Abyste vybrali, které vlastnosti aktualizovaných produktů mají být odeslány k přidruženým produktům, můžete použít vlastnosti logického seskupování.

Obchodní manažeři mohou upravit tyto zděděné vlastnosti produktů pro každý produkt za účelem splnění jednotlivých obchodních požadavků.


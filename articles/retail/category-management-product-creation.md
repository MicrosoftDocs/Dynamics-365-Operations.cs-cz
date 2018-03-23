---
title: "Správa kategorií produktů"
description: "Toto téma popisuje, jak obchodní manažeři mohou použít kategorie maloobchodní produktů ke správě vztahů mezi hierarchií maloobchodních produktů a podrobnostmi uvolněného produktu."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: cs-cz
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>Rozšířená správa kategorií a produktů

[!include[banner](./includes/banner.md)]

Toto téma popisuje rozšířený způsob správy kategorií maloobchodních produktů a produktů v aplikaci Dynamics 365 for Retail. Tato zlepšení umožní obchodním manažerům zobrazit společnou strukturu vlastností produktu mezi hierarchií maloobchodních produktů a podrobnostmi uvolněného produktu.

Pro další informace o správě kategorií maloobchodních produktů přejděte na položku **Hierarchie maloobchodních produktů** z pracovního prostoru **Správa kategorií a produktů** a všimněte si rozšířené struktury stránky **Kategorie maloobchodních produktů**.

![Pracovní prostor správy kategorií a produktů](media/LaunchRetailProductHierarchy.png)

V předchozích verzích byly vlastnosti produktu rozděleny do **vlastností základních produktů** a **vlastností maloobchodních produktů**, podle rozsahu použitelnosti. **Vlastnosti maloobchodních produktů** byly *globální* podle rozsahu použitelnosti, což znamená, že pro dané **vlastnosti maloobchodních produktů** se sdílela stejná hodnota napříč všemi právnickými osobami. **Vlastnosti základních produktů** jsou *specifické pro právnickou osobu*. Jinými slovy, pro danou **vlastnost základního produktu** se může hodnota lišit napříč právnickými osobami, v závislosti na obchodních požadavcích.

V rozšířené struktuře kategorie maloobchodních produktů jsou vlastnosti produktu logicky odděleny podle jejich použitelnosti v rámci skupiny tak, aby odrážely strukturu formuláře podrobností uvolněného produktu.

![Seskupení polí podle jejich rozsahu použitelnosti](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Můžete přepínat mezi správou vlastností specifických pro právnickou osobu mezi všemi právnickými osobami a spravovat je pro konkrétní právnickou osobu. To provedete výběrem možnosti **Zobrazit/upravit pro všechny právnické osoby** nebo **Zobrazit/upravit pro konkrétní právnickou osobu**.

![Přepnutí zobrazení mezi jednotlivými a všemi právnickými osobami](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Přepnutí zobrazení mezi jednotlivými a všemi právnickými osobami](media/ToggleToEditForAllLegalEntities.PNG)  

Ve srovnání s předchozími verzemi může v nové struktuře kategorií maloobchodních produktů obchodní manažer také definovat výchozí hodnoty pro další sadu vlastností produktů na individuální úrovni kategorií. V čase vytvoření produktu se tyto výchozí hodnoty vlastností produktu dědí podle produktu na základě jejich přidružení k jednotlivé kategorii z hierarchie maloobchodních produktů. Tyto zděděné vlastnosti produktu lze upravit pro každý produkt za účelem splnění jednotlivých obchodních požadavků.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Vyberte vlastnosti, abyste aktualizovali produkty z formuláře kategorií maloobchodních produktů 
 
Tuto novou rozšířenou strukturu vlastností produktu můžete použít pro výběr aktualizovaných vlastností produktu, které je třeba odeslat k přiřazeným produktům. 

![Nové rozšířené zobrazení možnosti Aktualizovat produkty](media/NewUpdateProductsEnhancedView.PNG) 

Obchodní manažeři mohou upravit tyto zděděné vlastnosti produktů pro každý produkt za účelem splnění jednotlivých obchodních požadavků.



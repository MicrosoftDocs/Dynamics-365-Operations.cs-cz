---
title: Správa kategorií produktů a produktů
description: Tento článek popisuje, jak obchodní manažeři mohou použít kategorie maloobchodní produktů ke správě vztahů mezi hierarchií produktů Commerce a podrobnostmi uvolněného produktu.
author: ashishmsft
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0871475e0910e0a46544c56083b505ff647fd6a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878562"
---
# <a name="manage-product-categories-and-products"></a>Správa kategorií produktů a produktů

[!include [banner](./includes/banner.md)]

Tento článek popisuje rozšířený způsob správy kategorií produktů a produktů v aplikaci Dynamics 365 Commerce. Tato zlepšení umožní obchodním manažerům zobrazit společnou strukturu vlastností produktu sdílenou mezi hierarchií produktů a podrobnostmi uvolněného produktu.

Další informace o správě v kategoriích produktu získáte tak, že v pracovním prostoru **Správa kategorie a produktu** vyberete dlaždici **Hierarchie produktů Commerce**.

Všimněte si vylepšené struktury rozšířené stránky **Hierarchie produktů Commerce**, která se zobrazí. V předchozích verzích aplikace byly vlastnosti produktu rozděleny na *základní vlastnosti základních* a *vlastností maloobchodních produktů*, podle rozsahu použitelnosti. Vlastnosti maloobchodních produktů jsou *globální* v rozsahu použitelnosti. Jinými slovy, pro danou vlastnost produktu se stejná hodnota sdílí mezi všemi právnickými osobami. Naproti tomu, vlastnosti základních produktů jsou *specifické pro právnickou osobu*. Jinými slovy, pro danou vlastnost základního produktu se může hodnota lišit napříč právnickými osobami, v závislosti na obchodních požadavcích každého právního subjektu.

V rozšířené struktuře kategorie produktů jsou vlastnosti produktu logicky odděleny podle jejich použitelnosti v rámci skupiny tak, aby odrážely strukturu formuláře podrobností uvolněného produktu.

![Seskupení polí podle jejich rozsahu použitelnosti.](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Můžete přepínat mezi správou vlastností specifických pro právnickou osobu mezi všemi právnickými osobami a spravovat je pro konkrétní právnickou osobu.

Abyste mohli spravovat vlastnosti ve všech právnických osobách, vyberte **zobrazit pro všechny právnické osoby** (nebo **upravit pro všechny právnické osoby**).

![Zobrazit nebo upravit pro všechny právnické osoby.](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Abyste mohli spravovat vlastnosti pro určitou právnickou osobu, vyberte **zobrazit pro určité právnické osoby** (nebo **upravit pro specifickou právnickou osobu**).

![Zobrazit nebo upravit pro specifickou právnickou osobu.](media/ToggleToEditForAllLegalEntities.PNG)

Dále pak ve vylepšené kategorii produktů může ve srovnání s předchozími verzemi v nové struktuře kategorií maloobchodních produktů obchodní manažer také definovat výchozí hodnoty pro další sadu vlastností produktů na individuální úrovni kategorií. Po vytvoření produktů se tyto výchozí hodnoty vlastností produktu dědí podle produktu na základě jejich přidružení k jednotlivé kategorii z hierarchie produktů. Tyto zděděné vlastnosti produktu lze upravit pro každý produkt za účelem splnění jednotlivých obchodních požadavků.

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a>Výběr vlastností pro aktualizaci produktů ze stránky hierarchie produktů Commerce

Tuto novou rozšířenou strukturu vlastností produktu můžete použít pro výběr aktualizovaných vlastností produktu, které je třeba odeslat k přiřazeným produktům. Na stránce **Hierarchie produktů Commerce** v podokně akcí vyberte **kategorie** a poté vyberte **aktualizovat produkty** k otevření dialogového okna **Aktualizace produktů**.

![Dialogové okno Aktualizovat produkty.](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
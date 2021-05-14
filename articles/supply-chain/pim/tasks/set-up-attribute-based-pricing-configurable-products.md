---
title: Nastavení ocenění podle atributů pro konfigurovatelné produkty
description: Toto téma vysvětluje, jak nastavit ceny na základě atributů.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921234"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Nastavení ocenění podle atributů pro konfigurovatelné produkty

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak nastavit ceny na základě atributů. Jako předpoklad musíte mít model konfigurace produktu, který má jednu nebo více komponent a atributů. Tento příklad využívá model špičkového reproduktoru v ukázkové datové společnosti USMF. Manažer produktu obvykle používá tuto proceduru.


## <a name="create-a-new-price-model"></a>Vytvoření nového cenového modelu

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
1. V seznamu vyberte řádek **Špičkový reproduktor**, ale nevybírejte odkaz pro název.
1. V podokně akcí zvolte **Model**.
1. Vyberte **Cenové modely**.
1. Zvolte **Nové**.
1. Do pole **Název cenového modelu** zadejte hodnotu. Použijte název, který usnadňuje identifikaci modelu.  
1. Zadejte hodnotu do pole **Popis**.
1. Zvolte **Uložit**.

## <a name="add-price-elements"></a>Přidání cenových prvků

1. Vyberte možnost **Upravit**. Každá komponenta v produktovém modelu u může mít element základní ceny a libovolný počet pravidel výrazu ceny. Můžete také přidat ceny v různých měnách.  
2. Zadejte hodnotu do pole **Výraz základní ceny**. Zadejte například 100. Výraz základní ceny může být číselná hodnota nebo se může skládat z aritmetického výpočtu, který zahrnuje jeden nebo více atributů.  
3. Vyberte **přidat**.
4. Do pole **Název** zadejte `Rosewood`. Název cenový výraz pomáhá určit, co představuje cenový prvek. V tomto příkladu vytváříme cenový prvek pro možnost Dokončení skříňky z růžového dřeva.  
5. Vyberte **Podmínku úpravy**. Cenové podmínky pomáhají zaručit, že prvek cenového výrazu je součástí prodejní ceny pouze v případě, že existuje určité kombinace atributů.  
6. Do pole **ConstraintBody** zadejte `CabinetFinish=="Rosewood"`.
7. Vyberte **OK**.
8. Zadejte hodnotu do pole **Výraz**. Zadejte například typ `50`. 
9. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
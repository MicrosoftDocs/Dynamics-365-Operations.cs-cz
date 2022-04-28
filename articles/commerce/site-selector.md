---
title: Modul pro výběr lokality
description: Tohle téma se zabývá modulem pro výběr lokality a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ad4d4d5f950d0631059d8f509e9e808a9106eb98
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551687"
---
# <a name="site-picker-module"></a>Modul pro výběr lokality

[!include [banner](includes/banner.md)]

Tohle téma se zabývá modulem pro výběr lokality a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Pokud má firma různé weby napříč trhy, regiony a národními prostředími, uživatelé webu potřebují snadný způsob, jak přepínat mezi lokalitami a vybrat si preferovaný nákupní web. Jako řešení tohoto scénáře umožňuje modul pro výběr lokality uživatelům procházet více webů. Nástroj pro výběr webu se také doporučuje, když [geodetekce a přesměrování](geo-detection-redirection.md) byly implementovány pro váš web elektronického obchodu, takže zákazníci mají možnost přepsat preference webu, které uvedou pomocí modulu [výběr země/oblasti](country-region-picker-module.md). 

Modul pro výběr lokality musí být nakonfigurován se seznamem webů (trhy, regiony nebo národní prostředí), které uživatelé webu mohou procházet. Následující obrázek ukazuje příklad modulu pro výběr lokality, který se nachází v záhlaví stránky webu.

![Příklad modulu pro výběr lokality v záhlaví stránky webu.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Vlastnosti modulu pro výběr lokality

| Název vlastnosti | Hodnota                 | Popis |
|---------------|-----------------------|-------------|
| Nadpis       | Text                  | Nadpis modulu. |
| Možnosti webu  | Název, obrázek, URL      | Tato vlastnost určuje název, odkaz na domovskou stránku webu a volitelný obrázek, který se má zobrazit pro každý web, který je součástí modulu. Obrázek může být vlajka nebo nějaké znázornění trhu, regionu nebo národního prostředí. |

## <a name="add-a-site-picker-module-to-a-page"></a>Přidání modulu pro výběr lokality na stránku

Modul pro výběr lokality lze přidat do pozice **Výběr lokality** [modulu záhlaví](author-header-module.md). Po přidání modulu pro výběr lokality můžete definovat možnosti záhlaví a webu modulu. Obecně je modul záhlaví obsažen ve fragmentu záhlaví, který lze sdílet na stránkách elektronického obchodu pro daný web. V následujícím příkladu byl modul pro výběr lokality přidán do pozice **Výběr lokality** modulu záhlaví, který je obsažen ve fragmentu záhlaví **HeaderContainer**.

![Příklad modulu pro výběr lokality ve fragmentu záhlaví.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul záhlaví](author-header-module.md)

[Modul popisu cesty](add-breadcrumb.md)

[Modul navigační nabídky](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

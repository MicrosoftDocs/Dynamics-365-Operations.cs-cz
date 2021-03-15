---
title: Modul volby lokality
description: Tohle téma se zabývá modulem volby lokality a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: ed00836c435bd391e5edef1f6a99889c80f45211
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985579"
---
# <a name="site-selector-module"></a>Modul volby lokality

[!include [banner](includes/banner.md)]

Tohle téma se zabývá modulem volby lokality a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Pokud má firma různé weby napříč trhy, regiony a národními prostředími, uživatelé webu potřebují snadný způsob, jak přepínat mezi lokalitami a vybrat si preferovaný nákupní web. Jako řešení tohoto scénáře umožňuje modul volby lokality uživatelům procházet více webů.

Modul volby lokality musí být nakonfigurován se seznamem webů (trhy, regiony nebo národní prostředí), které uživatelé webu mohou procházet.

> [!NOTE]
> Modul volby lokality je k dispozici v Dynamics 365 Commerce verze 10.0.14.

Následující obrázek ukazuje příklad modulu volby lokality, který se nachází v záhlaví stránky webu.

![Příklad modulu volby lokality v záhlaví stránky webu](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Vlastnosti modulu volby lokality

| Název vlastnosti | Hodnota                 | popis |
|---------------|-----------------------|-------------|
| Záhlaví       | Text                  | Nadpis modulu. |
| Možnosti webu  | Název, obrázek, URL      | Tato vlastnost určuje název, odkaz na domovskou stránku webu a volitelný obrázek, který se má zobrazit pro každý web, který je součástí modulu. Obrázek může být vlajka nebo nějaké znázornění trhu, regionu nebo národního prostředí. |

## <a name="add-a-site-selector-module-to-a-page"></a>Přidání modulu volby lokality na stránku

Modul volby lokality lze přidat do [modulu záhlaví](author-header-module.md) pod pozicí pro výběr lokality. Po přidání můžete definovat možnosti záhlaví a webu modulu.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul záhlaví](author-header-module.md)

[Modul popisu cesty](add-breadcrumb.md)

[Modul navigační nabídky](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
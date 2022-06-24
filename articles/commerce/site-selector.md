---
title: Modul pro výběr lokality
description: Tento článek se zabývá modulem pro výběr lokality a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/04/2022
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
ms.openlocfilehash: ef7753658f878fdf76c6a6beb82ce54e9c12e212
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884596"
---
# <a name="site-picker-module"></a>Modul pro výběr lokality

[!include [banner](includes/banner.md)]

Tento článek se zabývá modulem pro výběr lokality a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Pokud má firma různé weby napříč trhy, regiony a národními prostředími, uživatelé webu potřebují snadný způsob, jak přepínat mezi lokalitami a vybrat si preferovaný nákupní web. Jako řešení tohoto scénáře umožňuje modul pro výběr lokality uživatelům procházet více webů. Nástroj pro výběr webu se také doporučuje, když [geodetekce a přesměrování](geo-detection-redirection.md) byly implementovány pro váš web elektronického obchodu, takže zákazníci mají možnost přepsat preference webu, které uvedou pomocí modulu [výběr země/oblasti](country-region-picker-module.md). 

Modul pro výběr lokality musí být nakonfigurován se seznamem webů (trhy, regiony nebo národní prostředí), které uživatelé webu mohou procházet. Následující obrázek ukazuje příklad modulu pro výběr lokality, který se nachází v záhlaví stránky webu.

![Příklad modulu pro výběr lokality v záhlaví stránky webu.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Vlastnosti modulu pro výběr lokality

| Název vlastnosti | Hodnota                 | Popis |
|---------------|-----------------------|-------------|
| Nadpis       | Text                  | Nadpis modulu. |
| Možnosti webu  | Název, obrázek, URL      | Tato vlastnost určuje název, odkaz na domovskou stránku webu a volitelný obrázek, který se má zobrazit pro každý web, který je součástí modulu. Obrázek může být vlajka nebo nějaké znázornění trhu, regionu nebo národního prostředí. |

## <a name="add-a-site-picker-module-to-a-page"></a>Přidání modulu pro výběr lokality na stránku

Modul pro výběr lokality lze přidat do pozice **Výběr lokality** [modulu záhlaví](author-header-module.md). Po přidání modulu pro výběr lokality můžete definovat možnosti záhlaví a webu modulu. Obecně je modul záhlaví obsažen ve fragmentu záhlaví, který lze sdílet na stránkách elektronického obchodu pro daný web. 

Chcete-li přidat modul pro výběr lokality modulu záhlaví, postupujte takto:

1. V pozici **Výběr webu** modulu záhlaví fragmenu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** přidejte modul **Výběr webu** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností **Výběr webu** vyberte **Přidat seznam možností webu**. Zobrazí se editovatelná možnost **Seznam možností webu**.
1. Vyberte **Seznam možností webu**. Objeví se dialogové okno **Seznam možností webu**.
1. Jako **Název webu** zadejte text názvu webu, který se zobrazí v rozevíracím seznamu pro výběr webu.
1. V **Adresa URL přesměrování webu** vyberte **Přidat odkaz**. Objeví se plovoucí podokno **Přidat odkaz**.
1. V plovoucím podokně **Přidat odkaz** vyberte **Vlastní stránka** a poté vyberte **Další**.
1. Ze seznamu adres URL webu vyberte adresu URL s cestou, kterou jste vytvořili při přidávání kanálu na web (např. `www.adventure-works.com/fr-ca`) a poté vyberte **Použít**.
1. Vyberte **OK**.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Výběrem možnosti **Publikovat** publikujte stránku.

V následujícím příkladu byl modul pro výběr lokality přidán do pozice **Výběr lokality** modulu záhlaví, který je obsažen ve fragmentu záhlaví **HeaderContainer**.

![Příklad modulu pro výběr lokality ve fragmentu záhlaví.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul záhlaví](author-header-module.md)

[Modul popisu cesty](add-breadcrumb.md)

[Modul navigační nabídky](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

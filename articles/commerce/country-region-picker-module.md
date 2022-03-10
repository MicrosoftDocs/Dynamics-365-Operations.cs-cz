---
title: Modul pro výběr země/regionu
description: Toto téma se věnuje modulu výběru země/oblasti a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
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
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 1a8eebb589372051272573895a0ae5b4203eef62
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109774"
---
# <a name="countryregion-picker-module"></a>Modul pro výběr země/regionu

[!include [banner](includes/banner.md)]

Toto téma se věnuje modulu výběru země/oblasti a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.

Modul pro výběr země/oblasti používá funkci [geo detekce a přesměrování](geo-detection-redirection.md) v Dynamics 365 Commerce k zobrazení doporučených adres URL zákazníkům, kteří požadují adresu URL elektronického obchodu, která není spojena s jejich zemí nebo oblastí.

Zákazník v Kanadě například požaduje adresu URL webu, který není přidružen k Kanadě. V tomto případě modul pro výběr země/oblasti zobrazí dialogové okno s doporučením adres URL stránek spojených s Kanadou. Následující obrázek znázorňuje příklad dialogového okna pro výběr země/oblasti.

![Příklad dialogového okna pro výběr země/oblasti na domovské stránce.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Vlastnosti modulu pro výběr země/oblasti

| Název vlastnosti              | Hodnota       | popis |
| -------------------------- | ----------- | ----------- |
| Záhlaví                    | Text        | Nadpis, který se zobrazí v horní části dialogového okna. |
| Dílčí nadpis                 | Text        | Podnadpis, který se zobrazuje pod nadpisem. |
| Země: řetězec zobrazení    | Text        | Zobrazovaný název možnosti URL (například „Kanada“). |
| Země: podřetězec zobrazení | Text        | Volitelný podřetězec zobrazení pro možnost adresy URL (například „angličtina“ nebo „francouzština“). |
| Země: Obrázek země     | Mediální aktivum | Volitelný obrázek, který je přidružen k možnosti adresy URL (například obrázek kanadské vlajky). |
| Země: adresa URL země       | Text        | Adresa URL, která odpovídá kanálu a národnímu prostředí, které jsou nakonfigurovány pro zemi nebo oblast na stránce **Kanály** v nástroji Commerce site builder (**Nastavení webu \> Kanály**). Tato adresa URL se musí přesně shodovat s adresou URL, která je nakonfigurována na stránce **Kanály**. |
| Odkaz na akce                | Odkaz na akce | Volitelný odkaz, který se zobrazí v dolní části dialogového okna. Tento odkaz může například odkazovat na interní stránku, která poskytuje seznam všech zemí a oblastí, které web podporuje. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Přidání modulu pro výběr země/oblasti na stránku

Modul pro výběr země/oblasti lze přidat do modulu záhlaví buď přímo, nebo prostřednictvím sdíleného fragmentu. Další informace o modulech záhlaví viz [Modul záhlaví](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Konfigurace modulu pro výběr země/oblasti v Commerce site builderu

> [!NOTE]
> Adresy URL, které doporučujete svým zákazníkům, musí být nakonfigurovány jako objekty země v modulu pro výběr země/oblasti.

U každé adresy URL, kterou chcete zákazníkům ukázat a doporučit, postupujte v nástroji Commerce site Builder podle těchto kroků.

1. Vyberte slož modulu pro výběr země/oblasti.
1. V podokně vlastností v části **Seznam zemí** vyberte **Přidat zemi**.
1. Vyberte nové pole **Země**.
1. Do pole **Zobrazit řetězec** zadejte zobrazované jméno (např. **Kanada**).
1. Volitelné: Do pole **Zobrazit podřetězec** zadejte podřetězec zobrazení (např. **francouzština** nebo **fr-ca**).
1. Volitelné: Vyberte obrázek z knihovny médií.
1. Do pole **Adresa URL pro zemi** zadejte URL. Tato adresa URL se musí přesně shodovat s adresou URL, která se zobrazí na stránce **Kanály** a je namapována na kanál, včetně národního prostředí, které je spojeno se zemí nebo oblastí.
1. Vyberte **OK**.
1. Opakujte tyto kroky pro všechny ostatní adresy URL zemí, pro něž se má zobrazovat modul pro výběr zemí/oblastí.

## <a name="additional-resources"></a>Další prostředky

[Nastavení geografické detekce a přesměrování](geo-detection-redirection.md)

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul záhlaví](author-header-module.md)

[Modul pro výběr lokality](site-selector.md)

[Modul popisu cesty](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Modul pro výběr země/regionu
description: Toto téma se věnuje modulu výběru země/oblasti a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: stuharg
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
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 9c20e614053b7a79cf962990dbd13ca0f45d5a00
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551663"
---
# <a name="countryregion-picker-module"></a>Modul pro výběr země/regionu

[!include [banner](includes/banner.md)]

Toto téma se věnuje modulu výběru země/oblasti a popisuje, jak jej konfigurovat v řešení Microsoft Dynamics 365 Commerce.

Modul pro výběr země/oblasti používá funkci [geo detekce a přesměrování](geo-detection-redirection.md) v Dynamics 365 Commerce k zobrazení doporučených webů zákazníkům, kteří požadují adresu URL elektronického obchodu, která není spojena s jejich zemí nebo oblastí.

Zákazník v Kanadě například požaduje adresu URL webu, který je přidružen k jiné zemi, než je Kanada. V tomto případě modul pro výběr země/oblasti zobrazí dialogové okno s doporučením adres URL stránek spojených s Kanadou. 

## <a name="how-it-works"></a>Jak to funguje

Když je pro web povolena geodetekce a přesměrování a zákazník požaduje adresu URL webu, země, která je pro zákazníka zjištěna, a požadovaná adresa URL se použijí k určení, zda je tato adresa URL namapována na zemi, kde se zákazník nachází. Mapování mezi URL a zeměmi je definováno na stránce **Kanály** pod **Nastavení webu** v nástroji Commerce Site Builder. 

Pokud se adresa URL požadavku neshoduje s žádnou adresou URL, která je namapována na zemi zákazníka, v odpovědi se vrátí seznam jedné nebo více adres URL, které jsou namapovány na danou zemi. Výběr země/oblasti porovná každou adresu URL v tomto seznamu s adresami URL, které byly nakonfigurovány v modulu země/oblasti. U každé nalezené přesné shody vykreslí nástroj pro výběr země/oblasti zobrazovaný nadpis, podnadpis a obrázek pro danou adresu URL a vytvoří hypertextové odkazy na tyto prvky pomocí adresy URL.

Když zákazník vybere možnost ve výběru země/oblasti, bude přesměrován na adresu URL s hypertextovým odkazem. Tato adresa URL je zapsána do souboru cookie **\_msdyn365\_\_\_site\_**, aby jej bylo možné použít jako preferenci webu zákazníka. Když pak zákazník příště požádá o adresu URL, která není spojena s jeho zemí nebo regionem, bude automaticky přesměrován do preferované země. Proto vám doporučujeme používat také [modul pro výběr webu](site-selector.md) na vašem webu elektronického obchodu, aby zákazníci měli možnost přepsat nebo aktualizovat své preference webu. 

Pokud zákazník zavře dialogové okno pro výběr země/oblasti, nezapíše se žádný soubor cookie a zákazník zůstane na aktuálním webu. 

Následující obrázek znázorňuje příklad dialogového okna pro výběr země/oblasti.

![Příklad dialogového okna pro výběr země/oblasti na domovské stránce.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Vlastnosti modulu pro výběr země/oblasti

| Název vlastnosti              | Hodnota       | popis                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Záhlaví                    | Text        | Nadpis, který se zobrazí v horní části dialogového okna.       |
| Dílčí nadpis                 | Text        | Podnadpis, který se zobrazuje pod nadpisem.               |
| Země: řetězec zobrazení    | Text        | Zobrazovaný název možnosti URL (například „Kanada“).   |
| Země: podřetězec zobrazení | Text        | Volitelný podřetězec zobrazení pro možnost adresy URL (například „angličtina“ nebo „francouzština“). |
| Země: Obrázek země     | Mediální aktivum | Volitelný obrázek, který je přidružen k možnosti adresy URL (například obrázek kanadské vlajky). |
| Země: adresa URL země       | Text        | Adresa URL webu pro konfigurovanou zemi/oblast. Tato adresa URL se musí přesně shodovat s adresou URL, kterou jste pro tuto zemi/oblast zadali na stránce **Kanály** pod **Nastavení webu** v nástroji Commerce Site Builder. Doména adresy URL musí být navíc vlastní doménou, která je uvedena poli **Shoda domény** na stránce **Kanály**, nikoli pracovní adresa webu, který Commerce poskytuje při vytváření prostředí elektronického obchodu (např. `https://<yourcompany>.commerce.dynamics.com/`). |
| Odkaz na akce                | Odkaz na akce | Volitelný odkaz, který se zobrazí v dolní části dialogového okna. Tento odkaz může například odkazovat na interní stránku, která poskytuje seznam všech zemí a oblastí, které web podporuje. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Přidání modulu pro výběr země/oblasti na stránku

Modul pro výběr země/oblasti lze přidat do modulu záhlaví buď přímo, nebo prostřednictvím sdíleného fragmentu. Další informace o modulech záhlaví viz [Modul záhlaví](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Konfigurace modulu pro výběr země/oblasti v Commerce site builderu

> [!NOTE]
> Adresy URL, které doporučujete svým zákazníkům, musí být nakonfigurovány jako objekty země v modulu pro výběr země/oblasti.

U každé adresy URL webu, který chcete zákazníkům ukázat a doporučit, postupujte v nástroji Commerce site Builder podle těchto kroků.

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

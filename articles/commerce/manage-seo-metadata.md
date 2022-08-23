---
title: Správa metadat SEO
description: Tento článek popisuje způsob správy metadat optimalizace vyhledávačů (SEO) v aplikaci Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4b04d675a903279e667e1f5fcee387f05d979e81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276821"
---
# <a name="manage-seo-metadata"></a>Správa metadat SEO

[!include [banner](includes/banner.md)]

Tento článek popisuje způsob správy metadat optimalizace vyhledávačů (SEO) v aplikaci Microsoft Dynamics 365 Commerce.

Metadata SEO pro web lze spravovat pomocí map webů a metadat stránky.
    
## <a name="site-maps"></a>Mapy webu

Mapa webu je strojově čitelný seznam stránek na vašem webu ve formátu XML. Je určena k použití vyhledávacími weby, aby mohly poskytovat lepší výsledky hledání z vašeho webu. Mapy stránek mohou být ručně pokryty vyhledávacími stroji nebo publikovány v souboru robots. txt.

Dynamics 365 Commerce podporuje automatické generování map webu. Mapy stránek jsou při publikování a publikování stránek automaticky aktualizovány.

### <a name="turn-on-site-map-generation"></a>Zapnout generování mapy stránek

1. Přihlaste se k nástroji pro vytváření obsahu.
1. V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).
1. V navigačním podokně nalevo vyberte položku **Správa webu**.
1. Ujistěte se, že je zapnutá možnost **Mapy webů povoleno**.

## <a name="page-metadata"></a>Metadata stránky

Dynamics 365 Commerce umožňuje spravovat metadata SEO pro jednotlivé stránky. Tyto informace můžete zobrazit a upravit v oddílu **Vlastnosti SEO** kontejneru stránky. Jsou podporovány následující vlastnosti metadat SEO:

- Titul
- Popis
- Klíčová slova SEO
- Štítky standardu ARIA
- noindex
- nofollow
- noarchive
- nocache
- noOpenDirectoryProject
- nosnippet
- noImageIndex
- unavailableAfter

### <a name="modify-page-metadata"></a>Upravit metadata stránky

Chcete-li upravit metadata stránky, postupujte takto.
1. V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).
1. V navigačním podokně nalevo vyberte položku **Stránky**.
1. Vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.
1. Na příkazovém řádku vyberte možnost **Upravit**.
1. V editoru stránky v horní části ovládacího prvku obrysu stránky vlevo vyberte **Možnost režimu obrysu** (symbol ozubeného kola) a poté vyberte **Zobrazení rozšířeného obrysu**.
1. V zobrazení obrysu rozbalte ovládací prvky stromu a zobrazte obsah pozice **Záhlaví HTML**.
1. V pozici **Záhlaví HTML** vyberte požadovaný modul SEO (např. **Souhrn stránky**, **Souhrn produktové stránky**, **Přehled stránky kategorie** nebo **Metaznačky**).
1. V podokně vlastností vpravo upravte požadovaná data SEO pro vybraný modul SEO (např. **Nadpis**, **Popis** nebo **Sdílení obrázku**).
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Do pole **Komentáře** zadejte **Aktualizovaná SEO data** a pak vyberte **OK**.
1. Chcete-li zobrazit náhled stránky, vyberte volbu **Náhled**. Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.
1. Zvolte **Publikovat**.

> [!TIP]
> Autoři mohou použít **Možnost režimu obrysu** (symbol ozubeného kola) v horní části levého ovládacího prvku obrysu v editoru stránek, aby se přepínali mezi režimy **Zobrazení základního obrysu** a **Zobrazení rozšířeného obrysu**. **Zobrazení základního obrysu** je výchozí nastavení a filtruje obrys tak, že zobrazuje pouze moduly v pozici **Tělo** HTML stránky. **Zobrazení rozšířeného obrysu** zobrazuje celý modul stránky, včetně pozic **Záhlaví HTML**, **Začátek těla** a **Konec těla**. Toto zobrazení je užitečné, když autoři musí upravit konkrétní nastavení modulu SEO nebo skriptu pro stránku.

## <a name="additional-resources"></a>Další prostředky

[Úprava existující webové stránky](modify-existing-page.md)

[Přidání nové webové stránky](add-new-page.md)

[Výběr rozvržení stránky](select-page-layouts.md)

[Uložení, náhled a publikování stránky](save-preview-publish-page.md)

[Obohacení stránky produktu](enrich-product-page.md)

[Obohacení cílové stránky kategorie](enrich-category-page.md)

[Ověření přístupnosti obsahu stránky](verify-accessibility.md)

[Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

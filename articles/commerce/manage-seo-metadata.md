---
title: Správa metadat SEO
description: Toto téma popisuje způsob správy metadat optimalizace vyhledávačů (SEO) v aplikaci Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794204"
---
# <a name="manage-seo-metadata"></a>Správa metadat SEO

[!include [banner](includes/banner.md)]

Toto téma popisuje způsob správy metadat optimalizace vyhledávačů (SEO) v aplikaci Microsoft Dynamics 365 Commerce.

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
1. V podokně vlastnosti vpravo rozbalte možnost **Výchozí metatagy**.
1. Chcete-li přidat nový metatag, vyberte možnost **Přidat** a poté zadejte požadovanou značku do pole. Chcete-li odebrat existující metatag, vyberte symbol odpadkového koše napravo od něj.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Do pole **Poznámky** zadejte **Aktualizované MetaTagy** a pak vyberte **OK.**
1. Chcete-li zobrazit náhled stránky, vyberte volbu **Náhled**. Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.
1. Zvolte **Publikovat**.

## <a name="additional-resources"></a>Další zdroje

[Úprava existující webové stránky](modify-existing-page.md)

[Přidání nové webové stránky](add-new-page.md)

[Výběr rozvržení stránky](select-page-layouts.md)

[Uložení, náhled a publikování stránky](save-preview-publish-page.md)

[Obohacení stránky produktu](enrich-product-page.md)

[Obohacení cílové stránky kategorie](enrich-category-page.md)

[Ověření přístupnosti obsahu stránky](verify-accessibility.md)

[Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

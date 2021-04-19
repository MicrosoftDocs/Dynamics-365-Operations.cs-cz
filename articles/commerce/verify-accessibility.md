---
title: Ověření přístupnosti obsahu stránky
description: Toto téma popisuje, jak ověřit přístupnost obsahu stránky v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791624"
---
# <a name="verify-page-content-accessibility"></a>Ověření přístupnosti obsahu stránky

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak ověřit přístupnost obsahu stránky v Microsoft Dynamics 365 Commerce.

Po dokončení změn stránky byste měli zajistit, aby byl obsah přístupný všem uživatelům na webu. V nástrojích pro vytváření obchodních společností můžete snadno ověřit přístupnost obsahu stránky pomocí integrované služby [Microsoft Accessibility Insights](https://accessibilityinsights.io/). Tato služba ověřuje obsah stránky podle nejnovějších pokynů pro usnadnění přístupu [konsorcia W3C (World Wide Web Consortium)](https://www.w3.org/standards/webdesign/accessibility).

Integrace [Microsoft Accessibility Insights](https://accessibilityinsights.io/) musí být zapnuta na úrovni klienta nebo webu před použitím.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Zapněte Microsoft Accessibility Insights pro všechny weby v klientovi.

Chcete-li zapnout integraci [Microsoft Accessibility Insights](https://accessibilityinsights.io/) pro všechny weby Commerce ve vašem klientovi, postupujte následovně.

> [!NOTE]
> Chcete-li získat přístup k nastavení klienta, musíte být přihlášen ke Commerce jako správce systému.

1. Přihlaste se k Commerce jako správce systému.
1. V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.
1. V části **Nastavení klienta** vyberte **Funkce**.
1. Nastavte možnost **Kontrola dostupnosti** na **Zapnuto**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Zapnout Microsoft Accessibility Insights pro jeden web

Chcete-li zapnout integraci [Microsoft Accessibility Insights](https://accessibilityinsights.io/) pro jeden web Commerce, postupujte následovně.

1. V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).
1. V levém navigačním podokně vyberte **Nastavení webu** a rozbalte je.
1. V části **nastavení webu** vyberte **Funkce**.
1. Nastavte možnost **Kontrola dostupnosti** na **Zapnuto**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Ověření dostupnosti obsahu na domovské stránce

Chcete-li použít službu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) k prohledání a ověření obsahu domovské stránky v Commerce, postupujte podle následujících kroků.

1. V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).
1. V levém navigačním podokně vyberte položku **Stránky**.
1. Vyhledejte a vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.
1. Na příkazovém řádku vyberte možnost **Zkontrolovat dostupnost**. Zobrazí se stránka **Zkontrolovat dostupnost**.
1. Po dokončení skenování si prohlédněte obsah sestavy.
1. Pokud se některé kontroly nezdařily, vyberte každou nezdařené kontrolní položku a rozbalte ji tak, aby bylo možné zobrazit další podrobnosti.
1. Chcete-li sestavu po dokončení revize zavřít, posuňte se na konec stránky **Zkontrolovat dostupnost** a vyberte **OK**.

## <a name="additional-resources"></a>Další zdroje

[Úprava existující webové stránky](modify-existing-page.md)

[Přidání nové webové stránky](add-new-page.md)

[Výběr rozvržení stránky](select-page-layouts.md)

[Správa metadat SEO](manage-seo-metadata.md)

[Uložení, náhled a publikování stránky](save-preview-publish-page.md)

[Obohacení stránky produktu](enrich-product-page.md)

[Obohacení cílové stránky kategorie](enrich-category-page.md)

[Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Zvažování optimalizace webového vyhledávače pro váš web
description: Toto téma obsahuje informace o optimalizaci webového vyhledávače (SEO) pro váš web od rozvoje do výroby.
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 2f90581766dba3d3a671df52ec08339a1a0fd7dc
ms.sourcegitcommit: 9dd2d32fc303023a509d58ec7b5935f89d1e9c6d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/26/2022
ms.locfileid: "8806398"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Zvažování optimalizace webového vyhledávače (SEO) pro váš web


[!include [banner](includes/banner.md)]

Toto téma obsahuje informace o optimalizaci webového vyhledávače (SEO) pro váš web od rozvoje do výroby.

## <a name="a-site-that-is-under-development"></a>Web, který je ve vývoji

Aby bylo zajištěno, že vyhledávače nebudou indexovat web ve fázi vývoje, všechny stránky webu by měly mít meta tagy **noindex** a **nofollow**. Osvědčeným postupem je vytvořit fragment založený na [modulu MetaTags](metatags-module.md), který obsahuje následující záznam metaznačky, a zajistit, aby byl fragment přidán do části HTML \<head\> všech šablon používaných na vašem webu.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Předběžné spuštění webu

Během "předběžných spuštění" je webová stránka k dispozici pro omezenou cílovou skupinu nebo trh před tím, než dojde k úplnému spuštění. Pokud provedete předběžné spuštění vašeho webu, měli byste ponechat metaznačku **noindex** na místě. Tímto způsobem vám pomůže zaručit, že měkká spuštění zůstanou omezena na posluchače, kterých chcete dosáhnout.

## <a name="a-site-that-is-in-production"></a>Web, který je ve výrobě

Pokud je web ve výrobě, ujistěte se, že jsou všechny stránky webu správně označeny. Microsoft Dynamics 365 Commerce používá informace zadané pro stránku k vykreslení všech informací SEO na dané stránce. Následující moduly poskytují tuto funkci: souhrn stránek kategorií, souhrn stránek seznamů a souhrn stránky produktu.

Chcete-li optimalizovat indexování vyhledávače, vykreslovací systém používá obě informace z vlastností SEO, které jsou konfigurovány v Dynamics 365 Commerce a v informacích specifických pro modul. U webu, které je ve výrobě, se ujistěte, že soubor robots.txt umožňuje indexovat celý web a obsahuje odkazy na váš publikovaný dokument mapy webu. Měli byste zapnout funkci generování mapy webu na **Nastavení webu \> Mapy webů povoleny**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Nastavení SEO stránky pro interní náhled, omezené cílové skupiny a všechny cílové skupiny

Vzhledem k tomu, že aplikace Dynamics 365 Commerce podporuje ověřené náhledy (WYSIWYG) ve vizuálním tvůrci stránek, autoři můžou připravovat obsah stránky, aniž by se museli obávat, že tyto informace budou návštěvníkům webu viditelné. Pokud musí být stránka publikována, ale je nutné omezit její expozici, měla by mít metaznačku **noindex**, aby nebyla indexována vyhledávacími moduly. Poté, co je stránka připravena pro všechny cílové skupiny, by měla být k dispozici všechna základní metadata SEO, aby se maximalizovala efektivita indexování vyhledávacího modulu. Kromě toho by měla být odebrána metaznačka **noindex**.

## <a name="additional-resources"></a>Další prostředky

[Správa uživatelů a rolí elektronického obchodu](manage-ecommerce-users-roles.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)

[Správa zásad zabezpečení obsahu (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

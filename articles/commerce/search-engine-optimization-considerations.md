---
title: Zvažování optimalizace webového vyhledávače pro váš web
description: Toto téma obsahuje informace o optimalizaci webového vyhledávače (SEO) pro váš web od rozvoje do výroby.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6ffc772addb330abe7205007662a3f3e08a3e47f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410866"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Zvažování optimalizace webového vyhledávače pro váš web


[!include [banner](includes/banner.md)]

Toto téma obsahuje informace o optimalizaci webového vyhledávače (SEO) pro váš web od rozvoje do výroby.

## <a name="a-site-that-is-under-development"></a>Web, který je ve vývoji

Zatímco probíhá vývoj webu, všechny stránky webu by měly mít metaznačky **NOINDEX** a **NOFOLLOW** aby vyhledávače nemusely stránky indexovat a ukládat verze vývoje vašeho webu do mezipaměti. Chcete-li provést tuto konfiguraci, je nutné přidat výchozí modul metaznačky do šablony stránky webu. Výchozí vlastnosti metaznaček budou poté k dispozici v oddílu vlastnosti SEO v editoru stránek. Tyto vlastnosti lze použít ke správě metaznaček.

## <a name="soft-launch-of-a-site"></a>Předběžné spuštění webu

Během "předběžných spuštění" je webová stránka k dispozici pro omezenou cílovou skupinu nebo trh před tím, než dojde k úplnému spuštění. Pokud provedete předběžné spuštění vašeho webu, měli byste zvážit, zda nechcete mít metaznačku **NOINDEX** na místě. Tímto způsobem vám pomůže zaručit, že měkká spuštění zůstanou omezena na posluchače, kterých chcete dosáhnout.

## <a name="a-site-that-is-in-production"></a>Web, který je ve výrobě

Pokud je web ve výrobě, ujistěte se, že jsou všechny stránky webu správně označeny. Microsoft Dynamics 365 Commerce používá informace zadané pro stránku k vykreslení všech informací SEO na dané stránce. Následující moduly poskytují tuto funkci: souhrn stránek kategorií, souhrn stránek seznamů a souhrn stránky produktu.

Chcete-li optimalizovat indexování vyhledávače, vykreslovací systém používá obě informace z vlastností SEO, které jsou konfigurovány v Dynamics 365 Commerce a v informacích specifických pro modul. U webu, které je ve výrobě, se ujistěte, že soubor robots.txt umožňuje indexovat celý web a obsahuje odkazy na váš publikovaný dokument mapy webu. Měli byste zapnout funkci generování mapy webu na **Nastavení webu \> Mapy webů povoleny**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Nastavení SEO stránky pro interní náhled, omezené cílové skupiny a všechny cílové skupiny

Vzhledem k tomu, že aplikace Dynamics 365 Commerce podporuje ověřené náhledy (WYSIWYG) ve vizuálním tvůrci stránek, autoři můžou připravovat obsah stránky, aniž by se museli obávat, že tyto informace budou návštěvníkům webu viditelné. Pokud musí být stránka publikována, ale je nutné omezit její expozici, měla by mít metaznačku **NOINDEX**, aby nebyla indexována vyhledávacími moduly. Poté, co je stránka připravena pro všechny cílové skupiny, by měla být k dispozici všechna základní metadata SEO, aby se maximalizovala efektivita indexování vyhledávacího modulu. Kromě toho by měla být odebrána metaznačka **NOLIMIT**.

## <a name="additional-resources"></a>Další zdroje

[Správa uživatelů a rolí elektronického obchodu](manage-ecommerce-users-roles.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)

[Správa zásad zabezpečení obsahu (CSP)](manage-csp.md)

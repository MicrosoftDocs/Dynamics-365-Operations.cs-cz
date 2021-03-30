---
title: Přehled výchozí cílové stránky kategorie a stránky s výsledky hledání
description: Tohle téma obsahuje přehled výchozí cílové stránky kategorie a stránky výsledků hledání v řešení Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7a40df479bffdc6fdee8f0a7f64fde980cbbdbab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215714"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Přehled výchozí cílové stránky kategorie a stránky s výsledky hledání

[!include [banner](includes/banner.md)]

Tohle téma obsahuje přehled výchozí cílové stránky kategorie a stránky výsledků hledání v elektronickém obchodu Microsoft Dynamics 365 Commerce.

## <a name="default-category-landing-page"></a>Výchozí cílová stránka kategorie

Výchozí cílová stránka kategorie je stránka, na kterou jsou uživatelé webu obvykle přesměrování při výběru kategorie v navigační hierarchii. Stránka kategorie umožňuje procházení a také třídění a zpřesnění produktů zařazených do kategorií.

![Výchozí cílová stránka kategorie](./media/SimpleCategoryLandingDressCategory.png)

V horní části stránky se nachází záhlaví, ve kterém jsou zobrazeny všechny kategorie produktů, jak je vytvořitl manažer prodeje. Konfigurace je součástí konfigurace hierarchie navigace kanálu. V dolní částí stránky se nachází zápatí, které obsahuje rychlé odkazy na různá témata, která by mohla zajímat nakupujícího.

Pro kategorii jsou nezbytné následující součásti:

- **Dlaždice umístění produktu** zobrazuje produkty, které manažer prodeje definoval v kategorii jako součást konfigurace hierarchie navigace.
- **Souhr zpřesnění a voleb** jsou filtry, které poskytují počty a které lze je použít k upřesnění položek. Manažer prodeje je konfiguruje jako součást konfigurace metadat souvisejících s kategoriemi kanálů a atributy produktu.
- **Možnosti řazení** slouží návštěvníkům webu k třídění produktů. Ve výchozím nastavení jsou k dispozici následující možnosti řazení:

    - Cena – od nejnižší po nejvyšší
    - Cena – od nejvyšší po nejnižší
    - Název produktu – \[A–Z\]
    - Název produktu – \[Z–A\]
    - Hodnocení – od nejnižšího po nejvyšší
    - Hodnocení – od nejvyššího po nejnižší

- **Stránkování** umožňuje návštěvníkům webu přesun z jedné stránky výsledků kategorizovaného produktu na jinou stránku.
- **Celkový počet** udává celkový počet produktů, které jsou definovány v kategorii.

## <a name="enrich-a-category-landing-page"></a>Obohacení cílové stránky kategorie

Chcete-li, aby cílová stránka kategorie měla lépe přizpůsobené prostředí pro určitou kategorii, můžete „obohatit“ kategorii na dané cílové stránce kategorie. Můžete například přidat marketingové video a nějaký příběh kategorie, abyste získali pozornost nakupujícího. Další informace naleznete v tématu [Obohacení cílové stránky kategorie](enrich-category-page.md).

![Obohacená cílová stránka kategorie](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Automatické návrhy a stránky výsledků hledání

Uživatelé webu mohou web prozkoumat buď přechodem na kategorii z hierarchie navigace, nebo zadáním hledaného termínu do vyhledávacího pole.

Jakmile uživatelé začnou psát do vyhledávacího pole, projeví se moderní funkce automatických návrhů, které navrhují hledané termíny.

Zde jsou některé typy návrhů, které mohou být zobrazeny:

- **Klíčová slova** se používají k vyhledávání položek napříč všemi produkty, které jsou roztříděny v kanálu.
- **Produkty** poskytují přímé odkazy na stránku s podrobnostmi o produktu.
- **Návrhy vyhledávání ve vymezených kategoriích** uvádí různé kategorie a umožňují uživatelům hledat klíčové slovo v určité kategorii.

![Moderní automatické návrhy](./media/ImmersiveAutoSuggestUX.png)

Když uživatel vybere jeden z návrhů vyhledávání klíčového slova nebo ve vymezené kategorii, nebo když neexistují žádné návrhy pro hledaný termín, které zadají, budou přesměrováni na stránku s výsledky hledání. Uživatelé pak mohou procházet, třídit a upřesnit seznam výsledků hledání a vyhledat požadovanou položku.

![Cílová stránka vyhledávání](./media/SearchLanding.png)

Pro stránku výsledků hledání jsou nezbytné následující součásti:

- **Dlaždice umístění produktu** zobrazí produkty pro hledání uživatele. Ve výchozím nastavení jsou tyto dlaždice řazeny podle skóre relevantnosti cloudového vyhledávání uživatele.
- **Souhr zpřesnění a voleb** jsou filtry, které poskytují počty a které lze je použít k upřesnění položek. Manažer prodeje je konfiguruje jako součást konfigurace metadat „kategorie kanálu a atributy produktu“.
- **Možnosti řazení** slouží návštěvníkům webu k třídění produktů. Ve výchozím nastavení jsou k dispozici následující možnosti řazení:

    - Cena – od nejnižší po nejvyšší
    - Cena – od nejvyšší po nejnižší
    - Název produktu – \[A–Z\]
    - Název produktu – \[Z–A\]
    - Hodnocení – od nejnižšího po nejvyšší
    - Hodnocení – od nejvyššího po nejnižší
    - Výchozí

- **Stránkování** umožňuje návštěvníkům webu přesun z jedné stránky výsledků kategorizovaného produktu na jinou stránku.
- **Celkový počet** udává celkový počet produktů, které jsou definovány v kategorii a odpovídají kritériím hledání.

>[!NOTE]
>Tyto vyhledávací funkce využívající cloud jsou k dispozici od verze 10.0.8. Ujistěte se, že v části **Parametry velkoobchodu> Konfigurační parametry** je u položky ProductSearch.UseAzureSearch nastavena hodnota „true“. 
![Konfigurační parametry pro cloudové vyhledávání](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled hledání využívajícího cloud](cloud-powered-search-overview.md)

[Přehled domovské stránky](quick-tour-home-page.md)

[Přehled stránek s podrobnostmi o produktu](quick-tour-pdp.md)

[Přehled stránek košíku a pokladny](quick-tour-cart-checkout.md)

[Přehled stránek správy účtů](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
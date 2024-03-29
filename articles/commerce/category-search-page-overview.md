---
title: Přehled výchozí cílové stránky kategorie a stránky s výsledky hledání
description: Tento článek obsahuje přehled výchozí cílové stránky kategorie a stránky výsledků hledání v řešení Dynamics 365 Commerce.
author: ashishmsft
ms.date: 06/30/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: 1f2e4eb8825dd690f926f7f0bdfc39f1eb5fb83c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276366"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Přehled výchozí cílové stránky kategorie a stránky s výsledky hledání

[!include [banner](includes/banner.md)]

Tento článek obsahuje přehled výchozí cílové stránky kategorie a stránky výsledků hledání v elektronickém obchodu Microsoft Dynamics 365 Commerce.

## <a name="default-category-landing-page"></a>Výchozí cílová stránka kategorie

Výchozí cílová stránka kategorie je stránka, na kterou jsou uživatelé webu obvykle přesměrování při výběru kategorie v navigační hierarchii. Stránka kategorie umožňuje procházení a také třídění a zpřesnění produktů zařazených do kategorií.

![Výchozí cílová stránka kategorie.](./media/SimpleCategoryLandingDressCategory.png)

V horní části stránky se nachází záhlaví, ve kterém jsou zobrazeny všechny kategorie produktů, jak je vytvořitl manažer prodeje. Konfigurace je součástí konfigurace hierarchie navigace kanálu. V dolní částí stránky se nachází zápatí, které obsahuje rychlé odkazy na různé články, které by mohly zajímat nakupujícího.

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

- **Pokročilé možnosti řazení** slouží návštěvníkům webu k řazení produktů pomocí inteligentních kritérií. Aktivací [Doporučení produktu](product-recommendations.md) jsou dostupné následující možnosti řazení. Další informace naleznete v článku [Typy doporučení produktů](product-recommendations.md#types-of-product-recommendations).

    - Nové
    - Nejprodávanější
    - Trendy

- **Stránkování** umožňuje návštěvníkům webu přesun z jedné stránky výsledků kategorizovaného produktu na jinou stránku.
- **Celkový počet** udává celkový počet produktů, které jsou definovány v kategorii.

## <a name="enrich-a-category-landing-page"></a>Obohacení cílové stránky kategorie

Chcete-li, aby cílová stránka kategorie měla lépe přizpůsobené prostředí pro určitou kategorii, můžete „obohatit“ kategorii na dané cílové stránce kategorie. Můžete například přidat marketingové video a nějaký příběh kategorie, abyste získali pozornost nakupujícího. Další informace naleznete v tématu [Obohacení cílové stránky kategorie](enrich-category-page.md).

![Obohacená cílová stránka kategorie.](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Automatické návrhy a stránky výsledků hledání

Uživatelé webu mohou web prozkoumat buď přechodem na kategorii z hierarchie navigace, nebo zadáním hledaného termínu do vyhledávacího pole.

Jakmile uživatelé začnou psát do vyhledávacího pole, projeví se moderní funkce automatických návrhů, které navrhují hledané termíny.

Zde jsou některé typy návrhů, které mohou být zobrazeny:

- **Klíčová slova** se používají k vyhledávání položek napříč všemi produkty, které jsou roztříděny v kanálu.
- **Produkty** poskytují přímé odkazy na stránku s podrobnostmi o produktu.
- **Návrhy vyhledávání ve vymezených kategoriích** uvádí různé kategorie a umožňují uživatelům hledat klíčové slovo v určité kategorii.

![Moderní automatické návrhy.](./media/ImmersiveAutoSuggestUX.png)

Když uživatel vybere jeden z návrhů vyhledávání klíčového slova nebo ve vymezené kategorii, nebo když neexistují žádné návrhy pro hledaný termín, které zadají, budou přesměrováni na stránku s výsledky hledání. Uživatelé pak mohou procházet, třídit a upřesnit seznam výsledků hledání a vyhledat požadovanou položku.

![Cílová stránka vyhledávání.](./media/SearchLanding.png)

Pro stránku výsledků hledání jsou nezbytné následující součásti:

- **Dlaždice umístění produktu** zobrazí produkty pro hledání uživatele. Ve výchozím nastavení jsou tyto dlaždice řazeny podle skóre relevantnosti cloudového vyhledávání uživatele.
- **Souhr zpřesnění a voleb** jsou filtry, které poskytují počty a které lze je použít k upřesnění položek. Manažer prodeje je konfiguruje jako součást konfigurace metadat „kategorie kanálu a atributy produktu“.
- **Standardní možnosti řazení** slouží návštěvníkům webu k řazení produktů. Ve výchozím nastavení jsou k dispozici následující možnosti řazení:

    - Cena – od nejnižší po nejvyšší
    - Cena – od nejvyšší po nejnižší
    - Název produktu – \[A–Z\]
    - Název produktu – \[Z–A\]
    - Hodnocení – od nejnižšího po nejvyšší
    - Hodnocení – od nejvyššího po nejnižší
    - Výchozí 
    
    > [!NOTE]
    > Pokud jsou hodnoty **Pořadí zobrazení** definovány pro produkty v hierarchii navigace, řazení ve výchozím nastavení na stránce kategorie respektuje hodnoty definované v **Pořadí zobrazení**. V opačném případě bude řazení provedeno pomocí **Číslo produktu**.)
    
- **Pokročilé možnosti řazení** slouží návštěvníkům webu k řazení produktů pomocí inteligentních kritérií. Aktivací [Doporučení produktu](product-recommendations.md) jsou dostupné následující možnosti řazení. Další informace naleznete v článku [Typy doporučení produktů](product-recommendations.md#types-of-product-recommendations).

    - Nové
    - Nejprodávanější
    - Trendy

- **Stránkování** umožňuje návštěvníkům webu přesun z jedné stránky výsledků kategorizovaného produktu na jinou stránku.
- **Celkový počet** udává celkový počet produktů, které jsou definovány v kategorii a odpovídají kritériím hledání.

>[!NOTE]
>Tyto vyhledávací funkce využívající cloud jsou k dispozici od verze 10.0.8. Ujistěte se, že v části **Parametry velkoobchodu> Konfigurační parametry** je u položky ProductSearch.UseAzureSearch nastavena hodnota „true“. 
![Konfigurační parametry pro cloudové vyhledávání.](./media/CloudPoweredSearchConfigurationParameters.png)

>Chcete-li navíc používat pokročilé možnosti řazení, jako jsou nové, nejprodávanější a trendy, musíte aktivovat [Doporučení k produktu](product-recommendations.md) pro své prostředí. Pokročilé možnosti řazení jsou dostupné s Commerce SDK verze 9.35+ a Commerce verze 10.0.20.

## <a name="additional-resources"></a>Další prostředky

[Přehled hledání využívajícího cloud](cloud-powered-search-overview.md)

[Přehled domovské stránky](quick-tour-home-page.md)

[Přehled stránek s podrobnostmi o produktu](quick-tour-pdp.md)

[Přehled stránek košíku a pokladny](quick-tour-cart-checkout.md)

[Přehled stránek správy účtů](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

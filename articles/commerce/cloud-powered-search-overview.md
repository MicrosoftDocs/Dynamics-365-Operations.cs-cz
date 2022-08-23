---
title: Přehled vyhledávání využívajícího cloud
description: Tento článek poskytuje přehled o cloudovém vyhledávání v řešení Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 02/28/2022
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
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273659"
---
# <a name="cloud-powered-search-overview"></a>Přehled vyhledávání využívajícího cloud

[!include [banner](includes/banner.md)]

Tento článek poskytuje přehled o cloudovém vyhledávání v řešení Microsoft Dynamics 365 Commerce.

Možnost vyhledání produktu pomáhá zajistit, že zákazníci mohou snadno a rychle vyhledávat produkty pomocí procházení kategorií, vyhledávání a filtrování. Maloobchodníci považují zjišťování produktů za primární nástroj pro interakci se zákazníky napříč kanály využívajícími Cloud Scale Unit (CSU), jako je elektronický obchod a pokladní místo (POS).

Zákazníci jsou zvyklí na téměř okamžitou odezvu webových vyhledávačů, sofistikovaných webů elektronických obchodů, sociálních aplikací, automatických návrhů, které se zobrazují při zadávání hledaných podmínek, fasetové navigace a zvýrazňování. Pokud zákazníci rychle nenaleznou požadovaný produkt v jednom elektronickém obchodě, bez váhání přejdou do jiného elektronického obchodu.

Cloudové vyhledávání produktů v Commerce pomáhá maloobchodním prodejcům pokračovat v navyšování počtu udržených zákazníků a míry úspěšnosti pro všechny obsluhované jednotkou CSU.

Vyhledávání v Commerce má vylepšené funkce, které umožňují maloobchodníkům dosáhnout lepšího zjistitelnosti produktu. Tyto možnosti zároveň zajišťují škálovatelnost a výkon, které jsou potřebné pro provoz elektronického obchodu.

## <a name="browse-and-search"></a>Procházení a vyhledávání

Relevance a výkonnost vyhledávání jsou klíčovými faktory v prostředí omnikanálů, protože vyhledávání produktů spoléhá především funkce vyhledávání pro načítání informací a navigaci v obsahu. Účinné a efektivní procházení a vyhledávání pomáhá zvýšit úspěšnost.

Na následujícím obrázku je znázorněn příklad typických funkcí procházení a vyhledávání.

![Cílová stránka vyhledávání.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Souhrn fasetové navigace a voleb 

Fasetová navigace umožňuje zákazníkům snadněji procházet obsah, protože jim umožňuje filtrovat zpřesnění vyhledávání propojená s termíny v sadě termínů. Poté, co zákazník vybere a použije zpřesnění, zobrazí se přehled voleb. 

Použitím fasetové navigace můžete nakonfigurovat různá zpřesnění pro různé termíny v sadě termínů, aniž by bylo nutné vytvářet další stránky. 

Na následujícím obrázku je znázorněn příklad, ve kterém je při hledání použita fasetová navigace.

![Souhrn voleb.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Moderní automatické návrhy

Aktuální funkce automatických návrhů zobrazují klíčová slova, která spouštějí hledání odpovídajícího klíčového slova. Z důvodu nových vylepšení v Commerce mohou zákazníci často vyhledávat odkazy na produkty před tím, než dokončí zadávání.

Commerce také podporuje funkce pro shody klíčových slov v různých kategoriích. Tato funkce umožňuje zákazníkům zobrazit velké množství odpovídajících klíčových slov pro různé kategorie a spustit hledání klíčového slova v jiných kategoriích.

Na následujícím obrázku je znázorněn příklad použití moderního automatického návrhu.

![moderní automatické návrhy.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Seřadit

Funkce řazení umožňuje zákazníkům řadit, vyhledávat a procházet výsledky kategorií a zpřesnit je podle kritérií, jako je cena, název produktu a číslo produktu. Pokud aktivujete v prostředí [Doporučení produktů](product-recommendations.md), mohou zákazníci také řadit výsledky na základě pokročilých kritérií řazení, jako jsou nové, nejprodávanější a trendy.


> [!NOTE]
> Tyto vyhledávací funkce využívající cloud jsou k dispozici od verze 10.0.8. Ujistěte se, že v části **Parametry velkoobchodu> Konfigurační parametry** je u položky „ProductSearch.UseAzureSearch“ nastavena hodnota „true“. 
![Konfigurační parametry pro cloudové vyhledávání.](./media/CloudPoweredSearchConfigurationParameters.png)
>Pokročilé možnosti řazení, jako jsou nové, nejprodávanější a trendy, jsou k dispozici ve verzi Commerce SSK 9.35+ a Dynamics 365 Commerce vydání 10.0.20.  


## <a name="additional-resources"></a>Další prostředky

[Přehled výchozí cílové stránky kategorie a stránky výsledků hledání](category-search-page-overview.md)

[Správa metadat SEO](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]

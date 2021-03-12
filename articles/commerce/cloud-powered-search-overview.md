---
title: Přehled hledání využívajícího cloud
description: Toto téma poskytuje přehled o cloudovém vyhledávání v řešení Microsoft Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/29/2020
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
ms.openlocfilehash: 5a9cb82053640b7abdba420e087d0707208979de
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997643"
---
# <a name="cloud-powered-search-overview"></a>Přehled hledání využívajícího cloud


[!include [banner](includes/banner.md)]

Toto téma poskytuje přehled o cloudovém vyhledávání v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Možnost vyhledání produktu pomáhá zajistit, že zákazníci mohou snadno a rychle vyhledávat produkty pomocí procházení kategorií, vyhledávání a filtrování. Maloobchodní prodejci považují vyhledání produktu za primární nástrojem pro interakci se zákazníkem ve všech kanálech.

Zákazníci jsou zvyklí na téměř okamžitou odezvu webových vyhledávačů, sofistikovaných webů elektronických obchodů, sociálních aplikací, automatických návrhů, které se zobrazují při zadávání hledaných podmínek, fasetové navigace a zvýrazňování. Pokud zákazníci nenaleznou požadovaný produkt v jednom elektronickém obchodě, bez váhání přejdou do jiného elektronického obchodu.

Cloudové vyhledávání produktů v řešení Dynamics 365 Commerce pomáhá maloobchodním prodejcům pokračovat v navyšování počtu udržených zákazníků a míry úspěšnosti pro všechny kanály, tedy kanály elektronického obchodování a kanálů pokladních míst (POS).

Vyhledávání v řešení Dynamics 365 Commerce má vylepšené funkce, které umožňují maloobchodníkům dosáhnout lepšího zjistitelnosti produktu. Tyto možnosti zároveň zajišťují škálovatelnost a výkon, které jsou potřebné pro provoz elektronického obchodu.

## <a name="browse-and-search"></a>Procházení a vyhledávání

Relevance a výkonnost vyhledávání jsou klíčovými faktory v prostředí omnikanálů, protože vyhledávání produktů spoléhá především funkce vyhledávání pro načítání informací a navigaci v obsahu. Účinné a efektivní procházení a vyhledávání pomáhá zvýšit úspěšnost.

Na následujícím obrázku je znázorněn příklad typických funkcí procházení a vyhledávání.

![Cílová stránka vyhledávání](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Souhrn fasetové navigace a voleb 

Fasetová navigace umožňuje zákazníkům snadněji procházet obsah, protože jim umožňuje filtrovat zpřesnění vyhledávání propojená s termíny v sadě termínů. Poté, co zákazník vybere a použije zpřesnění, zobrazí se přehled voleb. 

Použitím fasetové navigace můžete nakonfigurovat různá zpřesnění pro různé termíny v sadě termínů, aniž by bylo nutné vytvářet další stránky. 

Na následujícím obrázku je znázorněn příklad, ve kterém je při hledání použita fasetová navigace.

![Souhrn voleb](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Moderní automatické návrhy

Aktuální funkce automatických návrhů pouze zobrazují klíčová slova, která spouštějí hledání odpovídajícího klíčového slova. Z důvodu nových vylepšení v Dynamics 365 Commerce mohou zákazníci často vyhledávat odkazy na produkty před tím, než dokončí zadávání.

Řešení Dynamics 365 Commerce také podporuje funkce pro shody klíčových slov v různých kategoriích. Tato funkce umožňuje zákazníkům zobrazit velké množství odpovídajících klíčových slov pro různé kategorie a spustit hledání klíčového slova v jiných kategoriích.

Na následujícím obrázku je znázorněn příklad použití moderního automatického návrhu.

![moderní automatické návrhy](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Seřadit

Rozšířené třídění v řešení Dynamics 365 Commerce umožňujě zákazníkům třídit, vyhledávat a procházet výsledky vyhledávání a zpřesnit je podle kritérií, jako je cena, název produktu a číslo produktu. Zákazníci mohou také seřadit výsledky podle toho, zda je produkt nový, nejprodávanější nebo naposledy přidaný.

>[!NOTE]
>Tyto vyhledávací funkce využívající cloud jsou k dispozici od verze 10.0.8. Ujistěte se, že v části **Parametry velkoobchodu> Konfigurační parametry** je u položky ProductSearch.UseAzureSearch nastavena hodnota „true“. 
![Konfigurační parametry pro cloudové vyhledávání](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled výchozí cílové stránky kategorie a stránky s výsledky hledání](category-search-page-overview.md)

[Správa metadat SEO](manage-seo-metadata.md)

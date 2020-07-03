---
title: Odhlášení přizpůsobených doporučení
description: V tomto tématu je vysvětleno, jak můžete zákazníkům vymezit přijetí individuálních doporučení v Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87c031c045249dbcde274d7c741beb72c3216aa8
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404272"
---
# <a name="opt-out-of-personalized-recommendations"></a>Odhlášení přizpůsobených doporučení

[!include [banner](includes/banner.md)]

V tomto tématu je vysvětleno, jak můžete zákazníkům vymezit přijetí individuálních doporučení v Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Při vytváření účtu jsou noví zákazníci automaticky nastaveni na příjem individuálních doporučení. Aplikace Dynamics 365 Commerce však poskytuje různé způsoby, jak mohou maloobchodní prodejci nechat uživatele odhlásit se z příjmu těchto doporučení a omezili zpracování jejich osobních údajů. Ověření uživatelé, kteří se odhlašují od individuálních doporučení, okamžitě zastaví zobrazování přizpůsobených seznamů. Kromě toho budou z modelů individuálních doporučení odebrány všechny osobní údaje získané pro individuální nastavení.

Další informace o povolení přizpůsobených doporučení produktů získáte v tématu [Povolení přizpůsobených doporučení produktů](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Způsoby, jak maloobchodní prodejci mohou uplatnit možnost odhlášení

Maloobchodní prodejci mají tři možnosti, jak uplatnit možnost odhlášení.

### <a name="opting-out-on-behalf-of-users"></a>Odhlášení jménem uživatelů

V modulu Správa účtu v obchodu v administrativě aplikace Commerce se maloobchodníci mohou odhlašovat jménem uživatelů.

1. Na administrativní domovské stránce hledejte **Všichni zákazníci**.
1. Vyhledejte a vyberte zákazníka a pak vyberte pevnou záložku **maloobchod**.

    ![Pevná záložka maloobchod](./media/Disablepersonalizationpart1.png)

1. V části **Ochrana osobních údajů** nastavte možnost **Zakázat individuální nastavení** na hodnotu **Ano**.

    ![Nastavení ochrany osobních údajů](./media/Disablepersonalizationpart2.png)

1. Zvolte **Uložit** a zavřete stránku.

### <a name="module-based-opt-out-experience"></a>Použití funkce odhlášení na základě modulu

Maloobchodní prodejci mohou sami umožnit ověřeným uživatelům odhlašovat individuální doporučení. Chcete-li tyto možnosti odhlášení poskytnout, přidejte do stránek profilu účtu odběratele modul odhlášení uživatele.

### <a name="custom-extensions"></a>Vlastní rozšíření

Maloobchodní prodejci mohou vytvářet svá vlastní rozšíření pro správu možnosti odhlášení pro uživatele. Další informace naleznete v tématu [Volání rozhraní API serveru](e-commerce-extensibility/call-retail-server-apis.md) a [Rozšiřitelnost online kanálu](e-commerce-extensibility/overview.md).

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Získejte digitální kopii přizpůsobených údajů doporučení jménem ověřeného uživatele

Zákazníci mohou požadovat získání digitální kopie svých osobních údajů a také zobrazit výsledky exportovaného zobrazení jejich doporučení. Pokud si tuto informaci zákazník vyžádá, musí prodejce vytvořit přizpůsobené rozšíření, které volá rozhraní API maloobchodního serveru a dotazuje se na úplné výsledky ze seznamu **Výběry pro vás**, a to na základě ID zákazníka. Výsledky mohou být exportovány ve formátu hodnot oddělených čárkami (CSV) a sdíleny se zákazníkem.

V následujícím příkladu je ukázáno, jak může maloobchodník provést tento úkol.

1. Maloobchodní prodejce vytváří vlastní rozšíření, které vybírá data osobních doporučení jménem uživatele. Informace o tom, jak vytvářet moduly, klonovat existující moduly, volat rozhraní API maloobchodního serveru a volat akce s daty, naleznete v tématu [Rozšiřitelnost online kanálu](e-commerce-extensibility/overview.md).
2. Vlastní rozšíření uskuteční volání do klíčové akce s daty **get-recommendations** a předá do ní požadované informace na základě požadavků seznamu. V případě seznamu **Výběr pro vás** je nutné, aby rozšíření předávalo správný název seznamu a ID odběratele k akci dat.

    Jedním ze způsobů, jak vytvořit vlastní rozšíření, je klonování existujícího modulu shromažďování produktů, který slouží k vrácení výsledků doporučení. Naklonováním tohoto existujícího modulu může maloobchodní prodejce změnit existující kód a přidat nové tlačítko, které exportuje výsledky doporučení do souboru CSV. Další informace naleznete v tématu [klonování modulu startovní sady](e-commerce-extensibility/clone-starter-module.md) a [Moduly kolekcí produktů](product-collection-module-overview.md).

    Chcete-li zobrazit úplné zobrazení knihovny rozhraní API maloobchodního serveru, naleznete informace v tématu [Rozhraní API zákazníka a spotřebitele maloobchodního serveru](dev-itpro/retail-server-customer-consumer-api.md).

3. Po vytvoření vlastního rozšíření může maloobchodní prodejce exportovat soubor CSV se všemi výsledky doporučení na základě jedinečného ID zákazníka ověřeného uživatele.
4. Maloobchodní prodejce může sdílet exportovaný soubor CSV, který obsahuje úplný osobní seznam doporučených produktů s ověřeným uživatelem.

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Přidání doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakce](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)

[Často kladené dotazy k doporučení produktu](faq-recommendations.md)

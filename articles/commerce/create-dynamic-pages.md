---
title: Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL
description: Tento článek popisuje, jak nastavit stránku elektronického obchodování Microsoft Dynamics 365 Commerce, která může poskytovat dynamický obsah na základě parametrů adresy URL.
author: bicyclingfool
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.openlocfilehash: 718bc099347f2924b299ccd4562d9d7055c43187
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282869"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak nastavit stránku elektronického obchodování Microsoft Dynamics 365 Commerce, která může poskytovat dynamický obsah na základě parametrů adresy URL.

Stránku elektronického obchodování lze nakonfigurovat tak, aby zobrazovala různý obsah na základě segmentu v cestě URL. Proto se stránka nazývá dynamická stránka. Segment se používá jako parametr k načtení obsahu stránky. Například stránka vytvořená v nástroji pro tvorbu webů s názvem **blog\_viewer** je namapována na adresu URL `https://fabrikam.com/blog`. Tuto stránku lze poté použít k zobrazení jiného obsahu na základě posledního segmentu v cestě URL. Například poslední segment v adrese URL `https://fabrikam.com/blog/article-1` je **article-1**.

Také můžete přepsat segment parametrizované adresy URL stránkou v nástroji pro tvorbu webů. Například stránka vytvořená v nástroji pro tvorbu webů s názvem **blog\_summary** může být namapována na adresu URL `https://fabrikam.com/blog/about-this-blog`. Je-li tato adresa URL `https://fabrikam.com/blog` požadována se segmentem `/about-this-blog` na konci, obsah stránky **blog\_summary** je vrácen namísto segmentu `/about-this-blog`, který je interpretován jako parametr, který se používá na stránce `https://fabrikam.com/blog`. 

Při výběru názvů pro parametry, které mají být předány dynamické stránce, název dynamické stránky, jak je uveden v adrese URL (`/blog` ve výše uvedeném příkladu), nelze použít jako název parametru nebo podřetězec názvu parametru. 

> [!NOTE]
> Funkce pro hostování, načítání a zobrazování dynamického obsahu stránky je implementována pomocí vlastního modulu. Další informace viz [Rozšíření online kanálu](e-commerce-extensibility/overview.md).

## <a name="set-up-a-dynamic-e-commerce-page"></a>Nastavení dynamické stránky elektronického obchodování

Chcete-li nastavit dynamickou stránku elektronického obchodování, musíte vytvořit dynamickou stránku, vytvořit základní adresu URL a nakonfigurovat cestu k dynamické stránce.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>Vytvoření stránky, která bude zobrazovat dynamický obsah

Chcete-li vytvořit stránku, která bude poskytovat dynamický obsah, postupujte podle pokynů v tématu [Prodání nové stránky webu](add-new-page.md). Stránka, kterou vytvoříte, bude vyžadovat implementaci modulu, který k načtení obsahu z externího zdroje dat použije poslední segment v cestě URL. Další informace o vývoji vlastních modulů najdete v tématu [Rozšíření online kanálu](e-commerce-extensibility/overview.md).

### <a name="create-the-base-url-for-the-dynamic-page"></a>Vytvoření základní adresy URL pro dynamickou stránku

Chcete-li vytvořit základní adresu URL pro dynamickou stránku v nástroji pro tvorbu webů Commerce, postupujte takto.

1. Přejděte na **Adresy URL** a vyberte **Nový \> Nová adresa URL**.
1. V dialogovém okně **Vytvořit novou adresu URL** vyberte **Interní stránka**. V části **Cesta URL** zadejte cestu, která bude sloužit jako kořen pro dynamickou stránku (v tomto příkladu **/blog**). Pak vyberte **Další**.
1. V dialogovém okně **Vybrat stránku** vyberte stránku, kterou jste vytvořili a která má sloužit jako dynamická stránka, a pak vyberte tlačítko **Uložit**.
1. Zvolte **Publikovat**.

### <a name="configure-the-route-to-the-dynamic-page"></a>Konfigurace cesty na dynamickou stránku

Chcete-li nakonfigurovat cestu k dynamické stránce v nástroji pro tvorbu webů Commerce, postupujte takto.

1. Přejděte na **Nastavení webu \> Rozšíření**.
1. V části **Parametrizované cesty URL** vyberte **Přidat** a poté zadejte cestu URL, kterou jste zadali při vytváření adresy URL (v tomto příkladu **/blog**).
1. Vyberte možnost **Uložit a publikovat**.

Po nakonfigurování trasy všechny požadavky na cestu parametrizované adresy URL vrátí stránku, která je přidružena k této adrese URL. Pokud nějaké požadavky obsahují další segment, vrátí se přidružená stránka a obsah stránky se načte pomocí segmentu jako parametru. Například `https://fabrikam.com/blog/article-1` vrátí stránku `https://fabrikam.com/blog` a zobrazí obsah, který načte pomocí parametru **/article-1**.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Přepsání parametrizované adresy URL vlastní stránkou

Chcete-li přepsat parametrizovanou adresu URL vlastní stránkou v nástroji pro tvorbu webů Commerce, postupujte takto.

1. Přejděte na **Adresy URL** a vyberte **Nový \> Nová adresa URL**.
1. V dialogovém okně **Vytvořit novou adresu URL** vyberte **Interní stránka**. V části **Cesta URL** zadejte cestu, která zahrnuje segment, který má být přepsán (v tomto příkladu **/blog/about-this-blog**). Pak vyberte **Další**.
1. V dialogovém okně **Vybrat stránku** vyberte vlastní stránku a poté vyberte **Uložit**.
1. Zvolte **Publikovat**.
1. Pokud vlastní stránka ještě nebyla publikována, přejděte na možnost **Stránky**, vyberte vlastní stránku a poté vyberte **Publikovat**.

Po publikování vlastní stránky se zobrazí místo dynamické stránky s parametrizovaným obsahem.

## <a name="additional-resources"></a>Další prostředky

[Úprava existující webové stránky](modify-existing-page.md)

[Přidání nové webové stránky](add-new-page.md)

[Výběr rozvržení stránky](select-page-layouts.md)

[Správa metadat SEO](manage-seo-metadata.md)

[Uložení, náhled a publikování stránky](save-preview-publish-page.md)

[Obohacení stránky produktu](enrich-product-page.md)

[Obohacení cílové stránky kategorie](enrich-category-page.md)

[Ověření přístupnosti obsahu stránky](verify-accessibility.md)

[Rozšiřitelnost online kanálu](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

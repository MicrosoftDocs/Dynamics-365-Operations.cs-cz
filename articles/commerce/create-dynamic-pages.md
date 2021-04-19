---
title: Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL
description: Toto téma popisuje, jak nastavit stránku elektronického obchodování Microsoft Dynamics 365 Commerce, která může poskytovat dynamický obsah na základě parametrů adresy URL.
author: StuHarg
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8f59b80880e6947e1b45c110df0e78d4bdd57c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795804"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak nastavit stránku elektronického obchodování Microsoft Dynamics 365 Commerce, která může poskytovat dynamický obsah na základě parametrů adresy URL.

Stránku elektronického obchodování lze nakonfigurovat tak, aby zobrazovala různý obsah na základě segmentu v cestě URL. Proto se stránka nazývá dynamická stránka. Segment se používá jako parametr k načtení obsahu stránky. Například stránka s názvem **blog\_viewer** je vytvořena a přidružena k adrese URL `https://fabrikam.com/blog`. Tuto stránku lze poté použít k zobrazení jiného obsahu na základě posledního segmentu v cestě URL. Například poslední segment v adrese URL `https://fabrikam.com/blog/article-1` je **article-1**.

Samostatné vlastní stránky, které přepisují dynamickou stránku, lze také přidružit k segmentům v cestě URL. Například stránka s názvem **blog\_summery** je vytvořena a přidružena k adrese URL `https://fabrikam.com/blog/about-this-blog`. Je-li tato adresa URL požadována, stránka **blog\_summary** stránka, která je přidružena k parametru **/about-this-blog**, je vrácena namísto stránky **blog\_viewer**.

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

Po nakonfigurování trasy všechny požadavky na cestu parametrizované adresy URL vrátí stránku, která je přidružena k této adrese URL. Pokud nějaké požadavky obsahují další segment, vrátí se přidružená stránka a obsah stránky se načte pomocí segmentu jako parametru. Například `https://fabrikam.com/blog/article-1` vrátí stránku **blog\_summary** a její obsah se načte pomocí parametru **/article-1**.

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

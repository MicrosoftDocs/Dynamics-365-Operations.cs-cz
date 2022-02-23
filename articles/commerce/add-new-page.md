---
title: Přidání nové webové stránky
description: Toto téma popisuje, jak přidat novou stránku webu v řešení Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: b0f1e290526c25aa6e6300c65e24044a325bee53
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410729"
---
# <a name="add-a-new-site-page"></a>Přidání nové webové stránky


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak přidat novou stránku webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Po vytvoření šablon a fragmentů pro váš web je dalším krokem vytváření stránek, které je používají. Než začnete, musíte vybrat šablonu nebo rozložení, název stránky a adresu URL stránky.

## <a name="template-or-layout"></a>Šablona nebo rozložení

Pro novou stránku můžete použít buď šablonu, nebo rozvržení. Další informace získáte v části [Přehled šablon a rozložení](templates-layouts-overview.md).

## <a name="page-name"></a>Název stránky

Název stránky musí být jedinečný pro vaši stránku. Měl by být názorný, aby jej bylo možné snadno najít a ostatní uživatelé věděli, pro k čemu je daná stránka určena. Název stránky vyberte pečlivě, protože jej nelze později změnit.

## <a name="page-url"></a>Adresa URL stránky

Máte možnost zadat adresu URL nové stránky. Při vytváření stránky můžete zadat řetězec, který bude použit k vytvoření úplné adresy URL. Tento řetězec je označován jako relativní adresa URL nebo jako slug adresy URL. Na základě slugu adresy URL je poté vytvořena úplná adresa URL a je jí přiřazena nová stránka. Tento slug adresy URL lze změnit později před publikováním stránky. Další informace naleznete v tématu [Vytvoření adresy URL stránky](create-page-URL.md).

> [!NOTE]
> Dynamics 365 Commerce odděluje adresy URL a obsah. Jinými slovy, lze vytvořit stránku, která není přidružena k adrese URL, a lze vytvořit adresu URL, která není přidružena ke stránce. Proto lze pro adresu URL lze prohodit obsah bez prostorů a přesměrování lze snázeji spravovat.

## <a name="add-a-new-page"></a>Přidání nové stránky

Chcete-li na svůj web přidat novou stránku webu, postupujte podle následujících kroků.

1. V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).
1. Zvolte **Nová stránka**.
1. V dialogovém okně **Nová stránka** vyberte šablonu a pak vyberte možnost **OK**.
1. Do pole **Název stránky** zadejte název stránky (například **Moje nová stránka**).
1. Do pole **Adresa URL** zadejte řetězec (slug adresy URL), čímž vytvoříte adresu URL (například **mojenovastranka**).
1. Vyberte **OK**. Zobrazí se editor stránek. Všimněte si, že záhlaví a zápatí jsou automaticky přidány na stránku na základě vybrané šablony.
1. V osnově stránky vyberte pozici **Hlavní**, vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. Vyberte **Kontejner** a potom **OK**.
1. Vyberte **Tekutý kontejner**, vyberte tlačítko se třemi tečkami a poté vyberte možnost **Přidat modul**.
1. Vyberte **Blok s formátovaným obsahem** a pak klikněte na tlačítko **OK**.
1. Vyberte **Blok s formátovaným obsahem**, vyberte tlačítko se třemi tečkami a poté vyberte možnost **Přidat modul**.
1. Vyberte **Položka bloku s formátovaným obsahem** a pak klikněte na tlačítko **OK**.
1. V podokně vlastností vpravo vyberte možnost **Odstavec** a pak v poli zadejte **Můj testovací text**.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Do pole **Poznámky** zadejte **Přidaná nová stránka** a pak vyberte **OK**.
1. Chcete-li zobrazit náhled stránky, vyberte volbu **Náhled**. Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.
1. Zvolte **Publikovat**.
1. V cestě navigace (popis cesty) vyberte **Fabrikam** (nebo název vašeho webu).
1. V navigačním podokně nalevo vyberte položku **Adresy URL**.
1. V seznamu vyhledejte a vyberte svou adresu URL (**mojenovastranka)**.
1. Zvolte **Publikovat**.

## <a name="additional-resources"></a>Další zdroje

[Úprava existující webové stránky](modify-existing-page.md)

[Výběr rozvržení stránky](select-page-layouts.md)

[Správa metadat SEO](manage-seo-metadata.md)

[Uložení, náhled a publikování stránky](save-preview-publish-page.md)

[Obohacení stránky produktu](enrich-product-page.md)

[Obohacení cílové stránky kategorie](enrich-category-page.md)

[Ověření přístupnosti obsahu stránky](verify-accessibility.md)

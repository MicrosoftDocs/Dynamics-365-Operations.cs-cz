---
title: Odeslat obrázky
description: Toto téma popisuje, jak odeslat obrázky v konfigurátoru webu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8571c52b98a87751400dab9482168ee370834bcc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096983"
---
# <a name="upload-images"></a>Odeslat obrázky

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak odeslat obrázky v konfigurátoru webu Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Knihovna médií pro konfigurátor webu Commerce umožňuje odesílat obrázky buď jednotlivě, nebo hromadně pomocí složek. Vždy byste měli odeslat verzi obrázku s nejvyšším rozlišením a kvalitou, protože komponenta pro změně velikosti obrázku automaticky optimalizuje obrázek pro různá zobrazení a jejich zarážky.

### <a name="image-information-specified-during-upload"></a>Informace o obrázku zadané při odeslání

Při odesílání obrázku lze zadat následující informace.

- **Název, alternativní text, popis, klíčová slova**: metadata obrázku nebo obrázky. Nadpis a alternativní text jsou povinné hodnoty.
- **Vybrat kategorii**:
    - **Žádná**: používá se pro obrázky příběhu e-Commerce.
    - **Produkt, kategorie, odběratel, zaměstnanec, katalog**: používá se pro multikanálové obrázky Dynamics 365 Commerce.
- **Publikovat majetek po odeslání**: Pokud je toto políčko zaškrtnuto, bude obrázek nebo obrázky publikovány ihned po odeslání.

> [!NOTE]
> Obrazové prvky s přiřazenou kategorií jsou také automaticky označeny kategorií jako klíčové slovo, které pomáhá vyhledávat majetek určité kategorie.

### <a name="naming-conventions-for-omni-channel-images"></a>Zásady vytváření názvů pro multikanálové obrázky 

Pokud jste nakonfigurovali knihovnu médií jako multikanálový obrázkový backend, můžete použít kategorie obrázků k označení kategorie, do které nahraný obrázek patří. Existuje také konvence pro vytváření názvů, která by měla být následována, aby bylo zajištěno správné načítání obrázků jinými kanály, jako je například pokladní místo (POS).

Výchozí zásady vytváření názvů se liší podle kategorie:
- Obrázky katalogu by měly mít název "**/Katalogy/\{LanguageId\}/\{CatalogName\}.jpg**"
- Obrázky kategorií by měly být pojmenované **"\{/Kategorie/\}CategoryName.** png"
- Obrázky zákazníků by měly mít název **"\{/Zákazníci/\}CustomerNumber.** jpg"
- Obrázky zaměstnanců by měly mít název **"\{/Pracovníci/\}WorkerNumber.** jpg"
- Obrázky produktu by měly mít název **"\{/Produkty/\}ProductNumber _000_001.** png"
    - 001 je posloupnost obrázku a může být 001, 002, 003, 004 nebo 005
- Obrázky variant produktu by měly mít název "**/Produkty/\{ProductNumber\}\_\{Velikost\}\_\{Barva\}\_\{Styl\}\_000_001.png**"

## <a name="upload-an-image"></a>Odeslat obrázek

Chcete-li odeslat obrázek v rámci konfigurátoru webu, postupujte podle následujících kroků.

1. V levém navigačním podokně vyberte položku **Knihovna médií**.
1. Na panelu příkazů vyberte možnost **Odeslat \> Odeslání mediálních položek**.
1. V okně Průzkumník souborů přejděte na jeden nebo více souborů s obrázky, které chcete odeslat, a vyberte možnost **Otevřít**.
1. V dialogovém okně **Odeslat mediální položku** zadejte požadovaný název a alternativní text.
1. Zadejte volitelný popis a klíčová slova a v případě potřeby vyberte kategorii. 
1. Chcete-li publikovat obrázky ihned po odeslání, zaškrtněte políčko **Publikovat mediální položky po odeslání**.
1. Vyberte **OK**.

## <a name="upload-a-folder-of-images"></a>Odeslat složku obrázků

Chcete-li hromadně odeslat složku obrázků v rámci konfigurátoru webu, postupujte podle následujících kroků.

1. V levém navigačním podokně vyberte položku **Knihovna médií**.
1. Na panelu příkazů vyberte možnost **Odeslat \> Odeslání složek**.
1. V okně Průzkumník souborů vyberte složku s obrázky, které chcete odeslat, a vyberte možnost **Otevřít**.
1. V dialogovém okně **Odeslat mediální položky** zadejte volitelná klíčová slova a v případě potřeby vyberte kategorii. 
1. Chcete-li publikovat obrázky ve složce ihned po odeslání, zaškrtněte políčko **Publikovat mediální položky po odeslání**.
1. Vyberte **OK**.

## <a name="additional-resources"></a>Další prostředky

[Přehled správy digitálního majetku](dam-overview.md)

[Odeslat video](dam-upload-video.md)

[Odeslat soubory](dam-upload-files.md)

[Oříznout obrázky](dam-crop-images.md)

[Přizpůsobit fokální místa obrázku](dam-custom-focal-point.md)
---
title: Odeslat videa
description: Toto téma popisuje, jak nahrát videa v konfigurátoru webu Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f481e5d3f323b0c86d637b67c119d13b956d5714dc0d990004834e2be05b370e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735623"
---
# <a name="upload-videos"></a>Odeslat videa

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak nahrát videa v konfigurátoru webu Microsoft Dynamics 365 Commerce.

Knihovna médií konfigurátoru webu Commerce umožňuje odesílat videozáznamy. Vždy byste měli odeslat verzi videa s nejvyšším datovým tokem a rozlišením, protože video bude automaticky konvertováno, aby bylo použitelné pro různá zobrazení a jejich zarážky.

### <a name="video-information-specified-during-upload"></a>Informace o video zadané při odeslání

Při odesílání videa lze zadat následující informace.

- **Nadpis, popis, klíčová slova**: metadata videa.
- **Automaticky generovat skryté titulky**: Určuje, zda mají být automaticky vygenerovány skryté titulky pro video (podporována je pouze angličtina). 
- **Skryté titulky**: Určuje skryté titulky, které mají být použity.
- **Normální zvuk**: Určuje běžnou zvukovou stopu, která má být použita.
- **Miniatura**: Určuje miniaturu videa. Pokud není zadána, nebude generován automaticky.
- **Popisný zvuk**: Určuje popisnou zvukovou stopu, která má být použita.

## <a name="upload-a-video"></a>Odeslat video

Chcete-li odeslat video v rámci konfigurátoru webu, postupujte podle následujících kroků.

1. V levém navigačním podokně vyberte položku **Knihovna médií**.
1. Na panelu příkazů vyberte možnost **Odeslat \> Odeslání mediálních položek**.
1. V okně Průzkumník souborů přejděte na jeden nebo více souborů s videi, které chcete odeslat, a vyberte možnost **Otevřít**.
1. V dialogovém okně **Odeslat mediální položku** zadejte požadovaný název a alternativní text.
1. Zadejte volitelný popis a klíčová slova a v případě potřeby vyberte kategorii. 
1. Chcete-li publikovat obrázky ihned po odeslání, zaškrtněte políčko **Publikovat mediální položky po odeslání**
1. Vyberte **OK**.

Pokud odesíláte více typů majetku současně (například obrázky a videozáznamy), můžete v dialogovém okně **Odeslat mediální položku** zadat pouze klíčová slova, zda mají být soubory publikovány ihned po odeslání a zda mají být automaticky vygenerovány skryté titulky pro videosoubory. Všechny majetky budou sdílet stejná klíčová slova.

## <a name="additional-resources"></a>Další prostředky

[Přehled správy digitálního majetku](dam-overview.md)

[Odeslání obrázků](dam-upload-images.md)

[Odeslat soubory](dam-upload-files.md)

[Oříznutí obrázků](dam-crop-images.md)

[Přizpůsobení ohniska obrázku](dam-custom-focal-point.md)

[Nahrání a obsloužení statických souborů](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

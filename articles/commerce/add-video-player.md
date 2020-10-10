---
title: Modul přehrávače videa
description: Tohle téma se zabývá moduly přehrávače videa a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3cf7ead9a5340d5db37a87bdf131ba87681d5a82
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817054"
---
# <a name="video-player-module"></a>Modul přehrávače videa


[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly přehrávače videa a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul přehrávače videa se používá k podpoře přehrávání videa. Lze jej přidat na libovolnou stránku za předpokladu, že se obsah videa nahrává do systému správy obsahu (CMS) a je k dispozici. Modul přehrávače videa podporuje typ média MP4.

## <a name="video-player-module"></a>Modul videopřehrávače

Modul přehrávače videa lze použít k prezentaci videí na webu elektronického obchodu. Podporuje všechny schopnosti přehrávání, jako je například přehrávání, pozastavení, režim úplné velikosti, audio popis a skryté titulky. Modul přehrávače videa podporuje také přizpůsobení skrytých titulků, které vyhovují standardům přístupnosti. Můžete například přizpůsobit velikost písma a barvu pozadí.

Modul přehrávače videa také podporuje sekundární zvukové stopy. Po nahrání videa do CMS lze také nahrát sekundární zvukovou stopu. Modul přehrávače videa pak může přehrávat sekundární zvukovou stopu, pokud ji uživatel vybere.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Příklady modulů přehrávače videa v elektronickém obchodu

- Instruktážní videa na stránkách s podrobnostmi o produktech nebo na marketingových stránkách
- Reklamní videa a videa o zásadách na marketingové stránce
- Marketingová videa se zvýrazněním charakteristik produktů na stránkách s podrobnostmi o produktech nebo na marketingových stránkách

Následující obrázek znázorňuje příklad modulu přehrávače videa na domovské stránce.

![Příklad modulu video přehrávače](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Vlastnosti modulu přehrávače videa

| Název vlastnosti         | Hodnota                               | popis |
|-----------------------|-------------------------------------|-------------|
| Automatické přehrání             | **Pravda** nebo **Nepravda**               | Je-li hodnota nastavena na **Pravda**, video se automaticky přehraje. |
| Ztlumit                  | **Pravda** nebo **Nepravda**               | Je-li hodnota nastavena na **Pravda**, zvuk je ztlumen. Pro tento přehrávač je výchozí hodnota **Nepravda**. V prohlížeči Chrome je ve výchozím nastavení ztlumeno přehrávání videozáznamů a zvuk je přehráván pouze v případě, že uživatel video přehrává ručně. |
| Smyčka                  | **Pravda** nebo **Nepravda**               | Je-li hodnota nastavena na **Pravda**, video se opakuje ve smyčce. |
| Média                 | Cesta a název souboru videa | Soubor videa, který je přehráván přehrávačem videa. |
| Přehrání na celé obrazovce       | **Pravda** nebo **nepravda**               | Je-li hodnota nastavena na **Pravda**, video se přehraje v režimu celé obrazovky. |
| Spuštění přehrání a pozastavení    | **Pravda** nebo **nepravda**               | Je-li hodnota nastavena na **Pravda**, na videu se zobrazí tlačítko Přehrát/pozastavit. |
| Ovládací prvky přehrávače videa | **Pravda** nebo **nepravda**               | Je-li tato hodnota nastavena nahodnotu **Pravda**, zobrazí se všechny ovládací prvky přehrávače videa. Tyto ovládací prvky zahrnují tlačítka Přehrát a Pozastavit, ukazatel průběhu a možnosti skrytých titulků. |
| Skrýt obrázek plakátu     | **Pravda** nebo **nepravda**               | Video může mít titulní snímek. Je-li tato vlastnost nastavena na hodnotu **Pravda**, je titulní snímek skrytý. |
| Úroveň masky            | Číslo od **0** do **100** | Maska použitá na video pro úpravu stylů. |

## <a name="add-a-video-player-module-to-a-page"></a>Přidání modulu přehrávače videa na stránku

> [!NOTE] 
> Před vytvořením modulu přehrávače videa je nejprve nutné odeslat video do knihovny médií.

Chcete-li přidat modul přehrávače videa na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona video přehrávače** a poté klikněte na tlačítko **OK**.
1. V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Video přehrávač** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte. 
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu video přehrávače, kterou jste vytvořili. V části **Název stránky** zadejte **Stránka video přehrávače** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Video přehrávač** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu video přehrávače vyberte možnost **Přidat video**.
1. V dialogovém okně **Výběr média** vyberte video a poté vyberte možnost **Odeslat novou mediální položku**.
1. V Průzkumníkovi souborů vyberte soubor videa a pak vyberte možnost **Otevřít**.
1. V dialogovém okně **Odeslat mediální položku** zadejte podle potřeby název a další informace a poté vyberte **OK**.
1. V dialogovém okně **Výběr média** vyberte možnost **Zavřít**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Na stránce by měl být zobrazen modul videa. Chcete-li přizpůsobit chování modulu, můžete změnit další nastavení.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte. 

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul propagačního banneru](add-alert.md)

[Karuselový modul](add-carousel.md)

[Modul textového bloku](add-content-rich-block.md)

[Modul bloku obsahu](add-hero-module.md)

---
title: Modul přehrávače videa
description: Tohle téma se zabývá moduly přehrávače videa a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: caf45eda4ad0e7140097cb856a6ef0a65d7ecba9
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638114"
---
# <a name="video-player-module"></a>Modul videopřehrávače

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly přehrávače videa a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul přehrávače videa se používá k podpoře přehrávání videa. Lze jej přidat na libovolnou stránku za předpokladu, že se obsah videa nahrává do systému správy obsahu (CMS) a je k dispozici. Modul přehrávače videa podporuje typ média MP4.

## <a name="video-player-module"></a>Modul videopřehrávače

Modul přehrávače videa lze použít k prezentaci videí na webu elektronického obchodu. Podporuje všechny schopnosti přehrávání, jako je například přehrávání, pozastavení, režim úplné velikosti, audio popis a skryté titulky. Modul přehrávače videa podporuje také přizpůsobení skrytých titulků, které vyhovují standardům přístupnosti. Můžete například přizpůsobit velikost písma a barvu pozadí.

Modul přehrávače videa také podporuje sekundární zvukové stopy. Po nahrání videa do CMS lze také nahrát sekundární zvukovou stopu. Modul přehrávače videa pak může přehrávat sekundární zvukovou stopu, pokud ji uživatel vybere.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Příklady modulů přehrávače videa v elektronickém obchodu

- Instruktážní videa na stránkách s podrobnostmi o produktech nebo na marketingových stránkách
- Reklamní videa a videa o zásadách na marketingové stránce
- Marketingová videa se zvýrazněním charakteristik produktů na stránkách s podrobnostmi o produktech nebo na marketingových stránkách

Následující obrázek znázorňuje příklad modulu přehrávače videa na domovské stránce.

![Příklad modulu video přehrávače.](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Vlastnosti modulu přehrávače videa

| Název vlastnosti         | Hodnota                               | popis |
|-----------------------|-------------------------------------|-------------|
| Záhlaví               | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Standardně je použita značka nadpisu **H2** pro nadpis, ale značku lze změnit, aby odpovídala požadavkům na přístupnost. |
| Formátovaný text             | Text odstavce | Modul podporuje text odstavce ve formátu RTF. Jsou podporovány některé základní funkce pro formát RTF, například hypertextové odkazy, tučné a podtržené písmo, kurzíva. Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul. |
| Připojení                  | Text odkazu, adresa URL odkazu, popisek ARIA (Accessible Rich Internet Applications) a volič **Otevřít odkaz na nové kartě** | Modul podporuje jeden nebo více odkazů „výzvy k akci“. Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA. Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění. Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě. |
| Dílčí text              | Nadpis, text nebo odkazy | Lze přidat další kontext pro modul přehrávače videa, například jméno autora nebo návrháře nebo odkazy na osobní blogy. |
| Automatické přehrání             | **Pravda** nebo **nepravda**               | Je-li hodnota nastavena na **Pravda**, video se automaticky přehraje. |
| Ztlumit                  | **Pravda** nebo **Nepravda**               | Je-li hodnota nastavena na **Pravda**, zvuk je ztlumen. Pro tento přehrávač je výchozí hodnota **Nepravda**. V prohlížeči Chrome je ve výchozím nastavení ztlumeno přehrávání videozáznamů a zvuk je přehráván pouze v případě, že uživatel video přehrává ručně. |
| Smyčka                  | **Pravda** nebo **Nepravda**               | Je-li hodnota nastavena na **Pravda**, video se opakuje ve smyčce. |
| Média                 | Cesta a název souboru videa | Soubor videa, který je přehráván přehrávačem videa. |
| Přehrání na celé obrazovce       | **Pravda** nebo **nepravda**               | Je-li hodnota nastavena na **Pravda**, video se přehraje v režimu celé obrazovky. |
| Spuštění přehrání a pozastavení    | **Pravda** nebo **nepravda**               | Je-li hodnota nastavena na **Pravda**, na videu se zobrazí tlačítko Přehrát/pozastavit. |
| Ovládací prvky přehrávače videa | **Pravda** nebo **nepravda**               | Je-li tato hodnota nastavena nahodnotu **Pravda**, zobrazí se všechny ovládací prvky přehrávače videa. Tyto ovládací prvky zahrnují tlačítka Přehrát a Pozastavit, ukazatel průběhu a možnosti skrytých titulků. |
| Skrýt obrázek plakátu     | **Pravda** nebo **nepravda**               | Video může mít titulní snímek. Je-li tato vlastnost nastavena na hodnotu **Pravda**, je titulní snímek skrytý. |
| Úroveň masky            | Číslo od **0** do **100** | Maska použitá na video pro úpravu stylů. |

> [!IMPORTANT]
> Vlastnosti **Nadpis**, **Bohatý text**, **Odkaz** a **Dílčí text** jsou k dispozici od Dynamics 365 Commerce verze 10.0.20.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]

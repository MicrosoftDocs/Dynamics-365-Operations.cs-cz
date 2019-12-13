---
title: Modul umístění obsahu
description: Tohle téma se zabývá modulem umístění obsahu a modulem položky umístění obsahu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785293"
---
# <a name="content-placement-module"></a>Modul umístění obsahu

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma se zabývá modulem umístění obsahu a modulem položky umístění obsahu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul umístění obsahu je speciální kontejner, do kterého lze umístit jiné moduly v určitém rozložení. Moduly umístění obsahu podporují následující typy modulů jako podřízené moduly: položka umístění obsahu, položka přivítání v účtu, položka objednávky účtu, položka seznamu přání účtu a položka profilu účtu.

Moduly umístění obsahu odvozují data z podřízených modulů, které podporují. Proto lze moduly umístění obsahu použít různými způsoby v závislosti na modulech, které jsou do něj přidány.

Moduly položek umístění obsahu používají obrázky i text k přezentaci promoakcí, zásad a funkcí produktu. Například modul položky umístění obsahu lze použít na domovské stránce k zobrazení zásad obchodu nebo informací o dodávce. Moduly položek umístění obsahu jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku. Lze je však použít pouze uvnitř modulu umístění obsahu.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>Příklady modulů umístění obsahu v elektronickém obchodování

* Moduly umístění obsahu, které obsahují moduly položek umístění obsahu, lze na domovské stránce nebo marketingových stránkách využít k prezentaci funkcí produktu, promoakcí, zásad obchodu, dodacích informací a dalších informací pomocí obrázků i textu.
* Moduly umístění obsahu s informacemi o modulech položek umístění obsahu mohou být použity na stránkách s podrobnostmi o produktu a prezentovat funkce produktu.
* Moduly umístění obsahu, které obsahují modul položky přivítání v účtu nebo modul položky objednávky účtu, lze použít na stránkách správy účtů.

## <a name="content-placement-module-properties"></a>Vlastnosti modulu umístění obsahu

| Název vlastnosti | Hodnota | Popis |
|---------------|-------|-------------|
| Šířka         | **Přizpůsobit kontejneru** nebo **Vyplnit obrazovku** | Je-li hodnota nastavena na **Přizpůsobit kontejneru**, budou položky uvnitř modulu umístění obsahu omezeny na jeho šířku. Je-li hodnota nastavena na **Vyplnit obrazovku**, položky nejsou omezeny na šířku modulu umístění obsahu, ale mohou přejít do režimu celé obrazovky. |

## <a name="content-placement-item-module-properties"></a>Vlastnosti modulu položky umístění obsahu

| Název vlastnosti | Hodnota | Popis |
|---------------|-------|-------------|
| Záhlaví       | Text a značky nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Každý modul položky umístění obsahu může mít nadpis. Vlastnost **Nadpis** podporuje značky nadpisů. Standardně je použita značka nadpisu **H2**, ale značku nadpisu lze změnit, aby odpovídala požadavkům na usnadnění. |
| Odstavec     | Text odstavce | Moduly položek umístění obsahu podporují text odstavce ve formátu RTF. Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo, kurzíva a hypertextové odkazy. Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul. |
| Obrázek         | Soubor obrázku | K textu může být přidružen obrázek. |
| Připojení          | Adresa URL odkazu a text odkazu | K textu lze přidat odkaz a přesměrovat uživatele na určitou stránku. |
| Velikost dlaždice     | Číslo od **1** do **12** | Tato vlastnost definuje pro každou položku umístění obsahu počet pozic, které by měla položka vyplnit v modulu umístění obsahu. Maximální velikost modulu umístění obsahu je 12 pozic. Pokud celková velikost dlaždice pro prvních *n* položek v modulu umístění obsahu překračuje 12 pozic, budou položky zalomeny na další řádek. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Přidání modulu umístění obsahu obsahujícího modul položky umístění obsahu na stránku

Chcete-li přidat modul umístění obsahu obsahující modul položky umístění obsahu na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte šablonu s názvem **Šablona umístění obsahu**.
1. V pozici **Hlavní** na výchozí stránce přidejte modul umístění obsahu.
1. V modulu umístění obsahu obsahujícího přidejte modul položky umístění obsahu.
1. Vraťte šablonu se změnami a publikujte ji.
1. Šablonu umístění obsahu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka umístění obsahu**.
1. V pozici **Hlavní** na nové stránce přidejte modul umístění obsahu.
1. V modulu umístění obsahu obsahujícího přidejte modul položky umístění obsahu.
1. V podokně vlastností pro modul položky umístění obsahu vyberte obrázek, přidejte nadpis, přidejte odstavec, přidejte odkaz, nastavte adresu URL odkazu a nastavte velikost dlaždice na **6**.
1. Zopakováním kroků 7 a 8 přidejte další položku umístění obsahu, která má stejnou velikost dlaždice.
1. Uložte stránku a zobrazte náhled. Měly by se zobrazit dvě položky umístění obsahu vedle sebe. Chcete-li dosáhnout požadovaného rozložení, můžete upravit vlastnost **Velikost dlaždice** u každého modulu položky umístění obsahu nebo přidat další moduly.
1. Vraťte stránku se změnami a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul výstrahy](add-alert.md)

[Karuselový modul](add-carousel.md)

[Modul bloku s formátovaným obsahem](add-content-rich-block.md)

[Propagační modul](add-feature-module.md)

[Modul hlavního banneru](add-hero-module.md)

[Modul přehrávače videa](add-video-player.md)

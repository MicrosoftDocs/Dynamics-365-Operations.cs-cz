---
title: Modul textového bloku
description: Tento článek se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 9e422c203d719b2e46620ce50b9d029e7ebd8d4c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270475"
---
# <a name="text-block-module"></a>Modul textového bloku

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul textového bloku je modul, který se používá k přidání textového obsahu. Tento obsah může být informativní nebo propagační.

Moduly textového bloku jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku. Jedná se o samostatné moduly, které nezávisejí na kontextu stránky ani na jiných modulech.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Příklady modulů textového bloku v elektronickém obchodování

Moduly tetových bloků lze používat následujícími způsoby:

* K prezentaci funkcí produktu na stránce s podrobnostmi o produktu.
* Pro informativní potřeby na libovolné stránce. Mohou například vysvětlit výhody věrnostních programů, popsat zásady dodávek a vrácení, odpovídat na nejčastější dotazy nebo poskytovat obsah „o nás“.
* Chcete-li přidat vlastní zprávy na stránce s podrobnostmi o produktu (například „Bezplatné poštovné u objednávek přes 1 000 Kč“).
* K zobrazení informací o právních omezeních a kontaktech na stránce s podrobnostmi o produktu, stránce košíku, stránkách pokladny a dalších stránkách (například „Dodávky a refundace podléhají zásadám obchodu“).

Následující obrázek ukazuje příklad modulu textového bloku použitého na domovské stránce.

![Příklad modulu textového bloku.](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Vlasstnosti modulu textového bloku

| Název vlastnosti     | Hodnota                                            | popis |
|-------------------|--------------------------------------------------|-------------|
| Formátovaný text         | Formátovaný text                                        | Text odstavce. Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo a kurzíva. |
| Vlastní název třídy | Název třídy Cascading Style Sheets (CSS)        | Název vlastní CSS třídy, kterou vývojář poskytuje k formátování tohoto modulu. Název třídy by měl být definován v balíku motivů. |
| Velikost písma         | **Malá**, **Střední**, **Velká** nebo **Extra velká** | Velikost písma obsahu. |

## <a name="add-a-text-block-module-to-a-page"></a>Přidání modulu textového bloku na stránku

Chcete-li přidat modul textového bloku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona obsahu**.
1. V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vyberte moduly** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Vytvořit novou stránku** v části **Název stránka** zadejte **Stránku obsahu** a poté vyberte **Další**.
1. V části **Zvolit šablonu** vyberte **Šablona obsahu** a pak vyberte **Další**.
1. V části **Vyberte rozložení** vyberte rozložení stránky (např. **Flexibilní rozložení**) a poté vyberte **Další**.
1. V části **Zkontrolovat a dokončit** zkontrolujte konfiguraci stránky. Pokud potřebujete upravit informace o stránce, vyberte **Zpět**. Pokud jsou informace o stránce správné, vyberte **Vytvořit stránku**. 
1. V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. V podokně vlastností modulu kontejner nastavte vlastnost **Šířka** na **Vyplnit kontejner**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Blok textu** a poté klikněte na tlačítko **OK**. 
1. V podokně vlastností modulu textového bloku přidejte text do pole **RTF**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul propagačního banneru](add-alert.md)

[Karuselový modul](add-carousel.md)

[Modul bloku obsahu](add-hero-module.md)

[Modul videopřehrávače](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

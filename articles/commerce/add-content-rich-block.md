---
title: Modul textového bloku
description: Tohle téma se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3926f23e4e762a49ef94ef0c8f3291e7e9a4a6a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206384"
---
# <a name="text-block-module"></a>Modul textového bloku

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Modul textového bloku je modul, který se používá k přidání textového obsahu. Tento obsah může být informativní nebo propagační.

Moduly textového bloku jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku. Jedná se o samostatné moduly, které nezávisejí na kontextu stránky ani na jiných modulech.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Příklady modulů textového bloku v elektronickém obchodování

Moduly tetových bloků lze používat následujícími způsoby:

* K prezentaci funkcí produktu na stránce s podrobnostmi o produktu.
* Pro informativní potřeby na libovolné stránce. Mohou například vysvětlit výhody věrnostních programů, popsat zásady dodávek a vrácení, odpovídat na nejčastější dotazy nebo poskytovat obsah „o nás“.
* Chcete-li přidat vlastní zprávy na stránce s podrobnostmi o produktu (například „Bezplatné poštovné u objednávek přes 1 000 Kč“).
* K zobrazení informací o právních omezeních a kontaktech na stránce s podrobnostmi o produktu, stránce košíku, stránkách pokladny a dalších stránkách (například „Dodávky a refundace podléhají zásadám obchodu“).

Následující obrázek ukazuje příklad modulu textového bloku použitého na domovské stránce.

![Příklad modulu textového bloku](./media/ecommerce-textblock.PNG)

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
1. V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona obsahu**. V části **Název stránky** zadejte **Stránka obsahu** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu kontejner nastavte vlastnost **Šířka** na **Vyplnit kontejner**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Textový blok** a poté klikněte na tlačítko **OK**. 
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
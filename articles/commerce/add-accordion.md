---
title: Modul ovládacího prvku Accordion
description: Tohle téma se zabývá moduly accordion a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ba973299291276fe48d82360e203ca28f02aaffb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796263"
---
# <a name="accordion-module"></a>Modul ovládacího prvku Accordion

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly accordion a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Moduly ovládacího prvku Accordion jsou moduly podobné kontejnerům, které slouží k uspořádání informací nebo modulů na stránce díky možnosti sbalení podobně jako u zásuvek. Modul ovládacího prvku Accordion lze použít na jakékoli stránce.

Do každého modulu ovládacího prvku Accordion lze přidat jeden nebo více modulů položky ovládacího prvku Accordion. Každý modul položky ovládacího prvku Accordion představuje sbalitelnou zásuvku. Do každého modulu položky ovládacího prvku Accordion lze přidat jeden nebo více modulů. Neexistují žádná omezení pro typy modulů, které mohou být přidány do modulu položky ovládacího prvku Accordion.

Následující obrázek znázorňuje příklad modulu ovládacího prvku Accordion, který slouží k uspořádání informací na stránce často kladených otázek (FAQ) v obchodě.

![Příklad modulu ovládacího prvku Accordion](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Vlastnosti modulu ovládacího prvku Accordion

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Nadpis | Text | Tato vlastnost určuje volitelný textový nadpis pro modul ovládacího prvku Accordion. |
| Rozbalit vše | **Pravda** nebo **nepravda** | Pokud je hodnota nastavena jako **pravda**, je zapnuta funkce rozbalení/sbalení, takže všechny položky v modulu ovládacího prvku Accordion lze rozbalit a sbalit. |
| Styl interakce | **Nezávislý** nebo **Rozbalit pouze jednu položku** | Tato vlastnost definuje styl interakce pro položky modulu ovládacího prvku Accordion. Pokud je hodnota nastavena na **Nezávislý**, lze každou položku modulu ovládacího prvku Accordion nezávisle rozbalit nebo sbalit. Pokud je hodnota nastavena na **Rozbalit pouze jednu položku**, současně lze rozbalit pouze jednu položku. Po rozbalení položek se dříve rozbalené položky sbalí. |

## <a name="accordion-item-module-properties"></a>Vlastnosti modulu položky ovládacího prvku Accordion

| Název vlastnosti | Hodnoty | popis |
|----------------|--------|-------------|
| Pozice | Text | Tato vlastnost určuje textový nadpis pro modul položky ovládacího prvku Accordion. Výběrem oblasti nadpisu mohou uživatelé sekci rozbalit nebo sbalit. |
| Rozbalit ve výchozím nastavení | **Pravda** nebo **nepravda** | Pokud je hodnota nastavena jako **pravda**, při načtení stránky se ve výchozím nastavení sbalí položka modulu ovládacího prvku Accordion. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>Přidání modulu ovládacího prvku Accordion na stránku často kladených otázek

Chcete-li přidat modul ovládacího prvku Accordion na stránku často kladených otázek a nastavit jeho vlastnosti v tvůrci webů, postupujte následujícím způsobem.

1. Přejděte na **Stránky** a pomocí marketingové šablony Fabrikam (nebo jakékoli šablony, která nemá žádná omezení) vytvořte novou pojmenovanou stránku **Často kladené otázky ohledně obchodu**.
1. V pozici **Hlavní** na **výchozí stránce** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Ovládací prvek Accordion** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu ovládacího prvku Accordion vyberte **Nadpis** vedle symbolu tužky.
1. V dialogovém okně **Nadpis** pod volbou **Text nadpisu** zadejte **Často kladené otázky**. Pak vyberte **OK**.
1. V podokně vlastností modulu ovládacího prvku Accordion zaškrtněte políčko **Rozbalit vše** a poté v poli **Styl interakce** vyberte pole **Nezávislý**.
1. V pozici **Ovládací prvek Accordion** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Položka ovládacího prvku Accordion** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu položky ovládacího prvku Accordion pod částí **Nadpis** zadejte text nadpisu (například **Jak funguje vrácení peněz?**).
1. V pozici **Položka ovládacího prvku Accordion** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Textový blok** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu textového bloku zadejte odstavec textu (například **Vratky musí být zpracovány prostřednictvím kontaktního střediska. Pro vrácení kontaktujte 1-800-FABRIKAM. Produkty mají 30denní zásadu vrácení. Vrácení musí být zahájeno v tomto časovém rámci.**).
1. V pozici **Ovládací prvek Accordion** přidejte několik dalších modulů ovládacího prvku Accordion. Do každého modulu položky ovládacího prvku Accordion přidejte modul textového bloku, který má obsah.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Na stránce se zobrazí modul ovládacího prvku Accordion s obsahem, který jste přidali.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul karty](add-tab.md)

[Modul textového bloku](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
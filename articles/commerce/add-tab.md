---
title: Modul karty
description: Tento článek se zabývá moduly karty a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 91c79ca1b70a776352ef99d854397ada34c548e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276966"
---
# <a name="tab-module"></a>Modul karty

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly karty a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Moduly karet podobně jako moduly kontejnerů slouží k uspořádání informací na stránce webu pomocí karet. Lze je použít na jakékoli stránce, kde je třeba informace prezentovat na kartách.

Do každého modulu karty lze přidat jeden nebo více modulů položek karty. Každý modul položky karty představuje jednu kartu. Do každého modulu položky karty lze přidat jeden nebo více modulů. Neexistují žádná omezení pro typy modulů, které mohou být přidány do modulu položky karty.

Následující obrázek znázorňuje příklad modulu karty na stránce webu. V tomto příkladu je vybrána karta **Expedice**.

![Příklad modulu karty.](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Vlastnosti modulu karty

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Záhlaví | Text | Tato vlastnost určuje volitelný textový nadpis pro modul karty. |
| Index aktivních karet | Počet | Tato vlastnost určuje kartu, která by měla být při načítání stránky ve výchozím nastavení aktivní. Pokud není zadána žádná hodnota, je první položka ve výchozím nastavení aktivní. |

## <a name="tab-item-module-properties"></a>Vlastnosti modulu položky karty

| Název vlastnosti | Hodnoty | popis |
|---------------|--------|-------------|
| Pozice | Text | Tato vlastnost určuje textový nadpis pro modul položky karty. |

## <a name="add-a-tab-module-to-a-page"></a>Přidání modulu karty na stránku

Chcete-li přidat modul karty na stránku a nastavit vlastnosti, postupujte následujícím způsobem.

1. Pomocí marketingové šablony Fabrikam (nebo jakékoli šablony, která nemá žádná omezení) vytvořte novou stránku s názvem **Stránka zásad obchodu**.
1. V pozici **Hlavní** na **výchozí stránce** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Kontejner** a poté klikněte na **OK**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Karta** a poté klikněte na **OK**.
1. V podokně vlastností modulu karty vyberte **Nadpis** vedle symbolu tužky.
1. V dialogovém okně **Nadpis** pod **Text nadpisu** zadejte text záhlaví (například **Zásady**). Pak vyberte **OK**.
1. V pozici **Karta** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Položka karty** a poté klikněte na **OK**.
1. V podokně vlastností modulu položky karty pod částí **Nadpis** zadejte text nadpisu (například **Dodání**).
1. V pozici **Položka karty** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Vybrat moduly** vyberte modul **Blok textu** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu textového bloku v sekci **Formátovaný text** zadejte odstavec textu.
1. V pozici **Karta** přidejte několik dalších modulů karet, které mají názvy. Do každého modulu položky karty přidejte modul textového bloku, který má obsah.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Na stránce se zobrazí modul karty, který obsahuje moduly položek karty s obsahem, který jste přidali.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul ovládacího prvku Accordion](add-accordion.md)

[Modul textového bloku](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

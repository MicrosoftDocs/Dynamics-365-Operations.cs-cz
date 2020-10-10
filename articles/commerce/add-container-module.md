---
title: Modul kontejneru
description: Tohle téma se zabývá moduly kontejneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9bb2c7d56184d009492b4aa839a3546160ad342f
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817395"
---
# <a name="container-module"></a>Modul kontejneru

[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly kontejneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul kontejneru je takový modul, který uvnitř hostuje jiné moduly. Primárním účelem modulu kontejneru je definovat pomocí vlastností, které jsou pro něj nastaveny, rozložení modulů, které obsahuje. Tyto moduly mohou být například umístěny vedle sebe ve dvou sloupcích, ve třech sloupcích, ve čtyřech sloupcích nebo v šesti sloupcích. Mohou být také omezeny na šířku kontejneru nebo mohou vyplnit obrazovku. Do každého modulu kontejneru lze také přidat nadpis.

Podporovány jsou tři moduly kontejneru: kontejner, kontejner se 2 pozicemi a kontejner se 3 pozicemi. Do těchto kontejnerů lze vložit moduly libovolného typu. 

> [!NOTE] 
> Doporučujeme, abyste do modulu kontejneru vždy vložili moduly, aby mohly být omezeny na šířku kontejneru.

## <a name="examples-of-container-modules-in-e-commerce"></a>Příklady modulů kontejneru v elektronickém obchodování

- Autor webu požaduje rozložení ve třech sloupcích, kde se tři moduly zobrazují vedle sebe. Autor webu proto používá modul kontejneru se 3 pozicemi.
- Autor webu požaduje rozložení v šesti sloupcích, kde se šest modulů zobrazuje vedle sebe. Autor webu proto používá typ kontejneru, který má uvnitř šest sloupců.
- Autor webu chce vložit modul na stránku, ale nechce, aby vyplnil obrazovku. Autor webu proto přidá do modulu kontejneru potřebný modul a nastaví vlastnost kontejneru **Šířka** na hodnotu **Přizpůsobit kontejneru**.

Následující obrázek ukazuje příklad modulu kontejneru, který obsahuje karuselový modul ve tvůrci webů Commerce. V tomto příkladu je vlastnost **Šířka** modulu kontejneru nastavena na **Vyplnit obrazovku**.

![Příklad modulu kontejneru](./media/ecommerce-container.PNG)

## <a name="container-module-properties"></a>Vlastnosti modulu kontejneru

| Název vlastnosti     | Hodnoty | popis |
|-------------------|--------|-------------|
| Záhlaví           | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Pro kontejner lze zadat volitelný nadpis. Standardně se pro značku nadpisu používá označení **H2**. Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění. |
| Šířka             | **Přizpůsobit kontejneru** nebo **Vyplnit obrazovku** | Je-li hodnota nastavena na **Přizpůsobit kontejneru** (výchozí hodnota), moduly uvnitř kontejneru jsou omezeny na šířku kontejneru. Je-li hodnota nastavena na **Vyplnit obrazovku**, moduly nejsou omezeny na šířku kontejneru, ale mohou vyplnit obrazovku. |
| Počet sloupců | **1**, **2**, **3**, **4**, **6** nebo **12** | Tato vlastnost definuje počet sloupců v kontejneru. Kontejner může mít až 12 sloupců. |

## <a name="container-with-2-slots"></a>Kontejner s 2 pozicemi

Kontejner se 2 pozicemi je optimalizován pro rozložení se dvěma sloupci. Tento typ kontejneru obsahuje dvě pozice, které umožňují zobrazení obsažených modulů vedle sebe.

Další vlastnosti lze použít k optimalizaci rozložení pro různé porty zobrazení (mobilní zařízení, tablety, počítače atd.). Pro každý port zobrazení lze definovat šířku jednotlivých sloupců. K dispozici jsou následující nastavení šířky sloupců:

- **75 % / 25 %** – První modul má šířku sloupce 75 procent a druhý modul má šířku sloupce 25 procent. K **dispozici je také** možnost 25 % / 75 %.
- **50 % / 50 %** – Oba moduly mají stejnou šířku sloupce.
- **67 % / 33 %** – První modul má šířku sloupce 67 procent a druhý modul má šířku sloupce 33 procent. K **dispozici je také** možnost 33 % / 67 %.
- **100 %** – Oba moduly mají maximální šířku sloupce. Proto jsou moduly poskládány svisle v jednom sloupci. Přestože tohle rozložení s jedním sloupcem neodpovídá záměru kontejneru se 2 pozicemi, může být vhodnější pro některé porty zobrazení (například pro velmi malé zobrazení pro mobilní zařízení).

### <a name="container-with-2-slots-properties"></a>Kontejner se 2 pozicemi

| Název vlastnosti                   | Hodnoty | Popis |
|---------------------------------|--------|-------------|
| Záhlaví                         | Text a značka nadpisu | Pro kontejner lze zadat volitelný nadpis. |
| Konfigurace portu s velmi malým zobrazením | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** nebo **100 %** | Tato vlastnost definuje rozložení pro porty s velmi malým zobrazením. |
| Konfigurace portu s malým zobrazením   | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** nebo **100 %** | Tato vlastnost definuje rozložení pro porty s malým zobrazením, například pro mobilní zařízení. |
| Konfigurace portu se středním zobrazením  | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** nebo **100 %** | Tato vlastnost definuje rozložení pro porty se středním zobrazením, například pro tablety. |
| Konfigurace portu s velkým zobrazením   | **25 % / 75 %**, **75 % / 25 %**, **50 % / 50 %**, **67 % / 33 %**, **33 % / 67 %** nebo **100 %** | Tato vlastnost definuje rozložení pro porty s velkým zobrazením, například pro počítače. |

## <a name="container-with-3-slots"></a>Kontejner s 3 pozicemi

Kontejner se 3 pozicemi je optimalizován pro rozložení se třemi sloupci.

Další vlastnosti lze použít k optimalizaci rozložení pro různé porty zobrazení. Pro každý port zobrazení lze definovat šířku jednotlivých sloupců. K dispozici jsou následující nastavení šířky sloupců:

- **33 % / 33 % / 33 %** – Všechny tři moduly mají stejnou šířku sloupce.
- **50 % / 25 % / 25 %** – První modul má šířku sloupce 50 procent a každý ze zbývajících dvou modulů má šířku sloupce 25 procent. K disozici jsou také možnosti rozložení **25 % / 50 % / 25 %** a **25 % / 25 % / 50 %**.
- **16 % / 16 % / 67 %** – První dva moduly mají šířku sloupce 16 procent a třetí modul má šířku sloupce 67 procent. K disozici jsou také možnosti rozložení **16 % / 67 % / 16 %** a **67 % / 16 % / 16 %**.

### <a name="container-with-3-slots-properties"></a>Kontejner se 3 pozicemi

| Název vlastnosti                   | Hodnoty | Popis |
|---------------------------------|--------|-------------|
| Záhlaví                         | Text a značka nadpisu | Do kontejneru lze přidat volitelný nadpis. |
| Konfigurace portu s velmi malým zobrazením | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** nebo **67 % / 16 % / 16 %** | Tato vlastnost definuje rozložení pro porty s velmi malým zobrazením. |
| Konfigurace portu s malým zobrazením   | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** nebo **67 % / 16 % / 16 %** | Tato vlastnost definuje rozložení pro porty s malým zobrazením, například pro mobilní zařízení. |
| Konfigurace portu se středním zobrazením  | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** nebo **67 % / 16 % / 16 %** | Tato vlastnost definuje rozložení pro porty se středním zobrazením, například pro tablety. |
| Konfigurace portu s velkým zobrazením   | **33 % / 33 % / 33 %**, **50 % / 25 % / 25 %**, **25 % / 50 % / 25 %**, **25 % / 25 % / 50 %**, **16 % / 16 % / 67 %**, **16 % / 67 % / 16 %** nebo **67 % / 16 % / 16 %** | Tato vlastnost definuje rozložení pro porty s velkým zobrazením, například pro počítače. |

## <a name="add-a-container-module-to-a-page"></a>Přidání modulu kontejneru na stránku

Chcete-li přidat modul kontejneru na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona kontejneru** a poté klikněte na tlačítko **OK**.
1. V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte. 
1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu video přehrávače, kterou jste vytvořili. V části **Název stránky** zadejte **Stránka kontejneru** a poté klikněte na tlačítko **OK**.
1. V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností modulu kontejneru nastavte vlastnost **Počet sloupců** na hodnotu **1** a vlastnost **Šířka** na hodnotu **Vyplnit kontejner**.
1. V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Blok obsahu** a poté klikněte na tlačítko **OK**.
1. V podokně vlastností pro modul bloku obsahu nakonfigurujte záhlaví, obrázek a rozvržení.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Měli byste vidět jeden propagační modul, který pasuje na šířku modulu kontejneru.
1. V podokně vlastností modulu kontejneru změňte hodnotu vlastnosti **Počet sloupců** na **3**.
1. Do modulu kontejneru přidejte další dva moduly bloku obsahu a nakonfigurujte je.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Nyní by měly být zobrazeny tři moduly bloku obsahu vedle sebe.
1. Poté, co dosáhnete požadovaného rozložení, vyberte **Dokončit úpravy**, čímž stránku vrátíte se změnami, a pak zvolte **Publikovat**, čímž ji publikujete.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Modul ovládacího prvku Accordion](add-accordion.md)

[Modul karty](add-tab.md)

[Karuselový modul](add-carousel.md)

[Modul textového bloku](add-content-rich-block.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)

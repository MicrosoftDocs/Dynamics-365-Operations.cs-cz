---
title: Modul bloku s formátovaným obsahem
description: Tohle téma se zabývá moduly bloků s formátovaným obsahem a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785414"
---
# <a name="content-rich-block-module"></a>Modul bloku s formátovaným obsahem

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly bloků s formátovaným obsahem a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul bloku s formátovaným obsahem je speciální kontejner, do kterého lze vložit jednu nebo více položek bloku s formátovaným obsahem. Moduly bloků s formátovaným obsahem se používají pro textový obsah na stránce. Tento obsah může být buď informativní, nebo propagační.

Moduly bloků s formátovaným obsahem jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku. Jedná se o samostatné moduly, které nezávisejí na kontextu stránky ani na jiných modulech.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>Příklady modulů bloků s formátovaným obsahem v elektronickém obchodování

Moduly bloků s formátovaným obsahem lze používat následujícími způsoby:

* K prezentaci funkcí produktu na stránce s podrobnostmi o produktu.
* Pro informativní potřeby na libovolné stránce. Mohou například vysvětlit výhody věrnostních programů, popsat zásady dodávek a vrácení, odpovídat na nejčastější dotazy nebo poskytovat obsah „o nás“.
* Chcete-li přidat vlastní zprávy na stránce s podrobnostmi o produktu (například „Bezplatné poštovné u objednávek přes 1 000 Kč“).
* K zobrazení informací o právních omezeních a kontaktech na stránce s podrobnostmi o produktu, stránce košíku, stránkách pokladny a dalších stránkách (například „Dodávky a refundace podléhají zásadám obchodu“).

## <a name="content-rich-block-module-properties"></a>Vlastnosti modulu bloku s formátovaným obsahem

| Název vlastnosti     | Hodnota                                 | Vlastnost |
|-------------------|---------------------------------------|----------|
| Počet sloupců | Číslo od **1** do **4**     | Počet sloupců v bloku s formátovaným obsahem. Může mít až čtyři sloupce. |
| Šířka             | **Vyplnit kontejner** nebo **Vyplnit obrazovku** | Je-li hodnota nastavena na **Vyplnit kontejner**, budou položky uvnitř kontejneru omezeny na jeho šířku. Je-li hodnota nastavena na **Vyplnit obrazovku**, položky nejsou omezeny na šířku kontejneru, ale mohou přejít do režimu celé obrazovky. Chcete-li dosáhnout požadovaného rozvržení, můžete změnit tuto hodnotu. |

## <a name="content-rich-block-item-module-properties"></a>Vlastnosti modulu položky bloku s formátovaným obsahem

| Název vlastnosti | Hodnota          | Popis |
|---------------|----------------|-------------|
| Odstavec     | Text odstavce | Text, který provází jednotlivé položky bloku s formátovaným obsahem. Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo a kurzíva. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Přidání modulu bloku s formátovaným obsahem na stránku

Chcete-li přidat modul bloku s formátovaným obsahem na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte šablonu stránky s názvem **Šablona obsahu**.
1. V pozici **Hlavní** na výchozí stránce přidejte modul bloku s formátovaným obsahem.
1. Vraťte šablonu se změnami a publikujte ji.
1. Šablonu obsahu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka obsahu**.
1. V pozici **Hlavní** na nové stránce přidejte modul bloku s formátovaným obsahem.
1. Ve vlastnostech modulu bloku s formátovaným obsahem nastavte počet sloupců na **2**.
1. V modulu bloku s formátovaným obsahem vyberte možnost **Přidat modul** a přidejte položku bloku s formátovaným obsahem (například **Položka1**).
1. V nové položce bloku s formátovaným obsahem přidejte text odstavce.
1. V modulu bloku s formátovaným obsahem vyberte možnost **Přidat modul** a přidejte položku bloku s formátovaným obsahem (například **Položka2**).
1. V nové položce bloku s formátovaným obsahem přidejte text odstavce.
1. Uložte stránku a zobrazte náhled změn. V zobrazení se dvěma sloupci byste měli vidět dva bloky s formátovaným textem.
1. Vraťte stránku se změnami a publikujte ji.

> [!NOTE]
> Přidáte-li třetí položku bloku s formátovaným obsahem, bude umístěna pod dvě dříve přidané položky. Změnou počtu sloupců a položek v kontejneru můžete dosáhnout různých rozložení textového obsahu.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul výstrahy](add-alert.md)

[Karuselový modul](add-carousel.md)

[Modul umístění obsahu](add-content-placement-modules.md)

[Propagační modul](add-feature-module.md)

[Modul hlavního banneru](add-hero-module.md)

[Modul přehrávače videa](add-video-player.md)


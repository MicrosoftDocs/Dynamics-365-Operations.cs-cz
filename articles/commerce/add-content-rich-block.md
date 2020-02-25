---
title: Modul textového bloku
description: Tohle téma se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025590"
---
# <a name="text-block-module"></a>Modul textového bloku


[!include [banner](includes/banner.md)]

Tohle téma se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Modul textového bloku je modul, který se používá k přidání textového obsahu. Tento obsah může být informativní nebo propagační.

Moduly textového bloku jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku. Jedná se o samostatné moduly, které nezávisejí na kontextu stránky ani na jiných modulech.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Příklady modulů textového bloku v elektronickém obchodování

Moduly tetových bloků lze používat následujícími způsoby:

* K prezentaci funkcí produktu na stránce s podrobnostmi o produktu.
* Pro informativní potřeby na libovolné stránce. Mohou například vysvětlit výhody věrnostních programů, popsat zásady dodávek a vrácení, odpovídat na nejčastější dotazy nebo poskytovat obsah „o nás“.
* Chcete-li přidat vlastní zprávy na stránce s podrobnostmi o produktu (například „Bezplatné poštovné u objednávek přes 1 000 Kč“).
* K zobrazení informací o právních omezeních a kontaktech na stránce s podrobnostmi o produktu, stránce košíku, stránkách pokladny a dalších stránkách (například „Dodávky a refundace podléhají zásadám obchodu“).

## <a name="text-block-module-properties"></a>Vlasstnosti modulu textového bloku

| Název vlastnosti     | Value                                            | Popis |
|-------------------|--------------------------------------------------|-------------|
| Formátovaný text         | Formátovaný text                                        | Text odstavce. Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo a kurzíva. |
| Vlastní název třídy | Název třídy Cascading Style Sheets (CSS)        | Název vlastní CSS třídy, kterou vývojář poskytuje k formátování tohoto modulu. Název třídy by měl být definován v balíku motivů. |
| Velikost písma         | **Malá**, **Střední**, **Velká** nebo **Extra velká** | Velikost písma obsahu. |

## <a name="add-a-text-block-module-to-a-page"></a>Přidání modulu textového bloku na stránku

Chcete-li přidat modul textového bloku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Vytvořte šablonu stránky s názvem **Šablona obsahu**. 
1. Do úseku **Tělo** přidejte modul **Výchozí stránka**.
1. Dokončete úpravy šablony a publikujte ji.
1. Šablonu obsahu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka obsahu**.
1. V úseku **Hlavní** nové stránky přidejte modul kontejneru.
1. V podokně vlastností modulu kontejner nastavte vlastnost **Šířka** na **Vyplnit kontejner**.
1. Přidejte modul textového bloku do modulu kontejneru. 
1. V podokně vlastností modulu textového bloku přidejte text do pole **RTF**.
1. Dokončete úpravy stránky a publikujte ji.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul propagačního banneru](add-alert.md)

[Karuselový modul](add-carousel.md)

[Modul bloku obsahu](add-hero-module.md)

[Modul videopřehrávače](add-video-player.md)


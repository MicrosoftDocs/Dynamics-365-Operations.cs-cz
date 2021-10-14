---
title: Omezení tabulek definovaná uživatelem nebo systémem
description: Tento článek popisuje dva typy omezení tabulky pro komponenty v modelu konfigurace produktu - definované uživatelem a systémem. Omezení tabulky představují matice povolených kombinací atributů, kde každý řádek určuje jednu sadu možných hodnot atributů.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4b484c99bc8f1cc830d4177460ec15a26714a56
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577377"
---
# <a name="system-defined-and-user-defined-table-constraints"></a>Omezení tabulek definovaná uživatelem nebo systémem

[!include [banner](../includes/banner.md)]

Tento článek popisuje dva typy omezení tabulky pro komponenty v modelu konfigurace produktu - definované uživatelem a systémem. Omezení tabulky představují matice povolených kombinací atributů, kde každý řádek určuje jednu sadu možných hodnot atributů.

Omezení tabulek představují matice kombinací atributů, které jsou povoleny pro komponenty v modelu konfigurace produktu. Každý řádek v tabulce definuje jednu sadu možných hodnoty atributů. V modelu konfigurace produktu můžete deklarovat dva typy omezení:

-   **Omezení výrazu** – vytvoření výrazu, který definuje vztahy mezi atributy, aby bylo zaručeno, že lze vybrat pouze kompatibilní hodnoty během konfigurace produktu.
-   **Omezení tabulky** – vytvoření tabulky, která definuje všechny kombinace povolené pro zadanou sadu atributů. Jsou k dispozici dva typy omezení tabulky: omezení tabulky definované uživatelem a omezení tabulky definované systémem.

Tento článek popisuje omezení tabulky definovaná uživatelem a systémem pro komponenty v modelu konfigurace produktu.

## <a name="user-defined-table-constraints"></a>Omezení tabulky definované uživatelem
Omezení tabulky definované uživatelem je typ matice, který se používá k popisu kombinací hodnot atributů, které jsou definovány pomocí typů atributů. Například pokud se vyrobí reproduktory, můžete v omezení tabulky definované uživatelem použít sloupce pro povrchovou úpravu skříně a přední mřížku. Typ atributu pro povrchovou úpravu skříně má čtyři hodnoty a typ atributu pro přední mřížku má tři hodnoty. Takže pokud omezení nejsou použita, je k dispozici 4 x 3 = 12 možných kombinací. Avšak v tomto příkladu je dovoleno pouze šest kombinací, jak je vidět v následující tabulce. Tyto informace se zobrazí na kartě **Povolené kombinace** na stránce **Upravit omezení tabulky**.

| Povrch skříňky | Přední mřížka |
|----------------|-------------|
| Černá          | Černá       |
| Černá          | Kov       |
| Dub            | Černá       |
| Palisandr       | Bílá       |
| Bílá          | Černá       |
| Bílá          | Bílá       |

Omezení tabulky definovaná uživatelem jsou definována vstupem statické tabulky, který pracuje stejně jako omezení výrazu. Při použití omezení tabulky definovaného uživatelem přináší výhodu v tom, že se tabulky často snadněji vytváří a udržují (a jsou také přehlednější) než dlouhá omezení výrazu.

## <a name="system-defined-table-constraints"></a>Omezení tabulek definovaná systémem
Omezení tabulky definované systémem vytvoří dynamické mapování mezi typem atributu a polem v tabulce. Pokud je v modelu konfigurace produktu zahrnuto omezení tabulky definované systémem, mapování zaručuje, že se v tabulce zobrazí data místo hodnot typů atributů. Výsledkem je dynamické omezení, protože obsah tabulky lze upravit (například z jiných modulů).  

Při vytváření omezení tabulky definovaného systémem vyberte tabulku, volitelně můžete definovat dotaz a potom můžete přidružit typy atributů k polím ve vybrané tabulce. Typy polí musí odpovídat typům atributů.  

Aby mohlo mít omezení tabulky vliv na model konfigurace produktu, je nutno zahrnout omezení tabulky do omezení v jedné z komponent modelu. Je třeba vytvořit nové omezení, vybrat typ omezení tabulky a poté vybrat definici omezení tabulky, kterou chcete použít. Nakonec je nutno všechna pole v omezení tabulky namapovat na atributy v modelu konfigurace produktu.

## <a name="additional-resources"></a>Další zdroje

[Přehled modelů konfigurace produktu](product-configuration-models.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
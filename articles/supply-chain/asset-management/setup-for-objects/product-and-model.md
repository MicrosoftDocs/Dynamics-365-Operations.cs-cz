---
title: Výrobci a modely majetku
description: Tento článek vysvětluje, jak nastavit výrobce majetku a související modely v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b00cb62926f3a482ec655235b6e2f5880edbcd04
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016268"
---
# <a name="asset-manufacturers-and-models"></a>Výrobci a modely majetku

[!include [banner](../../includes/banner.md)]

 

Tento článek vysvětluje, jak nastavit výrobce majetku a související modely v modulu Správa majetku. Modely mohou souviset s typy majetku.

## <a name="set-up-product-model-relations"></a>Nastavení vztahů produktů a modelů

1. Vyberte **Správa majetku** \> **Nastavení** \> **Majetek** \> **Výrobce a model**.
2. Zvolte **Nový** pro vytvoření nového produktu
3. Do pole **Výrobce** zadejte název výrobce majetku.
4. Zadejte popis do pole **Popis**.
5. Na záložce **Modely** vyberte **Přidat**, chcete-li vytvořit model majetku, který by měl souviset s výrobcem majetku.
6. Do pole **Model** zadejte název model majetku.
7. Zadejte popis do pole **Popis**.
8. V poli **Typ majetku** vyberte typ majetku, ke kterému by se měl vztahovat model výrobce.

    > [!NOTE]
    > Ve vyhledání **Typ majetku** můžete také nastavit vztahy pro typy majetku, výrobce a modely. Další informace naleznete v tématu [Typy majetku](../setup-for-objects/object-types.md).

    Na záložce **Podrobnosti** zobrazuje pole **Modely** počet modelů majetku nastavených pro vybraného výrobce majetku. Pole **Majetek** zobrazuje množství majetku, který používá vybraného výrobce.
    
    Pole **Majetek** zobrazuje počet objektů, které používají model výrobce.

> [!NOTE]
> Typ majetku nemůže mít žádné vztahy s modely výrobců majetku, může se vztahovat k jednomu modelu výrobce majetku nebo se může vztahovat k více modelům výrobců majetku. Pokud typ majetku souvisí alespoň s jedním modelem výrobce, mohou být na těchto stránkách správy majetku vybrány pouze kombinace nastavené ve vyhledávání **Model výrobce**, kde může být nastavena kombinace typu majetku, výrobce a modelu. Tyto stránky zahrnují řádky **Všechen majetek**, **Úrovně služby Majetek**, **Výchozí typy úloh** a **Rozpočet údržby**. Pokud některé typy majetku nesouvisejí s žádným modelem výrobce, na stránkách se zobrazí pouze ty typy majetku a modely výrobců, které také nemají žádný vztah k typům majetku.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Výběr výrobce a modelu na objektu

1. Vyberte **Správa majetku** \>  **_Majetek_* \> **Všechen majetek**.
2. Ve sloupci **Majetek** vyberte odkaz na majetek. Zobrazí se stránka **Podrobnosti**.
3. Vyberte možnost **Upravit**.
4. Na záložce **Obecné** vyberte hodnoty v polích **Výrobce** a **Model**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Výrobci a modely majetku
description: Toto téma vysvětluje, jak nastavit výrobce majetku a související modely v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b77605070387871335c480e25cbe23af1155d6e8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812161"
---
# <a name="asset-manufacturers-and-models"></a>Výrobci a modely majetku

[!include [banner](../../includes/banner.md)]

 

Toto téma vysvětluje, jak nastavit výrobce majetku a související modely v modulu Správa majetku. Modely mohou souviset s typy majetku.

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

1. Vyberte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek**.
2. Ve sloupci **Majetek** vyberte odkaz na majetek. Zobrazí se stránka **Podrobnosti**.
3. Vyberte možnost **Upravit**.
4. Na záložce **Obecné** vyberte hodnoty v polích **Výrobce** a **Model**.

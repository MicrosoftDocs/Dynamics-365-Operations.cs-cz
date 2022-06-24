---
title: Typy atributů údržby
description: Tento článek vysvětluje, jak vytvořit typy atributů v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a0aca3ccf24505c064ad59f0adafb771056ba95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887653"
---
# <a name="maintenance-attribute-types"></a>Typy atributů údržby

[!include [banner](../../includes/banner.md)]

 

Tento článek vysvětluje, jak vytvořit typy atributů v modulu Správa majetku. Atributy slouží k popisu vlastností různých prvků. Můžete nastavit atributy následujících prvků:

- [Typy funkčních míst](../setup-for-functional-locations/functional-location-types.md)
- [Vytvoření funkčních míst](../functional-locations/create-functional-locations.md)
- [Typy majetku](../setup-for-objects/object-types.md)
- Majetek

Atributy, které můžete nastavit, se mohou lišit v závislosti na prvku. Například pro funkční umístění můžete nastavit atributy pro konfiguraci a fyzickou velikost skladového místa. U typu majetku nebo majetku můžete nastavit atributy pro objem motoru, spotřebu energie a maximální nosnost za různých podmínek.

## <a name="create-attribute-types"></a>Tvorba typů atributů

Můžete vytvořit vlastní typy atributů. Dále je možné převést dimenze produktu na stránku **Typy atributů**.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Typy atributů**.
2. Při prvním nastavení typů atributů vyberte možnost **Vytvořit dimenze produktů**, aby se automaticky přesunuly standardní dimenze produktů.
3. Zvolte **Nový** pro vytvoření nového typu atributu.
4. Do pole **Typ atributu** zadejte název typu atributu.
5. Zadejte popis do pole **Popis**.
6. V poli **Jednotka** vyberte odpovídající jednotku atributu podle potřeby.
7. V poli **Formát datu** vyberte typ dat pro jednotku.
8. Pokud jste jako typ dat vybrali **Řetězec**, vytvořte pomocí následujících kroků hodnoty pro typ atributu:

    1. Vyberte typ atributu a pak vyberte **Hodnoty**.
    2. V poli **Hodnoty atributu** vyberte možnost **Nový**.
    3. V poli **Typ atributu** vyberte požadovaný typ atributu (dimenze).
    4. V poli **Hodnota** zadejte související hodnotu.
    5. Zadejte popis do pole **Popis**.
    6. Uložte záznam.
    7. Vraťte se na stránku **Typy atributů**.

9. Uložte záznam.

    Pole **Typy funkčních míst** zobrazuje počet funkčních míst, která používají typ atributu. Pole **Typy majetku** zobrazuje počet typů majetku, které jej používají.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
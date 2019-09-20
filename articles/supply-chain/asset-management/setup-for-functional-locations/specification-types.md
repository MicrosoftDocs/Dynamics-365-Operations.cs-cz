---
title: Typy atributů údržby
description: Toto téma vysvětluje, jak vytvořit typy atributů v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783118"
---
# <a name="maintenance-attribute-types"></a>Typy atributů údržby

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Toto téma vysvětluje, jak vytvořit typy atributů v modulu Správa majetku. Atributy slouží k popisu vlastností různých prvků. Můžete nastavit atributy následujících prvků:

- [Typy funkčních míst](../setup-for-functional-locations/functional-location-types.md)
- [Funkční místa](../functional-locations/create-functional-locations.md)
- [Typy majetku](../setup-for-objects/object-types.md)
- Prostředky

Atributy, které můžete nastavit, se mohou lišit v závislosti na prvku. Například pro funkční umístění můžete nastavit atributy pro konfiguraci a fyzickou velikost skladového místa. U typu majetku nebo majetku můžete nastavit atributy pro objem motoru, spotřebu energie a maximální nosnost za různých podmínek.

## <a name="create-attribute-types"></a>Tvorba typů atributů

Můžete vytvořit vlastní typy atributů. Dále je možné převést dimenze produktu ze Microsoft Dynamics 365 for Finance and Operations na stránku **Typů atributů**.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Typy atributů**.
2. Při prvním nastavení typů atributů vyberte možnost **Vytvořit dimenze produktů**, aby se automaticky přesunuly standardní dimenze produktů Finance and Operations.
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
---
title: Vytvoření skupiny variant
description: V tomto článku je popsán postup při vytvoření skupiny variant velikosti, stylu nebo barev pro produkt v Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a46dc9fd5cdb848818964e771d373924b217147a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874954"
---
# <a name="create-a-variant-group"></a>Vytvoření skupiny variant


[!include [banner](includes/banner.md)]

V tomto článku je popsán postup při vytvoření skupiny variant velikosti, stylu nebo barev pro produkt v Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Dynamics 365 Commerce podporuje více variant produktů. Je ideální pro nastavení skupin variant pro různé kategorie produktů. Skupinu velikostí lze například vytvořit pro trička s velikostí extra small, small, medium, large, and extra large nebo může být vytvořena skupina barev, která obsahuje všechny dostupné barvy produktu. Před přidáním produktů je třeba přidat skupiny variant.

V tomto článku bude vytvořena a konfigurována skupina velikostí. Podobné postupy lze použít pro přidání a konfiguraci skupin stylů a skupin barev.

## <a name="create-a-size-group"></a>Vytvoření skupiny velikostí

Pokud chcete vytvořit skupinu velikostí, postupujte takto.
 
1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Produkty a kategorie \> Skupiny variant \> Skupiny velikostí**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Skupiny velikostí** zadejte jedinečný název skupiny velikostí.
1. Je-li to nutné, zadejte popis do pole **Popis**.
1. V podokně akcí vyberte **Uložit**.

## <a name="add-attributes-to-the-size-group"></a>Přidání atributů do skupiny velikostí

Chcete-li přidat atributy ke skupině velikostí, postupujte takto:

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Produkty a kategorie \> Skupiny variant \> Skupiny velikostí**
1. V navigačním podokně vyberte skupinu velikostí.
1. V položce **Řádky skupiny velikostí** vyberte **Přidat**.
1. Do pole **Velikost** zadejte řetězec přestavující velikost (např. "XL").
1. Do pole **Název velikosti** zadejte název velikosti (například "Extra Large").
1. Do pole **Hmotnost doplnění** zadejte číslo představující hmotnost doplnění.
1. Do pole **číslo v čárovém kódu** zadejte číslo představující čárový kód.
1. V poli **Pořadí zobrazení** zadejte číslo pořadí zobrazení.
1. Po dokončení přidávání velikostí vyberte možnost **Uložit** v podokně akcí.

Následující obrázek znázorňuje příklad skupiny velikostí pro "velikosti volnočasových košil".

![Vytvoření skupiny velikostí.](media/create-variant-group.png)

## <a name="additional-resources"></a>Další prostředky

[Přehled informací o produktech](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Nastavení maloobchodních produktů](set-up-retail-products.md)

[Dimenze produktu](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
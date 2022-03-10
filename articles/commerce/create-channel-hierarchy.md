---
title: Vytvoření hierarchie navigace sítě
description: Toto téma popisuje, jak vytvořit hierarchie navigace kanálu v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d522838bdddf6cda6d7e451b27183f733e3de53df865d49cdadf846cf99cc953
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749948"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Vytvoření hierarchie navigace sítě


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak vytvořit hierarchie navigace kanálu v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Hierarchie navigace kanálů se používá k seskupení a uspořádání produktů do kategorií, aby je bylo možné procházet online nebo v prodejních místech (POS).

## <a name="create-a-channel-navigation-hierarchy"></a>Vytvoření hierarchie navigace sítě

Chcete-li vytvořit hierarchii navigace kanálu, postupujte následovně.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Produkty a kategorie \> Kategorie navigace kanálů**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Název** zadejte název.
1. Zadejte popis do pole **Popis**.
1. Vyberte **Vytvořit**.
1. V podokně akcí vyberte **Nový uzel kategorie** k vytvoření kořenového uzlu.
1. Do pole **Název** zadejte název.
1. Zadejte popis do pole **Popis**.
1. Do pole **Popisný název** zadejte popisný název produktu.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek znázorňuje příklad kořenového uzlu.

![Ukázkový kořenový uzel.](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Vytvoření uzlů navigačních kategorií

Chcete-li vytvořit další uzly navigační kategorie, které budou představovat kategorie produktů v kanálu, postupujte podle následujících kroků.

1. V navigačním podokně vyberte nadřazený uzel, ke kterému chcete přidat kategorii.
1. V podokně akcí vyberte možnost **Nový uzel kategorií**.
1. Do pole **Název** zadejte název.
1. Zadejte popis do pole **Popis**.
1. Do pole **Popisný název** zadejte popisný název produktu.
1. V poli **Pořadí zobrazení** zadejte pořadí zobrazení (volitelné).
1. V podokně akcí vyberte **Uložit**.

Následující obrázek znázorňuje příklad dokončené navigační hierarchie kanálů.

![Vzorová hierarchie kanálu.](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Přidat produkty do uzlů kategorií

Chcete-li přidat produkty do uzlů kategorií, postupujte podle následujících kroků.

1. Vyberte uzel kategorií.
1. Ve volbě **Produkty** vyberte **Přidat**.
1. Vyhledejte nové produkty, které chcete přidat pomocí čísla produktu nebo názvu produktu, a poté vyberte **OK**.
1. V podokně akcí vyberte **Uložit**.

> [!NOTE]
> Přidání produktů do uzlu v hierarchii navigace kanálu není dostatečné, aby se produkty na vybraném kanálu zobrazily, ale tyto produkty musí být také roztříděny do kanálu. Další informace o sortimentech naleznete v [Správa sortimentu](assortments.md).

Následující obrázek znázorňuje příklad uzlu s přidanými produkty.

![Produkty přidané do uzlu kategorií.](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Přidat skupiny atributů produktů do uzlů kategorií

> [!NOTE]
> Skupiny atributů je nutné vytvořit před jejich přidáním do uzlu v hierarchii navigace kanálu.

Přidání produktu skupiny atributů do uzlu kategorií provedete následovně.

1. Vyberte uzel kategorií.
1. Ve **Skupině atributů produktu** vyberte možnost **Přidat**.
1. Vyhledejte skupiny atributů, které chcete přidat, a poté vyberte **OK**.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek znázorňuje příklad uzlu s přidanými skupinami atributů produktů.

![Skupiny atributů produktu v uzlu.](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Další prostředky

[Nastavení sortimentu](set-up-assortments.md)

[Správa atributů a skupin atributů](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

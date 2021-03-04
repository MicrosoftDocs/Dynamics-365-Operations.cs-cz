---
title: Konfigurace kanálu pro použití hierarchie navigace sítě
description: Toto téma popisuje, jak konfigurovat kanál pro použití hierarchie navigace kanálu v aplikaci Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7b5041d35d310125c314ab2cb77d3cc40cdb7113
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410687"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Konfigurace kanálu pro použití hierarchie navigace sítě


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak konfigurovat kanál pro použití hierarchie navigace kanálu v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Hierarchie navigace kanálů uspořádá produkty do kategorií, aby je bylo možné procházet na stránkách e-Commerce nebo v prodejních místech (POS). Maloobchodní a online kanály musí být nakonfigurovány s hierarchií navigačních kanálů.

## <a name="configure-the-channel"></a>Konfigurace kanálu

Chcete-li konfigurovat kanál pro použití hierarchie navigace sítě, postupujte následovně.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.
1. Vyberte kanál, který chcete konfigurovat.
1. V podokně akcí zvolte **Nastavit metadata atributu**.
1. V rozevíracím seznamu **Hierarchie kategorií** vyberte patřičnou hierarchii navigace kanálu.
1. V podokně akcí vyberte **Uložit**.
1. V položce **Skupina atributů** přidejte všechny skupiny atributů, které budou globálními atributy pro všechny uzly.

Následující obrázek ukazuje, jak konfigurovat kanál pro použití hierarchie navigace sítě.

![Příklad konfigurace kanálu](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Nastavit metadata atributu

Nastavení metadat atributu umožní konfiguraci atributů v každém uzlu.

Pro nastavení metadat atributů postupujte následujícím způsobem.

1. V podokně akcí zvolte **Nastavit metadata atributu**.
1. Pro každý uzel vyberte **Atributy produktu kanálu**.
1. Nastavte **Zobrazit atribut na kanálu** na **Ano** a **Lze upřesnit** na **Ano**, chcete-li povolit zpřesnění na daném kanálu.
1. Po nakonfigurování každého uzlu podle potřeby vyberte v **Podokně akcí** tlačítko **Uložit**.
1. Vyberte **X** v pravém horním rohu, chcete-li ukončit tuto obrazovku a vrátit se zpět na stránku **Kategorie kanálu a atributy produktu**.

Následující obrázek znázorňuje ukázkovou sadu atributů produktu kanálu nakonfigurovaných v uzlu kategorie kanálu.

![Atributy kanálu v uzlu kategorie kanálu](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Publikovat změny

Změny se projeví až po publikování změn.

Změny se publikují tímto způsobem.

1. V podokně akcí vyberte možnost **Publikovat aktualizace kanálů**.
1. V podokně **Publikovat aktualizace kanálů** vyberte **OK**.

Následující obrázek ukazuje, jak publikovat aktualizace kanálů.

![Publikovat aktualizace kanálů](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Další zdroje

[Vytvoření hierarchie navigace sítě](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Vytvoření nové hierarchie produktu
description: Tento článek popisuje, jak vytvořit novou hierarchii produktů v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 54a29381bb9231766d76b653904339d4bd60c257
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270120"
---
# <a name="create-a-new-product-hierarchy"></a>Vytvoření nové hierarchie produktu


[!include [banner](includes/banner.md)]

Tento článek popisuje, jak vytvořit novou hierarchii produktů v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Dynamics 365 Commerce podporuje více maloobchodních sítí. Tyto maloobchodní kanály zahrnují online obchody, kontaktní střediska a maloobchody (neboli kamenné obchody). Každý kanál maloobchodu může mít vlastní metodu plateb, cenové skupiny, pokladny na pokladních místech (POS), účty příjmů a výdajů a zaměstnance. Všechny tyto prvky je třeba nastavit pro maloobchod před vytvořením kanálu maloobchodu. 

Hierarchie produktů Commerce se používá, chcete-li definovat celkovou hierarchii produktů pro organizaci. Hierarchii produktů Commerce lze použít pro výrobní události, tvorbu cen a promoakce, sestavy a plánování sortimentu. Organizaci může být přiřazen pouze jedna hierarchie produktů Commerce.

## <a name="create-and-configure-a-product-hierarchy"></a>Vytvoření a konfigurace hierarchie produktu

Chcete-li vytvořit a konfigurovat novou hierarchii produktů Commerce, postupujte dle těchto kroků.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Produkty a kategorie \> Hierarchie produktů Commerce**.
1. Pokud dosud žádná hierachie neexistuje, vyberte v **Podokně akcí** možnost **Nový** a vytvořte kořenový adresář hierarchie.
1. V **Obecné**:
    1. Do pole **Název** zadejte název.
    1. Zadejte popis do pole **Popis**.
    1. Do pole **Popisný název** zadejte popisný název produktu.
    1. Nastavte **Aktivní** na **Ano**.

## <a name="add-hierarchy-nodes"></a>Přidání uzlů hierarchie

Chcete-li přidat uzly hierarchie, postupujte podle následujících kroků.

1. V podokně akcí vyberte možnost **Upravit hierarchii kategorií**.
1. Vyberte nadřazený uzel, do kterého chcete přidat nový uzel, a poté vyberte **Nový uzel kategorie**.
1. V části **Obecné** zadejte **název**, **popis**, **popisný název** a **klíčová slova**.
1. V **Obecné**:
    1. Do pole **Název** zadejte název.
    1. Zadejte popis do pole **Popis**.
    1. Do pole **Popisný název** zadejte popisný název produktu.
    1. Do pole **klíčová slova** zadejte příslušná klíčová slova.
    1. V poli **Pořadí zobrazení** zadejte číslo pořadí zobrazení (volitelné).
1. V podokně akcí vyberte **Uložit**.
1. Zopakováním výše uvedených kroků přidejte další uzly.

V následujícím obrázku je znázorněno vytvoření nového uzlu hierarchie produktů.

![Vytvoření hierarchie produktu.](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Další nastavení

Skupiny atributů kategorií lze podle potřeby přiřadit ke každé skupině.  

## <a name="additional-resources"></a>Další zdroje

[hierarchie obchodu](retail-hierarchies.md)

[Správa kategorií produktů a produktů](category-management-product-creation.md)

[Změna pořadí řazení pro entity podpory prodeje](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

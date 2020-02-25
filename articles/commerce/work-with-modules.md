---
title: Práce s moduly
description: V tomto tématu jsou popsány důvody, kdy a jak používat moduly v aplikaci Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
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
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025872"
---
# <a name="work-with-modules"></a>Práce s moduly

V tomto tématu jsou popsány důvody, kdy a jak používat moduly v aplikaci Microsoft Dynamics 365 Commerce.


[!include [banner](includes/banner.md)]

## <a name="overview"></a>Přehled

Moduly jsou logické stavební bloky, které tvoří strukturu stránek a mají různé účely a zaměření. Některé moduly jsou kontejnery vysoké úrovně a jejich jediným účelem je obsahování a uspořádání dalších modulů (podřízených modulů). Ostatní moduly, jako je například jednoduchý modul umístění obrázku, mají velmi specifický účel. Mezi těmito dvěma kategoriemi patří i jiné moduly, například karuselový modul.

Ve výchozím nastavení váš web Dynamics 365 Commerce obsahuje knihovnu modulů startovní sady, která umožňuje dosáhnout většiny základních scénářů e-Commerce. Pomocí pouze těchto modulů by mělo být možné vytvořit komplexní web e-Commerce. Můžete však také přizpůsobit tyto moduly nebo sestavit nové, vlastní moduly pro specifické potřeby. Chcete-li vytvořit vlastní moduly, je k dispozici sada SDK (Software Development Kit), která usnadňuje vytvoření vlastní knihovny modulů.

## <a name="container-modules-and-slots"></a>Moduly a sloty kontejneru

Jak bylo zmíněno dříve, některé moduly jsou navrženy pro uchovávání podřízených modulů. Tyto moduly jsou označovány jako *kontejnery* a umožňují hierarchie vnořených modulů. Kontejnerové moduly obsahují *sloty*. Sloty se používají k obsluze rozvržení a účelu podřízených modulů v kontejneru. Příkladem může být základní modul kontejneru stránky (modul nejvyšší úrovně pro libovolnou stránku), který definuje několik důležitých slotů:

- Slot záhlaví
- Slot obsahu
- Slot zápatí

Vývojář modulu definuje tyto sloty a určuje, které podřízené moduly a kolik podřízených modulů je možné přímo do ní vložit. Například slot záhlaví může podporovat pouze jeden modul typu **Modulu záhlaví**, zatímco slot obsahu může podporovat neomezený počet modulů typu (kromě jiných modulů kontejneru stránky).

V nástrojích pro vytváření obsahu nemusí autoři stránek předem vědět, které moduly lze a nelze vložit do jednotlivých slotů. Když autoři stránek vybírají slot a pak se pokusí vybrat modul, který se má přidat, uvidí filtrované zobrazení typů modulů, které jsou pro daný slot podporovány.

## <a name="content-modules"></a>Moduly obsahu

Moduly obsahu obsahují obsah a multimediální prvky, například text (například nadpisy, odstavce a odkazy) nebo odkazy na materiály (například obrázky, video a PDF). Příklady typických typů modulů obsahu jsou **Hero**, **Funkce** a **Banner**. Moduly těchto tří typů mohou obsahovat text nebo média a nevyžadují žádné podřízené moduly, aby je bylo možné zobrazit na stránce.

Většina typických, každodenních aktivit vytváření stránek a obsahu zahrnuje moduly obsahu, především proto, že tyto moduly definují skutečný obsah, který je vykreslený v nadřazených modulech kontejnerů. K dispozici je mnoho modulů obsahu a tyto moduly jsou obvykle posledními částmi, které přidáte do hierarchie vnořených modulů.

Následující ilustrace znázorňuje, jak jsou moduly vnořené v nadřazených slotech modulu kontejneru.

![Vnoření modulů](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Přidat nebo odebrat moduly

Následující postupy popisují způsob přidávání a odebírání modulů.

### <a name="add-a-module"></a>Přidat modul

Chcete-li přidat modul do slotu nebo kontejneru na stránce, postupujte podle následujících kroků.

1. V podokně osnovy vlevo vyberte kontejner nebo slot, do kterých lze přidávat podřízený modul.

    > [!NOTE]
    > Návrhář modulů definuje seznam typů modulů, které lze přidat do určitého slotu modulu. Autoři šablon pak mohou vylepšit povolené možnosti modulu, aby zajistily konzistentní optimalizaci vyhledávače (SEO) a efektivitu vytváření pro všechny stránky, které jsou vytvořeny z určité šablony.

1. Vyberte tlačítko se třemi tečkami (**...**) pro modul a poté vyberte možnost **Přidat modul**. Zobrazí se dialogové okno **Přidat modul**. Toto dialogové okno je automaticky filtrováno, takže zobrazuje pouze moduly, které jsou podporovány ve vybraném kontejneru nebo slotu. Seznam modulů je určen šablonou stránky nebo definicí modulu kontejneru.

    > [!NOTE]
    > Pokud kontejner nebo slot nepodporuje nové podřízené moduly, nebude možnost **Přidat modul** k dispozici.

1. V dialogovém okně vyhledejte a vyberte modul, který chcete přidat na svoji stránku.

    > [!TIP]
    > **Funkce** a **Hero** jsou dobrými typy modulů pro začátečníky.

1. Výběrem tlačítka **OK** přidáte vybraný modul do vybraného kontejneru nebo slotu na stránce.

### <a name="remove-a-module"></a>Odebrání modulu

Chcete-li odebrat modul ze slotu nebo kontejneru na stránce, postupujte podle následujících kroků.

1. V podokně osnovy vlevo vyberte tlačítko se třemi tečkami vedle názvu modulu, který chcete odebrat, a pak vyberte tlačítko odpadkového koše.
1. Až budete vyzváni k potvrzení odebrání modulu, vyberte **OK.**

## <a name="configure-modules"></a>Konfigurace modulů

Následující postupy popisují způsob konfigurace modulů obsahu a kontejneru.

### <a name="configure-a-content-module"></a>Konfigurace modulu obsahu

Chcete-li konfigurovat modul obsahu na stránce, postupujte podle následujících kroků.

1. V podokně osnovy vlevo rozbalte stromovou strukturu a vyberte libovolný modul obsahu (například **Funkce**, **Hero** nebo **Banner**).
1. V podokně vlastností vpravo vyhledejte ovládací prvky s obsahem a nastavením modulu.
1. Zadejte vlastnosti pro jakékoli požadované ovládací prvky modulu.
1. Na příkazovém řádku vyberte možnost **Uložit**. Tím se také obnoví plátno náhledu.

### <a name="configure-a-container-module"></a>Konfigurace modulu kontejneru

Chcete-li konfigurovat modul kontejneru na stránce, postupujte podle následujících kroků.

1. Vyberte na stránce kontejnerový modul (například modul karuselového nebo tekutého kontejneru).
1. V podokně vlastnosti vpravo rozbalte vnořené ovládací prvky výběrem záhlaví a nastavte požadované hodnoty ovládacích prvků.
1. V podokně osnovy vlevo vyberte tlačítko se třemi tečkami vedle názvu kontejneru nebo slotu uvnitř kontejneru a pak vyberte **Přidat modul**. Poté přidejte do vybraného kontejneru podřízené moduly. Další informace naleznete v oddílu [Práce s moduly](#add-a-module) dříve v tomto tématu.
1. Pokud existuje více podřízených modulů v nadřazeném kontejneru na stejné úrovni, můžete změnit pořadí jejich zobrazení v nadřazeném kontejneru. Vyberte tlačítko se třemi tečkami pro modul a pak použijte tlačítka se šipkou nahoru a dolů.

## <a name="additional-resources"></a>Další zdroje

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Práce se šablonami](work-with-templates.md)

[Práce s přednastavenými rozloženími](work-with-layouts.md)

[Práce s fragmenty](work-with-fragments.md)

[Přidání modulu kontejneru na stránku](add-container-module.md)

[Práce s publikovacími skupinami](publish-groups.md)

